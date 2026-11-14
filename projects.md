---
layout: default
title: Projects
permalink: /projects/
description: A few things I keep returning to — agents for reverse engineering, local inference, and the odd piece of hardware.
---
<section>
  <h1>Projects</h1>
  <p class="subtitle">A few things I keep returning to, running on hardware I own.</p>

  <h2 class="project-group">Agents for reverse engineering</h2>
  <p>Most of my recent work is a small fleet of agents that do mobile reverse engineering, driven by models running on my own network instead of an API. Each action is scored by risk, logged, and paused for my approval is the intent, and top of mind for research is agent sandboxing and model fine tuning.</p>

  <p class="project"><a href="https://github.com/EdibleTuber/PARE"><b>PARE</b></a> — Personal Agentic Reverse Engineer. A conversational operator for mobile RE: it answers from a curated research vault, runs static APK analysis, Frida instrumentation, and HTTPS interception, and routes every action through a dispatch layer that scores it by risk, pauses the risky ones for approval, and logs the call.</p>

  <p class="project"><a href="https://github.com/EdibleTuber/agent_core"><b>agent_core</b></a> — the shared spine under PARE and PAL: daemon runtime, socket protocol, model client, and an MCP tool layer with the same risk-gated dispatch and audit logging. New agents subclass it and implement a handful of handlers.</p>

  <p class="project"><a href="https://github.com/EdibleTuber/PAL"><b>PAL</b></a> — Personal Agentic Librarian. A terminal assistant over an Obsidian knowledge base that PARE reads from: it searches, edits, and organizes notes, and asks before fetching the web or publishing.</p>

  <p class="project"><b>PARE's MCP workers</b> — the hands: separate services for <a href="https://github.com/EdibleTuber/pare-mitm-mcp">mitm proxying</a>, <a href="https://github.com/EdibleTuber/pare-frida-mcp">Frida</a>, <a href="https://github.com/EdibleTuber/pare-static-mcp">static analysis</a>, and <a href="https://github.com/EdibleTuber/pare-hardware-mcp">hardware</a>, plus a <a href="https://github.com/EdibleTuber/pare-worker-kit">worker kit</a> for building more.</p>

  <p class="project"><a href="https://github.com/EdibleTuber/apk-re-agents"><b>apk-re-agents</b></a> — the predecessor that taught me the pattern: a multi-agent framework for APK reverse-engineering workflows that offloads routine steps to local models.</p>

  <h2 class="project-group">Running models locally</h2>

  <p class="project"><a href="https://github.com/EdibleTuber/inference-server"><b>inference-server</b></a> — a native llama.cpp server for Ubuntu that fronts several llama-server backends ("slots") behind one LAN endpoint, speaks both OpenAI- and Anthropic-compatible APIs, and routes each request to whichever slot has that model loaded. This is the box everything above talks to.</p>

  <h2 class="project-group">Hardware &amp; one-offs</h2>

  <p class="project"><a href="https://github.com/EdibleTuber/smart_rower_server"><b>smart_rower_server</b></a> — a FastAPI proxy for a connected rower, running on a Raspberry Pi, that lets it work offline and keeps workout history in SQLite. The subject of my first write-up.</p>

  <p class="project"><a href="https://github.com/EdibleTuber/DumpsterFire-Reflow-Hotplate"><b>DumpsterFire</b></a> — a low-cost reflow-soldering controller: a microcontroller, solid-state relay, OLED, and rotary encoder turn a hotplate into a programmable oven with preheat, soak, and reflow profiles.</p>
</section>
