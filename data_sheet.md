## Data Sheet for the German Credit Dataset


### 1. Motivation

**Why was this dataset created?**
To enable the development and benchmarking of machine learning models for credit risk evaluation.

**Who funded or created the dataset?**
The dataset originates from the UCI Machine Learning Repository, contributed by Professor Hans Hofmann.

**What tasks is it designed to support?**
Binary classification: predicting whether a loan applicant is a good or bad credit risk.



### 2. Composition

**What does each instance represent?**
Each row represents a loan applicant described by 20 features.

**How many instances are there?**
1,000 rows (examples).

**What are the features?**
Credit history, loan purpose, employment duration, personal status, existing credit, etc.

**What is the target label?**
Binary label: 1 (good credit) or 0 (bad credit).

**Are there missing values?**
No explicit missing values are reported.

**Is it imbalanced?**
Yes — about 70% good credit, 30% bad credit.

**Sensitive features present?**
Potentially — such as personal status and employment type.



### 3. Collection Process

**How was the data collected?**
Compiled from actual loan applications by a German bank. 

**Was consent obtained?**
Not specified.

**Timeframe of data collection?**
Exact dates not provided — likely pre-2000s.

**Sampling strategy?**
Not explicitly mentioned.

**Has it been preprocessed?**
Some variables were converted from categorical to numerical formats.


### 4. Preprocessing & Labeling

**What preprocessing was done?**
- Encoding of categorical features
- Scaling numeric fields
- Target variable reformatted to 0 and 1

**Label source?**
Inferred from loan repayment performance

**Was manual labeling required?**
No


### 5. Uses

**What can the data be used for?**
- Credit risk scoring
- Binary classification model development
- Model fairness analysis

**Risks?**
- Model bias if sensitive features are not addressed
- Not generalisable beyond German applicants

**Appropriate for production?**
With caution and ethical review.



### 6. Distribution

**Where can it be found?**
[UCI Repository - German Credit Data](https://archive.ics.uci.edu/ml/datasets/statlog+(german+credit+data))

**License?**
Open for academic and research purposes.

**How is it maintained?**
Static dataset; not updated.



### 7. Contact

**Maintainer:** UCI Machine Learning Repository

**Point of Contact:** https://archive.ics.uci.edu/ml/about.html
