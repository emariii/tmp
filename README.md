# Training Process and Preprocessing README

This README provides a brief overview of the training process and preprocessing steps in the given Python code.

## Training Process Overview
The training process involves the following steps:

1. Reading and combining multiple CSV files into a single DataFrame.
2. Preprocessing the data, including text cleaning and feature selection.
3. Splitting the data into training and test sets based on the topic labels.
4. Handling unseen data by mapping unknown values to the most frequent value in the training set.
5. Encoding the target labels using LabelEncoder.
6. Combining the title and story columns into a single "Combined" column.
7. Transforming the text data into TF-IDF (Term Frequency-Inverse Document Frequency) vectors using TfidfVectorizer.
8. Training a logistic regression model using the transformed features and encoded target labels.
9. Making predictions on the test set using the trained model.
10. Evaluating the model's performance by generating a classification report.

## Preprocessing Steps
The preprocessing steps involved in the code are as follows:

1. Text Cleaning:
   - Removing URLs, hashtags, and mentions from the sentences.
   - Removing punctuation marks and digits.
   - Keeping only Arabic letters.
   - Removing stop words from the sentences.

2. Data Processing:
   - Removing unnecessary columns from the DataFrame.
   - Removing duplicate rows.
   - Applying text cleaning to the "story" and "title" columns.

3. Splitting Data:
   - Splitting the preprocessed data into training and test sets for each topic label.

4. Handling Unseen Data:
   - Handling unseen values in the "author" column of the test set by mapping them to the most frequent value in the training set.

5. Encoding Labels:
   - Encoding the target labels (topic labels) using LabelEncoder.
   - Encoding the "author" column of the training and test sets using LabelEncoder.

6. Feature Engineering:
   - Combining the "title" and "story" columns into a single "Combined" column.

7. TF-IDF Transformation:
   - Transforming the text data in the "Combined" column into TF-IDF vectors using TfidfVectorizer.
   - Creating separate TF-IDF DataFrames for the training and test sets.

8. DataFrame Concatenation:
   - Concatenating the "author" column with the TF-IDF DataFrames for both the training and test sets.

## Final Training and Evaluation
After preprocessing and feature engineering, a logistic regression model is trained using the transformed features and encoded target labels. The trained model is then used to make predictions on the test set. Finally, the classification report is generated to evaluate the model's performance.

Note: The code provided assumes the availability of the necessary libraries and the presence of the required datasets in the specified path. Make sure to adapt the code as needed and ensure the datasets and dependencies are properly set up for successful execution.
