# Struttura generale di REDCap

**REDCap** è composto da una **facciata web**, accessibile via Internet, sulla quale l’utente lavora direttamente, e da una **componente database**, non direttamente accessibile, nella quale vengono memorizzati i dati caricati.  

Ciascun progetto di ricerca, identificato da un **Project Identification (PID) number**, è separato dagli altri:  
- Solo gli account con privilegio di accesso a uno specifico PID possono visualizzare i contenuti.  
- In base ai privilegi, possono modificarli o scaricarli.  
- Un singolo account può avere accesso a più PID (ad esempio un *data collector* che lavora su più studi o un PI che gestisce diversi progetti).  
- I PID ai quali l’account non ha accesso non sono nemmeno visualizzati.

---

## Funzionalità del PI (Principal Investigator)

All’interno di ciascun PID, l’account del PI può gestire:  
- Il disegno dei form di raccolta dati.  
- Gli account dei collaboratori.  
- Il download o la visualizzazione dei dati caricati.

---

# Account e privilegi

Gli account sono strettamente personali e identificati da uno **username** scelto dall’amministratore (solitamente nel formato `nome.cognome`).  

### Sicurezza
- Gli account sono protetti da **password** (non nota all’amministratore).  
- È attiva un’**autenticazione a due fattori**: in fase di login, oltre alla password, viene richiesto un **token numerico temporaneo**, inviato via email o generato tramite l’app *Microsoft Authenticator*.

---

## Creazione degli account

- Gli account vengono creati dall’amministratore della piattaforma REDCap SIGG.  
- L’account del **PI**, con pieni privilegi sul progetto, viene creato contemporaneamente all’attivazione del progetto.  
- Gli account dei **collaboratori** (ad esempio *data collector*, *manager*, *designer*) vengono creati solo dopo richiesta formale via email da parte del PI.  

Nella fase iniziale, solo l’account del PI ha accesso al progetto. I collaboratori vengono **associati** al PI tramite una **sponsorizzazione**, che consente al PI di:  
- Includere gli account collaboratori nel progetto.  
- Definirne due caratteristiche fondamentali:  
  - **I privilegi**.  
  - **La partecipazione ai Data Access Groups (DAG)**.

