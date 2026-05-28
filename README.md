# Moe Eldouma

**AI Engineer | Open-Source Contributor**

Building AI agentic workflows, training and fine-tuning agents.

---

## Open-Source Contributions

### Critical Data-Loss Bug Fix in Hermes Agent (Nous Research)

Discovered, diagnosed, and proposed the fix for a **P1 critical data-loss vulnerability** in [Hermes Agent](https://github.com/NousResearch/hermes-agent) — Nous Research's open-source autonomous agent framework.

**The Bug:** The Kanban task system's scratch workspace cleanup (`shutil.rmtree`) could silently and permanently delete a user's entire projects directory when a board's `default_workdir` pointed to a real working directory. No confirmation, no warning, no recovery.

**What I Did:**
- Traced the root cause through system logs and bash history to the exact function (`_cleanup_workspace()` in `kanban_db.py`) and the exact timestamp of the `kanban_complete` call
- Filed a detailed bug report with full reproduction steps, root cause analysis, and three concrete fix proposals
- Applied a local protected-path guard patch immediately to prevent further damage

**The Outcome:**
- All three of my suggested fixes were adopted upstream almost exactly as proposed
- The maintainers implemented a **3-layer defense-in-depth** solution across multiple PRs
- Recognized by Nous Research with primary credit for "the most actionable diagnosis"
- The fix is now live on main, protecting all Hermes users

> *"The diagnosis from @MoeEldouma was on target... primary bug report with the most actionable diagnosis — correct identification of `_cleanup_workspace()` as the deletion site, full trace from `kanban_complete` to `rmtree`, and the three concrete suggested fixes that match what landed almost exactly."*
> — **teknium**, Nous Research

[View the full issue and resolution](https://github.com/NousResearch/hermes-agent/issues/30151)

---

## Projects

### [Arabic TTS](https://github.com/MoeEldouma/arabic-tts)
Improving XTTS-v2 for natural Arabic speech synthesis with multi-dialect support.

### Eldouma Studio
AI video generation platform combining LLM-driven scripting, text-to-speech, and video synthesis into an end-to-end production pipeline.

---

## Tech Stack

`Python` `PyTorch` `LLMs` `Diffusion Models` `TTS/STT` `ComfyUI` `Agent Frameworks` `Linux`

---

<p align="center">
  <a href="mailto:eldoumamoe@gmail.com">Email</a>
</p>
