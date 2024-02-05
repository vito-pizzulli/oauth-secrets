# Secrets

## Descrizione
Questo progetto implementa un sistema di autenticazione. L'utente autenticato può inserire un proprio segreto, che verrà salvato a visualizzato nella rispettiva pagina. Può anche inserire un nuovo segreto che andrà a sovrascrivere il precedente. Ogni utente può visualizzare solo il proprio segreto.

## Funzionalità
- Registrazione e autenticazione locale con email e password.
- Autenticazione con Google OAuth 2.0.
- Sessioni utente persistenti anche dopo la chiusura del browser.
- Protezione delle rotte non accessibili agli utenti non autenticati.

## Tecnologie Utilizzate
- Node.js
- Express
- EJS
- postgreSQL
- passport
- dotenv
- session

## Installazione e Avvio Locale
1. Assicurati di avere Node.js installato sul tuo computer.
2. Clona o scarica il repository del progetto sul tuo computer.
3. Naviga nella directory del progetto tramite il terminale.
4. Apri il terminale e digita `npm install` per installare tutte le dipendenze necessarie.
5. Assicurati di avere postgreSQL e pgAdmin installati sul tuo computer.
6. Crea un database postgreSQL e inserisci i dati di connessione nel file `.env` nella cartella del progetto. Puoi usare il file `.env.example` come modello e modificare le variabili d'ambiente.
7. Esegui le query contenute nel file queries.sql con pgAdmin, in modo da creare tutte le tabelle necessarie.
8. Avvia il server locale con il comando `node index.js` o preferibilmente installare nodemon e utilizzare il comando `nodemon index.js`.

## Come Utilizzare
1. Apri il tuo browser e vai all'indirizzo localhost:3000 per utilizzare l'applicazione.
2. Puoi autenticarti al sito in due modi:
    1. Registrandoti con la tua email e scegliendo una password, che poi userai per effettuare il login.
    2. Cliccando su `Sign In with Google` in alto a destra, potrai loggare tramite il tuo account Google.
3. Dopo esserti autenticato, verrai reindirizzato alla pagina nella quale visualizzerai il tuo segreto, oppure un messaggio di default nel caso non l'abbia ancora inserito.
4. Cliccando su `Submit a Secret`, potrai inserire un segreto che andrà a sovrascrivere il precedente nel caso sia presente. Con il pulsante `Submit` potrai confermare e sarai nuovamente reindirizzato alla pagina contenente il segreto aggiornato.
5. Cliccando sul pulsante `Log Out`, verrai disconnesso al tuo account e reindirizzato alla pagina iniziale.

## Variabili d'ambiente
Il progetto utilizza le seguenti variabili d'ambiente, che andranno inserite nel file `.env`:
- `SESSION_SECRET`: una stringa segreta utilizzata per firmare il cookie della sessione.
- `DB_USER`: il nome utente del database.
- `DB_HOST`: l'host del database.
- `DB_NAME`: il nome del database.
- `DB_PASSWORD`: la password del database.
- `DB_PORT`: la porta del database.
- `GOOGLE_CLIENT_ID`: Client ID di Google OAuth 2.0.
- `GOOGLE_CLIENT_SECRET`: Client Secret di Google OAuth 2.0.
