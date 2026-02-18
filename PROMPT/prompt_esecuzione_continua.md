Sei CODEX. Esegui SOLO gli step definiti in: AI/AI_TASKS.md

REGOLE:
- Prima leggi: AI/AI_PROJECT.md + AI/Knowledge.yaml + AI/AI_TASKS.md
- Non fare refactor, non cambiare architettura, non aggiungere dipendenze, non toccare file non richiesti dallo step.
- Niente web/network a meno che lo step lo chieda esplicitamente.
- Se AI/AI_TASKS.md o istruzioni/percorsi sono mancanti/ambigui: STOP e scrivi cosa manca.

WORKFLOW (ripeti per ogni STEP in ordine):
1) Implementa esattamente “Changes/Scope” dello step (patch minima).
2) Esegui i comandi di test/build indicati in AI/AI_PROJECT.md (fallback: python -m compileall Backend/app).
3) Aggiorna AI/KNOWLEDGE.yaml (solo ciò che è cambiato: file/moduli/endpoint/tabelle/relazioni).
4) Marca lo step come DONE in AI/AI_TASKS.md (aggiungi breve “What changed”).
5) Crea 1 commit con la “Commit message” dello step. Nessun altro commit.

FINE (quando tutti gli step sono DONE):
- Crea/aggiorna file: .temp/AUDIT_AI_TASKS.md con:
  - Data/ora, branch, ultimo commit hash
  - Lista commit (hash + message) in ordine
  - Per ogni step: file toccati + cosa è cambiato (3-6 righe)
  - Test eseguiti + esito
  - Problemi latenti / TODO rimasti / rischi regressione (se presenti) + dove intervenire
  - Note su decisioni “best-effort” (solo se inevitabili)
- Output finale in chat con: path audit + lista commit + eventuali problemi latenti.