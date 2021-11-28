# HackerEarth-ML-Challenge-Nov-2021
Credit card default risk is the chance that companies or Individuals will not be able to return the money lent on time.

<strong>Task</strong>
<p>I had been given relevant information about the customers of a company.&nbsp;</p>
I had to build a machine learning model that can predict if there will be credit card default.


<strong>Task</strong>

<h3>An Overview of Solution</h3>
our data contains columns:
customer_id	name	age	gender	owns_car	owns_house	no_of_children	net_yearly_income	no_of_days_employed	occupation_type	total_family_members	migrant_worker	yearly_debt_payments	credit_limit	credit_limit_used(%)	credit_score	prev_defaults	default_in_last_6months	credit_card_default

In feature engineering, I first go to gender columns contains two class labels "M" and "F". so, I have just replaced with 1 for "F" and 0 for "M".
same in owns_car and owns_house if "Y" then replacing with 1 and "N" with 0.
then, I had checked null values across all columns.
no_of_children          774
no_of_days_employed     463
total_family_members     83
migrant_worker           87
yearly_debt_payments     95
credit_score              8
then, I just replaced the null values with mean. 
for training, I have just removed customer_id, name.
I didn't removed occupation_type column because it will effect on result.
for occupation type, I have create dummies and added up in original dataset. 
I have used svm because for final result "credit_card_default" column we need binary classification.
