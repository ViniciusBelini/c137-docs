---
description: >-
  This quickstart shows you how to get started with the C137 API using the
  Python SDK.
---

# 🐍 Python

## Install the SDK <a href="#install-sdk" id="install-sdk"></a>

You can install the Python SDK for C137 API in the C137 package. install the dependency using pip:

```python
pip install c137
```

## Generating the first text

After installing the SDK you will be able to generate texts simply and quickly, but first you will have to configure the model like the example below:

```python
import c137

model = c137.configure(
    key="YOUR_API_KEY",
    model_name="c137_safe"
)
```

* **key:** Your secrete API key
* **model\_name:** The model that will proccess your input (see the list here)

### Generate text

After all, you can quickly generate your text using the code below:

```python
response = model.text_generate("Why is the sky blue?")
```

Now you can generate texts using AI quickly and simply.
