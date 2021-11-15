![Image](https://github.com/Clevrai/Clevr/blob/main/clevr-api.png)

# Clevr Python Library

Welcome! This is the official repository for the Clevr Python 3 package to access the developer API. This package includes prebuilt classes and methods to quickly make calls to our API and integrate into your backend.

## Documentation

See the [Official API documentation](https://beta.clevr-ai.com/docs) for more examples.

## Installation
To install this package, run this command in your terminal:

```sh
pip install clevr
```

## Usage

Before using the Clevr SDK/Developer API, you must have created an account to get an API key. During our beta, each account recieves 250 free API calls for the first 3 months.

Recommended setup:

```python
import clevr
import os

key = os.environ.get("CLEVR-API-KEY")
```

### Quickstart

To get started, use the Athena API for realtime image classification
```python
import clevr
import os

key = os.environ.get("CLEVR-API-KEY")

clevr.Athena.classification(
  api_key=key,
  
  learning_object={
    "image": {
      "cat": [
        "cat-example1.jpg",
        "cat-example2.jpg",
        "cat-example3.jpg"
       ],
       
       "dog": [
        "cat-example1.jpg",
        "cat-example2.jpg",
        "cat-example3.jpg"
       ],
     },
     
     input_val={"image": "cat-inference-image.jpg"}
)
```


## Requirements

- Python 3.7.0+

If you experience any issues, please let us know at [our support form](https://beta.clevr-ai.com/support) 


## Feedback
We always appreciate feedback about how we could improve our products. Please submit feedback through your account's dashboard!
