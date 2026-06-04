# PRIVACY POLICY — ORA Esoteric AI Platform
## Version 2.3 | June 4, 2026
## Data Controller: Santiago Sáiz / Fundación Hostelling del Ecuador
## privacy@oratrology.com | dpo@oratrology.com

---

## KEY PRINCIPLES
- We collect only what we need
- We never sell your data
- Biometric data (hand/iris photos) deleted immediately after reading
- Emotional analysis data never stored — real-time only
- Location data (birth city) transmitted to Google only during onboarding autocomplete
- You control your data — full rights below
- Open-source components used for calculations only — your data never processed by them in identifiable form

---

## 1. DATA COLLECTED

### Standard Data
- Identity: name, email
- Birth data: date, time, place (for readings)
- Location data: birth city or place name entered during onboarding (see Section 6 — Google Places API)
- Visual: hand photos (palmistry), iris photos (iridology), coffee photos (tasseography)
- Narrative: dream descriptions, personal questions
- Payment: processed by Apple/Google/Stripe/PayPal (not stored by ORA)
- Auto-collected: device info, usage, IP, general location, analytics (anonymized)

### 1.1 BIOMETRIC DATA — MAXIMUM PROTECTION

Hand and iris photographs = biometric data under GDPR Art.9, LOPDP Art.26, LGPD Art.11, BIPA (Illinois).

| Rule | Detail |
|------|--------|
| Double consent | Separate explicit consent — distinct from general account consent |
| Always optional | Text description always available as alternative — photos never mandatory |
| Purpose limitation | Used ONLY to generate your reading — never for ID verification, AI training, or profiling |
| Immediate deletion | Deleted permanently immediately after reading is generated |
| Encryption | TLS 1.3 in transit + AES-256 at rest |
| No third-party sharing | Only to Anthropic Claude API for reading generation, under DPA |
| No AI training | Explicitly prohibited |
| 24h deletion on request | Contact privacy@oratrology.com |

### 1.2 EMOTIONAL ANALYSIS — PASSIVE CAMERA DATA

During active reading sessions, ORA may use your device's front camera to perform real-time emotional analysis, used exclusively to personalize your reading.

| Rule | Detail |
|------|--------|
| No recording | No video or images are captured, stored, or transmitted |
| Real-time only | Not retained after session ends |
| Internal use only | Never shown to you as output |
| Never shared | Never sent to third parties |
| No AI training | Never used to train AI models |
| Optional | Deny camera permission anytime via device Settings → ORA → Camera |

**Legal basis:** GDPR Art. 9(2)(a) + Art. 6(1)(f) | Ecuador LOPDP Art. 26 | Brazil LGPD Art. 11(I)

---

## 2. OPEN-SOURCE COMPONENTS AND DATA PROCESSING

ORA uses open-source software (including Swiss Ephemeris under AGPLv3) exclusively for astronomical and calendar calculations. Your personal data is NEVER processed by these components in identifiable form — they receive only anonymous numerical inputs (date, time, coordinates).

---

## 3. LEGAL BASIS (GDPR)

| Activity | Basis |
|----------|-------|
| Account/readings/payments | Contract Art. 6(1)(b) |
| Biometric data (hand/iris) | Explicit consent Art. 9(2)(a) |
| Birth data | Explicit consent Art. 9(2)(a) |
| Emotional analysis (camera) | Explicit consent Art. 9(2)(a) + Legitimate interest Art. 6(1)(f) |
| Location autocomplete (onboarding) | Legitimate interest Art. 6(1)(f) |
| Analytics | Legitimate interest Art. 6(1)(f) |
| Marketing | Consent Art. 6(1)(a) |
| Legal compliance | Legal obligation Art. 6(1)(c) |

Ecuador: LOPDP consent/legitimacy/proportionality | Brazil: LGPD Art. 7 and 11

---

## 4. DATA USE

- Readings: birth data + photos used ONLY to generate your reading
- Emotional analysis: real-time personalization only — not stored
- Location data: birth city stored in profile for astrological calculations only
- Account: name/email for management and receipts
- Personalization: reading history and preferences
- Astral Rewards: activity data for balance

**NEVER:** sell data, share with advertisers, use photos or emotional data for AI training.

---

## 5. DATA RETENTION

| Data | Period |
|------|--------|
| Account data | Account duration + 3 years |
| Reading history | Account + 1 year |
| Biometric photos (hand/iris) | IMMEDIATE DELETION after reading |
| Emotional analysis data | NOT RETAINED — real-time session only |
| Other photos (coffee) | 90 days after reading |
| Birth location (city name) | Account duration |
| Payment records | 7 years (Ecuador tax law) |
| Analytics (anon) | 3 years |

Account deletion: personal data deleted within 30 days, photos within 7 days.

---

## 6. DATA SHARING

| Provider | Role | Data Shared | Location |
|----------|------|-------------|----------|
| Supabase | DB / auth / storage | Account + reading data | USA (AWS) |
| Anthropic Claude | AI reading generation | Birth data, reading context | USA |
| Apple (App Store / IAP) | App distribution, payments | Purchase tokens only | USA |
| Google (Firebase / Auth) | Authentication, push notifications | Device token, auth credentials | USA |
| **Google (Places API)** | **Birth location autocomplete — onboarding only** | **Partial place name text typed by user** | **USA** |
| Stripe / PayPal | Payments | Tokenized payment data | USA |
| OneSignal | Push notifications | Device token | USA |

**EU transfers:** Standard Contractual Clauses (SCCs) with all US providers.
**No data sale. No data broker activity.**
**Emotional analysis data:** processed on-device or in-session only — never transmitted to any third party.

### 6.1 Google Places API — Specific Disclosure

ORA integrates the Google Places Autocomplete API exclusively during onboarding to help users enter their birth city. The following applies:

- **What is sent to Google:** only the partial text typed in the birth location field
- **What Google does NOT receive:** name, email, birth date/time, photos, readings, or any other personal data
- **What ORA stores:** only the final selected place name, as part of your profile for astrological calculations
- **Google's processing:** governed by Google's own Terms of Service (https://developers.google.com/maps/terms) and Privacy Policy (https://policies.google.com/privacy)
- **Your alternative:** you may type your birth city manually — autocomplete is not mandatory

ORA is not responsible for Google's data processing practices beyond this disclosure.

---

## 7. YOUR RIGHTS (ALL USERS)

Access, Correction, Deletion, Portability, Withdraw Consent, Complaint.

**EU/GDPR additional:** Restriction, Object, No automated decisions.
**Ecuador LOPDP:** Complaint to Superintendencia de Protección de Datos Personales.
**Brazil LGPD:** Complaint to ANPD (gov.br/anpd).
**California CCPA:** Right to know, delete, opt-out of sale (we don't sell).

Contact: privacy@oratrology.com — Response: 30 days.

---

## 8. SECURITY

- TLS 1.2+ in transit | AES-256 at rest (Supabase)
- Supabase Auth with MFA support
- Access controls, regular security reviews
- GDPR breach notification: 72 hours to authorities

---

## 9. AI DISCLOSURE

ORA uses Anthropic Claude API. Reading requests processed by Anthropic under DPA. Data minimization applied. No data used for AI training without consent.

---

## 10. CONTACT

- Privacy: privacy@oratrology.com
- DPO (EU/BR): dpo@oratrology.com
- Legal: legal@oratrology.com
- Legal Hub: https://oratrology.com/legal/

---

## CHANGELOG

| Version | Date | Changes |
|---------|------|---------|
| v2.3 | June 4, 2026 | Section 1: "Location Data" added to data collected. Section 3: legal basis for location autocomplete added. Section 6: Data Sharing table expanded — Google split into two entries (Firebase/Auth and Places API). Section 6.1 added: Google Places API specific disclosure. |
| v2.2 | June 3, 2026 | Section 2 added: Open-Source Components & AGPLv3 data isolation. Section 6: open-source provider note added. |
| v2.1 | May 14, 2026 | Sections 1.1–1.2 added: Biometric data maximum protection and Emotional Analysis passive camera. |
| v2.0 | May 11, 2026 | Initial published version. |

*ORA Privacy Policy v2.3 | Santiago Sáiz / Fundación Hostelling del Ecuador | oratrology.com*
