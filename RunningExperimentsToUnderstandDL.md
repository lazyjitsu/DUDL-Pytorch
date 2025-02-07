# Runnin experiments to understand DL

- How to be an experimental scientist with DL!
- What a "parametric experiment" is
- How to evaluate and interpret parametric experiments

### Flavors of Scientists

Type of scientest   Description of science philsophy

Theoretical:  Ideas, theories, math (no data). Works with theories and mathematical formulas

Ecological:  Observe adn describe the real world

Experimental:  Run experiments, manipulate variables, collect data .. inferential statistics

### Flavors of DL researchers

Theoreticfal:  Heavy on theory/math development
Ecological: Use existing (pretrained) models
Experimental: Systematically modify model parameters and observe which is best


We will be experimental of course so we can learn DL. So how do we do this? By running parametric experiments

### Parametric experiments

Parametric experiment: repeating an experiment whicl systematically manipulating one or two variables.

Independent variable: The variables you manipulate (learning rate, batch size, optimizer, loss function, ...).

Dependent variable: The key outcome variable you use to evaluate model performance (accuracy, speed).

# What to conclude fro mparametric experiments

Correct interpretation of DL experiments:
- "This is the best set of parameters for this model, this architecture, and this dataset"
- "This is a general pattern that I'm likely to see in othe rmodels and other datasets"

Incorrect interpretation of DL experiments:

"This is the exact optimal parameter for every model and every dataset"  
Note: This is the difficulty with DL. One model might perform well with dataset A but not so well with dataset B

Problems with an experimental approach to DL

Feasibility: Samll or simple models are fast to compute, but large models take a long time to train and evaluate.

Generalizability: Specific findings from one model may not replicate in other architectures or other sets of parameters.

Solution: Use the experimental approach to build intuition and gain expertise about DL modeling in general.





