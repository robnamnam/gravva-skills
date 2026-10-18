# Gravva program builder

Let an AI assistant design a workout program for the [Gravva](https://getgravva.com) calisthenics tracker. It produces one JSON file that you load in the app: **Programs → My Programs → Import**.

Pick your assistant:

## Claude (skill)

1. Download this repo (Code → Download ZIP) or zip the `claude/gravva-program` folder.
2. **Claude.ai / desktop:** Settings → Capabilities → Skills → upload the zip.
   **Claude Code:** copy `claude/gravva-program` to `~/.claude/skills/`.
3. Ask: "Make me a 3-day rings program, intermediate, 45 min sessions."

## ChatGPT (custom GPT)

1. ChatGPT → Explore GPTs → Create.
2. Paste `gpt/INSTRUCTIONS.md` into **Instructions**.
3. Upload `gpt/exercises.md` under **Knowledge**.
4. Ask for a program, copy the JSON it returns.

## Gemini (Gem)

1. Gemini → Gem manager → New Gem.
2. Paste `gemini/INSTRUCTIONS.md` into **Instructions**.
3. Add `gemini/exercises.md` as a knowledge file.
4. Ask for a program, copy the JSON it returns.

## Any other chatbot

Paste `gpt/INSTRUCTIONS.md` and `gpt/exercises.md` at the start of a chat, then describe the program you want.

## Importing into Gravva

Save the JSON as `my-program.json` (or copy it), then in the app: Programs → My Programs → Import. The app validates the file and tells you what is wrong if anything is.

`exercises.md` is generated from the app's exercise catalogue; the format spec is in `SKILL.md`.
