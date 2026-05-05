# NLP Projects with Python

This repository contains two beginner-friendly Python projects that explore core concepts of Natural Language Processing (NLP). Both are written as Jupyter Notebooks and are great for anyone learning how to work with text data using Python.

---

## Project 1 — NLP Basics (`NLP.ipynb`)

This notebook is a hands-on introduction to the most common text preprocessing steps in NLP. If you've ever wondered how programs "read" and clean up text before doing anything useful with it, this is a great place to start.

### What it does

You give it a raw, messy sentence like:

```
"Hello!!! My email is abc123@gmail.com. I am running late. Call me at 03121234567."
```

And it walks through the following steps:

- **Extract emails** — uses regex to pull out any email addresses from the text
- **Extract phone numbers** — finds 11-digit phone numbers using a pattern match
- **Clean the text** — strips out special characters, punctuation, emojis, and numbers so only plain words remain
- **Tokenization** — splits the cleaned sentence into individual words (tokens)
- **Remove stopwords** — filters out common filler words like "is", "am", "the", "at" so you're left with only the meaningful words

### Libraries used

- `re` — Python's built-in regex library
- `nltk` — Natural Language Toolkit for tokenization and stopwords

### Sample output

```
Email: ['abc123@gmail.com']
Phone: ['03121234567']
Clean Text: Hello My email is abcgmailcom I am running late Call me at
Tokens: ['Hello', 'My', 'email', 'is', ...]
Filtered Words: ['Hello', 'email', 'running', 'late', 'Call']
```

---

## Project 2 — NLP Chatbot (`Chatbot_NLP_(1).ipynb`)

This one takes things a step further. It's a simple command-line chatbot that doesn't just reply to your messages — it also analyzes them using NLP tools. Think of it as a chatbot that understands a little more than just keywords.

### What it does

You type a message, and the chatbot:

1. **Detects the sentiment** of your message — positive, negative, or neutral
2. **Classifies your intent** and gives a relevant reply (greetings, questions about NLP, weather, etc.)
3. **Remembers your last 3 messages** so it can look back at the conversation
4. On the command `show ner` — shows **Named Entity Recognition** results from your recent messages (e.g., it picks up names, cities, organizations)
5. On the command `show pos` — shows **Part of Speech** tags for each word (noun, verb, adjective, etc.)

### Example interaction

```
You: hi
Chatbot: Neutral
Chatbot: Hello! Nice to meet you!

You: ali is running in lahore
Chatbot: Neutral
Chatbot: Tell me more!

You: show ner
Chatbot: Showing NER from last inputs:
ali -> PERSON
lahore -> GPE
```

### Libraries used

- `spacy` with the `en_core_web_md` model — for NER and POS tagging
- `nltk` with the VADER lexicon — for sentiment analysis

---

## How to run these notebooks

1. Clone the repository or download the `.ipynb` files
2. Open them in [Google Colab](https://colab.research.google.com/) or Jupyter Notebook
3. Run each cell in order — the first cell usually installs or downloads the required models
4. For the chatbot, just type your messages in the input box that appears and hit Enter

### Requirements

```
nltk
spacy
```

For spacy, you'll also need to download the English model:

```bash
python -m spacy download en_core_web_md
```

---

## What you'll learn

By going through both notebooks, you'll get comfortable with:

- Writing regex patterns to extract information from text
- Cleaning and preprocessing raw text for NLP
- Tokenization and stopword removal
- Sentiment analysis using VADER
- Named Entity Recognition (NER) and Part of Speech (POS) tagging
- Building a simple rule-based chatbot with memory

These are the building blocks used in real-world NLP applications like search engines, chatbots, and text classifiers. A solid starting point!
