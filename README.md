# machine-learning-challenge
Exoplanet Classification
Submitted by Farshad Esnaashari

For the Exoplanet Exploration the project goal is to explore modeling techniques that can classify Exoplantes according to the inputs (features) that are provided in the raw data.  
I used the following modeling techniques:

1. Support Vector Classifier, also known as the Support Vector Machine
2. Basic Neural Network with one hidden layer
3. Deep Neural Network with an additional hidden layer

The following activities performed:

I. Prepared the data:
    1. Read the CSV file into a DataFrame
    2. Examined the data for the relevant features 
    3. Removed features (inputs) that deemed irrelevant to the outcome, e.g., error columns
    4. Removed the labels column
    5. Using scikit-learn libraries, performed the following:
        a. created two sets of data: training, and test (validation) sets from the raw data
        b. Normalizated and scaled data ( I used MinMax scaler)
        c. Encoded data using one_hot_encodiung
II. Create a Support Network Classifier
    I used Support Vector Classifier to create a model and examined the scores using train and test data sets. 
    Score using training data = 0.79
    Score using test data = 0.78

    I then tuned the model using GridSearchCV.  The tuning improved the model slightly.   
    
    Tuned score using training data = 0.80
    Tuned score using test data = 0.79

    Best parameters for tuning:  C= 10, gamma = : 0.0001
    Best score after tuning = 0.80

    Finally, I used the tuned model to predict the first 5 outcomes.   
Conclusion:  A Tuned Support Vector Classifier is easy to setup and can classify Exoplanets with a high degree of accuracy.

III. Create a Neural Network
    I setup two Neural Networks:  Basic (Normal), and Deep Learning

    For the normal network, I used 19 inputs, and a hidden layer about 3 times the total number of inputs, i.e., 60 nodes, and an output layer with 3 outputs:  Candidate, Confirmed, and False Positive

    Then, I added an additional layer to the network with 60 nodes, to create the deep learning network.

    Examining the normal vs. deep learning yields the following results:
                            Accuracy   Loss
    Normal Neural Network   0.798      0.379
    Deep Learning Network   0.835      0.339

Conclusion:   A Neural Network Model is intuitive to setup and shows improved accuracy over the SVM model. In addition, the model can be improved for deep learning by adding additional hidden layers.  Further exploration of activation functions and other parameters may improve the accuracy of the model.   Overall, based on my limited time spent on this homework I prefer the Neural Network Model.







    






    


