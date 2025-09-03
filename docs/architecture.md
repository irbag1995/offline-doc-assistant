# Architettura MVP

## 🧱 Schema dati
- **documents**: id, path, hash, created_at, source, title, category, tags_json, doc_date, due_date, amount_cents, currency, parties_json
- **text_index (FTS5)**: doc_id, title, tags, full_text
- **events**: id, document_id, kind, when_epoch, reminded_bool
- **settings**: k, v
- **audit_local**: ts, action, info_json (nessun contenuto)

---

## 🔐 Sicurezza & Privacy
- DB e file cifrati con SQLCipher
- Pass-phrase utente → derivazione chiave Argon2/PBKDF2
- Nessun dato lascia il device senza export manuale
- Telemetria opt-in: solo conteggi, tempi, crash (no contenuti)

---

## ✅ Criteri di successo demo
- TTD (scan → doc pronto) < 10s
- TTA (query → risultati) < 1s
- Accuratezza estrazione ≥ 90%
- Search success (click top-3) ≥ 75%
- Crash-free sessions ≥ 99%
