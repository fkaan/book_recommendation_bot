# Book Recommendation and Summary Chatbot

This repository contains a simple chatbot application designed to provide book summaries and recommendations based on user input. The chatbot utilizes Natural Language Processing (NLP) techniques to understand user queries and respond appropriately. It is built using Python and several libraries, including `spaCy`, `fuzzywuzzy`, `nltk`, `pandas`, and `scikit-learn`. The graphical user interface (GUI) is created using `tkinter`.

## Features

1. **Intent Classification**: The chatbot can classify user input into different intents, such as requesting a book summary or asking for book recommendations.
2. **Book Summary Retrieval**: Given a book title, the chatbot retrieves the summary of the book from a preloaded dataset.
3. **Book Recommendations**: Based on the book title and its genres, the chatbot provides recommendations for similar books.
4. **Natural Language Processing**: Utilizes `spaCy` for extracting book titles from user input.
5. **Fuzzy Matching**: Uses `fuzzywuzzy` to match user input with book titles in the dataset.
6. **Cosine Similarity**: Calculates the similarity between book descriptions to recommend similar books.
7. **Interactive GUI**: The `tkinter` library provides an interactive chat interface for user interaction.

## Installation

To run this chatbot, you need to have Python installed on your system along with the required libraries. You can install the dependencies using `pip`:

```bash
pip install spacy fuzzywuzzy pandas nltk scikit-learn
python -m spacy download en_core_web_sm
```

## Usage

1. **Prepare the Dataset**: Ensure you have a CSV file named `duzeltilmisdftocsv.csv` with the book data, including columns for book titles and descriptions.
2. **Run the Chatbot**: Execute the Python script to start the chatbot interface.

```bash
python chatbot.py
```

## Code Overview

- **Intent Classification**: The `classify_intent` function uses keywords and fuzzy matching to classify user input as either a request for a summary or a recommendation.
- **Book Summary Retrieval**: The `get_book_summary` function uses fuzzy matching to find the best match for the book title in the dataset and returns its summary.
- **Book Recommendations**: The `recommend_books` function finds similar books based on genre and description similarity using TF-IDF and cosine similarity.
- **Natural Language Processing**: The `extract_book_title` function uses `spaCy` to extract book titles from user input.
- **GUI**: The `ChatBotGUI` class creates the chat interface using `tkinter`.

## Example

1. **Request a Summary**:
   - User: "Can you give me a summary of The Great Gatsby?"
   - Chatbot: "Kitap Başlığı: The Great Gatsby\nÖzet: [Book summary]"

2. **Ask for Recommendations**:
   - User: "Can you recommend me some books like The Great Gatsby?"
   - Chatbot: "Önerebileceğim benzer kitaplar [Book 1], [Book 2], [Book 3]"

## License

This project is licensed under the MIT License.

## Contributing

Contributions are welcome! Feel free to open an issue or submit a pull request.

## Acknowledgements

Special thanks to the developers of `spaCy`, `fuzzywuzzy`, `nltk`, `pandas`, and `scikit-learn` for providing the tools necessary to build this chatbot.
