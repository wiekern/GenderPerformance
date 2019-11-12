# Gender Performance in online communities

Goal: Analyze reviews posted by which gender subject to performative gender are more helpful in online communities like Yelp, StackOverflow etc.

# How to use
1. Clean your dataset refer to `clean_dataset.ipynb`, obtaining datasets for training, test and validation.
    1. Apply training dataset to train the RNN model
    2. Predict gender label for undisclosed dataset
    3. Apply majority voting on predicted undisclosed dataset
2. Run `SentimentReadabilityLengthCal.ipynb` to analyze review's sentiment, length, readability. Four datasets produced, Disclosed Male (DM), Disclosed Female (DF), Undisclosed Male (UM), Undisclosed Female (UF)
3. Run `NaturalExptCategory(not_pairwise).ipynb` to find matches for each pair group of (DM, DF), (DM, UM), (DF, UF), (UM, UF). After matches of each pair group found, analyzing the helpfuness score to get a conclusion.
