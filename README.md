# Lec6 : Stages of Building LLMs from Scratch

Stage 1 Sebatian Rashka book:
    -building LLM
        - Data Preperation and Sample
        - Attention Mechanishm 
        - LLM architecture

    Purpose: Main mechanisam understanding 
    Tokenisation, Vector Embeddings, we need to encode every word

    Positional encoding we need to learn
    How to convert into batches of data
    Context understanding
    Data Batching Sequence implementation

    Multihead, Maskmultihead attention etc we will read


Stage 2: Foundational Model After Assemble all data
    
    - Foundational model on unlabled data
    - Training large language model scheme (in book)
    - weight saving and loading main compoment
    - we will also see open ai

    - Training Loop + Model Evaluation + Load pretrained weights


Stage 3: Fine Tuning LLM's
    - Classifier
    - Personal assistant

    - we here give specific label data
    LangChain
    Ollama

    e.g classify spanm or not spam

Recap :
    1. LLM0s field of NLP used for advancement in generation understanding and translation of human language
    2. Two main Steps
        - Training unlabled data - very large datasets needed
        - Fine Tuning on smaller lableled dataset - needed for production
        - Fine Tuned Perfomace > LLMs on specific tasks

    3. Secret Source :
        Transformer achitectre : Attention Block make it more powerful - it allows model to understand importance of the words in context and helps to predict next words

    4. Original transformer:
        - Encoder + Decor
    
    5. GPT :
        Only Decoder

    6. LLM's develop Emerging Property
        - as they are trained for next word but they can classify and translate or other tasks

