# POLITIQUE DE CONFIDENTIALITÉ — ORA Plateforme IA Ésotérique
## Version 2.3 | 4 juin 2026
## Responsable du traitement : Santiago Sáiz / Fundación Hostelling del Ecuador
## privacy@oratrology.com | dpo@oratrology.com

---

## PRINCIPES CLÉS
- Collecte minimale des données
- Jamais de vente de données
- Données biométriques supprimées immédiatement après la lecture
- Données d'analyse émotionnelle jamais stockées — temps réel uniquement
- Données de localisation (ville de naissance) transmises à Google uniquement lors de l'autocomplétion pendant l'onboarding
- Composants open source utilisés uniquement pour les calculs — vos données ne sont jamais traitées par eux de manière identifiable

---

## 1. DONNÉES COLLECTÉES

- Identité : nom, email
- Données de naissance : date, heure, lieu
- **Données de localisation :** ville ou lieu de naissance saisi lors de l'onboarding (voir Section 6 — API Google Places)
- Visuels : photos de main, iris, café
- Narratifs : descriptions de rêves, questions personnelles
- Paiement : traité par Apple/Google/Stripe/PayPal (non stocké par ORA)
- Auto-collectés : infos appareil, utilisation, IP, localisation générale, analytique (anonymisée)

Données biométriques (main/iris) : consentement double, suppression immédiate après lecture, chiffrement TLS 1.3 + AES-256, jamais partagées sauf Anthropic Claude API sous DPA.

Analyse émotionnelle passive : temps réel uniquement, aucun enregistrement, jamais transmise à des tiers.

---

## 2. COMPOSANTS OPEN SOURCE

ORA utilise des composants open source (Swiss Ephemeris sous AGPLv3) exclusivement pour des calculs astronomiques. Vos données personnelles ne sont JAMAIS traitées par ces composants de manière identifiable.

---

## 3. BASE LÉGALE (RGPD)

| Activité | Base |
|----------|------|
| Compte/lectures/paiements | Contrat Art. 6(1)(b) |
| Données biométriques | Consentement explicite Art. 9(2)(a) |
| Données de naissance | Consentement explicite Art. 9(2)(a) |
| Analyse émotionnelle | Consentement explicite Art. 9(2)(a) + Intérêt légitime Art. 6(1)(f) |
| Autocomplétion localisation (onboarding) | Intérêt légitime Art. 6(1)(f) |
| Analytique | Intérêt légitime Art. 6(1)(f) |
| Marketing | Consentement Art. 6(1)(a) |

---

## 4. CONSERVATION DES DONNÉES

| Donnée | Période |
|--------|---------|
| Données de compte | Durée du compte + 3 ans |
| Historique des lectures | Compte + 1 an |
| Photos biométriques | SUPPRESSION IMMÉDIATE après lecture |
| Données analyse émotionnelle | NON CONSERVÉES — temps réel uniquement |
| Autres photos (café) | 90 jours après lecture |
| Ville de naissance | Durée du compte |
| Données de paiement | 7 ans (fiscalité équatorienne) |
| Analytique (anon) | 3 ans |

---

## 5. PARTAGE DES DONNÉES

| Fournisseur | Rôle | Données partagées | Localisation |
|-------------|------|-------------------|--------------|
| Supabase | BD / auth / stockage | Compte + données de lecture | États-Unis (AWS) |
| Anthropic Claude | Génération de lectures IA | Données de naissance, contexte | États-Unis |
| Apple (App Store / IAP) | Distribution app, paiements | Tokens d'achat uniquement | États-Unis |
| Google (Firebase / Auth) | Authentification, notifications push | Token appareil, identifiants auth | États-Unis |
| **Google (API Places)** | **Autocomplétion lieu de naissance — onboarding uniquement** | **Texte partiel du lieu saisi par l'utilisateur** | **États-Unis** |
| Stripe / PayPal | Paiements | Données de paiement tokenisées | États-Unis |
| OneSignal | Notifications push | Token appareil | États-Unis |

**Transferts UE :** Clauses Contractuelles Types (CCT) avec tous les fournisseurs américains.
**Aucune vente de données. Aucune activité de courtier en données.**

### 5.1 API Google Places — Divulgation Spécifique

ORA intègre l'API Google Places Autocomplete exclusivement lors de l'onboarding pour aider l'utilisateur à saisir sa ville de naissance :

- **Ce qui est envoyé à Google :** uniquement le texte partiel saisi dans le champ de lieu de naissance
- **Ce que Google ne reçoit PAS :** nom, email, date/heure de naissance, photos, lectures ou autres données personnelles
- **Ce qu'ORA stocke :** uniquement le nom du lieu sélectionné, dans votre profil pour les calculs astrologiques
- **Traitement par Google :** régi par les CGU Google (https://developers.google.com/maps/terms) et la Politique de confidentialité Google (https://policies.google.com/privacy)
- **Alternative :** vous pouvez saisir votre ville manuellement — l'autocomplétion n'est pas obligatoire

ORA n'est pas responsable des pratiques de traitement des données de Google au-delà de cette divulgation.

---

## 6. VOS DROITS

Accès, Rectification, Suppression, Portabilité, Retrait du consentement, Restriction, Opposition, Réclamation auprès de la CNIL ou autorité compétente.
Contact : privacy@oratrology.com — Réponse : 30 jours.

---

## 7. CONTACT

privacy@oratrology.com | dpo@oratrology.com | legal@oratrology.com
Hub Légal : https://oratrology.com/legal/

---

## CHANGELOG

| Version | Date | Modifications |
|---------|------|---------------|
| v2.3 | 4 juin 2026 | Section 1 : "Données de localisation" ajoutées. Section 3 : base légale autocomplétion. Section 5 : Google séparé en deux entrées (Firebase/Auth et API Places). Section 5.1 ajoutée : divulgation spécifique API Google Places. |
| v2.2 | 3 juin 2026 | Section 2 ajoutée : composants open source AGPLv3. |
| v2.1 | 14 mai 2026 | Données biométriques et analyse émotionnelle ajoutées. |
| v2.0 | 11 mai 2026 | Version initiale publiée. |

*ORA Politique de Confidentialité v2.3 | Santiago Sáiz / Fundación Hostelling del Ecuador | oratrology.com*
