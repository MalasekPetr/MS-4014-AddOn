# Konvence

Pravidla pro psaní materiálů. Cíl: konzistence a snadná údržba mezi běhy.

## Jazyk

- **Obsah**: čeština.
- **Názvy produktů a UI prvků**: anglicky, jak je student uvidí v UI (viz [`GLOSSARY.md`](GLOSSARY.md)).
- **Cesty a názvy souborů/složek**: angličtina, `kebab-case`.

## Struktura

Jeden blok = jedna složka se slugem. Pořadí drží [`agenda.md`](agenda.md). Každý `README.md` končí sekcemi `## Kontrolní otázky` a `## Stav produktu / delta`.

## Autorská práva

- Microsoft MCT materiály (PPTX, PDF, speaker notes, knowledge checks) **nekopírovat**. Složka `ms/` je v `.gitignore`.
- Z MS materiálů jen **parafrázovat a doplňovat**. Z článků nepřebírat delší citace — shrnout vlastními slovy a odkázat.

## Zákaznický kontext

Repo je veřejné. **Nikdy nejmenovat zákazníka** ani neuvádět nic, z čeho by šel identifikovat: název, obor, lokalita, tenant, licence, interní systémy, konkrétní prostředí.

- Povolené obecné označení: *velká organizace*, *mezinárodní korporátní organizace*.
- Příklady psát obecně, ne podle konkrétního zákazníka.
- Před každým commitem kontrola: `git grep -niE "<jména zákazníků>"` musí být prázdný.

## Currency-markery

```md
> [!WARNING] Ověřit k datu běhu — stav k <RRRR-MM>.
> <co se může změnit>
```

```md
> [!IMPORTANT] Slidy vs. realita
> <co říká slide> → <aktuální stav>.
```
