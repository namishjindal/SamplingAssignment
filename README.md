# SamplingAssignment
## Sampling
Sampling is a method that allows us to get information about the population based on the statistics from a subset of the population (sample), without having to investigate every individual from the population.
<br>
Before exploring different sampling techniques, a crucial preliminary step was taken to address the imbalance in our dataset. Initially, the dataset contained 763 non-fraudulent cases and only 9 fraudulent cases. To rectify this imbalance, an oversampling technique was employed. This involved creating additional instances of the minority class (fraudulent cases) to align more closely with the majority class (non-fraudulent cases). Subsequently, the balanced dataset was stored into a single data frame having shape of 1487 rows and 31 columns.
<br>
Sampling Techniques used:
- Simple Random Sampling:
   Pick the sample, at random. 

- Systematic Sampling:
   The samples are chosen at regular intervals. A random start and then proceeds with the selection of every ‘kth’ element.

- Cluster Sampling:
   The entire population is divided into smaller groups or clusters, and then a random sample of these clusters is selected.

- Stratified Sampling:
   The population is divided into subgroups or strata based on a certain characteristic or criterion.  

- Bootstrap Sampling:
   The bootstrap sampling technique employs resampling with replacement, allowing for the creation of multiple samples from the original dataset. 
<br>
After computing five distinct samples using five different techniques, I applied five models(Random Forest, Gradient Boosting Trees, Naive Bayes, Decision Trees, KNN) to each sample. The accuracies for each model for a sample are summarized in the table below:

| Sample Technique      | Logistic Regression | SVM       | Naive Bayes      | Decision Trees   | KNN              |
|-----------------------|---------------------|-----------|------------------|------------------|------------------|
| Simple Random Sampling| 0.8889              | 0.6889    | 0.7556           | 0.9222           | 0.9556           |
| Systematic Sampling   | 0.9118              | 0.6176    | 0.6373           | 0.951            | 0.9118           |
| Cluster Sampling      | 0.963               | 0.8201    | 0.9683           | 0.9735           | 0.9841           |
| Stratified Sampling   | 0.8795              | 0.7349    | 0.7349           | 0.9277           | 0.9518           |
| Bootstrap Sampling    | 0.9375              | 0.7875    | 0.7125           | 0.975            | 0.975            |

In above table, each row corresponds to a sampling technique, and each column represent the accuracy achieved by each model applied to the respective sample generated using that respective technique.
<br>
### The KNN outperformed all other models when applied to Cluster Sampling Technique.
