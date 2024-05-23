# Mental Health Chatbot ReadMe

## Overview

This project implements a simple mental health chatbot using Python and Tkinter for the GUI. The chatbot responds to user inputs based on predefined patterns and responses stored in a JSON file. It features a chat interface, message history saving, and contact information display.

## Features

- **User-Friendly Chat Interface:** Interact with the chatbot through a simple, easy-to-use chat window.
- **Message Timestamping:** Each message is timestamped to keep track of the conversation flow.
- **Save Chat Log:** Save the chat history to a text file.
- **Send Chat Log:** Send the chat history to a specified email address.
- **Clear Chat Log:** Clear the current chat history.
- **Contact Information:** Access important contact numbers for mental health support.

## Installation

1. **Clone the Repository:**
    ```bash
    git clone https://github.com/your-repo/mental-health-chatbot.git
    cd mental-health-chatbot
    ```

2. **Install Dependencies:**
    This project requires Python 3.x. You can install the required packages using pip:
    ```bash
    pip install tk
    ```

3. **Prepare the Intents File:**
    Ensure you have an `intents.json` file in the project directory with the following structure:
    ```json
    {
        "intents": [
            {
                "tag": "greeting",
                "patterns": ["Hi", "Hello", "Hey"],
                "responses": ["Hello! How can I assist you today?", "Hi there! How are you feeling today?"]
            },
            ...
        ]
    }
    ```

## Usage

1. **Run the Application:**
    ```bash
    python main.py
    ```

2. **Interacting with the Chatbot:**
    - Type your message in the input field and press Enter or click the "Send" button.
    - The chatbot will respond based on the predefined patterns and responses in the `intents.json` file.

3. **Using Menu Options:**
    - **File Menu:**
        - *Save Chat Log:* Save the chat log to a text file.
        - *Send Chat Log:* Send the chat log to an email address.
        - *Clear Chat Log:* Clear the chat log.
        - *Cancel:* Close the application.
    - **Contact Menu:**
        - *Contact Numbers:* Display important contact numbers for mental health support.

## Code Overview

### `MentalHealthBot` Class

- **`__init__(self, intents_file):`** Loads the intents from a JSON file.
- **`get_respon
