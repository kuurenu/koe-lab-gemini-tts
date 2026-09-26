# Koe Lab — Gemini TTS Playground

A Japanese, single-page playground for trying Gemini text-to-speech. It is built for GitHub Pages and has no build step or server.

## Features

- Gemini 3.8 Flash TTS and Flash-Lite, with optional legacy Gemini 3.1 and 2.5 Flash TTS models
- Single-speaker narration and two-speaker dialogue, including a separate voice and delivery style for each speaker
- Sustained delivery directions, inline vocal tags, and sample scripts
- Inline pause / breath / laugh tags and pipe-delimited backchannels for overlapping dialogue
- 30 prebuilt voices, the Extended Voice Library, and existing Voice Design / Voice Replication IDs
- WAV, Linear PCM, μ-law, and A-law output, with 24 kHz, 16 kHz, or 8 kHz sample rates on Gemini 3.8
- Streaming audio reception, cancel, in-page playback, and download

## Run on GitHub Pages

1. In the repository, open **Settings → Pages**.
2. Choose **Deploy from a branch**, select `main` and `/ (root)`, then save.
3. Open the Pages URL after GitHub finishes its first deployment.

The site is plain HTML, CSS, and JavaScript. There are no packages to install and no build command.

## Use

Enter a Gemini API key in the page, choose a model and voice, then generate speech. The key is held in the open page only and sent directly to the Gemini API in a request header. This project does not store the key, text, or generated audio and has no backend or analytics. Do not put an API key in this repository or use the site on a shared computer with a key you do not control.

Voice Design and Voice Replication are created through Google's tools. Paste the resulting voice ID into the site. Custom voice IDs in a two-speaker script are synthesized turn by turn, which makes additional API requests. Gemini API availability, quotas, and billing depend on the Google project and selected model.

## API reference

- [Gemini text-to-speech guide](https://ai.google.dev/gemini-api/docs/speech-generation)
- [Google AI Studio API keys](https://aistudio.google.com/apikey)
