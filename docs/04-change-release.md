# 4. Change & Release

*The plan to take NordIQ into production — and back out.*

## Varför

Change & Release beskriver hur NordIQ går till produktion på ett kontrollerat sätt, med tydlig authority, observerbara kriterier och säker rollback.

## Beslut / Krav

- Martin Lindqvist (CIO) är formell Change Authority för go/no-go.
- CAB ska ge komplett beslutsunderlag från drift, teknik, kostnad och användarperspektiv.
- Go/no-go-kriterier måste vara uppfyllda innan release passerar.
- RFC ska innehålla syfte, scope, risk, tidsfönster, kommunikation, rollback och approvers.
- Rollback ska kunna aktiveras direkt vid definierade triggers.

### CAB-perspektiv (varför varje roll behövs)

- **Anna (IT Ops Lead):** Säkerställer att tjänsten är driftbar och hanterbar efter go-live.
- **Karl (Dev Lead):** Säkerställer realistisk teknisk riskbild, begränsningar och åtgärdsförmåga.
- **Erik (CFO):** Säkerställer kontroll på leverantörs- och kostnadsrisker.
- **Lina (HR):** Säkerställer användarvärde, adoption och att tjänsten fungerar i praktiken.

### Go / No-Go-kriterier (observerbara)

- Plan för kvarstående mindre fel (P2/P3) är godkänd av IT Ops.
- Mindre än 5 % av test-promptar returnerar felmeddelande.
- Health checks är gröna i 24 sammanhängande timmar.
- Skriftligt godkännande finns från samtliga i CAB.
- Acceptanskriterier för normalflöden är godkända i kvalitetssäkrad miljö.

### RFC-mall (minimum)

1. Purpose
2. Scope
3. Technical Change Description
4. Risk Assessment
5. Rollback Plan
6. Timeline and Window
7. Communication Plan
8. Approver List

```mermaid
flowchart TD
    A["Go / No-Go Criteria"] --> B{"Kriterier uppnådda?"}
    B -->|Ja| C["Skriftligt godkännande från samtliga i CAB"]
    B -->|Nej| D["Tjänsten får inte passera"]
    E["Rollback trigger"] --> F["Martin godkänner beslut om rollback"]
    F --> G["NordIQ tas offline"]
    G --> H["Ärenden omdirigeras till SharePoint FAQ och befintligt ticketing-system"]
    H --> I["Anna och IT-teamet återtar full manuell first-line-hantering"]
    I --> J["Lina och samtliga medarbetare meddelas via e-post"]
```

## Mätetal

| Mätområde | Mål |
| :--- | :--- |
| Go-live readiness | Samtliga kriterier uppfyllda och godkända |
| Health checks | Gröna i 24 sammanhängande timmar |
| Testkvalitet | < 5 % felmeddelanden i test-promptar |
| Rollback-beredskap | Triggerlista och steg verifierade |

## Ansvarig

- **Change Authority:** Martin Lindqvist (CIO)
- **Operativ releaseberedskap:** Anna (IT Ops Lead)
- **Teknisk risk/åtgärd:** Karl (Dev Lead)
- **Leverantör/kostnadsrisk:** Erik (CFO)
- **Användarpåverkan/användaracceptanstest:** Lina (HR)

## Nästa steg

1. Bekräfta att alla CAB-medlemmar godkänner kriterier och roller.
2. Kör go/no-go-gateway med dokumenterat beslutsunderlag.
3. Genomför rollback-övning innan produktionsdatum.

## Vidare läsning

- [1. Cover & Snapshot](./01-cover-snapshot.md)
- [2. Service Levels](./02-service-levels.md)
- [3. Operational Readiness](./03-operational-readiness.md)
