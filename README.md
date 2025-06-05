# chatgpt-chatbot

The `chatgpt-chatbot` project is a terminal-based chatbot that uses the OpenAI API to simulate a conversation with a user. It consists of two main files: `index.js`, which contains the core logic for interacting with the user and OpenAI, and `open-ai.js`, which sets up and exports the OpenAI client using an API key loaded from environment variables via `dotenv`.

The chatbot starts by greeting the user in the terminal using styled output from the `colors` library and continuously prompts the user for input using `readline-sync`. It maintains a conversation history (`chatHistory`) to preserve context across turns, reconstructing this history into the `messages` format expected by OpenAI’s GPT-3.5 model on each new input.

The model's response is printed in green, and both the user's input and the assistant's reply are appended to the history. The loop exits cleanly when the user types `"exit"`, after returning the bot's final reply. The program includes error handling to gracefully display issues related to the API or network.

Overall, the project demonstrates key concepts such as asynchronous JavaScript, API communication, stateful conversation management, error handling, and clean separation of concerns between configuration and application logic. **The key thing to remember is that, in the free plan of the OpenAI API, usage is limited to only a few responses, so excessive requests may lead to temporary restrictions or errors if the quota is exceeded.**
