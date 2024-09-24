# LLaMA Model Usage on AWS Bedrock

This repository contains a Python script that demonstrates how to use LLMAa model on AWS bedrock. It's a simple example that generates recipes using a list of ingredients. The script interacts with an AWS Bedrock Runtime client to generate the recipe in JSON format, conforming to a predefined schema. You can use this as a starting point to build your own application, of course you can change the schema, model, and prompt to fit your needs!

## Prerequisites

- Python 3.7+
- AWS account with access to Bedrock Runtime
- AWS credentials (Access Key ID and Secret Access Key)
- `boto3` library
- `pydantic` library
- `python-dotenv` library

## Installation

1. Clone the repository:
    ```sh
    git clone https://github.com/yourusername/recipe-generator.git
    cd recipe-generator
    ```

2. Create a virtual environment and activate it:
    ```sh
    python -m venv venv
    source venv/bin/activate  # On Windows, use `venv\Scripts\activate`
    ```

3. Install the required packages:
    ```sh
    pip install -r requirements.txt
    ```

4. Create a `.env` file in the root directory of the project and add your AWS credentials:
    ```env
    AWS_ACCESS_KEY_ID=your_access_key_id
    AWS_SECRET_ACCESS_KEY=your_secret_access_key
    AWS_REGION=your_aws_region
    ```

## Usage

1. Run the script:
    ```sh
    python recipe_generator.py
    ```

2. The script will generate a recipe using the specified ingredients and print it in JSON format.

## Example
```sh
python recipe_generator.py
```
```json
{
"name": "Chicken and Rice Bowl",
    "ingredients": [
        "1 lb boneless, skinless chicken breast or thighs",
        "2 cups cooked white or brown rice",
        "2 bell peppers (any color), sliced",
        "1 large onion, sliced"
    ],
    "instructions": [
        "Heat 2 tablespoons of oil in a large skillet over medium-high heat.",
        "Add the sliced onions and cook until they're translucent and starting to caramelize, about 5 minutes.",
        "Add the sliced bell peppers and cook for another 5 minutes, until they're tender.",
        "Add the chicken to the skillet and cook until it's browned and cooked through, about 5-7 minutes.",
        "Serve the chicken and vegetables over the cooked rice."
    ]
}
```