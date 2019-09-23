# A Simplified Classification Decision Tree
## Data files
- each item has two continuous features x 2 R2
- the class label is binary and encoded as y 2 f0; 1g
- data files are in plaintext with one labeled item per line, separated by whitespace:
                                
                                |x11 |x12 |y1 |
                                | :  | :  | : |
                                |xn1 |xn2 |yn |

## My decision tree follows the following guidelines:
- Candidate splits (j; c) for numeric features should use a threshold c in feature dimension j in the form of xj >= c.
- c should be on values of that dimension present in the training data; i.e. the threshold is on training points,
not in between training points.
- The left branch of such a split is the “then” branch, and the right branch is “else”.
- Splits should be chosen using mutual information (i.e. information gain). If there is a tie you may break it
arbitrarily.
- The stopping criteria (for making a node into a leaf) are that
   * the node is empty, or
   * all splits have zero mutual information
- To simplify, whenever there is no majority class in a leaf, let it predict y = 1.

## References
Guidelines are cited from [UW-Madison CS760 Fall2019 HW2](http://pages.cs.wisc.edu/~jerryzhu/cs760.html)

Code cimplementation are based on the help from [Let’s Write a Decision Tree Classifier from Scratch](https://www.youtube.com/watch?v=LDRbO9a6XPU)
