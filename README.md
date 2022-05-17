# Constructed Datasets
***Please contact yangzhao@ibm.com if you would like to use 1k compression dataset for commercial purpose (research use is fine) ***
## 1k Annotated Compression Dataset 
 - We tokenized 1k sentences with jieba tokenizer and asked two human annotaters to label "1" or "0" for each word in the sentences. "1" refers to keeping word whereas "0" refers to deleting it.
 - [Data_Annotation-1 download](https://github.com/ExperimentCode/data/blob/main/data_annotation-1_1k.txt)
 - [Data_Annotation-1 download](https://github.com/ExperimentCode/data/blob/main/data_annotation-2_1k.txt)


## 151k pairs of sentence and compression

We herein describe how we constructed 151k pairs of sentences and compression step by step. 

### Environment setup
 - Please install the necessary packages by cloning this repo and run:

```bash
pip install -r requirements.txt 
```
 - Download [langconv.py](https://raw.githubusercontent.com/skydark/nstools/master/zhtools/langconv.py) and [zh_wiki.py](https://raw.githubusercontent.com/skydark/nstools/master/zhtools/zh_wiki.py) and put both .py files in the same directory as the following `data_processing.py` script.

### Extract pairs of sentence and headline
Extract raw data (sentence and headline) from Chinese Gigaword Third Version. Downlaod [Chinese Gigaword Third Version](https://catalog.ldc.upenn.edu/LDC2007T38) and there are four folders, i.e., ```afp_cmn```, ```cna_cmn```, ```xin_cmn```, ```zbn_cmn``` under gigawords dataset folder. Put ```afp_cmn```, ```cna_cmn```, ```xin_cmn```, ```zbn_cmn```, ```zh_wiki.py```, ```langconv.py```, ```data_processing.py``` in the same  directory. Please refer to [Chinese Gigaword Third Version](https://catalog.ldc.upenn.edu/LDC2007T38) for details of these folders. 
 - step 1: Extract tirst sentence and headline of each news article.
 - step 2: Clean text by removing non-English text and strange punctuation.'
 - step 3: Remove all sentences containing tradictional Chinese chracters as there were a lot of parsing errors for tradictional Chinese words, which will affect dependecy tree transformation a lot.
 - step 4: Tokenize the headline and the first sentence using jieba within the Stanza NLP pipeline to identify content words through part-of-speech tags.
 - step 5: Filter out the cases where length requirement is not satisfied according to the rules in Appendix A of the paper.

Run `data_processing.py` to implement step 1-5.
```bash
python data_processing.py 
```

After the above processing, you will get two output files in the same directory, ```data_s_parse.txt``` and ```data_h_parse.txt```, the parsed sentences and parsed headlines. 

### contructed pairs of sentence and deletion-based compression


