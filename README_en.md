# TTS Dialogue Audio Generator (Edge-TTS)

A GUI application based on Edge-TTS that converts dialogue text into natural speech audio, supporting multiple speakers, pause control, and audio merging features.

## Features

- 🗣️ **Multi-speaker Support**: Supports up to 6 different speakers (A-F), each can be assigned a different voice
- 🔊 **Diverse Voices**: Provides multiple English male and female voices from US and UK
- ⏸️ **Pause Control**: Use `[pause_X]` tags in text to add custom length pauses (X in seconds, supports decimals)
- 🎵 **Audio Processing**: Can save audio for each speaker separately or merge all audios into one file
- 🖥️ **Intuitive Interface**: Graphical user interface for easy operation and configuration
- 📁 **Flexible Output**: Customizable output directory, file naming format, and merge options

## System Requirements

- Windows 7 or higher
- Python 3.7+
- Internet connection required (Edge-TTS requires online service)

## Installation

1. Clone or download this repository to your local machine

2. Install the required dependencies:
   ```
   pip install edge-tts numpy
   ```

3. (Optional) For better audio processing capabilities, it's recommended to install additional audio libraries:
   ```
   pip install librosa soundfile
   ```

## Usage

1. Run the application:
   ```
   python tts_V5.py
   ```

2. Enter dialogue content in the input box using the following format:
   ```
   A: Hello, welcome to our program[pause_1].
   B: Today we have a special guest.
   C: Thank you for having me, happy to be here.
   ```

3. Select appropriate voices for each speaker (A-F)

4. Set output directory and other options:
   - Merge all audios into a single file
   - Delete individual audio files after merging
   - Customize merged file name
   - Customize naming format for individual files

5. Click the "GENERATE Audio" button to start audio generation

6. To stop the generation process, click the "STOP Generation" button

## Voice Options

### US English Male Voices
- Andrew (US)
- Brian (US)
- Christopher (US)
- Roger (US)
- Steffan (US)
- Guy (US, Default)

### US English Female Voices
- Ana (US)
- Aria (US)
- Ava (US)
- Jenny (US, Default)
- Michelle (US)

### UK English Male Voices
- Libby (UK)
- Ryan (UK, Default)

### UK English Female Voices
- Sonia (UK)
- Maisie (UK)

## Input Format

Dialogues must be entered in the following format:
```
Speaker Identifier: Dialogue Content[pause_number]
```

For example:
```
A: Hello, I'm your host[pause_2]Today we'll discuss an important topic.
B: Yes, this is indeed an issue worth paying attention to[pause_1.5]I think...
```

The `[pause_X]` tag can be inserted anywhere in the text to add X seconds of silence at that position.

## Output Options

1. **Save Directory**: Choose where to save the generated audio files
2. **Merge Audio**: Merge all individual audio clips into one complete audio file
3. **Delete Singles**: Automatically delete individual audio files after successful merging
4. **Merged Filename**: Set the name of the merged file
5. **Single File Format**: Customize individual file naming using `{index}` and `{speaker}` placeholders

## Notes

- The application requires a stable internet connection to function properly
- Pause effects and limited audio merging functionality if `librosa` and `soundfile` libraries are not installed
- It's recommended to run this program using the project's virtual environment
- Generated audio files are in WAV format

## License

This project is for personal learning and research purposes only. Please comply with the terms of Microsoft Edge TTS service.