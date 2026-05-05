# VYBSTAK Builder v0.1

The Loop. Builder, Composition Graph, live Runtime preview, Claude-powered Prompt Mode.
Vanilla HTML / CSS / JS. Node and Express. Railway-ready.

> The Creator is the Asset. Not the Product.

---

## What this is

This is the foundational surface of the VYBSTAK Creator OS. A creator can:

* compose a social platform from primitives (Feed, Aesthetic, Interaction, Profile, Moderation)
* describe a platform in natural language and have Architect (Claude Opus 4.7) compose the DNA
* see the runtime preview update live as the Composition Graph changes
* export the canonical Platform DNA as JSON

This is Phase 1 of the architecture doctrine: *The Loop*. Marketplace, plugins, sovereignty, and AI Companions arrive in subsequent phases.

---

## Run locally

```bash
cd vybstak-builder
cp .env.example .env
# edit .env and set ANTHROPIC_API_KEY
npm install
npm start
```

Open `http://localhost:3000`.

---

## Deploy to Railway

```bash
railway init
railway variables set ANTHROPIC_API_KEY=sk-ant-...
railway up
```

Railway uses the `railway.json` config and the `start` script in `package.json`. `PORT` is provided automatically.

---

## File map

```
vybstak-builder/
├── server.js              Express + Claude proxy (claude-opus-4-7)
├── package.json
├── railway.json
├── .env.example
├── public/
│   ├── index.html         Builder shell (three panes)
│   ├── styles.css         Brutalist VYBSTAK visual system
│   └── app.js             DNA state, runtime renderer, gesture wheel
└── README.md
```

---

## What works in v0.1

**Composition Graph.** Five canonical widgets per platform: Feed, Aesthetic, Interaction, Profile, Moderation. Click any variant in the left palette to instantly mutate the DNA and re-render the runtime preview.

**Live Runtime preview.** Eight seeded posts re-rendered every state change. Feed engines visibly differ: Originality-First reorders by score, Slow Feed dims everything below the fold, Discovery shuffles deterministically by platform id, Debate surfaces variance.

**Aesthetics.** Six full atmospheres: Valencia Warm, Brutalist Minimal, Cinematic, Deep Focus, Calm Analog, Reactive Neon. Each shifts colour, motion timing, line weights, and accent.

**Gesture Wheel.** Pick `Interaction → Gesture Wheel`, then long-press any post. Eight radial actions (Respect, Original, Remix, Annotate, Voice, Save, Boost, Report).

**Prompt Mode.** Right-pane Prompt tab. Describe a platform; Architect composes the DNA. Example: *"a slow social platform for documentary photographers, no ads, originality-first feed, gesture-driven, warm analog atmosphere, invite-only"*.

**Architect Chat.** Quick questions about the current platform configuration. Same tab, below Prompt.

**Inspector.** Click any node in the Composition Graph (left, below palette) to edit its variant and atmosphere parameters.

**Export DNA.** Top-right button. Downloads the full Platform DNA as JSON.

---

## What does not work yet

* Persistence (the DNA lives only in browser memory until exported).
* Custom code mode (Code Mode is in the doctrine; not in v0.1).
* Plugin runtime, Marketplace, custom domains, PWA / native packaging, sovereignty deployment.
* Multi-user / multiplayer Builder.
* Real authentication or identity. The runtime preview is fully simulated.

These are roadmap items. v0.1 is the demo that proves the architecture is real.

---

## Architecture invariants

The DNA is canonical. Every visible change in the runtime is a deterministic function of the DNA. The Builder, the Inspector, and Prompt Mode all mutate the same single state object. Export captures it whole. Reload re-creates the platform identically.

This is the property that the doctrine demands and the rest of the roadmap depends on.

---

Powered by VYBSTAK. The future belongs to creators.
"# Vybstak-builder" 
