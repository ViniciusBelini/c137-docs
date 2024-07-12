---
description: This guide will walk you through making a simple POST request to the C137 API.
---

# 🚀 C137 API quickstart

## **Prerequisites**

* A valid C137 API account (sign up for free at  [C137 Signup](https://c137.belini.shop/signup))
* Your preferred programming language and tools (e.g., Python with requests library)

## **Scenario**

Let's say you want to use the C137 API to analyze the sentiment level in a piece of text from 0 to 10.

### **Steps**

1. **Think of the Endpoint:**\
   The specific endpoint for text generation is /text\_generate. It's like a special address in the API where you say what you want to do.
2. **Write a Message:**\
   Imagine you're writing a message to the API. For sentiment analysis, you'd write something like:

```json
{
    "instructions": "Analyze the level of sentiment in a section of text from 0 to 10.",
    "text": "This is a fantastic API! I highly recommend it."
}
```

3. **Send the Message:**\
   Now, use your programming tools to "send" this message to the API's address. This is where things get technical, but don't worry, there are tools to help!

```python
import requests

KEY = "YOUR_KEY"
MODEL_NAME = "c137_safe"

url = "https://c137.belini.shop/api/generateText"
headers = {'Content-Type': 'application/json'}
data = {
    "instructions": "Analyze the level of sentiment in a section of text from 0 to 10.",
    "text": "This is a fantastic API! I highly recommend it.",
    "key": KEY,
    "model_name": MODEL_NAME
}

response = requests.post(url, headers=headers, json=data)

print(response.json())
```

If your key is valid, after executing the code above the response will look like this:

{% hint style="success" %}
```json
{
    "status": "success",
    "response": 200,
    "text": "The sentiment in this text is 10/10. It expresses strong positive sentiment with words like \"fantastic\" and \"highly recommend\"."
    ...
}
```
{% endhint %}

In case of any error, you will see something like:

{% hint style="danger" %}
```json
{
    "status": "error",
    "response": 401,
    "msg": ...
}
```
{% endhint %}

Browse the documentation to understand how each endpoint works or to troubleshoot errors.
