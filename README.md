# Offline Document Assistant (MVP Demo)

## 🎯 Obiettivo
Costruire una **demo Scenario A (100% on-device, privacy-first)** per gestione documenti con OCR, estrazione campi chiave, ricerca semantica leggera, promemoria scadenze e backup cifrato.

Target: test chiuso con 10–20 persone (iOS/Android/Windows/Web), raccolta metriche anonime e feedback UX.

---

## 📦 Stack Tecnico
- **Framework mobile**: Flutter
- **OCR on-device**: Google ML Kit Text Recognition
- **DB**: SQLite (SQLCipher) + FTS5
- **Ricerca**: full-text + sinonimi statici
- **Backup**: file cifrato `.vault` export/import
- **Promemoria**: notifiche locali
- **Telemetria**: opt-in, solo metriche anonime (no contenuti)

---

## 🛠 Roadmap 8 settimane (Demo)
1. Setup progetto, DB cifrato, indice FTS
2. OCR camera/import + estrazione campi chiave
3. UI documento + ricerca base
4. Promemoria locali + notifiche
5. Backup .vault + restore
6. Telemetria opt-in + raccolta log
7. QA + test golden
8. Release su TestFlight / Internal Testing

---

## 🧪 Script test (per amici/parenti)
1. Scansiona 3 documenti (bolletta, scontrino, PDF medico) e controlla metadati.
2. Trova “spese > 100€” e “documenti in scadenza entro 30 giorni”.
3. Correggi un importo riconosciuto male.
4. Imposta promemoria su due_date.
5. Fai backup `.vault` e ripristina su altro device.

---
