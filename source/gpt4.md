# GPT4

The GPT4 class is a wrapper for the GPT-4 API project. It provides an automated interface for interacting with the GPT-4 model developed by OpenAI.

## Installation

To use the GPT4 class, make sure you have the following dependencies installed:

- `selenium`
- `colorama`

## Usage

Here is an example of how to use the GPT4 class:

```python
from GPT4 import GPT4

# Initialize GPT4
gpt4 = GPT4(config_file='config.ini')

# Login to the GPT-4 API
gpt4.login()

# Ask a question
gpt4.ask_question('What is the capital of France?')

# Get the response
response = gpt4.get_response()
print(response)

# Design something
design = gpt4.design('Create a logo for my company')
print(design)

# Close the GPT4 instance
gpt4.close()
```

## Methods

- `__init__(self, config_file)`: Initializes the GPT4 instance. Takes a config file as input.
- `login(self)`: Logs in to the GPT-4 API using the credentials specified in the config file.
- `ask_question(self, question, max_t)`: Asks a question to the GPT-4 model. Returns a suitable response.
- `get_response(self)`: Returns the response generated by the GPT-4 model.
- `design(self, query, max_t)`: Generates a design based on the given query. Returns the design.
- `close(self)`: Closes the GPT4 instance and quits the webdriver.

## Config File

The config file should be a JSON file with the following structure:

```json
{
  "CREDENTIALS": {
    "username": "your_username",
    "password": "your_password"
  }
}
```

Make sure to replace `"your_username"` and `"your_password"` with your actual credentials.

## Dependencies

- [selenium](https://pypi.org/project/selenium/)
- [colorama](https://pypi.org/project/colorama/)