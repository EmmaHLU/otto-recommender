# otto-recommender

##Project Description
This project (otto-recommender) is to predict the user's next action(click, add to cart, or order)on a very large set of items. To perform the time series sequence-to-sequence prediction, Otto-recommender uses the transformer encoder architecture and was trained based on a large-scale real-world dataset known as OTTO (https://github.com/otto-de/recsys-dataset). 

##Some key features of the dataset (OTTO) are:
1. 12M real-world anonymized user sessions
2. 220M events, consiting of clicks, carts and orders
3. 1.8M unique articles in the catalogue

##Technique details:
Data Preprocessing Pipeline: filter out items with low frequency --> encoding--> split data w.r.t. sequence length --> train/test split
The transformer encoder uses 4 layers with 4 multiple heads.
Negative sampling is used to compute the Loss function, defined as cross entropy.
NDCG is used to measure the effectiveness of this ranking system.
