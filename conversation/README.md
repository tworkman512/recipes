# Conversation

> Chat with TJ!

This recipe uses the [Watson Conversation](https://www.ibm.com/watson/developercloud/conversation.html) and [Watson Text to Speech](https://www.ibm.com/watson/developercloud/text-to-speech.html) services to turn TJ into a chatting robot.

## Hardware

This recipe requires a TJBot with a microphone and a speaker.

[This instructable] (http://www.instructables.com/id/Build-a-Talking-Robot-With-Watson-and-Raspberry-Pi/) provides step-by-step instructions for preparing your TJBot to use this recipe.

## Build and Run

First, make sure you have configured your Raspberry Pi for TJBot.

    $ cd tjbot/bootstrap && sudo sh bootstrap.sh

Go to the `recipes/conversation` folder.

    $ cd ../recipes/conversation

Create instances of the [Watson Conversation](https://www.ibm.com/watson/developercloud/conversation.html) and [Watson Text to Speech](https://www.ibm.com/watson/developercloud/text-to-speech.html) services and note the authentication credentials.

Import the `workspace-sample.json` file into the Watson Conversation service and note the workspace ID.

Make a copy the default configuration file and update it with the Watson service credentials and the conversation workspace ID.

    $ cp config.default.js config.js
    $ nano config.js
    <enter your credentials and the conversation workspace ID in the specified places>

Run!

    sudo node conversation.js

# Watson Services

- [Watson Conversation](https://www.ibm.com/watson/developercloud/conversation.html)
- [Watson Text to Speech](https://www.ibm.com/watson/developercloud/text-to-speech.html)

# License

This library is licensed under Apache 2.0. Full license text is available in [LICENSE](../../LICENSE).

# Contributing

See [CONTRIBUTING.md](../../CONTRIBUTING.md).
