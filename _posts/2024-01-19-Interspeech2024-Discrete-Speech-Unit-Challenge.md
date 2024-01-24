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


### Track-specific dataset

- ASR: [Librispeech](https://www.openslr.org/12) and [ML-SUPERB](https://drive.google.com/file/d/1zslKQwadZaYWXAmfBCvlos9BVQ9k6PHT/view?usp=sharing)
- TTS: [LJSpeech](https://keithito.com/LJ-Speech-Dataset/) and [Expresso](https://speechbot.github.io/expresso/)
- SVS: [Opencpop](https://wenet.org.cn/opencpop/)


### Data for discrete representation learning and extraction
- General Policy: There are no restrictions on using datasets for learning and extracting discrete representations. This applies broadly to all datasets.

- Specific Restrictions for Supervision Data: The key restriction is on using test sets from certain datasets for supervision in specific tasks. Specifically:
  - Automatic Speech Recognition (ASR): The test sets of the Librispeech and ML-SUPERB datasets cannot be used for learning the discrete representation. However, their training sets are permissible.
  - Text-to-Speech (TTS): The test sets of the LJSpeech and Expresso datasets are off-limits for discrete representation learning, but their training sets can be used. For TTS training, phone alignment information for non-autoregressive training can be also used in training phase.
  - Singing Voice Synthesis (SVS): The test set of the Opencpop dataset is restricted for use in discrete representation learning, though the training set is allowed.

<!-- ### Rules
* For each task, the training data must follow the baseline systems. However, there is no constraint on the data used in the foundation models.
* For submission, more details will be provided later for each task.
 -->

## Detailed tracks and rules

### ASR Challenge

* Data: LibriSpeech_100 + ML-SUPERBB 1h set
* Framework: We recommend to use ESPnet for fair comparison. Feel free to let us know your preferrence.
* Evaluation metrics: Word Error Rates (WERs) on Librispeech dev/test sets and Character Error Rates (CERs) on ML-SUPERB.
* Ranking: 
  * Word/Character Error Rate: The primary method for ranking all systems is based on their Word/Character Error Rate. This metric measures the performance of a system in terms of the accuracy of the words recognized or generated compared to a reference. 
  * Efficiency of discrete tokens (bitrate): In addition to WER, the efficiency of discrete tokens in the systems will also be evaluated and ranked based on bitrate.
* Submission
  * Submission package details:
    1. The discrete speech units corresponding to the test sets in kaldi format.
    2. The predicted transcription corresponding to the test sets.
    3. A technical report in Interspeech2024 paper format (no length limit)

### TTS Challenge - Acoustic+Vocoder

* Data: LJSpeech, following the train-dev-test split in [here](https://github.com/ftshijt/Interspeech2024_DiscreteSpeechChallenge).
* Framework: No framework or model restriction in TTS-Acoustic+Vocoder challenge, but the organizers have prepared the baseline training scripts (baseline model to be released soon) in [ESPnet](https://github.com/espnet/espnet/tree/tts2/egs2/ljspeech/tts2).
* Evaluation metrics: Mean cepstral distortion, F0 root mean square error, Bitrate, [UTMOS](https://github.com/sarulab-speech/UTMOS22/tree/master)
* Ranking:
  * UTMOS: The The primary method for ranking all systems is based on their UTMOS score.
  * Efficiency of discrete tokens (bitrate): the efficiency of discrete tokens in the systems will also be evaluated and ranked based on bitrate.
* Submission
   * Submission package details:
     * The synthesized voice of LJSpeech test set using full training set (with at least 16kHz).
     * The synthesized voice of LJSpeech test set using 1-hour training set (with at least 16kHz).
     * The discrete representation corresponding to the test set
     * A technical report in Interspeech2024 paper format (no length limit)
   * Notes:
     * We encourage participants to additional contrast results in addition to their primary submission. However, due to the budget, we cannot gaurantee those all submitted results will be evaluated in the subjective metric.
     * More details about the submission process will be updated later.


### TTS Challenge - Vocoder

* Data: Expresso, following the train-dev-test split in [here](https://github.com/ftshijt/Interspeech2024_DiscreteSpeechChallenge) (Note that this is different from the original train-dev-test split in the benchmark paper).
* Framework: No framework or model restriction in TTS-Vocoder challenge, but the organizers have prepared the baseline training scripts (baseline model to be released soon) in [ESPnet](https://github.com/espnet/espnet/tree/tts2/egs2/ljspeech/tts2) and [ParallelWaveGAN](https://github.com/kan-bayashi/ParallelWaveGAN).
* Evaluation metrics: Mean cepstral distortion, F0 root mean square error, Bitrate, [UTMOS](https://github.com/sarulab-speech/UTMOS22/tree/master)
* Ranking:
  * UTMOS: The The primary method for ranking all systems is based on their UTMOS score.
  * Efficiency of discrete tokens (bitrate): the efficiency of discrete tokens in the systems will also be evaluated and ranked based on bitrate.
* Submission
   * Submission package details:
     * The synthesized voice of LJSpeech test set using full training set (with at least 16kHz).
     * The discrete representation corresponding to the test set
     * A technical report in Interspeech2024 paper format (no length limit)
   * Notes:
     * We encourage participants to additional contrast results in addition to their primary submission. However, due to the budget, we cannot gaurantee those all submitted results will be evaluated in the subjective metric.
     * More details about the submission process will be updated later.


### SVS Challenge

* Data: Opencpop, following the original segmentation and train/test split.
* Framework: No framework or model restriction in SVS challenge, but the organizers have prepared the baseline training scripts (baseline model to be released soon) in [ESPnet-Muskits](https://github.com/A-Quarter-Mile/espnet/tree/tmp_muskit/egs2/opencpop/svs2).
* Evaluation metrics
   * Objective metrics: Mean cepstral distortion, F0 root mean square error, Bitrate for efficiency measure
   * Subjective metrics: Mean Opinion Score (MOS) by organizers
* Ranking:
  * MOS: The The primary method for ranking all systems is based on their MOS score.
  * Efficiency of discrete tokens (bitrate): the efficiency of discrete tokens in the systems will also be evaluated and ranked based on bitrate.
* Submission
   * Submission package details:
     * The synthesized voice of Opencpop test set (with at least 16kHz)
     * The discrete representation corresponding to the test set
     * A technical report in Interspeech2024 paper format (no length limit)
   * Notes:
     * We encourage participants to additional contrast results in addition to their primary submission. However, due to the budget, we cannot gaurantee those all submitted results will be evaluated in the subjective metric.
     * More details about the submission process will be updated later.


### Research in discrete representation of speech and audio

* Call for research papers: As a special session, the track also accepts research papers in discrete representation of speech and audio. The paper could be related to any of the following topics:
  * Discrete speech/audio/music representation learning
  * Discrete representation application for any speech/audio processing downstream tasks (ASR, TTS, etc.)
  * Evaluation of speech/audio discrete representation
  * Efficient discrete speech/audio discrete representation
  * Interpretability in discrete speech/audio discrete representation
  * Other novel usage of discrete representation in speech/audio
* Please refer to the "Paper submission" section for detail guidance of paper submission.


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

## Contact
- discrete_speech_challenge@googlegroups.com
