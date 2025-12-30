---
title: Gestione degli utenti e dei privilegi di accesso
nav_order: 5
---

# Gestione degli utenti e dei privilegi di accesso

Gli account delle persone che partecipano al progetto (ad esempio data
collector, project manager, data manager) possono essere gestiti tramite
il menu *User Rights*, accessibile dalla barra laterale sinistra. Da
questa sezione è possibile aggiungere utenti già presenti nel sistema
REDCap SIGG al progetto, assegnando loro privilegi personalizzati,
oppure applicare ruoli predefiniti.

È importante ricordare che possono essere aggiunti al progetto
esclusivamente account già esistenti nella piattaforma REDCap SIGG.
Qualora sia necessario creare nuovi account, il Principal Investigator
deve contattare l'amministratore di sistema.

## Utilizzo dei ruoli

Si raccomanda fortemente di utilizzare i ruoli per l'assegnazione dei
privilegi, soprattutto nei progetti con un numero elevato di
collaboratori. L'uso dei ruoli consente una gestione più coerente,
sicura e facilmente modificabile delle autorizzazioni. I ruoli possono
essere definiti nella stessa pagina *User Rights*, nella sezione Create
new roles. È necessario assegnare a ciascun ruolo un nome identificativo
(ad esempio Data Collector) e selezionare successivamente i privilegi
associati tramite l'apposita schermata.

## I privilegi

Privilegi di livello più elevato:

-   Nella sezione Highest level privileges sono presenti i privilegi
    relativi a Project Design e *User Rights*. Gli utenti in possesso di
    tali autorizzazioni possono modificare in modo significativo la
    struttura del progetto e gestire completamente gli accessi degli
    altri utenti. Per questo motivo, si raccomanda di riservare questi
    privilegi esclusivamente all'account del Principal Investigator.

Altri privilegi consentono l'accesso a funzionalità avanzate o di
supporto alla gestione del progetto, come ad esempio:

-   *Survey Distribution Tools*

-   *Calendar*

-   *Alerts & Notifications*

-   *Data Import*

Tali autorizzazioni possono risultare utili per figure come il data
manager, ma in genere non sono necessarie per i data collector. È
inoltre possibile autorizzare un account alla creazione e all'esecuzione
delle regole di *Data Quality*, nonché all'accesso alle *API* di REDCap.

Per quanto riguarda i privilegi relativi alla gestione dei record
(tipicamente necessari ai data collector), si segnalano in particolare:

-   *Create records*: consente la creazione di nuovi record nel database
    (privilegio necessario per la raccolta dati);

-   *Rename records*: consente la modifica dell'identificativo di un
    record esistente (privilegio generalmente sconsigliato per i data
    collector);

-   *Delete records*: consente la cancellazione di record già inseriti
    (privilegio fortemente sconsigliato per i data collector).

La funzionalità di locking dei record (blocco delle modifiche ai dati
già inseriti) è sempre disponibile per l'account del PI. È tuttavia
possibile concedere l'accesso a questa funzione anche ad altri utenti
tramite un apposito privilegio. Anche in questo caso, si raccomanda di
limitare la concessione di tale autorizzazione al minimo indispensabile.

I Data Viewing Rights, visualizzati nella colonna destra della schermata
di configurazione dei ruoli, consentono di definire il livello di
interazione di ciascun ruolo con gli strumenti di raccolta dati:

-   *No access*: l'utente non può visualizzare lo strumento;

-   *Read only*: l'utente può visualizzare lo strumento senza modificarne
    i contenuti;

-   *View & edit*: l'utente può visualizzare e compilare lo strumento
    (impostazione necessaria per la raccolta dati).

-   Il flag *Delete* consente la cancellazione di singoli valori
    all'interno di un record ed è distinto dal privilegio *Delete*
    records, che riguarda invece l'eliminazione dell'intero record dal
    database.

I Data Export Rights regolano la possibilità di esportare e scaricare i
dati presenti nel database. Si raccomanda di mantenere la maggior parte
degli utenti senza accesso a questa funzionalità (*No access*), riservando
al Principal Investigator la possibilità di esportare l'intero dataset
(Full dataset). Anche le altre modalità di esportazione (ad esempio
De-identified o Remove all identifier fields) devono essere utilizzate
con estrema cautela. Il livello effettivo di anonimizzazione dei dati
esportati dipende infatti dal disegno della eCRF e dalla corretta
attribuzione del flag identifier ai campi rilevanti. Inoltre, i dati
esportati, anche se anonimizzati o pseudo-anonimizzati, non devono
essere considerati equivalenti a dati aggregati e devono essere trattati
in conformità alla normativa vigente.

## I *Data Access Group* (DAG)

Dal menu laterale sinistro è possibile accedere alla sezione dedicata ai
*Data Access Group* (DAG). I DAG sono gruppi di utenti che consentono di
limitare l'accesso ai record del database, rendendo visibili agli utenti
solo i dati associati al proprio gruppo di appartenenza. I DAG sono
utilizzati principalmente negli studi multicentrici, nei quali i data
collector di un determinato centro non devono poter visualizzare i
record relativi agli altri centri, ma devono poter creare e consultare
esclusivamente i record dei partecipanti afferenti al proprio centro.

È fortemente consigliato pianificare la struttura e l'assegnazione dei
DAG prima dell'avvio della raccolta dati e dell'apertura del progetto
agli utenti. Modifiche ai DAG effettuate durante una fase attiva di
raccolta dati possono infatti determinare violazioni della separazione
tra i gruppi e generare incongruenze nella struttura del database. Le
informazioni relative all'appartenenza ai DAG vengono infatti
automaticamente incluse nel dataset esportato. Per ciascun DAG, il
Principal Investigator (o un account da lui designato) assegna un nome
descrittivo. REDCap attribuisce automaticamente a ogni DAG anche un nome
breve e un identificativo numerico (ID), che saranno riportati nei file
di esportazione dei dati. Ogni utente può essere associato a un solo
DAG. È tuttavia possibile utilizzare lo strumento *DAG Switcher* per
consentire a un utente di operare su più DAG. In questo caso, è
fondamentale che l'utente selezioni esplicitamente il DAG corretto prima
di procedere all'inserimento dei dati; in caso contrario, il record
verrà associato in modo errato al DAG selezionato al momento della
creazione, con conseguenze sulla visibilità e sull'esportazione dei
dati.

Gli utenti che non sono associati ad alcun DAG hanno accesso a tutti i
record del progetto: questo impone che, in caso venga aggiunto un nuovo
utente ad un progetto già attivato, questo debba essere immediatamente
associato al DAG corretto. In caso contrario, il nuovo account avrà
libero accesso a tutti i record caricati e i record creati tramite
l'account non saranno associati a nessun DAG. Infine, è importante
ricordare che i DAG rappresentano una sovrastruttura rispetto ai
privilegi di accesso, ma non li sostituiscono. Essi devono pertanto
essere utilizzati in modo complementare alla corretta configurazione dei
ruoli e dei privilegi degli utenti.
