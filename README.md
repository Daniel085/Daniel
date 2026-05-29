# Daniel O'Rorke

**Product Manager | AI Systems Architect | Developer Tools**

I design and operate AI systems hands-on — multi-agent pipelines, agentic workflows, and developer tools that multiply team capability. 10+ years shipping API platforms and developer products; currently building with Claude and exploring what "AI-native" product management actually means in practice.

📍 Boise | 💼 [LinkedIn](https://linkedin.com/in/danielororke) | 📧 daniel@ororke.com

---

## Docs-as-Code — Agentic Engine for OpenAPI → Developer Portals

*Source is private — [architecture and case study available here](https://github.com/Daniel085/docs-as-code-case-study)*

A five-loop pipeline that turns a terse OpenAPI spec into a branded developer portal. The core bet: stop trying to fix the LLM — fix the inputs and outputs around it.

**The problem:** LLMs hallucinate when specs are silent. Point a model at an incomplete OpenAPI spec and it invents plausible-sounding sentences for missing fields, undocumented error codes, and unspecified defaults. A reference page that's 95% correct is unusable when you can't tell which 5% is wrong.

**The architecture:** Five event-triggered loops, each owning one transformation. Every LLM call is bracketed by deterministic steps — gap detection before, accuracy review after. Gaps surface as visible admonitions rather than invented prose. Regeneration is scoped to only the pages whose spec dependencies changed, so cost scales with what changed rather than spec size.

| | |
|---|---|
| **Agent roster** | 12 agents across 5 loops; Opus for judgement-critical roles, Sonnet for structured transformations |
| **Cost** | ~$0.65/op cold full run; ~$1.50 for a typical incremental spec change |
| **Tests** | 167 Python test functions, 25 Node tests, WCAG A/AA validated via Playwright + axe-core |
| **Key rule** | No product-specific logic in the engine — every per-product behaviour lives in three config files |

[Read the case study →](https://github.com/Daniel085/docs-as-code-case-study)

---

## Other Projects

### [SocialMediaManager](https://github.com/Daniel085/SocialMediaManager)
**Human-in-the-loop AI content review pipeline**

Click CLI frontend + Flask review UI for AI-generated social content. Uses claude-sonnet-4-6 to draft posts; a human reviews and approves before anything publishes. Built to explore where AI augments rather than replaces editorial judgement.

**Tech:** Python, Click, Flask, Claude claude-sonnet-4-6

---

### [dadJokeGenerator](https://github.com/Daniel085/dadJokeGenerator) — [Live Demo](https://daniel085.github.io/dadJokeGenerator/)
**Shipped in under an hour as a new-dad warm-up**

Dual-mode dad joke generator: live API (1000+ jokes) or local vault (750+), with session-tracked anti-repeat, keyboard shortcuts, and a garage/workshop theme. Vanilla JS, no frameworks.

**Tech:** Vanilla JS, HTML5, CSS3, icanhazdadjoke API | **Status:** ✅ Live

---

### [Family Meal Planner](https://github.com/Daniel085/new-project)
**Next.js 15 meal planner with pluggable LLM abstraction**

Generates personalised meal plans via a `LLMProvider` interface that switches cleanly between Claude and OpenAI. Puppeteer-driven Walmart cart automation adds ingredients automatically.

**Tech:** TypeScript, Next.js 15, Anthropic Claude API, Puppeteer

---

### [GrocerySelector](https://github.com/Daniel085/GrocerySelector)
**In-browser AI: Phi-3 + SDXL-Turbo via WebGPU**

Runs Phi-3 (language) and SDXL-Turbo (image generation) entirely in the browser over WebGPU — no server, no API key, no cloud. An exploration of what frontier on-device inference looks like today.

**Tech:** JavaScript, WebGPU, Phi-3, SDXL-Turbo

---

### [iOS-WebRTC-Demo](https://github.com/Daniel085/iOS-WebRTC-Demo)
**Production-ready native iOS dialer with 12-guide documentation suite**

Full CallKit integration (lock screen calls, CarPlay, Bluetooth), VoIP push notifications, contacts integration, and a complete backend architecture (signaling server, TURN/STUN, DB schema). Built to understand the full stack of a production calling app.

**Tech:** Swift 5.9+, SwiftUI, GoogleWebRTC, CallKit, PushKit, Node.js, Socket.io, PostgreSQL

---

### [SampleClickToCall](https://github.com/Daniel085/SampleClickToCall)
**SIP click-to-call with interface-driven design and real CI**

Interface-driven architecture with a `FakeSipClient` for deterministic testing — a deliberate proof-of-concept for engineering rigour habits applied to personal projects.

**Tech:** SIP, interface-driven testing, CI/CD

---

## Future Projects

### [Hearth](https://github.com/Daniel085/Hearth) — Privacy-First Relationship Assistant
*Design phase complete, moving to implementation*

iOS app for relationship management with all AI processing on-device via Core ML. No cloud, no data collection. Built around the idea that technology should support intentional connection rather than interrupt it.

**Tech:** Swift, SwiftUI, Core ML, Vision, PhotoKit, EventKit, Core Location

---

## Background

10+ years building developer tools and API platforms at Vonage (TokBox), SendGrid, VoiceBase, Aerohive Networks, and Charter Communications. Managed SDKs across iOS, Android, Web, Windows, Linux, and HoloLens. Deep background in WebRTC and real-time communications.

$3M revenue captured through API migration automation at Vonage · 60% reduction in integration time at VoiceBase · ISTE "Best in Show" for a WebRTC education app · 2 patents in WiFi credential automation (15/073,593 & 62/350,158)

---

## Contact

📧 daniel@ororke.com | 💼 [linkedin.com/in/danielororke](https://linkedin.com/in/danielororke)

---

*I don't just manage products — I build them.*
