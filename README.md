# rasa-handoff

**This is just a proof of concept**

Experients with enabling human handoff in Rasa
<img width="719" alt="screenshot 2018-09-28 11 14 53" src="https://user-images.githubusercontent.com/5963656/46217830-12149800-c311-11e8-8567-f3a26cf5fbea.png">


For more information on the Rasa Stack, please visit the docs here:
- [Rasa Core](https://core.rasa.com/)
- [Rasa NLU](https://nlu.rasa.com/)

This project is based on:
- [Rasa Starter Pack](https://github.com/RasaHQ/starter-pack)
- [Rasa Livestream Tensorflow Pipeline](https://github.com/RasaHQ/livestream-tf-pipeline)

## Setup
_You can use `pyenv` to instantiate a virtual environment to run this project_

1. Install the dependencies
```
pip install -r requirements.txt
```

2. Install spacy language model
```
python -m spacy download en
```

3. To run the bot you'll need to create an `.env` file and insert the following
```
MEETUP_KEY=<meetup_api_key>
GOOGLE_KEY=<google_directions_api_key>
```
- [Get Meetup API key here](https://secure.meetup.com/meetup_api/key/)
- [Activate Google Directions API and get API key](https://developers.google.com/maps/documentation/directions/start)


## Usage

To train the NLU model, run ``make train-nlu``

To train the Core model, run ``make train-core``

To run the bot on the command line run ``make cmdline``

## human-in-the-loop
To run mock api:
```
python hitl-api/api.py
```
then ask the bot: "I'm looking for tech meetups in Toronto"

### todo
- [ ] resolve weird behaviour of chatbot responding with incorrect conversation upon resuming conversation when it was paused during hitl
