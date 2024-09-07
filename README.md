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
