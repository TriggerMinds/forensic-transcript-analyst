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

## Vereisten & Docker Quickstart

Voor volledige functionaliteit en naleving van het brondiversificatieprotocol wordt aanbevolen om de bijgeleverde lokale Docker-infrastructuur te draaien:

- **SearxNG** (poort 8080) — meta-zoekmachine (geconfigureerd voor onafhankelijke indices).
- **Crawl4AI** (poort 11235) — scraping-service voor markdown-extractie.

### Quickstart

Start de services in de root-map van de repository:

```bash
# Start de containers in de achtergrond
docker compose up -d

# Controleer of alle containers actief zijn
docker compose ps

# Bekijk de logbestanden van de services
docker compose logs -f

# Stop de containers (met behoud van cache en instellingen)
docker compose stop
```

Zie [infrastructure/README.md](file:///c:/Users/gewoo/New%20folder%20(88)/infrastructure/README.md) voor meer geavanceerde beheerinstructies en probleemoplossing.

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
