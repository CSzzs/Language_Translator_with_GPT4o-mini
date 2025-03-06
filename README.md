# Translator_with_GPT4o_mini 🈸

A simple, elegant translation application powered by ChatGPT 4o-mini via the LangChain framework and Streamlit.

## Overview

Translator.AI is a web-based application that provides translation services between multiple languages. Built with Streamlit for the frontend and leveraging OpenAI's GPT-4o-mini model through LangChain for translations, this app offers a user-friendly interface for quick and accurate translations.

## Features

- Translate between multiple languages including English, French, Spanish, German, Latin, Japanese, Tamil, Hindi, and Sinhala
- Simple and intuitive UI built with Streamlit
- Powered by OpenAI's GPT-4o-mini model for high-quality translations
- Easy to deploy and use

## Project Structure

```
translator-ai/
├── config.json        # Configuration file with API keys
├── main.py            # Streamlit application entry point
├── translator_utils.py # Utility functions for translation
├── requirements.txt   # Project dependencies
└── README.md          # Project documentation
```

## Installation

1. Clone the repository:
   ```
   git clone https://github.com/yourusername/translator-ai.git
   cd translator-ai
   ```

2. Install the required dependencies:
   ```
   pip install -r requirements.txt
   ```

3. Set up your OpenAI API key:
   - Either update the `config.json` file with your API key
   - Or set the OPENAI_API_KEY environment variable

## Usage

1. Start the Streamlit application:
   ```
   streamlit run main.py
   ```

2. Access the application in your web browser (typically at http://localhost:8501)

3. Select the input and output languages from the dropdown menus

4. Enter the text you want to translate in the text area

5. Click the "Translate" button to get your translation

## How It Works

### Frontend (main.py)

The frontend is built using Streamlit and provides:
- A title and page configuration
- Two dropdown menus for selecting input and output languages
- A text area for entering the text to be translated
- A button to trigger the translation
- A display area for the translated output

### Translation Logic (translator_utils.py)

The translation functionality is implemented using:
- LangChain framework to simplify interactions with language models
- OpenAI's GPT-4o-mini model as the translation engine
- A prompt template that instructs the model to translate between specific languages
- Environment configuration to securely handle the API key

## Dependencies

- streamlit (1.43.0): For building the web interface
- langchain (0.3.20): Framework for working with language models
- langchain.openai (0.3.7): OpenAI integration for LangChain

## Configuration

The application requires an OpenAI API key to function. This key is stored in `config.json` and loaded by the application at runtime. For security reasons, do not commit your actual API key to the repository.

Example `config.json`:
```json
{
  "OPENAI_API_KEY": "your-api-key-here"
}
```

## Security Considerations

- **IMPORTANT**: The current repository includes an API key in the config.json file. This is not recommended for production use. Before pushing to a public repository, make sure to:
  - Remove the actual API key from config.json
  - Add config.json to your .gitignore file
  - Consider using environment variables instead

## Future Improvements

- Add support for more languages
- Implement language detection for input text
- Add a history feature to save past translations
- Improve error handling for API failures
- Implement caching to reduce API costs for repeated translations

## Contributing

Contributions are welcome! Please feel free to submit a Pull Request.

## Acknowledgements

- OpenAI for providing the GPT-4o-mini model
- Streamlit for the easy-to-use web application framework
- LangChain for simplifying interactions with language models
