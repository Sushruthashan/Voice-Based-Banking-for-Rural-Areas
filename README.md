# Voice-Based Banking for Rural Areas 🗣️🏦
A voice-driven, AI-powered system that enables rural Kannada-speaking users to fill English bank forms using natural speech — bridging the language barrier in digital banking.

## 📖 Overview

Language remains a major barrier to financial inclusion in rural India. This project presents a **voice-based banking assistant** that allows users to interact with banking systems entirely in **Kannada**. The system uses an AI Avatar to capture speech, transcribe it, translate it into English, and automatically fill a bank application form — all in real time.

Built on **Microsoft Azure Cloud Services**, the solution is scalable, secure, and designed for users with low digital literacy.

## ✨ Features

- 🎤 **Voice-First Interaction** – Speak naturally in Kannada, no typing or English required.
- 🤖 **AI Avatar Guidance** – Interactive avatar explains fields, validates inputs, and confirms details.
- 🌐 **Real-Time Translation** – Azure Translator converts Kannada speech to English text.
- 📄 **Automated Form Filling** – Populates Word/PDF bank forms using `docxtpl`.
- ☁️ **Cloud-Native & Scalable** – Built with Azure Functions, Speech Services, and AI services.
- 🔒 **Secure & Compliant** – Encrypted communication, secure API keys, and session-based data handling.

## 🏗️ System Architecture

```
User (Kannada Speech)
       ↓
Azure AI Avatar (Speech Studio)
       ↓
Azure Speech-to-Text → Azure Translator
       ↓
Azure Function (Python Backend)
       ↓
Word Document Template (.docx)
       ↓
Filled Bank Form (Downloadable)
```

## 🛠️ Tech Stack

| Component               | Technology / Service                          |
|--------------------------|-----------------------------------------------|
| **Cloud Platform**       | Microsoft Azure                               |
| **Speech Processing**    | Azure Speech Service, AI Avatar               |
| **Translation**          | Azure Translator Service                      |
| **Backend**              | Azure Functions (Python)                      |
| **Templating Engine**    | `docxtpl`, `python-docx`                      |
| **Development**          | VS Code, Postman, Azure Functions Core Tools  |
| **Languages Supported**  | Kannada → English (extensible to other Indian languages) |

## 📁 Project Structure

```
├── function_app.py           # Main Azure Function logic
├── templates/
│   └── Canara_Bank_Template.docx
├── requirements.txt          # Python dependencies
├── README.md                 # This file
└── .github/workflows/       # CI/CD pipelines (optional)
```

## 🚀 Getting Started

### Prerequisites
- Python 3.8+
- Azure Account with active subscription
- VS Code with Azure Functions extension
- Postman (for API testing)

### Setup & Deployment

1. **Clone the repository**
   ```bash
   git clone https://github.com/yourusername/voice-based-banking.git
   cd voice-based-banking
   ```

2. **Install dependencies**
   ```bash
   pip install -r requirements.txt
   ```

3. **Configure Azure Services**
   - Create Azure Speech Service & Translator Service
   - Note down API keys and endpoints
   - Set environment variables in `local.settings.json` (for local) / Azure Function App settings (for cloud)

4. **Run locally**
   ```bash
   func start
   ```

5. **Test with Postman**
   - Send a POST request to `http://localhost:7071/api/fill_word` with JSON payload:
     ```json
     {
       "fields": {
         "name": "ರಾಮಕೃಷ್ಣ",
         "address": "ಬೆಂಗಳೂರು",
         "dob": "1990-05-15"
       }
     }
     ```

6. **Deploy to Azure**
   ```bash
   func azure functionapp publish <YourFunctionAppName>
   ```

## 📊 Results & Impact

- ✅ **85%+ speech recognition accuracy** for Kannada
- ✅ **<5 sec end-to-end latency** (speech → document)
- ✅ **No literacy or English required** for users
- ✅ **Supports rural financial inclusion** & aligns with UN SDGs (1, 4, 8, 9, 10)

## 🧪 Testing

- **Local Testing:** Use `func start` + Postman
- **Cloud Testing:** Azure Speech Studio (Voice Playground)
- **Unit Tests:** Pytest for core functions (extensible)

## 📈 Future Enhancements

- Multi-language support (Tamil, Telugu, Hindi, etc.)
- Integration with live banking APIs
- Voice biometrics for authentication
- Mobile app with embedded avatar
- Offline/low-bandwidth mode
- OCR for document verification (Aadhaar, PAN)

## 👨‍💻 Contributors

- **Sushrutha Shanbhogue**  
- **Raghavendra S S**  
- **Sowndarya S**  
- **Iram A.K Shaikh**  

*Under the guidance of **Mr. Raghavendra Sooda**, Assistant Professor, Dept. of CSE, SCEM.*

[Paper submitted to 2026 3rd International Conference on Emerging Trends in Engineering and Medical Sciences]

### 🌍 Social Impact

This project directly supports **financial inclusion**, **digital literacy**, and **regional language preservation** in rural India. By removing language barriers, we empower communities to access formal banking securely and independently.
