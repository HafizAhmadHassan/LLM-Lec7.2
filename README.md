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

- Pre Training?
training large on diverse dataset
its about understanding human semantics

- they are called base models or foundational models
- these models can be used to fine tuning : served specific purpose of your company data

- Many LLM's pretrained are available open sourced

- check Open Source vs closed source model 
Check Graph in Video
 Green line open source is comparative to GPT

LLAMA (open source): performace bit better you can still continue with LLAMA


- GPT Architecture : only consist of decoding block it is scaled up version of transformer model. Implemented on 2018 paper. 

why it is Autoregressive?
    next word is prediction for gpt thats why see visual in Lecture
    sentence itself is input output because we do not give label

Other tasks: translation, spell correction etc

because of autoregressive token creation takes lot of computation time so its costs alot. thats why it is self supervised learning

High level notion:

Input block of words ==> next word
Input block of words ==> predicted word

Goal minimise (predicted word,next word) distance so we update weights

175Billion parameters are weights of GPT

Autoregressive : previous output is used as input for future prediction

Pretraining:
Unsupervised, Autoregressive model

- GPT input text only passd to decoder.

Transformaer :6 encoder - decoder blocks

GPT : 96 transformer layers and 196 Billion parameters

Visualise Iteration : check lecture 
iteration#1 , iteration#2 , iteration#3

why it also capable of doing translation?
    - it is called emerging behaviour

Technically GPT is not able to produce MCQ's but it does

- Emergent Behaviour
    - Search google scholar emerging behaviour is one of best topic 