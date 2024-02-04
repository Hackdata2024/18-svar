# HACKDATA-SNU


# SVAR - AI-Driven Speech Therapy App

## Project Description

SVAR is a groundbreaking speech therapy application that leverages the power of Artificial Intelligence to automate and personalize the speech therapy process. Designed with both therapists and patients in mind, SVAR aims to make speech therapy more accessible, efficient, and effective. By utilizing advanced AI algorithms and speech recognition technology, the app provides real-time feedback, personalized therapy sessions, and progress tracking, addressing a wide range of speech disorders in users of all ages.

## Technological Stack

- **Frontend**: Flutter
- **Backend**: Python, Flask (for API services), Firebase (Database), AWS (Hosting)
- **AI/ML**: PyTorch for developing AI model

## Team

- **Tejas Kumar** 
- **Ujjwal Mathur** 
- **Vikash Meena** 
- **Anurag Tiwari** 

## How to Run the Project

2. **Navigate to the project directory**: `cd svar`
3. Install flutter and dart in your system, and also install python and pip in your system.
4. **Install the dependencies**: `flutter pub get`
5. **Run the app**: `flutter run`   

6. **Navigate to the backend directory**: `cd Voice_ml`
7. run the python file `test.py` to start test ing the ml model on the given data, it will generate the test data and plots in logs and plots folder respectively.


## Core Code Explanation

The core of SVAR's functionality lies in its AI-driven speech analysis and therapy recommendation engine. 

We have Developped an extensive AI model that can analyze speech patterns and identify speech disorders. The model is trained on a large dataset of speech samples and uses advanced machine learning algorithms to identify patterns and anomalies in the user's speech. With these insights, SVAR can provide personalized therapy recommendations and track the user's progress over time.

in `Voice_ml` folder we have the code for the AI model in wav2vec2.py, the model class `ASTSvar` is the architecture of the model, it utilizes the `wav2vec2` model from `transformers` library, the state of the art architecture, also behind `chatGPT` and other LLMs. We have collected the voice samples from internet for pronoucing phonemes and trained the model on it, the model is trained on 40 phonemes, and can be extended to more phonemes, and the accuracy is 98.5% on the test data, the model is saved in `model` folder, and can be used for testing and prediction.

`We have hosted this model on EC2 instance of AWS, and the API is developed using Flask, the flutter app sends the voice data to the API, and the API sends the prediction back to the app, the code for the API is in `server.py` file, and the model is loaded in the API and the prediction is made, and sent back to the app.`

To make it kids freindly we have also added a feature of game in the app, with the help of flutter, the design of the game is also done in figma, the link to the design is given in `figma.md` .

In flutter we have built our own custom widgets for the app, with the game like looks for child.
To go through app code, go to `svar/lib` folder, the Readme of Svar app is in `svar/README.md` file, which explains the file structure. 