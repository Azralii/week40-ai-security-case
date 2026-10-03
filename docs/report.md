# AI Security Case Investigation – Case A

## 1. Executive Summary

Denna rapport analyserar ett fall där flera medarbetare inom en kommunal
förvaltning har fått välformulerade mejl som ser ut att komma från intern
IT-support. Mottagarna uppmanas att använda en länk för att behålla åtkomsten
till ett internt system. En medarbetare har öppnat länken, men det finns ingen
bekräftelse på att inloggningsuppgifter har lämnats, att ett konto har
komprometterats eller att ett intrång har skett. Det är inte heller fastställt
att AI har använts för att skapa mejlen.

Analysen fokuserar på användarkonton, inloggningsuppgifter, interna system och
information som relevanta tillgångar. Confidentiality bedöms vara den mest
relevanta delen av CIA-triaden eftersom en möjlig exponering av
inloggningsuppgifter skulle kunna leda till obehörig åtkomst. Integrity och
Availability kan också påverkas vid ett eventuellt kontoövertagande, men detta
är inte bekräftat.

Riskbedömningen är kvalitativ och risken bedöms som medel utifrån det
tillgängliga underlaget. Analysen använder CIS Controls 6, 8 och 14 för
åtkomstkontroll, logghantering och säkerhetsmedvetenhet. Prioriterade åtgärder
är begränsade behörigheter, relevant autentiserings- och åtkomstloggning samt
rollanpassad phishingutbildning. Fortsatt granskning av teknisk evidens,
särskilt autentiserings- och åtkomstloggar, behövs innan en starkare slutsats
kan dras.

## 2. Fakta, antaganden och scope

### Givna fakta

- Mejlen har skickats till flera medarbetare.
- Avsändarnamnet liknar intern IT-support.
- En mottagare har öppnat länken.
- Ingen bekräftad inloggningsinformation har lämnats.
- Det finns ännu ingen bekräftad incident.
- AI-användning är en möjlighet, inte ett fastställt faktum.

### Antaganden och hypoteser

Följande ska inte behandlas som bekräftade fakta:

- Att mejlen skapades med AI.
- Att ett användarkonto har komprometterats.
- Att inloggningsuppgifter har stulits.
- Att en obehörig person har fått åtkomst till kommunens interna system.

### Information som behöver verifieras

- Vilken adress och domän skickades mejlen från?
- Vart leder länken?
- Har någon lämnat uppgifter efter att ha öppnat länken?
- Finns misstänkta autentiserings- eller åtkomsthändelser i loggarna?
- Har någon obehörig fått åtkomst till ett konto eller system?
- Finns teknisk evidens som kan säga något om hur mejlen skapades?

Analysen avgränsas till de givna uppgifterna i Case A. Möjliga konsekvenser
beskrivs som risker och inte som bekräftade incidenter.

## 3. Tillgångar och händelsekedja

### Relevanta tillgångar

1. Medarbetarnas användarkonton och inloggningsuppgifter.
2. Kommunens interna system.
3. Information som hanteras i de interna systemen.
4. Förtroendet för kommunens interna IT-support.

### Händelsekedja

1. Flera medarbetare får mejl där avsändarnamnet liknar intern IT-support.
2. Mottagarna uppmanas att logga in via en länk för att behålla åtkomsten till
   ett internt system.
3. En medarbetare öppnar länken.
4. Det är inte bekräftat att medarbetaren lämnar några inloggningsuppgifter.
5. Eventuell obehörig åtkomst behöver utredas eftersom det inte finns någon
   bekräftad incident eller något bekräftat intrång.

## 4. CIA och enkel riskbedömning

### Confidentiality

Om inloggningsuppgifter skulle lämnas via länken kan en obehörig person
potentiellt få tillgång till användarkontot och information i kommunens interna
system. Detta är inte bekräftat i caset.

### Integrity

Om ett konto skulle komprometteras kan en obehörig person potentiellt ändra
information eller agera genom användarens konto. Detta skulle kunna påverka
informationens tillförlitlighet. Någon sådan påverkan är inte bekräftad.

### Availability

Om ett konto skulle missbrukas eller behöva spärras som säkerhetsåtgärd kan
användarens åtkomst till det interna systemet påverkas. Caset innehåller ingen
bekräftad störning eller otillgänglighet.

### Kvalitativ riskbedömning

Risken bedöms som **medel**. Flera medarbetare har fått mejlen och en mottagare
har öppnat länken, vilket visar att manipulationen kan leda till handling.
Samtidigt finns ingen bekräftelse på att inloggningsuppgifter har lämnats eller
att ett intrång har skett. Konsekvensen skulle kunna bli betydande om ett konto
komprometteras, men den faktiska påverkan är fortfarande osäker.

## 5. CIS-mappning

### CIS 6 – Access Control Management

CIS 6 är relevant eftersom begränsade behörigheter kan minska konsekvensen om
ett användarkonto skulle komprometteras.

**Åtgärd:** Granska och begränsa användarnas behörigheter till den åtkomst som
behövs för deras arbetsuppgifter.

**Verifiering:** Granska behörigheter och testa att användare inte kan komma åt
resurser som de saknar behörighet till.

### CIS 8 – Audit Log Management

CIS 8 är relevant eftersom autentiserings- och åtkomstloggar kan stödja
upptäckt, spårbarhet och utredning av misstänkt aktivitet.

**Åtgärd:** Säkerställ att relevanta autentiserings- och åtkomsthändelser
loggas och kan granskas.

**Verifiering:** Genomför en kontrollerad testhändelse och kontrollera att
händelsen registreras korrekt och går att granska.

### CIS 14 – Security Awareness and Skills Training

CIS 14 är relevant eftersom medarbetare behöver kunna känna igen phishing och
veta hur misstänkta meddelanden ska verifieras och rapporteras.

**Åtgärd:** Genomför rollanpassad phishingutbildning och inför en tydlig rutin
för rapportering och verifiering.

**Verifiering:** Genomför phishingövningar och följ upp hur medarbetarna
identifierar och rapporterar misstänkta meddelanden.

## 6. Prioriterade åtgärder

De tre prioriterade åtgärderna är:

1. Granska och begränsa användarnas behörigheter.
2. Säkerställ relevant autentiserings- och åtkomstloggning.
3. Genomför rollanpassad phishingutbildning med en tydlig verifierings- och
   rapporteringsrutin.

Åtgärderna kombinerar åtkomstkontroll, upptäckt och mänsklig
säkerhetsmedvetenhet.

## 7. Teknisk koppling

En relevant teknisk koppling är logganalys. I caset har en medarbetare öppnat
länken, men det finns ingen bekräftad information om att ett konto har
komprometterats.

Autentiserings- och åtkomstloggar kan användas som evidens för att undersöka
om det finns exempelvis ovanliga eller obehöriga inloggningsförsök. Detta
kopplar till CIS 8, Audit Log Management, eftersom relevanta loggar behöver
samlas in och kunna granskas för upptäckt och utredning.

Logghändelser ska inte automatiskt tolkas som bevis för ett intrång. De behöver
analyseras tillsammans med övrig information innan en slutsats dras.

## 8. English Security Summary

Den engelska sammanfattningen finns i:

`docs/english_security_summary.md`

## 9. AI- och källredovisning

AI-användning, verifiering och egna korrigeringar redovisas i:

`ai_usage.md`

Källförteckningen finns i:

`docs/references.md`

## 10. Slutsats

Analysen visar att phishingmejlen innebär en säkerhetsrisk för kommunens
användarkonton, inloggningsuppgifter och interna system. Flera medarbetare har
fått mejlen och en medarbetare har öppnat länken. Det finns däremot ingen
bekräftelse på att inloggningsuppgifter har lämnats, att ett konto har
komprometterats eller att ett intrång har skett.

Confidentiality bedöms vara den mest relevanta CIA-dimensionen eftersom en
möjlig exponering av inloggningsuppgifter skulle kunna leda till obehörig
åtkomst till information. Integrity och Availability kan också påverkas vid
ett eventuellt kontoövertagande, men någon sådan påverkan är inte bekräftad.

CIS 6, CIS 8 och CIS 14 används för att koppla risken till åtkomstkontroll,
loggning och säkerhetsmedvetenhet.

Den viktigaste kvarvarande osäkerheten är om länken har lett till någon faktisk
säkerhetspåverkan. Autentiserings- och åtkomstloggar behöver därför granskas
innan en starkare slutsats kan dras. Det är inte heller fastställt att AI har
använts för att skapa mejlen.