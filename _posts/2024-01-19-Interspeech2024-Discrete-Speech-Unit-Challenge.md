---
layout: post
title: Interspeech2024 Speech Processing Using Discrete Speech Unit Challenge
description: This is the Interspeech2024 challenge website for speech processing using discrete speech unit challenge
date: 2024-01-19 09:00:00-0800
comments: false
---

<!---
### The Challenge Overview

Description here
--->

## Introduction

In conventional speech processing approaches, models typically take either raw waveforms or high-dimensional features derived from these waveforms as input. For instance, spectral speech features continue to be widely employed, while learning-based deep neural network features have gained prominence in recent years. A promising alternative arises in the form of discrete speech representation, where speech signals within a temporal window can be represented by a single index $d$ within a range $K$: $d \in \{1, 2, \dots, K\}$.

Three challenging tasks are proposed for using discrete speech representations. 
    1. Automatic speech recognition (ASR): We will evaluate the ASR performance of the proposed systems on the proposed data.
    2. Text-to-speech (TTS): We will evaluate the quality of the generated speech.
    3. Singing voice synthesis (SVS): We will evaluate the quality of the synthesized singing voice.


Participation is open to all. Each team can participate in any task. This challenge has preliminarily been accepted as a special session for Interspeech 2024, and participants are strongly encouraged to submit papers to the special session. The focus of the special session is to promote the adoption of discrete speech representations and encourages novel insights.

<!---
### Resources
--->

## Resources


### Baseline systems & toolkits
- [Automatic speech recognition (ASR)](https://github.com/simpleoier/espnet/tree/is2024_dsu_asr2/egs2/interspeech2024_dsu_challenge/asr2)
- [Text-to-speech (TTS)](https://github.com/espnet/espnet/tree/tts2/egs2/ljspeech/tts2)
- [Singing voice synthesis (SVS)](https://github.com/A-Quarter-Mile/espnet/tree/tmp_muskit/egs2/opencpop/svs2)
- [Discrete vocoder training](https://github.com/kan-bayashi/ParallelWaveGAN)

### Dataset

- ASR: [Librispeech](https://www.openslr.org/12) and [ML-SUPERB](https://drive.google.com/file/d/1zslKQwadZaYWXAmfBCvlos9BVQ9k6PHT/view?usp=sharing)
- TTS: [LJSpeech](https://keithito.com/LJ-Speech-Dataset/) and [Expresso](https://speechbot.github.io/expresso/)
- SVS: [Opencpop](https://wenet.org.cn/opencpop/)


<!-- ### Rules
* For each task, the training data must follow the baseline systems. However, there is no constraint on the data used in the foundation models.
* For submission, more details will be provided later for each task.
 -->

## Detailed tracks and rules

### ASR Challenge

* Data
* Framework
* Evaluation metrics
* Submission

### TTS Challenge

* Data
* Framework
* Evaluation metrics
* Submission

### SVS Challenge

* Data
* Framework
* Evaluation metrics
* Submission

### Research in discrete representation of speech and audio

* Call for research papers: As a special session, the track also accepts research papers in discrete representation of speech and audio. The paper could be related to any of the following topics:
  * Discrete speech/audio/music representation learning
  * Discrete representation application for any speech/audio processing downstream tasks (ASR, TTS, etc.)
  * Evaluation of speech/audio discrete representation
  * Efficient discrete speech/audio discrete representation
  * Interpretability in discrete speech/audio discrete representation
  * Other novel usage of discrete representation in speech/audio

##  Paper submission

Papers for Interspeech Special Session have to be submitted following the same schedule and procedure as regular papers of [INTERSPEECH 2024](https://interspeech2024.org/). The submitted papers will undergo the same review process by anonymous and independent reviewers.

Submission URL : (TBA)

<!---
### Schedules
--->

## Important dates
The schedule for the challenge is as follows
* Feb 20, 2024: Leaderboard is online and accepting submissions
* Mar  2, 2024: Paper Submission Deadline
* Mar  9, 2024: Paper Revision Deadline
* After Mar. 9: Leaderboard will still be open and new submissions will be evaluated

<!---
### Organizers
--->

## Organizers

* Xuankai Chang (Carnegie Mellon University, U.S.)
* Jiatong Shi (Carnegie Mellon University, U.S.)
* Shinji Watanabe (Carnegie Mellon University, U.S.)
* Yossi Adi (Hebrew University, Israel)
* Xie Chen (Shanghai Jiao Tong University, China)
* Qin Jin (Renmin University of China, China)