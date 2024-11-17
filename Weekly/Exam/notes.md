What to know:

Funcions to know:
	- Forward pass
	- Loss functions
	- Activation functions
	- Confusion matrix

Combination and mutations:


Loss functions:
    - MSE
    - Cross entropy:
        -(general) = - sum[y_i * log(p_i)]
        - (binary) = - 1/n sum[y_i * log(p_i) + (1-y_i)*log(1-p_i)]



Fig 5.4 - why is idealized population from fitness share is shared evenly


Exam:
	- Non uniform mutation: Add random deviances to each variable seperately, taken from N(0, sigma) gaussian dsitribution, then curtail to range. Formula: x_i = x_i + N(0, sigma)
	- PMX
	- Go through lecture slides: briefly mentioned
	- Edge recombination
    - ML is not jsut subset of AI, but they overlap
    - 1955/1956, invented by McCarthy
    - Minima of loss function
    - Roulette: Prob of 3 inviduals with fitness: [32, 21, 13]. Prob for 21 is 21/(32+21+13)
    - Tournament: Select subset and pick fittest individuals in each k subset.
    - No rank based
    - Backprop by chain rule partial derivatives: go from end point y back to x1 in all paths.
    - Explainable AI: last 2 lectures. Using another model to explain another model. 
    - Problem with explainable AI, hidden layers/black box
    - Relu: no vanishing gradient problem
    - F1 score: harmonic mean. 2*(precision * recall)/ (precision + recall)
    - Multiple objectives: most money and least distance. We will get multiple suboptimal solutions
    - Bias variance tradeoff: high bias (more generalized) -> underfittting, high variance -> overfitting
    - 

Formulas:
    - Fitness sharing
    - Gaussian distribution, how it can affect EA
    - Losses/regression
        - Linear: mean squared error
        - Logistic: cross entropy
    - Forward pass (neural network)
    - Confusion matrix and F1
    - Tournament, roulette and rank
    - K-fold cross validation
        - Nested k fold: For tuning hyperparameters.
            - For each hyperparamter we train k models. E.g 3125 models. Models = k_inner (possible hyperparams) * k_outer (folds) * combinations
    - 



Example table:
Class 1:
True positive: 100  (row 1)
False positive:  100
True negative: 250 (diag 2 3)
False negative: 100 (col 1)

Acc = sum diagonals / sum of all = 350 / 700 = 0.5 

Prescision: TP / (TP + FP) = 100 / (100 + 100) = 0.5
Recall = TP / (TP + FN) = 100 / (100 + 100) = 0.5

F1 = 2 * 0.5 * 0.5 / 1 = 0.5


