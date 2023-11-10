# I310D-Assignment-3
<h1> Bias and Fairness Assessment of Models </h1>

For this assignment, I examined a dataset of internet comments and their scores, in addition to formulating my own queries and using the Perspective API client to score the toxicity of online comments. 

Documentation for the Perspective API can be found <a href="https://developers.perspectiveapi.com/s/?language=en_US">here</a>. 
Since the API gives scores between 0 and 1, I set the threshold to 0.5 and considered any probability above 0.5 as toxic and below 0.5 as non toxic.

<h2> Hypothesis </h2> 
Perspective will be less accurate when there are common obscenities in a comment.

<h2> Methods </h2>
Toxic comments were derived from a dataset found on Kaggle from https://www.kaggle.com/datasets/areeves87/rscience-popular-comment-removal along with some comments that I came up with myself. 
I developed my own (small) test set of 30 example comments, documented the model scores and labels extracted from the model using the threshold of 0.5 and saved these data in a csv file that was uploaded into a Google Colab Notebook. Here the column toxic represents whether or not the Perspective Probability met the threshold of 0.5. If the comment went above the threshold, the comment was given the classification True under the column toxic. If not, the comment was given the label False. The column y represents the actual toxicity of the comments.

<h2> Findings </h2>
For Class 0 Obscene comments, the Perspective API seems to suffer from low-accuracy at detecting toxicity. This strengthens my hypothesis that Perspective will be less accurate when there are common obscenities in a comment because the lowered accuracy for the Class 0 Obscene comments indicates that although the comment was non-toxic, Perspective still classified this comment as toxic.

Additionally, Perspective had low-accuracy in detecting Class 1 Clean comments for toxicity which allowed toxic comments without obscene language to not be detected.

This may point to the fact that obscene or common swear words are more easily detected and flagged without the machine having to understand the underlying nuances of language for detecting toxic language. This could point either ways as obscene language could lead to false positives in detecting toxic comments while Class 1 Clean comments could lead to false negatives of letting potentially toxic comments go undetected.


