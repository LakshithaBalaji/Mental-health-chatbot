#Mental Health Chatbot ReadMe
Overview
This project implements a simple mental health chatbot using Python and Tkinter for the GUI. The chatbot responds to user inputs based on predefined patterns and responses stored in a JSON file. It features a chat interface, message history saving, and contact information display.

Features
User-Friendly Chat Interface: Interact with the chatbot through a simple, easy-to-use chat window.
Message Timestamping: Each message is timestamped to keep track of the conversation flow.
Save Chat Log: Save the chat history to a text file.
Send Chat Log: Send the chat history to a specified email address.
Clear Chat Log: Clear the current chat history.
Contact Information: Access important contact numbers for mental health support.
Installation
Clone the Repository:

bash
Copy code
git clone https://github.com/your-repo/mental-health-chatbot.git
cd mental-health-chatbot
Install Dependencies:
This project requires Python 3.x. You can install the required packages using pip:

bash
Copy code
pip install tk
Prepare the Intents File:
Ensure you have an intents.json file in the project directory with the following structure:

json
Copy code
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
Usage
Run the Application:

bash
Copy code
python main.py
Interacting with the Chatbot:

Type your message in the input field and press Enter or click the "Send" button.
The chatbot will respond based on the predefined patterns and responses in the intents.json file.
Using Menu Options:

File Menu:
Save Chat Log: Save the chat log to a text file.
Send Chat Log: Send the chat log to an email address.
Clear Chat Log: Clear the chat log.
Cancel: Close the application.
Contact Menu:
Contact Numbers: Display important contact numbers for mental health support.
Code Overview
MentalHealthBot Class
__init__(self, intents_file): Loads the intents from a JSON file.
get_response(self, message): Returns a response based on the input message.
MessageWidget Class
__init__(self, master=None, sender=None, message=None, **kwargs): Initializes the message widget.
create_widgets(self): Creates and configures the message label.
Utility Functions
send_message(): Handles sending user messages and displaying bot responses.
display_message(sender, message): Displays a message in the chat log.
get_timestamp(): Returns the current timestamp.
clear_chat_log(): Clears the chat log after user confirmation.
save_chat_log(): Saves the chat log to a text file.
send_chat_log(): Sends the chat log to an email address.
cancel_chat_log(): Closes the application after user confirmation.
contact_numbers(): Displays important contact numbers.
Main Function
main(): Initializes the Tkinter GUI, sets up the chat interface, menu, and starts the main loop.
Notes
Customize the intents.json file to add more patterns and responses based on your needs.
Implement email functionality in send_chat_log() if required.
License
This project is licensed under the MIT License.
