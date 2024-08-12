# deep-learning-challenge
Module 21 Challenge


----------------ANALYSIS OVERVIEW----------------

The purpose of this analysis is to determine whether the model can help select applicants for funding with the best chance of success in their ventures. 
The classification model would take the data and ideally predict whether they would be successful if funded by Alphabet Soup. 


----------------RESULTS----------------

Data Preprocessing

What variable(s) are the target(s) for your model?
- The target variable for the model is the 'IS_SUCCESSFUL' column from the application dataframe.

What variable(s) are the features for your model?
- The feature variables for the model are the other columns from the application dataframe after dropping the 'IS_SUCCESSFUL' column.

What variable(s) should be removed from the input data because they are neither targets nor features?
- The 'EIN' and 'NAME' column were removed from the input data because they're irrelevant as targets or features. 

Compiling, Training, and Evaluating the Model

How many neurons, layers, and activation functions did you select for your neural network model, and why?
- For training the model, I started the hidden layers of 80 nodes and 30 nodes to start. There were 2 hidden layers and basic activation functions with 100 Epochs. This resulted in a loss of 0.569 with an accuracy of 72.4%.

Were you able to achieve the target model performance?
- The model was not able to achieve the target model performance of 75%. It stayed consistently at 72.3% - 72.4%.

What steps did you take in your attempts to increase model performance?
- First I increased the hidden layer nodes up to 100 for each of the 2 hidden layers. This brought accuracy up from 72.36% to 72.4%, but it also increased loss by 0.64%. Next the nodes in the hidden layer were reset to 80 and 30, but a learning rate was added to fine tune the rate the model was learning as there was concern that if the model was learning too fast, it would give a suboptimal solution, vice versa. This had no effect on accuracy and it did bring loss down, but not enough to matter. For the 3rd attempt at optimization, Hidden layers 1 and 2 were adjusted to have 20 nodes and 10 nodes, but a 3rd hidden layer was added with 5 nodes. Epochs were also adjusted to 50 instead of 100, bringing accuracy up to 72.5% and loss down to 0.557. The last attempt was adjusting the hidden layers to 10, 8, and 6, but the loss and accuracy remained the same.

----------------SUMMARY----------------

In summary, the model was not able to achieve the target model performance of 75% accuracy and it stayed consistently at 72.5% after attempts at optimization. A different model I would recommed would be a pre-trained model, also known as transfer learning. These models have already been trained on large datasets and have been fine-tuned. These models are more accurate due to having already learned from large and more complex datasets, so these models would likely be more highly accurate.
