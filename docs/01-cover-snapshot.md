# 1. Cover & Snapshot

*Describes NordIQ in service language — not as a stack.*

## Varför

NordIQ finns för att ge medarbetare snabbare first-line-stöd utan onödig väntetid och utan att användaren själv behöver förstå intern routing.

## Beslut / Krav

- NordIQ ska vara en tjänst med tydligt värde för HR, IT Ops, Dev, CIO och CFO.
- Utility: omedelbar självbetjäning, intelligent triage och datadrivna förbättringar.
- Warranty: hög tillgänglighet, fungerande failover och korrekt information från Knowledge Base.
- Ansvarsgräns för AI-svar måste vara tydlig mellan IT Ops och Dev.

### Stakeholder risk- och kostnadsbalans

| Roll | Risk Removed | Risk Imposed | Cost Removed | Cost Imposed |
| :--- | :--- | :--- | :--- | :--- |
| Lina (HR) | Mindre väntetid vid onboarding | Felaktiga AI-svar kan ge fel accessflöde | Mindre manuell koordinering | Extraarbete vid felaktiga svar |
| Karl (Dev) | Mindre avbrott för enkla L1-frågor | Tekniskt ansvar när agenten svarar fel | Mindre ad hoc-support | Löpande arbete med kunskapsbas |
| Martin (CIO) | Lägre operativ och politisk risk vid lyckad leverans | Hög synlighet vid misslyckad lansering | Effektivare supportmodell | Beslutsrisk vid fel timing |
| Erik (CFO) | Mer förutsägbar supportkostnad | Rörlig API-kostnad kan öka snabbt | Lägre manuell first-line-kostnad | Ny löpande kostnad för tokens/hosting |
| Anna (IT Ops) | Lägre volym repetitiva ärenden | Felklassificering kan ge fel belastning | Mer tid för komplexa incidenter | Driftansvar för en tjänst hon inte byggt |

## Mätetal

| Mätområde | Målbild |
| :--- | :--- |
| Tjänstens värde | Minskat manuellt first-line-arbete och snabbare hjälp till användare |
| Riskkontroll | Definierade risker per roll med beslutad hantering |
| Informationskvalitet | Knowledge Base hålls aktuell för att minska felaktiga AI-svar |

## Ansvarig

- **Tjänsteägare/beslutsägare:** Martin (CIO)
- **Drift och eskalering:** Anna (IT Ops Lead)
- **Teknisk plattform:** Karl (Dev Lead)
- **Kostnad/leverantör:** Erik (CFO)
- **Användarperspektiv:** Lina (HR)

## Nästa steg

1. Fastställ ägarskap för AI-svar och eskalering.
2. Säkerställ att riskbilden i denna sida matchar SLO, incident- och change-sidorna.
3. Godkänn att denna sida används som gemensam tjänstebeskrivning inför go-live.

## Vidare läsning

- [2. Service Levels](./02-service-levels.md)
- [3. Operational Readiness](./03-operational-readiness.md)
- [4. Change & Release](./04-change-release.md)
