https://www.kaggle.com/c/instacart-market-basket-analysis

After selecting products through the Instacart app, personal shoppers review your order and 
do the in-store shopping and delivery for you.

Currently they use transactional data to develop models that predict which products a user will buy again, 
try for the first time, or add to their cart next during a session. 

Use this anonymized data on customer orders over time to predict which previously purchased products 
will be in a user’s next order.

Takeaways: 

3rd place:
https://github.com/sjvasquez/instacart-basket-prediction

The task was reformulated as a binary prediction task: Given a user, a product, and the user's prior purchase history, 
predict whether or not the given product will be reordered in the user's next order.

In short, the approach was to fit a variety of generative models to the prior data and use the internal representations 
from these models as features to second-level models.

11th place:
User-Product pairs:
The probability of user-product pair is predicted by LightGBM model. 
The model is trained with all training data + part of priors data. 
Limited to my ram, I add the last 2 prior orders of every user, which boosts my score about 0.001. 
Adding the last 3 or 4 prior orders may help to get a better score.
