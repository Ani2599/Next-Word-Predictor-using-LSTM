# Next Word Prediction with LSTM and Early Stopping

This project is a **Streamlit** web application that predicts the next word in a given text sequence using a pre-trained **LSTM** (Long Short-Term Memory) model. It uses **Keras** for model loading and **Streamlit** for the frontend interface. 

## Features

- **Predict Next Word**: Enter a sequence of words, and the app will predict the next word using the trained LSTM model.
- **Interactive Interface**: User-friendly Streamlit interface for easy interaction.
- **Early Stopping**: The LSTM model is trained with early stopping to avoid overfitting.

## How It Works

1. **Input Text Sequence**: The user enters a sequence of words through the Streamlit app.
2. **Text Preprocessing**: The sequence is tokenized and padded to match the LSTM input format.
3. **Prediction**: The pre-trained LSTM model predicts the next word.
4. **Output**: The predicted next word is displayed on the interface.

## Project Structure

- `app.py`: The main file to run the Streamlit application.
- `next_word_lstm.h5`: The pre-trained LSTM model.
- `tokenizer.pickle`: The tokenizer used to preprocess the text.

## Installation

1. Clone the repository:
   ```bash
   git clone https://github.com/yourusername/next-word-prediction-lstm.git
   cd next-word-prediction-lstm
   ```

2. Install the required dependencies:
   ```bash
   pip install -r requirements.txt
   ```

3. Place the `next_word_lstm.h5` model and `tokenizer.pickle` files in the project directory.

4. Run the Streamlit app:
   ```bash
   streamlit run app.py
   ```

## Usage

1. Launch the app with `streamlit run app.py`.
2. Enter a sequence of words in the text input box (e.g., "To be or not to").
3. Click the "Predict Next Word" button to get the next predicted word.

## Code Explanation

- `predict_next_word`: This function takes the input text, tokenizes it, and pads it to ensure the correct input shape for the model. It then uses the LSTM model to predict the next word based on the given sequence.
- **Streamlit Interface**: The Streamlit code creates an interactive app where users can enter a word sequence and receive the next predicted word.

## Dependencies

- `streamlit`: For building the interactive web interface.
- `tensorflow`: For loading and running the LSTM model.
- `numpy`: For data manipulation.
- `pickle`: For loading the pre-trained tokenizer.

## Example

Example input: `"To be or not to"`

Predicted output: `Next word: be`

## Future Enhancements

- Add support for multiple predictions (e.g., suggest multiple possible next words).
- Allow users to select different sequence lengths.
- Implement more sophisticated text generation techniques.

## License

This project is open-source and available under the MIT License.

