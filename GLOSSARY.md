# Glosář — názvosloví a přejmenování

Jediný zdroj pravdy pro názvy. Ve slidech, na Learnu, v článcích a v UI se můžete setkat s různými názvy pro tutéž věc.

> [!WARNING] Ověřit k datu běhu — stav k 2026-11.

## Základní pojmy

| Pojem (UI / EN) | Česky | Význam |
|---|---|---|
| **Microsoft Copilot** | — | Aplikace Copilot pro práci (dříve *Microsoft 365 Copilot app*). Licence se dál jmenuje **Microsoft 365 Copilot**. |
| **Copilot Home** | domovská stránka | Jedno místo, kde se potkává Chat a Cowork. |
| **Copilot Chat** | — | Konverzace s Copilotem: otázka → odpověď. |
| **Copilot Cowork** | — | Delegování dlouho běžících vícekrokových úkolů napříč Microsoft 365. Postaveno na technologii Claude Cowork (Anthropic). |
| **Copilot Code** | — | Tvorba aplikací z přirozeného jazyka; aplikace hostuje Copilot Managed Runtime. |
| **Autopilot** | — | Trvalý, proaktivní agent s vlastní identitou. |
| **Office in Copilot** | — | Word, Excel a PowerPoint editované přímo vedle chatu v aplikaci Copilot. |
| **Copilot Workspaces** | pracovní prostory | Sdílený prostor týmu a agentů se společným kontextem; nástupce Copilot Notebooks. |
| **Projects** | projekty | Úkoly, instrukce a kontext pohromadě (osobní). |
| **Skill** | dovednost | Uložené instrukce pro opakovaný úkol (soubor `SKILL.md`). |
| **Connector** | konektor | Napojení na externí systém nebo data (MCP, Power Platform, Copilot connectors). |
| **Plugin** | — | Balíček (Microsoft 365 app package) obsahující skills a/nebo connectors. |
| **Copilot Credits** | kredity | Jednotka spotřebního účtování (Cowork, Copilot Studio agenti, Today Feed aj.). |
| **Copilot Managed Runtime** | — | Hosting a governance aplikací z Code, Cowork, Copilot Studia a kompatibilních nástrojů. |
| **AI agent** | agent | Program, který s pomocí AI automatizuje a vykonává business procesy vedle člověka nebo za něj. |
| **Declarative agent** | deklarativní agent | Agent definovaný konfigurací (instrukce, znalosti, akce), běží na modelu a orchestrátoru Copilotu. |
| **Custom engine agent** | agent s vlastním enginem | Agent s vlastním modelem a orchestrací (Foundry, Agents SDK). |
| **Agent Builder** | — | No-code tvorba agentů v Microsoft Copilot. |
| **Copilot Studio** | — | Low-code platforma pro agenty (s pro-code rozšířeními). |
| **Microsoft Foundry** | — | Pro-code platforma pro AI aplikace a agenty v Azure. |
| **Microsoft IQ** | — | Rodina služeb pro grounding: Work IQ, Foundry IQ, Fabric IQ, Web IQ. |
| **MCP** | Model Context Protocol | Otevřený standard pro napojení agentů na nástroje a data. |
| **A2A** | Agent-to-Agent protocol | Otevřený standard pro komunikaci agentů napříč frameworky a platformami. |
| **Microsoft Entra Agent ID** | identita agenta | Identita pro každého agenta v Entra ID. |
| **Agent identity blueprint** | šablona identity | Opakovaně použitelná šablona oprávnění a sponzorství pro agenty stejného typu. |
| **Microsoft Agent 365** | — | Control plane pro agenty: registr, vlastnictví, lifecycle, bezpečnost, náklady. |
| **Copilot Control System** | — | Správa Copilotu a agentů v Microsoft 365 admin center (mj. schvalování agentů). |
| **Frontier** | — | Program předběžného přístupu Microsoftu. Funkce „ve Frontier“ **nejsou GA**. |

## Přejmenování (co v materiálech potkáte)

| Od | Starší název | Aktuální název |
|---|---|---|
| 11/2026 | Copilot Notebooks | **Copilot Workspaces** |
| 10/2026 | Microsoft 365 Copilot app | **Microsoft Copilot** |
| 10/2026 | Agent flows, Power Automate flows v Copilot Studiu | **Workflows** |
| 10/2026 | AI Toolkit for VS Code | **Foundry Toolkit** |
| 10/2026 | Foundry „Agent Application“ | **Foundry agent endpoint** |
| 7/2026 | Graph connectors | **Copilot connectors** |
| 7/2026 | Teams Toolkit | **Microsoft 365 Agents Toolkit** |
| 11/2025 | Azure AI Foundry, Azure AI Agent Service | **Microsoft Foundry, Foundry Agent Service** |
| 11/2025 | Teams AI Library | **Teams SDK** |
| 11/2025 | Semantic Kernel + AutoGen | **Microsoft Agent Framework** (Semantic Kernel jen pro existující aplikace) |
| 11/2025 | Agent Builder ↔ „lite version of Copilot Studio“ | Aktuální MS-4014 deck opět používá **Agent Builder** |
| 1/2025 | BizChat, Business Chat | **Copilot Chat** |

> [!IMPORTANT] Slidy vs. realita
> Starší verze MS-4014 (2025) stavěly kurz na volbě „extend Copilot vs. build custom agent“ ve 4 modulech. Od 7/2026 má kurz **3 moduly** a důraz je na **plánování agentního řešení** a governance.
