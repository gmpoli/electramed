# Pre-training dataset

The pre-processed PubMed texts used to pre-traing ELECTRAMed are available at the following link: [https://ftp.ncbi.nlm.nih.gov/pub/lu/Suppl/NCBI-BERT/pubmed_uncased_sentence_nltk.txt.tar.gz](https://ftp.ncbi.nlm.nih.gov/pub/lu/Suppl/NCBI-BERT/pubmed_uncased_sentence_nltk.txt.tar.gz).

The corpus consists of 28,714,373 PubMed abstracts (uncompressed, approximately 26GB), representing the whole amount of abstracts published on the free digital repository until September 2018.
In more detail, the corpus contains ~181M sentences and ~4B words and was subject to the following common NLP pre-processing steps applied by the  proponents of the dataset:
* Text lowercasing;
* Special characters (`\x00`-`\x7F`) removal;
* Text tokenization using [NLTK Treebank tokenizer](https://www.nltk.org/_modules/nltk/tokenize/treebank.html).

The corpus was made public by Peng Y, Yan S, Lu Z. [Transfer Learning in Biomedical Natural Language Processing: An
Evaluation of BERT and ELMo on Ten Benchmarking Datasets](https://arxiv.org/abs/1906.05474). In *Proceedings of the Workshop on Biomedical Natural Language Processing (BioNLP)*. 2019.