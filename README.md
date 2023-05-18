Esercizio: Vite Breaking Bad

Nome Repo: vite-breaking-bad

Descrizione - Parte 1:
Creare un nuovo progetto utilizzando Vite e Vue 3 e definite i componenti necessari per strutturare il layout come da screenshot allegato.
Al caricamento della pagina, effettuare una chiama ajax all'API di Yu-Gi-Oh!:
https://ygoprodeck.com/api-guide/
e con i dati restituiti, stampate una card per ogni personaggio.

Bonus:
Creare un componente loader da visualizzare fintantoché i risultati non sono pronti.

Descrizione - Parte 2:
Aggiungere una select per filtrare i risultati in base alla proprietà archetype.
Quando l'utente seleziona un valore dalla lista, viene effettuata una chiamata alle API con l'archetype selezionato.

Milestone 1:
Recuperare tramite chiamata API tutti gli archetype richiamando l'endpoint https://db.ygoprodeck.com/api/v7/archetypes.php e salvare i risultati. Utilizzare i dati salvati per riempire la select che servirà per filtrare i dati

Milestone 2:
Implementare la logica di filtraggio dei risultati delle carte: al cambio del valore della select, effettuare una nuova chiamata API per ottenere una nuova lista di carte

Bonus:
Creare un componente che mostri il numero totale di risultati ottenuti.

Nota:
Per capire come comunicare alle API l'archetype di cui volete vedere le carte, è necessario fare riferimento alla documentazione che trovate qui: https://ygoprodeck.com/api-guide/

 <h1 align="center">Anteprima<h1>
<div align="center"><img src="Traccia Esercizio - Parte 1.png" width="800">
