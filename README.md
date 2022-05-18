# Neural Network Charity Analysis

## Overview of Analysis
The purpose of this analysis is to predict whether applicants will be successful if funded by Alphabet soup. To do this we've created a binary classifier. The data presented is from more than 34,000 organizations that Alphabet Soup. has funded over the years. Below are our results. 


## Results

### Data Preprocessing

* The variable considered a target for our model is the IS_SUCCESSFUL column.
* The variables considered features to our model are all other columns with exception to EIN and NAME columns as we dropped those. 
* The variables removed from our input data were the EIN and NAME columns.

### Compiling, Training, and Evaluating the Mode

* For our neural network model we selected 2 hidden layers, the first with 80 neurons, and the second with 30 meurons. The 2 hidden layes have the ReLU activation function, and the output layer uses the Sigmoid activation function.

* We did not achieve target model performance as our accuracy came to 0.68 so we tried optimizing the model as explained below. 

* To increase model performance, we first tried adding more neurons to the hidden layers as shown below. Instead of 80,30 we went to 100,45 but our accuracy came back at 0.45.
![This is an image](https://github.com/belennlopezvega/Neural_Network_Charity_Analysis/blob/main/images/adding_neurons.png)
![This is an image](https://github.com/belennlopezvega/Neural_Network_Charity_Analysis/blob/main/images/results_adding_neurons.png)
* Next we tried adding 4 more hidden layers making the total number of layers 4. As shown below, our accuracy was higher than adding more neurons at 0.53.
![This is an image](https://github.com/belennlopezvega/Neural_Network_Charity_Analysis/blob/main/images/Adding_hidden_layers.png)
![This is an image](https://github.com/belennlopezvega/Neural_Network_Charity_Analysis/blob/main/images/results_hidden_layers.png)
* Last, we tried went back to our original 2 hidden layers with 80,30 neurons per layer respectively and instead changed the hidden layers activation function from ReLU to Tahn but our results were at .045 so there wasn't much improvement changing the activation function.
![This is an image](https://github.com/belennlopezvega/Neural_Network_Charity_Analysis/blob/main/images/tanh_function.png)
![This is an image](https://github.com/belennlopezvega/Neural_Network_Charity_Analysis/blob/main/images/results_tanh%20function.png)


## Summary
Overall, our original binary classifier model yieled the best results but did not reach that 75% accuracy score and the attemps to optimize the model didn't work to our advantage. This could be due to the model overfitting. In the future we could add more input data with additional hidden layers. We also recommend using a random forest classifier in place of binary classifier in the future as a random forest classifier can sample preprocessed data, they are more robust and overall it's faster. 
