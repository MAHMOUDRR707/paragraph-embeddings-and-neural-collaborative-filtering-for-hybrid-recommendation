# paragraph-embeddings-and-neural-collaborative-filtering-for-hybrid-recommendation

One of the popular approaches for making recommendations is collaborative filtering.
Despite matrix factorization's efficiency for collaborative filtering, the inner product operator, which combines the linear multiplication of latent characteristics, might not be enough to capture the intricate structure of user interaction ratings.
However, we contend that there is a significant gap between user ratings and actual interest preferences.

A brand-new hybrid recommendation system is what we suggest. It uses neural networks, which have a high level of non-linearity for capturing the intricate structure of user interaction ratings, to take advantage of user-item evaluations for collaborative filtering.

Additionally, it makes use of item embeddings to capture the content feature for auxiliary data, partially resolving the cold start issue.

In specifically, we develop two neural networks to capture the sentiment of user reviews and the content feature of things, and we use paragraph embeddings to represent user reviews and item descriptions.

Then, in order to build the hybrid recommendation system, we treat these embeddings as attention weights for users and items and combine them with user-item ratings.

Extensive testing on the Amazon product dataset shows that our method outperforms other cutting-edge algorithms in terms of rating prediction.

## Methodology
We present the UTER hybrid recommendation model. Its framework mainly consists of three components:

(1) The input module offers and initializes the embedding representation of user reviews and item descriptions, which are pre-trained on user reviews and item descriptions using paragraph vectors, respectively. The input module also uses one-hot encoding  to initialize user and item input, which is high-dimensional and sparse binary vectors converted from the user–item ratings. 

(2) The hybrid recommendation module is constructed for better recommendation quality. It combines the one-hot encoding of users and items, text embeddings of user reviews and item descriptions to unify a hybrid recommendation model .

(3) The rating prediction module aggregates the hybrid representation by fusing different embeddings in the neural network, and then outputs the prediction score of the user–item pair
 We can also stack more nonlinear layers to improve the recommendation performance, because stacking more hidden layers can bring a high degree of nonlinearity to optimize model parameters.


