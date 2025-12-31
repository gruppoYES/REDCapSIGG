---
title: L'esportazione dei dati
nav_order: 6
---

# L'esportazione dei dati

In REDCap l'esportazione dei dati può avvenire principalmente in due
modi:

-   Download del dataset in vari formati (il più comune è il Comma
    Separated Values -- CSV).

-   Accesso tramite *API* (Application Programming Interface) di REDCap.

Nella maggior parte dei casi è consigliabile concludere la raccolta dati
e poi scaricare il dataset. L'opzione è disponibile nel menu laterale:
Applications → *Data Exports, Reports and Stats* → *Export Data*. Nella
schermata di esportazione è possibile scegliere formato del file,
opzioni relative a identifier, formati data, gestione dei campi di testo
libero, e il separatore da usare nel CSV.

È importante ricordare che non tutti i formati consentono di includere
contemporaneamente valori e etichette. In particolare:

-   Un CSV in formato "raw data" contiene il nome della variabile (es.
    `sex`, definito durante la creazione della eCRF) e il codice
    associato alla risposta (es. `1`, `2`).

-   Un CSV in formato "labels" contiene la descrizione della variabile
    (es. "Indicare il sesso del partecipante") e la descrizione delle
    risposte visualizzata dall'utente (es. "Maschio", "Femmina").

Le domande di tipo checkbox (selezione multipla) vengono esportate come
più colonne, una per ciascuna opzione: ogni colonna riporta tipicamente
0 se l'opzione non è stata selezionata e 1 se è stata selezionata.

L'*API*, invece, è una modalità più avanzata che consente l'accesso in
tempo reale ai dati. Può essere utile per analisi in itinere o per
evitare il download manuale del dataset su un dispositivo locale.
L'accesso avviene tramite la generazione di un token ("Create *API* token
now" nella pagina *API* del progetto): solo gli utenti con permessi
adeguati (spesso il PI) possono generarlo. Il token è a tutti gli
effetti una chiave di accesso diretta ai dati del progetto e deve quindi
essere conservato e condiviso con la massima cautela; in ogni momento
può essere revocato. In caso di dubbi, è opportuno contattare
l'amministratore di sistema.

Nella sezione "*API Playground*", dopo la generazione del token, è
possibile ottenere esempi di codice nei principali linguaggi (ad es.
PHP, Python, Ruby, R, C#) per personalizzare l'esportazione e
semplificare l'utilizzo dell'*API*.

Si ricorda di utilizzare sia l'esportazione sia l'accesso via *API* nel
rispetto della normativa vigente e delle procedure locali di gestione e
protezione dei dati.
