---
title: Build JARVIS in Your Hostel Room
---

# Build JARVIS in your hostel room 🤖

The parts list from the reel and how they connect. Most of it is free software on the laptop you already have.

## The parts list

| Part | What it does | Use | Cost |
|---|---|---|---|
| Ears | Speech to text | [Whisper](https://github.com/openai/whisper) (or the faster [faster-whisper](https://github.com/SYSTRAN/faster-whisper)), runs on your laptop | Free, open source |
| Voice | Text to speech | [Kokoro](https://huggingface.co/hexgrad/Kokoro-82M), a small open-weight voice model | Free, open source |
| Eyes | A camera | Your old Android phone with an IP-camera app, on a stand | ₹0 if you have one |
| Seeing | Understands the photo | The [Gemini API](https://ai.google.dev/gemini-api/docs) (vision) | Free tier with limits |
| Brain | Decides what to do next | [Ollama](https://ollama.com/) running Gemma or Llama on your laptop, or the Gemini API | Free |
| Body | Switches your room light | A Wi-Fi smart plug (about ₹700), or an ESP32 board (about ₹400) for low-voltage projects | ₹400–700 |
| Acts on its own | Wakes you, tracks attendance | A Python script that reads your timetable | Free |

Prices are what they usually cost on Amazon.in; check on the day you buy.

## How it connects

```
mic ──► Whisper ──► text ──► brain (Ollama or Gemini) ──► decides:
                                   │   • answer          ──► Kokoro ──► speaker
                                   │   • "light off"     ──► smart plug
                                   │   • "what's this?"  ──► phone camera photo ──► Gemini vision
                                   └── timetable script runs on its own: alarm 30 min before class
```

1. **Listen:** record a few seconds from the mic and transcribe it with Whisper.
2. **Think:** send the text to the brain with a short system prompt: "You are JARVIS. You can call these tools: light_on, light_off, look, next_class, attendance." Ollama and the Gemini API both support tool (function) calling.
3. **Act:** when the brain calls a tool, your Python code does it: switch the plug, grab a photo from the phone's camera URL and send it to Gemini vision, or read the timetable.
4. **Speak:** turn the reply into audio with Kokoro and play it.
5. **On its own:** a scheduled script (cron, Task Scheduler, or Python's `schedule` library) reads your timetable and wakes you 30 minutes before your first class. Give it your attendance numbers and it can refuse to let you bunk when you're at 74%.

## The light, safely

**Please don't touch the mains yourself.** A tube light runs on 230 V.

- **Easiest:** plug the light (or a lamp) into a Wi-Fi smart plug. Many smart plugs can be controlled from Python through community libraries or the brand's own integrations. Check that your plug model is supported before you buy.
- **ESP32:** great for LED strips, sensors and a buzzer, all low voltage. If you want it to switch a mains appliance, get a licensed electrician to do the wiring.

## Make it your final-year project

Write down what each part does, measure how fast it responds (voice in → light off), and show the timetable feature live. That's a project your HOD will actually remember.

Last checked: 13 Nov 2026. Free tiers and prices change, so check each page before you rely on it.

Follow [@souradip.sh](https://www.instagram.com/souradip.sh/) for more.
