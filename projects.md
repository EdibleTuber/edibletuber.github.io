---
layout: default
title: Projects
permalink: /projects/
description: Agents for reverse engineering, local inference, and the odd piece of hardware — running on hardware I own.
---
<section>
  <h1>Projects</h1>
  <p class="subtitle">Agents for reverse engineering, local inference, and the odd piece of hardware.</p>

  <h2 class="project-group">Agents for reverse engineering</h2>

  <p>Most of my recent work is a small fleet of agents that do reverse engineering and research, driven by models running on my own network instead of a hosted API. Every action is scored by risk, logged, and gated for my approval. The guiding constraint: an agent examining untrusted targets should never need to phone out, and a small local model can do this work if the architecture holds the line.</p>

  <p class="project"><a href="https://github.com/EdibleTuber/PARE"><b>PARE</b></a> — Personal Agentic Reverse Engineer. The flagship. A conversational RE operator: it augments its reasoning with a curated research vault, extends itself through MCP worker services, and routes every action through a dispatch layer that scores it by risk, pauses the risky ones for operator approval, and logs the call. Its context economy is built for real RE output — large captures are stored, stubbed, and searched by reference instead of pasted into the conversation.</p>

  <p class="project"><a href="https://github.com/EdibleTuber/PAL"><b>PAL</b></a> — Personal Agentic Librarian. Curates the Obsidian knowledge base other agents read from: it searches, edits, and organizes notes, and asks before fetching the web or publishing. CLI and Discord front ends; Discord is my preference because every channel keeps its own scratchpad and context.</p>

  <p class="project"><a href="https://github.com/EdibleTuber/agent_core"><b>agent_core</b></a> — the shared runtime under PARE and PAL, so no agent starts from scratch: daemon lifecycle, socket protocol, model client, and an MCP tool layer with the same risk-gated dispatch and audit logging. New agents subclass it and implement a handful of handlers.</p>

  <p class="project"><b>PARE's MCP workers</b> — the hands. Separate services for <a href="https://github.com/EdibleTuber/pare-mitm-mcp">mitm proxying</a>, <a href="https://github.com/EdibleTuber/pare-frida-mcp">Frida</a>, <a href="https://github.com/EdibleTuber/pare-static-mcp">static analysis</a>, and <a href="https://github.com/EdibleTuber/pare-hardware-mcp">hardware</a>, plus a <a href="https://github.com/EdibleTuber/pare-worker-kit">worker kit</a> for building more.</p>

  <p class="project"><a href="https://github.com/EdibleTuber/apk-re-agents"><b>apk-re-agents</b></a> — my first RE workflow attempt: a multi-tool framework for APK reverse-engineering that offloads routine steps to local models. Mostly mechanical, deterministic static RE.</p>

  <h2 class="project-group">Running models locally</h2>

  <p class="project"><a href="https://github.com/EdibleTuber/inference-server"><b>inference-server</b></a> — a native llama.cpp server for Ubuntu that fronts several llama-server backends ("slots") behind one LAN endpoint, speaks both OpenAI- and Anthropic-compatible APIs, and routes each request to whichever slot has that model loaded. A self-hosting labor of love.</p>

  <h2 class="project-group">Hardware &amp; one-offs</h2>

  <p class="project"><a href="https://github.com/EdibleTuber/smart_rower_server"><b>smart_rower_server</b></a> — a mitmdump-based proxy for a connected rower, running on a Raspberry Pi, that lets it work offline and keeps workout history in SQLite. The subject of my BSides PDX talk, <a href="https://www.youtube.com/watch?v=7MVtut1qZEQ"><b>Rudder Nonsense: Steering Smart Rowers Off Course</b></a>.</p>

  <p class="project"><a href="https://github.com/EdibleTuber/DumpsterFire-Reflow-Hotplate"><b>DumpsterFire</b></a> — a low-cost reflow-soldering controller: a microcontroller, solid-state relay, OLED, and rotary encoder turn a hotplate into a programmable oven with preheat, soak, and reflow profiles.</p>
</section>
