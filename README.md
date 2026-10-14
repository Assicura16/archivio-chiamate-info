# Archivio chiamate backup — pagine informative

Sito statico per la configurazione OAuth Google del progetto privato Assicura Cars.

## Contenuto pubblico

- `index.html`: descrizione e stato del progetto.
- `privacy.html`: informativa sul collegamento Drive e su GitHub Pages.
- `termini.html`: condizioni d’uso.
- `styles.css`: stile condiviso, senza risorse esterne.
- `.nojekyll`: disattiva l’elaborazione Jekyll.

Il pacchetto non contiene registrazioni, database, credenziali OAuth o configurazioni del VPS.
La pubblicazione del sito non attiva i backup. Il contatto è l’email di assistenza
già selezionata nella configurazione OAuth Google; verificarla prima della pubblicazione.

## Pubblicazione gratuita prevista

1. Creare sotto `Assicura16` il repository pubblico `archivio-chiamate-info`.
2. Estrarre il pacchetto e caricare i file nella radice del repository, non lo ZIP.
3. In `Settings` → `Pages`, scegliere `Deploy from a branch`, ramo `main`, cartella `/(root)` e `Save`.
4. Attendere la distribuzione; verificare che homepage, privacy e condizioni siano accessibili senza login.

URL attesi dopo pubblicazione (non ancora attivati da questo pacchetto):

- Homepage: https://assicura16.github.io/archivio-chiamate-info/
- Privacy: https://assicura16.github.io/archivio-chiamate-info/privacy.html
- Condizioni: https://assicura16.github.io/archivio-chiamate-info/termini.html

Dominio autorizzato Google: `assicura16.github.io` (senza https o percorso).
Inserire i link in Branding soltanto dopo aver verificato le pagine online.
Se Google richiede una verifica di proprietà, seguire la relativa procedura in Search Console.

## Completamento Google OAuth

In `Accesso ai dati` dichiarare soltanto `https://www.googleapis.com/auth/drive.file`
per il collegamento previsto. Lo stesso scope dovrà essere usato da rclone.
Completare Branding, poi portare l’app in produzione da Pubblico e soltanto dopo
autorizzare il server. Rimanere in Test comporta la scadenza settimanale delle autorizzazioni Drive.
Non caricare il file client_secret*.json in questo repository pubblico.

## Dopo l’attivazione

Aggiornare la nota di configurazione solo dopo un backup e un ripristino verificati.
Allineare l’informativa alle effettive impostazioni di conservazione e di sicurezza.
L’informativa dell’integrazione non sostituisce quella per la registrazione delle telefonate.

## Riferimenti tecnici

- https://rclone.org/drive/#making-your-own-client-id
- https://support.google.com/cloud/answer/15549049
- https://developers.google.com/workspace/drive/api/guides/api-specific-auth
- https://developers.google.com/terms/api-services-user-data-policy
- https://docs.github.com/en/pages/getting-started-with-github-pages/creating-a-github-pages-site
- https://docs.github.com/en/pages/getting-started-with-github-pages/what-is-github-pages

Verificati il 14 ottobre 2026.
