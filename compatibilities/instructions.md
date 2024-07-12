# 📖 Instructions

Instructions are a powerful tool that allows you to customize the behavior of your AI model and influence the way it interacts with you. By providing instructions during initialization, you can shape the model's responses, persona, and overall tone.

## How Instructions Work

Instructions are simple text prompts that are fed to the model alongside your input text. The model processes both the instructions and the input, using them to generate its response.

## Types of Instructions

You can use instructions to define various aspects of your model's behavior, including:

* Persona: Define a specific role or identity for the model, such as a teacher, a lawyer, a poet, or a fictional character.
* Tone and Style: Specify the tone and style of the model's responses, for example, formal, informal, humorous, or poetic.
* Knowledge Domain: Guide the model to focus on a specific area of expertise, such as history, science, literature, or a particular industry.
* Formatting: Specify the desired output format, like bullet points, numbered lists, or code snippets.
* Constraints: Set boundaries for the model's responses, like limiting the number of words or characters, or preventing the use of certain words or phrases.

## Examples

Here are some examples of how you can use instructions to customize your model's behavior:

* **Persona:**
  * `"You are a friendly and helpful chatbot designed to answer questions about history."`
* **Tone and Style:**
  * `"Speak like a Shakespearean bard."`
* **Knowledge Domain:**
  * `"Focus your responses on the field of artificial intelligence."`
* **Formatting:**
  * `"Please provide your answer in a numbered list."`
* **Constraints:**
  * `"Limit your responses to 100 words."`

## Best Practices

* Be clear and concise: Use simple language and avoid ambiguity in your instructions.
* Use specific examples: Illustrate your desired behavior with concrete examples.
* Experiment with different instructions: Test different combinations of instructions to find what works best for your needs.
* Avoid overly complex instructions: Keep instructions simple and focused on a single aspect of the model's behavior.

## Basic Example

To include an instruction in your request, simply add a key-value pair to your request. The key should be "instructions" and the value should be the instruction you want to provide.

Here's a Python example:

```python
import requests

URL = "https://c137.belini.shop/api/generateText"
KEY = "YOUR KEY HERE"

INSTRUCTIONS = "Please provide your answer in a numbered list."

data = {
    "key": KEY,
    "instructions": INSTRUCTIONS,
    "text": "List 5 big countries."
}

response = requests.post(URL, data=data)

print(f'Status: {response.status_code}')

print('------------------------------------------')
print(response.text)
print('------------------------------------------')
```

If your key is valid, the response will look something like this:

{% hint style="success" %}
```json
{
    "status": "success",
    "code": 200,
    "message": "All working successfully.",
    "generated_text": "Here are 5 big countries, based on population:\n\n1.  **China**\n2.  **India**\n3.  **United States**\n4.  **Indonesia**\n5.  **Pakistan** \n"
}
```
{% endhint %}
