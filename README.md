# I310D-Assignment-3
<h1> Bias and Fairness Assessment of Models </h1>

For this assignment, I examined a dataset of internet comments and their scores, in addition to formulating my own queries and using the Perspective API client to score the toxicity of each comment. 

Documentation for the Perspective API can be found <a href="https://developers.perspectiveapi.com/s/?language=en_US">here</a>. 
Since the API gives scores between 0 and 1. We can set the threshold to 0.5 and consider anything above 0.5 as toxic and below 0.5 as non toxic.

<h2> Hypothesis </h2> 
INSERT HERE

<h2> Methods </h2>
Toxic comments were derived from a dataset found on Kaggle from https://www.kaggle.com/datasets/areeves87/rscience-popular-comment-removal 
I developed my own (small) test set of N example comments, documented the model scores and labels extracted from the model using the threshold of 0.5. 

<h2> Findings </h2>
Write a few paragraphs, either in the README or in the notebook, reflecting on what you have learned, what you found, what (if anything) surprised you about your findings, and/or what theories you have about why any biases might exist, if you find they exist. You can also include any questions this assignment raised for you about bias or machine learning. Questions you may wish to answer include:

- What biases do you think might exist in the model based on intuitions or public documentation about how the model was created?
- What were your results?
- What theories do you have about why your results are what they are?
