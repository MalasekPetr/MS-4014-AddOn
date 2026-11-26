# MS-4014 AddOn — AI agenti a novinky Microsoft Copilotu (česká vrstva)

Doplňkové studijní materiály ke kurzu **MS-4014: Introduction to building AI agents** v rozšířené 6hodinové verzi, která navíc pokrývá novinky Microsoft Copilotu po Ignite 2026. Vše v Markdownu, renderovatelné přímo na GitHubu.

> [!IMPORTANT] Co tohle repo je — a co není
> Oficiální obsah kurzu tvoří **Microsoft slidy + Microsoft Learn**. Tohle repo je **česká nadstavba**: výklad pro opakování a samostudium, aktuální stav produktů, přehled zdrojů a šablona pro návrh agenta. Oficiální MCT materiály (PPTX/PDF, knowledge checks) v repu **nejsou a nebudou** (licence MCT).

## Jak repo číst

- **Pořadí bloků** drží [`agenda.md`](agenda.md).
- **Názvosloví a přejmenování**: [`GLOSSARY.md`](GLOSSARY.md) — Microsoft v roce 2026 přejmenoval téměř vše.
- **Všechny zdroje na jednom místě**: [`SOURCES.md`](SOURCES.md).
- **Samostudium**: projděte složky v pořadí z agendy; každá končí kontrolními otázkami.
- **Konvence** psaní materiálů: [`CONVENTIONS.md`](CONVENTIONS.md).

## Struktura

```text
MS-4014-AddOn/
├─ README.md                # tento soubor
├─ agenda.md                # průběh dne
├─ GLOSSARY.md              # názvosloví a přejmenování
├─ SOURCES.md               # všechny zdroje (Microsoft, analýzy, standardy)
├─ CONVENTIONS.md           # jak psát materiály
├─ ai-market/               # Blok 1 — trh AI asistentů, vliv ChatGPT, Claude, Gemini
├─ copilot-news/            # Blok 2 — Home, Cowork, Code, Autopilot, Office in Copilot, náklady, správa
├─ cowork-extensibility/    # Blok 3 — plugins, skills, connectors (Cowork i Chat)
├─ projects-workspaces/     # Blok 4 — Projects a Copilot Workspaces
├─ ai-agents-intro/         # Blok 5 — co je AI agent (MS-4014 M1)
├─ agent-platform/          # Blok 6 — nástroje, kanály, Microsoft IQ, MCP, A2A (MS-4014 M2)
├─ agent-governance/        # Blok 7 — identita, Agent 365, governance (MS-4014 M2 U5, M3 U4)
├─ plan-agent-solution/     # Blok 8 — plánování agenta + workshop šablona (MS-4014 M3)
└─ review/                  # opakovací otázky a další kroky
```

Každá složka obsahuje `README.md` s výkladem pro studenty. Lektorské poznámky jsou v `instructor-notes.md` tam, kde dávají smysl.

## Legenda

- `> [!WARNING] Ověřit k datu běhu` — rychle se měnící fakt (dostupnost, licence, preview/GA).
- `> [!IMPORTANT]` — přejmenování nebo místo, kde se oficiální slidy **rozcházejí** s aktuálním stavem.
- `> [!TIP]` — praktická rada lektora navíc.

## Oficiální zdroje (Microsoft)

- Kurz: [MS-4014 na Microsoft Learn](https://learn.microsoft.com/en-us/training/courses/ms-4014)
- Copilot Cowork: [What's new in Copilot Cowork](https://learn.microsoft.com/en-us/copilot/cowork/whats-new)
- Ignite 2026: [Book of News](https://news.microsoft.com/events/ignite/2026/book-of-news/)

Související repo: [MS-4019-AddOn](https://github.com/MalasekPetr/MS-4019-AddOn) (deklarativní agenti v Agent Builderu a SharePointu).

## Stav

Obsah pro běh **2026-11-26**. Vychází z MS-4014 verze **October 2026** (Change Log / TPG, release 30. 10. 2026), z oznámení **Microsoft Ignite 2026** (17.–20. 11. 2026) a ze stavu produktů k **2026-11-26**.
