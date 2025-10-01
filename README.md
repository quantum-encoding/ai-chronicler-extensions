# AI Chronicle - The Scribe

**Browser extension for capturing and exporting your AI conversations from Google AI Studio (Gemini) and ChatGPT.**

![Version](https://img.shields.io/badge/version-1.0.0-blue)
![Chrome](https://img.shields.io/badge/Chrome-Supported-green)
![Firefox](https://img.shields.io/badge/Firefox-Supported-orange)

---

## 🎯 Overview

AI Chronicle is a powerful browser extension that helps you capture, export, and archive your AI conversations. Built by [Quantum Encoding Ltd](https://www.quantumencoding.io) for developers, researchers, and AI enthusiasts who want to keep their valuable AI interactions.

### ✨ Features

- **📥 Download Current Conversation** - Instantly capture the conversation you're viewing
- **🔥 Download All Conversations** - Batch download your entire conversation library
- **⛔ Stop & Resume** - Pause batch downloads and resume from any conversation number
- **📝 Multiple Export Formats** - Markdown, JSON, or Plain Text
- **⚡ Blazing Fast** - Intelligent dot navigation for instant jumps through long conversations (Gemini)
- **🔒 100% Private** - Everything runs locally in your browser

### 🌐 Supported Platforms

| Platform | Single Conversation | Batch Download | Status |
|----------|-------------------|----------------|---------|
| **Google AI Studio (Gemini)** | ✅ | ✅ | Fully Supported |
| **ChatGPT** | ✅ | ✅ | Fully Supported |
| **Claude** | 🟠 | 🟠 | Use [Official Export](https://claude.ai/settings) + [Anthropic Export Extractor](https://github.com/quantum-encoding/anthropic-export-extractor) |

---

## 📦 Installation

### Chrome Web Store
*Coming soon*

### Firefox Add-ons
*Coming soon*

### Manual Installation

#### Chrome
1. Download `chrome-scribe-edition-chrome-v1.0.0.zip` from [Releases](https://github.com/quantum-encoding/ai-chronicler-extensions/releases)
2. Unzip the file
3. Open Chrome and go to `chrome://extensions/`
4. Enable "Developer mode" (top right)
5. Click "Load unpacked" and select the unzipped folder

#### Firefox
1. Download `chrome-scribe-edition-firefox-v1.0.0.zip` from [Releases](https://github.com/quantum-encoding/ai-chronicler-extensions/releases)
2. Unzip the file
3. Open Firefox and go to `about:debugging#/runtime/this-firefox`
4. Click "Load Temporary Add-on"
5. Select the `manifest.json` file from the unzipped folder

---

## 🚀 Usage

### Google AI Studio (Gemini)

#### Download Current Conversation
1. Navigate to any Gemini conversation
2. Click the AI Chronicle extension icon
3. Select your export format (Markdown, JSON, or Plain Text)
4. Click **"Download Current Conversation"**
5. File downloads automatically with conversation title and timestamp

#### Download All Conversations (Batch Mode)
1. Navigate to your [Gemini Library](https://aistudio.google.com/library)
2. Click the AI Chronicle extension icon
3. (Optional) Enter a conversation number to start from (useful for resuming)
4. Click **"Download All Conversations"**
5. Confirm the batch operation
6. Watch the extension work through your library automatically
7. Click **"Stop Batch Download"** anytime to pause

**Pro Tips:**
- You can switch to other tabs while batch downloading continues in the background
- With "Continue running background apps when browser is closed" enabled, downloads continue even if you close the browser
- Check the extension badge for progress (e.g., "15/93")
- Resume interrupted downloads by entering the last completed conversation number

### ChatGPT

#### Download Current Conversation
1. Navigate to any ChatGPT conversation
2. Click the AI Chronicle extension icon
3. Select your export format
4. Click **"Download Current Conversation"**

#### Download All Conversations (Batch Mode)
1. Navigate to your ChatGPT conversation list
2. Click the AI Chronicle extension icon
3. Click **"Download All Conversations"**
4. The extension scrolls through and downloads each conversation

### Claude

**⚠️ The Claude scraper is currently unreliable due to complex DOM structure.**

**Recommended approach:**
1. Use Claude's [official export feature](https://claude.ai/settings) (Account Settings → Export Data)
2. Download the monolithic JSON file
3. Use our [Anthropic Export Extractor](https://github.com/quantum-encoding/anthropic-export-extractor) tool to split it into individual conversations with artifacts

---

## 🔥 Power User Tools

Once you've captured your conversations, unlock advanced search capabilities with our high-performance C-based command-line toolkit:

### [AI Chronicle Toolkit](https://github.com/quantum-encoding/ai-chronicle-toolkit)

Search and analyze your conversations locally at native speed:
- `md2json` - Convert markdown to structured JSON
- `aiquery` - Search conversations with context
- 100% private - everything runs locally

---

## 📁 Export Formats

### Markdown (.md)
```markdown
## Message 1

Your message here...

---

## Message 2

AI response here...

---

### 💭 Model Thoughts (Message 2)

> Thinking process...
> Analysis...
```

### JSON (.json)
```json
{
  "timestamp": "2025-10-01T17:30:25.312Z",
  "platform": "Google AI Studio (Gemini)",
  "stats": {
    "total": 51,
    "messages": 33,
    "thoughts": 18
  },
  "entries": [
    {
      "type": "MESSAGE",
      "text": "Your message here...",
      "order": 0,
      "hasThoughts": false,
      "parentMessage": 0
    },
    {
      "type": "THOUGHTS",
      "text": "AI thinking process...",
      "order": 1,
      "hasThoughts": false,
      "parentMessage": 1
    },
    {
      "type": "MESSAGE",
      "text": "AI response here...",
      "order": 2,
      "hasThoughts": true,
      "parentMessage": 1
    }
  ]
}
```

### Plain Text (.txt)
```
Message 1

Your message here...

--------------------------------------------------

THOUGHTS (Message 2)

AI thinking process...

--------------------------------------------------

Message 2

AI response here...
```

---

## 🛠️ Technical Details

### Filename Format
```
{ConversationTitle}-{Timestamp}-ai-chronicle.{ext}
```

Example:
```
Interactive-Tech-Nexus-Component-Design-2025-10-01T14-30-25-ai-chronicle.md
```

### Permissions
- `activeTab` - Access current tab content
- `storage` - Remember your preferences
- `clipboardWrite` / `clipboardRead` - Copy to clipboard feature
- `scripting` - Run content scripts on AI platforms
- `notifications` - Batch download completion alerts

### Browser Requirements
- **Chrome**: Version 88+
- **Firefox**: Version 112+

---

## 📝 License

MIT License - Copyright (c) 2025 Quantum Encoding Ltd

See [LICENSE](LICENSE) file for details.

---

## 🏢 About Quantum Encoding

**AI Data Export Services**

We build tools that give you control over your AI-generated content.

- 🌐 Website: [quantumencoding.io](https://www.quantumencoding.io)
- 📧 Email: [info@quantumencoding.io](mailto:info@quantumencoding.io)
- 🐛 Issues: [GitHub Issues](https://github.com/quantum-encoding/ai-chronicler-extensions/issues)

---

## 🤝 Contributing

We welcome contributions! If you'd like to help improve AI Chronicle:

1. Fork the repository
2. Create a feature branch
3. Make your changes
4. Submit a pull request

For major changes, please open an issue first to discuss what you'd like to change.

---

## 🔗 Related Projects

- [AI Chronicle Toolkit](https://github.com/quantum-encoding/ai-chronicle-toolkit) - High-performance C-based search tools
- [Anthropic Export Extractor](https://github.com/quantum-encoding/anthropic-export-extractor) - Split Claude exports into individual conversations

---

## ⭐ Support

If you find AI Chronicle useful, please consider:
- ⭐ Starring this repository
- 🐛 Reporting bugs via [GitHub Issues](https://github.com/quantum-encoding/ai-chronicler-extensions/issues)
- 📧 Sharing your feedback at [info@quantumencoding.io](mailto:info@quantumencoding.io)

---

**Made with ❤️ by Quantum Encoding Ltd**
