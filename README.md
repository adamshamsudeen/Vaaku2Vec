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
- [**Pretrained Language Models**]() 

- Raw Data for Language Model shared above: [Malayalam Wikipedia](https://dumps.wikimedia.org/mlwiki/latest/mlwiki-latest-pages-articles.xml.bz2) 
- [Wikipedia Processed Data]() - please use this to train your model


### TODO
- [x] Language modeling based on wikipedia dump
- [x] Release Language Models: [Malayalam Language Model]()
- [x] Create Text classifier
- [ ] Benchmark with [mlmorph](https://gitlab.com/smc/mlmorph) as tokenizer.
- [ ] Benchmark with [Byte pair encoding for tokenization](https://nlp.h-its.org/bpemb/ml/)



#### Thanks

**Special thanks to Sebastian Ruder and Jeremy Howard and other contributors to [fastai](https://github.com/fastai/fastai)**. 
