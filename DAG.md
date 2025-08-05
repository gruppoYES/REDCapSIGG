# Data Access Groups (DAG)

I **Data Access Groups** (DAG) sono uno strumento fondamentale in REDCap per garantire la riservatezza dei dati nei progetti multi-centro o in cui più gruppi di lavoro raccolgono dati in modo indipendente.  
Attraverso i DAG, è possibile limitare la visibilità dei record agli utenti di uno specifico gruppo, evitando che visualizzino dati inseriti da altri gruppi.

---

## A cosa servono i DAG

I DAG permettono di **segmentare i dati raccolti** tra diversi gruppi di utenti. Ogni utente assegnato a un DAG potrà:
- vedere **solo i record creati dal proprio gruppo**,
- creare nuovi record che saranno automaticamente associati al proprio DAG,
- non avere accesso ai dati inseriti da altri gruppi.

Questa impostazione è particolarmente utile in scenari come:

- **Progetti multicentrici:** ogni centro clinico può accedere solo ai propri dati.
- **Raccolta dati distribuita:** ad esempio, operatori territoriali o strutture diverse coinvolte in uno stesso studio.
- **Collaborazioni interistituzionali:** per separare i dati tra enti o team, pur mantenendo un'unica piattaforma.

> ⚠ Gli utenti **non assegnati ad alcun DAG** (tipicamente il PI e il data manager centrale) possono visualizzare **tutti i record**.

---

## Come si creano e gestiscono i DAG

Per gestire i DAG in un progetto REDCap è necessario avere il privilegio **Data Access Groups**.

Dalla schermata iniziale del progetto, dopo il login, è possibile:
1. Cliccare su **Data Access Groups** nel menu laterale.
2. Creare nuovi DAG, assegnando un nome identificativo (es. "Centro 1", "Ospedale A").
3. Visualizzare e gestire l'elenco degli utenti assegnati a ciascun DAG.

<p align="center">
  <img src="images/dag_creazione.png" alt="Creazione DAG" style="width:75%;">
</p>

---

### Assegnazione degli utenti ai DAG

L’assegnazione di un utente a un DAG può essere effettuata:
- manualmente, dalla pagina **User Rights** del progetto,
- automaticamente, tramite lo script di importazione utenti (vedi sezione creazione account),
- oppure direttamente tramite la **Sponsor Dashboard** se lo sponsor ha questo privilegio.

Per ogni utente si può selezionare il DAG desiderato dal menu a tendina.

<p align="center">
  <img src="images/dag_user_assignment.png" alt="Assegnazione DAG all’utente" style="width:75%;">
</p>

---

## Considerazioni importanti

- I DAG **non sono retroattivi**: se un utente viene assegnato a un DAG dopo aver inserito dei record, questi rimangono visibili globalmente.
- È possibile attivare l’**etichetta DAG** nei nomi dei record per facilitarne l’identificazione.
- Gli utenti **possono essere assegnati a un solo DAG alla volta**.
- È possibile esportare i dati **inclusi o esclusi i DAG**, a seconda del livello di accesso.

---

## Esempio di utilizzo

Supponiamo uno studio multicentrico su pazienti fragili, condotto in:
- **Ospedale A**
- **Ospedale B**
- **Ambulatorio territoriale**

Ogni sede ha un proprio team di raccolta dati. Grazie ai DAG:
- I ricercatori dell’Ospedale A vedranno solo i dati dei propri pazienti.
- Il PI, non assegnato a nessun DAG, avrà visibilità completa su tutti i centri.
- I dati rimarranno compartimentalizzati fino all’analisi finale.

---

## Collegamenti utili

Per maggiori dettagli, è possibile consultare:  
<a href="https://redcap.vanderbilt.edu/consortium/vuguides/dag_user_guide.pdf" target="_blank">Guida ufficiale REDCap sui DAG (PDF)</a>
