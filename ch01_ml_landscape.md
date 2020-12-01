# Hands-On Machine Learning with Scikit-Learn, Keras, and TensorFlow
Author: Géron, Aurélien.

### Chapter 1 - Machine Learning Landscape

1. How would you define Machine Learning? 
Building systems that can learn from data. Learning means getting better at some task, given some performance measure.

2. Can you name four types of problems where it shines?
Great for complex problem with no algorithmic solution, for problems with fluctuating environments, help humans learn (data mining), replace hand-tuned rules.

3. What is a labeled training set? 
A training set that contains the desired solution/label/output for each instance/output.

4. What are the two most common supervised tasks? 
Regression and classification. 

5. Can you name four common unsupervised tasks? 
Clustering, anomaly detection, dimensionality reduction, visualization, association rule learning.

6. What type of Machine Learning algorithm would you use to allow a robot to walk in various unknown terrains?
Reinforcement learning

7. What type of algorithm would you use to segment your customers into multiple groups? 
Clustering if groups are not defined yet. If they are, then classification algorithm (supervised learning).

8. Would you frame the problem of spam detection as a supervised learning problem or an unsupervised learning problem? 
Supervised problem normally and learning is performed once spam emails are labeled.

9. What is an online learning system? What is out-of-core learning? What type of learning algorithm relies on a similarity measure to make predictions? 
Learning system that is able to incorporate learning from new data incrementally, as opposed to batch learning system. Out of core learning means the algorithm can handle large data that cannot fit into one computer memory. It chops data into mini batches and uses online learning techniques. 
An instance-based learning system learns training data by heart and when given a new instance, it uses similarity measure to find the most similar learned instances and uses them to make predictions.

10. What is the difference between a model parameter and a learning algorithm’s hyperparameter? What do model-based learning algorithms search for? What is the most common strategy they use to succeed? How do they make predictions?
Model parameters determine how the model will predict new instances. A hyperparameter is a parameter of the learning algorithm itself, not of the model. 
Model-based algorithms search for optimal value of the model parameters so it can generalize well to new instances. Usually done by minimizing a cost function + a penalty if regularization is used. 

11. Can you name four of the main challenges in Machine Learning? 
Lack of data, unrepresentative data, biased data (poor data quality) , models that underfit (too simple) or overfit (too complex).

12. If your model performs great on the training data but generalizes poorly to new instances, what is happening? Can you name three possible solutions?
That means the model is overfitting the training data. Solution is to reduce data, reduce model complexity through more regularization or using lower order terms, or remove features that are not important. Reducing noise in training data is another alternative.

13. What is a test set, and why would you want to use it? What is the purpose of a validation set? 
Test set is used to estimate the generalization error the model makes on new instances. It's only allowed to run once. 
A validation set is used to compare models. It allows comparison of model and tuning of hyperparameters.

14. What is the train-dev set, when do you need it, and how do you use it?
A train-dev set is used when there is a risk of mismatch between training data and data used in validation and test. The train-dev set is part of the training set that's held out. The model is trained on the rest of the training set and evaluated on both the train-dev set and the validation set. 
If the model performs well on the training set but not on the train-dev set, then the model is likely overfitting the training set.
If the model performs well on both training and train-dev set, but not on validation datasetm there is probably a mismatch between training data and validation + test data. 
We should try to improve the training data so that it looks more like validation + test data. 

15. What can go wrong if you tune hyperparameters using the test set?
We risk overfitting the test set, and the generalization error we measure may be underestimated.