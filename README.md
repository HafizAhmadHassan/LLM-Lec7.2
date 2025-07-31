# Lec7 : Stages of Building LLMs from Scratch

**First Building Block** 
**We will implement Data Preperation and Sample** 

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

So:
    Context: Huge number of documents


    How do you prepare input text for training LLMs?
    1. splitting text into individual workd 
    2. convert tokents into token id's
    3. Encode token ids into vector representation

    Let us look at step1: tokenisation text
    - take books
    - split sentence
    - split word
    - convert token to ids
    - Token embeddings which is input to GPT

DataSet :
    Vook Edith Wharton book
    - Available free to download
    - Task to tokenise other books or list of books

Lets Code :
    - Create Tokens: read txt file and print counts and see 100 characters
    - Split we use : Re library .. regular expression
        - based on space(\s) we split \s means wherethe wide space
        - we want split comma and dot so we add [,.]|\s
        - items.strip remove wide spaces

        Removing white spaces or not?
            - depend on application and requirements
            - Good to reduce memory
            - train model to exact structure of sentence
            - for example python code generation we need spaces because our code are sensitive to that indendation matter in this case
        - we want ! -- ( ) : ? " | as seperate token
        - Now after testing we apply technique to raw text
        - we had now preprocessed variable with tokens
