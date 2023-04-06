# NLP Arabic Empathetic Chatbot 
A project for GUC NLP elective course using the Facebook Empathetic Dialogues to create an Open-domain Conversation chatbot but in Arabic.
The main goal of the chatbot is to recognise feelings in the conversation partner and respond appropriately; the available datasets that help in recognising feelings and improving conversations in chatbots are the Facebook Empathetic Dialogues; however, there are no freely available similar datasets for Arabic language. As a result, we created our own Arabic dataset by translating the data from Facebook Empathetic Dialogues and built an Arabic chatbot.

# How to use:- 
- Only run the Chatbots Notebook. No need to run other notebooks. 
- all inputs from the data are available, if the chatbot recieved any input in english it'll give a default response of "I don't understand"
- write "Quit" to quit. 

# The Repo contains 3 python notebooks, beside the chatbot exported in a notebook
each of the mentioned notebooks represents a step or a phase done in the project whether starting with translating followed by preprocessing and then training the model

# The Translating notebook is mainly for Data Translation and Reorganization and consists of the following :-

- Loading datasets and obtaining the relevant columns from it
- Creating placeholders for ordered Data and splitting it into (emotion, context, response).
- obtaining the translated training data.

# The Preprocessing notebook is mainly for Modifying the data and making it more suitable for the model and consists of the following :-

- Reading the data, normalizing , tokenzing and saving it into a tockenized dataset.
- Polarizing data into 2 emotion labels instead of 32 (Happy or Sad) 
- After predicting the emotion, the chatbot compares cosine similarity between the user input and the contexts with the matching emotion and computes a list of the maximum cosine similarities and retrieves their responses and chooses one of those responses randomly
- Saving full dataset with the extra binary emotion column for training

# The Model training notebook and it consists of the following :- 
- Setting hyperparameters
- tokenizing and encoding class labels
- Creating model architecture
- Training with epochs = 500
- Evaluating to get accuracy value
- Saving the model 
 
 # Model's accuracy is 73% 
