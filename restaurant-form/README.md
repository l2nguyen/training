# Restaurant form bot

Example of form 

Note: This uses Rasa 3.x

## What’s inside this example?

The bot consists of the following files:

- **actions/actions.py** contains code to validate form
- **data/nlu.yml** contains training examples for the NLU model
- **data/rules.yml** contains training rules for the Core model
- **config.yml** contains the model configuration
- **domain.yml** contains the domain of the assistant
- **endpoints.yml** contains the webhook configuration for the custom actions

## How to use this example?

1. Train a Rasa model containing the Rasa NLU and Rasa Core models by running:
    ```
    rasa train
    ```
    The model will be stored in the `/models` directory as a zipped file.

2. Run an instance of [duckling](https://rasa.com/docs/rasa/nlu/components/#ducklingentityextractor)
   on port 8000 by either running the docker command
   ```
   docker run -p 8000:8000 rasa/duckling
   ```
   or [installing duckling](https://github.com/facebook/duckling#requirements) directly on your machine and starting the server.


3. Start your action server
   ```
   rasa run actions
   ```

4. Test the assistant by running:
    ```
    rasa shell
    ```
    This will load the assistant in your command line for you to chat.

For more information about the individual commands, please check out our
[documentation](http://rasa.com/docs/rasa/command-line-interface).

5. To activate form, say something that would trigger the `request_restaurant` intent to the bot.
