# VoiceOps
AI-Based Voice Clone Detection and Risk Assessment System

VoiceOps – AI-Powered Voice Cloning Detection & Risk Assessment
Smart India Hackathon 2026 | Problem Statement ID: 26104

VoiceOps is an AI-based system designed to detect AI-generated and cloned voices to help prevent voice impersonation attacks.
1. Problem Statement
AI-generated voices can imitate real individuals and be misused for impersonation and fraud. VoiceOps aims to identify such voices using deep learning-based audio analysis.
2. Proposed Solution
The system analyses audio and classifies it as:
- REAL: Genuine human voice.
- AI-GENERATED: Potentially cloned or synthetic voice.
It aims to provide confidence scores, risk assessment, and alerts for suspicious audio interactions.
3. System Architecture
Incoming Audio
      ↓
Audio Preprocessing (16 kHz)
      ↓
Audio Chunking
      ↓
Deep Learning Model
      ↓
REAL / AI-GENERATED
      ↓
Confidence Score
      ↓
Risk Assessment
      ↓
Low / Medium / High Alert


4. Model Benchmarking
Dataset: ASVspoof 2021 – Deepfake (DF), accessed through Hugging Face.

Models explored:
- Wav2Vec2: Tested on 200 balanced samples. Accuracy: 50%. The model predicted all samples as REAL, failing to detect spoof audio.
- W2V2-AASIST: Explored using ONNX Runtime. Reported AUC: 0.9847 and estimated EER: 6%. These results require further validation due to an evaluation issue.
- RawNet2: Investigated as an alternative model; same-dataset benchmarking is pending.
5. Technologies Used
Python, PyTorch, Hugging Face Transformers, Wav2Vec2, W2V2-AASIST, ONNX Runtime, Librosa, Torchaudio, Scikit-learn and Hugging Face Datasets.
6. Current Implementation
- ASVspoof 2021 dataset exploration.
- Pretrained model loading and testing.
- Audio preprocessing and classification experiments.
- Model performance evaluation.
- Comparison and exploration of alternative architectures.
7. Future Scope
- Improve detection accuracy.
- Validate and compare models.
- Integrate a backend API.
- Implement pre-call screening and continuous monitoring.
- Introduce real-time risk alerts.
- Test across accents, background noise and compressed audio.
8. References
- ASVspoof 2021 Dataset
- Wav2Vec2 Model
- Hugging Face Transformers
- ONNX Runtime
Note: VoiceOps is currently at the prototype and benchmarking stage. Live-call integration and real-time monitoring are proposed features, not completed implementations.
