# Aktieanalys med Python

## Titel
Aktieanalys – portföljvärdering med realtidsdata från Yahoo Finance

## Mål
Projektet ska visa hur Python kan användas för att hämta och analysera realtidsdata från en extern datakälla och omvandla den till användbar information, i det här fallet aktiekurser och portföljvärde. Målet är att koppla grundläggande Python-kunskaper (klasser, arv, funktioner, API-anrop, felhantering) till ett verklighetsbaserat problemområde: investeringar och aktiehandel.

## Metod
Projektet hämtar aktuella aktiekurser via ett externt API (Yahoo Finance), bygger upp en portfölj av innehav med hjälp av klasser (`Aktie` och den ärvande klassen `Utdelningsaktie`), beräknar värdeförändring och risk för varje innehav, och sparar resultatet som en JSON-fil.

Tekniker som används:
- Klasser och arv (`Aktie` → `Utdelningsaktie`)
- Funktioner för beräkning och klassificering
- Felhantering med try/except vid API-anrop
- Standardbiblioteket `json` och `csv`
- Externa biblioteket `requests` för att hämta data via API
- Filhantering (läsning/skrivning av JSON)

## Resultat
Programmet hämtar realtidspriser för tre svenska aktier (VOLV-B.ST, ERIC-B.ST, HM-B.ST), beräknar portföljens totala värde samt värdeförändring och direktavkastning per innehav, och sparar resultatet i portfolj.json. Exempel på utskrift:

```
VOLV-B.ST: 10 st à 323.3 kr = 3233.0 kr
Förändring sedan köp: 29.3% (Uppgång, Hög risk)
Totalt portföljvärde: 6342.5 kr
```

## Analys
Resultatet visar att samma grundmönster som används i AI-utveckling, det vill säga att hämta data från en extern källa via API, strukturera den i objekt och analysera den programmatiskt, direkt går att applicera på finansbranschen. Automatiserad datainsamling och analys är grunden för många verktyg inom algoritmisk handel och riskhantering. Felhanteringen i projektet visar också varför robust kod är viktig när man är beroende av externa datakällor som kan vara otillgängliga eller returnera oväntad data.

## Branschanalys (Mål 1)
Python är ett av de mest använda språken inom finansbranschen, bland annat för dataanalys, algoritmisk handel och riskmodellering. Yrkesroller inom området inkluderar Quantitative Developer, Data Analyst och AI-utvecklare inom fintech, där uppgifter ofta handlar om att hämta, rensa och analysera stora mängder marknadsdata. Trenden går mot mer automatisering, där Python-script och AI-modeller används för att fatta snabbare och mer datadrivna investeringsbeslut. Det här projektet är en enkel version av den typen av verktyg som används i branschen.

## Certifikat-koll (Mål 5)
Några certifikat som är relevanta för en AI-utvecklare inom data- och finansrelaterade roller:
- **AWS Certified Cloud Practitioner** – grundläggande förståelse för molntjänster, ofta en bra start för att visa kunskap om infrastruktur som används för databehandling.
- **Microsoft Certified: Azure AI Fundamentals** – visar grundläggande förståelse för AI- och datatjänster i Azure.
- **Python Institute PCEP/PCAP** – certifierar praktisk kunskap i Python, direkt kopplat till det här projektets teknikval.

## Koppling till kursmål
- **Mål 1** (yrkesroller & branschtrender): Branschanalysen ovan kopplar projektet till hur Python används inom finansbranschen.
- **Mål 2** (Python-syntax): Hela notebooken består av fungerande Python-kod med variabler, loopar och villkor.
- **Mål 3** (objektorienterad programmering): Klassen `Aktie` och barnklassen `Utdelningsaktie` som ärver från den och lägger till egna metoder.
- **Mål 4** (bibliotek & versionshantering): Standard- och externa bibliotek används, och projektet finns på GitHub med minst 5 commits.
- **Mål 5** (certifikat): Certifikat-koll-sektionen ovan listar relevanta certifikat för yrkesrollen.
- **Mål 6** (utveckla pythonprogram): Hela flödet, från att hämta data till att spara resultatet, är ett fungerande eget program.
- **Mål 7** (använda pythonbibliotek): `json` och `csv` som standardbibliotek, `requests` som externt bibliotek för API-anropet.
- **Mål 8** (reflektion): Reflektionen nedan beskriver vad som var svårt och vad jag skulle göra annorlunda.

## Reflektion (Mål 8)
Det svåraste momentet var att hantera externa beroenden som inte alltid fungerar som förväntat, till exempel när det första API:et jag testade (Stooq) slutade fungera och jag fick byta till Yahoo Finance istället. Det tvingade mig att lära mig felsökning på riktigt, inte bara skriva kod som fungerar i teorin. Jag stötte även på problem med git-autentisering när jag bytte GitHub-konto, vilket lärde mig mer om hur versionshantering faktiskt fungerar bakom kulisserna, inte bara kommandona. Om jag gjorde om projektet skulle jag lägga till fler felkontroller tidigare i processen istället för att upptäcka dem efter hand.

## AI-verktyg
Jag har använt AI (Claude) som stöd under projektet, för att förstå Python-koncept, felsöka API-anrop och strukturera klasserna. Jag kan förklara och motivera all kod som lämnas in. Inga personuppgifter har delats med AI-verktyget, endast offentlig aktiekursdata.

## GitHub-länk
https://github.com/Adam-Paktinat/aktieanalys-python

## Installation
1. Clone repot: `git clone https://github.com/Adam-Paktinat/aktieanalys-python.git`
2. Installera requests: `python -m pip install requests`
3. Öppna aktieanalys.ipynb i VS Code eller Jupyter och kör cellerna i ordning.