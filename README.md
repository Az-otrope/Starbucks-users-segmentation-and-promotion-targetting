# Starbucks-Offers-and-Users-Demographics
- [Motivation](#Project-Motivation)
- [Installation](#Installation)
- [Results](#Results)
- [Discussion](#Discussion)
- [Licensing, Authors, Acknowledgements](#License)

## Project Motivation <a name="Project-Motivation"></a>

**Background:** This data set contains 1-month simulated data that mimics customer behavior on the Starbucks rewards mobile app. The dataset entails customers’ input information, spending habits, and transactions made on the app.
Starbucks sends out an offer to users of the mobile app every few days. Some users may receive offers frequently, some may not for a while. The offers are presented in 3 ways:
Discount: user gains a reward equal to a fraction of the amount spent
BOGO (buy one get one free): user needs to spend a certain amount to get a reward equal to that threshold amount
Informational: an advertisement for a drink or product
Not all users receive the same offer, and not all purchases are made using offers. That makes data wrangling a big challenge for this dataset.

**The goal** of this project is to combine transaction, demographic, and offer data to determine which demographic groups respond best to which offer type.

## Installation <a name="Installation"></a>
The following packages and versions are used in this jupyter notebook. Any newer versions should work. 
| Package  | Version |
| ------------- | ------------- |
| Python  | 3.8.5  |
| Pandas  | 1.1.3  |
| Numpy   | 1.19.2 |
| Matplotlib | 3.3.2|

## Results <a name="Results"></a>
Based on the extensive EDA, two groups of customers were found to be responsive to offers and likely to make a purchase (convert).
**Male Adult**:
- most responsive (received, viewed) to offers
- is also currently the target audience to receive many offers compared to other genders in all age group
**Female Adult**:
- most likely to make a purchase using offers (completed)
- Type of offers: We can continue to send out discounts and BOGO since they drive customers’ buying decisions. The reward value also excites customers.
- The source of offers that highly correlates with conversion rate is the website. Here is the cue that we should focus on optimizing the presentation of offers on the Starbucks homepage.

## Discussion <a name="Discussion"></a>
More sophisticated strategies could be employed to achieve a higher conversion rate among Starbucks customers. Uplift modeling can be used to identify the right customer group for a specific promotion. The uplift model method of "two classifiers" can be used. The process will consist of two steps:
1. Conduct a randomized A/B test, in which the treatment group of customers receives and offers and the control group does not. Train classifiers to predict the likelihood (probability) of conversion for both groups. Add two classifiers into one using a special library (upliftML , casualML). Use a combined classifier on the entire customer base to identify customers with high conversion probability.
2. Conduct a second A/B test, in which the treatment group is customers with a high conversion probability receive promo offers and the control group consisting of random customers also receive promo offers. Calculate lift as the difference in total conversion or total amount spent.

This method allows for more quantitative customer segmentation and promo offerings, rather than qualitative, human-decision-based strategies.

## Licensing, Authors, Acknowledgements <a name="License"></a>
* Starbucks for providing the datasets and project goal
* [Udacity](https://www.udacity.com/) for instructions
* The main findings and results of this project can be found in this [post](https://medium.com/@nguyenpham111/starbucks-promotional-offers-how-they-influence-customers-buying-behaviors-57e62ca2c0f5)
* Author: [Nguyen Pham](https://github.com/Az-otrope)
