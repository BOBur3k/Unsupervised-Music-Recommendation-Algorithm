# Unsupervised Music Recommendation Algorithm
![Dalle3_ART](docs/dalle3.png)
<p align="right">
  Artwork created by Dalle 3 AI
</p>

This project involves the analysis of music genres and themes using machine learning techniques. The project is divided into four phases: Exploratory Data Analysis (EDA), Data Cleaning, Data Modeling, and Reporting.

## Project Overview
The project is structured into the following phases:

### 1. Exploratory Data Analysis (EDA):

- Analyzed data to gain insights into music genres, themes, and artist distribution.
- Explored correlations between different features.
- Identified trends in song release dates, genres, and themes over time.
- Visualized distributions of song lengths, genres, and themes.

#### Insights from EDA:
- Observed a rise in the combination of hip-hop and obscenity in music starting from the early 2010s.
- Found that out of 5424 artists, only 3308 have more than one song in the training dataset.
- Discovered that the top 10 artists in the dataset are not primarily hip-hop, reggae, or pop artists.

#### Graphs to Include:
- Histogram of song release years.
- Bar plot of song counts by genre.
- Bar plot of song counts by theme.
- Bar plot of song lengths by genre.

### 2. Data Cleaning:

- Prepared the data for K-Mean Classification Model.
- Dropped irrelevant and strongly correlated columns indentified by use of HEATMAPs.
- Manipulate the dataframes to extract identifiers and features to meet the requirements for classification model.

### 3. Data Modeling:

- Utilized K-means clustering algorithm with 5 clusters, identified by combination of Elbow and Silhouette  Plot.
- Use the developed model on the test dataset.
- Applied Principal Component Analysis (PCA) to reduce dimensionality for visualization.
- Assigned cluster labels to each song and identifier.
- Developed an interactive recommendation tool based on cluster classification.

### 4. Reporting:

- Summarized insights gained from EDA.
- Described the process of determining optimal clusters.
- Provided human-interpretable descriptions of the clusters.
- Presented a recommendation tool for users based on their song preferences.

## Code Details
The script employs `if`, `else`, and `elif` functions for handling user choices. The `if` statement checks whether the user wants to encrypt or decrypt the message. If encrypting, it enters the corresponding line of code; if decrypting, it enters another line of code. The `elif` function is used for additional conditions. Additionally, basic `for` loops are used for both encryption and decryption processes. These loops iterate through each character in the input message, applying the Caesar Cipher algorithm. The `ord` function is used to convert characters to their corresponding ASCII values, and the `chr` function is used to convert ASCII values back to characters. The `''.join` function is also utilized to concatenate the characters back into a string, providing a more readable format for the final result. To make sure that code can handle big numbers for a key variable, the encoding and decoding code includes functions like `(ord(z)- 32 + key) % 95 + 32` for encoding and `(ord(z)- 32 - key) % 95 + 32` for decoding. Dividing by `95` ensure that our `ord` value will not overflow the limits of ASCII model and adding and subtracting `32` ensure the set limits.  

## Limitations
- The encoded message appearance can vary based on the chosen key, potentially resulting in non-alphabetic characters.
- A temporary fix is implemented by instructing users to copy and paste the encoded message for future decryption.
- Considerations for improving the user experience, such as finding alternatives to manual copying and pasting, are mentioned.

## Future Steps
- Explore solutions to make the encoding and decoding process more user-friendly without manual copying.
- Consider adapting the code for use in a Telegram bot to provide a more streamlined and accessible experience.

## How to Use
1. Run the script in a Python environment.
```bash
python caesar_cipher.py
```
2. Choose whether to encrypt or decrypt a message by entering 'E' or 'D' respectively.
3. If encrypting, enter the message to be encoded and a key for encryption.
4. If decrypting, enter the message to be decoded and the encryption key used.
5. Copy and save the resulting encrypted or decrypted message.
6. The program prompts whether you want to use the Caesar Cipher tool again. Respond with 'Y' to continue, or 'N' to exit.
