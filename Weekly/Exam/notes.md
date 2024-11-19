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
    - Problem with explainable AI, hidden layers/black box and might learn on wrong things such as dogs on snow background
    - Relu: no vanishing gradient problem
    - F1 score: harmonic mean. 2*(precision * recall)/ (precision + recall)
    - Multiple objectives: most money and least distance. We will get multiple suboptimal solutions
    - Bias variance tradeoff: high bias (more generalized) -> underfittting, high variance -> overfitting
        (5-6 QUESTIONS!!)


    - 
    - Multiclass vs multilabel
    - philosphy: chinese argumetn, turing test, areas of philosphy
    - history of AI: SVM (support vector machine) classification 
    - What is GAN: generator and discriminator
    - Acc on unbalanced data sets is not good metric
    - Ridge and lasso regression: lambda * sum(w_i**2), lambda * sum(w_i)

    Philoshpy
    - weak vs strong AI
    - Turing test
    - chinese room argument (ai is weak)
    - classical (human ability to see patterns/reason) vs techincal (practical application)
    - Dreyfus Critique AND frame problem (problem determine which aspects of a situation is relevant)
    - Connections
    - SVM: classification mainly, seperates data points with hyperlane.
    - Encoder/decorder
    - Harder to interpret better/complex models.
    - Bias we have as a society will be reflected in AI, because the way we collect data. E.g use of certain words between genders, use in CV.
    

    Lecture:
    - With replacement we have less selection pressure, witout = more selection pressure
    - suppose you are tuning hyperparameters with nested k-fold using gridsearch. k=10
    Q: approx how many models will it train in total if 2 hyperparameters are each tested with 4 different values.
    4 * 4 = 16 combinations times outer and inner loop: 10*10 -> 16*10*10 = 1600

    - 4 values of each params: 

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
    - In a cross-validation experiment, the models accuracy fluctuates significantly across folds. You hypothesize that this is due to variance in class distribution between training and test folds. Which method could help mitigate this this issue?
        A: Increasing the number of folds in cross-validation
        b: Using stratified k-fold cross-validation
        C: Reducing the complexity of the model
        D: Addint more data to each fold 
    Answer: B, by stratifing we balance the classes proporting evenly across the folds

    - Q: Suppose a model AUC - ROC score is 0.85. What does this imply about the models ability to rank predictions?
        A: It has an accruarcy of 85% in classification
        B: It correctly ranks a random positive example higher than a random negative example 85% of the time
        C: it has high precision
    Answer: B, roc is about proportion of TP against FP.


    - Q: a regularized linear regression model uses an L2 penalty with a reg param lambda = 0.5. If lambda is increased to 1, which of the folloing changes is most likely to occur?
        A: The model complexity increases
        B: The weights (coeffeicents) decrease, reducing model variance
        C: The model becomes less interpretable due to sparsity
        D: The model starts discarding irrelevant features by setting coefficients to zero
    Answer: B, ridge regularization reduce variance. (L1 makes some zero)



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


