# Voice Recorder Application

## Overview
This is a web-based voice recorder that records audio, detects silence, and automatically saves and uploads the recordings to a server. Each recording session generates a unique 8-character random string that remains the same for all audio files until manually stopped.

## Features
- **Automatic silence detection**: Stops recording after 1 second of silence and starts a new segment.
- **Session-based recording filenames**: All recordings in the same session use a consistent random identifier.
- **Real-time logging**: Displays status messages while recording.
- **Backend file storage**: Saves recordings to the `uploads` directory on the server.

## Installation

### Prerequisites
- Node.js installed
- npm (Node Package Manager)

### Setup Instructions
1. **Clone the repository**:
   ```sh
   git clone <repository-url>
   cd <directory>
   ```

2. **Install dependencies**:
   ```sh
   npm install
   ```

3. **Start the server**:
   ```sh
   node server.js
   ```

4. **Open the application**:
   - Open a browser and go to: `http://localhost:5000`

## Usage
You can adjust the silence sensitivity and timeout duration in index.html by modifying the avg threshold in checkSilence() and changing the timeout duration from 1000 milliseconds (1 second) to your preferred value.
1. Click the "Record" button to start recording.
2. The system will automatically stop after 1 second of silence and upload the segment.
3. The recording will continue until "Stop Recording" is manually clicked.
4. All recordings in a session will have filenames in the format:
   ```sh
   recording_<random_string>_<timestamp>.wav
   ```
5. Check the `uploads` folder to see saved recordings.

## License
This project is open-source and free to use.

