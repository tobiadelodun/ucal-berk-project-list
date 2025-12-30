**Coupon Acceptance Analysis**
_Project Overview_

This project analyzes customer acceptance behavior for different types of coupons using a real-world survey dataset. The objective is to identify which demographic, behavioral, and contextual factors are associated with higher coupon acceptance rates, with a particular focus on Bar and Coffee House coupons.

The analysis applies structured data cleaning, exploratory data analysis (EDA), and targeted subgroup comparisons to surface actionable insights that could inform personalized, context-aware coupon delivery strategies.

_Problem Statement_

The core business question addressed in this project is:

Which customer segments are more likely to accept specific coupon types, and under what conditions?

_More specifically:_

How does prior venue visitation frequency impact coupon acceptance?

Do demographics such as age, income, occupation, and passenger composition influence acceptance?

Are there meaningful behavioral differences between Bar and Coffee House coupon acceptance?

_Repository Structure_
.
├── README.md
└── coupon_acceptance_analysis.ipynb

Data Preparation

Key preprocessing steps include:

Explicit handling of missing values:

Categorical variables filled using modal values

Numeric variables filled using medians

Rows with missing target values (Y) removed

_Feature engineering:_

Conversion of frequency categories into numeric approximations

Derivation of age midpoints from categorical age ranges

Creation of behavioral and demographic indicator variables (e.g., passenger type, occupation groupings)

All transformations are performed using idiomatic pandas patterns and avoid chained assignment issues.

_Key Findings_
Bar Coupons

Acceptance rates are significantly higher among individuals who visit bars more than once per month.

Younger drivers and those not traveling with children show greater responsiveness.

Occupations outside farming, fishing, and forestry exhibit higher acceptance.

Combining behavioral and demographic conditions yields substantially higher acceptance rates than the baseline.

Coffee House Coupons

Acceptance is highest among frequent coffee drinkers.

Drivers traveling alone or with other adults are more likely to accept.

Acceptance decreases noticeably when children are present, suggesting coffee stops are viewed as personal or social activities rather than family-oriented ones.

_Recommendations_

Based on the analysis, the following actions are recommended:

Target Bar coupons toward:

Frequent bar visitors

Younger demographics

Drivers without children as passengers

Target Coffee House coupons toward:

Regular coffee drinkers

Solo drivers or adult-only passenger groups

Avoid broad, untargeted coupon delivery, especially for family-oriented trips where acceptance likelihood is lower.

_Next Steps_

Potential extensions of this analysis include:

Applying logistic regression or tree-based models to quantify feature importance

Testing interaction effects between income, age, and frequency variables

Incorporating temporal and geographic features (time of day, destination proximity)

Evaluating model-driven coupon personalization strategies

_Tools & Libraries_

Python

pandas

seaborn

matplotlib

Jupyter Notebook
