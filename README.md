<br />
<p align="center">
  <a href="https://github.com/gmpoli/electramed">
    <img src="images/logo.png" alt="Logo" width="80" height="80">
  </a>

  <h3 align="center">ELECTRAMed</h3>

  <p align="center">
    A new pre-trained language representation model for biomedical NLP
    <br />
  </p>
</p>



<!-- TABLE OF CONTENTS -->
<details open="open">
  <summary><h2 style="display: inline-block">Table of Contents</h2></summary>
  <ol>
    <li>
      <a href="#about-electramed">About ELECTRAMed</a>
      <ul>
        <li><a href="#built-with">Built With</a></li>
      </ul>
    </li>
    <li>
      <a href="#download">Download</a>
    </li>
    <li><a href="#datasets">Datasets</a></li>
    <li><a href="#models">Models</a></li>
    <li><a href="#license">License</a></li>
    <li><a href="#contacts">Contacts</a></li>
  </ol>
</details>



<!-- ABOUT ELECTRAMed -->
## About ELECTRAMed

**Motivation**  
The overwhelming amount of biomedical scientific texts calls for the development of effectivelanguage models able to tackle a wide range of biomedical natural language processing (NLP) tasks.
Themost recent dominant approaches are domain-specific models, initialized with general-domain textualdata and then trained on a variety of scientific corpora.
However, it has been observed that for specializeddomains in which large corpora exist, training a model from scratch with just in-domain knowledge mayyield better results.
Moreover, the increasing focus on the compute costs for pre-training recently led tothe design of more efficient architectures, such as ELECTRA.

**Results**  
We propose a pre-trained domain-specific language model, called ELECTRAMed, suited for the biomedical field.
The novel approach inherits the learning framework of the general-domain ELECTRA architecture, as well as its computational advantages.
Experiments performed on benchmark datasets for several biomedical NLP tasks support the usefulness of ELECTRAMed, which sets the novels tate-of-the-art result on the BC5CDR corpus for named entity recognition,
and provides the best outcome in 2 over the 5 runs of the 7th BioASQ-factoid Challange for the question answering task.


### Built With

* TensorFlow 1.5.3 (pre-training)
* TensorFlow 2.3.0 (fine-tuning)
* HuggingFace 3.4.0


<!-- DOWNLOAD -->
## Download

Pre-training was performed leveraging the [original ELECTRA code](https://github.com/google-research/electra) provided by Google Research.  
The corpus used for pre-training was published by [Peng _et al._, 2019](https://arxiv.org/abs/1906.05474) and consists of 28,714,373 PubMed abstracts (uncompressed, approximately 26GB), representing the entirety of PubMed until 2018.  
It is available for download in its preprocessed version [here](https://ftp.ncbi.nlm.nih.gov/pub/lu/Suppl/NCBI-BERT/pubmed_uncased_sentence_nltk.txt.tar.gz).  
For more information about how the pre-training was performed, refer to the paper.

Currently, there is only one version of the model available. Its weights, vocabulary and config files can be downloaded from the [Hugging Face model repository](https://huggingface.co/giacomomiolo/electramed_base_scivocab_1M/tree/main).  



<!-- DATASETS -->
## Datasets

ELECTRAMed was fine-tuned and tested on three biomedical NLP tasks: named entity recognition (NER), relationship extraction (RE) and question answering (QA).  
The datasets used are detailed in the paper and are made available in [electramed/data](https://github.com/gmoli/electramed/data).


<!-- MODELS -->
## Models

We will soon publish the available fine-tuned models for NER, RE and QA.


<!-- LICENSE -->
## License

Distributed under the MIT License. See `LICENSE` for more information.


<!-- CONTACTS -->
## Contacts

Giacomo Miolo - [giacomo.miolo@mip.polimi.it](giacomo.miolo@mip.polimi.it)  
Giulio Mantoan - [giulio.mantoan@mip.polimi.it](giulio.mantoan@mip.polimi.it)  
Carlotta Orsenigo - [orsenigo@polimi.it](orsenigo@polimi.it)  

<!-- ACKNOWLEDGEMENTS -->
## Acknowledgements

We thank Dr. Sandra Coecke from the Join Research Center at European Commission and Dr. Anna Beronius from Karolisnka Institute for their valuable and fruitful discussions that fostered a positive and encouraging environment which greatly contributed to the development of our work.    
We also thank the authors of ELECTRA, SciBERT and BlueBERT for making the data and codes publicly available.  
