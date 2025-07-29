# Introduzione
*REDCap* (Research Electronic Data Capture) è un sistema web based di raccolta dati sviluppato dalla Vanderbilt University per supportare la ricerca clinica e traslazionale. Permette di costruire database e sondaggi in modo flessibile, mantenendo elevati standard di sicurezza e integrità dei dati.  La piattaforma è utilizzata da oltre 7 000 centri e permette la collaborazione tra team multidisciplinari.  REDCap offre un flusso di lavoro completo: dalla progettazione del questionario alla raccolta e gestione dei dati, fino all’analisi statistica, con la possibilità di esportare i dati in formati compatibili con Excel, SAS, SPSS, R e Stata.

## Struttura generale di REDCap

**REDCap** è composto da una **facciata web**, accessibile via Internet, sulla quale l’utente lavora direttamente, e da una **componente database**, non direttamente accessibile, nella quale vengono memorizzati i dati caricati.  

Ciascun progetto di ricerca, identificato da un **Project Identification (PID) number**, è separato dagli altri:  
- Solo gli account con privilegio di accesso a uno specifico PID possono visualizzarne i contenuti.  
- In base ai privilegi, alcuni account possono inserire dati, modificarli o scaricarli.  
- Un singolo account può avere accesso a più PID (ad esempio un *data collector* che lavora su più studi o un PI che gestisce diversi progetti).
- Tutte le azioni svolte all'interno del progetto vengono registrate (*logging*) automaticamente, in linea con la normativa vigente 





