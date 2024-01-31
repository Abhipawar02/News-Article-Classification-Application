# News-Article-Classification-Application
A deployed streamlit Application to classify news articles, into following four categories:
    1. Business
    2. Entertainment 
    3. Sports
    4. World

application linnk - http://ec2-54-90-142-109.compute-1.amazonaws.com

## Getting Started

### Prerequisites

- Python 3.8.18
- Install required libraries: `pip install -r requirements.txt`

### Running the Script

1. Clone the repository: `git clone https://github.com/Abhipawar02/News-Article-Classification-Application.git` 
2. Navigate to the project directory: `cd News-Article-Classification-Application`
3. Run the script: `streamlit run app.py`

## Data Collection and Data Wrangling
- The raw data was collected from [Public News Website](https://indianexpress.com/).
- For detailed steps and code, refer to the [News Website-Scrapper](https://colab.research.google.com/drive/1gdkgr0gaqWT4HwUxo6iMaCf7_3D6ofoD?usp=sharing).  

### Check https://github.com/Abhipawar02/news-data-scrapping-and-section-classification Repository.

## Dataset

The raw dataset is included in the `dataset` directory, consisting of 193 entries with the following format:

- Article Title
- Article Body
- Section Value (Categorized into 'Entertainment', 'Business', 'World', 'Sport')

## Data Preprocessing
In order to prepare the dataset for analysis and modeling, the following data preprocessing steps were undertaken:
1. **Handling Null and Duplicated Values:**
   - Removed null values and duplicates, resulting in 128 non-null and unique entries.

2. **Visualizing Data Balance:**
   - Visualized the dataset to ensure a balanced distribution of entries within the 'Section_Value' categories ('Entertainment', 'Business', 'World', 'Sport').

3. **Creating 'Full Article' Column:**
   - Added a new column named 'Full Article' by combining the 'Article Title' and 'Article Body'.

4. **Text Cleaning with NLTK:**
   - Utilized the Natural Language Toolkit (NLTK) to perform the following text cleaning steps on the 'Full Article' column:
     - Removal of HTML tags.
     - Handling special characters.
     - Removal of stopwords.
     - Conversion of text to lowercase.
     - Lemmatization of words.

5. **Vectorization using Sklearn.CountVectorizer:**
   - Applied Sklearn's CountVectorizer to convert the 'Full Article' column into a numerical format suitable for machine learning models.

6. **Train-Test Split:**
   - Performed the train-test split to divide the dataset into training and testing sets for model training and evaluation.

## Hypertuning with sklearn Pipelines and MLFLOW integration
- We configured a pipeline using sklearn's `Pipeline` class, incorporating the `OneVsRestClassifier` for multi-class classification. The following models were included in the hyperparameter tuning process:

    - Logistic Regression
    - Random Forest
    - Multinomial Naive Bayes
    - Support Vector Machine (SVM)
    - Decision Tree
    - K-Nearest Neighbors (KNN)
    - Gaussian Naive Bayes

- For each model, we defined hyperparameter grids to search for the optimal combination of hyperparameters. These grids were used in conjunction with sklearn's `GridSearchCV` to perform cross-validated hyperparameter tuning.

- We utilized MLFLOW to log and track the hyperparameter tuning experiments. The local MLFLOW tracking URI was set to `http://127.0.0.1:5000` for easy monitoring of the experiments.

## Model Evaluation, Analysis And Selection
- After running the hyperparameter tuning process, the following models and their corresponding metrics were logged:

    - Test Accuracy
    - Precision
    - Recall
    - F1-score

- Below are the results for each model:
    - ![Result Image](relative/path/to/your/image.jpg)

## streamlit application 
- The best-performing model has been chosen based on evaluation metrics, and it is loaded into the app.py file for making predictions using streamlit library.

## DockerFile
- Created an DockerFile to create The image of the application based on Python 3.8-slim-buster and includes the necessary dependencies to run the application.
- For a Streamlit Application
    - ENTRYPOINT ["streamlit", "run", "app.py", "--server.port=8501", "--server.address=0.0.0.0"]

## AWS Setups And Github Actions CI/CD Pipelines
- 

## Issues and Solutions
- To be add

## Security and Network Configure (AWS)
- To be add

## Ready to Share !
- http://ec2-54-90-142-109.compute-1.amazonaws.com)http://ec2-54-90-142-109.compute-1.amazonaws.com


