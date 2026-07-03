# Speech Processing Pipeline for Automatic Video Filtering

## Overview

This project implements an end-to-end speech processing pipeline in Python that automatically detects and replaces target words in spoken audio while preserving synchronization with the original video.

The pipeline accepts MP4 videos as input, extracts the audio, generates word-level transcriptions using OpenAI Whisper, identifies target words from the transcript, synthesizes replacement speech using Microsoft Edge TTS, reconstructs the modified audio track, and merges it back with the original video to produce a filtered MP4 output.

The project was completed as part of coursework in speech processing and explores how modern ASR and TTS systems can be combined to automate speech editing tasks.

## Features

* Automatic audio extraction from MP4 video
* Word-level speech transcription using Whisper ASR
* Configurable dictionary of target-word replacements
* Speech synthesis using Microsoft Edge TTS
* Audio reconstruction with timestamp alignment
* Generation of synchronized filtered video
* Optional stereo outputs for comparing original and filtered audio

## Built with

* OpenAI Whisper
* Microsoft Edge TTS
* ffmpeg
* pydub

## Evaluation

The pipeline was evaluated on multiple movie trailers and a longer movie clip using precision, recall, and F1 score based on Whisper-generated transcripts.

During development, I also compared different Whisper models and experimented with fuzzy matching for profanity detection. While fuzzy matching initially appeared promising, testing showed that it introduced  false positives, so it was removed from the final implementation. This iterative evaluation helped improve the overall reliability of the pipeline.

## Current Limitations

This project is intended as a proof of concept rather than a full system pipeline.

Current areas for future improvement include:

* More accurate timestamp alignment
* Better volume normalization
* Voice cloning for more natural replacement speech
* Support for multi-word phrase replacement
* Evaluation on longer-form audio such as full-length films or television episodes

## Repository Contents

This repository includes:

* Python source code
* Technical report
* Sample input videos
* Sample filtered outputs
