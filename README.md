# Building-a-Censoring-Pipeline-for-Movie-Trailers-and-Movie-Clips

This project uses a pipeline built in Python that takes in videos of varying lengths and
applies a filtering system. Whisper AI is used to transcribe the audio and flags chosen profanity.
Replacement words are reinserted into the audio using edge-tts and then the audio and video are
merged together to create one single censored mp4 file. While it does have base functionality,
improvements such as better volume and timestamp matching could be added to the pipeline for
an improved and efficient filtering system.
