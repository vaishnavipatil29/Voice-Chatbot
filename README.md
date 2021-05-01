# Voice-Chatbot

Course Project done in Speech Processing Course.

The chatbot has 2 features:
1. Question and Answer
2. Speaker Recognition

Option 1: QnA
The overall work it does is: 
1) Receive audio input from user. Convert the audio array into .wav file.
2) Speech recognition of .wav file through get_large_audio_transcription(). [Converting it into text form]
3) Searching for its answers from the processed Corpus, and returning the output.

Corupus used: intro.txt file

Option 2: Speaker Recognition

Work:
Input number of samples, chatbot takes the input and chooses the samples randomly and recognises speakers.

Objective: Classify speakers from the frequency domain representation of speech recordings, obtained via Fast Fourier Transform (FFT).

Dataset: https://www.kaggle.com/kongaevans/speaker-recognition-dataset
5 speakers: (each 1500 audio files, each 1 second long and sampled at 16000 Hz)
Background noise (2 folders, 6 files, longer than 1 sec, need to resample them to 16k Hz)

Procedure used:
1. Prepare a dataset of speech samples from different speakers, with the speaker as a label.
2. Add background noise to these samples to augment our data.
3. Take the FFT of these samples.
4. Train a 1D convnet to predict the correct speaker given a noisy FFT speech sample

Reference: https://blog.usejournal.com/create-a-voice-chatbot-in-python-using-nltk-speech-recognition-google-text-to-speech-445468c083f8
