# Grammar-Analyzer
This code takes a string input from the user, analyzes its grammar, and returns a JSON object indicating whether the input text is grammatically correct. If there are any errors, the object also includes the first occurrence of wrongness.

Installation:
1.	Install Python 3 from python.org.
2.	Install Spacy by running pip install spacy in your terminal.
3.	Download the en_core_web_sm model for Spacy by running python -m spacy download en_core_web_sm in your terminal.

The approach used to accomplish this task is as follows:
1.	Load the English language model for parsing using Spacy's en_core_web_sm module.
2.	Parse the input text using the Spacy parser and obtain a Doc object.
3.	Iterate through the Doc object sentence by sentence and token by token.
4.	Check if each token is a noun, verb, adjective, adverb, or pronoun using the pos_ attribute.
5.	Check if each token has a subject or object dependency using the dep_ attribute.
6.	Check if each token is capitalized, indicating a proper noun, using the is_title attribute.
7.	If any of the above checks fail, set a flag indicating that there is an error in the grammar, and record the index and text of the first token that fails the checks.
8.	Construct a JSON object indicating whether the input text is grammatically correct and including information about the first occurrence of wrongness (if any).
9.	Return the JSON object.

Advantages of this solution:
•	The modification is simple and only involves adding a single line of code, which prompts the user for input.
•	The input() function automatically converts the user's input to a string, so there is no need to add any additional type checking or conversion.
•	The modified code is easy to read and understand, even for someone who is not familiar with Python.

Disadvantages of this solution:
•	The input() function will pause the program until the user enters some text, which could cause the program to hang if the user takes a long time to enter input.
•	The modified code assumes that the user will enter valid text that can be parsed by the Spacy language model. If the user enters text that contains invalid characters or syntax errors, the program may crash or produce unexpected results. To handle this scenario, additional input validation and error handling may be needed.
