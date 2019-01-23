# Vaaku2Vec
State-of-the-Art Language Modeling and Text Classification in Malayalam Language
---



## Results
We trained a malayalam langiage model on the wikipedia article dump from Oct, 2018. The wikipedia dump had 55k+ articles. The difficuly in training a malayalam language model is text tokenization since [Malayalam is a highly inflectional and agglutinative language.](https://thottingal.in/blog/2017/11/26/towards-a-malayalam-morphology-analyser/). In the current model we are using nltk tokenizer(will try better alternative in the future) and the vocab size is 30k. The language model was used to train a classifier which classify a news into 5 categories(India, Kerala, Sports, Business, Entertainment). Our classifier came out to have a whooping 92% accuracy in the classification task.  


## Releases

- Wikipedia processed data with train and test split.
- Code and weights for Malayalam Language model.
- Malayalam text classifier with pretrained weights.
- Inference code for text classifier.

## Downloads
- [**Pretrained Language Models**](https://www.dropbox.com/sh/a9wmsg5cjpzmyg1/AABmyHP-4bLmqrwJSB5-KeU1a?dl=0) 

- Raw Data for Language Model shared above: [Malayalam Wikipedia](https://dumps.wikimedia.org/mlwiki/latest/mlwiki-latest-pages-articles.xml.bz2) 
- [Wikipedia Processed Data]() - please use this to train your model

## Requirements

### Installing dependencies
python3.6+ fastai==0.7

If you are using virtualenvwrapper use the following steps:
1. mkvirtualenv -p python3.6 venv  
2. workon venv
3. pip install -r requirements.txt

## Training language model with  preprocessed data:

1. Create tokens:  
 `python lm/create_toks.py <path_to_processed_wiki_dump>`  
eg: `python lm/create_toks.py /home/adamshamsudeen/mal/Vaaku2Vec/wiki/ml/`
2. Create a token to id mapping:  
 `python lm/tok2id.py <path_to_processed_wiki_dump>`  
eg: `python lm/tok2id.py /home/adamshamsudeen/mal/Vaaku2Vec/wiki/ml/`
3. Train language model:  
`python lm/pretrain_lm.py <path_to_processed_wiki_dump> 0 --lr 1e-3 --cl 40`  
`eg: python lm/pretrain_lm.py /home/adamshamsudeen/mal/Vaaku2Vec/wiki/ml/ 0 --lr 1e-3 --cl 40`  
`lr` is the learning rate and `cl` is the no of epochs.
 





### TODO
- [x] Language modeling based on wikipedia dump
- [x] Release Language Models: [Malayalam Language Model]()
- [x] Train Text classifier
- [ ] Benchmark with [mlmorph](https://gitlab.com/smc/mlmorph) as tokenizer.
- [ ] Benchmark with [Byte pair encoding as tokenization](https://nlp.h-its.org/bpemb/ml/)



#### Thanks

**Special thanks to Sebastian Ruder and Jeremy Howard and other contributors to [fastai](https://github.com/fastai/fastai)**. 
