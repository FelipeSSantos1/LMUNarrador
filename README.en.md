# Narrador LMU

🇧🇷 [Português](README.md) · 🇬🇧 **English**

Live two-voice race commentary for **Le Mans Ultimate (LMU)**: a **narrator** who describes the
action and a **commentator** who analyses the race. Built for streams and recordings: the audio
comes out on a separate channel, and you pick it up in OBS with VB-Cable.

> **Language note:** the narration is in **Brazilian Portuguese** and the app interface is in
> Portuguese. This page is a full English guide. Whenever it mentions a tab or button, the
> Portuguese name shown in the app is given in *italics*. See the [interface glossary](#interface-glossary).

This is where you download the app and find the steps to activate your subscription and set up
the AI service keys.

- Download the latest version from **[Releases](https://github.com/FelipeSSantos1/LMUNarrador/releases/latest)**.
- Subscription (monthly or yearly): **[buy a license](https://lmunarrador.lemonsqueezy.com/checkout/buy/c4b8a09f-1c1d-4f7e-a5c7-00b046d23bbc?enabled=2317876%2C2317894)**.

---

## Contents

- [See it in action](#see-it-in-action)
- [What it does](#what-it-does)
- [Requirements](#requirements)
- [Subscription](#subscription)
- [Interface glossary](#interface-glossary)
- [1. Installation](#1-installation)
- [2. Activate your subscription](#2-activate-your-subscription)
- [3. API keys: what they are and where to paste them](#3-api-keys-what-they-are-and-where-to-paste-them)
- [4. Create a Gemini key](#4-create-a-gemini-key)
- [5. Create a DeepSeek key](#5-create-a-deepseek-key)
- [6. Emotion voice (optional): ElevenLabs](#6-emotion-voice-optional-elevenlabs)
- [7. Updating the app](#7-updating-the-app)
- [8. Troubleshooting](#8-troubleshooting)
- [9. Privacy](#9-privacy)

---

## See it in action

- Channel with many videos of the app at work: **https://www.youtube.com/@LMUinVR**
- Example video: [watch on YouTube](https://youtube.com/shorts/gEExHJTlZ5o)

| | |
|:---:|:---:|
| <img src="https://github.com/user-attachments/assets/38d7f3b1-ac04-443a-9c38-07fa38eb75cf" width="420" alt="Dashboard tab"><br>**Dashboard** (*Painel*) | <img src="https://github.com/user-attachments/assets/ec4c0146-9482-446a-9247-10a6c6178bcf" width="420" alt="Voices tab"><br>**Voices** (*Vozes*) |
| <img src="https://github.com/user-attachments/assets/cbdc1126-75b7-4c91-b159-9669ce7f2e64" width="420" alt="Personality tab"><br>**Personality** (*Personalidade*) | <img src="https://github.com/user-attachments/assets/fdf4aead-653d-4a9f-8bbc-6fd11a14773e" width="420" alt="Keys tab"><br>**Keys** (*Chaves*) |
| <img src="https://github.com/user-attachments/assets/1eee11cf-0d56-4d88-8cf9-bd65e72a2259" width="420" alt="LLM tab"><br>**LLM** | |

---

## What it does

- **Reads the game directly.** Uses LMU's shared-memory telemetry. No plugin to install: just
  switch on *Enable Plugins* in the game settings.
- **Two voices that talk to each other.** The narrator describes the action; the commentator
  analyses the race. Each event produces 1 to 3 short lines.
- **Knows what matters.** Focuses on your car's class (for example GT3). Warns you when
  faster-class cars approach from behind, and also calls out serious events of any class:
  crashes, a leader spinning, full-course yellow (FCY) and rain.
- **Never slows the game.** Telemetry runs on its own threads and never waits for the
  narration or the audio.
- **Stream-ready.** Sends the narration to a separate audio device (for example VB-Cable),
  which shows up as its own source in OBS. It can also play through your speakers.
- **Portable.** One folder, no installer, and nothing written outside it. To uninstall, delete
  the folder.
- **Never goes silent.** If the AI service is slow or fails, the app falls back to ready-made
  lines (templates).

---

## Requirements

- Windows 11 (64-bit)
- Le Mans Ultimate with *Settings → Gameplay → Enable Plugins → ON* (fully close and reopen
  the game after turning it on)
- About 500 MB of disk space (the local voices are included)
- Optional: an API key for **Gemini** and/or **DeepSeek**, for AI-written lines
- Optional: [VB-Cable](https://vb-audio.com/Cable/) to send the narration to OBS as a separate
  source

---

## Subscription

Sales are handled by [Lemon Squeezy](https://www.lemonsqueezy.com/), which takes care of payment
and taxes. After you buy, the license key arrives by email.

| Plan | Price | Includes |
|-------|-------|--------|
| Monthly | CA$ 2.99 / month | Full app: AI-written lines and all voices (you use your own AI key) |
| Yearly | CA$ 29.90 / year | Same as monthly, with 2 months free |

**Without a license** the app opens and narrates using templates only, with the local voices
(Piper and Kokoro). AI-written lines and the optional emotion voices (ElevenLabs and Gemini
TTS) require an active subscription.

- **One active computer per key.** To use another PC, open the app on the first one, go to the
  **License** tab (*Licença*) and click **Deactivate this computer** (*Desativar este
  computador*); then activate the key on the other one.
- The license is checked online every 6 hours and stays valid for up to 7 days without internet.
- If the subscription ends, the app goes back to templates only. Renew to get AI-written lines
  back.

---

## Interface glossary

The app is in Portuguese. Here is what you will see:

| In the app | Meaning |
|---|---|
| **Painel** | Dashboard |
| **Geral** | General |
| **Vozes** | Voices |
| **LLM** | LLM (the AI that writes the lines) |
| **Eventos** | Events |
| **Personalidade** | Personality |
| **Chaves** | Keys |
| **Licença** | License |
| **Avançado** | Advanced |
| **Ativar** | Activate |
| **Desativar este computador** | Deactivate this computer |
| **Renovar/Assinar** | Renew / Subscribe |
| **Minhas compras** | My orders |
| **Salvar chaves** | Save keys |
| **Carregar vozes** | Load voices |
| **Ouvir** | Listen (test the voice) |
| "LMU: aguardando o jogo" | "LMU: waiting for the game" |
| "Licença ativa neste computador" | "License active on this computer" |
| "vencida" | "expired" |
| "Licença não confirmada" | "License not confirmed" |
| "Licença necessária" | "License required" |
| "Esta licença já está ativa em outro computador" | "This license is already active on another computer" |

---

## 1. Installation

The app is **portable**: one folder, no installer. To uninstall, delete the folder.

1. On [Releases](https://github.com/FelipeSSantos1/LMUNarrador/releases/latest), download the file `NarradorLMU-<version>-win64.zip`.
2. **Extract** the `.zip` to a folder of your choice, for example `D:\Apps\NarradorLMU`. Always use the same folder: your keys, license and settings live inside it.
3. **Enable the plugin in LMU:** *Settings → Gameplay → Enable Plugins → ON*. Then **fully close and reopen the game**. Without this, the app stays on "LMU: aguardando o jogo" (waiting for the game).
4. Run LMU and `NarradorLMU.exe` with the **same permission level**: both normal (recommended) or both as administrator. Mixing them makes telemetry reading fail with no error message.
5. Double-click `NarradorLMU.exe`.

**Windows warning:** the `.exe` does not have a company code-signing certificate. Windows Defender or SmartScreen may show a warning the first time ("Windows protected your PC"). If you downloaded it from the official link above, click **More info → Run anyway**.

**Audio:** the app uses local voices (Piper and Kokoro) that come in the folder. To send the narration to OBS as a separate source, install [VB-Cable](https://vb-audio.com/Cable/) and pick the output device in the **General** tab (*Geral*).

---

## 2. Activate your subscription

**Without a license the app opens and narrates, but only with ready-made lines (templates).** It does not use the AI (Gemini or DeepSeek) or the emotion voice. The local voices keep working. With an active license, the AI and the emotion voice are unlocked.

### Step by step

1. **Buy the subscription** here: **[buy a license](https://lmunarrador.lemonsqueezy.com/checkout/buy/c4b8a09f-1c1d-4f7e-a5c7-00b046d23bbc?enabled=2317876%2C2317894)**. Choose the monthly or the yearly plan. Billing is handled by Lemon Squeezy.
2. **Find the license key in the email** you used for the purchase. It is also on your Lemon Squeezy orders page ("My Orders").
3. In the app, open the **License** tab (*Licença*).
4. **Paste the key** into the field (it is masked) and click **Activate** (*Ativar*).
5. The tab now shows **"License active on this computer"** (*Licença ativa neste computador*). The AI and the emotion voice you configured start working again from the next line, with no restart.

> For the AI to actually narrate you still need your own Gemini or DeepSeek key (sections 3 to 5).

### License rules

- **One active computer per key.** To use another PC, open the app on the first one and click **Deactivate this computer** (needs internet). Then activate the same key on the other PC. If the first PC no longer exists (reformatted, broken), message me on Discord to free the slot.
- **Pasting the already-active key again** only tells you it is already active on this computer. Pasting a **different** key replaces the license, and the previous one is deactivated on this computer.
- **When the subscription ends** (cancelled or expired), the tab shows **"vencida"** (expired) and the app goes back to templates only from the next line. A warning line also appears in the main window. To come back, renew in **My Orders** (*Minhas compras*) or subscribe again with the **Renew/Subscribe** button (*Renovar/Assinar*) on the tab. A new subscription may issue a new key: activate it on the tab.
- **Offline:** the app checks the license every 6 hours and **tolerates up to 7 days** without being able to check. After that it shows "Licença não confirmada" (License not confirmed) until the internet is back, and then recovers on its own within a few minutes.
- **Windows clock:** setting the computer clock back invalidates the license until the next online check. Keep automatic time on.
- The `licenca.dat` file, in the app folder, stores the license state. It is tied to your computer. **Do not edit it, copy it to another PC or share it**: it contains your key.

---

## 3. API keys: what they are and where to paste them

The app uses third-party AI services to write the lines and, if you want, for the emotion voice. Each service requires a **personal API key**: a password that identifies your account, **created by you**. Usage is billed (or uses the free quota) **on your account**, not mine.

| What for | Service | Required? |
|---|---|---|
| Writing the lines (the "AI") | **Gemini** (Google) **or** DeepSeek | You need **one of the two** |
| Emotion voice | **ElevenLabs** (or Gemini TTS, with the same Gemini key) | Optional |

**Where to paste:** the **Keys** tab (*Chaves*) in the app. There is one block per service: paste the key into the field and click **Save keys** (*Salvar chaves*). After saving, the app only shows the last 4 characters. Keys are stored **only on your computer**, in the `chaves.toml` file inside the app folder.

Security rules:

- **Never share** an API key or the `chaves.toml` file. Whoever has the key spends your account.
- If a key leaks, **delete it on the service's website** and create another.
- Set a **spending limit** on the service account if it offers one.

Prices and free quotas change often: always check each service's website.

---

## 4. Create a Gemini key

Gemini is Google's AI service. The key is generated in **Google AI Studio**.

1. Go to **<https://aistudio.google.com/apikey>** and sign in with your Google account.
2. Click **Create API key**. If asked, pick or create a project.
3. **Copy** the key (it starts with `AIza…`).
4. In the app, **Keys** tab (*Chaves*), **Gemini** block: paste it and click **Save keys** (*Salvar chaves*).
5. In the **LLM** tab, choose **Gemini**.

Google's documentation on the key: <https://ai.google.dev/gemini-api/docs/api-key>.
Pricing and limits: <https://ai.google.dev/gemini-api/docs/pricing>.

The same Gemini key also works for the **Gemini TTS emotion voice** (section 6).

---

## 5. Create a DeepSeek key

DeepSeek is an alternative to Gemini for writing the lines.

1. Create an account at **<https://platform.deepseek.com>** and sign in.
2. Open the keys page: **<https://platform.deepseek.com/api_keys>**.
3. Click **Create new API key**, give it a name (for example "Narrador LMU") and **copy the key right away**: once created it is **not shown again**.
4. DeepSeek usually requires a **balance on the account** (prepaid top-up) for the key to work. If the app says the key was rejected or there is no balance, check your account's billing page.
5. In the app, **Keys** tab (*Chaves*), **DeepSeek** block: paste it and click **Save keys** (*Salvar chaves*).
6. In the **LLM** tab, choose **DeepSeek**.

Documentation: <https://api-docs.deepseek.com/>.

If the app says "Licença necessária" (License required) when you pick Gemini or DeepSeek, your license is not active yet (section 2).

---

## 6. Emotion voice (optional): ElevenLabs

Besides the local voices (Piper and Kokoro), the app can use an online **emotion voice**. It speaks the strongest moments of the race (crash, leader spinning, overtake, finish) with more expression.

**Two advantages:**

- **Uses less of your PC's CPU.** Local voices are generated by your processor, which hurts when the game and the stream already use a lot of it. The emotion voice is generated on the service's servers and only the audio comes back.
- It sounds more natural and expressive.

**The cost:** it needs an **ElevenLabs account** and a **personal API key**. Each line spends credits from **your** ElevenLabs account.

### How to set up ElevenLabs

1. Create an account at **<https://elevenlabs.io>**.
2. Once signed in, open **<https://elevenlabs.io/app/settings/api-keys>**. If the address changes, look for **API Keys** in your account menu.
3. Click to **create a key**, give it a name (for example "Narrador LMU") and **copy** it. If ElevenLabs lets you restrict the key's permissions, leave only what is needed to generate speech and list voices.
4. In the app, **Keys** tab (*Chaves*), **ElevenLabs** block: paste it and click **Save keys** (*Salvar chaves*).
5. **Voices** tab (*Vozes*): choose the **elevenlabs** engine, click **Load voices** (*Carregar vozes*) and pick a voice from your account. On the free plan, library voices may be rejected by the API: use a voice that is **yours** or on your list. For the narrator and the commentator to sound different, pick **different voices**.
6. Use the **Listen** button (*Ouvir*) to test. If it fails, it shows the reason (for example "chave recusada", key rejected, or "voz não encontrada", voice not found).
7. **Restart the app** for the engine change to take effect.

ElevenLabs documentation:

- How the API key works: <https://elevenlabs.io/docs/api-reference/authentication>
- Quickstart: <https://elevenlabs.io/docs/quickstart>
- Plans and pricing: <https://elevenlabs.io/pricing>

### How much of the race it covers

In the **Voices** tab (*Vozes*) the **Coverage** option (*Cobertura*) controls the spend:

| Coverage | What is spoken with the emotion voice |
|---|---|
| **críticos** (critical, default) | Only the narrator, on critical events. The rest stays on the local voices. This is the cheapest option. |
| **narrador** (narrator) | All of the narrator's lines. |
| **tudo** (everything) | Narrator and commentator, the whole broadcast. |

Start with **críticos**. The more lines on the emotion voice, the more credits you spend. The app has a **daily call limit** to protect your wallet: when it runs out, lines continue on the local voices. If a line fails or is slow, it plays on the local voice and the narration goes on.

### Alternative: Gemini TTS

If you already have a Gemini key, the **gemini** engine in the **Voices** tab (*Vozes*) uses the same key, with no new account. Setup is the same: pick the engine, the voice, test with **Listen** (*Ouvir*) and restart the app.

> The emotion voice also only works with an **active license**.

---

## 7. Updating the app

When it starts, the app checks whether a new version exists and shows a link in the main window ("Versão X disponível — baixar", meaning "Version X available — download"). Updating is **manual**:

1. Download the new `.zip` from [Releases](https://github.com/FelipeSSantos1/LMUNarrador/releases/latest).
2. Close the app.
3. Extract the new version into a **new folder** (not over the old one: the `.zip` ships a default `config.toml` that would erase your settings). Then **copy** your `chaves.toml`, `config.toml` and `licenca.dat` files from the old folder to the new one.
4. Open the app. If the license is not recognized, activate the key again in the **License** tab (*Licença*).
5. When everything works, delete the old folder.

Read the notes for each version on [Releases](https://github.com/FelipeSSantos1/LMUNarrador/releases): when a version changes some `config.toml` value that you need to adjust, it is mentioned there.

---

## 8. Troubleshooting

- **"LMU: aguardando o jogo" (waiting for the game).** Check *Enable Plugins* in the game (section 1), fully close and reopen LMU, and use the same permission level for both.
- **The License tab says "Licença não confirmada" (not confirmed).** No internet for more than 7 days, or the Windows clock is wrong. Connect and check that automatic time is on. The app retries on its own.
- **"Esta licença já está ativa em outro computador" (already active on another computer).** Use **Deactivate this computer** on the other PC, or message me on Discord if it no longer exists.
- **"Licença necessária" (License required).** The subscription is not active. Activate the key (section 2) or renew.
- **The AI does not speak, only ready-made lines.** The Gemini/DeepSeek key is missing, was rejected, or the account has no balance/quota. Check the **Keys** tab (*Chaves*) and the LLM indicator in the main window.
- **The emotion voice falls back to the normal voice.** ElevenLabs key missing or rejected, voice not found, credits running low or daily limit reached. Test with **Listen** (*Ouvir*).
- **No sound in OBS.** Choose the VB-Cable device in the **General** tab (*Geral*) and restart the app.

For other problems, open an *issue* in this repository or message me on Discord: **https://discord.gg/M57WADguZ**. If you can, attach the file from the `logs\` folder (it does not contain your keys).

---

## 9. Privacy

- Your API keys stay **only on your computer**, in `chaves.toml`. The app does not send them to me or write them to logs.
- To validate the license, the app contacts **Lemon Squeezy** (`api.lemonsqueezy.com`) and sends the **license key** and your **computer name**. Nothing else is sent for validation, and the app does not store your purchase details.
- To write the lines, the app sends the **text of the race events** (positions, times, incidents) to the AI service you chose, using **your** key and subject to its terms.
- The app does not send your game telemetry anywhere else.

---

*Narrador LMU is an independent fan project and is not affiliated with or endorsed by Studio 397, Motorsport Games or the FIA WEC.*
