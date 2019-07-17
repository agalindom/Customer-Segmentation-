# Overview
The notebook contains code for the final capstone project of the Udacity Data Science Nanodegree.

# Description
In order to complete the project two tasks must be achieved:
  1. From the general population, and using unsupervised learning techniques, find the group that contains characteristics of the individuals that have the most probability of being new customers for Arvato Financial Services.
  2. Using supervised learning, and using a labeled dataset, train a model that learns to distinguish individuals that are potential customers to the ones that are not.

The results of the second task are submitted to an inclass kaggle competition

# Files
Customer_segmentation.ipynb : Jupyter notebook containing the code for the project

# Libraries

 * pandas
 * numpy
 * matplotlib
 * sklearn
 * imblearn

# Results
## Unsupervised Part:
  After all the predictions were done these were the final findings regarding the two groups: Popular, refering to the characteristics of the individuals that are potential customers and Unpopular, regarding the characteristics of the people that are not potential customers.

  * For the analysis i picked ['ANREDE_KZ','HH_EINKOMMEN_SCORE', 'OST_WEST_KZ', 'wealth_encode', 'life_stage_encode', 'MOBI_REGIO'], because i believe they could give a good assesment overall of what the target must be for the mail campaign.

  * Popular

    - Anrede_kz: The difference between men and women is almost non existent.
    - Hh_einkommen_score: Persons with very high and high income.
     Ost_west_kz: People from the west.
    - Wealth_encode: Wealthy and prosperous households.
    - life_stage_encode : Mature to elder couples.
    - Mobi_regio : Very little to no movement.

  * Unpopular

    - Anrede_kz(gender): Women.
    - Hh_einkommen_score(household net income): People with average and low income.
    - Ost_west_kz: West living people.
    - wealth_encode: Poorer and less affluent households.
    - life_stage_encode : Pre-Family Couples & Singles.
    - Mobi_regio : High movility and very high movility.

  * Conclusion:

    - Popular: The best individuals to target after the unsupervised learning model can be described as mature to elder couples that have considerable income and wealth, that are well settled in one place.
    - Unpopular: The worst individuals for the company to target are pre-family couples or singles (women) that are young, don't have much income and wealth and have high movility.

## Supervised Part:
  After creating the final model architecture, i proceeded to use it and predict on the given test data, which positioned me at the 15th place in the leaderboard with an AUC score of .79930, having the top score at .8081.

# Extras
If it is of any interest to you, you can find the medium article explaining the project in the following link:
https://medium.com/@alejandrogalindomedina/unsupervised-and-supervised-learning-for-customer-segmentation-part-1-54fec0cff9e6?source=friends_link&sk=40d22c004816c95a397c5d203e8a4173
