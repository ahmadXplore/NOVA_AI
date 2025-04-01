# NOVA Voice Assistant

NOVA is an advanced desktop voice assistant with a modern, animated UI built using PyQt6. It features voice recognition, natural language processing, text-to-speech capabilities, and an interactive animated robot character.


## Features

- **Voice Activation**: Say "NOVA" to activate the assistant
- **Natural Language Processing**: Powered by Mistral AI for intelligent responses
- **Multi-language Support**: Automatic translation for non-English inputs
- **Modern UI**: Sleek design with animated robot assistant and particle effects
- **Text-to-Speech**: Natural sounding voice responses
- **Multi-Modal Input**: Use voice commands or text input

### Prerequisites

- Python 3.8+
- PyQt6
- Internet connection (for API services)

### Setup

1. Clone the repository:
   ```bash
   git clone https://github.com/ahmadXplore/NOVA-AI.git
   cd NOVA-AI
   ```

2. Create a virtual environment:
   ```bash
   python -m venv venv
   source venv/bin/activate  # On Windows: venv\Scripts\activate
   ```

3. Install dependencies:
   ```bash
   pip install -r requirements.txt
   ```

4. Create a `.env` file in the project root with your Mistral API key:
   ```
   MISTRAL_API_KEY=your_mistral_api_key_here
   ```

5. Run the application:
   ```bash
   python NOVA-AI.py
   ```

## Requirements

```
PyQt6
pyttsx3
SpeechRecognition
deep-translator
mistralai
python-dotenv
requests
Pillow
```

## Usage

1. Launch the application
2. Say "NOVA" to activate voice commands
3. Ask questions or give commands
4. For text input, type your question and press Enter or click Send

### Voice Commands

- "NOVA, set timer for X seconds" - Sets a timer
- "NOVA, play music" - Attempts to play music from your music folder or opens YouTube
- "NOVA, goodbye" - Exits conversation mode

## Configuration

You can modify the following parameters in the code:

- Voice settings (rate, volume, voice type)
- UI colors and styles
- Microphone sensitivity settings
- API parameters for Mistral AI

## Project Structure

```
NOVA-AI/
├── NOVA-AI.py             # Main application file
├── requirements.txt       # Python dependencies
├── .env                   # Environment variables (API keys)
├── README.md              # Project documentation
```

## How It Works

1. **Voice Recognition**: Uses the SpeechRecognition library with Google's speech recognition API
2. **Natural Language Processing**: Utilizes Mistral AI's language models
3. **User Interface**: Built with PyQt6 including custom animations and particle effects
   - Animated robot character that moves and reacts
   - Particle background with dynamic motion
   - Modern message bubbles with timestamps
4. **Translation**: Integrates Google Translator for multi-language support
5. **Text-to-Speech**: Implements pyttsx3 for voice feedback

## UI Components

- A header with the animated robot character and NOVA title
- Status indicators showing when the assistant is actively listening
- A chat display area for conversation history
- A text input field at the bottom for typing questions
- A sleek "Send" button for submitting questions
- A footer reminder to say "NOVA" to activate voice commands
- An elegant particle background animation

## Customization

### Changing the Voice

Modify the `init_text_to_speech()` function to select different voices:

```python
def init_text_to_speech():
    engine = pyttsx3.init()
    voices = engine.getProperty('voices')
    # Change index to select different voice
    engine.setProperty('voice', voices[1].id)  # [0] is usually male, [1] is female
    return engine
```

### Modifying UI Colors

The UI colors can be customized in the `setup_styles()` method within the `JarvisUI` class. The current theme uses a dark blue color scheme with transparency effects for a modern look.

## Contributing

Contributions are welcome! Please feel free to submit a Pull Request.

1. Fork the repository
2. Create your feature branch (`git checkout -b feature/amazing-feature`)
3. Commit your changes (`git commit -m 'Add some amazing feature'`)
4. Push to the branch (`git push origin feature/amazing-feature`)
5. Open a Pull Request

## License

This project is licensed under the MIT License - see the LICENSE file for details.

## Acknowledgments

- [Mistral AI](https://mistral.ai/) for the natural language processing capabilities
- [PyQt6](https://www.riverbankcomputing.com/software/pyqt/) for the UI framework
- [SpeechRecognition](https://pypi.org/project/SpeechRecognition/) for voice recognition

## Future Improvements

- [ ] Add more built-in commands (weather, news, etc.)
- [ ] Implement conversation history storage
- [ ] Add user profiles and customization options
- [ ] Improve offline capabilities
- [ ] Add more animations and visual feedback

---

Created with ❤️ by Muhammad Ahmad Asif
