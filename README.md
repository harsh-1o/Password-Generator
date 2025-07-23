# Password Generator in Python

A simple, customizable password generator built with Python. This command-line tool allows you to create strong, random passwords based on your chosen criteria—length, character sets (uppercase/lowercase letters, numbers, symbols), and more. Perfect for learning Python fundamentals and improving your programming skills!

## Features

- Select password length.
- Choose which character types to include:
  - Uppercase letters (A-Z)
  - Lowercase letters (a-z)
  - Numbers (0-9)
  - Symbols (e.g., !@#$%^&*)
- Basic input validation for safer results.
- Designed to be beginner-friendly and easy to understand.

## Demo

```bash
$ python main.py
Enter password length: 12

Should password contain upper case characters? (y/n): y
Should password contain lower case characters? (y/n): y
Should password contain symbols (y/n): y
Should password contain digits (y/n): y

Generated password: @$xgwRwzAa0z
```

## How It Works

1. User enters the desired password length.
2. User selects which character sets to include.
3. The script builds a list of allowed characters based on your choices.
4. The program randomly selects characters until the password is the desired length.

## Requirements

- Python 3.x
- No external libraries required (uses only the built-in `random` and `string` modules).

## Usage

1. **Clone this repository** or [download the script].
2. **Run the script** from your command line:

   ```bash
   python main.py
   ```

3. **Follow the prompts** to select password criteria.
4. **Copy your generated password** and use it where needed!

## Code Overview

```python
import random
import string

def generate_password(length, use_upper, use_lower, use_symbols, use_digits):
    characters = ''
    if use_upper:
        characters += string.ascii_uppercase
    if use_lower:
        characters += string.ascii_lowercase
    if use_symbols:
        characters += string.punctuation
    if use_digits:
        characters += string.digits

    if not characters or length < 1:
        return "Please choose length more than 0."
    
    password = ''.join(random.choice(characters)for _ in range(length))
    return password
```

## Contributing

Pull requests are welcome! For major changes, please open an issue first to discuss what you would like to change.

## License

This project is open-source and available under the [MIT License].

## Author

- [harsh-1o]
