# AI-basert kvalitetssikring og kontroll av FDVU-dokumentasjon iht. NS 3456

## Versjon 0.1

### Målgruppe

- Byggherre
- Eiendomsforvalter
- FDV-ansvarlig
- Prosjektleder
- Digitaliseringsansvarlig
- BIM-/informasjonsforvalter

---

# 1. Bakgrunn og problemstilling

Ved overlevering av bygge- og anleggsprosjekter mottar byggherre ofte store mengder FDVU-dokumentasjon. Dokumentasjonen består gjerne av tusenvis av filer fordelt på ulike formater, leverandører, fagområder og systemer.

Selv om dokumentasjonen formelt er levert, er det ofte krevende å verifisere at:

- all nødvendig dokumentasjon foreligger
- dokumentene er knyttet til riktige bygningsdeler og systemer
- dokumentasjonen inneholder nødvendig informasjon
- dokumentene er oppdaterte og relevante
- dokumentasjonen følger anbefalt struktur og innhold i NS 3456
- informasjonen lar seg gjenfinne og benytte effektivt i driftsfasen

NS 3456 beskriver hvilke typer FDVU-dokumentasjon som skal være tilgjengelig for eier av bygninger og tilhørende uteområder, slik at eier får nødvendig grunnlag for forvaltning, drift, vedlikehold og utvikling gjennom byggets levetid. 【1-e2dfd9】【2-18d98e】

Kontroll av FDVU-leveranser gjennomføres i dag ofte manuelt, noe som medfører:

- høyt ressursforbruk
- risiko for menneskelige feil
- ulik vurderingspraksis mellom prosjekter
- begrenset sporbarhet
- mangelfull kontroll av dokumentenes faktiske innhold

Det er derfor behov for en løsning som automatisk kan analysere, klassifisere og kvalitetssikre FDVU-dokumentasjon opp mot kravene i NS 3456. 【3-6fe06b】【4-6f5041】

---

# 2. Målsetting

Målet er å etablere en AI-basert kontrollagent som bistår prosjektledere og FDV-ansvarlige med å:

## Kontrollere kompletthet

Avdekke manglende dokumentasjon for:

- bygninger
- systemer
- komponenter
- tekniske installasjoner
- uteanlegg

## Kontrollere struktur

Verifisere at dokumentene er korrekt organisert, klassifisert og knyttet til riktige objekter.

## Kontrollere kvalitet

Vurdere om dokumentenes innhold faktisk tilfredsstiller kravene til dokumenttypen.

Eksempel:

Et dokument kan hete:

> Vedlikeholdsinstruks.pdf

Mens innholdet i realiteten kun består av et produktdatablad.

Løsningen skal kunne avdekke slike avvik.

## Gi beslutningsstøtte

Prosjektleder og FDV-ansvarlig skal få en rask oversikt over:

- leveransens modenhet
- mangler
- avvik
- risikoområder
- dokumentasjonskvalitet

---

# 3. Overordnet strategi

## Fase 1 – Digitalisering av kontrollprosessen

Automatisere innsamling og analyse av FDVU-dokumentasjon.

Mål:

- redusere manuelt arbeid
- standardisere kontroller
- etablere sporbar dokumentasjon

---

## Fase 2 – Etablere en felles informasjonsmodell

Bygge en struktur som kobler sammen:

```text
Bygg
 └─ System
     └─ Komponent
         └─ Dokument
```

Basert på:

- NS 3451
- TFM (NS 3457)
- BIM-modeller
- FDVU-struktur

---

## Fase 3 – Innføre AI-basert kvalitetskontroll

Løsningen skal benytte språkmodeller og dokumentanalyse for å:

- forstå dokumentinnhold
- identifisere dokumenttyper
- finne mangler
- avdekke feilplassering og feilklassifisering

---

## Fase 4 – Kontinuerlig forbedring

Systemet forbedres gjennom:

- historiske prosjekter
- registrerte avvik
- brukerfeedback
- forbedrede regelsett

---

# 4. Forslag til løsning

## Hovedarkitektur

```text
Dokumentlager
      |
      v
Dokumentinnlesing
      |
      v
OCR / Tekstekstraksjon
      |
      v
AI Analyse
      |
      v
Kunnskapsgraf
      |
      v
NS 3456 Regelmotor
      |
      v
Webportal / Agent
```

---

## Dokumentkilder

Løsningen skal ikke være avhengig av SharePoint.

Dokumenter kan hentes fra:

- filservere
- nettverksdisker
- SharePoint
- Teams
- Azure Blob Storage
- AWS S3
- FDVU-systemer
- BIM-plattformer
- dokumentarkiv

---

## Støttede dokumentformater

- PDF
- DOCX
- XLSX
- PPTX
- IFC
- XML
- E-post
- Bilder
- Skannede dokumenter

---

## Dokumentanalyse

For hvert dokument registreres blant annet:

```text
Dokumentnummer
Dokumenttype
Leverandør
Produkt
System
Komponent
TFM-kode
Revisjon
Versjon
Dato
```

---

## Innholdsanalyse med AI

Løsningen skal kunne vurdere om dokumentet inneholder forventet informasjon.

Eksempel:

### Driftsinstruks

Forventet innhold:

- oppstart
- normal drift
- feilhåndtering
- alarmhåndtering

### Vedlikeholdsinstruks

Forventet innhold:

- vedlikeholdsintervaller
- kontrollrutiner
- reservedeler
- anbefalt service

### Garantidokument

Forventet innhold:

- garantiperiode
- leverandørinformasjon
- kontaktinformasjon
- reklamasjonsbetingelser

---

## Regelmotor

Regelmotoren bygger på NS 3456 samt virksomhetens egne krav.

Eksempel:

### Ventilasjonsaggregat

Krav:

```text
✓ Driftsinstruks
✓ Vedlikeholdsinstruks
✓ Produktdatablad
✓ Garantidokument
✓ Samsvarserklæring
```

Manglende dokumentasjon registreres automatisk som avvik.

---

## Kunnskapsgraf

For å håndtere komplekse relasjoner anbefales en grafdatabase, eksempelvis Neo4j.

### Informasjonsmodell

```text
Bygg
 |
 +-- System
        |
        +-- Komponent
                |
                +-- Dokument
                |
                +-- Leverandør
```

Fordeler:

- effektiv avviksanalyse
- sporbarhet
- fleksible søk
- kobling mot BIM og TFM

---

# 5. Milepælsplan

## Milepæl 1 – Foranalyse

Varighet: 4 uker

Leveranser:

- kartlegging av dagens prosess
- identifisering av dokumentkilder
- kravspesifikasjon
- teknologivalg

---

## Milepæl 2 – Prototype

Varighet: 6 uker

Leveranser:

- innlesing av PDF og Word
- automatisk dokumentklassifisering
- enkel dokumentoversikt

Resultat:

Første fungerende demonstrator.

---

## Milepæl 3 – NS 3456-regelmotor

Varighet: 8 uker

Leveranser:

- definisjon av kontrollregler
- avvikshåndtering
- kompletthetsanalyse

Resultat:

Automatisk kontroll av dokumentleveranser.

---

## Milepæl 4 – Kunnskapsgraf

Varighet: 8 uker

Leveranser:

- Neo4j-modell
- relasjoner mellom bygg, systemer og dokumenter
- avanserte søk og kontroller

---

## Milepæl 5 – AI-kvalitetskontroll

Varighet: 10 uker

Leveranser:

- innholdsanalyse
- dokumentvurdering
- kvalitetsscore

Resultat:

Automatisk vurdering av dokumentkvalitet.

---

## Milepæl 6 – Pilotprosjekt

Varighet: 12 uker

Leveranser:

- analyse av reell FDVU-leveranse
- brukerakseptansetest
- gevinstanalyse
- anbefaling for videre utrulling

---

# 6. Forslag til brukergrensesnitt

## Designprinsipper

Løsningen skal være:

- enkel
- intuitiv
- handlingsorientert
- forståelig for ikke-tekniske brukere

Primære brukere:

- prosjektledere
- FDV-koordinatorer
- eiendomsforvaltere

---

## Hovedside

```text
FDVU Kontroll

Prosjekt:
Bergen Kulturhus

Status:
87 % komplett

Kritiske avvik: 12
Mindre avvik: 31

[Vis detaljer]
```

---

## Dashboard

```text
Dokumenter analysert: 12 543

Korrekt klassifisert: 11 921

Mangler: 322

Avvik: 108

Kvalitetsscore: 91 %
```

Grafiske indikatorer:

- trafikklys
- prosentindikatorer
- trendgrafer
- risikovarsler

---

## Byggoversikt

```text
Bygg A

✅ VVS

⚠ Elkraft

✅ Tele

⚠ Utomhus
```

Brukeren kan navigere ned til system- og komponentnivå.

---

## Systemoversikt

Eksempel:

```text
Ventilasjonsanlegg
```

Resultat:

```text
Driftsinstruks ............ ✅
Vedlikeholdsinstruks ...... ✅
Produktdatablad ........... ✅
Garanti ................... ✅
Samsvarserklæring ......... ❌
```

---

## Avvikssenter

```text
Kritiske avvik

1. Aggregat V-01
   Mangler samsvarserklæring

2. SD-anlegg
   Mangler driftshåndbok

3. Brannsentral
   Mangler garantidokumentasjon
```

Alle avvik kan eksporteres til Excel eller PDF.

---

## AI-assistent

Brukerne kan kommunisere med løsningen i naturlig språk.

Eksempler:

> Vis alle komponenter uten vedlikeholdsinstruks.

> Hvilke systemer har lavest dokumentasjonskvalitet?

> Hvilke dokumenter ser ut til å være feilklassifisert?

> Vis alle avvik for bygg A.

> Generer sluttrapport for prosjektet.

---

# 7. Teknologiforslag

## Utviklingsplattform

- Visual Studio Code
- GitHub Copilot

## Backend

- Python
- FastAPI

## AI-komponenter

- Azure OpenAI
- Azure AI Document Intelligence

## Database

- Neo4j

## Frontend

- React
- Power BI (rapportering)

---

# 8. Forventede gevinster

## Operasjonelle gevinster

- 50–90 % reduksjon i manuell dokumentkontroll
- raskere overtakelsesprosesser
- standardisert kvalitetskontroll
- bedre sporbarhet

## Kvalitetsgevinster

- høyere kvalitet på FDVU-dokumentasjon
- færre mangler ved overlevering
- bedre grunnlag for drift og vedlikehold

## Strategiske gevinster

- digitalisert FDVU-prosess
- bedre datakvalitet
- grunnlag for digital tvilling
- muliggjør fremtidig prediktivt vedlikehold
- mer effektiv informasjonsforvaltning gjennom byggets livsløp

---

# 9. Konklusjon

En AI-basert kontrollagent for FDVU-dokumentasjon etter NS 3456 er fullt gjennomførbar med dagens teknologi. Ved å kombinere dokumentanalyse, kunstig intelligens, kunnskapsgraf og regelbasert kontroll kan store deler av dagens manuelle kvalitetskontroll automatiseres.

Løsningen vil kunne kontrollere:

- om dokumentasjon er levert
- om dokumentasjon er korrekt klassifisert
- om dokumentinnholdet er relevant og tilstrekkelig
- om leveransen oppfyller krav og forventninger i NS 3456

Resultatet vil være bedre FDVU-kvalitet, redusert ressursbruk og et mer komplett digitalt grunnlag for forvaltning, drift, vedlikehold og utvikling av bygg og anlegg.