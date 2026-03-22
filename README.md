🤖 Friday AI Assistant

Friday is a fully local, voice-enabled AI assistant with memory, emotional awareness, and real-time interaction — designed for privacy, responsiveness, and extensibility.

✨ Features
🎙️ Voice + Text Interaction
Wake-word activated assistant
Real-time voice command capture
Parallel text input mode
Smooth switching between input methods

🧠 Local AI (Offline-First)
Powered by Ollama
Uses LLaMA 3
No cloud dependency — runs entirely locally

💬 Memory System
Short-term memory (conversation context)
Long-term memory stored in fridays_memory.json
Automatically remembers:
Preferences
Facts about the user
Past conversations

😊 Emotional Awareness
Detects tone from user input:
Friendly
Concerned
Enthusiastic
Gentle
Dynamically adapts personality and responses
Emotion decay resets mood over time

🔊 Text-to-Speech
High-quality local speech using Piper TTS
Custom voice model support
Real-time playback

🎧 Wake Word Detection
Powered by openWakeWord
Always-on listening with low resource usage
Debounce protection against false triggers

📝 Speech Recognition
Fast transcription via faster-whisper
Works locally without internet

⚡ Multithreaded System
Voice input, text input, and processing run concurrently
Responsive, non-blocking experience

🚀 Demo Flow
Say wake word → “Hey Mycroft”
Friday responds: “I’m listening.”
Speak your command
Friday:
Transcribes speech
Thinks 🤖
Responds (text + voice)

OR

👉 Type directly in the terminal

🛠️ Installation
1. Clone the repo
git clone https://github.com/yourusername/friday-ai.git
cd friday-ai
2. Install dependencies
pip install -r requirements.txt
3. Install & Setup Ollama

Install Ollama and pull model:

ollama run llama3
4. Setup Piper TTS
Download Piper TTS
Download a voice model (e.g. en_GB-alba-medium)

Update paths in code:

PIPER_EXE = r"C:\piper\piper.exe"
PIPER_MODEL = r"C:\piper\voices\en_GB-alba-medium.onnx"
5. Run the assistant
python main.py
⚙️ Configuration

You can tweak:

Parameter	Description
THRESHOLD	Wake word sensitivity
COMMAND_DURATION	Recording time
SAMPLE_RATE	Audio quality
MAX_TURNS	Short-term memory size
Memory limits	Long-term storage size
📁 Project Structure
friday-ai/
│
├── main.py
├── fridays_memory.json
├── audio/
└── README.md
🧠 How Memory Works
Short-Term Memory
Stored in conversation
Limited to last N turns
Long-Term Memory

Stored in:

{
  "facts": [],
  "dialogue": []
}
Facts extracted from phrases like:
“I like…”
“My name is…”
Dialogue history retained (capped)
⚠️ Known Limitations
Emotion detection is keyword-based
No multi-user support
Wake word is fixed
Memory is not semantic (no embeddings yet)
CPU-only by default (slower on low-end systems)
🔮 Roadmap
🧠 Vector database memory (semantic recall)
👤 Multi-user recognition
🔌 Plugin/tool system (apps, automation)
🎯 Custom wake word training
⚡ GPU acceleration
🎭 Advanced emotion modelling
🙌 Acknowledgements
Ollama
openWakeWord
faster-whisper
Piper TTS
📜 License

MIT License (recommended — update if needed)

👤 Author

Akif Jabir

💡 Final Note

Friday is built as a fully local AI assistant combining:

Voice interaction
Memory
Personality

The goal is to create a private, intelligent, and extensible assistant that runs entirely on your machine
