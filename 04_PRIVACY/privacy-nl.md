# PRIVACYBELEID — ORA Esoterisch AI-Platform
## Versie 2.3 | 4 juni 2026
## Verwerkingsverantwoordelijke: Santiago Sáiz / Fundación Hostelling del Ecuador
## privacy@oratrology.com | dpo@oratrology.com

---

## KERNPRINCIPES
- Minimale gegevensverzameling
- Nooit verkoop van gegevens
- Biometrische gegevens direct na de reading verwijderd
- Emotionele analysegegevens nooit opgeslagen — alleen realtime
- Locatiegegevens (geboortestad) alleen tijdens onboarding-autocomplete naar Google verzonden
- Open-source componenten alleen voor berekeningen — uw gegevens nooit identificeerbaar verwerkt

---

## 1. VERZAMELDE GEGEVENS

- Identiteit: naam, e-mail
- Geboortegegevens: datum, tijd, plaats
- **Locatiegegevens:** geboortestad of -plaats ingevoerd tijdens onboarding (zie Sectie 5 — Google Places API)
- Visueel: handfoto's, irisfoto's, koffiefoto's
- Narratief: droombeschrijvingen, persoonlijke vragen
- Betaling: verwerkt door Apple/Google/Stripe/PayPal (niet opgeslagen door ORA)
- Automatisch verzameld: apparaatgegevens, gebruik, IP, algemene locatie, analyses (geanonimiseerd)

Biometrische gegevens (hand/iris): dubbele toestemming, directe verwijdering na reading, TLS 1.3 + AES-256, alleen gedeeld met Anthropic Claude API onder DPA.

Passieve emotionele analyse: alleen realtime, geen opname, nooit doorgezonden aan derden.

---

## 2. OPEN-SOURCE COMPONENTEN

ORA gebruikt open-source software (Swiss Ephemeris onder AGPLv3) uitsluitend voor astronomische berekeningen. Uw persoonsgegevens worden NOOIT in identificeerbare vorm verwerkt door deze componenten.

---

## 3. RECHTSGRONDSLAG (AVG/GDPR)

| Activiteit | Grondslag |
|------------|-----------|
| Account/readings/betalingen | Overeenkomst Art. 6(1)(b) |
| Biometrische gegevens | Uitdrukkelijke toestemming Art. 9(2)(a) |
| Geboortegegevens | Uitdrukkelijke toestemming Art. 9(2)(a) |
| Emotionele analyse | Uitdrukkelijke toestemming Art. 9(2)(a) + Gerechtvaardigde belangen Art. 6(1)(f) |
| Locatie-autocomplete (onboarding) | Gerechtvaardigde belangen Art. 6(1)(f) |
| Analyses | Gerechtvaardigde belangen Art. 6(1)(f) |
| Marketing | Toestemming Art. 6(1)(a) |

---

## 4. BEWAARPERIODEN

| Gegeven | Periode |
|---------|---------|
| Accountgegevens | Accountduur + 3 jaar |
| Readinggeschiedenis | Account + 1 jaar |
| Biometrische foto's | DIRECTE VERWIJDERING na reading |
| Emotionele analysegegevens | NIET BEWAARD — alleen realtime sessie |
| Andere foto's (koffie) | 90 dagen na reading |
| Geboortestad | Accountduur |
| Betalingsgegevens | 7 jaar (Ecuadoriaans belastingrecht) |
| Analyses (anon) | 3 jaar |

---

## 5. GEGEVENSDELING

| Aanbieder | Rol | Gedeelde gegevens | Locatie |
|-----------|-----|-------------------|---------|
| Supabase | DB / auth / opslag | Account + readinggegevens | VS (AWS) |
| Anthropic Claude | AI-readinggeneratie | Geboortegegevens, context | VS |
| Apple (App Store / IAP) | App-distributie, betalingen | Alleen aankooptokens | VS |
| Google (Firebase / Auth) | Authenticatie, pushmeldingen | Apparaattoken, auth-gegevens | VS |
| **Google (Places API)** | **Geboorteplaats-autocomplete — alleen onboarding** | **Gedeeltelijke plaatsnaam getypt door gebruiker** | **VS** |
| Stripe / PayPal | Betalingen | Getokeniseerde betalingsgegevens | VS |
| OneSignal | Pushmeldingen | Apparaattoken | VS |

**EU-overdrachten:** Standaardcontractbepalingen (SCC's) met alle Amerikaanse aanbieders.
**Geen gegevensverkoop. Geen datamakelaaractiviteit.**

### 5.1 Google Places API — Specifieke Openbaarmaking

ORA integreert de Google Places Autocomplete API uitsluitend tijdens onboarding om de gebruiker te helpen bij het invoeren van zijn geboortestad:

- **Wat naar Google wordt verzonden:** alleen de gedeeltelijke tekst getypt in het geboorteveld
- **Wat Google NIET ontvangt:** naam, e-mail, geboortedatum/-tijd, foto's, readings of andere persoonsgegevens
- **Wat ORA opslaat:** alleen de geselecteerde plaatsnaam in het profiel voor astrologische berekeningen
- **Verwerking door Google:** onderhevig aan Servicevoorwaarden van Google (https://developers.google.com/maps/terms) en Privacybeleid van Google (https://policies.google.com/privacy)
- **Alternatief:** u kunt uw geboorteplaats handmatig invoeren — autocomplete is niet verplicht

ORA is niet verantwoordelijk voor de gegevensverwerkingspraktijken van Google buiten deze openbaarmaking.

---

## 6. UW RECHTEN

Inzage, Rectificatie, Verwijdering, Overdraagbaarheid, Intrekking Toestemming, Beperking, Bezwaar, Klacht bij de Autoriteit Persoonsgegevens (AP).
Contact: privacy@oratrology.com — Reactie: 30 dagen.

---

## 7. CONTACT

privacy@oratrology.com | dpo@oratrology.com | legal@oratrology.com
Juridische Hub: https://oratrology.com/legal/

---

## CHANGELOG

| Versie | Datum | Wijzigingen |
|--------|-------|-------------|
| v2.3 | 4 jun 2026 | Sectie 1: "Locatiegegevens" toegevoegd. Sectie 3: rechtsgrondslag autocomplete. Sectie 5: Google opgesplitst in twee vermeldingen (Firebase/Auth en Places API). Sectie 5.1 toegevoegd: specifieke openbaarmaking Google Places API. |
| v2.2 | 3 jun 2026 | Sectie 2 toegevoegd: open-source componenten AGPLv3. |
| v2.1 | 14 mei 2026 | Biometrische gegevens en emotionele analyse toegevoegd. |
| v2.0 | 11 mei 2026 | Eerste gepubliceerde versie. |

*ORA Privacybeleid v2.3 | Santiago Sáiz / Fundación Hostelling del Ecuador | oratrology.com*
