# DECISIONS

## ADR-0001
- Date: 2026-02-16
- Context: Bootstrap iniziale AI Kit con struttura presente ma file quasi vuoti.
- Decision: Popolare i file core con baseline riusabile.
- Alternatives:
  - Lasciare placeholder minimi senza linee guida operative.
  - Rimandare esempi e checklist a una fase successiva.
- Consequences:
  - Avvio piu' rapido nei nuovi progetti.
  - Minore rischio di task non allineati.

## ADR-0002
- Date: 2026-02-16
- Context: Necessita' di uniformare placeholder e guida operativa della cartella AI.
- Decision: Standardizzare i placeholder su `<<REQUIRED>>` e `<<OPTIONAL>>`.
- Alternatives:
  - Mantenere placeholder eterogenei.
- Consequences:
  - Compilazione piu' coerente e prevedibile.

## ADR-0003
- Date: 2026-02-16
- Context: Flusso definitivo: copia diretta della cartella `AI/` nelle repo target, senza duplicati locali.
- Decision: Rimuovere directory e file duplicati non necessari e mantenere un unico set di documenti attivi in `AI/`.
- Alternatives:
  - Mantenere contenuti duplicati con rischio divergenza.
- Consequences:
  - Meno manutenzione e meno inconsistenze.
  - Onboarding piu' lineare per i team.

## ADR formato
- Date: <<REQUIRED>>
- Context: <<REQUIRED>>
- Decision: <<REQUIRED>>
- Alternatives:
  - <<OPTIONAL>>
- Consequences:
  - <<OPTIONAL>>
