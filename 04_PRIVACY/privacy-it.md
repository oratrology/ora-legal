# INFORMATIVA SULLA PRIVACY — ORA Piattaforma AI Esoterica
## Versione 2.3 | 4 giugno 2026
## Titolare del trattamento: Santiago Sáiz / Fundación Hostelling del Ecuador
## privacy@oratrology.com | dpo@oratrology.com

---

## PRINCIPI CHIAVE
- Raccogliamo solo ciò che è necessario
- Non vendiamo mai i tuoi dati
- Dati biometrici eliminati immediatamente dopo la lettura
- Dati di analisi emotiva mai archiviati — solo in tempo reale
- Dati di localizzazione (città di nascita) trasmessi a Google solo durante l'autocompletamento dell'onboarding
- Componenti open source solo per calcoli — i tuoi dati non sono mai elaborati da essi in forma identificabile

---

## 1. DATI RACCOLTI

- Identità: nome, email
- Dati di nascita: data, ora, luogo
- **Dati di localizzazione:** città o luogo di nascita inserito durante l'onboarding (vedere Sezione 6 — API Google Places)
- Visivi: foto della mano, iride, caffè
- Narrativi: descrizioni dei sogni, domande personali
- Pagamento: elaborato da Apple/Google/Stripe/PayPal (non archiviato da ORA)
- Raccolti automaticamente: info dispositivo, utilizzo, IP, posizione generale, analisi (anonimizzate)

Dati biometrici (mano/iride): doppio consenso, eliminazione immediata dopo la lettura, crittografia TLS 1.3 + AES-256, mai condivisi tranne con Anthropic Claude API sotto DPA.

Analisi emotiva passiva: solo in tempo reale, nessuna registrazione, mai trasmessa a terze parti.

---

## 2. COMPONENTI OPEN SOURCE

ORA utilizza componenti open source (Swiss Ephemeris sotto AGPLv3) esclusivamente per calcoli astronomici. I tuoi dati personali non vengono MAI elaborati da questi componenti in forma identificabile.

---

## 3. BASE GIURIDICA (GDPR)

| Attività | Base |
|----------|------|
| Account/letture/pagamenti | Contratto Art. 6(1)(b) |
| Dati biometrici | Consenso esplicito Art. 9(2)(a) |
| Dati di nascita | Consenso esplicito Art. 9(2)(a) |
| Analisi emotiva | Consenso esplicito Art. 9(2)(a) + Interesse legittimo Art. 6(1)(f) |
| Autocompletamento localizzazione (onboarding) | Interesse legittimo Art. 6(1)(f) |
| Analisi | Interesse legittimo Art. 6(1)(f) |
| Marketing | Consenso Art. 6(1)(a) |

---

## 4. CONSERVAZIONE DEI DATI

| Dato | Periodo |
|------|---------|
| Dati account | Durata account + 3 anni |
| Storico letture | Account + 1 anno |
| Foto biometriche | ELIMINAZIONE IMMEDIATA dopo lettura |
| Dati analisi emotiva | NON CONSERVATI — solo sessione in tempo reale |
| Altre foto (caffè) | 90 giorni dopo lettura |
| Città di nascita | Durata dell'account |
| Registrazioni pagamenti | 7 anni (legge fiscale Ecuador) |
| Analisi (anon) | 3 anni |

---

## 5. CONDIVISIONE DEI DATI

| Fornitore | Ruolo | Dati condivisi | Ubicazione |
|-----------|-------|----------------|------------|
| Supabase | DB / auth / storage | Account + dati letture | USA (AWS) |
| Anthropic Claude | Generazione letture IA | Dati di nascita, contesto | USA |
| Apple (App Store / IAP) | Distribuzione app, pagamenti | Solo token di acquisto | USA |
| Google (Firebase / Auth) | Autenticazione, notifiche push | Token dispositivo, credenziali auth | USA |
| **Google (API Places)** | **Autocompletamento luogo di nascita — solo onboarding** | **Testo parziale del luogo digitato dall'utente** | **USA** |
| Stripe / PayPal | Pagamenti | Dati di pagamento tokenizzati | USA |
| OneSignal | Notifiche push | Token dispositivo | USA |

**Trasferimenti UE:** Clausole Contrattuali Standard (SCC).
**Nessuna vendita di dati. Nessuna attività di data broker.**

### 5.1 API Google Places — Divulgazione Specifica

ORA integra l'API Google Places Autocomplete esclusivamente durante l'onboarding per aiutare l'utente a inserire la propria città di nascita:

- **Cosa viene inviato a Google:** solo il testo parziale digitato nel campo luogo di nascita
- **Cosa Google NON riceve:** nome, email, data/ora di nascita, foto, letture o altri dati personali
- **Cosa ORA conserva:** solo il nome del luogo selezionato, nel profilo per i calcoli astrologici
- **Elaborazione da parte di Google:** regolata dai Termini di Servizio di Google (https://developers.google.com/maps/terms) e dalla Privacy Policy di Google (https://policies.google.com/privacy)
- **Alternativa:** puoi digitare la tua città manualmente — l'autocompletamento non è obbligatorio

ORA non è responsabile delle pratiche di trattamento dei dati di Google al di là di questa divulgazione.

---

## 6. I TUOI DIRITTI

Accesso, Rettifica, Cancellazione, Portabilità, Revoca del Consenso, Restrizione, Opposizione, Reclamo al Garante per la Protezione dei Dati Personali.
Contatto: privacy@oratrology.com — Risposta: 30 giorni.

---

## 7. CONTATTI

privacy@oratrology.com | dpo@oratrology.com | legal@oratrology.com
Hub Legale: https://oratrology.com/legal/

---

## CHANGELOG

| Versione | Data | Modifiche |
|----------|------|-----------|
| v2.3 | 4 giu 2026 | Sezione 1: "Dati di localizzazione" aggiunti. Sezione 3: base giuridica autocompletamento. Sezione 5: Google separato in due voci (Firebase/Auth e API Places). Sezione 5.1 aggiunta: divulgazione specifica API Google Places. |
| v2.2 | 3 giu 2026 | Sezione 2 aggiunta: componenti open source AGPLv3. |
| v2.1 | 14 mag 2026 | Dati biometrici e analisi emotiva aggiunti. |
| v2.0 | 11 mag 2026 | Versione iniziale pubblicata. |

*ORA Informativa sulla Privacy v2.3 | Santiago Sáiz / Fundación Hostelling del Ecuador | oratrology.com*
