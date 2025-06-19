# dwani.ai - knowledge through voice

## Overview

dwani.ai is a self-hosted GenAI platform designed to provide voice AI interaction for Kannada and other Indian languages. 

```bash
pip install --upgrade dwani

import dwani
import os

dwani.api_key = os.getenv("DWANI_API_KEY")

dwani.api_base = os.getenv("DWANI_API_BASE_URL")
```

- gemma3 - with translation
```python
resp = dwani.Chat.create(prompt="Hello!", src_lang="english", tgt_lang="kannada", model="gemma3")
print(resp)
```
```json
{'response': 'ನಮಸ್ತೆ! ಭಾರತ ಮತ್ತು ಕರ್ನಾಟಕವನ್ನು ಗಮನದಲ್ಲಿಟ್ಟುಕೊಂಡು ಇಂದು ನಿಮ್ಮ ಪ್ರಶ್ನೆಗಳಿಗೆ ನಾನು ನಿಮಗೆ ಹೇಗೆ ಸಹಾಯ ಮಾಡಲಿ?'}
```

- gemma3 - without translation
```python
resp = dwani.Chat.direct(prompt="Hello!", model="gemma3")
print(resp)
```
```json
{'response': 'Hello! I am Dwani, ready to assist you with information pertaining to India, specifically Karnataka. '}
```


Website -> [dwani.ai](https://dwani.ai)

[Download App on Google Play](
https://play.google.com/store/apps/details?id=com.slabstech.dhwani.voiceai&pcampaignid=web_share)

## Research Goals

- Measure and improve the Time to First Token Generation (TTFTG) for model architectures in ASR, Translation, and TTS systems.
- Develop and enhance a Kannada voice model that meets industry standards set by OpenAI, Google, ElevenLabs, xAI
- Create robust voice solutions for Indian languages, with a specific emphasis on Kannada.


## Models and Tools

The project utilizes the following open-source tools:

| Open-Source Tool                       | Source Repository                                          | 
|---------------------------------------|-------------------------------------------------------------|
| Automatic Speech Recognition : ASR   | [ASR Indic Server](https://github.com/dwani-ai/asr-indic-server) | 
| Text to Speech : TTS                  | [TTS Indic Server](https://github.com/dwani-ai/tts-indic-server)  | 
| Translation                           | [Indic Translate Server](https://github.com/dwani-ai/indic-translate-server) | 
| Document Parser                       | [Indic Document Server](https://github.com/dwani-ai/docs-indic-server) |
| dwani API Server | [Dwani Server](https://github.com/dwani-ai/dwani-api-server) | 
| dwani Android | [Android](https://github.com/dwani-ai/dwani-android) |
| dwani python sdk | [python-sdk](https://github.com/dwani-ai/dwani-python-sdk) |
| vllm-arm64 | [vllm-arm64](https://github.com/dwani-ai/vllm-arm64) |



## Features

| Feature                      | Description                                                                 |  Components          | 
|------------------------------|-----------------------------------------------------------------------------|-----------|
| Kannada Voice AI                | Provides answers to voice queries using a LLM                     | LLM                 | 
| Text Translate               | Translates text from one language to another.                                |  Translation         |
| Text Query                   | Allows querying text data for specific information.                          | LLM                 | 
| Voice to Text Translation    | Converts spoken language to text and translates it.                          |  ASR, Translation    |
| PDF Translate                | Translates content from PDF documents.                                       |  | Translation         |
| Text to Speech           | Generates speech from text.                                                  |  TTS                 |
| Voice to Voice Translation   | Converts spoken language to text, translates it, and then generates speech.   |  ASR, Translation, TTS|
| Answer Engine with Translate| Provides answers to queries with translation capabilities.                   |  ASR, LLM, Translation, TTS| 

## Contact
- For any questions or issues, please open an issue on GitHub or contact us via email.
- For collaborations
  - Join the discord group - [invite link](https://discord.gg/WZMCerEZ2P) 
- For business queries, Email : sachin (at) dwani (dot) ai



