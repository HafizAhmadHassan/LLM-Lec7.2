# Lec5 :  Zero Shot vs Few Shot Learning 
- Transformations of GPT version

Papers:
    1. GPT: Attention all u need contain encoder : long range dependencies
    2. GPT1: Self Supervision : no encier key Generative pre-training and unlabeled text. OpenAI also have blog about results. combined transformers and unsupervised learning.Commercial space had not heard about this.
    3. GPT2: Language Models : they introduced GPT2 Architecture and with Large parameters.
    4. GPT3 : 175B parameters big boom . Emotional recognition. Answers lot of parameters
    5. GPT3.5 introduced after
    6. Now we have GPT4o

Zero Shot : unseen task ability to generalise them without any context

Example: Translate sentence english to french
cheese =>

OneShot : one example of task

Few Shot: Learning from minimum examples:

sea otther => loutre de mer
peppermint => something
cheese => ?

GPT3 was few short learner it can do. use autoregressive

GPT4 is few shot learner and it can even do zero shot learning but few shot is main thing.

Datasets:
CommonCrawl: free open rego 250 billion pages web crawl 410 billion pages they have 60% data
WebText : covering Reddit submission from 2005 . 22% data
Book1
Book2 
Wikipedia

Token is unit of text which model reads for now think 1 token is 1 word

Total pretraining cost 4.6 million dollars

What happens in Pretraining?