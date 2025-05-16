# AI-import nltk
from nltk.chat.util import Chat, reflections
# Define chatbot responses
pairs = [
["hi|hello|hey", ["Hello! How can I assist you today?"]],
["(.*) help (.*)", ["I can help with account queries, troubleshooting, and more."]],
["bye|goodbye", ["Goodbye! Have a great day!"]]
]
# Create chatbot instance
chatbot = Chat(pairs, reflections)
# Start conversation
print("Chatbot: Hello! How can I assist you?")
while True:
user_input = input("You: ")
if user_input.lower() == "bye":
print("Chatbot: Goodbye! Have a great day!")
break
while True:
user_input = input("You: ")
response = chatbot.respond(user_input)
print("Chatbot:", response)
