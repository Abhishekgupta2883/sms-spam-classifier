# Email/SMS Spam Classifier

This project is a web application built using Streamlit that can classify whether a given email or SMS message is spam or not.

## Installation

To run this project, you'll need to have the following dependencies installed:

- Python 3.x
- Streamlit
- Pickle
- NLTK (Natural Language Toolkit)

You can install the required dependencies using pip:

```
pip install streamlit pickle nltk
```

Additionally, you'll need to download the NLTK resources used in the project:

```python
import nltk
nltk.download('punkt')
nltk.download('punkt_tab')
```

## Usage

To run the application, execute the following command in your terminal:

```
streamlit run app.py
```

This will start the Streamlit server and open the application in your default web browser.

Once the application is running, you can enter an email or SMS message in the text area and click the "Predict" button to classify the message as spam or not spam.

## API

The main functionality of the application is provided by the `transform_text()` function, which preprocesses the input text by performing the following steps:

1. Converts the text to lowercase.
2. Tokenizes the text using NLTK's `word_tokenize()` function.
3. Removes non-alphanumeric characters.
4. Removes stop words and punctuation.
5. Applies stemming using the Porter Stemmer.
6. Joins the processed tokens back into a single string.

The `tfidf` and `model` variables are loaded from pre-trained pickle files, which are used to vectorize the preprocessed text and make the spam/not spam prediction.

## Contributing

If you'd like to contribute to this project, please follow these steps:

1. Fork the repository.
2. Create a new branch for your feature or bug fix.
3. Make your changes and commit them.
4. Push your changes to your forked repository.
5. Submit a pull request to the main repository.


```

This will run any tests that have been defined in the `tests/` directory.
