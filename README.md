Classification is a fundamental task in machine learning, where the goal is to assign input data to one of several predefined categories or classes. This technique is widely used in various applications, such as image recognition, spam detection, and medical diagnosis. Classification models learn from labeled data, making predictions by recognizing patterns and features within the input data.

The Problem with Multi-Class Classification
One of the challenges in traditional multi-class classification is that the model always makes a prediction, even when the input data does not belong to any of the predefined classes. This occurs because the softmax activation function, typically used in multi-class classification, forces the sum of the output probabilities to equal 100%. As a result, the model is compelled to select one of the classes, even when the input is irrelevant or does not contain any of the target classes.

Addressing the Issue: Potential Solutions
To overcome this limitation, several approaches can be considered:

Bayesian Neural Networks (BNNs): BNNs incorporate uncertainty into their predictions, providing a measure of confidence in the output. This allows the model to express uncertainty when the input does not clearly belong to any class. To see more about BNN : https://colab.research.google.com/drive/1Yw60JFnnsxU-4xNLkzOCci8KD49nGz8G?usp=sharing#scrollTo=_Ub9UZY1WaiV

Multi-Label Classification: Another effective solution is to reframe the problem as a multi-label classification task. In this approach, each class is treated independently, and a sigmoid activation function is used for each output neuron. This allows the model to output a probability for each class, which can then be thresholded to determine whether the class is present. This approach eliminates the issue of the model always predicting a class, as it allows for the possibility of no class being selected if all probabilities fall below the threshold. In that notebook we will explore how this approach can be applied to solve a multiclass classification problem.

# Traditional approach
 ![1](https://github.com/user-attachments/assets/139c0880-5135-4647-8975-b94c503188a3)

# Instead we will try that approach
![2](https://github.com/user-attachments/assets/ab7587af-1529-4814-8644-c39fe0cae0e3)

