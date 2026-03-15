# 🤖 Chatbot — React-Powered Web Chatbot

A simple, interactive chatbot web application built with **React.js** (via CDN) and a pre-built chatbot response library. Features a clean chat UI with user and robot message bubbles, auto-scrolling, and real-time responses.

---

## 🖼️ Preview

```
┌─────────────────────────────┐
│                             │
│  🤖 Hello! How can I help?  │
│                             │
│          Hi there!  👤      │
│                             │
│  🤖 Hey! What's up?         │
│                             │
│ [Send a message...] [Send]  │
└─────────────────────────────┘
```

---

## ✨ Features

- 💬 Real-time chat interface with user and robot message bubbles
- 🤖 Automated responses powered by `supersimpledev/chatbot.js`
- 🔄 Auto-scroll to the latest message
- 🎨 Clean, minimal UI with distinct styling for user and robot messages
- 📱 Centered, responsive layout (max-width 600px)
- 🆔 Unique message IDs using `crypto.randomUUID()`

---

## 🗂️ Project Structure

```
chatbot/
├── index.html        # Main application file (HTML + React + CSS)
├── robot.png         # Robot avatar image
└── user.png          # User avatar image
```

---

## ⚙️ Tech Stack

| Technology       | Purpose                                      |
|------------------|----------------------------------------------|
| HTML/CSS         | Structure and styling                        |
| React.js (CDN)   | UI components and state management           |
| Babel (CDN)      | JSX transpilation in the browser             |
| chatbot.js (CDN) | Pre-built chatbot response engine            |

> All dependencies are loaded via CDN — no build tools or npm required.

---

## 🚀 Getting Started

### Prerequisites
- Any modern web browser (Chrome, Firefox, Edge, Safari)
- A local web server (recommended) OR just open the file directly

### Run Locally

**1. Clone the repository**
```bash
git clone https://github.com/YOUR_USERNAME/chatbot.git
cd chatbot
```

**2. Add avatar images**

Place the following images in the project root:
- `robot.png` — Robot/bot avatar
- `user.png` — User avatar

**3. Open in browser**

Option A — Open directly:
```
Double-click index.html
```

Option B — Use a local server (recommended for best results):
```bash
# Using Python
python -m http.server 3000

# Then open: http://localhost:3000
```

---

## 🧩 Component Breakdown

### `App`
- Root component
- Manages `chatMessages` state (array of message objects)
- Pre-loaded with sample conversation

### `ChatMessages`
- Renders the scrollable list of all messages
- Uses `useRef` + `useEffect` to auto-scroll to the latest message

### `ChatMessage`
- Renders a single message bubble
- Conditionally styles and positions based on `sender` (`'user'` or `'robot'`)
- Displays avatar image on the appropriate side

### `ChatInput`
- Controlled input field with `inputText` state
- Sends user message and fetches bot response on button click
- Clears input after sending

---

## 💬 Message Object Structure

```js
{
  message: "Hello! How can I help?",  // Message text
  sender: "robot",                    // "user" or "robot"
  id: "550e8400-e29b-41d4-..."        // Unique ID (crypto.randomUUID)
}
```

---

## 🔮 Future Improvements

- Add keyboard support (press Enter to send)
- Integrate a real AI/NLP API (OpenAI, Gemini, etc.)
- Add typing indicator animation for the bot
- Support message timestamps
- Add dark mode toggle
- Make it mobile-responsive with a full-screen layout
- Allow users to clear chat history

---

## 📄 License

MIT License — free to use, modify, and distribute.

---

## 🙋‍♂️ Author

Built with ❤️ —Rajan Singh

<img width="1920" height="1080" alt="Screenshot 2026-03-11 204910" src="https://github.com/user-attachments/assets/e547f1c9-c319-4adc-97ba-0de2e22453da" />
