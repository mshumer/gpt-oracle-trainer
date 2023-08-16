# gpt-oracle-trainer
[![Twitter Follow](https://img.shields.io/twitter/follow/mattshumer_?style=social)](https://twitter.com/mattshumer_) [![Open Main Version In Colab](https://colab.research.google.com/assets/colab-badge.svg)](https://colab.research.google.com/drive/1xB0ZeiBAF78FAxNCz-TeRRwQtmmVjxOh?usp=sharing)

## Overview

Creating a chatbot that can accurately answer questions about a product or service's documentation is a complex task. You can fine-tune on the documentation itself (but results won't be conversational), use embeddings (risks losing relevant context), etc. `gpt-oracle-trainer` is an experimental tool that aims to simplify this process and potentially produce better results.

**Simply provide your product or service's documentation, describe your product or service, select a temperature for data generation, and choose the number of training examples to generate per document. The system will then generate the dataset in the correct format, train the model, and allow you to test it.**

## Features

- **Data Generation**: The system generates a question-and-answer dataset based on your documentation, service description, temperature, and number of examples. The data is formatted correctly for model training.

- **Model Training**: The system trains the model using the generated dataset.

- **Model Testing**: Test the trained model with a custom prompt.

## How to Use
1. [Open the notebook in Google Colab ](https://colab.research.google.com/drive/1xB0ZeiBAF78FAxNCz-TeRRwQtmmVjxOh?usp=sharing)or in a local Jupyter notebook.

2. Add your OpenAI API key to the line `openai.api_key = "OPENAI API KEY HERE"`.

3. Paste your documentation into the `docs` list, each document as a separate string.

4. Define your `service_name_and_description`, `temperature`, and `number_of_examples_per_doc`. For example:

```
service_name_and_description = "MosaicML, a platform that makes it easier to train and fine-tune large AI models"
temperature = .7
number_of_examples_per_doc = 10
```

3. Run the cells to generate the dataset, train the model, and test it.

4. The final trained model will be saved under the name you specify in `new_model`.

## Contributions are welcome! Some ideas:
- improve the data generation process
- add more customization options for the model training

## License

This project is [MIT](https://github.com/mshumer/gpt-oracle-trainer/blob/master/LICENSE) licensed.

## Contact

Matt Shumer - [@mattshumer_](https://twitter.com/mattshumer_)

Project Link: [https://github.com/mshumer/gpt-oracle-trainer](url)

Lastly, if you want to try something even cooler than this, sign up for [Personal Assistant](https://www.hyperwriteai.com/personal-assistant) (most of my time is spent on this). It's basically an AI that can operate your web browser to complete tasks for you.
