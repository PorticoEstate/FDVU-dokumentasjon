# Automatisk kvalitetskontroll av FDVU-dokumentasjon

## Prinsippskisse

### Sammendrag

Kommunen mottar store mengder FDVU-dokumentasjon ved overtakelse av bygg og anlegg. Kontroll og kvalitetssikring av denne dokumentasjonen utføres i dag i stor grad manuelt, noe som er ressurskrevende og innebærer risiko for at mangler og feil ikke avdekkes.

Prosjektet skal utvikle en digital kontrollassistent som automatisk analyserer FDVU-dokumentasjon og kontrollerer at leveransene er komplette, strukturerte og i samsvar med NS 3456.

Løsningen vil redusere ressursbruk, redusere risiko ved overtakelse og bidra til høyere kvalitet på dokumentasjonen som benyttes gjennom byggets levetid.

---

# 1. Bakgrunn

Ved overtakelse av byggeprosjekter mottar kommunen ofte flere tusen dokumenter fordelt på:

- PDF
- Word
- Excel
- Tegninger
- BIM-modeller
- Produktdokumentasjon
- Garantidokumenter
- Samsvarserklæringer
- Drifts- og vedlikeholdsinstrukser

Erfaring viser at dokumentasjonen ofte:

- er ufullstendig
- er feil kategorisert
- mangler nødvendig innhold
- er vanskelig å finne igjen i driftsfasen

Kontroll utføres i dag hovedsakelig manuelt og krever betydelige ressurser fra prosjektledere, FDV-koordinatorer og driftspersonell.

---

# 2. Utfordringsbildet

Dagens arbeidsprosess gir flere utfordringer:

## Ressursbruk

- Kontroll av FDVU-leveranser kan ta dager eller uker.
- Store deler av arbeidet består av manuelle gjennomganger.

## Kvalitetsrisiko

- Mangler oppdages ofte sent.
- Viktige dokumenter kan bli oversett.
- Kvaliteten varierer mellom prosjekter.

## Økonomisk risiko

Mangelfull FDVU-dokumentasjon kan føre til:

- ekstra innhenting av dokumentasjon
- tap av garantier
- ineffektiv drift
- økte vedlikeholdskostnader

## Manglende sporbarhet

- Vanskelig å dokumentere hva som er kontrollert.
- Vanskelig å følge opp avvik.

---

# 3. Formål

Prosjektet skal utvikle en løsning som automatisk:

- leser inn FDVU-dokumentasjon
- klassifiserer dokumentene
- kontrollerer at nødvendig dokumentasjon er levert
- identifiserer mangler og avvik
- gir brukerne en enkel statusoversikt

Målet er å gjøre kvalitetskontrollen raskere, mer konsistent og mer sporbar.

---

# 4. Målsetting

## Hovedmål

Redusere tiden brukt på kontroll av FDVU-dokumentasjon med minimum 50 %.

## Delmål

### Kompletthetskontroll

Løsningen skal kunne identifisere:

- manglende dokumenter
- manglende leveranser
- manglende garantier
- manglende drifts- og vedlikeholdsinstrukser

### Strukturkontroll

Løsningen skal kunne kontrollere:

- korrekt kategorisering
- korrekt plassering
- korrekt kobling til system og komponent

### Kvalitetskontroll

Løsningen skal kunne vurdere:

- om dokumentet faktisk inneholder forventet informasjon
- om dokumentet fremstår relevant
- om dokumentet ser ut til å være feilklassifisert

---

# 5. Forslag til løsning

## Prinsipp

Bruk kunstig intelligens til å analysere og kontrollere FDVU-dokumentasjon automatisk.

Brukeren laster opp eller peker til en FDVU-leveranse.

Systemet analyserer dokumentene og produserer en samlet statusrapport.

---

## Hva løsningen skal gjøre

### Trinn 1

Lese dokumenter fra:

- filområder
- prosjektmapper
- SharePoint
- dokumentlager

### Trinn 2

Identifisere:

- dokumenttype
- leverandør
- produkt
- system
- komponent

### Trinn 3

Kontrollere om nødvendig dokumentasjon finnes.

Eksempel:

```text
Ventilasjonsaggregat

✓ Driftsinstruks
✓ Vedlikeholdsinstruks
✓ Produktdatablad
✗ Garanti
✗ Samsvarserklæring
```

### Trinn 4

Generere avviksliste og kvalitetsrapport.

---

# 6. Gevinstpotensial

## Effektivisering

Forventet reduksjon i manuelt kontrollarbeid:

- 50–80 %

## Kvalitetsforbedring

Forventede gevinster:

- færre mangler ved overtakelse
- mer komplett dokumentasjon
- bedre dokumentstruktur

## Redusert risiko

Tidlig identifisering av:

- manglende garantier
- manglende samsvarserklæringer
- manglende vedlikeholdsdokumentasjon
- manglende driftsinstrukser

## Bedre drift

Gir bedre grunnlag for:

- drift
- vedlikehold
- investeringer
- rehabilitering

---

# 7. Forslag til gjennomføring

## Fase 1 – Proof of Concept

### Varighet

6 uker

### Mål

Teste løsningen på én eksisterende FDVU-leveranse.

### Leveranser

- dokumentanalyse
- klassifisering
- avviksrapport
- gevinstvurdering

### Suksesskriterier

- dokumenter identifiseres korrekt
- mangler oppdages automatisk
- potensielle gevinster dokumenteres

---

## Fase 2 – Pilot

### Varighet

3 måneder

### Mål

Ta løsningen i bruk i ett reelt byggeprosjekt.

### Leveranser

- full prosess for FDVU-kontroll
- brukergrensesnitt
- rapportering

### Suksesskriterier

- redusert kontrolltid
- positiv tilbakemelding fra brukerne

---

## Fase 3 – Produksjonssetting

### Varighet

3–6 måneder

### Mål

Implementere løsningen som ordinært arbeidsverktøy.

### Leveranser

- integrasjon mot dokumentlagring
- standardisert arbeidsprosess
- opplæring

---

# 8. Brukergrensesnitt

## Prosjektleder

Prosjektleder skal møte et enkelt dashbord.

Eksempel:

```text
Prosjekt:
Ny skole

Dokumenter analysert:
2 314

Kompletthet:
92 %

Kritiske avvik:
4

Mindre avvik:
17
```

Rødt, gult og grønt benyttes for status.

---

## FDV-ansvarlig

FDV-ansvarlig skal kunne gå ned på systemnivå.

Eksempel:

```text
Ventilasjonsanlegg

✓ Driftsinstruks
✓ Vedlikeholdsinstruks
✓ Produktdatablad
✗ Garanti
```

Systemet foreslår nødvendige oppfølgingspunkter.

---

## Avviksoversikt

Eksempel:

```text
Mangler garanti:
12

Mangler samsvarserklæring:
4

Mulig feilklassifisert:
21
```

Avvik kan eksporteres til Excel eller PDF.

---

## Digital assistent

Brukeren kan stille spørsmål i naturlig språk.

Eksempler:

- Vis alle komponenter uten vedlikeholdsinstruks.
- Hvilke systemer har flest avvik?
- Lag en statusrapport for prosjektet.
- Hvilke dokumenter bør gjennomgås manuelt?

---

# 9. Teknologisk tilnærming

Prosjektet kan gjennomføres med eksisterende teknologi.

## Utviklingsverktøy

- Visual Studio Code
- GitHub Copilot

## Backend

- Python
- FastAPI

## AI

- Dokumentanalyse
- Språkmodeller
- OCR

## Database

- Neo4j (kunnskapsgraf)

## Brukergrensesnitt

- Webbasert løsning
- Dashboard og rapportering

---

# 10. Anbefaling

Det anbefales å starte med et begrenset Proof of Concept basert på én eksisterende FDVU-leveranse.

Målet er å dokumentere:

- treffsikkerhet
- tidsbesparelse
- kvalitetsforbedring
- gevinstpotensial

Prosjektet representerer en lavrisiko investering med høy sannsynlighet for gevinst. Samtidig vil det bidra til digitalisering av eiendomsforvaltningen og etablere et bedre informasjonsgrunnlag for drift, vedlikehold og utvikling av kommunens bygg og anlegg.