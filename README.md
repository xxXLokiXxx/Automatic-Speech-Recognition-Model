# Automatic Speech Recognition Model

!ASR

## Table of Contents
- Introduction
- Features
- Data and Resources
- Evaluation and Analysis
- Tasks
- Contributing
- License
  
## Introduction
The Automatic Speech Recognition (ASR) Model is designed to convert spoken language into text. It leverages advanced machine learning techniques to achieve high accuracy and efficiency.

## Features
- **High Accuracy**: Utilizes state-of-the-art algorithms for precise speech recognition.
- **Real-time Processing**: Capable of processing audio in real-time.
- **Multilingual Support**: Supports multiple languages for diverse applications.

## Data and Resources
- **Data**: A small collection of recordings from ASR students, comprising short utterances with words randomly selected from the phrase: "Peter Piper picked a peck of pickled peppers. Where’s the peck of pickled peppers Peter Piper picked?" (Casing and punctuation can be ignored.)
- **Resources Provided**:
    - Pronunciation dictionary (`lexicon.txt`) and phone list (`phonelist.txt`) for all words in the vocabulary.
    - Pre-trained neural network for computing pseudo-likelihoods.
    - Modules for observation probabilities and Word Error Rate (WER) computation.

## Evaluation and Analysis
In your experimental work and report, consider the following:
1. **Word Error Rate (WER)**: Measure the accuracy of the output using WER.
2. **Decoding Speed**: Estimate the time taken by the Viterbi decoder.
3. **Memory Usage**: Provide counts of states and arcs in the WFST.

## Tasks
### Task 1 – Initial Systems
- Perform baseline experiments using your Viterbi decoder and a WFST recognizing any sequence of words from the vocabulary.
- Analyze results based on WER and other measures.

### Task 2 – System Tuning
- Adjust WFST parameters to improve results.

## Contributing
Contributions are welcome! Please fork the repository and submit a pull request.

## License
This project is licensed under the MIT License. See the LICENSE file for details.
