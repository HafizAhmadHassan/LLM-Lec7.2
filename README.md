# Lec7cd  : Stages of Building LLMs from Scratch

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
    
    - Now convert tokens to id for numerical representation
        - token id is numerical representation
        - create vocab
            - list of unique words or tokens in alphabetical order
            - each token is mapped to number (look lecture for visual)
        
        Python implementation:
            - sorted(set(preprocessed))
            - vocab_size
        create Dictionary:
            - key: value pair word:vlaue in alphabetical order
            - enumerate take all words in alphabetical order assigned integer to it
            - Result: Vocabloury think of this process as encoder
            - Decoder is opposite of encoder which is 
    
    - Create Class of Tokenisation in Python 
        - we have vocab
        - we are doing reverse mapping
        - It will have two methods :
            - encoder : input text --> split based on space (words) --> assigned numbers
            - decoder : reverse of encoder re.(sub) : the fox chased . --> the fox chased.
        - create instance by passing vocab as input
        - apply method .encode covert to ids
        - tokenzer.decode take ids as input it covert to original text back

    - Hello is not in Vocab so what we will do in encode
        - so encoding in it is problem

    - SimpleTokenizerV2: Special Context Token to deal with
        - Let say we have fox chased the dog
        - unk - unknown token 783
        - endoftext - 784
        - document1 endoftext token -  document2 endoftext token -  document3 endoftext token
        - used between text end of particular segment
        - between different books we have to add
        - extend python command to add on vocabloury
        - we saw last 5 text
        - there are changes in encoder part
        - we make sample test and saw the outputs in notebooks.
    - Other BOS - begining of Sequence
            EOS - Ending of Sequence
            PAD - Padding
    - GPT3 do not use aboce mentioned tokens whereas these tokens were previously mentioned
        - Byte pair tokenization : words into subword units



