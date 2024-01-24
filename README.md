# Build-Chatbots-with-Python-Capstone
**Codecademy chatbot assignment**

**Title:** Camping Bot

**Name:** You-shan Chung

**Username:** emyschung

**Retrieval or generative:** Retrival

**Why a closed-domain architecture:** Simply because I want to make sure that this bot will not generate something too wild (which could happen since I'm new to modeling). 

**Use case(s):** When someone's at a total loss of where to camp, this bot can inform some common factors one might want to consider. 

**Techniques:** BoW (for intent classification) and Word2Vec (for response selection)

**Reflection:** 
I focused on the basics buidling a bot.

**Data:** I used ChatGPT 3.5 to generate query-response pairs, with the following _prompt_ :
  
  "List 10 queries for various camping sites and their possible responses. For example:

**Query:** Ideally, as close to the beach as possible without being too windy.
**Response:** Sure. Some of the best coast campgrounds include Big Sur, California, Assateague Island National Seashore, Maryland, and Bahia Honda State Park, Florida. Do you live in the US?"

**Imports:** Mostly from a restaurant bot built for a previous Codecademy final project

**Script:** Also from that same previous restaurant bot

Still, two challenges with Pandas and importing. 

The Pandas issue was with .replace, which didn't work until I realized I should add .str. 

As for importing, I defined queries and responses in the same file as blank_spot (i.e. category keyword to which the most similar word in a query will be identified and fill the slot in every response), and only the first two worked. The problem disappeared after restarting Jupyter Notebook. 

**Dependencies:**

**BoW:** a self-defined counter function

**word2vec:** Spacy's 'en_core_web_md'

**preprocessing:** nltk word_tokenize,pos_tag,nltk_corpus

**visual:** Below is a concluded conversation between me (purple numbers) and the bot (blue numbers). The converation involves 1 welcome message (number 1), 3 queries (number 2,5,8), one exit command (number 11) and 7 responses (number 3,4,6,7,9,10,12). 

![image](https://github.com/youshanchung/Build-Chatbots-with-Python-Capstone/assets/92421932/86fc34de-7c42-4319-93de-4d7cb633eacb)

The bot doesn't stop prompting the user with "any other questions" until the user's message is the same as one of the exit commands. On such commands, the bot terminates and returns a good-bye message immediately. 
