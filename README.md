# Translation Assignment---AI-Ml
This code is a Python program that translates English text into Hinglish, a blend of Hindi and English, using a pre-trained neural machine translation (NMT) model. It uses the Hugging Face Transformers library, which is a powerful library for working with state-of-the-art NLP models.

Here's a step-by-step explanation of the code:

1. Installation of Required Libraries:
   - It starts by installing three Python libraries: `transformers`, `torch`, and `sentencepiece`. These libraries are used for working with NLP models, including the Marian NMT model used for translation.

2. Importing Required Modules:
   - The code imports necessary modules and classes from the installed libraries, such as `MarianTokenizer` and `MarianMTModel` from the `transformers` library.

3. Loading the Translation Model:
   - It loads a pre-trained Marian NMT model specifically for translating English to Hindi. The model is identified by its name, which is "Helsinki-NLP/opus-mt-en-hi."

4. Hinglish Translation Function:
   - A function called `hinglish_translation` is defined, which takes an English text input as an argument.
   - Inside the function:
     - It tokenizes the input English text using the `tokenizer.encode` method, returning tensors ("pt" refers to PyTorch tensors).
     - The translation is generated using the NMT model with parameters like `max_length`, `num_beams`, and `early_stopping` to control the translation process.
     - The translated text is decoded from the generated tokens using `tokenizer.decode`. It also removes special tokens from the output.
     - The translated text is returned as the output of the function.

5. User Input and Translation:
   - The code takes user input for the English text to be translated using the `input()` function.
   - It calls the `hinglish_translation` function with the user's input and stores the translated text in the `hinglish_output` variable.

6. Printing the Results:
   - The code prints both the input English text and the corresponding Hinglish translation using the `print` statements.

In summary, this code utilizes a pre-trained Marian NMT model to perform English-to-Hinglish translation. It demonstrates how to use the Transformers library to work with such models. Users can input their English text, and the code will provide a Hinglish translation for better readability and understanding by non-native Hindi speakers.
