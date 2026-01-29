# AudioBrain 🧠 

**AudioBrain** is a professional-grade Telegram bot built with n8n that transforms voice notes into actionable, structured summaries using AI. It is specifically designed to bypass standard platform limitations to provide a seamless "upload and forget" experience.

## 🔗 Link to Bot
Start using the bot here: [@AudioBrain_bot](https://t.me/AudioBrain_bot)
  
## 🚀 Key Features
- **Large File Support (v2.0):** Bypasses the 20MB Telegram Bot API limit and Groq's 25MB limit using a custom MTProto Bridge and on-the-fly Cloudinary compression.
- **Voice-to-Text:** Powered by Groq (Whisper-large-v3) for lightning-fast transcription.
- **AI Analysis:** Powered by Claude 3.5 Sonnet (Anthropic) to extract summaries, action items, and insights.
- **Bilingual & Context-Aware:** Seamlessly handles Hebrew and English, responding in the same language as the audio.
- **Privacy-First:** Automatic cloud storage cleanup (Delete-on-Completion) ensures your data is never stored longer than necessary.

## 🛠 Tech Stack & Architecture
AudioBrain isn't just a simple bot; it's a distributed system designed for scale:
- **n8n:** The central orchestrator managing the logic and API flows.
- **Node.js Microservice (Render):** A custom-built MTProto bridge that acts as a User-Client to download large files.
- **Cloudinary:** High-speed media storage and real-time audio transformation (Bitrate & Codec optimization).
- **Groq API:** Sub-second transcription using Whisper-large-v3.
- **Anthropic API:** Advanced LLM for high-fidelity summarization.

## 💡 The Problem & The Solution
**The Problem:** Telegram Bots are limited to 20MB files, and LLM providers (like Groq) often cap uploads at 25MB. This makes summarizing long lectures or meetings impossible with standard tools. **The Solution:** AudioBrain detects large files and routes them through a dedicated "Bridge." The bridge optimizes the audio (32kbps Mono) to shrink the file size by up to 80% without losing speech quality, ensuring it fits perfectly into the AI's processing window.

## 📅 Roadmap (Upcoming)
### v3.0 - Productivity Ecosystem
- **Calendar Integration**: Automatic creation of Google Calendar events/reminders directly from voice notes.
- **Personalized Storage**: Users can choose where to save meeting summaries (Notion, Google Sheets, or Obsidian) via bot commands.

---
🛠️ **Developed by:** [Inbal Sertshuk](https://www.linkedin.com/in/inbal-sertshuk-46858519)
