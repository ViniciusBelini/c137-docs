---
description: >-
  To start using C137 you must have an API Key. You can create a new key with
  just one click in C137 Console.
---

# 🔑 Get a key

## **Obtain an API Key**

To obtain your API key, please follow the steps below.

1. Create your account on [C137 website.](https://c137.belini.shop/signup)
2. Access the [C137 Console](https://c137.belini.shop/console).
3. Within the submenu, choose the option labeled "Create new key".

## Verify your new API Key

To ensure your new API key is functioning correctly, you can utilize the [C137 Tester](https://c137.belini.shop/tester). The C137 Tester is a dedicated tool for testing the functionality of API keys, allowing you to confirm if your key is valid and properly configured to access the API's resources.

Alternatively, you can test your new API key using a Curl command. Curl is a versatile command-line tool that allows you to send HTTP requests. By constructing a Curl command with your API key and the appropriate endpoint, you can verify its validity and functionality.

```actionscript
KEY="YOUR_KEY"
MODEL_NAME="c137_safe"
curl -H 'Content-Type: application/json' \
     -d '{"text":"Hello, C137!"}' \
     "https://c137.belini.shop/api/text_generate?model_name={MODEL_NAME}&=${KEY}"
```

_Replace 'YOUR\_KEY' with your secret key._
