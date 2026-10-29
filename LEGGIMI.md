# Lobiz Agency — versione SEO

Versione preparata il 29 ottobre 2026 a partire dall’HTML, CSS e JavaScript allegati. Il sito pubblico non è stato modificato.

## Aprire subito il sito con la grafica

1. Estrai completamente lo ZIP.
2. Apri la cartella `sito`.
3. Fai doppio clic su `index.html`.

Mantieni insieme HTML, CSS, JavaScript e cartella `assets`: non spostare il solo HTML fuori dalla cartella. Grafica, immagini, gallerie e pagine interne funzionano anche con apertura locale.

## Cosa trovi

La cartella `sito` contiene il sito statico completo, senza compilazione e senza dipendenze da installare:

- homepage con la grafica originale, payoff, animazioni e otto gallerie;
- indice dei progetti e dieci pagine progetto;
- quattro pagine servizi, Agenzia e Contatti;
- pagina di errore 404;
- immagini originali e varianti responsive;
- `sitemap.xml`, `robots.txt`, `vercel.json`, favicon e immagine social;
- `seo.css`, dedicato alle aggiunte, e `page.js` per il menu delle pagine interne.

I file principali hanno i nomi corretti per il sito: `index.html`, `styles.css`, `script.js`. Non mantenere le numerazioni dei download come `index(5).html` o `styles(2).css`.

## Pubblicazione nel progetto GitHub / Vercel esistente

1. Conserva il commit attuale come punto di ripristino, oppure lavora in un nuovo branch.
2. Copia **il contenuto della cartella `sito`** nella cartella del repository che contiene l’attuale `index.html`. Non caricare soltanto l’HTML: servono anche le cartelle `progetti`, `servizi`, `agenzia`, `contatti`, gli asset e gli altri file.
3. Se esiste già un `vercel.json`, integra le regole di questo pacchetto preservando le impostazioni necessarie del progetto. Quello incluso è per hosting statico: non contiene un redirect generale di tutte le pagine alla home.
4. In Vercel usa il progetto già collegato al dominio. Per un repository statico senza framework, il preset è **Other**, senza build; la directory pubblicata deve essere quella che contiene il nuovo `index.html`. Evita di pubblicare per errore la cartella superiore con il solo README.
5. Controlla l’anteprima Vercel, quindi pubblica la versione sul dominio esistente.
6. In Domains verifica che `www.lobiz.it` sia il dominio di riferimento. Il `vercel.json` incluso reindirizza `lobiz.it` a `www.lobiz.it`, mantenendo il percorso. Rimuovi un eventuale redirect opposto già configurato nella dashboard: altrimenti creerebbe un ciclo. La configurazione degli URL è stata preparata, ma il redirect reale potrà essere verificato solo dopo il deploy.

Non occorre cambiare provider, ricomprare il dominio o creare un secondo sito pubblico.

## Subito dopo il deploy

Apri questi indirizzi e verifica che siano corretti:

- https://www.lobiz.it/
- https://www.lobiz.it/progetti/
- https://www.lobiz.it/progetti/mini-padel-league/
- https://www.lobiz.it/servizi/eventi-brand-experience/
- https://www.lobiz.it/sitemap.xml
- https://www.lobiz.it/robots.txt

Verifica anche un URL inesistente: deve restituire HTTP 404, non la home con stato 200. Controlla che le pagine interne siano raggiungibili direttamente, anche dopo un aggiornamento del browser.

## Google Search Console

Usa la proprietà dominio già configurata per lobiz.it, oppure verifica la proprietà se manca. Non serve inserire un nuovo codice di verifica HTML quando la verifica DNS della proprietà dominio è già attiva.

1. In **Sitemap**, invia `https://www.lobiz.it/sitemap.xml`.
2. In **Controllo URL**, ispeziona `https://www.lobiz.it/`, esegui il test live e richiedi l’indicizzazione dopo la pubblicazione.
3. Controlla una pagina servizio e una pagina progetto: contenuti leggibili, scansione consentita, URL canonico coerente.
4. Nei giorni successivi controlla eventuali errori di indicizzazione; nelle settimane successive misura impression, clic, CTR e posizione per “Lobiz”, “Lobiz Agency” e varianti.
5. Esegui PageSpeed Insights su mobile e desktop dopo la pubblicazione. Qui non è stato attribuito un punteggio Lighthouse o misurato il rendimento reale degli utenti.

Sitemap, dati strutturati e richiesta di indicizzazione non garantiscono indicizzazione o prima posizione. Search Console e il dominio pubblicato sono necessari per verificare il risultato effettivo.

## Miglioramenti implementati

- Titoli e descrizioni unici per ogni pagina, H1 descrittivo e contenuti HTML leggibili senza JavaScript.
- Canonical coerenti su `https://www.lobiz.it/`, con percorsi distinti.
- Identità Lobiz Agency / Lobiz Srl, dati strutturati `Organization`, `WebSite`, `WebPage`, `BreadcrumbList` e `Service` dove pertinenti.
- Collegamenti HTML dalle schede ai progetti, dai servizi ai lavori e dai lavori ai servizi. Breadcrumb nelle pagine interne.
- Open Graph, Twitter Card, favicon e immagine social originale basata sulla grafica del sito.
- Dimensioni esplicite delle immagini, caricamento differito sotto la prima schermata e varianti responsive per tredici immagini principali.
- Miniature delle gallerie create soltanto all’apertura; script differiti; menu mobile e preferenza movimento ridotto.
- Il riferimento `assets/urban-verity.jpg.webp`, che sul sito pubblico restituiva 404, è stato sostituito con una copia della fotografia Verity già disponibile nei materiali del progetto.
- La scheda Verity è stata denominata “Verity / Edicola” per descrivere il lavoro senza riprendere l’ambigua etichetta “Sony Music Premier”.

## Contenuti da arricchire nel tempo

I testi delle nuove pagine sono ricavati dalle descrizioni e dalle categorie dei file forniti. Non sono stati inventati risultati numerici, testimonianze, date, nomi del team o prestazioni commerciali. Per rendere i case study più forti, aggiungi il ruolo preciso di Lobiz, il contesto, le date e risultati verificati quando disponibili.

Allinea il nome pubblico **Lobiz Agency** e il link ufficiale su LinkedIn, Instagram e altri profili dell’agenzia. Questi profili esterni non sono stati modificati. Valuta la scheda Google dell’attività se idonea.

Non sono stati aggiunti strumenti analytics, form o tracker. I collegamenti email, social e mappa sono normali link. Eventuali nuove funzionalità di raccolta dati vanno configurate separatamente.

## Verifiche eseguite

- 19 documenti HTML: 18 pagine indicizzabili e una 404 con `noindex`.
- Sitemap con 18 URL e canonical coerenti.
- 718 riferimenti locali verificati: pagine, immagini, script, CSS e frammenti.
- JSON-LD e configurazione JSON correttamente parsati; titoli e descrizioni unici; un H1 per pagina; nessun ID duplicato.
- Sintassi dei JavaScript verificata.
- Apertura di tutte le otto gallerie, avanzamento foto su Prada e navigazione alla pagina progetto verificati nel browser.
- Controllo visivo desktop della home e del progetto Prada; controllo a larghezza 390 px della home, di MINI Padel League e del servizio Urban; apertura/chiusura del menu mobile.

I redirect di dominio, l’indicizzazione Google e i Core Web Vitals reali rimangono verifiche da effettuare sull’ambiente pubblico dopo il caricamento.

## Anteprima tramite server, facoltativa

Il doppio clic su `sito/index.html` è ora sufficiente. Le risorse usano percorsi relativi; quando il protocollo è `file:`, un piccolo script adatta i collegamenti alle pagine locali. Sul sito pubblico rimangono URL puliti e canonical invariati. Se preferisci simulare un server e hai Python installato, entra nella cartella `sito` e avvia:

```sh
python3 -m http.server 8000
```

Poi apri http://localhost:8000/ nel browser. In alternativa usa l’anteprima del progetto Vercel esistente.

## Riferimenti tecnici

- Google Search Central: https://developers.google.com/search/docs/appearance/site-names
- Google Search Central: https://developers.google.com/search/docs/appearance/structured-data/organization
- Vercel: https://vercel.com/docs/project-configuration/vercel-json

## Correzione apertura locale

Risolto il mancato caricamento di CSS, immagini e script nell’apertura diretta dell’HTML. Controllati 464 riferimenti alle risorse con risoluzione file:// e i collegamenti alle pagine locali.

## Ultime modifiche grafiche

Rimossa da tutte le pagine la fascia partner con Cesana Brokers, Detectia e Assolombarda/CDO e le relative didascalie. Conservati i dati societari e i collegamenti del footer. Nella sezione “The City is our Media” resta una sola fotografia della metropolitana, con rapporto originale 1000:667, senza collage, rotazioni o deformazioni.

## Sedi e mappe

Rimossa Roma dalle indicazioni delle sedi. Inserite sede legale Milano (Via Archimede, 57), sede operativa Milano (Via San Sisto, 3), sede operativa Piacenza (Via Emilia Pavese, 107). Ogni indirizzo apre una ricerca Google Maps in una nuova scheda. Aggiornati footer, pagina Contatti, presentazione dell’agenzia e dati strutturati.

## Footer blu
Sfondo blu continuo fino al fondo pagina, testi bianchi, schede sedi con icone e pulsanti Apri mappa, navigazione a pulsanti.

## Edicole Lilly
Lilly è il progetto 10, subito dopo Verity. La copertina apre la galleria di sei foto con frecce, miniature e swipe. Rimossa la sezione autonoma.
