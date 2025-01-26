
# Text Generation with Language Model

This repository contains a project for text generation using a language model. The project utilizes various libraries such as NLTK, NumPy, PyTorch, and Streamlit to build and interface with the language model.

## Contents

- `app.py` - The main script that includes data loading, preprocessing, model definition, training, and text generation.
- `dataset.txt` - The dataset used for training the model (downloaded and saved by `app.py`).

## Features

- **Data Loading and Preprocessing**: Downloads a dataset, tokenizes text, removes punctuation and stop words, and converts tokens to numerical indices.
- **Model Definition**: Defines a language model using an LSTM neural network.
- **Training**: Trains the language model on the preprocessed data.
- **Text Generation**: Generates text based on a user-provided prompt using the trained model.
- **Streamlit Interface**: Provides a web interface for users to input text prompts and receive generated text.

## Setup

### Prerequisites

- Python 3.x
- Required libraries: `requests`, `nltk`, `numpy`, `torch`, `streamlit`

### Installation

1. Clone the repository:
    ```sh
    git clone https://github.com/Rida12-fatma/st125481_nlpA2.git
    cd st125481_nlpA2
    ```

2. Install the required libraries:
    ```sh
    pip install -r requirements.txt
    ```

### Running the Application

1. Run the `app.py` script:
    ```sh
    streamlit run app.py
    ```

2. Open your web browser and go to `http://localhost:8501`.

3. Enter a text prompt in the input box and click "Enter". The model will generate and display a continuation of the text.

## Model Training

The language model is trained using the following steps:

1. **Data Loading**: Downloads the dataset and saves it to `dataset.txt`.
2. **Preprocessing**: Tokenizes the text, removes punctuation and stop words, and converts tokens to numerical indices.
3. **Model Definition**: Defines a language model with an embedding layer, LSTM layers, and a fully connected layer.
4. **Training**: Trains the model using the preprocessed data.
5. **Saving the Model**: Saves the trained model to `model.pth`.

## Usage

You can use the `generate_text` function to generate text based on a prompt:

```python
from app import generate_text, model

start_text = "Harry Potter is"
generated_text = generate_text(model, start_text)
print(generated_text)
```

## License

This project is licensed under the MIT License. See the [LICENSE](LICENSE) file for details.
