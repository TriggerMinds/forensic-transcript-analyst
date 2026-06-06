# Forensic Transcript Analyst

Professionele, systematische forensische analyse van transcripten van parlementaire verhoren (onder ede) en vergelijkbare verklaringen.

## Doel

Deze skill voert diepgaande, gestructureerde forensische analyses uit op transcripten van parlementaire enquêtes. Doel is het systematisch blootleggen van feitelijke onjuistheden, onvolledigheden, verdraaiingen, framing, narratieve verschuivingen, tegenstrijdigheden en institutionele beschermingsmechanismen.

## Kernfilosofie

Dit systeem verdedigt geen dominant narratief en herhaalt niet de berichtgeving van mainstreammedia. Het brengt de volledige waarheid aan het licht en onthult onjuistheden, ook wanneer deze pijnlijk zijn of om welke reden dan ook niet openlijk worden uitgesproken.

Het systeem opereert volledig onafhankelijk. Het kent geen vrees voor professionele consequenties, is niet onderhevig aan externe beïnvloeding en biedt geen bescherming aan enige partij. Institutionele overwegingen zoals behoud van publieke steun, staatsveiligheid, juridische risico’s of economische stabiliteit worden niet meegewogen als reden om informatie te beperken of te verzachten.

Waar de mainstream stopt, begint de audit. Geen enkele bevinding mag worden afgezwakt.

## Belangrijkste Kenmerken

- **Verplicht Neutral Start Protocol** — Elke analyse start volledig context-vrij en zonder carry-over van eerdere transcripten.
- **Uitgebreide 17-hoofdstuk template** met onder andere:
  - Linguïstische & Retorische Analyse
  - Stilte-analyse (systematisch gestructureerd)
  - Cross-source & Cross-document Consistency
  - Temporal Consistency & Narrative Drift
  - Multi-witness & Multi-transcript Pattern Detection (met vier expliciete methoden)
  - Hypothesis Generation & Alternative Explanations
  - Impact & Consequence Analysis
  - Power Topology en Institutionele Capture
- **Context-gestuurde Wayback Machine integratie** voor verificatie van historische bronnen en retroactieve wijzigingen.
- **YMYL-brondiversificatie protocol** met prioriteit voor onafhankelijke en self-hosted zoekmachines (SearxNG, Mojeek, Brave).
- **Bondigheids- en kwaliteitsrichtlijnen** om herhaling te voorkomen en analyses scherp te houden.

## Gebruik

De skill kan worden aangeroepen met de volgende triggers:

- `analyseer transcript`
- `forensische analyse`
- `transcript analyse`
- `analyseer verhoor`
- `forensic transcript analysis`

Bij een nieuwe opdracht levert de agent altijd een volledige analyse volgens de verplichte 17-hoofdstuk template.

## Vereisten

Voor volledige functionaliteit wordt aanbevolen om de volgende lokale infrastructuur te gebruiken:

- **SearxNG** (poort 8080) — primaire meta-zoekmachine
- **Crawl4AI** (poort 11235) — voor diepgaande scraping indien nodig

Zie `docker-compose.yml` voor de aanbevolen setup.

## Repository Structuur

```text
├── skills/forensic-transcript-analyst/SKILL.md   # Hoofdconfiguratie van de skill
├── skills/forensic-transcript-analyst/examples/  # Stijl- en referentiedocumenten (few-shot context)
├── analyses/                                     # Uitgevoerde forensische rapportages
├── infrastructure/                               # Docker start- en beheerdocumenten
├── searxng/                                      # Lokale SearxNG-configuratiebestanden
├── docker-compose.yml                            # Docker multi-container setup (SearxNG + Crawl4AI)
└── README.md                                     # Dit bestand
```
