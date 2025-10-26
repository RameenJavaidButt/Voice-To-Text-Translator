# Voice-To-Text-Translator
This project implements a bi-directional Urdu–English translation system that can translate both text and speech using fine-tuned MBART models, Whisper speech recognition, and a FastAPI backend for deployment.
# Key Features

1. Dataset Creation & Preprocessing

Downloads and processes TED2020 English–Urdu parallel corpus.

Cleans, trims, and saves bilingual data into a structured CSV format.

2. Model Fine-tuning

Fine-tunes MBART50 (Multilingual BART) for both directions:

English → Urdu

Urdu → English

Uses Hugging Face Transformers with Seq2SeqTrainer for efficient training and evaluation.

Supports GPU training and mixed-precision (fp16) for speed.

3. Model Evaluation

Evaluates translation accuracy using BLEU and F1 Score metrics.

Includes tokenization and reference-based comparison for precise evaluation.

4. Speech-to-Text Integration (Whisper)

Uses OpenAI’s Whisper model for speech recognition in English and Urdu.

Converts uploaded audio files (.opus) into text before translation.

5. RESTful API (FastAPI + ngrok)

Provides endpoints for:

/upload-audio → upload speech for translation

/send-message → text-based translation

/hello and / → test endpoints

Supports CORS for frontend integration and exposes via ngrok tunnel.

6. Real-Time Translation
# Libraries & Tools Used

Core Language	Python
Deep Learning / NLP	PyTorch, Transformers (Hugging Face), MBART50, MarianMT, NLTK
Dataset Handling	pandas, datasets (Hugging Face)
Speech Recognition	Whisper (OpenAI), ffmpeg, pydub
Model Training	Seq2SeqTrainer, Seq2SeqTrainingArguments
Model Evaluation	BLEU (evaluate), scikit-learn (F1 score)
Environment Utilities	torch, os, subprocess
Automatically detects translation direction (eng-to-urd or urd-to-eng).

Performs speech transcription → text translation pipeline in real time.
# Contact

For any questions or feedback, feel free to reach out:

Email:rameenbutt990@gmail.com
