# IMDB Sentiment Classifier

This project demonstrates how to build and deploy a movie review sentiment classifier using Hugging Face Transformers and Gradio. The core of the project involves fine-tuning a pre-trained BERT model on the IMDB dataset to classify movie reviews as either positive or negative. An interactive web interface is then created using Gradio, allowing users to input their own reviews and get real-time sentiment predictions.

## Table of Contents

- [Project Overview](#project-overview)
- [Features](#features)
- [Dataset](#dataset)
- [Model](#model)
- [Setup and Installation](#setup-and-installation)
- [Usage](#usage)
- [Contributing](#contributing)
- [License](#license)
- [Acknowledgements](#acknowledgements)

## Project Overview

This repository contains a Google Colab notebook (`.ipynb` file) that guides you through the process of:
1.  Loading and preprocessing the IMDB movie review dataset.
2.  Fine-tuning a `bert-base-uncased` model for binary sentiment classification.
3.  Evaluating the fine-tuned model's performance.
4.  Saving and reloading the trained model and tokenizer.
5.  Deploying an interactive sentiment classification interface using Gradio.

## Features

*   **Sentiment Classification**: Classifies movie reviews as 'positive' or 'negative'.
*   **Hugging Face Transformers**: Leverages the power of pre-trained BERT models for state-of-the-art NLP.
*   **Fine-tuning**: Demonstrates how to fine-tune a model on a custom dataset.
*   **Gradio Interface**: Provides a user-friendly, interactive web application for real-time predictions.
*   **Reproducibility**: Uses seeding to ensure consistent results.
*   **Ease of Use**: Designed to be run directly in Google Colab.

## Dataset

The project utilizes the **IMDB Movie Review Dataset**, which consists of 50,000 movie reviews labeled as either positive (1) or negative (0). The dataset is loaded using the `datasets` library from Hugging Face.

For demonstration purposes, a smaller subset of the original dataset is used for training and evaluation to ensure faster execution within the Colab environment.

## Model

The chosen model is `bert-base-uncased`, a widely used and powerful transformer model. It is fine-tuned for sequence classification using the `AutoModelForSequenceClassification` class from the `transformers` library. The fine-tuning process adapts the pre-trained weights to the specific task of sentiment analysis on movie reviews.

## Setup and Installation

To run this project, you will need a Google Colab environment or a local Python environment with the following dependencies. The Colab notebook handles most of this automatically.

1.  **Google Colab (Recommended)**:
    *   Open the `.ipynb` file in Google Colab.
    *   Ensure you have a GPU runtime enabled (`Runtime > Change runtime type > GPU`).
    *   The notebook will automatically install all required libraries.

2.  **Local Environment (Optional)**:
    *   Clone this repository.
    *   Install Python 3.8+.
    *   Install the required libraries:
        ```bash
        pip install transformers datasets scikit-learn accelerate gradio torch
        ```

## Usage

Once the notebook is run in Google Colab, follow these steps:

1.  **Run all cells**: Execute all cells in the notebook (`Runtime > Run all`).
2.  **Gradio Interface**: After the model training and saving steps are complete, a Gradio interface will be launched. You will see a public URL (e.g., `https://xxxxxx.gradio.live`) in the output of the final cell.
3.  **Interact**: Click on the provided URL to open the interactive sentiment classifier.
4.  **Input Review**: Type or paste a movie review into the text box.
5.  **Get Prediction**: The interface will instantly display the sentiment prediction (Positive/Negative) along with a confidence score.

### Example Output (from Gradio Interface):

![Gradio Demo Screenshot](https://raw.githubusercontent.com/YourGitHubUsername/YourRepoName/main/gradio_screenshot.png) <!-- Replace with an actual screenshot link if you have one -->

**Example Predictions:**

*   `{'label': 'positive', 'confidence': 0.9961} -> This movie was absolutely fantastic. Brilliant acting and a ...`
*   `{'label': 'negative', 'confidence': 0.9931} -> I hated this film. It was boring, too long, and badly writte ...`
*   `{'label': 'positive', 'confidence': 0.5348} -> It was okay - some good moments, but overall forgettable. ...`

## Contributing

Feel free to fork this repository, open issues, or submit pull requests to improve the project. 

## License

This project is open-source and available under the [MIT License](LICENSE). <!-- Link to your LICENSE file -->

## Acknowledgements

*   **Hugging Face Transformers**: For providing the powerful libraries and pre-trained models.
*   **Hugging Face Datasets**: For easy access to the IMDB dataset.
*   **Gradio**: For simplifying the deployment of machine learning models into interactive web apps.
*   **Google Colab**: For providing a free and accessible environment for development.
