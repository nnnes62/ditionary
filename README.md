# ditionary
# Dictionary Management System

## Overview

This project implements a simple Dictionary Management System in Python. It consists of two main classes: `DictionaryEntry` and `Dictionary`. The `Dictionary` class allows users to add, display, search, delete, and update dictionary entries.

## `DictionaryEntry` Class

### Constructor

```python
def __init__(self, english_word, thai_translation, word_type):
    """
    Initializes a new DictionaryEntry object.

    Parameters:
    - english_word (str): The English word.
    - thai_translation (str): The Thai translation.
    - word_type (str): The type of the word (e.g., noun, verb).

    Usage:
    entry = DictionaryEntry("hello", "สวัสดี", "greeting")
    """
    self.english_word = english_word
    self.thai_translation = thai_translation
    self.word_type = word_type
def add_entry(self, entry):
    """
    Adds a new entry to the dictionary.

    Parameters:
    - entry (DictionaryEntry): The entry to add.

    Usage:
    my_dictionary.add_entry(entry)
    """
    self.entries.append(entry)
def display_entries(self):
    """
    Displays all entries in the dictionary.

    Usage:
    my_dictionary.display_entries()
    """
    for entry in self.entries:
        print(f"{entry.english_word} ({entry.word_type}): {entry.thai_translation}")
def search_entry(self, word):
    """
    Searches for an entry in the dictionary by English word.

    Parameters:
    - word (str): The English word to search for.

    Returns:
    - entry (DictionaryEntry or None): The found entry or None if not found.

    Usage:
    result = my_dictionary.search_entry("hello")
    if result:
        print(f"Found: {result.english_word}")
    else:
        print("Entry not found.")
    """
    for entry in self.entries:
        if entry.english_word.lower() == word.lower():
            return entry
    return None
