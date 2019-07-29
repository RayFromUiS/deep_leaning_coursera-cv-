# Deep Learning tutorial(....continuing)

This is repo for totebook and reminder for my learning curve of Coursera specialization ['Deep learning'] (https://www.coursera.org/specializations/deep-learning? "Deep learning").
It is composed with such 5 courses,
1. Neural Networks and Deep Learning
2. Improving Deep Neural Networks
3. Structuring Machine Learning Projects
4. Convolutional Neural Networks
5. Sequence Models
Flowing will be notes and erros which i made and correct through corresponding courses
## Course1,Neutral networks and deep learning

## Course2,Improving Deep Neural Networks
Three weeks needed to cover this course, initialization,gradient checking, and regulization 
are covered in the first week. Then week two introduce optimization function, followed with 
thrid week of tensorflow tutorial for a multi-class assignment.
Three ipynb notebook homework need to be coded.
* week 1,initialization,gradient checking and regulization
  * initialization
  Three initializaiton method is compared based on a data classification problem.
   1. Zeros initialization which basically  setting "zeros" in the input argument.
    loss function is barely learning with such weight as zeros, which produce a barely learning line.
    symmetry is not broken down with such initialization method
   2. Random initialization,the weights to large random values.
    symmetry is interrupted and each neuron is leaning differently.
   3. He initialization .
    > Best way of initial for relu activation
  * gradient checking
  **Instructions**:
- First compute "gradapprox" using the formula above (1) and a small value of $\varepsilon$. Here are the Steps to follow:
    1. $$ \theta^{+} = \theta + \varepsilon $$
    2. $$ \theta^{-} = \theta - \varepsilon $$
    3. $$ J^{+} = J(\theta^{+}) $$
    4. $$ J^{-} = J(\theta^{-}) $$
    5. $$ gradapprox = \frac{J^{+} - J^{-}}{2  \varepsilon} $$
- Then compute the gradient using backward propagation, and store the result in a variable "grad"
- Finally, compute the relative difference between "gradapprox" and the "grad" using the following formula:
$$ difference = \frac {\mid\mid grad - gradapprox \mid\mid_2}{\mid\mid grad \mid\mid_2 + \mid\mid gradapprox \mid\mid_2} \tag{2} $$
You will need 3 Steps to compute this formula:
   - 1'. compute the numerator using np.linalg.norm(...)
   - 2'. compute the denominator. You will need to call np.linalg.norm(...) twice.
   - 3'. divide them.
- If this difference is small (say less than $$10^{-7}$$), you can be quite confident that you have computed your gradient correctly. Otherwise, there may be a mistake in the gradient computation. 
  

## Course4,Convolutional Neural Networks

* week 1, fundation of con neural networks
 * genreal
 Introduct the process of how to convolutionlize a ready to train matrix,Using the filter,
Which will covert origianl matrix accordingly. Also key concepts have been explained, such as
padding,stride,poolling and most importantly, the dimension controling over the whole dataset.
In case of same, might maintain the dimension of training example dimentsion, while valid,usuallly
reduce the dimensionlity of training matrix.
 * programming assignment
 For this assignment, it mainly about how to construct a con network for scraching.

* week2, Case studies
 * general
   In this week's study, several conv network strutuce has been involved,such as Resnet,Inception 
   network,and other pretrained well-known network, vgg16,vgg19 and so on.
 * programming assignment
 A Resnet 50 has been stacked from stratch.
