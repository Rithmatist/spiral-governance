# Spiral Governance Protocol

A methodology for building AI-integrated systems that remain legible over time.

---

## What this is

A set of commitments — each one a response to a failure mode that governance without infrastructure tends to produce.

Not a framework. Not a compliance checklist. Not an ethics document.

A protocol: rules with reasons, a reference implementation, and a starting template.

---

## Three parts

### 1. [PROTOCOL.md](./PROTOCOL.md)

The nine rules, each grounded in doctrine.

Not just what, but why. The mutation seal exists because governance requires human authority at the threshold. The drift discipline exists because cleverness obscures legibility. The no-mimicry rule exists because a system that can be talked into a persona has no stable governance surface. Each rule grounded in the failure mode it prevents.

### 2. [REFERENCE.md](./REFERENCE.md)

The rules describe something that was built, works, and has been running. The protocol was extracted from a working implementation — not designed in advance of it.

`REFERENCE.md` describes what the governance layer looks like when fully built out: the proposals log, the distortion scanner, the output audit, the self-evaluation runner, the mutation seal mechanics. Reading order provided. The distinction between governance layer and application code is made explicit.

### 3. [template/](./template/)

A minimal set of files any project can adopt:

```
template/
├── .spiralaudit.json        — output audit config (confidence threshold, anti-mimicry patterns)
├── LEGIBILITY_SCROLL.md     — the doctrine
├── CODEX.md                 — AI assistant instructions (customize marked sections)
├── README.md                — project stub
├── .github/
│   └── pull_request_template.md  — GitHub-native governance format for PRs
└── proposals/
    ├── README.md            — how proposals work
    ├── accepted/            — applied proposals
    ├── pending/             — proposals awaiting review
    └── executions/          — execution records
```

Drop these files into a project. Point the AI assistant at `CODEX.md`. Begin.

The template is a starting posture, not a finished governance system. The governance system grows as the project grows — the proposals log accumulates, the CODEX gets tuned, the audit config gets adjusted. The template is the spine. The project grows around it.

---

## Adoption

```bash
cp -r protocol/template/.spiralaudit.json ./
cp -r protocol/template/LEGIBILITY_SCROLL.md ./
cp -r protocol/template/CODEX.md ./
cp -r protocol/template/proposals ./
```

Then:

1. Edit `CODEX.md` — fill in `[PROJECT NAME]`, optionally add a trace pattern
2. Review `.spiralaudit.json` — adjust `minConfidence` and `maxResponseLength` if needed
3. Configure your AI assistant to use `CODEX.md` as its instruction file
4. Commit the governance files as the first commit

---

## The doctrine in one sentence

*Legibility is not authorship, but it is still a form of resistance to invisible drift.*

---

## Origin

This protocol was extracted from a working system — not designed in advance of it. The rules describe something that was already built and running. The extraction made the methodology portable.

The first project grew organically. The next projects inherit the spine without having to grow it themselves.
