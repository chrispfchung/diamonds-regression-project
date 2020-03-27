# Predicting Diamond Prices with Multiple Linear Regression

## In this project we predict the price of diamonds using a dataset containing 54,000 data points. Data includes diamond price and the following 9 features:
- Carat
- Clarity
- Cut
- Color
- Depth
- Table
- X (length)
- Y (width)
- Z (depth)

# We also perform EDA and test two hypotheses based on our findings:
### Hypothesis Test 1 - Do people pay extra for a little more Carat? Carat Weight vs. Price
**Our Curiosity**: We have heard that there is a significant increase in price when the carat hits 2. Are people spending much more to hit the 2 carat breakpoint? We split up the diamonds by carat right before 2 carat (1.9-1.999) and compared it to the average prices of 2-2.1 carat diamonds.<br>

**Null Hypothesis** : There is no significant difference between the price of diamonds of weights 1.9-2 and weights 2-2.1.<br>
**Alternate Hypothesis** : There is a significant difference between the price of diamonds of weights 1.9-2 and weights 2-2.1.<br>
*Alpha value* = 0.05

P-value is less than our alpha value of 0.05, therefore:
Reject the null hypothesis meaning there is a statistically significant difference between the prices of diamonds weighted 1.9-2 and weights 2-2.1.<br>
*Inference*:
Carat weight is the most critical predictor of price, it appears that the weight of 2 is a significant point where the value rises.


### Hypothesis Test 2 Cut vs. Clarity
**Scenario**: If someone went to buy a wedding ring for their partner, would the person look for the best cut? The best clarity? We wanted to find out if a diamond with the best cut is more expensive than one with the best clarity.<br>
**Null Hypothesis** : There is no significant difference between the price of diamonds with the best cut and diamonds with the best clarity.<br>
**Alternate Hypothesis** : There is a significant difference between the price of diamonds with the best cut and diamonds with the best clarity.
<br>
*Alpha value* = 0.05


p_value = 2.744688067675461e-10, reject null hypothesis<br>
P-value is less than our alpha value of 0.05, therefore:
Reject the null hypothesis meaning there is a statistically significant difference between the prices of diamonds with the best cut and diamonds with the best clarity.<br>
*Inference*:
The best cut diamonds have a higher price on average and are more valuable than diamonds with the best clarity.

# We run a multiple linear regression 
Our first model performed very well on the training and testing dataset. We decided not to create another model. Our results:

Train R2: 0.9806005580054734
<br>
Test R2: 0.9804433773941287
<br>
<br>
Train Root Mean Squared Error: 0.018207304797526316
<br>
Test Root Mean Squared Error: 0.01841116334943573

![actualvpredicted](https://github.com/chrispfchung/diamonds-regression-project/blob/chris-chung/images/actualvspredicted.png)

![bestfeaturesplot](https://github.com/chrispfchung/diamonds-regression-project/blob/chris-chung/images/bestfeaturesplot.png)

# Best Features Interpretation
Our strongest features are Carat and IF Clarity.<br>
**Carat Interpretation**: For every 1 increase in Carat, the price increases by 18%. <br>
**IF Clarity Interpretation**: If the diamond has IF clarity, the price increases by 15%.<br>


# Business Inferences for Seller:
- A high grade color may not increase the diamond value, but having a lower grade color will actually decrease it.
- Diamond cut doesn’t have a significant effect on the diamond value either positively or negatively.
- Carat has the highest influence on the diamond’s value. 
- All clarity grades have the second highest influence on the diamond’s value.

# Business Inferences for a Budget Buyer
- Buy under 2 carats as the price of a diamond just under 2 is significantly less.
- If you want the largest diamond for your money, and that’s the only parameter of interest, then look for a high carat diamond with a low grade color and clarity.
- Cut doesn’t influence the price as much as the other qualities.

**BEST DEAL**:    
- Low grade clarity, low grade color, any cut, under 2 carats.


