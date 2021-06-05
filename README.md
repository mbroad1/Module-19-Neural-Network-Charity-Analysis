# Module 19 Challenge: Neural Network Charity Analysis

## Purpose:
The purpose of this analysis is to evaluate which non-profit organizations should receive funding from another non-profit organization, Alphabet Soup Charity, which allocates funds to different non-profits annually. In order to determine which non-profit organizations should receive funding, I created a deep learning neural network that evaluated the success of previous non-profit organizations that received funding based on several factors like the type of application they submitted and the purpose of the funding as the inputs to the neural network. After creating the neural network, I did my best to optimize it in order to increase its accuracy in determining which non-profit organizations would be successful in utilizing the funding effectively.
---

## Results:

### Data Preprocessing
#### Target and Features:
![Targets_and_Features](https://github.com/mbroad1/Module-19-Neural-Network-Charity-Analysis/blob/main/target%20and%20features.png)
- The target, y, was assigned to the column "IS_SUCCESSFUL" which assigned a 1 to organizations that were successful in utilizing the donated funds effectively and a 0 to organizations that failed to use the funds wisely.
- The features (denoted all as X) were all the other variables that were not "IS_SUCCESSFUL", "EIN", and "NAME" such as "APPLICATION_TYPE" and "USE_CASE" because these inputs may be helpful in determining the relationships between the variables and how those relationships influence the success or failure of an organization to use the donated funds well.

#### Dropped Features:
![Dropped_Features](https://github.com/mbroad1/Module-19-Neural-Network-Charity-Analysis/blob/main/dropped%20features.png)
- The features dropped from the dataset were "EIN" and "NAME" because these inputs are arbitrary and ultimately would not influence whether an organization would be successful in utilizing donated funds effectively.

### Compiling, Training, and Evaluating the Model
#### Numbers of Neurons, Layers, and Activation Function for my Initial Model:
![Initial_Model](https://github.com/mbroad1/Module-19-Neural-Network-Charity-Analysis/blob/main/initial%20model.png)
- For my intial model, I created a deep learning neural network that had two hidden layers:
  - The first hidden layer had 80 neurons.
  - The second hidden layer had 30 neurons.
- The activation function for each hidden layer was relu and the activation function for the output layer was sigmoid.
- The accuracy of this model after training over 100 epochs was **72.42%**

#### Optimized Model Attempt #1:
![Keras_Tuner_Results](https://github.com/mbroad1/Module-19-Neural-Network-Charity-Analysis/blob/main/Module%2019%20Challenge_KerasTuner_Results%20%232.png)
- In order to optimize the deep learning neural network for this dataset, I ran keras-tuner on the dataset and found that the best activation function for the hidden layers was tanh.
  - Likewise, the keras-tuner results showed that I needed to add an additional 4 layers to my model (so in total there would be 5 hidden layers) with the following number of neurons in each layer:
   - First hidden layer: 9 neurons
   - Second hidden layer: 7 neurons
   - Third hidden layer: 9 neurons
   - Fourth hidden layer: 5 neurons
   - Fifth hidden layer: 3 neurons
 - Additionally, the keras-tuner suggested to use 20 epochs to train the model.

![Keras_Tuner_Model_#1](https://github.com/mbroad1/Module-19-Neural-Network-Charity-Analysis/blob/main/optimized_model_%231_results.png)
- The accuracy of the best model from the keras-tuner was **72.65%**, a slight increase from the initial model, but not quite 75%.

#### Optimized Model Attempt #2:
![Model_#2](https://github.com/mbroad1/Module-19-Neural-Network-Charity-Analysis/blob/main/optimized_model_%232.png)
- For my second optimized model, I used the same layout as my initial model (2 hidden layers with 80 neurons in the first and 50 neurons in the second with relu as their activation functions and sigmoid as the activation function for the output layer) and added an additional third hidden layer with 30 neurons.
- Additionally, I trained the model over 20 epochs.
![Model_#2_Accuracy](https://github.com/mbroad1/Module-19-Neural-Network-Charity-Analysis/blob/main/optimized_model_%232_results.png)
- The accuracy of this model was **72.49%** which was very similar to the accuracy of the intial model.


#### Optimized Model Attempt #3:
![Model_#3](https://github.com/mbroad1/Module-19-Neural-Network-Charity-Analysis/blob/main/optimized_model_%233.png)
- Finally, for my third attempt at optimizing the model, I used the exact same model as the initial model except I trained this model over 200 epochs instead of 100 epochs.
![Model_#3_Accuracy](https://github.com/mbroad1/Module-19-Neural-Network-Charity-Analysis/blob/main/optimized_model_%233_results.png)
- The accuracy of this model was **72.58%**.
