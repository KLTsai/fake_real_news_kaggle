# fake_real_news_kaggle
<b>purpose: Classifying the news</b>

- Preparation for the True.csv and Fake.csv files in the ../data folder
  - Notebook was worked on <b>Windows OS</b> and <b>Python 3.8.12</b>
  - Cells provide a few directions and approaches that can help readers to understand how it works
  - Kaggle data sources: https://www.kaggle.com/clmentbisaillon/fake-and-real-news-dataset
  - Summary is on the end of the notebook

# Model selection
- Using Pipleline with <b>TF-IDF</b> (Referance: https://kavita-ganesan.com/tfidftransformer-tfidfvectorizer-usage-differences/#.Yhgei-hKh1c) and <b>machine learning models</b> 

- Showcases following down below (source code and referance are adapted from links):
    - Random forest
        - https://github.com/SushwanthReddy/Fake-News-Detection-using-Machine-Learning
        - https://github.com/RamyaVidiyala/Fake-news-classifier
    - Logistic Regression <b>(baseline)</b>
        - https://github.com/martentyrk/FakeNewsDetection
    - LSTM 
        - https://www.kaggle.com/parvezsohail/classification-of-fake-news-with-lstm
        - https://leemeng.tw/shortest-path-to-the-nlp-world-a-gentle-guide-of-natural-language-processing-and-deep-learning-for-everyone.html
 
# Summary

By comparing models performance with Random Forest(RF), Logistic Regression(LR), and Regression, Long-Short Term Memory(LSTM), I have tried to use ROC Curves [1] to demonstrate how good model these are.

- In this case, I choose Random Forest rather than decision tree since Random Forest models have resulted in significant improvements in prediction accuracy as compared to a single tree by growing ’N’ number of trees; each tree in the training set is sampled randomly without replacement [2]. Besides, it was one of non-linear classifiers that apply fake news detection [3]. 


- Logistic Regression is one of generalized linear models [4] which can compare to Random Forest(non-linear classifier). It was also applied fake news detection [5]. Meanwhile, I would like to understand how performance they are between Logistic Regression and Random Forest. Therefore, I regard Logistic Regression as the baseline model.


- LSTM is a specific recurrent neural network (RNN) architecture and it has the potential to outperform standard RNNs for textual data of different lengths [7]. For LSTM, it has been frequently used for solving Natural language processing (NLP) problems. As a result, I would like to use deep learning model to compare to maching learning models. 


- The reason why I consider the value of AUC rather than accuracy or f1-score is that the it visualizes the quality of the ranker or probabilistic model on a testing set, without committing to a classification threshold [8][9].


You can discover this work regarding binary classifier, ROC and AUC values in machine learning classifiers(Random Forest and Logistic Regression) are slightly different, but Logistic Regression is still better than Random Forest. In addition, LSTM performance(0.997) is given by AUC metric, it outperforms other classifiers obviously.

# Referances
[1].https://scholar.smu.edu/datasciencereview/vol1/iss3/9/ </br>
[2].https://link.springer.com/article/10.1023/a:1010933404324 </br>
[3].https://www.anjs.edu.iq/index.php/anjs/article/view/2306 </br>
[4].https://online.stat.psu.edu/stat504/lesson/beyond-logistic-regression-generalized-linear-models-glm </br>
[5].https://www.ijeat.org/wp-content/uploads/papers/v9i1/A2633109119.pdf </br>
[6].https://www.sciencedirect.com/science/article/pii/S1877050920300806 </br>
[7].https://ieeexplore.ieee.org/document/8701258 </br>
[8].https://en.wikipedia.org/wiki/Receiver_operating_characteristic </br>
[9].https://link.springer.com/chapter/10.1007/3-540-44886-1_25
