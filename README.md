# Support Vector Machine

### Introduction 

Support Vector Machine algorithm is used to find a hyperplane in an N-dimensional space, with N being the number of features, that classifies data points. <br>

People tend to use this model for its simplicity and vercitility.<br>

For instance to separate the 2 classes of data points, there are many possible hyperplanes that could be chosen. The goal is to find a plane that has the max margin, meaning the maximum distance provides some reinforcement so that future data points can be classified with more confidence.<br>

### Hyperplanes and Support Vectors

**Hyperplanes:** are decision boudaries that help classify the data points. Data points either on the hyperplane can be attributed to different classes. The diemnsion of the hyperplane depends on the number of features. For instance id the input features is 2, then the hyperlane is a line (1D), or if it's three then the hyperlane become 2-demensional, etc... <br>

Support vecotors are data points that are closer to the hyperplane and influence the position and orientation of the hyperplane.

### Large Margin Intuition

In logistic regression, we take the output of the linear function and squash the value within the range of [0,1] using the stigmoid Function. If the value is greater than a centrain thereshhold then it becomes 1, if it's less it becomes 0. In this model we take the output of the linear function and it it is greater that 1, we identify it with one class and if it is -1, we identify it with another class. 

### Cost Function
This algorithm maximizes the margin between the data points and the hyperplane. The loss function that margin is hinge loss function defined as: ``` c(x,y, f(x)) = (1-y*f(x))₊``` <br>

The cost is 0 if the predicted value is the actual value. If not then we calculate the loss value as follows: ```min𝑤 λ ||𝑤||² + Σ(1-𝑦𝑖 <x𝑖, 𝑤>)₊``` <br>

we take partial derivatives of the function above with respect to the weights and find the gradient  using the gradient we can update the weigts to get the final gradient update of ```𝑤 = 𝑤 + ⍺ (𝑦𝑖 * x𝑖 - 2λ𝑤)``` <br>

### Implementation of Support Vector Machine

Please look at the supporting python file [here](SVM.py).

### Sources

- [Towards Data Science](https://towardsdatascience.com/support-vector-machine-introduction-to-machine-learning-algorithms-934a444fca47)
