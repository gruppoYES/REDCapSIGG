# L'account

Gli account sono strettamente personali e identificati da uno **username** scelto dall’amministratore (solitamente nel formato `nome.cognome`). Solo l'amministratore del sistema può creare nuovi account all'interno della piattaforma. Tutte le azioni svolte all'interno di un progetto vengono automaticamente registrate da **REDCap SIGG** (in ottemperanza con la normativa vigente) e associate al relativo account. È fortemente sconsigliato condividere le proprie credenziali con altre persone.

---

## Sicurezza

- Gli account sono protetti da **password** (non nota all’amministratore). La validità della password è di 90 giorni.
- È attiva un’**autenticazione a due fattori** (*two-factor authentication*).

Dopo 90 giorni, la piattaforma richiede la modifica della password. L’autenticazione a due fattori garantisce una maggiore sicurezza nell’accesso, tramite l’inserimento di un **codice numerico temporaneo**. L’utente può scegliere, ad ogni login, se ricevere il codice temporaneo via **email** (quella indicata in fase di registrazione) o generarlo tramite l’app *Microsoft Authenticator*.  
<a href="https://support.microsoft.com/it-it/account-billing/come-aggiungere-gli-account-a-microsoft-authenticator-92544b53-7706-4581-a142-30344a2a2a57" target="_blank">Qui</a> è disponibile una guida per impostare Microsoft Authenticator sul proprio cellulare.

La piattaforma prevede politiche di **sospensione automatica** degli account:  
- Ogni account ha una durata predefinita di un anno dalla creazione.
- Gli account inattivi per lunghi periodi possono essere sospesi.  
  In tal caso, la piattaforma invia un’email di avviso.  
- La riattivazione può essere richiesta contattando l’amministratore (per il PI) o tramite il PI (per i collaboratori), mantenendo i privilegi precedenti.

---

### Reset della password

La richiesta di reset della password può essere effettuata in autonomia dalla **pagina principale di REDCap SIGG**, cliccando su *Forgot your password?*. L’amministratore non ha la possibilità di conoscere o inviare la password all’utente.

<p align="center">
  <img src="images/recupero_pdw.png" alt="recupero password" style="width:75%;">
</p>

---

## Creazione degli account  

- L’account del **PI**, con pieni privilegi sul progetto, viene creato contestualmente all’attivazione del progetto.  
- Gli account dei **collaboratori** (ad esempio *data collector*, *manager*, *designer*) vengono creati solo su richiesta formale via email da parte del PI.

Se sono necessari numerosi account per i collaboratori, l’amministratore della piattaforma può richiedere la compilazione di un form dedicato per semplificare il caricamento e la gestione. È possibile scaricarlo <a href="files/UserImportTemplate.zip" target="_blank">qui</a>.

---

### Gli account dei collaboratori (sponsorizzazione)

Gli account dei collaboratori sono **associati al PI**, che assume il ruolo di *sponsor*. La sponsorizzazione permette al PI di gestire in autonomia gli account dei propri collaboratori.

Il PI può accedere alla gestione degli account sponsorizzati dalla pagina principale di **REDCap SIGG**, dopo il login, cliccando su *Sponsor Dashboard* (in verde nell'immagine sotto).

<p align="center">
  <img src="images/sponsor_accesso.png" alt="sponsor accesso" style="width:75%;">
</p>

Dalla *Sponsor Dashboard*, il PI può:
- richiedere il reset della password,
- estendere il periodo di validità dell’account,
- riattivare o sospendere gli account.

<p align="center">
  <img src="images/sponsor_dashboard.png" alt="sponsor dashboard" style="width:75%;">
</p>

Per includere un collaboratore nel progetto, il PI deve:
1. Accedere al progetto.
2. Dalla pagina iniziale del progetto, cliccare su **User Rights** (freccia rossa).
3. Inserire lo **username** del collaboratore sotto *Add new users* (freccia blu).

<p align="center">
  <img src="images/add_user.png" alt="adding user" style="width:75%;">
</p>

---

## I privilegi

Gli account in **REDCap SIGG** sono caratterizzati da **privilegi di accesso** di diverso livello.  
Il PI è responsabile dell’assegnazione dei privilegi agli account di cui è sponsor, garantendo sempre il **principio del privilegio minimo** (solo i permessi strettamente necessari).

Guide dettagliate (in inglese) sui privilegi di REDCap sono disponibili <a href="https://kb.wisc.edu/smph/informatics/page.php?id=96752" target="_blank">qui</a>  e <a href="https://ws.engr.illinois.edu/sitemanager/getfile.asp?id=1359" target="_blank">qui</a>.

---

### Privilegi personalizzabili in REDCap SIGG

- **Privilegi di alto livello:**  
  - **Project Design and Setup:** modifica delle impostazioni di progetto (es. disegno longitudinale), creazione/modifica/cancellazione degli strumenti di raccolta dati, cambio stato (sviluppo, produzione, archiviazione).
  - **User Rights:** gestione degli account (aggiunta utenti e modifica dei privilegi).
  - **Data Access Group:** creazione e modifica dei DAG (vedi sezione dedicata).

- **Altri privilegi:** gestione di strumenti aggiuntivi come calendario, report, API, regole di qualità dei dati.

- **Privilegi sui record (tipicamente corrispondenti a un partecipante):**  
  - **Create Records:** inserire nuovi dati nel database (fondamentale per i *data collector*).  
  - **Rename Records:** modificare l’ID di un record già inserito.  
  - **Delete Records:** eliminare record già inseriti.

- **Privilegi di "locking":** permettono di bloccare la modifica/cancellazione di specifici record da parte di utenti senza questo privilegio.

- **Privilegi di visualizzazione/esportazione:** configurano la possibilità di vedere o scaricare i dati contenuti nei form del progetto.

---

## Ruoli e assegnazione dei privilegi

Per semplificare la gestione degli accessi, REDCap consente la **creazione di ruoli predefiniti** (roles), ciascuno con un set di privilegi già configurato.  
Il PI può assegnare un ruolo agli utenti invece di selezionare manualmente ogni privilegio, garantendo coerenza e velocità nella gestione.

### Esempi di ruoli

- **CRF Designer**  
  - *Project Design and Setup:* **abilitato** (può creare e modificare i form).  
  - *User Rights:* **non abilitato** (non può gestire altri account).  
  - *Create Records:* opzionale (a seconda delle necessità).  
  - Privilegi su export/report: solo se deve testare i dati.  
  Questo ruolo è tipico di chi si occupa di progettare il **Case Report Form** (CRF).

- **Data Collector**  
  - *Create Records:* **abilitato** (può inserire nuovi dati).  
  - *Rename Records* e *Delete Records:* **disabilitati** (per evitare cancellazioni/modifiche accidentali).  
  - Privilegi di export: generalmente **non concessi**.  
  Questo ruolo è pensato per chi raccoglie dati in campo o in studi clinici.

L’uso dei ruoli consente al PI di **assegnare rapidamente privilegi standardizzati** ai vari collaboratori, riducendo il rischio di errori di configurazione.
