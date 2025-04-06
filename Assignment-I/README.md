***I have used vetorstore to store the embeddings of the investor details.***
  
  **Reasons** : 
            
            1. The information retrieval is very fast from the vector database.
            
            2. We cannot directly the large corpus of data to the AI model because it will unable to handle it due limited context size.
            
***I then connect the llm with the retriever so that I can retrieve investor interested in start-up.***
  
  **Explaination** : 
  
       1. Since the retriever generates random data based on similarity with start-up detail but the LLM improves that random into proper format that
                    we need using the prompt provided.

       2. The llm with retriever provided the response as the list of investor that is most similar to the start-up in this way we reduce the corpus of data
                     which is now ready to directly feed into the gemini model for matching score.

***Finally I used gemini model and provide the start-up and matched investor details to it. After the model analyze the details it provide the match score and ranks them.***

*Improvements*

1. Using a more better premium vector databases like AstraDB,Pinecone which can store more embeddings with higher dimension making the
   retrieved document more accurate.
