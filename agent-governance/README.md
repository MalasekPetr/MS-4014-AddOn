# Blok 7 · Identita a governance agentů

> Typ: výklad + demo · Odhad: 25 min · Zdroj: MS-4014 Modul 2 Unit 5 a Modul 3 Unit 4, Microsoft Agent 365

## Cíle

- Víte, proč má každý agent **identitu, vlastníka a sponzora**.
- Znáte roli **Microsoft Agent 365**.
- Rozlišíte, kde se governance **dědí** a kde ji musí nastavit tým.
- Zvolíte **identitní model** a umístíte **guardrails**.

## Identita agenta

- **Microsoft Entra Agent ID** (GA) dává identitu každému agentovi; u Copilot Studia a Foundry automaticky při vytvoření.
- **Agent identity blueprint** — šablona pro agenty stejného typu: oprávnění, metadata, model přihlašovacích údajů, **sponsor (povinný)** a owner (volitelný). Agent sám nemá vlastní tajemství — drží je blueprint.
- **Least privilege** — jen oprávnění, která agent opravdu potřebuje; platforma některé vysoce privilegované role pro agenty blokuje.

| Vzor | Identita | Příklad |
|---|---|---|
| **Interaktivní** | delegovaná oprávnění přihlášeného uživatele | agent v konverzaci s uživatelem |
| **Autonomní** | vlastní identita, aplikační oprávnění se souhlasem admina | plánovaný agent, A2A specialista |
| **Autonomní + agent's user account** | navíc uživatelský objekt | odesílání ze sdílené schránky, plánování schůzek |

## Microsoft Agent 365

**Control plane** pro agenty Microsoftu i třetích stran. GA od 1. 5. 2026, 15 USD za uživatele měsíčně, součást Microsoft 365 E7 ([AMA](https://techcommunity.microsoft.com/event/microsoft365-events/live-ama-microsoft-agent-365/4499549/comments/4503539)). Od spuštění v něm firmy zaregistrovaly přes 50 milionů agentů ([Agent 365 blog](https://techcommunity.microsoft.com/blog/agent-365-blog/whats-new-in-microsoft-agent-365-ignite-2026/4571753)).

- **Discovery** — všichni agenti v jednom registru.
- **Accountability** — owner a sponsor u každého agenta.
- **Lifecycle** — schvalování, lifecycle workflows v Entra.
- **Security & compliance** — Defender, Intune, Purview, Entra.
- **Náklady (Ignite 2026)** — Cost Management (preview): limity, politiky, alerty; Business Analytics (Frontier): útraty, adopce, výsledky.

## Dědičnost governance

| Platforma | Co dostanete automaticky | Co musí nastavit tým |
|---|---|---|
| **Microsoft Copilot** | compliance a DLP Microsoft 365, retence, audit, rozsah tenantu | — |
| **Copilot Studio** | Power Platform data policies (DLP); Microsoft 365 kontroly v Teams/Copilot kanálech | ostatní kanály podle typu |
| **Microsoft Foundry** | — | Azure RBAC, politiky, logování a audit |

> [!IMPORTANT] Agent 365 práci neodebírá
> Agent 365 sjednotí pohled, ale u Foundry agentů zůstává konfigurace governance na týmu.

## Guardrails

| Místo zásahu | Riziko | Největší expozice |
|---|---|---|
| **Vstup uživatele** | jailbreak | externí kanály, veřejné portály |
| **Volání nástroje** | prompt injection v argumentech | agent zapisuje do systémů, posílá zprávy |
| **Odpověď nástroje** | nepřímá prompt injection v dokumentech | agent čte znalostní báze, web |
| **Výstup** | škodlivý obsah, osobní údaje | všichni, nejvíc externí agenti |

## Lifecycle

- **Conditional Access** pro identity agentů (podmínka rizika agenta je preview).
- **Access reviews** — sponzor pravidelně potvrzuje oprávnění.
- **Deprovisioning triggery** — konec use case, změna týmu, výkon pod cílovými metrikami. Agent bez nich se nevyřadí, jen se na něj zapomene.

## Data a modely

> [!IMPORTANT] EU Data Boundary
> Modely Anthropic v Copilotu, Researcheru a Copilot Studiu jsou podle Microsoftu aktuálně **mimo EU Data Boundary** ([Microsoft](https://www.microsoft.com/en-us/copilot/resources/compete-copilot-vs-claude-enterprise)). Rozhodnutí o jejich povolení patří adminovi a compliance týmu.

## Kontrolní otázky

1. Proč je u blueprintu povinný sponsor?
2. Agent běží bez uživatele a posílá e-maily ze sdílené schránky. Jaký identitní model potřebuje?
3. Proč má Foundry agent „od výroby“ méně governance než Copilot Studio agent?
4. Agent předává výňatky z dokumentů jinému agentovi a v dokumentech jsou skryté instrukce. Kam patří kontrola?
5. Jaké tři oblasti nákladů a hodnoty řeší Agent 365 od Ignite 2026?

## Stav produktu / delta

> [!WARNING] Ověřit k datu běhu — stav k 2026-11.
> Agent 365 Cost Management preview, Business Analytics Frontier, agent-risk Conditional Access preview.
