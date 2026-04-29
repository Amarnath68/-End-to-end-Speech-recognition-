# -End-to-end-Speech-recognition-
# README.md

# Speech Recognition System using RNN + Seq2Seq + Attention + KenLM

This project is a Deep Learning based Speech Recognition System built using **PyTorch**, **Librosa**, and **KenLM**.
It converts speech audio (`.wav`) into text transcripts using:

* Acoustic Model (LSTM-based RNN)
* Seq2Seq Decoder with Attention
* Beam Search Decoder
* Optional KenLM Language Model
* Word Error Rate (WER) Evaluation

The system is trained using the **LJSpeech Dataset** and performs preprocessing like:

* Voice Activity Detection (VAD)
* Noise Reduction
* MFCC Feature Extraction
* Audio Normalization
* Pre-emphasis

Based on the uploaded code 

---

# Features

## Audio Preprocessing

* Pre-emphasis
* Audio normalization
* Voice Activity Detection (VAD)
* Noise reduction
* MFCC feature extraction

## Acoustic Model

* LSTM-based RNN
* Learns speech acoustic patterns

## Seq2Seq Decoder

* Encoder-Decoder architecture
* Attention mechanism included

## Decoding

* Greedy decoding
* Beam Search decoding
* Optional KenLM Language Model support

## Evaluation

* Word Error Rate (WER)

## Model Saving

* `acoustic_model.pkl`
* `seq2seq_decoder.pkl`

---

# Technologies Used

* Python
* PyTorch
* Librosa
* NumPy
* KenLM
* CSV
* Pickle
* TQDM

---

# Dataset Used

## LJSpeech Dataset

Path used in code:

```python
/content/dataset/LJSpeech-1.1/
```

Contains:

* `.wav` files
* `metadata.csv`

---

# Project Structure

```text
project/
│
├── main.py
├── acoustic_model.pkl
├── seq2seq_decoder.pkl
├── metadata.csv
├── wavs/
│   ├── LJ001-0001.wav
│   ├── LJ001-0002.wav
│   └── ...
│
└── README.md
```

---

# Installation

## Step 1: Clone Project

```bash
git clone your-repository-link
cd project-folder
```

## Step 2: Install Requirements

```bash
pip install torch librosa numpy tqdm kenlm
```

---

# How to Run

## Training

```bash
python main.py
```

This will:

* Extract transcripts
* Load dataset
* Train Acoustic Model
* Train Seq2Seq Decoder
* Save models

---

# Inference

Example test file:

```python
test_file = "/content/dataset/LJSpeech-1.1/wavs/LJ001-0001.wav"
```

Output:

```text
Predicted text: Hello world
```

---

# Word Error Rate (WER)

WER is used to evaluate prediction quality.

Formula:

```text
WER = (Substitutions + Insertions + Deletions) / Total Words
```

Lower WER = Better Accuracy

---

# Future Improvements

* CTC Loss integration
* Transformer-based ASR
* Better language model
* Real-time microphone input
* Deployment using Streamlit / Flask
* GPU optimization

---

# Author

Developed for Deep Learning based Speech Recognition Project

Using:

RNN + Seq2Seq + Attention + KenLM

---

# License

This project is for Educational and Research purposes only.
