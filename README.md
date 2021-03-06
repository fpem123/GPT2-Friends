# GPT2 Friends

[![Run on Ainize](https://ainize.ai/images/run_on_ainize_button.svg)](https://ainize.web.app/redirect?git_repo=https://github.com/fpem123/GPT2-Friends)

This project generate Friends script using GPT-2 model.

You can download the model here: [Hugging face](https://huggingface.co/HScomcom/gpt2-friends/tree/main)

Fine tuning data: [Kaggle](https://www.kaggle.com/divyansh22/friends-tv-show-script)

### Model information

    Base model: gpt-2 large
    Epoch: 30
    Train runtime: 8982.6895 secs
    Loss: 0.0346

### How to use

    * First, Choose Friends character name.
    * Second, Fill what the character will say in text. This will be base of script.
    * And then, Fill number in length. Text is created as long as "length". I recommend between 100 and 300.
    * If length is so big, generate time will be long.

### Post parameter

    name: The Friends character name.
    text: The base of script.
    length: The size of generated text.(min: 50)

### Output foramt

    {"0": [[character name, dialog], [character name, dialog], ...]}


### Image reference

[static/README.md](https://github.com/fpem123/GPT2-Friends/blob/master/static/README.md)

## * With CLI *

#### Input example

    curl -X POST "https://master-gpt2-friends-fpem123.endpoint.ainize.ai/friends" -H "accept: application/json" -H "Content-Type: multipart/form-data" -F "name=Rachel" -F "text=Hello" -F "length=50"

#### Output example

    {
      "0": [
        [
          "Rachel",
          " Hello."
        ],
        [
          "Joey",
          " (on phone) Hey, its Joey!"
        ],
        [
          "Rachel",
          " Hey, Joey! Hey! Ooh! Ooh! I just say someone on the-that looks just like you on the subway. And I was gonna go"
        ]
      ]
    }


## * With swagger *

API page: [Ainize](https://ainize.ai/fpem123/GPT2-Friends?branch=master)

## * With a Demo *

Demo page: [End-point](https://master-gpt2-friends-fpem123.endpoint.ainize.ai/)
