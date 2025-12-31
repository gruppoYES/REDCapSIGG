---
title: Impostazione generale di REDCap SIGG
nav_order: 3
---

# Impostazione generale di REDCap SIGG

In REDCap SIGG (ricerca.sigg.it/redcap), ogni studio corrisponde ad un
progetto. Ciascun progetto è slegato rispetto agli altri: i dati sono
mantenuti separati (per quanto caricati sul medesimo server) e solo gli
utenti con autorizzazioni rilasciate dall'amministratore del sistema o
dal PI hanno accesso al progetto (con gradi, all'interno, di autonomia
variabili). Ogni progetto è caratterizzato da un nome e da un *Project ID*
(*PID*) numerico che permette l'identificazione. Un utente può avere
accesso, con ruoli anche diversi, a più progetti.

Il progetto può passare tra diverse fasi che definiscono l'operatività
del progetto. In particolare:

-   La fase di sviluppo (*development*) è quella dedicata alla
    preparazione dello studio (es. disegno eCRF e suo testing estensivo,
    creazione dei ruoli utente, dei *Data Access Group* etc). In questa
    fase, le modifiche al progetto sono semplici e immediate. E'
    consigliabile mantenere il progetto in questa fase fino a che non si
    è conclusa la fase di test e il progetto non è pronto per la fase
    successiva. In questa fase, per contro, è sconsigliato inserire dati
    di partecipanti reali allo studio.

-   La fase di produzione (*production)* è quella pensata per l'attuale
    implementazione della eCRF sul campo e per la raccolta dati. In
    questa fase, le modifiche a eCRF o ad altri aspetti del progetto
    sono molto più laboriose: richiedono -- solitamente -- un passaggio
    in una fase di *draft* (nella quale le modifiche vengono registrate
    ma non implementate) e una sottomissione delle modifiche
    all'amministratore di sistema. Le modifiche minori vengono
    solitamente accettate automaticamente, mentre le altre -- specie se
    potenzialmente possono modificare la struttura dei dati già
    registrati.

-   Chiusura del progetto: il progetto non è più raggiungibile e
    modificabile. I dati, però, rimangono salvati sul database finché il
    progetto non viene attivamente cancellato. Ha la funzione di
    "archivio".

Il *Principal Investigator* (o una persona da lui incaricata -ad
esempio un data manager) ha il compito di gestire il progetto e le
utenze. In particolare, è bene ricordare che:

-   Alla creazione del progetto, da parte dell'amministratore della
    piattaforma, l'unico account con il diritto di accesso sarà quello
    del PI;

-   Il PI può sempre segnalare la necessità di creazione di nuove
    utenze. L'amministratore della piattaforma crea gli account nel
    minor tempo possibile. In generale, è fortemente consigliato che
    ogni persona che ha accesso al progetto abbia un account personale.
    Inoltre, REDCap SIGG implementa un sistema di Multi-Factor
    Authentication (MFA) che richiede l'utilizzo di un secondo device
    (ad esempio, cellulare) o l'accesso all'email personale per
    effettuare l'accesso alla piattaforma;

-   Una volta create le utenze, sarà cura del PI introdurle all'interno
    del progetto di interesse, dotandole dei privilegi necessari per
    svolgere le azioni previste;

-   Il PI verrà indicato come "sponsor" delle utenze: avrà quindi la
    possibilità di sospendere o revocare la sospensione degli account,
    nonché estenderne la durata.
