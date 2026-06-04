# DATENSCHUTZERKLÄRUNG — ORA Esoterische KI-Plattform
## Version 2.3 | 4. Juni 2026
## Verantwortlicher: Santiago Sáiz / Fundación Hostelling del Ecuador
## privacy@oratrology.com | dpo@oratrology.com

---

## GRUNDPRINZIPIEN
- Minimale Datenerhebung
- Keine Weitergabe oder Verkauf von Daten
- Biometrische Daten sofort nach der Lesung gelöscht
- Emotionsanalysedaten nie gespeichert — nur in Echtzeit
- Standortdaten (Geburtsstadt) nur beim Onboarding-Autocomplete an Google übermittelt
- Open-Source-Komponenten nur für Berechnungen — keine identifizierbare Verarbeitung Ihrer Daten

---

## 1. ERHOBENE DATEN

- Identität: Name, E-Mail
- Geburtsdaten: Datum, Uhrzeit, Ort
- **Standortdaten:** Geburtsstadt oder -ort, beim Onboarding eingegeben (siehe Abschnitt 5 — Google Places API)
- Visuell: Handfotos, Irisfotos, Kaffeefotos
- Narrativ: Traumbeschreibungen, persönliche Fragen
- Zahlung: verarbeitet von Apple/Google/Stripe/PayPal (nicht von ORA gespeichert)
- Automatisch erhoben: Gerätedaten, Nutzung, IP, allgemeiner Standort, Analytik (anonymisiert)

Biometrische Daten (Hand/Iris): doppelte Einwilligung, sofortige Löschung nach Lesung, TLS 1.3 + AES-256, nur an Anthropic Claude API unter DPA weitergegeben.

Passive Emotionsanalyse: nur in Echtzeit, keine Aufzeichnung, nie an Dritte übermittelt.

---

## 2. OPEN-SOURCE-KOMPONENTEN

ORA verwendet Open-Source-Software (Swiss Ephemeris unter AGPLv3) ausschließlich für astronomische Berechnungen. Ihre personenbezogenen Daten werden von diesen Komponenten NIEMALS in identifizierbarer Form verarbeitet.

---

## 3. RECHTSGRUNDLAGE (DSGVO)

| Aktivität | Grundlage |
|-----------|-----------|
| Konto/Lesungen/Zahlungen | Vertrag Art. 6(1)(b) |
| Biometrische Daten | Ausdrückliche Einwilligung Art. 9(2)(a) |
| Geburtsdaten | Ausdrückliche Einwilligung Art. 9(2)(a) |
| Emotionsanalyse | Ausdrückliche Einwilligung Art. 9(2)(a) + Berechtigtes Interesse Art. 6(1)(f) |
| Standort-Autovervollständigung (Onboarding) | Berechtigtes Interesse Art. 6(1)(f) |
| Analytik | Berechtigtes Interesse Art. 6(1)(f) |
| Marketing | Einwilligung Art. 6(1)(a) |

---

## 4. AUFBEWAHRUNGSFRISTEN

| Daten | Zeitraum |
|-------|----------|
| Kontodaten | Kontodauer + 3 Jahre |
| Lesungsverlauf | Konto + 1 Jahr |
| Biometrische Fotos | SOFORTIGE LÖSCHUNG nach Lesung |
| Emotionsanalysedaten | NICHT GESPEICHERT — nur Echtzeitsitzung |
| Sonstige Fotos (Kaffee) | 90 Tage nach Lesung |
| Geburtsstadt | Kontodauer |
| Zahlungsbelege | 7 Jahre (ecuadorianisches Steuerrecht) |
| Analytik (anon) | 3 Jahre |

---

## 5. DATENWEITERGABE

| Anbieter | Rolle | Weitergegebene Daten | Standort |
|----------|-------|----------------------|----------|
| Supabase | DB / Auth / Speicher | Konto + Lesungsdaten | USA (AWS) |
| Anthropic Claude | KI-Lesungsgenerierung | Geburtsdaten, Kontext | USA |
| Apple (App Store / IAP) | App-Vertrieb, Zahlungen | Nur Kauf-Token | USA |
| Google (Firebase / Auth) | Authentifizierung, Push-Benachrichtigungen | Geräte-Token, Auth-Daten | USA |
| **Google (Places API)** | **Geburtsort-Autovervollständigung — nur Onboarding** | **Vom Nutzer eingegebener Teilortsname** | **USA** |
| Stripe / PayPal | Zahlungen | Tokenisierte Zahlungsdaten | USA |
| OneSignal | Push-Benachrichtigungen | Geräte-Token | USA |

**EU-Transfers:** Standardvertragsklauseln (SCC) mit allen US-Anbietern.
**Kein Datenverkauf. Keine Datenmakler-Aktivität.**

### 5.1 Google Places API — Spezifische Offenlegung

ORA integriert die Google Places Autocomplete API ausschließlich beim Onboarding, um dem Nutzer die Eingabe seiner Geburtsstadt zu erleichtern:

- **Was an Google übermittelt wird:** nur der im Geburtsortfeld eingegebene Teilortsname
- **Was Google NICHT erhält:** Name, E-Mail, Geburtsdatum/-uhrzeit, Fotos, Lesungen oder andere personenbezogene Daten
- **Was ORA speichert:** nur der ausgewählte Ortsname im Profil für astrologische Berechnungen
- **Verarbeitung durch Google:** unterliegt den Google-Nutzungsbedingungen (https://developers.google.com/maps/terms) und der Google-Datenschutzerklärung (https://policies.google.com/privacy)
- **Alternative:** Sie können Ihren Geburtsort manuell eingeben — die Autovervollständigung ist nicht obligatorisch

ORA ist nicht verantwortlich für Googles Datenverarbeitungspraktiken über diese Offenlegung hinaus.

---

## 6. IHRE RECHTE

Auskunft, Berichtigung, Löschung, Datenübertragbarkeit, Widerruf, Einschränkung, Widerspruch, Beschwerde bei der zuständigen Datenschutzbehörde (z.B. BfDI).
Kontakt: privacy@oratrology.com — Antwort: 30 Tage.

---

## 7. KONTAKT

privacy@oratrology.com | dpo@oratrology.com | legal@oratrology.com
Rechts-Hub: https://oratrology.com/legal/

---

## CHANGELOG

| Version | Datum | Änderungen |
|---------|-------|------------|
| v2.3 | 4. Jun 2026 | Abschnitt 1: „Standortdaten" hinzugefügt. Abschnitt 3: Rechtsgrundlage Autocomplete. Abschnitt 5: Google in zwei Einträge aufgeteilt (Firebase/Auth und Places API). Abschnitt 5.1 hinzugefügt: spezifische Offenlegung Google Places API. |
| v2.2 | 3. Jun 2026 | Abschnitt 2 hinzugefügt: Open-Source-Komponenten AGPLv3. |
| v2.1 | 14. Mai 2026 | Biometrische Daten und Emotionsanalyse hinzugefügt. |
| v2.0 | 11. Mai 2026 | Erstveröffentlichte Version. |

*ORA Datenschutzerklärung v2.3 | Santiago Sáiz / Fundación Hostelling del Ecuador | oratrology.com*
