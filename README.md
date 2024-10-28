# Customer Churn Prediction with Artificial Neural Networks
This project uses an Artificial Neural Network (ANN) to predict customer churn, based on customer demographics, account details, and transaction activity. By leveraging customer data, this model aims to classify customers as "churned" or "active," helping businesses identify potential churn and develop retention strategies.

### Project Overview
Customer churn is a critical metric for customer-centric businesses, as retaining an existing customer is typically more cost-effective than acquiring a new one. This project addresses the need to predict churn early and accurately, using machine learning techniques and neural networks. The dataset used includes 10,000 customers with demographic and account-related features. The primary model is a neural network built with Keras and TensorFlow.

### Data Overview
The dataset contains the following key features:

1) CreditScore: Credit score of the customer
2) Geography: Customer’s location (encoded as France, Spain, and Germany)
3) Gender: Gender of the customer (binary encoded)
4) Age: Age of the customer
5) Tenure: Number of years with the bank
6) Balance: Account balance
7) NumOfProducts: Number of products held by the customer
8) HasCrCard: Credit card status (binary)
9) IsActiveMember: Active membership status (binary)
10) EstimatedSalary: Estimated annual salary
11) Exited: Churn status (target variable)

### Data Preprocessing

##### Feature Encoding:
. Binary encoding for Gender
. One-hot encoding for Geography

#### Scaling: StandardScaler is used to normalize numerical features for better ANN performance.

### Model Architecture
A simple ANN was developed with Keras to classify customers as either "exited" or "active." The model architecture consists of:

1. Input Layer: Accepts the input features after scaling and encoding.
2. Hidden Layers: Two dense layers with ReLU activation functions, providing non-linearity.
3. Output Layer: A single neuron with a sigmoid activation function, outputting a binary classification for churn prediction.

### Model Training
The model is compiled using the Adam optimizer with binary cross-entropy as the loss function. The training process utilizes:

### TensorBoard for performance monitoring
Early Stopping to prevent overfitting, with the best weights restored after 10 epochs of non-improvement in validation loss.

### Training Results
The model achieved an accuracy score of around 87% on training data, with similar performance on validation data.

### Usage
The trained model can be loaded and applied to predict customer churn on new data. The project also includes saved encoders and a scaler for consistent preprocessing of future data.
