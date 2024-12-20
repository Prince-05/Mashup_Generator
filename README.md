# Mashup Generator

This project is a simple and interactive Streamlit application that generates audio mashups by downloading audio tracks from YouTube, trimming them to a specified duration, and merging them into a single audio file.

## Features

- Download audio tracks from YouTube based on a singer's name.
- Trim audio tracks to a specified duration.
- Merge multiple audio tracks into a single mashup file.
- Save the generated mashup file locally.

## Requirements

Make sure you have the following installed on your system:

- Python 3.7 or later
- Required Python packages:
  - `streamlit`
  - `yt-dlp`
  - `pydub`
  - `ffmpeg`
  - `shutil`

## Installation

1. Clone the repository or copy the project files to your local system.
2. Install the required dependencies:

   ```bash
   pip install streamlit yt-dlp pydub
   ```

3. Install FFmpeg if it is not already installed. You can follow the instructions [here](https://ffmpeg.org/download.html).

## Usage

1. Run the Streamlit app:

   ```bash
   streamlit run create_mashup.py
   ```

2. Enter the following details in the app interface:
   - **Singer Name**: The name of the singer or artist whose songs you want to download.
   - **Number of Videos**: The number of videos to download.
   - **Audio Duration in Seconds**: The duration (in seconds) to which each audio track will be trimmed. Must be greater than 20 seconds.
   - **Output File Name**: The name of the output mashup file (e.g., `mashup.mp3`).

3. Click the "Create the Mashup" button to start the process.

4. Once completed, the mashup audio file will be saved in the same directory as the application.

## File Structure

```
.
|-- create_mashup.py                 # Main application script
|-- README.md              # Project documentation
|-- <singer_name>/         # Folder containing downloaded audio files
|-- <output_file>.mp3      # Generated mashup file
```

## Example

### Input:
- Singer Name: `Adele`
- Number of Videos: `3`
- Audio Duration in Seconds: `30`
- Output File Name: `adele_mashup.mp3`

### Output:
- A folder named `Adele` containing the downloaded audio files.
- A mashup file named `adele_mashup.mp3` saved in the current directory.

## Known Issues

1. **YouTube Restrictions**: Some YouTube videos may not be downloadable due to copyright restrictions.
2. **FFmpeg Dependency**: Ensure FFmpeg is correctly installed and accessible in your system's PATH.

## Acknowledgments

- [Streamlit](https://streamlit.io/) for creating an excellent framework for building interactive web applications.
- [yt-dlp](https://github.com/yt-dlp/yt-dlp) for enabling YouTube downloads.
- [Pydub](https://github.com/jiaaro/pydub) for audio processing.

