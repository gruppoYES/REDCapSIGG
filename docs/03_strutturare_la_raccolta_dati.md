---
title: Strutturare la raccolta dati
nav_order: 4
---

# Strutturare la raccolta dati

In REDCap, la raccolta dei dati può avvenire attraverso due modalità
principali:

-   Moduli di electronic Case Report Form (eCRF), che richiedono che
    l'utente incaricato dell'inserimento dei dati effettui l'accesso
    (login) alla piattaforma.

-   Survey, ovvero moduli accessibili tramite un collegamento web, che
    non richiedono necessariamente che il compilatore sia autenticato in
    REDCap SIGG.

La scelta tra eCRF e survey (o l'utilizzo combinato di entrambe) dipende
dal disegno dello studio, dal profilo dei compilatori e dai requisiti di
sicurezza e tracciabilità dei dati.

## Disegnare la eCRF

La progettazione e la strutturazione della eCRF avvengono tramite il
menu "*Designer*", accessibile dalla barra laterale sinistra della
piattaforma. Il Principal Investigator ha sempre accesso a questa
sezione; gli altri utenti inseriti nel progetto devono invece essere
esplicitamente autorizzati dal PI. È fortemente consigliato limitare
l'accesso al *Designer* a un numero ristretto e selezionato di utenti, al
fine di ridurre il rischio di modifiche involontarie o non controllate
alla struttura della raccolta dati.

All'interno della pagina *Designer* è possibile creare e modificare le
form. Da un punto di vista teorico, l'intera raccolta dati di uno studio
potrebbe essere concentrata in una singola form; tuttavia, è
generalmente preferibile suddividere la raccolta in più form, poiché
questo approccio offre diversi vantaggi:

-   consente di suddividere la raccolta dati in segmenti logici,
    facilitando il lavoro dei data collector, che possono operare in
    momenti diversi;

-   permette di creare form ripetibili (come descritto nelle sezioni
    successive), utilizzabili in più occasioni dello studio. Ad esempio,
    se una valutazione funzionale tramite Barthel Index è prevista sia
    al baseline sia al follow-up, è consigliabile costruire un'unica
    form contenente il Barthel Index e renderla ripetibile, anziché
    creare form distinte per ciascun time point.

Ogni form è costituita da uno o più campi che consentono l'inserimento
dei dati. L'unico campo sempre presente e precompilato è il record_id,
che rappresenta l'identificativo univoco di ciascun record del database
(nella maggior parte dei casi corrispondente al singolo partecipante
allo studio) ed è assegnato automaticamente da REDCap SIGG.

Gli altri campi possono essere configurati con diverse tipologie di
risposta, tra cui:

-   testo libero;

-   risposta chiusa (tramite pulsanti radio o menu a tendina);

-   risposta multipla (check box);

-   scale di tipo Likert.

I campi a testo libero possono essere associati a regole di validazione
dei dati (*data validation*), che consentono di restringere il formato
delle risposte ammissibili. Le validazioni possono basarsi sul tipo di
dato (ad esempio solo lettere, solo numeri interi, data in formato
europeo o statunitense) oppure su un intervallo di valori
minimo--massimo.

In REDCap SIGG è inoltre possibile collegare alcuni campi di testo
libero a BioPortal, un portale che mette a disposizione numerose
classificazioni ufficiali utilizzabili nella raccolta dati. Ad esempio,
è possibile associare un campo alla classificazione ATC dei farmaci,
consentendo al data collector di ricercare il principio attivo (in
lingua inglese) e di memorizzarne automaticamente il codice nel
database. In modo analogo, è possibile utilizzare codifiche standard
come ICD-9 o ICD-10 per le diagnosi.

All'interno della eCRF possono inoltre essere definite matrici di
risposte, che permettono di applicare lo stesso schema di risposta
(tipicamente a scelta chiusa) a più domande correlate. Questo approccio
semplifica sia la costruzione della eCRF sia la fase di inserimento dei
dati.

Infine, l'utilizzo delle branching logics consente di mostrare al data
collector determinate domande solo quando viene fornita una specifica
risposta a una domanda precedente. Le condizioni possono fare
riferimento a campi presenti nella stessa form, in altre form dello
stesso progetto o, in alcuni casi, a informazioni già registrate nel
database. Questo strumento permette di rendere la raccolta dati più
efficiente, riducendo il numero di campi non pertinenti visualizzati e
migliorando la qualità complessiva dei dati raccolti.

Ogni variabile può essere poi flaggata come "obbligatoria" -- in questo
caso il sistema darà errore nel caso in cui il data collector chiuda la
raccolta dati senza aver fornito una risposta - o come "identifier". In
questo caso, la risposta verrà di norma censura nell'export dei dati. E'

bene tenere a mente che per quanto l'identifier aiuti a mantenere
l'anonimizzazione del dato, non è un'opzione che permette di crittare la
risposta all'interno del database. A prescindere quindi dall'utilizzo di
questa opzione, si rimanda il PI alla vigente normativa circa la
raccolta dei dati identificativi negli studi di ricerca scientifica.

Nella pagina di *project setup* è possibile attivare gli strumenti
ripetuti e/o attivare il disegno longitudinale di studio. In
quest'ultimo caso, sarà necessario formalizzare degli eventi di studio
(ad es, baseline, primo follow-up, follow-up 12 mesi etc), mentre nel
primo questo passaggio non è richiesto. Una volta costruiti le form,
sarà possibile -- mentre il Progetto si trova ancora in fase di disegno,
identificare quali form sono ripetibili o quali form vengono riproposte
nei diversi eventi programmati.

Si rimanda alla guida interna sulle smart variables per comprendere
l'utilizzo della branching logic nel momento in cui siano presenti più
eventi o lo strumento sia ripetibile.

## Disegnare una survey

Dal pannello di *Project Setup*, selezionando *Main Project Settings*, è
possibile abilitare l'utilizzo delle survey all'interno del progetto. È
importante sottolineare che non tutte le form di un progetto devono
necessariamente essere configurate come survey; tuttavia, nella maggior
parte dei casi viene creata una singola form specificamente destinata a
questo scopo.

Una volta attivata la funzionalità survey, è possibile creare la
relativa form tramite lo strumento *Designer*, seguendo modalità analoghe
a quelle descritte per la progettazione delle eCRF. In aggiunta,
all'interno della pagina *Designer* diventano disponibili le
survey-related options, che consentono di personalizzare la survey (ad
esempio nei testi introduttivi o di chiusura) e l'opzione per
automatizzare l'invio, sfruttando liste di indirizzi email già presenti
nel sistema. E' bene però ricordare che nella maggior parte dei casi, la
survey risulta uno strumento utile perché liberamente accessibile via
web: per questo scopo, è possibile utilizzare il menu Survey
Distribution Tools (accessibile dalla barra laterale sinistra, nella
sezione *Data Collection*). Da qui è possibile generare un link automatico
e permanente alla survey, che potrà essere distribuito attraverso i
canali di comunicazione ritenuti più appropriati (ad esempio email, siti
web o altri strumenti informativi).
