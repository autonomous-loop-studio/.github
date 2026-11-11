# Autonomous Loop Studio

**A self-hosted AI agent console in plain PHP.** No Docker, no Node, no build step, no account.

![Autonomous Loop Studio — the wordmark over the live network map, the chat and the settings rails](https://raw.githubusercontent.com/autonomous-loop-studio/Autonomous/master/screenshots/banner.png)

Point it at any model — hosted, or running on a machine of your own — hand the agents real tools, and
watch the loop on a live map. It is one folder of PHP and static files, so it runs on the host you
already pay for.

**[The app](https://github.com/autonomous-loop-studio/Autonomous)** ·
**[Landing page](https://autonomous-loop-studio.github.io/Autonomous/)** ·
**[Roadmap](https://github.com/autonomous-loop-studio/Autonomous/discussions/1)** ·
**[Releases](https://github.com/autonomous-loop-studio/Autonomous/releases)**

## What's inside

- **🤖 Any model, any provider** — OpenAI, Anthropic, Google, OpenRouter, Groq, DeepSeek, xAI, Mistral, Cerebras, Together, Perplexity, NVIDIA NIM, or Ollama, LM Studio and vLLM on your own LAN.
- **🧭 An auto-fitting harness** — detects each provider's API shape and its tool dialect, speaks it correctly, and reads the reply back.
- **🔀 Routing chart** — draw workflows on the map: agents, loops, checkpoints, delays and parallel fan-out.
- **🛠️ Real tools, not toys** — files, shell, web, a code interpreter, git, editors and MCP, with timeouts that end the process instead of the turn.
- **🌐 A browser you both drive** — a real Chrome or Edge the agents can click and type in; you watch, and you can take over.
- **♾️ Loops that keep going** — Always-On re-prompts a standing goal on a cadence, with iteration and time caps, per-agent hold, and one master kill switch.
- **🧠 Brain Lab** — every per-agent setting in one rail: provider, model, locks, memory, files and custom tools.
- **🧪 API Lab** — paste a curl, get it in ten languages, then send it server-side for real.
- **🖥️ Two interfaces, one switch** — Classic or Desktop 2026, the same features over the same store.

<p align="center">
  <img src="https://raw.githubusercontent.com/autonomous-loop-studio/Autonomous/master/screenshots/Brain-Lab.png" width="49%" alt="Brain Lab: every provider on one bench, with the harness deciding how each agent calls it.">
  <img src="https://raw.githubusercontent.com/autonomous-loop-studio/Autonomous/master/screenshots/routing-three-workfows.png" width="49%" alt="A routing chart: three workflows handing work to the same fleet of agents.">
</p>

Apache-2.0. Free tiers are paced to each provider's ceiling, so one exhausted key never stops the fleet.
Issues and questions belong in [the repository](https://github.com/autonomous-loop-studio/Autonomous), not here.
