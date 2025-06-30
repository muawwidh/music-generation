# Music Generation using LSTM 

This project demonstrates how to automatically generate music using artificial intelligence—specifically, a Recurrent Neural Network (RNN) with Long Short-Term Memory (LSTM) layers. The model is trained on melodies in ABC notation, and after training, it can generate entirely new, original musical compositions.

## Problem Statement

**How can we use AI to generate music automatically?**  
In this project, you will learn how to use an LSTM-based model to compose single-instrument melodies. The AI is trained on existing music and learns the patterns of note sequences, so it can create new and coherent compositions (not just copy-paste!).

## Approach

1. **Data Collection:**  
   - Uses public domain ABC notation music files.  
   - Example training set: 340 Irish "Jigs" melodies ([source](http://abc.sourceforge.net/NMD/)).
2. **Data Preparation:**  
   - Converts each ABC file into a long character sequence.
   - Prepares batches for character-level prediction.
3. **Model Architecture:**  
   - Character-level LSTM neural network (built with Keras/TensorFlow).
   - Layers: Embedding → LSTM → Dropout → Dense (with softmax activation).
4. **Training:**  
   - The network is trained to predict the next character in a sequence.
   - Trains for a configurable number of epochs (default: 80).
5. **Music Generation:**  
   - After training, the model can generate new ABC music text by sampling predictions step by step.
   - Outputs new, never-before-seen musical pieces in ABC notation.

## How to Use

### 1. Clone the repository

```bash
git clone https://github.com/YOUR_USERNAME/music-lstm-generation.git
cd music-lstm-generation
```
### 2. Install dependencies

```bash
pip install -r requirements.txt
```

### 3. Download the dataset
 - Go to http://abc.sourceforge.net/NMD/

 - Download the "Jigs" dataset (or any ABC notation files you want)

 - Place the data in the correct folder as described in the notebook.

### 4. Run the notebook
```bash
jupyter notebook music.ipynb
```
 - Follow the instructions in the notebook to train the model and generate music!

### How to use your generated output online:
- Copy the ABC notation output from your notebook (the generated text).
- Go to: [abcjs Editor](https://www.abcjs.net/abcjs-editor.html)
- Paste the ABC notation into the left text area.
- You will see the sheet music and can press "Play" to listen!

### Example: Output
The generated music will be output in ABC notation, ready for playback using any ABC music player. Here’s a sample (the notebook will show you how to generate your own!):
The following image is how it will look like after you paste the output music
   ![image](https://github.com/user-attachments/assets/1bfa4a55-6f8b-4639-a220-01afa935e519)
