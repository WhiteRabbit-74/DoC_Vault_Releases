<div align="center">
  <img src="https://via.placeholder.com/150/4f46e5/ffffff?text=DocVault+Logo" alt="DocVault Logo" width="120" />

  # DocVault™ – Release Ufficiali & Aggiornamenti
  
  **Document Management System Enterprise con Intelligenza Artificiale On-Premise**
  
  [![Release](https://img.shields.io/github/v/release/WhiteRabbit-74/DoC_Vault_Releases?style=for-the-badge&color=4f46e5)](https://github.com/WhiteRabbit-74/DoC_Vault_Releases/releases)
  [![Platform](https://img.shields.io/badge/Platform-Windows%2010%2B-blue?style=for-the-badge&logo=windows)](https://github.com/WhiteRabbit-74/DoC_Vault_Releases/releases)
  [![Security](https://img.shields.io/badge/Security-Local--First-success?style=for-the-badge)](#)
</div>

---

## 🔒 Sicurezza e Trasparenza (Architettura Local-First)

Benvenuti nel canale di distribuzione ufficiale di **DocVault**. 
In conformità con i più rigidi standard di sicurezza aziendale (GDPR e privacy del dato), **DocVault è un software 100% Local-First**.

Ciò significa che il codice sorgente del motore AI e le logiche crittografiche risiedono in una repository privata e sigillata, inaccessibile dall'esterno. Questo spazio pubblico è dedicato **esclusivamente** alla distribuzione trasparente degli eseguibili finali (OTA Updates) e all'audit delle versioni.

I vostri documenti non lasceranno **mai** il perimetro del vostro ufficio.

---

## 🚀 Come funzionano gli Aggiornamenti (OTA)

Non è necessario scaricare manualmente i file da questa pagina. 
L'applicazione DocVault installata sui vostri server aziendali è dotata di un **motore di Auto-Update silente**.

1. Il demone interno interroga questa repository una volta all'ora.
2. Quando viene rilevata una nuova Release Ufficiale, il pacchetto di aggiornamento viene scaricato in background.
3. Un pop-up discreto vi avviserà all'interno del software.
4. Al successivo riavvio, DocVault applicherà la patch mantenendo **perfettamente intatti** il vostro database SQLite e tutti i documenti archiviati.

---

## 📥 Installazione Manuale (Primo Avvio)

Se siete l'Amministratore di Sistema incaricato della prima installazione:

1. Visitate la sezione **[Releases](../../releases/latest)** sulla destra.
2. Scaricate l'ultimo file eseguibile `DocVault-Setup-vX.Y.Z.exe`.
3. Eseguitelo sulla macchina Windows designata come Server Documentale (Richiesti min. 8GB RAM).
4. Terminato il setup, DocVault si aprirà e vi guiderà nella creazione del primo account `OWNER` dell'azienda.
5. Da quel momento, tutti i dipendenti della vostra rete LAN potranno accedere digitando l'indirizzo IP del server nel loro browser.

---

## 🛡️ Note di Sicurezza per gli Amministratori IT

- **Nessuna dipendenza cloud:** DocVault utilizza un motore Transformer AI ottimizzato (ONNX) che gira localmente sulla CPU/GPU del server.
- **Isolamento Rete:** L'applicazione non richiede l'apertura di porte sul firewall aziendale verso l'esterno, se non per interrogare `api.github.com` (solo protocollo HTTPS, porta 443) al fine di verificare le versioni in questa repository.
- **Cifratura Password:** Tutte le password degli utenti sono crittografate tramite algoritmo **Bcrypt** a 12 round (Salted) e archiviate nel file `docvault.db` locale.

---

<div align="center">
  <p><i>Sviluppato con passione per garantire l'assoluta sovranità sui dati aziendali.</i></p>
  <p>&copy; 2026 DocVault Enterprise. Tutti i diritti riservati.</p>
</div>
