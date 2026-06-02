<div align="center">
  <h1>DocVault™ – Release Ufficiali & Aggiornamenti</h1>
  
  <p><b>Document Management System Enterprise Local-First con Intelligenza Artificiale On-Premise</b></p>
  
  <p>
    🛡️ <b>Sicurezza:</b> Local-First &amp; GDPR Compliant | 
    💻 <b>Piattaforma:</b> Windows 10+ (min. 8GB RAM) | 
    🚀 <b>Rilascio:</b> OTA &amp; Offline Installer
  </p>
</div>

---

## 🔒 Sicurezza e Sovranità del Dato (Architettura Local-First)

Benvenuti nel canale di distribuzione ufficiale di **DocVault**. 
In conformità con le più severe normative in materia di privacy e GDPR per le PMI italiane, **DocVault opera interamente offline ed è ad architettura Local-First**.

Il codice sorgente del nucleo applicativo e le logiche di business risiedono in una repository privata e sicura. Questa repository pubblica è adibita **esclusivamente** al download degli eseguibili compilati per l'installazione e dei pacchetti OTA per l'aggiornamento.

I vostri documenti aziendali non transitano **mai** su server esterni o nel cloud: rimangono integralmente all'interno del vostro server locale e della vostra rete LAN.

---

## 🧠 Intelligenza Artificiale Locale & Semantic Search On-Premise

DocVault integra avanzate capacità di analisi ed estrazione dati basate su IA eseguiti direttamente sul vostro hardware locale, senza costi di API cloud e con privacy garantita:
* **Analisi e Classificazione Locale**: Motore Transformer ONNX locale che analizza il testo dei documenti estratti per suggerire categorie, titoli e date di scadenza critiche.
* **Ricerca Semantica Offline**: Generazione locale di vettori/embeddings in memoria (modello `multilingual-e5-small`) per consentire ricerche intelligenti in base al significato dei documenti, anche in presenza di sinonimi o query in linguaggio naturale.
* **Indicizzazione Full-Text (FTS5)**: Ricerca ultra-veloce tramite motore SQLite FTS5 integrato e sanitizzazione preventiva degli input per la massima sicurezza da SQL Injection.

---

## 🔄 Gestione Sicura degli Aggiornamenti (OTA Updates)

Gli aggiornamenti software in DocVault sono progettati per essere sicuri, trasparenti e sotto il controllo totale degli amministratori IT:
1. **Rilevamento su Richiesta**: Nessun processo silente in background o demone effettua chiamate esterne continue. Il controllo delle versioni viene eseguito esclusivamente quando il Super Amministratore accede alla pagina **Impostazioni di Sistema > Aggiornamenti** dell'interfaccia locale di DocVault.
2. **Download del Pacchetto**: Se è disponibile una nuova release, il sistema scaricherà in locale l'archivio `update.zip` direttamente dalle release pubbliche di questa repository.
3. **Backup Automatico Preventivo**: Prima di applicare qualsiasi patch, DocVault esegue una copia fisica immediata del database SQLite `docvault.db` e del file `config.json` in una directory temporanea di sicurezza.
4. **Hot-Swap della Logica**: Lo script di aggiornamento installa le nuove dipendenze e sovrascrive esclusivamente i file logici compilati. I vostri documenti archiviati e i dati del database SQLite rimangono perfettamente intatti e protetti.

---

## 📥 Guida all'Installazione

1. Accedi alla sezione **[Releases](../../releases/latest)** di questa repository.
2. Scarica il file eseguibile `DocVault-Setup-vX.Y.Z.exe` per Windows.
3. Avvia l'installer sulla macchina Windows designata come server documentale dell'organizzazione (requisiti consigliati: min. 8GB RAM).
4. Al termine del setup guidato di onboarding, crea il primo account aziendale con ruolo `OWNER`.
5. La piattaforma sarà accessibile a tutti i dipendenti all'interno della rete aziendale LAN tramite l'indirizzo IP locale della macchina server (es. `http://192.168.1.100:3000`).

---

## 🛡️ Standard di Sicurezza IT
* **Connessioni Esterne**: L'unica connessione internet richiesta (porta 443, protocollo HTTPS) è quella effettuata dal server locale verso l'endpoint `api.github.com` per verificare la presenza di release in questo archivio.
* **Isolamento Organizzazioni**: Architettura predisposta per l'isolamento multi-tenant dei dati tramite controlli logici rigorosi (`organizationId`).
* **Controllo Clearance**: Accesso ai documenti protetto da clearance granulare a 5 livelli di riservatezza, verificato a livello server su ogni singola richiesta.
* **Cifratura**: Tutte le password degli utenti sono crittografate localmente mediante algoritmo Bcrypt con 12 round di salatura.

---

<div align="center">
  <p><i>Garantire l'assoluta sovranità e riservatezza del patrimonio informativo aziendale.</i></p>
  <p>&copy; 2026 DocVault Enterprise. Tutti i diritti riservati.</p>
</div>
