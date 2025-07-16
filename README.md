**Status:** 🚧 *Pre‑alpha — planning phase*

---

## What is this project?

A lightweight pipeline that takes recorded meetings (Arabic + English mix), automatically detects each speaker, converts speech to text, and asks a Large Language Model (LLM) to produce:

* **Concise bullet‑point summaries** (Arabic by default, English optional)
* **Action‑item lists** with owner & due date

All with **zero manual note‑taking**.

---

## Why does it matter?

1. **Hands‑free minutes:** Focus on the conversation, not on typing.
2. **Bilingual accuracy:** Handles code‑switching common in MENA tech teams.
3. **Fast MVP:** Built entirely on open models (Whisper, pyannote, GPT‑based LLM).

---

## Planned MVP Features

| Phase | Feature                                   | Notes                                       |
| ----- | ----------------------------------------- | ------------------------------------------- |
| 1     | One‑command CLI (`python run.py <audio>`) | Converts MP4/WAV → summary.md + actions.csv |
| 2     | Speaker diarization                       | Labels as Speaker 1, 2, …                   |
| 3     | Bilingual ASR (Arabic + English)          | Whisper large‑v3 out‑of‑box                 |
| 4     | LLM‑generated bullets & action items      | GPT‑4o via API (configurable)               |
| 5     | Glossary injection                        | Replace company jargon correctly            |

---

## Quick Start (will evolve)

```bash
# Create & activate env
python -m venv venv && source venv/bin/activate
pip install -r requirements.txt

# Run the prototype (placeholder)
python run.py samples/meeting_01.mp4
```

> **Note:** scripts & requirements will be added as we build.

---

## Tech Stack (draft)

* **Python 3.11**
* **ASR:** OpenAI Whisper large‑v3 (local or API)
* **Speaker Diarization:** pyannote.audio pretrained
* **Summarization:** GPT‑4o (or Mistral‑Large) via API
* **Audio Handling:** FFmpeg, pydub

---

## Roadmap

1. 🔊 **Data Ingestion** – confirm recording formats
2. 🗣️ **Diarization Module** – plug pyannote pipeline
3. ✍️ **Transcription** – run Whisper on segments
4. 🧠 **LLM Prompting** – draft summary & action template
5. 🛠️ **Glue Code** – merge into single CLI
6. 📝 **Iterate** – test on 5–10 real meetings

---

## Contributing

Currently a solo build. Once structure stabilizes we’ll open issues & PR guidelines.

---

## License

TBD — likely MIT for code, CC‑BY for docs.

---

*Made with ☕ in Saudi Arabia.*
