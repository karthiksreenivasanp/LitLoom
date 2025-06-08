# ◆ LitLoom ◆
### Your Personal Digital Atelier for Poetry Analysis

LitLoom is an elegant and powerful desktop application designed for poets, students, and literature enthusiasts. It provides a beautiful and intuitive space to write, and then seamlessly unveils the intricate layers of your poetry through a suite of advanced analytical tools. From rhyme schemes to sentimental tone, LitLoom transforms your creative process into a journey of discovery.

![LitLoom Demo](https://i.imgur.com/your-gif-url.gif)
> **Note:** It is *highly recommended* that you replace the link above with a GIF showcasing your application. A short screen recording converted to a GIF is incredibly effective. You can use a tool like [ScreenToGif](https://www.screentogif.com/) or [GIPHY Capture](https://giphy.com/apps/giphycapture).

---

## ✨ Key Features

* ✒️ **Elegant & Themed Interface:** A custom-built, vintage-inspired UI with rounded corners, custom fonts, and a warm color palette that makes writing and analysis a pleasure.
* ✍️ **Intuitive Poem Editor:** A clean, focused writing space with useful tools.
    * **Example Poems:** Get inspired with a click that loads classic poem snippets.
    * **Interactive Spell Checker:** A custom popup finds misspelled words and offers smart suggestions without interrupting your flow.
* 🗣️ **Text-to-Speech (TTS):**
    * Listen to your poems or analysis reports read aloud.
    * Utilizes the native Windows SAPI5 engine for high-quality, responsive audio via the `pywin32` library.
    * Features a custom control panel to switch between installed Windows voices and adjust playback speed.
* 🔬 **Comprehensive Analysis Suite:**
    * **Overview:** Get a snapshot of your poem's structure, including line count, word count, and a content snippet.
    * **Rhyme Scheme Detection:** Automatically analyzes the end-words of each line to determine the poem's rhyme scheme (e.g., ABAB, AABB) and groups rhyming words.
    * **Parts of Speech (POS) Tagging:** Uses `NLTK` to identify and group all nouns, verbs, adjectives, adverbs, and more.
    * **Figure of Speech Detection:** Employs heuristics to find potential instances of similes, metaphors, and alliterations in your text.
    * **Sentimental Tone Analysis:** Uses NLTK's VADER to score the emotional tone of your poem, classifying it as positive, negative, or neutral.
* 🌍 **Multi-Language Translation:**
    * Translate your poem into dozens of languages using the `deep-translator` library.
    * Perfect for multilingual poets or for understanding poetry in a new linguistic context.
* 📄 **Professional PDF Export:**
    * Generate a beautifully formatted PDF report of the complete analysis using `ReportLab`.
    * Includes custom font support (`NotoSans`) to ensure that translated characters are rendered correctly in the PDF.

---

## 🚀 Getting Started

There are two ways to get LitLoom running: as a user with a pre-built application, or as a developer from the source code.

### 1. For Users (Recommended)

If you have created an executable (`.exe`) of this application, this is the easiest method for users.

1.  Go to the [**Releases**](https://github.com/your-username/your-repo-name/releases) page of this repository.
2.  Download the latest `LitLoom.zip` file.
3.  Unzip the folder to a location of your choice.
4.  **Important:** Ensure the `assets` folder is in the same directory as the executable.
5.  Double-click `LitLoom.exe` to run the application!

### 2. For Developers (Running from Source)

If you want to run the application from the `LitLoom.py` script:

1.  **Clone the repository:**
    ```bash
    git clone [https://github.com/your-username/your-repo-name.git](https://github.com/your-username/your-repo-name.git)
    cd your-repo-name
    ```

2.  **Set up a Python virtual environment (recommended):**
    ```bash
    python -m venv venv
    source venv/bin/activate  # On Windows, use `venv\Scripts\activate`
    ```

3.  **Install the required libraries:**
    The script relies on several external libraries. You can install them all using pip:
    ```bash
    pip install pyspellchecker pyttsx3 nltk deep-translator reportlab Pillow pywin32
    ```

4.  **Run the application:**
    ```bash
    python LitLoom.py
    ```
    The first time you run it, `NLTK` will automatically download necessary data packages (`punkt`, `vader_lexicon`, etc.). Please ensure you have an internet connection for this one-time setup.

---

## 📖 How to Use LitLoom

1.  **Welcome Screen:** Upon launching, you are greeted with a beautiful welcome screen. Click **"Let's Go!"** to begin.

2.  **Poem Editor:**
    * Type or paste your poem into the main text area.
    * Use the **`Add Example`** button to cycle through sample poems.
    * Click **`Spell Correct`** to launch the spell check popup.

3.  **Text-to-Speech (TTS):**
    * Click the **sound icon** in the editor or analysis page to open the TTS controls.
    * To use voices for other languages, you must first install them in your Windows settings: **Settings > Time & Language > Language & Region > Add a language**. Once a language with TTS support is installed, its voice will appear in the dropdown.

4.  **Analyze Your Poem:**
    * Once you are ready, click the **`Analyze`** button.

5.  **Analysis Page:**
    * Your poem's analysis is now available! Use the sidebar buttons to switch between different reports: **`Overview`**, **`Parts of speech`**, **`Figure of speech`**, and **`Tone`**.
    * **Translate:** Click the **`Translation`** button, then select a language from the dropdown to see your poem translated.
    * **Adjust View:** Use the `+` and `–` buttons to change the font size for readability.
    * **Export:** Click **`Convert to PDF`** to open the export dialog, choose a save location, and generate your analysis report.

---

## 📂 File Structure

The repository is organized to keep the code and its resources clean and accessible. The `assets` folder is crucial for the application's appearance and functionality.


*LitLoom/
*├── LitLoom.py           # The main application script
*├── assets/              # Folder for all external resources
*│   ├── fonts/
*│   │   ├── NotoSans-Regular.ttf
*│   │   └── NotoSans-Bold.ttf
*│   ├── background.jpeg
*│   ├── bg.jpeg
*│   ├── open-book.png
*│   ├── Quill With Ink.png
*│   ├── LitLoom.png
*│   ├── Sound I.png
*│   └── Sound II.png
*└── README.md            # This file


---

## 🤝 Contributing

Contributions are welcome! If you have ideas for new features, bug fixes, or improvements, please feel free to:

1.  Fork the repository.
2.  Create a new branch (`git checkout -b feature/AmazingNewFeature`).
3.  Commit your changes (`git commit -m 'Add some AmazingNewFeature'`).
4.  Push to the branch (`git push origin feature/AmazingNewFeature`).
5.  Open a Pull Request.

## 📜 License

This project is licensed under the MIT License - see the `LICENSE` file for details.

## 🙏 Acknowledgments

This application was made possible by the incredible work of the developers behind these open-source libraries:
* [Tkinter](https://docs.python.org/3/library/tkinter.html)
* [Pillow](https://python-pillow.org/)
* [pyspellchecker](https://github.com/barrust/pyspellchecker)
* [pywin32](https://github.com/mhammond/pywin32)
* [NLTK (Natural Language Toolkit)](https://www.nltk.org/)
* [Deep-Translator](https://github.com/nidhaloff/deep-translator)
* [ReportLab](https://www.reportlab.com/)
