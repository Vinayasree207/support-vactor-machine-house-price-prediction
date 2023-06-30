# support-vactor-machine-house-price-prediction

__Introduction to SVM__

What is SVM? 
Support Vector Machines (SVM) is a supervised learning algorithm which can be used for classification and regression problems as support vector classification (SVC) and support vector regression (SVR). 
It is used for smaller dataset as it takes too long to process. 

__The Ideology Behind SVM__
SVM is based on the idea of finding a hyperplane that best separates the features into different domains. 

What is Hyperplane? 
We can draw a line in 1-D, a plane in 2-D, anything beyond is a hyperplane. 

__Intuition Development__

There is a stalker who is sending you emails and now you want to design a function(hyperplane) which will clearly differentiate the two cases, such that whenever you received an email from the stalker it will be classified as a spam. 

The following are the figure of two cases in which the hyperplane is drawn, which one will you pick and why? 

<img width="424" alt="image" src="https://github.com/Vinayasree207/avacado-price-prediction/assets/119283715/14e56c88-097c-4e43-8e71-7e333c7b8fb7">

Take a moment to analyze the situation. 

I guess you would have picked the fig(a). 

Did you think why have you picked the fig(a)? 

Because the emails in fig(a) are clearly classified and you are more confident about that as compared to fig(b). 

Basically, SVM is composed of the idea of coming up with an optimal hyperplane which will clearly classify the different classes (in this case they are binary classes). 

__Terminologies Used in SVM__

<img width="364" alt="image" src="https://github.com/Vinayasree207/avacado-price-prediction/assets/119283715/f1d9f3c4-7db7-4264-a263-54786c5bcf6b">

The points closest to the hyperplane are called as the support vector points 

The distance of the vectors from the hyperplane is called the margin. 

The basic intuition to develop over here is that farther the SV points, from the hyperplane, better__ the probability of correctly classifying the points in their respective class regions. 

SV points are very critical in determining the hyperplane because if the position of the vectors changes the hyperplane’s position is altered. 

Technically this hyperplane can also be called as margin maximizing hyperplane. 


__Hyperplane(Decision Surface)__

The hyperplane is a function which is used to differentiate between features. 

In a 2-D data, the function used to classify is that of a line. 

The function used to classify the features in a 3-D data is that of a plane.  

Beyond 3-D its a hyperplane. 

__How Does It Work?__

Above, we got accustomed to the process of segregating the two classes with a hyper-plane. 

Now, “How can we identify the right hyper-plane?”. 

__Scenario-1__: Identify the right hyper-plane 

Here, we have three hyper-planes (A, B and C). Now, identify the right hyper-plane to classify star and circle.

<img width="290" alt="image" src="https://github.com/Vinayasree207/avacado-price-prediction/assets/119283715/d3440297-269b-45cd-bbb8-d4205a9f0e83">

You need to remember a thumb rule to identify the right hyper-plane: 
 
“Select the hyper-plane which segregates the two classes best”. 

In this scenario, hyper-plane “B” has excellently performed this job. 


__Scenario-2__: Identify the right hyper-plane  

Here, we have three hyper-planes (A, B and C) and all are segregating the classes well. Now, How can we identify the right hyper-plane? 

<img width="277" alt="image" src="https://github.com/Vinayasree207/avacado-price-prediction/assets/119283715/6ace498a-0752-4739-8a4e-6a1a32f3b1b5">

Here, maximizing the distances between nearest data point (either class) and hyper-plane will help us to decide the right hyper-plane. 

This distance is called Margin. Hence, we name the right hyper-plane as C.Another reason for selecting the hyper-plane with higher margin is robustness. 

If we select a hyper-plane having low margin then there is high chance of miss-classification. 


__Scenario-3__: Identify the right hyper-plane 

<img width="294" alt="image" src="https://github.com/Vinayasree207/avacado-price-prediction/assets/119283715/8de56651-cab0-448e-a566-93b3ab25e1f1">

Some of you may have selected the hyper-plane B as it has higher margin compared to A. 

But, SVM selects the hyper-plane which classifies the classes accurately prior to maximizing margin. 

Here, hyper-plane B has a classification error and A has classified all correctly. 

Therefore, the right hyper-plane is A. 

SVM can solve this problem easily. 


__What is Kernel Trick?__

The kernel computes in a way such that when you project the 2-D data into a 3-D space, the data points close to the center of the data gets to the top and those far away from center gets into the bottom of the 3-D space. 

Types of Kernels
1. Linear Kernel 
2. Polynomial Kernel 
3. Radial Basis Function (RBF) Kernel / Gaussian Kernel 

We will be focusing on the polynomial and gaussian kernel since they are the most commonly used. 

__Polynomial Kernel__

In general, the polynomial kernel is defined as: 

𝑘(𝑥,𝑦)=(𝛼𝑥𝑡𝑦+𝑐)𝑑 

Here: 
𝛼 = Slope 
𝑐 = Constant Term 
𝑑 = Polynomial Degree of the Kernel 

In the polynomial kernel, we simply calculate the dot product by increasing the power of the kernel. 

__Radial Basis Function (RBF) Kernel / Gaussian Kernel__

Gaussian RBF (Radial Basis Function) is another popular kernel method used in SVM models. 

RBF kernel is a function whose value depends on the distance from the origin or from some point. 

Similarity is the angular distance between two points. 

Parameters: 

C: Inverse of the strength of regularization. 
Behavior: 
As the value of C increases the model overfits. 
As the value of C decreases the model underfits. 

`γ`: Gamma (used only for RBF kernel) 
Behaviour: 
As the value of γ increases the model overfits. 
As the value of γ decreases the model underfits. 

__SVR is different from SVM.__

As the name suggests SVR is a regression algorithm, so we can use SVR for continuous values instead of classification which is done using SVC. 

__Terminologies Related to SVR__

Kernel: The function used to map a lower dimensional data to higher dimensional data. 
Hyper-Plane: In SVM this is basically the separation line between the data classes. 
Although in SVR we are going to define it as the line that will help us predict the continuous value or target value. 
Boundary Lines: In SVM there are two lines other than Hyper Plane which creates a margin. 
The support vectors can be on the boundary lines or outside it. This boundary line separates the two classes. In SVR the concept is same. 
Support Vectors: These are the data points which are closest to the boundary. The distance of the points is minimum or least. 

Why SVR? What's the main difference between SVR and simple regression model? 
In simple regression we try to minimize the error rate. While in SVR we try to fit the error within a certain threshold. 

<img width="429" alt="image" src="https://github.com/Vinayasree207/avacado-price-prediction/assets/119283715/2b32378a-ccfa-4cf8-b845-cf74bb0f9247">

In the figure above, all the points are within the boundary lines. 

Our objective when we are moving on with SVR is to basically consider the points that are within the boundary line. 
  
Our best fit line is the line hyperplane that has maximum number of points. 


__Pros and Cons of SVM__
Pros: 

It is really effective in the higher dimension. 
Effective when the number of features are more than training examples. 
Best algorithm when classes are separable. 
The hyperplane is affected by only the support vectors thus outliers have less impact. 

Cons: 
For larger dataset, it requires a large amount of time to process. 
Does not perform well in case of overlapped classes. 
Selecting appropriately, hyperparameters of the SVM that will allow for sufficient generalization performance. 
Selecting the appropriate kernel function can be tricky 

__Is SVR the same as Linear Regression?__ 

SVR:  
As the output is a real number it becomes very difficult to predict the information at hand, which has infinite possibilities. 
A margin of tolerance (epsilon) is set in approximation to the SVM. 

The main idea behind it is to minimize error, individualizing the hyperplane which maximizes the margin, keeping in mind that part of the error is tolerated. 
Comes handy in case of non linear approach. 

Linear Regression: 
In statistics, linear regression is a linear approach for modeling the relationship between a scalar dependent variable y and one or more explanatory variables (or independent variables) denoted X. 
The case of one explanatory variable is called simple linear regression. 
