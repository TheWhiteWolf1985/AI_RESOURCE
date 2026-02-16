# AI_TASKS

Regole:
- Ogni step deve avere: `Status`, `Goal`, `Scope`, `Changes`, `Commands`, `Acceptance criteria`, `Commit message`.
- `Status` ammessi: `TODO`, `DOING`, `DONE`.
- Commit solo con verifiche verdi (se sono previsti comandi di verifica).
- Se lo step contiene una commit message, usarla identica.
- Aggiornare `KNOWLEDGE` e, se serve, `DECISIONS` dopo ogni step.

## Step standard

### STEP <<REQUIRED>> - <<REQUIRED>>
- Status: TODO
- Goal: <<REQUIRED>>
- Scope: <<REQUIRED>>
- Changes:
  - <<REQUIRED>>
- Commands:
  - <<OPTIONAL>>
- Acceptance criteria:
  - <<REQUIRED>>
- Commit message:
  - "<<REQUIRED>>"
- Blockers/Notes:
  - <<OPTIONAL>>

## Esecuzione corrente

### STEP 001 - Cleanup AI kit repository
- Status: DONE
- Goal: Rimuovere contenuti duplicati non piu' previsti e allineare la documentazione al flusso definitivo.
- Scope: `AI/README.md`, `AI/KNOWLEDGE.yaml`, `AI/AI_TASKS.md`, `AI/AI_INVENTORY.md`, `AI/AI_RUNBOOK.md`, `AI/DECISIONS.md`, `AI/METADATA.yaml`.
- Changes:
  - Rimossa documentazione ridondante non piu' necessaria.
  - Pulita la struttura del kit da componenti dismessi.
  - Aggiornato il flow in `AI/README.md` su copia diretta di `AI/`.
  - Pulite referenze obsolete in documentazione e knowledge.
- Commands:
  - `Get-ChildItem -Recurse -Force`
  - `rg -n -i "legacy_ai_flow_markers"`
- Acceptance criteria:
  - Nessun riferimento residuo a elementi rimossi.
  - README coerente con la tree reale.
- Commit message:
  - "chore(ai): cleanup ai folder structure"
- Blockers/Notes:
  - <<OPTIONAL>>
