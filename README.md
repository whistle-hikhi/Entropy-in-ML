# Entropy in ML

Entropy in machine learning is a measure of uncertainty or randomness in a system. It originates from information theory and helps in understanding the distribution of information in a dataset. In decision trees, for instance, entropy is used to decide how well a split on a feature separates the classes.

The formula for entropy (H) is:
<p align="center">
$H(S) = - \sum_{i=1}^{n} p_{i}log_{2}(p_{i})$
</p>
  

Where:
- $S$ is the dataset
- $p_{i}$ is the probability of class $i$
- $n$ is the total number of unique classes

The lower the entropy, the less the randomness (or uncertainty) in the dataset. For example, if a dataset contains all samples from one class, its entropy is 0 (no randomness).
On the other hand, if the samples are equally divided among different classes, the entropy is higher, indicating more randomness.

## Entropy in Decision Tree

In decision trees, entropy is used to select the feature that provides the maximum information gain (i.e., the best split). The information gain is calculated as the difference between the entropy of the parent node and the weighted average entropy of the child nodes.

Information Gain (IG) is calculated as:

<p align="center">
$IG(S, A) = H(S) - \sum_{v\in Values(A)} \frac{|S_{v}|}{|S|} H (S_{v})$
</p>

Where:
- $A$ is the attribute being considered for spliting
- $S_{v}$ is the subset of date fro which attribute $A$ has value $v$
- $H(S)$ is the entropy of the original set
- $H(S_{v})$ is the entropy after the split
