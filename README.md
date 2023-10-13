# Rasa Chatbot Project Setup Guide

This guide will help you set up and run a Rasa chatbot project with a Spacy language model. The chatbot will be deployed using Rasa's API and actions server. [Here's a demo](https://drive.google.com/file/d/1-zcT3Cy3ozCGnyZG45OiW0ra3AT8h7H1/view?usp=sharing). Follow the steps below to get started:


## Prerequisites

Make sure you have the following software installed on your system:

- Python (preferably Python 3.6 or higher)
- pip (Python package manager)

## Step 1: Clone the Repository

Clone the project repository to your local machine:

```bash
git clone <repository_url>
cd <repository_name>
```

## Step 2: Install Rasa and Spacy Model

Install Rasa and the Spacy language model using pip:

```bash
pip install rasa
pip install spacy
python -m spacy download en_core_web_trf
```

## Step 3: Train the Rasa Model

Train the Rasa chatbot model using the following command:

```bash
rasa train
```

## Step 4: Run Rasa Server

Run the Rasa server to expose the chatbot API:

```bash
rasa run -m models --enable-api --cors "*"
```

## Step 5: Run Actions Server

Open a separate terminal window, navigate to your project directory, and run the Rasa actions server:

```bash
rasa run actions
```

## Step 6: Test the Chatbot

Now that both the Rasa server and actions server are running, you can test the chatbot's API using the `index.html` provided in the project.

1. Open `index.html` in your web browser.

2. Type your messages in the chat window and observe the responses from the chatbot.

## Additional Configuration

- If you want to customize the chatbot's behavior, modify the `domain.yml` and `data/nlu.yml` files for adding intents, entities, responses, and more.

- You can also create custom actions by editing the `actions.py` file.

- To integrate your chatbot with external systems (e.g., databases, APIs), modify the corresponding custom actions and adapt them to your requirements.

## Conclusion

Congratulations! You have successfully set up and deployed your Rasa chatbot project using the Spacy language model and Rasa's API. You can further enhance the chatbot's capabilities by training it with more data and exploring additional Rasa features.

If you encounter any issues during the setup or have any questions, please refer to the official Rasa documentation or seek help from the Rasa community. Happy chatbot building!
