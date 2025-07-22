# Lec4 : Transformers
- most LLMS rely on the transformers architecture
- schemantic of transfers?
- embeddings?

Secrect Sauce :
    - LLM are transformers
    - deep neural netwrok architecture - Attention is all you need : Research Paper
    - This paper let tso many architectures
    - GPT originated from this paper
    - very important to undersand this paper
    -

Today just overview:
    - It was introduced to translation task
    - English to German and French

Schemantics:
    - page 3 of article
    - 8 steps:
    LHS:
        - prompt english language : ""
        - tokenization : sentences split to individual words or subwords and assign id to each token
        - encoder : preprocessed text: passed to it which will do vector embeddings : represent it with sementic meanings for example : I will convert dog and bear to its id's : 
        - Embedding Vectors : can I somehow tell dog and bear are close to each other this is what embeddings do : see in Lecture Picture representation : Fruits (apple , banana close to each other), (Man, Women), Neural network trained for that .. Encoder does that
        huge number of dimension space sp sementic meanings captures. IT is giant dimension space there are more visuals shown
    RHS:
        - Decoder (German Translator): we can get partial output remember model complete one word at time by the time we reach last output the previous outputs will be available to model For example :
        I give prompt : "This is example" Model doing translation "Das est ein" this is available to model "example words is not generated" : The magic here is Das est ein will also pass to decoder again as input
        now Decoder recived Partial output and Embeddings from embeding vector --> So decorder will give final output "Das est ein Beispiel"

Transformer Simply neural network and we update some layers of it

Blocks:
    Encoder : input text to embeding vecotrs
    Decoder : Generate output from embedding vectors + partial output of itself

GPT Arch:
    - its differrent it does not have encoder

Key Part:
    Self Attention Mechanism:
        - Allows to model : dependencies between different words without regards to how close and far are the words apart 
        - Allows Model to : weight importance of different words/ tokens relative to each other Lets say : Harry porter in next to station - when I predict "station" the previous context is important for me i.e the importance of previous words : which words should be given more more attention
        
        Blocks : Multi-Head Attention in architecture
        - Enables model to capture long range dependencies

Later Variation:
    BERT : Bidirectiontional encoder representation from Transformers : predicts hidden words - it mask some words and try to predict.. fill words
        Steps : Input --> Preprocessing --> Encoder
    GPT : Generative Pretrained Transformers : predicts next word - we just have to predict next words
        Steps : input --> Preprocessing --> Decoder
    
    Look the the pricture on Lecture

    Why Bert is Good in Sentimental Analysis :
        - Bert Look sentence on both direction whereas GPT on one direction
        e.g Bert can differentiate betweem bank and financial institute and Bank with riverBank

Both of them have Transformers in them


Transformers vs LLM's
    - Not all transformers are LLM's
    - Transformers can also be used for Computer Vision
    - also for language
    - Check viso.ai :
        - Medical

 ViT vs CNN (viso.ai)
    - ViT is weaker bias
    - gaining lot of popularity

1980 RNN : 
1997 LSTM : Two Paths Green Line Long term memory blue line short term memory
Transformers 2017

Not All LLMs are transformers
LLMs can be based on RNN or CNN architecture as well