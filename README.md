# Nano ORYKSA

**The offline AI of the ORYKSA mobile app.**

When the phone loses signal - on a plane, in a tunnel, in a basement - the ORYKSA
assistant does not go dark. A smaller version of her, **Nano ORYKSA**, takes over
from inside the phone. She is more limited than the ORYKSA you talk to online, but
she carries the memory: your profile, your services, your prices, your opening
hours and your whole Brain.

This repository hosts the model files the app downloads. Nothing here runs on a
server: everything is meant to run on the phone itself.

Developed by **Weslley Harakawa** - [ORYKSA](https://oryksa.com)

---

## What Nano ORYKSA does with no connection

- Answers about your business, from the memory synced to the phone
- Takes note of anything you ask her to change, and runs it the moment you are back online
- Talks with you, and helps you settle when you are stressed or anxious
- Gives emergency numbers and basic first aid, with no connection at all

## What she cannot do offline

- Read new customer messages (those live on the server)
- Book appointments or change your account (they go to a queue instead)
- Search the web

She says so plainly instead of pretending. Anything that needs the server is queued
and executed, one by one, as soon as the phone is back online.

---

## How the app picks a brain

| Phone | What runs | Download |
|---|---|---|
| iPhone 15 Pro and newer, iOS 26 with Apple Intelligence | the model Apple already ships inside iOS | **none** |
| Older iPhones and Android | the model published in this repository | optional, on demand |
| Anything else | memory lookup, no model at all | none |

The ORYKSA app in the stores **never ships a model**. It stays small. The offline AI
is downloaded only if the owner asks for it, and can be deleted at any time to free
up space.

## The memory

Before the signal drops, the app keeps a copy of everything Nano ORYKSA needs to
know. It is text, measured in kilobytes, pulled from `GET /api/app/offline-pack`
and refreshed automatically every time the app opens or comes back to the screen.

## Releases

Model files are published as release assets. The app reads the download address
from the ORYKSA backend, so the model can be swapped or switched off without
shipping a new version of the app.

| Asset | Model | Size | Format |
|---|---|---|---|
| `oryksa-nano.gguf` | Gemma 3 1B Instruct (Q4_K_M) | 778 MB | GGUF |

## Licence of the models

The model weights published here keep the licence of their original authors.
Gemma is distributed under the [Gemma Terms of Use](https://ai.google.dev/gemma/terms)
by Google. Using this repository means accepting those terms.

## About the author

**Weslley Harakawa** - Founder of ORYKSA AI and Chief Innovation Officer at Harakawa Tech. Based in Lisbon, Portugal. Specialties: artificial intelligence, web and mobile development, blockchain tokenization. Education: University of the People.

- Website: https://harakawa.tech
- LinkedIn: https://www.linkedin.com/in/weslleyharakawa/
- Instagram: https://www.instagram.com/weslley.harakawa
- ORYKSA AI Employees: https://oryksa.com (X: https://x.com/oryksa, Instagram: https://www.instagram.com/oryksaai, YouTube: https://www.youtube.com/@ORYKSA)

The ORYKSA name, brand and app are property of Weslley Harakawa.
