# Automatic Speech Recognition Model

![a4240093-b609-47be-be25-58bc3859cc16](https://github.com/xxXLokiXxx/Automatic-Speech-Recognition-Model/assets/99037815/047854e1-8efc-41da-a35f-6b73740f5035)


## Table of Contents
- Introduction
- Features
- Data and Resources
- Evaluation and Analysis
- Tasks
- Experiment Results
- Installation
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
    - **Self-loop Probabilities**: Experiment with different self-loop probabilities to see their effect on WER.
    - **Final Probabilities**: Adjust the final state probabilities to optimize the likelihood of the correct path.
    - **Silence State**: Incorporate a silence state to model gaps between words and reduce insertion errors.

### Task 3 – Pruning
- Implement a pruning threshold in the forward_step function to reduce computational complexity and improve decoding speed.

### Task 4 – Advanced Topics
- **Improving the Lexicon**: Modify the lexicon to allow for multiple pronunciations of words.
- **Tree-structured Lexicon**: Use the OpenFST determinize function to create a more efficient tree-structured lexicon.
- **Bigram Language Model**: Implement a bigram language model to consider word transitions and improve recognition accuracy.

## Experiment Results

### Baseline Model
- **WER**: 144.88%
- **Substitutions (S)**: 605
- **Deletions (D)**: 19
- **Insertions (I)**: 2885
- **Decode Time**: 320.61s
- **Backtrace Time**: 0.083s
- **Forward Computations**: 32307072
- **States, Arcs**: 116, 230

### Self-loop Probabilities
- **0.2**: WER = 103.47%, S = 618, D = 36, I = 1852
- **0.5**: WER = 75.63%, S = 607, D = 56, I = 1169
- **0.8**: WER = 66.06%, S = 583, D = 96, I = 921
- **0.99**: WER = 59.41%, S = 601, D = 203, I = 635

### Silence State
- **WER**: 55.62%
- **Substitutions (S)**: 631
- **Deletions (D)**: 56
- **Insertions (I)**: 660
- **Decode Time**: 337.27s
- **Backtrace Time**: 0.079s
- **Forward Computations**: 32307072
- **States, Arcs**: 116, 230

### Bigram Language Model
- **WER**: 130.68%
- **Substitutions (S)**: 546
- **Deletions (D)**: 25
- **Insertions (I)**: 2594
- **Decode Time**: 364.33s
- **Backtrace Time**: 0.087s
- **Forward Computations**: 32307072
- **States, Arcs**: 117, 323

![Screenshot (84)](https://github.com/xxXLokiXxx/Automatic-Speech-Recognition-Model/assets/99037815/2cda964e-2601-4dce-a7fa-81e5d81720c0)


## Installation (applicable in DICE machine only)
1. Clone the repository:
    ```bash
    git clone https://github.com/YourUsername/ASR-Model.git
    ```
2. Set up your environment (similar to lab setup):
    ```bash
    source /opt/conda/etc/profile.d/conda.sh
    conda activate asr_env
    ```
3. Open the assignment notebook:
    ```bash
    cd ASR-Model
    jupyter notebook
    ```

## Contributing
Contributions are welcome! Please fork the repository and submit a pull request.

## License
This project is licensed under the MIT License. See the LICENSE file for details.

