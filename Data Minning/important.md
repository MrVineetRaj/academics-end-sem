# Important Topics

## Unit 3

- Support confidence , lift , association rules

  - Definition, formula numerical & differences
  - No -> MLD , STACK

- Apriori & FP- growth algo ( _Numerical , diff, steps_ )

- Bagging & Boosting & Stacking

---

## Unit 4

- Naive Bayes -> numerical - ml
- KNN -> numerical - ml
- Confusion Matrix - all four definition their meaning
- Decision tree - numerical ml
  Cross validation - ml

---

## Unit 5

- DBSCAN
- K means
- Hierarchical
  - Single Linkage
  - Complete Linkage
- Numerical for all along with definition

---

_`Note : Revisit topics from MID sem`_

---

# Overview

### **Unit III: Association Rules and Algorithms**

#### **Support, Confidence, Lift, and Association Rules**

1. **Definitions and Formulas**

   - **Support**: Measures how frequently an itemset appears in the dataset.  
     **Formula:**

     - Support(A) = Frequency of transactions containing A / Total transactions

   - **Confidence**: Measures the likelihood of B being purchased when A is purchased.  
     **Formula:**

     - Confidence(A → B) = Support(A ∩ B) / Support(A)

   - **Lift**: Determines the strength of association between items.  
     **Formula:**
     - Lift(A → B) = Confidence(A → B) / Support(B)

2. **Numerical**: Practice support-confidence-lift examples like market basket analysis (e.g., milk, bread, butter).
3. **Differences**: Highlight when each measure is most useful.

#### **Apriori and FP-Growth Algorithms**

1. **Definitions**
   - **Apriori**: Uses a candidate generation approach, pruning unqualified itemsets.
   - **FP-Growth**: Uses a compact data structure (FP-Tree), avoiding candidate generation.
2. **Numerical Example**: Solve itemset generation step-by-step for both algorithms.
3. **Differences**: Efficiency, memory usage, and dataset size.

#### **Bagging, Boosting, and Stacking**

1. **Definitions**
   - **Bagging**: Reduces variance by training multiple models on random subsets and averaging outputs (e.g., Random Forest).
   - **Boosting**: Sequentially builds models where each corrects the errors of the previous ones (e.g., AdaBoost).
   - **Stacking**: Combines predictions of multiple models using a meta-model.
2. **Comparison**: Efficiency, ensemble type, and impact on bias/variance trade-off.

---

### **Unit IV: Supervised Learning and Evaluation**

#### **Naive Bayes**

1. **Definition**: Probabilistic classifier using Bayes' theorem.
2. **Numerical**: Solve using:  
   \[
   P(A|B) = \frac{P(B|A) \cdot P(A)}{P(B)}
   \]
   Example: Classify spam emails based on word probabilities.

#### **K-Nearest Neighbors (KNN)**

1. **Definition**: Instance-based learning algorithm that uses distance metrics.
2. **Numerical**: Classify points based on K neighbors (distance calculations).

#### **Confusion Matrix**

1. **Definitions and Importance**
   - **True Positive (TP)**: Correctly predicted positive cases.
   - **True Negative (TN)**: Correctly predicted negative cases.
   - **False Positive (FP)**: Incorrectly predicted as positive.
   - **False Negative (FN)**: Incorrectly predicted as negative.
2. **Metrics**:
   - **Accuracy**: \((TP + TN) / (TP + TN + FP + FN)\)
   - **Precision**: \(TP / (TP + FP)\)
   - **Recall**: \(TP / (TP + FN)\)
   - **F1-Score**: \(2 \cdot \frac{\text{Precision} \cdot \text{Recall}}{\text{Precision} + \text{Recall}}\)

#### **Decision Tree**

1. **Definition**: Uses splitting criteria like Gini index or entropy.
2. **Numerical**: Solve using ID3 algorithm, calculating information gain or Gini index for splitting.

#### **Cross-Validation**

1. **Definition**: A method to evaluate model performance by splitting data into training and test sets.
2. **Key Variants**: k-fold, leave-one-out, stratified k-fold.

---

### **Unit V: Clustering Algorithms**

#### **DBSCAN**

1. **Definition**: Density-based clustering algorithm.
2. **Numerical**: Solve based on ε (radius) and MinPts (minimum points in neighborhood).

#### **K-Means**

1. **Definition**: Partition-based clustering method.
2. **Numerical**: Solve iteratively by calculating centroids.

#### **Hierarchical Clustering**

1. **Definitions**:
   - **Single Linkage**: Distance between two clusters is the smallest distance between any point in one cluster and any point in the other.
   - **Complete Linkage**: Distance is the largest distance between points in two clusters.
2. **Numerical**: Solve using dendrograms.

---

### **Summary**

For each topic:

1. **Understand the definitions and key formulas**.
2. **Practice numerical examples**, ensuring clarity on what is being asked.
3. Highlight differences and connections between algorithms (e.g., Apriori vs FP-Growth, Bagging vs Boosting).

This approach will help with clear conceptual and practical understanding across all units. Let me know which topic you'd like to dive deeper into!
