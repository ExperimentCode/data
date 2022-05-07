## Constructed Datasets
***Both datasets are used for research purpose only***
### 1k Annotated Compression Dataset 
 - We tokenized 1k sentences with jieba tokenizer and asked two human annotaters to label "1" or "0" for each word in the sentences. "1" refers to keeping word whereas "0" refers to deleting it.
 - [Data_Annotation-1 download](https://github.com/ExperimentCode/data/blob/main/data_annotation-1_1k.txt)
 - [Data_Annotation-1 download](https://github.com/ExperimentCode/data/blob/main/data_annotation-2_1k.txt)


### 151k Parallel Training Dataset
- construction of 151k training data requires 
Once you download [Chinese Gigawords Third version](https://catalog.ldc.upenn.edu/LDC2007T38), you can reproduce the 151k pairs of sentence and compression following our [data construction procedure](https://github.com/ExperimentCode/code/blob/main/README.md#code-for-constructing-151k-data). Alternatively, you may download the [model](https://github.com/ExperimentCode/model) we trained using 151k pairs of sentence and compression without accessing the Chinese Gigawords corpus. 
