# Piano di Sviluppo - App Gestione Torneo Burraco

## File da Creare/Modificare

### 1. src/pages/Index.tsx
- Pagina principale con navigazione tra le sezioni
- Layout con tabs per: Partecipanti, Sorteggio, Premiazione

### 2. src/components/ParticipantsManager.tsx
- Form per aggiungere partecipanti manualmente
- Upload file (Excel, ODS, CSV)
- Tabella con lista partecipanti
- Funzioni per eliminare/modificare partecipanti

### 3. src/components/DrawManager.tsx
- Bottone per eseguire il sorteggio
- Visualizzazione accoppiamenti sorteggiati
- Salvataggio risultati sorteggio

### 4. src/components/PrizesManager.tsx
- Form per assegnare i premi ai partecipanti
- Selezione vincitori per:
  - 1° Premio
  - 2° Premio
  - 3° Premio
  - 4° Premio
  - 5° Premio
  - Premio Tecnico
- Visualizzazione classifica finale

### 5. src/lib/fileParser.ts
- Funzioni per parsare file Excel (.xlsx)
- Funzioni per parsare file ODS
- Funzioni per parsare file CSV
- Validazione dati importati

### 6. src/lib/tournamentLogic.ts
- Logica per il sorteggio casuale
- Gestione stato torneo
- Utility functions

### 7. index.html
- Aggiornare il titolo della pagina

## Dipendenze da Aggiungere
- xlsx: per parsing file Excel
- papaparse: per parsing file CSV

## Ordine di Implementazione
1. Aggiornare index.html con titolo appropriato
2. Creare fileParser.ts per gestione file
3. Creare tournamentLogic.ts per logica sorteggio
4. Creare ParticipantsManager.tsx
5. Creare DrawManager.tsx
6. Creare PrizesManager.tsx
7. Aggiornare Index.tsx con layout completo
8. Test e lint finale