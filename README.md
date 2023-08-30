# Electronic Store Customer Service Assistant with OpenAI GPT-3.5 Turbo

## Introduction
This repository contains a Jupyter notebook that emulates a customer service assistant using OpenAI's GPT-3.5 Turbo model. The assistant provides users with details about various electronic products.

## Overview
The project is designed for learning purposes and demonstrates how to integrate OpenAI's GPT-3 model with a user interface to simulate a customer service interaction.

## Contents
1. **Electronic Products Data (JSON):** A JSON file containing details about various electronic products, including their category, brand, model number, features, description, and price.
2. **Utility Functions (utils.py):** A set of utility functions to assist with extracting product information and generating appropriate responses.
3. **Interactive Assistant (Jupyter Notebook):** A Jupyter notebook that integrates the GPT-3 model with a Panel-based GUI for real-time interactions. Users can ask about specific products, and the assistant will provide relevant details.

## Key Function and Features

### Utility Documents `utils.py`:
  - `get_products_and_category():` This function reads the JSON file containing product details and returns a dictionary of products categorized by their types.
  - `find_category_and_product_only(user_input, products_data):` Accepts user input and the product data, then identifies and extracts the categories and products    mentioned in the user input.
  - `generate_output_string(category_and_product_list):` Uses the identified categories and products to generate a formatted output string containing relevant product details.

### Jupyter Notebook
- `get_completion_from_messages(messages):` Utilizes the OpenAI API to get completion suggestions based on the provided messages.
- `process_user_message(user_input, all_messages):` Processes the user's input message, fetches product information, and generates a response for the user. It ensures the response is appropriate by checking it against the Moderation API.
- `Interactive GUI:` The notebook contains an interactive GUI built using the panel library. It captures user input, displays the assistant's responses, and allows for a real-time conversation-like experience.

### JSON products file
The provided JSON file contains detailed information about various products. Here's a breakdown of its structure:

- **Product Identifier**: Each product is uniquely identified by its name.
- **Attributes**: Each product has multiple attributes associated with it:
   - `name`: Name of the product
   - `category`: Category to which the product belongs
   - `brand`: Brand name of the product
   - `model_number`: Model number of the product
   - `warranty`: Warranty period
   - `rating`: Rating out of 5
   - `features`: A list of features associated with the product
   - `description`: A brief description of the product
   - `price`: Price of the product

From a cursory analysis, the JSON primarily contains information about products. The products span various categories like "Computers and Laptops", "Smartphones and Accessories", "Televisions and Home Theater Systems", "Gaming Consoles and Accessories", "Audio Equipment", and "Cameras and Camcorders". 

## Usage
1. Load the Jupyter notebook.
2. Ensure you have the required libraries installed (openai, panel, dotenv, etc.).
3. Set up your .env file with the OpenAI API key.
4. Run the notebook cells to initialize the GUI and start interacting with the assistant.

## Note
This project is designed for learning and demonstration purposes. Error handling and some advanced features (like moderation strictness or response evaluation) can be considered for future versions.
