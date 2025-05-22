# Edge TTS Generator by BossKham

A user-friendly desktop application for generating speech using Microsoft Edge's online Text-to-Speech voices. Create high-quality audio from text with various customization options.

## Features

* **Wide Range of Voices:** Access to all languages and voices available through Microsoft Edge's TTS service.
* **Customization:** Adjust speech rate, pitch, and volume.
* **Silence Removal:** Option to automatically remove leading/trailing silences from generated audio.
* **Multiple Output Formats:** Save audio as MP3 (default), WAV, or M4A.
* **Single & Batch Generation:**
    * **Single Mode:** Quickly generate audio from pasted text.
    * **Batch Mode:** Process multiple lines of text from a `.txt` file and get a ZIP archive of the audio files.
* **User-Friendly Interface:** Simple and intuitive GUI with light and dark theme options.

## 💾 Installation

1.  **Download the Application:**
    * Go to the [**Releases**](https://github.com/BossKham/edge_tts_gui/releases) page of this repository.
    * Download the latest `EdgeTTSGenerator_YourVersion.zip` (or `.exe` if provided directly) file from the "Assets" section.
    * Extract the ZIP file to a folder on your computer if you downloaded a ZIP.

2.  **Install FFmpeg (Required for WAV/M4A output and some audio processing):**
    * This application uses FFmpeg for converting audio to WAV or M4A formats and potentially for other audio processing tasks. **FFmpeg version 7.1 or later is recommended.**
    * **Windows:**
        * Download FFmpeg from the official site: [https://ffmpeg.org/download.html](https://ffmpeg.org/download.html) (e.g., from the "Windows builds by BtbN" section).
        * Extract the downloaded archive (e.g., to `C:\ffmpeg`).
        * Add the `bin` folder inside the extracted FFmpeg folder (e.g., `C:\ffmpeg\bin`) to your system's **PATH environment variable**.
            * Search for "environment variables" in the Windows search bar.
            * Click on "Edit the system environment variables".
            * In the System Properties window, click the "Environment Variables..." button.
            * Under "System variables", find the variable named `Path` and select it. Click "Edit...".
            * Click "New" and add the path to your FFmpeg `bin` folder.
            * Click "OK" on all open windows to save the changes.
            * You may need to restart your computer or log out and log back in for the changes to take effect.
    * **macOS:**
        * The easiest way is using Homebrew: `brew install ffmpeg`
    * **Linux:**
        * Use your distribution's package manager. For example, on Debian/Ubuntu: `sudo apt update && sudo apt install ffmpeg`
    * **Verify Installation:** Open a new terminal or command prompt and type `ffmpeg -version`. If it's installed correctly and in your PATH, you should see version information.

## 🚀 How to Use

1.  **Run the Application:**
    * After downloading and extracting (if necessary), double-click the `EdgeTTSGenerator.exe` (or the equivalent executable for your OS) to start the application.

2.  **Select Language and Voice:**
    * Choose your desired **Language** from the dropdown menu.
    * Once a language is selected, the **Voice** dropdown will populate with available voices for that language. Select the voice you want to use.

3.  **Adjust Audio Settings (Optional):**
    * **Rate:** Control the speed of the speech (-100% to +100%).
    * **Pitch:** Adjust the pitch of the voice (-20st to +20st).
    * **Volume:** Modify the volume of the generated audio (-100% to +100%).
    * **Remove Silence:** Check this box to automatically trim silences from the beginning and end of the audio.
    * **Output Format:** Choose between MP3, WAV, or M4A for the saved audio file.

4.  **Generate Audio:**

    * **Single Generate Tab:**
        * Enter or paste your text into the "Input Text" box.
        * Click the "✨ Generate Audio" button.
        * Once generated, you can "▶️ Play Audio" or "💾 Save Audio".

    * **Batch Generate Tab:**
        * Click "📁 Select .txt file" to choose a text file containing lines of text you want to convert (one line per audio file).
        * Click the "⚡ Generate Batch Audio" button.
        * After processing, the "⬇️ Save Batch ZIP" button will become active, allowing you to save a ZIP file containing all the generated audio files.

5.  **Themes:**
    * Click the "Switch to Light ☀️" / "Switch to Dark 🌙" button in the top right to toggle between interface themes.

## ⚠️ Troubleshooting

* **"Error loading voices" / No voices appear:**
    * Ensure you have a stable internet connection, as the application needs to fetch the voice list from Microsoft's services.
    * Try restarting the application.
* **WAV or M4A output fails / "Error converting audio":**
    * Make sure FFmpeg (version 7.1 or later) is correctly installed AND its `bin` directory is added to your system's PATH environment variable. Restart the application (and possibly your computer) after updating the PATH.
* **Application does not start:**
    * If you downloaded a ZIP, ensure you extracted all files to a folder before running the executable.

## 🙏 Credits

* Application created by **BossKham** ([GitHub Profile](https://github.com/BossKham)).
* Powered by the `edge-tts` Python library and Microsoft Edge's online TTS services.
* Audio processing uses the `pydub` library.

---

*Note: This application requires an active internet connection to communicate with Microsoft Edge's TTS services for voice listing and speech synthesis.*
