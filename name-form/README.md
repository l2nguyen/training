# Name form bot

This is a simple example of a form and slot validation. 

Note: This uses Rasa 3.0.x

## What’s inside this example?

The bot consists of the following files:

- **data/nlu.yml** contains training examples for the NLU model
- **data/rules.yml** contains training rules for the Core model
- **actions/actions.py** contains the implementation of a form validation using `FormValidationAction`
- **config.yml** contains the model configuration
- **domain.yml** contains the domain of the assistant
- **endpoints.yml** contains the webhook configuration for the custom actions

## How to use this example?

1. Train a Rasa model containing the Rasa NLU and Rasa Core models by running:
    ```
    rasa train
    ```
    The model will be stored in the `/models` directory as a zipped file.

2. Test the assistant by running:
    ```
    rasa run actions
    rasa shell
    ```
    This will load the assistant in your command line for you to chat.

For more information about the individual commands, please check out our
[documentation](http://rasa.com/docs/rasa/command-line-interface).

3. To activate the name form, use the `request_names` intent by either typing `/request_names` or typing `i want to give you my name`
