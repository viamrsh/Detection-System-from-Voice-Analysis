# Emotion-Detection-System-from-Voice-Analysis

# Objective: 
The primary objectives of this project are:  
- To develop a machine learning model capable of classifying emotions from voice recordings.  
- To implement a real-time recording system for live emotion detection.  
- To create an interactive and visually appealing interface for users.  
- To ensure high accuracy in emotion prediction using feature extraction techniques.

# Tools
- Librosa – For audio feature extraction (MFCC, chroma, mel spectrogram)  
- Scikit-learn – For machine learning (SVM classifier, data preprocessing)  
- Matplotlib – For visualization of results  
- IPython & Google Colab – For interactive web-based execution  
- Pydub – For audio file handling  
- Joblib – For model serialization  

# Dataset
- RAVDESS (Ryerson Audio-Visual Database of Emotional Speech and Song)  
  - Contains 24 professional actors (12 male, 12 female)  
  - 8 emotional states: *neutral, calm, happy, sad, angry, fearful, disgust, surprised*  

# Code Explain

**Emotion Detection System Code Explanation**  


### **1. System Overview**  
The system is built as a modular pipeline that records audio, extracts meaningful features, trains a machine learning model, and predicts emotions. It uses **Librosa** for audio processing, **Scikit-learn** for machine learning, and **IPython** for interactive visualization.  

### **2. Configuration (Config Class)**  
The `Config` class centralizes all system settings, including:  
- **Audio parameters** (sample rate, duration, MFCC coefficients)  
- **File paths** (model and dataset directories)  
- **Emotion labels** (neutral, happy, sad, angry, etc.)  
- **Directory setup** (ensures required folders exist)  

### **3. Audio Processing (AudioProcessor Class)**  
This class handles feature extraction from audio files:  
- **MFCCs (Mel-Frequency Cepstral Coefficients)** – Captures spectral features of speech.  
- **Chroma Features** – Represents pitch and harmonic content.  
- **Mel Spectrogram** – Simulates human auditory perception.  
- **Preprocessing** – Trims silence and normalizes audio.  

### **4. Model Training (EmotionTrainer Class)**  
The system uses a **Support Vector Machine (SVM)** for classification:  
- **Data Loading** – Reads audio files and extracts features.  
- **Train-Test Split** – 80% training, 20% testing.  
- **Feature Scaling** – Standardizes features for better model performance.  
- **Training & Evaluation** – Trains the model and displays accuracy metrics.  
- **Model Saving** – Stores the trained model for future use.  

### **5. Recording System (LiveRecorder Class)**  
A browser-based audio recorder with:  
- **Noise Suppression & Echo Cancellation** – Improves recording quality.  
- **Real-Time Waveform Visualization** – Shows audio levels during recording.  
- **Automatic Saving** – Converts recordings to WAV format.  
- **Error Handling** – Detects failed recordings and prompts retries.  

### **6. Main Application (EmotionApp Class)**  
Orchestrates the entire workflow:  
- **Training Mode** – Loads data, trains, and evaluates the model.  
- **Prediction Mode** – Records speech, extracts features, and predicts emotions.  
- **Results Display** – Shows emotion probabilities and waveform.  

### **7. User Interface**  
The system provides two interfaces:  
- **Console Menu** – For command-line interaction.  
- **Interactive Web UI** – Buttons for recording and analysis with real-time feedback.  

### **8. Key Features**  
- **Accurate Predictions** – Uses optimized feature extraction and SVM.  
- **Robust Recording** – Handles noise and varying speech lengths.  
- **Visual Feedback** – Displays waveforms, probabilities, and confusion matrices.  
- **Easy Deployment** – Works in Google Colab and local environments.  

### **9. Workflow**  
1. **Train the model** on a labeled dataset.  
2. **Record speech** via microphone or upload.  
3. **Extract features** (MFCCs, chroma, etc.).  
4. **Predict emotion** using the trained model.  
5. **Display results** with confidence scores.  


