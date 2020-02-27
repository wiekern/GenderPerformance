# Gender Effect in social media platforms
Our project is an extension of https://github.com/Sandipan99/amazonReview

Goal: study gender effect on perceived helpfuness of reviews depending on the gender of authors

# Datasets
1. Yelp: https://www.yelp.com/dataset
2. Reddit: http://files.pushshift.io/reddit/comments/
3. StackExchange: https://data.stackexchange.com/

# How to use
1. Place your dataset under the folder `datasets/DATASETNAME` where DATASETNAME is the folder name you give.
2. Clean your dataset by one of ipynb files with suffix `Dataset.ipynb`, obtaining datasets for training, test and validation.
3. Go to the folder `models/HAN`, executing `preprocess.py` to preprocess the datasets
4. Go to the folder `models/GRU`, executing `RNN_model_batch.py` to train the model. After the training is done, run `inference.py` to infer the gender labels for the undisclosed dataset.
5. Open `MajorityVoting.ipynb`, apply majority voting on predicted undisclosed dataset
6. Open `SentimentReadabilityLengthCal.ipynb` to analyze review's sentiment, length, readability. Four datasets produced, Signaling Man (SM), Signaling Woman (SW), Performing Man (PM), Performing Woman (PW)
7. Open `NaturalExptCategory(not_pairwise).ipynb` to find matches for each pair group of (SM, SW), (SM, PM), (SW, PW). After matches of each pair group found, analyzing the helpfuness score to get a conclusion.
