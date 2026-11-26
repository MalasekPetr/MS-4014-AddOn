# Blok 6 · Microsoftí platforma pro agenty

> Typ: výklad · Odhad: 30 min · Zdroj: MS-4014 Modul 2 — *Choose tools and services for your agent on Microsoft's agent platform* (unity 1–4)

## Cíle

- Vyberete **přístup ke stavbě** agenta: Agent Builder, Copilot Studio, Microsoft Foundry.
- Znáte **kanály**, kterými se agent dostane k uživatelům.
- Přiřadíte data ke správné službě **Microsoft IQ**.
- Víte, k čemu slouží **MCP** a **A2A**.

## Vrstvy vývoje agenta

Každý agent má pět vrstev: **platforma** (stavba, hosting, publikace) · **model** · **orchestrace** · **kanál** · **AI-assisted development**. Čím méně kódu, tím víc vrstev řeší platforma za vás.

## Tři přístupy

| | Agent Builder | Copilot Studio | Microsoft Foundry |
|---|---|---|---|
| Přístup | no-code, v Microsoft Copilot | low-code (+ pro-code rozšíření) | pro-code (i low-code) |
| Pro koho | jednotlivci, malé týmy | makeři, business, vývojáři | vývojářské týmy |
| Typický scénář | rychlý agent v toku práce | oddělení, provozní procesy | produkční AI systémy |
| Vrstvy | vše řeší platforma | většinu řeší platforma | každá vrstva je vaše volba |

Přístupy se **nevylučují** — firmy je kombinují.

### Pro-code stack (Foundry)

| Vrstva | Možnosti |
|---|---|
| Platforma | **Foundry Agent Service** — *prompt agents* (konfigurace) nebo *hosted agents* (vlastní kód) |
| Model | **Foundry model catalog** — modely Microsoftu a dalších poskytovatelů |
| Orchestrace | **Microsoft Agent Framework** (doporučeno), Semantic Kernel (jen existující aplikace), jiné frameworky |
| Kanál | **Microsoft 365 Agents SDK**, **Teams SDK**, přímé API přes **agent endpoint** |
| Nástroje | Visual Studio / VS Code, Foundry Toolkit, Microsoft 365 Agents Toolkit, GitHub Copilot |

## Kanály

| Kanál | Pro koho | Governance |
|---|---|---|
| **Microsoft Copilot, Teams** | interní uživatelé Microsoft 365 | zděděno (DLP, retence, audit, Copilot Control System) |
| **SharePoint** | agent na webu | respektuje oprávnění SharePointu |
| **Voice** | hlasová interakce | jako ostatní + práce s hlasovými daty |
| **Vlastní aplikace, web** | externí uživatelé, lidé bez licence | **na vývojáři** |
| **Messaging (Azure Bot Service)** | kanály třetích stran | **na vývojáři** |
| **A2A** | volají ho jiní agenti | Entra ID, bez anonymního přístupu |

- **Copilot Studio:** kanál → rozsah (já / skupiny / organizace) → schválení v Microsoft 365 admin center.
- **Foundry:** každý agent má stabilní **agent endpoint** s Entra identitou; publikace do Copilotu a Teams, nebo přímé API.

## Grounding: Microsoft IQ

Služby IQ řeší indexaci, aktuálnost, napojení zdrojů a hlavně **přístupová práva** — uživatel uvidí jen to, co smí vidět ve zdroji.

| Data | Příklady | Služba |
|---|---|---|
| Obsah Microsoft 365 | e-maily, Teams, soubory, kalendář | **Work IQ** |
| Firemní dokumenty | manuály, směrnice, knowledge base | **Foundry IQ** |
| Strukturovaná a provozní data | záznamy, OneLake, metriky | **Fabric IQ** |
| Externí web | aktuální informace mimo firmu | **Web IQ** |

Jeden agent může kombinovat více služeb. Microsoft IQ byl na Ignite 2026 prezentován jako GA vrstva firemního kontextu.

> [!IMPORTANT] On-premises obsah
> Work IQ pracuje nad obsahem v Microsoft 365. Obsah v on-premises systémech (např. SharePoint Server) potřebuje **Copilot connector** nebo migraci.

## Akce a integrace

- **MCP** je hlavní otevřený standard pro napojení agentů na nástroje; služby Microsoft IQ ho nabízejí jako rozhraní.
- **Copilot Studio** — pět vzorů: Power Platform connectory, **workflows**, MCP servery, REST API akce (preview), Computer Use.
- **Pro-code** — Azure Logic Apps, Azure Functions, OpenAPI nástroje, Computer Use.
- **Více agentů:** uvnitř Microsoftu nativní propojení (Copilot Studio → Foundry agent je preview; Foundry → Foundry přes Agent Framework workflows). Napříč platformami **A2A** (otevřený standard pod Linux Foundation).

> [!TIP] Doporučení Microsoftu
> Interní toky orchestrujte nativně; **A2A** použijte pro propojení napříč platformami, frameworky nebo tenanty.

## Kontrolní otázky

1. Tým potřebuje zákaznického agenta s vlastní orchestrací a volbou modelu. Který přístup zvolí?
2. Agent má odpovídat z produktových manuálů a směrnic. Která služba IQ?
3. Který kanál dědí Microsoft 365 compliance automaticky a který ne?
4. Kdy použít MCP a kdy A2A?

## Stav produktu / delta

> [!WARNING] Ověřit k datu běhu — stav k 2026-10 (MS-4014 release 30. 10. 2026).
> Preview: Copilot Studio → Foundry agent, REST API akce v Copilot Studiu. Status jednotlivých služeb Microsoft IQ ověřit.
