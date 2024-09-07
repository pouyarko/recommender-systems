### Project Description

This project is a result of participating in a competition organized by Café Bazaar on the Quera platform. The goal of this competition was to predict the future apps that users would install based on their previous data. This competition was held during the opening workshop of the ICPC Tehran Regional Contest 2023, exclusively for the participants of this event.

The main objective of this project is to develop an advanced LSTM model to predict the future apps that Café Bazaar users will install. This model can analyze and predict future installations based on training data, which enhances the user experience.

### Long Short-Term Memory Networks (LSTM)

The Long Short-Term Memory (LSTM) model is a type of Recurrent Neural Network (RNN) specifically designed for modeling and predicting sequential data. Unlike standard RNNs, LSTMs can retain long-term information and avoid the vanishing gradient problem. These features make LSTMs highly suitable for tasks such as natural language processing, machine translation, and time series prediction.

### Data Used in This Project

The data used in this project includes two files:

1. **csv.apps_installed**: This file contains information about the apps installed by users. Each row represents a user and has two columns named `id_user` and `apps_installed`. The first column is the user ID, and the second column is a list of app IDs installed by the user, sorted by installation time.

2. **csv.apps_related**: This file provides data about similar apps in the Café Bazaar app. It shows how many times each app has been installed in the similar apps section of another app and from which index. This file includes four columns: `id_app_src` (source app ID), `id_app_dst` (destination app ID displayed in the similar apps section), `index` (the index at which it was displayed, starting from zero), and `installs` (number of installations).

### Recommender Systems

Such problems generally relate to recommender systems. The goal of these systems is to predict the user's next move based on their past behavior and provide optimal recommendations to capture more user attention. A similar example in Café Bazaar is akin to the challenges faced by online shopping sites, where new items are recommended to users based on their purchase or search history, increasing the likelihood of purchase and thereby enhancing profitability.

### Output

The expected output requires us to print 10 predictions for the next app to be installed by each of the one million users in the dataset. Each prediction should be printed with the corresponding uid in a row of a CSV file and uploaded to Quera. If the next installed app is one of the 10 predicted, the user is considered correctly predicted. The Quera judge will score us based on the percentage of all users we correctly predicted.

###Steps

You can find the code for our project in the `ipynb.send` file. Various Python libraries such as TensorFlow, Matplotlib, Numpy, and Pandas have been used. The goal of this project is to predict the apps installed by users. The step-by-step explanation of the code is as follows:

1. **Importing Libraries:**
   - `numpy` for numerical computations.
   - `matplotlib` for plotting graphs.
   - `tensorflow` and `keras` for building and training deep learning models.
   - `pandas` for reading and processing data.
   - `tqdm` for displaying progress bars.

2. **Reading Data:**
   - Data related to installed apps (`apps_installed.csv`) and related apps (`apps_related.csv`) are read from CSV files.

3. **Initial Settings:**
   - Various parameters such as the number of epochs, number of classes, and model storage path are set.

4. **Data Processing:**
   - The length of each row (number of apps installed by each user) is calculated and rows are grouped based on their length.
   - A graph of the distribution of row lengths is plotted.

5. **Defining the Model:**
   - An LSTM model with three recurrent layers and three dense layers is built.
   - The model is compiled using the `categorical_crossentropy` loss function and the Adam optimizer.

6. **Generating Data:**
   - Two functions, `size_by_numpy` and `size_by_numpy_test`, are defined to create training and test data based on row lengths.

7. **Training the Model:**
   - The model is trained for different data lengths and saved at each length.

8. **Prediction and Evaluation:**
   - Predictions are made for the test data and the results are reviewed to suggest new apps for each user.

9. **Creating Output File:**
   - The predicted data is saved in a CSV file named `result.csv`.
