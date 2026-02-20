# 🤖 IAdnan AI — Multi-Personality Chatbot

A personal AI chatbot powered by **Groq API** (Llama 3.3 70B), featuring 4 switchable personalities loaded dynamically from an XML file — no frameworks, pure HTML, CSS, and JavaScript.

---

## ✨ Features

- 🧠 **Groq AI Powered** — Uses Llama 3.3 70B model for fast, intelligent responses
- 🎭 **4 Personalities** — Switch between Public, Education, Funny, and Creativity modes
- 📄 **XML-Driven Config** — Personalities and system prompts loaded from `personalities.xml`
- 💬 **Live Chat UI** — Smooth message animations with typing indicator (bouncing dots)
- ⌨️ **Enter to Send** — Press Enter for quick messaging
- 🌐 **RTL Support** — Full Arabic right-to-left layout
- 📱 **Fully Responsive** — Optimized for all screen sizes from 360px to desktop
- 🔄 **Conversation Memory** — Maintains full message history per session

---

## 🚀 How to Use

1. Clone the repository:
   ```bash
   git clone https://github.com/Adnan-Ghiyath/Certificate-generator.git
   ```
2. Get a free API key from [Groq Console](https://console.groq.com)
3. Open `IAdnan_Ai.js` and replace the API key:
   ```js
   const API_KEY = "your_groq_api_key_here";
   ```
4. Open `IAdnan_Ai.html` in your browser — **requires a local server** due to XML fetch:
   ```bash
   # Using VS Code Live Server, or:
   npx serve .
   ```

---

## 📁 Project Structure

```
IAdnan_Ai.html         # Main HTML page (RTL Arabic layout)
IAdnan_Ai.css          # All styles and responsive design
IAdnan_Ai.js           # Groq API calls, XML loading, chat logic
personalities.xml      # AI personalities and system prompts config
```

---

## 🎭 Personalities (from XML)

| Icon | Name | Description |
|------|------|-------------|
| 👔 | Public | General helpful assistant |
| 🎓 | Education | Science and learning tutor |
| 🤡 | Funny | Humorous and entertaining |
| 🎨 | Creativity | Creative ideas and storytelling |

Personalities are defined in `personalities.xml` and loaded dynamically — you can add or modify them without touching the JavaScript code.

---

## ⚙️ How It Works

```
Page loads
      ↓
loadPersonalitiesFromXML() → fetch + DOMParser → fill topic menu
      ↓
Default personality selected (Public)
      ↓
User types message → selects personality → sends
      ↓
Build API messages: [system prompt (from XML), ...history, user message]
      ↓
POST to Groq API → llama-3.3-70b-versatile
      ↓
Show typing indicator → receive response → render in chat
```

**Key concepts used:**
- `fetch()` + `DOMParser` for XML parsing
- Groq API (OpenAI-compatible format)
- Conversation history array (`messages[]`)
- Dynamic DOM rendering with animations
- Responsive CSS with RTL direction

---

## 🔗 API Used

| API | Model | Cost |
|-----|-------|------|
| [Groq](https://console.groq.com) | llama-3.3-70b-versatile | Free tier available |

---

## ⚠️ Security Note

> The API key is currently stored directly in `IAdnan_Ai.js`. For a public repository, consider using environment variables or a backend proxy to keep your key secure.

---

## 🛠️ Built With

![HTML5](https://img.shields.io/badge/HTML5-E34F26?style=flat&logo=html5&logoColor=white)
![CSS3](https://img.shields.io/badge/CSS3-1572B6?style=flat&logo=css3&logoColor=white)
![JavaScript](https://img.shields.io/badge/JavaScript-F7DF1E?style=flat&logo=javascript&logoColor=black)
![Groq](https://img.shields.io/badge/Groq-AI-F55036?style=flat)

- Pure Vanilla JavaScript
- Groq API (Llama 3.3 70B)
- XML for personality configuration
- Zero dependencies — no npm, no frameworks

---

## 📄 License

This project is open source and available under the [MIT License](LICENSE).

---

> Made with ❤️ by [Adnan-Ghiyath](https://github.com/Adnan-Ghiyath)
