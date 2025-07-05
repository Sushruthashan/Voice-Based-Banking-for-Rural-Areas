# Voice-Based-Banking-for-Rural-Areas

## Description

This project addresses the challenges faced by rural populations in accessing and utilizing banking services, primarily due to language barriers, low digital literacy, and limited exposure to formal financial systems. It develops an intelligent, voice-enabled chatbot that allows users to interact with banking systems using regional languages like Kannada, and even unwritten languages such as Tulu and Konkani. The system uses the OpenAI Whisper model to transcribe and translate regional language speech to English text, and then processes it to extract relevant information and automatically generate filled-out banking forms for account creation or loan applications. This aims to encourage rural people to engage with banking procedures, promoting financial security and education.

## Features

  * **Voice Input Handling:** Accepts real-time voice input in Kannada, Tulu, or Konkani through a microphone.
  * **Speech Recognition:** Utilizes the OpenAI Whisper model to transcribe regional voice input into text, supporting noisy and accented speech conditions.
  * **Language Translation:** Transcribes regional language text and translates it into English using HuggingFace Transformers (version 4.28 or higher).
  * **Intent Detection and NLP:** A chatbot engine analyzes translated English text to determine user intent (e.g., opening an account, checking balance, applying for a loan).
  * **User Profile Management:** Maintains structured user profiles, including personal details, for reuse in future interactions.
  * **Form Generation:** Auto-generates banking forms in PDF or DOCX format using `fpdf` or `python-docx` based on user input.
  * **Banking API Integration:** Integrates with (or simulates) core banking APIs for backend operations like account creation and balance queries.
  * **Text-to-Speech Output:** Converts the system's final response into voice output in the user's regional language using Coqui TTS for playback.
  * **Web Interface:** Provides a simple, intuitive, icon-driven web interface with minimal textual elements.

## Non-Functional Requirements

  * **Usability:** Designed for users with low or no digital literacy, minimizing reliance on reading or typing.
  * **Scalability:** The architecture supports easy extension to five or more additional languages with minimal code changes.
  * **Robustness:** Maintains recognition and translation accuracy in noisy rural environments (up to 60 dB ambient sound).
  * **Compatibility:** The web interface is compatible with the latest versions of Google Chrome and Mozilla Firefox.
  * **Maintainability:** The codebase is modular and well-documented for future maintenance and feature additions.
  * **Resilience:** The system returns appropriate voice error messages and logs failures without crashing if speech recognition or translation modules fail.

## Technologies Used

  * **Backend Framework:** Python 3.8+, Flask or Django.
  * **Frontend Technologies:** HTML/CSS/JavaScript for responsive web-based UI.
  * **Speech Recognition:** OpenAI Whisper model.
  * **Text-to-Speech (TTS):** Coqui TTS (v0.11).
  * **Document Generation:** FPDF and `python-docx` libraries.

## System Architecture

The system employs a voice-enabled banking chatbot designed for regional language users. User voice input in a regional language (e.g., Kannada) is captured by a microphone and sent to the chatbot system. The core is OpenAI’s Whisper model, a Transformer-based neural network that converts speech into a log-Mel spectrogram, recognizes, and transcribes the speech. The transcribed regional language speech is then translated into English. This translated English text is passed to the chatbot module, which interprets user intent. Based on the intent, the system either generates a voice-based response in Kannada or English via a speaker, or automatically populates and prints a bank application form. This process aims to provide seamless banking access without requiring English literacy or complex digital interface proficiency.

## Installation (Conceptual)

1.  **Clone the repository:**
    ```bash
    git clone <repository-url>
    cd voice-based-banking
    ```
2.  **Set up Python environment:**
    Ensure Python 3.8+ is installed. It is recommended to use a virtual environment.
    ```bash
    python -m venv venv
    source venv/bin/activate # On Windows, use `venv\Scripts\activate`
    ```
3.  **Install dependencies:**
    Install required Python libraries. A `requirements.txt` file should be provided in the repository.
    ```bash
    pip install -r requirements.txt
    ```
    This would include libraries like `Flask` or `Django`, `openai-whisper`, `transformers`, `CoquiTTS`, `fpdf`, and `python-docx`.
4.  **Hardware Considerations:**
      * **Client Device:** A PC with a microphone, at least a 2 GHz dual-core processor, and a minimum of 32 GB RAM.
      * **Server:** An 8-core CPU, 64 GB RAM, and an NVIDIA GPU for efficient AI model operation.
      * A noise-cancelling microphone is recommended.
      * Uninterrupted power supply (UPS) is recommended for client and server locations in rural areas.

## Usage (Conceptual)

1.  **Start the Backend Server:**
    Run the Flask/Django application to expose the RESTful APIs.
2.  **Access the Web Interface:**
    Open the web interface in a compatible browser (Google Chrome or Mozilla Firefox latest versions).
3.  **Voice Interaction:**
    Use the microphone to provide voice commands in regional languages like Kannada, Tulu, or Konkani. The system will process your voice, translate it, understand your intent, and respond verbally or generate necessary banking forms.

## Contributors

  * Sushrutha Shanbhogue (4SF22CS225) 
  * Raghavendra SS (4SF22CS158)
  * Sowndarya S (4SF22CS218) 
  * Iram A.K Shaikh (4SF23CS404) 

**Under the Guidance of:**

  * Mr. Raghavendra Sooda, Assistant Professor, Department of CSE

## Acknowledgements

We extend our gratitude to Mr. Raghavendra Sooda for his invaluable advice and encouragement. We also thank Dr. Suhas A Bhyratae and Ms. Prapulla G, Project Coordinators, and Dr. Mustafa Basthikodi, Professor and Head, Department of Computer Science and Engineering, for their unwavering support and guidance. A special thanks to Dr. S. S. Injaganeri, Principal, Sahyadri College of Engineering and Management, for being a constant source of inspiration. Finally, heartfelt thanks to our family and friends for their wishes and encouragement throughout this project.
