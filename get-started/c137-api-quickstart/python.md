---
description: >-
  This quickstart shows you how to get started with the C137 API using the
  Python request.
---

# 🐍 Python

## Quickstart: Python Requests

This quickstart demonstrates how to use the C137 API with Python's `requests` library.

### Requirements:

* Python 3.6 or later
* `requests` library: `pip install requests`

### Steps:

1. Obtain your API key: Visit the C137 Console to obtain your unique API key.
2. Import necessary libraries:

```python
import requests
```

3. Make API requests:

```python
# Replace 'YOUR_API_KEY' with your actual API key
URL = "https://c137.belini.shop/api/generateText"
KEY = "YOUR_API_KEY"

data = {
    "key": KEY,
    "text": "List 5 big countries."
}

response = requests.post(URL, data=data)

print(f'Status: {response.status_code}')

print('------------------------------------------')
print(response.text)
print('------------------------------------------')
```

### Explanation:

\* The \`requests.post()\` function sends a POST request to the specified URL.\
\* The \`response\` object contains the server's response.\
\* \`response.status\_code\` indicates the HTTP status code (e.g., 200 for success).\
\* \`response.json()\` converts the response content into a Python dictionary.

## Further exploration:

* Consult the official C137 API documentation for a complete list of endpoints and their parameters:
* Use Python libraries like `json` to manipulate the response data more effectively.
