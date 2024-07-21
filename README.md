

OpenNLP Chat Bot
This project is a custom chat agent for automated chat replies for FAQs. It uses different features of Apache OpenNLP to understand what the user is asking for. NLP stands for Natural Language Processing.

Features
Sentence Detection
Tokenization
Part-of-Speech Tagging
Lemmatization
Document Categorization
Prerequisites
Java 8 or higher
Apache OpenNLP library
Installation
Clone the repository:

bash
Copy code
git clone <repository-url>
cd <repository-directory>
Download the necessary OpenNLP models and place them in the project directory:

en-sent.bin
en-token.bin
en-pos-maxent.bin
en-lemmatizer.bin
faq-categorizer.txt (Custom training data)
Add the Apache OpenNLP library to your project dependencies. You can download it from Apache OpenNLP.

Project Structure
OpenNLPChatBot.java: Main class containing the chat bot logic.
faq-categorizer.txt: Custom training data with categories as per chat requirements.
en-sent.bin: Sentence detection model.
en-token.bin: Tokenizer model.
en-pos-maxent.bin: Part-of-Speech tagging model.
en-lemmatizer.bin: Lemmatizer model.
Usage
Compile the project:

bash
javac -cp "path-to-opennlp-library" OpenNLPChatBot.java
Run the project:

bash

java -cp ".:path-to-opennlp-library" OpenNLPChatBot
The chat bot will start, and you can enter your queries in the console.

Example Interaction
shell
##### You: Hello
Category: greeting
##### Chat Bot:  Hello, how can I help you?

##### You: What is the price of the product?
Category: price-inquiry
##### Chat Bot:  Price is $300

##### You: Thank you
Category: conversation-complete
##### Chat Bot:  Nice chatting with you. Bye.
Training the Model
The chat bot uses a categorizer model trained on custom data provided in faq-categorizer.txt. The file contains training data with categories to understand user queries better.

Customization
You can customize the predefined answers for each category by modifying the questionAnswer map in OpenNLPChatBot.java.

License
This project is licensed under the MIT License. See the LICENSE file for more details.

Author
Sharon Opudo

Acknowledgments
Apache OpenNLP for providing the NLP tools used in this project.
