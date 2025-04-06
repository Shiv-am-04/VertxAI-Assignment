I have used two ways to Analyze and score picth deck of the start-up.

I - ***Extraction based***

  1. First is to extract the content of the PDF.
  2. I have used langchain's PyPDFLoader to extract content from the pdf.
  3. I then used two llm models deepseek and qwen-32b to analyze the pitch and score it based on their own analysis. We can also use more different models.
  4. The scoring of both the models are then provided to the gemini model for evaluation. The gemini model based on scores of both the model
     provides the final score for the pitch and also the feedback.

II - ***OCR based***

  1. First convert the pdf pages into the images using pdf2image library.
  2. I have used llama vision model to extract the text from the images and then analyze it to provide the score for the pitch. We can use more vision models alongside.
  3. Just like the previous approach the scoring of the model is then provided to the gemini model for evaluation.
     The gemini model based on score of the model provides the final score for the pitch and also the feedback.

*Improvements*

1. We can use more multiple models for scoring so that, different model thinking helps to analyze the picth more better just like multiple real investors analyze it.

2. Incorporate more better models like GPT-4o,Claude as they provides larger context size which is helpful for large pitches and also provides better accuracy.

3. Also incorporate human experts for scoring the pitch which also adds a perspective of human which can make the evaluation process more better.
