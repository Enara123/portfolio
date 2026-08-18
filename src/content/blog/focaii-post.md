---
title: "Focaii – AI note-taking"
description: "Building an AI-powered note-taking app with GPT and voice input."
date: "2026-08-01"
---

# Focaii – AI note-taking

I recently spent a month building a productivity app called Focaii that uses AI to make note-taking simpler.

---

## What is Focaii?

It’s a note-taking app that automatically structures and summarizes your notes using AI.

I wanted to solve two main problems I face when taking notes:

1. **Structure**: I often dump ideas without organizing them, making them hard to search later.
2. **Time**: Summarizing long notes or audio recordings takes time I don't always have.

Focaii solves this by:
- Automatically tagging and categorizing notes.
- Generating summaries for long notes or voice recordings.
- Allowing you to ask questions about your notes (e.g., "What did I learn about X?") and get AI-powered answers.

---

## Why I built it

I wanted to understand how AI could improve productivity tools, especially for students and researchers.
I also wanted hands-on experience integrating:
- Text and voice input
- AI summarization
- Semantic search

---

## Tech stack

I used:
- **Frontend**: React + Vite
- **Backend**: Node.js + Express
- **Database**: Supabase
- **AI**: OpenAI API
- **Voice**: Web Speech API

---

## Key features

### 1. Voice notes with auto-transcription

You can record notes using your microphone, and the app automatically transcribes and saves them.

### 2. AI summaries

For long notes or voice recordings, the AI generates a summary. This is super useful for quickly reviewing topics before a test or meeting.

### 3. Smart search

Instead of only searching for keywords, Focaii uses AI to understand the *meaning* of your query. For example, if you search "productivity tips", it can find notes that talk about productivity even if they don't use those exact words.

### 4. Auto-tagging

When you save a note, the AI suggests relevant tags. This helps keep your notes organized without manual effort.

---

## How it works

1. **User records voice note** → Web Speech API transcribes it
2. **Text sent to OpenAI API** → AI extracts summary + tags
3. **Note + metadata saved to Supabase**
4. **User searches** → Query goes through AI-powered search to find relevant notes

---

## Challenges I faced

- **Latency**:
  - Voice transcription and AI summaries take time.
  - I implemented loading states and background processing to keep the UI responsive.

- **Accuracy**: AI summaries can sometimes miss key details.
  - I added a feature where you can edit the AI summary.

- **Cost**: OpenAI API calls cost money, especially for long voice notes.
  - I implemented rate limiting and cost estimation.

---

## Results

I used Focaii for my own notes for about two weeks, and it saved me significant time.
Getting quick summaries of long recordings was especially helpful.

---

## What I learned

- Integrating voice and AI is more complex than standard text input
- Real-time transcription requires careful handling of audio chunks
- AI summaries are great but still need human review for important content
- Managing API costs is crucial for side projects

---

## Future ideas

- Integration with Google Calendar to automatically summarize notes related to meetings
- Multi-language support
- Export notes to Notion/Evernote
- More sophisticated AI analysis (e.g., identifying action items, key decisions)

---

## Try it out

You can check out Focaii here:

- **[Try Focaii](http://focaii.com)**

---

## Feedback welcome

Since this was a personal project, I'd love to hear what you think. Feel free to share any feedback or suggestions!