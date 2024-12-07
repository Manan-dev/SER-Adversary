# ECE 469/569 Final Project -- Exploiting Vulnerabilities in Emotion Recognition for Health Monitoring Systems
by Zachary Perry, Manan Patel, Jaehwan Park, Jennifer Maranville


### Dataset -- RAVDESS Dataset
---
This portion of the RAVDESS dataset contains 1440 audio files made up of 60 trials from 24 different actors. Each audio file contains audio of one of the actors vocalizing statements with a particular emotion. These emotions include calm, happy, sad, angry, fearful, surprise, and disgust. Each emotion is captured twice with different levels of intensity.

For more information, please visit: https://www.kaggle.com/datasets/uwrfkaggler/ravdess-emotional-speech-audio

### Approach
---
We decided to create and train our own CNN model with this dataset for emotion classification via audio clips. Doing so involved data processing (of the audio files), training of our model, testing, and supporting the ability to give it an audio file and have it classify correctly.

### Attacks
---
To exploit our CNN and attack the emotion classification, we utilized two different, untargeted attacks: 
1. FGSM
2. PGD

The goal was to create adversarial audio examples and get the model to make the wrong prediction.

### Running the code
---
All code is contained within `main.ipynb`. The dataset is also included in this repo. Any dependencies that are needed can be uncommented and downloaded within the notebook.
Additionally, we have included example outputs within the `adversarial_outputs/` directory. Lastly, we also provide a pretrained model (85% testing accuracy) that can be loaded and used. It's called `model.h5`. We ran multiple training session for ~12hrs and saved the best one, this one being the best.

NOTE: If you are wanting to train your own model, then you will need to rename `model.h5`, as, currently, if it exists, it will use this.
