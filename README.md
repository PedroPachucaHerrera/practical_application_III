## Practical Application III: Comparing Classifiers

Overview: In this practical application, the goal is to compare the performance of the following classifiers K Nearest Neighbor, Logistic Regression, Decision Trees, and Support Vector Machines. We will utilize a dataset related to marketing bank products over the telephone.


this implementation is based on the CRISP-DM methodology, Our dataset comes from the UCI Machine Learning repository


# Business understanding 

The data is from a Portugese banking institution and is a collection of the results of multiple marketing campaigns. 

The business goal is to find a model that can explain if a client subscribes to a deposit. Such model can increase campaign efficiency by identifying the main characteristics that affect success, helping to better manage the available resources (e.g. phone calls, time) and selection of a high quality and affordable set of potential buying customers.

# Data understanding 

The data is related with direct marketing campaigns of a Portuguese banking institution. The marketing campaigns were based on phone calls. Often, more than one contact to the same client was required, in order to access if the product (bank term deposit) would be ('yes') or not ('no') subscribed. 

![image](https://github.com/PedroPachucaHerrera/practical_application_III/assets/39275405/12c1a1a6-4f40-48ff-8316-f70fa67a64b8)

- Dataset contains 41,188 entries and 21 columns including targeted variable
- Dataset has not missing values
- Dataset contains 11 numerical variables (including taregeted variable)
- Dataset contains 10 categorical variables
- Dataset contains 12 duplicated entries which were removed 

# Data preparation

Firts step was to see a correlection map to undertnad the fetuare correlation 

![image](https://github.com/PedroPachucaHerrera/practical_application_III/assets/39275405/ee24bee8-2b84-4ea5-914e-8817d7a17cdc)

Findings

Based on the correlation Matrix, 'duration' has the stronges positive coorelation with the targeted variable and 'previus' has the second larget correlation, it is importnat to notice that "nr.employed", "euribor3m" and "pdays" have significant negative correlation with the targeted variable

next step was to run histograms to see the data distribution, below is just one example of the histogram of one feature

![image](https://github.com/PedroPachucaHerrera/practical_application_III/assets/39275405/d811602e-63ca-432d-985c-0eaf809425f8)

Findings

Based on the above plots, the data is distributed for most columns except for duration, campaign, pdays and previous. We are going to keep this records intact for now until further analysis.

Next Step

We will now review the relationship of the tareted variable and all the categorical columns, below is one example of the plots

![image](https://github.com/PedroPachucaHerrera/practical_application_III/assets/39275405/6d01bb5b-8556-4451-9716-74d4f32efe76)

Findings

Based on the Box plots, only Job, Month and POutcome are the only three categorical features that have direct relationship with Outcome of user subscribing to bank's cd.

before we  build a basic model, we must work to encode the data. Using just the bank information features (columns 1 - 7), prepare the features and target column for modeling with appropriate encoding and transformations

![image](https://github.com/PedroPachucaHerrera/practical_application_III/assets/39275405/ce5b11be-515b-48bc-877b-f2c477e9ab27)


# Modeling

Fisrt step is to stablish a baseline model as a reference, the baseline score from this base model is 0.882. we will compare subsequen models to this based model.

using default setting four models are created : Logistit regression, Decision Tree, and SVM, yielding the below resuts:


# Evaluation

# Deployment 

