# deep-learning-challenge
This challenge contains two Jupyter Notebooks as well as two h5 files which were outputted from the notebooks. AlhabelSOupCharity.ipynb preproccesses data within charity_data.csv, which is found at https://static.bc-edx.com/data/dl-1-2/m21/lms/starter/charity_data.csv, and creates a model to determine successful applicants. The Notebook outputs the model in the file AlphabelSoupCharity_model.h5. The notebook AlphabetSoupCharity_Optimization.ipynb repeats the preproccessing of charity_data.csv, and tries to optimize the model. The notebook outputs the final attempt at the optimized model in the file AlphabetSoupCharity_Optimization.h5.
# Neural Network Model Report
## Analysis
The nonprofit foundation Alphabet Soup wants a tool that can help it select the applicants that will be successful in their ventures with funding. 

## Results 
### Data Preprocessing
The variable column "IS_SUCCESSFUL" is the the target for the model. The variable columns "APPLICATION_TYPE", "AFFILIATION", "CLASSIFICATION", "USE_CASE", "ORGANIZATION", "STATUS", "INCOME_AMT", "SPECIAL_CONSIDERATIONS", and "ASK_AMT" are the features for the model. The variable columns "EIN" and "NAME" are removed as they are neither targets nor features.

### Compiling, Training, and Evaluating the Model
In the process of optimizing the model, three models were made. 
- The first model had 3 hidden layers and 1 outer layer
    - layer 1: 20 neurons with relu activation function
    - layer 2: 15 neurons with relu activation function
    - layer 3: 10 neurons with relu activation function
    - output layer: 1 neuron with sigmoid activation function
- The second model had 3 hidden layers and 1 outer layer
    - layer 1: 25 neurons with tanh activation function
    - layer 2: 13 neurons with relu activation function
    - layer 3: 5 neurons with sigmoid activation function
    - output layer: 1 neuron with sigmoid activation function
- The third model had 3 hidden layers and 1 outer layer
    - layer 1: 20 neurons with relu activation function
    - layer 2: 10 neurons with relu activation function
    - layer 3: 5 neurons with relu activation function
    - output layer: 1 neuron with sigmoid activation function

With all three optimization attempts, the highest model performance was model 1 with a model accuracy of 72.79%. When trying to increase model performance, I tried changing the number of neurons within each layer, adding an additional hidden layer, and changing the activation functions within each layer.

## Summary
Overall, I was not able to optimize the model to have an accuracy of more thna 75%. A different model may be able to have a better accuracy with more neurons in each layer and potentially another hidden layer.