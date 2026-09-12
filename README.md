# AirGapScribe — offline meeting transcription for Windows

Records your meetings, transcribes them, and writes the summary **without sending a single word to the internet**. No bot joins your call. No account. No cloud.

This repository hosts the public installers for the free Demo. The application source code is private.

**Download:** [Releases](../../releases) · [Microsoft Store](https://apps.microsoft.com/detail/9NWK1NZVHG8X) · [airgapscribe.com](https://airgapscribe.com)

---

## Why this exists

Most meeting-notes tools send your audio to a server, and many of them join the call as a visible bot. That is a problem in three situations that keep coming up:

- **Your IT department blocks them.** Otter, Fireflies and Zoom AI are commonly blocked on corporate networks, and asking for an exception takes weeks.
- **You are under an NDA or professional confidentiality.** Lawyers, therapists, auditors and HR often cannot upload a recording anywhere, at all.
- **You have no connection.** A plane, a basement meeting room, a client site with locked-down guest wifi.

AirGapScribe runs the whole pipeline on the machine, so none of those situations stop it.

## How it works

| | |
|---|---|
| **Audio capture** | Microphone and system audio recorded separately, so a video call keeps both sides distinguishable |
| **Transcription** | Whisper, running locally. English and Spanish, with a custom vocabulary for names and jargon |
| **Summary** | A local AI model writes the minutes when the recording stops |
| **Chat** | A local assistant you can ask about meetings you already recorded |
| **Account** | None. There is nothing to sign up for |

The base transcription model and a 1,066 MB local AI model **ship inside the installer** — a fresh install can record, transcribe and summarize with nothing else downloaded.

Optional downloads exist, are always requested by you, and always show their size first: an NVIDIA acceleration pack (780 MB compressed, 1,647 MB on disk), a larger AI model that hallucinates less when summarizing (2,008 MB), and additional transcription models (75–2,900 MB).

## Verifying the "local only" claim

You do not have to take this on faith, and the free Demo is enough to check it:

1. Install it and put the machine in airplane mode, or pull the network cable.
2. Record and transcribe a meeting. It works.
3. If you want to be thorough, run a network monitor while it processes. There is no outbound traffic to send.

## What it does not do

Stated plainly, because you will find out anyway:

- **Windows only.** No macOS, no Linux.
- **No mobile apps.** Desktop only.
- **No real-time collaboration** and no calendar integrations. If your team needs shared live notes, a cloud tool fits better.
- Running models locally uses your CPU (or GPU) while it works. That is the trade for not uploading anything.

## Frequently asked

**Does a bot join my meeting?**
No. It captures the audio your own machine already plays and records, so there is nothing for other participants to see.

**Does it work behind a corporate firewall?**
Yes. It does not need outbound connections to transcribe, which is the usual reason cloud notetakers get blocked.

**Where are my recordings stored?**
On your machine, in your user data directory. Nothing is uploaded, so there is no server copy to delete.

**Is it free?**
The Demo is free with sessions up to 10 minutes, unlimited over time, and no account. Pro lifts the limit — pricing on [airgapscribe.com](https://airgapscribe.com).

**What languages?**
Transcription in English and Spanish. The interface is available in both.

---

## En español

AirGapScribe graba tus reuniones, las transcribe y prepara la minuta **sin enviar una sola palabra a internet**. Ningún bot entra a la llamada, no hay cuenta y no hay nube.

Todo el procesamiento ocurre en tu equipo con modelos de IA instalados localmente: Whisper para transcribir, en español o inglés, con vocabulario propio para los nombres y términos de tu trabajo. Funciona detrás de firewalls corporativos y sin conexión, que es justamente donde las herramientas en la nube dejan de servir.

Solo Windows. Sin apps móviles ni colaboración en tiempo real.

Este repositorio aloja únicamente los instaladores públicos de la versión Demo. El código fuente es privado.

Sitio oficial: [airgapscribe.com](https://airgapscribe.com)

---

Built by [Prototype Servicios Informáticos y Comercializadora E.I.R.L.](https://airgapscribe.com) · Bug reports and questions: [Issues](../../issues) or support@airgapscribe.com
