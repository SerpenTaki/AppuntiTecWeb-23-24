*L'accessibilità è "l'usabilità di un prodotto, servizio, ambiente o strumento, per persone col più ampio raggio di capacità"*.

### Accessibilità per il web
- Il termine accessibilità riferito al web intende la possibilità di accedere alle informazioni e ai servizi disponibili in rete da parte di categorie di utenti diversificate e da una gamma di dispositivi diversi.
- L'attenzione è concentrata sulla possibilità di accedere all'informazione da parte di categorie di utenti svantaggiate sotto il profilo fisico o psichico: in un numero significativo di casi l'accesso all'informazione richiede l'uso di dispositivi diversi dai browser comunemente utilizzati.

### Classi di utenti svantaggiati
- Non sono in grado di vedere, ascoltare o muoversi o di trattare alcuni tipi di informazione
- Difficoltà nella lettura o nella comprensione del testo
- Non sono in grado di usare una tastiera o un mouse
- Dispongono di uno schermo non grafico (solo testo), piccolo o di una connessione lenta
- Non parlano o comprendono correttamente la lingue con la quale è scritto il documento
- In situazioni in cui i loro organi sensoriali (occhi, orecchie, mani) sono occupati o impediti (es. guidano)
- Hanno una versione precedente del browser, un browser diverso da quello su cui è sviluppato il sito, un diverso SO etc....
### Accessibilità e legislazione
l'attenzione all'accessibilità, in molti casi, fa parte delle buone regole di progettazione di un sito, che raggiunge l'obiettivo di rendere l'informazione più facile da consultare per TUTTI gli utenti-
- Nel caso di siti governativi, l'accessibilità diventa un obiettivo da perseguire obbligatoriamente
	- Negli USA la normativa della Section 508 (giugno 2001), stabilisce che tutta l'informazione diffusa da agenzie federali sia accessibile da utenti con disabilità
	- In Italia la legge STANCA (n. 4, gennaio 2004, rivista nell'aprile 2010), obbliga le amministrazioni pubbliche ad avere siti accessibili, pena l'applicazione di sanzioni
	- In europa lo standard WCAG 1.0 e 2.0 sono usate come standard legale per il giudizio di accessibilità

### La legge Stanca
- riconosce "*il diritto di ogni persona ad accedere a tutte le fonti di informazione e ai relativi servizi, ivi compresi quelli che si articolano attraverso gli strumenti informatici e telematici*"
- Nei confronti della **Pubblica Amministrazione** apporta obblighi sorretti da sanzioni in caso di illecito;
- nei confronti dei *privati* è prevista la possibilità di ottenere una certificazione di diversi livelli di accessibilità previsti dalla legge.
- **DIDATTICA**: una delle finalità principali della legge si esplica nell'art.5 che sottolinea la necessità di favorire l'accesso agli strumenti d'istruzione da parte di persone con disabilità, con particolare riferimento a non vedenti o ipovedenti.

#### Il ruolo dell'AGID
- L'**AGID** è *l'agenzia per l'italia digitale*, istituita con il decreto legge n.83 del 22 giugno 2023
- il decreto legge n.189 del 2012 impone l'obbligo per le **PA** di definire e pubblicare sul proprio sito web gli obiettivi annuali di accessibilità
	- AGID viene incaricata del monitoraggio e dell'intervento verso i non adempienti, e dal 2017 ha al suo interno il *difensore civico per il digitale*
- Nel novembre 2019 l'AGID definisce le "*linee Guida sull'Accessibilità degli strumenti informatici*"
- 9 gennaio 2020: AGID rende disponibili
	- Dichiarazione di accessibilità
	- Modello di valutazione

### Obblighi per le Pubbliche Amministrazioni
- Entro il *31 Marzo* di ogni anno devono pubblicare gli *obiettivi di accessibilità* per l'anno corrente e lo stato di attuazione del piano per l'utilizzo del telelavoro
- Entro il *23 Settembre* di ogni anno devono effettuare un'analisi completa dei siti web e compilare la dichiarazione di accessibilità
	- la *dichiarazione di accessibilità* deve essere inserita nel footer del sito
	- deve contenere un meccanismo di feedback

### Obblighi per i privati
- Determinazione n.117/2022 definisce per i soggetti che offrono servizi al pubblico attraverso siti web o applicazioni mobili, con un fatturato medio, negli ultimi 3 anni di attività, superiore a 500 milioni di euro:
	- compilare la dichiarazione di accessibilità e inserirla nel footer del sito
	- prevedere dei meccanismi di feedback per segnalare problemi
- Se una verifica dell'AGID riscontra un problema di accessibilità il non adeguamento comporta una sanzione che può arrivare al 5% del fatturato
- Tutti i soggetti devono adeguarsi entro giugno 2025 come previsto dall'Accessibility Act, mentre per le PA e i soggetti di cui sopra il termine era il 28 giugno 2022

## Idee Sbagliate
- Accessibilità non vuol dire che il sito deve essere perfettamente identico (pixel a pixel) su ogni dispositivo e con qualsiasi browser
- Non è vero che l'accessibilità costa troppo. Molti accorgimenti fanno già parte delle regole per creare un buon sito web (*standard web*) o richiedono davvero poco sforzo ([[TecWeb/AppuntiTecWeb-23-24/HTML5|HTML5]] *uso del tabindex*)
- L'accessibilità non può essere raggiunta semplicemente utilizzando un opportunuo strumento di autore 
- è discutibile che i designer possano ignorare i requisiti di accessibilità se i loro clienti gli dicono di farlo

### WAI
- **WAI**, Web Accessibility Initiative: è una delle iniziative più significative nel campo dell'accessibilità. è definita dal consorzio W3C con l'obiettivo di rendere il web accessibile universalmente
- Il gruppo di lavoro WAI
	- definisce le linee guida per assicurare l'accessibilità di un sito web
	- assicura che le tecnologie e gli standard promossi dal W3C supportino l'accessibilità (Flash non è promosso da questo consorzio)
	- promuove la ricerca e la formazione sulla materia

#### Raccomandazioni WAI
- Sono rivolte a 3 classi di utenza
- Linee guida per l'accessibilità dei contenuti web
	- si rivolgono ai *web designer* e agli *autori* di pagine web fornendogli regole e tecniche affinchè un documento sia accessibile
- Linee guida per l'accessibilità degli strumenti di authoring
	- si rivolgono ai *creatori di strumenti di authoring* affinchè rendano facile la creazione di contenuto conforme agli standard per l'accessibilità e rendano accessibili gli stessi strumenti di authoring
- Linee guida per l'accessibilità degli strumenti per navigare il web
	- Si rivolgono agli *sviluppatori di strumenti di navigazione*, dai browser classici agli strumenti specializzati per persone con disabilità

### Linee guida per l'accessibilità ai contenuti WEB
- Le linee guida per l'accessibilità ai contenuti web costituiscono un documento di riferimento per i principi generali circa l'accessibilità e per idee riguardanti la progettazione
- Il documento delle linee guida rappresenta una versione *stabile*: non fornisce quindi informazioni specifiche circa il supporto delle diverse tecnologie da parte di particolari browser, data la rapidità con cui tali informazioni possono variare
- Al completamento delle linee guida per il web designer, il gruppo WAI ha emesso un documento (**Tecniche relative alle linee guida per l'accessibilità ai contenuti web**) che fornisce tecniche per l'implementazione dei punti di controllo visti precedentemente.

#### Organizzazione delle linee guida
- **Ciascuna linea guida comprende**:
	- il numero 
	- l'obiettivo
	- la logica dietro la linea guida e alcune categorie di utenti destinate a beneficiarne
	- Una lista di definizione dei punti di controllo
- Le definizioni dei punti di controllo presenti in ciascuna delle linee guida spiegano in che modo la specifica linea guida è applicabile in tipici scenari di sviluppo dei contenuti. Ciascuna definizione dei punti di controllo contiene:
	- Il numero 
	- L'obiettivo
	- La priorità
	- Note informative opzionali, esempi chiarificatori, e riferimenti incrociati
	- il riferimento ad una sezione del documento sulle tecniche dove sono discusse le implementazioni

#### Priorità
- Il livello di priorità è basato sull'impatto che tale punto possiede sull'accessibilità
	- **Priorità 1**
		- lo sviluppatore **deve** conformarsi al presente punto di controllo, pena le preclusione di una o più categorie di utenti dall'accesso alle informazioni
		- costituisce un requisito base
	- **Priorità 2**
		- Lo sviluppatore **dovrebbe** conformarsi al presente punto di controllo, altrimenti ad una o più categorie di utenti risulterà difficile accedere alle informazioni
		- Consente di rimuovere barriere significative
	- **Priorità 3**
		- Lo sviluppatore **può** tenere in considerazione questo punto di controllo, altrimenti ad una o più categorie di utenti sarà in qualche modo ostacolata nell'accedere alle informazioni
		- Migliora l'accesso ai documenti web

#### Conformità
- Sono stati definiti 3 livelli di conformità:
	- Livello di conformità:"**A**" conforme a tutti i punti di controllo di priorità 1
	- Livello di conformità: "**Doppia A**"(**AA**) conforme a tutti i punti di controllo di priorità 1 e 2
	- Livello di conformità: "**Tripla A"(**AAA***) conforme a tutti i punti di controllo di priorità 1, 2 e 3

## I 4 principi fondamentali introdotti dalle WCAG 2.0
- Un servizio è accessibile quando è **PURO**:
	- P: percepibile
	- U: Comprensibile (*Understandable*)
	- R: Robusto
	- O: Utilizzabile (*Operable*)

### Principi di progettazione
- Le linee guida si basano su 2 principi generali:
1. Assicurare una **Trasformazione elegante**
	- Le pagine che si trasformano con eleganza rimangono accessibili nonostante le limitazioni dovute a disabilità fisiche, sensoriali e dell'apprendimento, limitazioni causate da barriere tecnologiche
2. Rendere il contenuto **comprensibile** e **navigabile**
	- Gli sviluppatori dovrebbero utilizzare un linguaggio chiaro e semplice, fornire meccanismi facilmente comprensibili per la navigazione all'interno della pagina e tra pagine diverse

### Trasformazione elegante
Alcuni principi chiave:
- Separare la struttura dalla presentazione
- Fornire sempre un'equivalente testuale per ogni media diverso dal testo: il testo può essere riprodotto secondo modalità accessibili a quasi tutti gli utenti
- Creare documenti che  veicolino l'informazione anche se l'utente non può vedere o sentire: fornire informazioni attraverso diversi canali sensoriali alternativi
- Creare documenti che non necessitino di un HW specifico: le pagine dovrebbero essere utilizzabili anche senza mouse, con piccoli schermi, a bassa risoluzione, in bianco e nero, oppure senza schermo attraverso output di voce o testo

### Contenuto comprensibile e navigabile
- Dotare la pagina di strumenti di *navigazione* ed *orientamento* ne massimizza l'accessibilità e l'utilizzabilità
- Non tutti gli utenti sono in grado di utilizzare le indicazioni visive come immagini sensibili, barre di scorrimento proporzionali, frame affiancati, o comunque elementi grafici che possono essere utilizzati solamente da utenti vedenti
- Gli utenti possono inoltre perdere informazioni relative al contesto qualora possano vedere solo una parte della pagina. Senza informazioni che aiutino l'orientamento, tabelle di grandi dimensioni, elenchi e menù, possono non essere comprensibili per alcune categorie di utenti.

#### Contenuti equivalenti
- Un contenuto è *equivalente* ad un altro quando entrambi svolgono essenzialmente la stessa funzione o scopo nei confronti dell'utente
- Particolarmente importante per gli utenti con disabilità
- Dal momento che il contenuto testuale può essere presentato all'utente sotto forma di sintesi vocale, braille e il testo mostrato visivamente, le linee guida richiedono *equivalenti testuali* per le informazioni grafiche e audio, scritti in modo da veicolare l'intero contenuto essenziale
- Gli *equivalenti non testuali* (ad es. descrizione uditiva, un video con una persona che usa il linguaggio dei segni) migliorano l'accessibilità anche per le persone che non possono accedere all'informazione visiva o al testo scritto, inclusi molti individui con disabilità della vista, cognitive, dell'apprendimento, dell'udito
	- Caso CAPTCHA

## Linee guida per l'accessibilità ai contenuti web

1. Fornire alternative equivalenti al contenuto audio visivo
	- Rimarca l'importanza del fornire contenuti equivalenti per le informazioni non testuali
	- Fornire contenuto che, presentato all'utente, trasmetta lo stesso scopo o funzione del contenuto audio o visivo
	- Fornire alternative per immagini, film, suoni, applet, etc...
	- Fornire equivalenti non testuali (immagini, video audio) del testo scritto è di beneficio per alcuni utenti, specialmente gli illetterati o le persone che hanno difficoltà di lettura
2. Non fare affidamento sul solo colore
	- Assicurarsi che testo e grafica siano comprensibili se consultati senza il colore
		- Se alcune informazioni sono veicolate solo con il colore (es. link non visitati) le persone che non li distinguono o con un monitor in bianco e nero non ricevono l'informazione
3. Usare marcatori e fogli di stile e farlo in modo appropriato
	- Marcare i documenti con i corretti elementi strutturali. L'uso di tabelle per l'impaginazione impedisce l'accessibilità e la navigazione con software specialistico
	- controllare la presentazione con i soli fogli di stile dei browser
4. Chiarire l'uso dei linguaggi naturali
	- Utilizzare marcatori che facilitino la pronuncia o l'interpretazione di testi stranieri o abbreviati. Questo aiuta le sintesi vocali e le periferiche braille che possono selezionare automaticamente la nuova lingua
	- Gli sviluppatori dovrebbero esplicitare le abbreviazioni e gli acronimi
5. Creare tabelle che si trasformino in maniera elegante
	- Usare la marcatura corretta per le tabelle, che devono essere usate solo per i dati realmente tabellari e non per il layout
	- Alcuni interpreti consentono agli utenti di navigare tra le celle delle tabelle e di accedere alle intestazioni e ad altre informazioni nelle celle. A meno che non sia stata realizzata una marcatura corretta, queste tabelle non forniranno agli interpreti le informazioni appropriate.
6. Assicurarsi che le pagine che danno spazio a nuove tecnologie si trasformino in maniera elegante
	- Le pagine devono essere accessibili anche quando la tecnologia più recenti non sono supportate o disabilitate
	- Non sempre l'uso della tecnologia più recente è una buona scelta
7. Assicurarsi che l'utente possa tenere sotto controllo i cambiamenti di contenuto nel corso del tempo
	- Gli elmenti in movimento, lampeggianti, scorrevoli o che si autoaggiornano, devono poter essere arrestati temporaneamente o definitivamente
		- velocità eccessiva
		- i lettori di schermo non li leggono
8. Assicurare l'accessibilità diretta delle interfacce utente incorporate
	- La progettazione delle interfacce utente deve seguire i principi dell'accessibilità: accesso alle diverse funzionalità indipendente dai dispositivi usati, possibilità di operare da tastiera, comandi vocali, etc. Questo deve valere anche per gli oggetti incorporati
9. Progettare per garantire l'indipendenza da dispositivo
	-  Usare le caratteristiche che permettono di attivare gli elementi della pagina attraverso una molteplicità di dispositivi di input
	- Accesso indipendente dal dispositivo significa che gli utenti possono interagire con l'interprete o con il documento con il dispositivo di I/O preferito
	- Fornendo equivalenti testuali per immagini sensibili o per immagini usate come collegamento si dà agli utenti la possibilità di interagire con esse senza un dispositivo di puntamento
	- Se una pagina permette di interagire con la tastiera in genere è accessibile anche tramite input vocale o interfaccia a linea di comando
10. Usare soluzioni provvisorie
	- usare soluzioni provvisorie in modo che le tecnologie assistive e i browser più vecchi possano operare correttamente
	- I punti di controllo di questa linea guida sono classificati come *provvisori*, nel senso che il gruppo di lavoro li ritiene validi e necessari per l'accessibilità del web *al momento della pubblicazione del documento*
11. Usare le tecnologie e le raccomandazioni del W3C
	- Se questo non è possibile, oppure se utilizzando una specifica W3C si ottiene materiale che non si trasforma in modo elegante, fornire una versione alternativa del contenuto accessibile
	- Le tecnologie W3C contengono elementi di accessibilità *integrati*
	- Molti formati non W3C come shockware e PDF richiedono *plug-in* o applicazioni autonome
12. Fornire informazioni per la contestualizzazione e l'orientamento per aiutare gli utenti a comprendere pagine od elementi complessi
	- Fornire informazioni contestuali può essere utile per tutti gli utenti. Relazioni complesse tra parti di una pagina possono essere difficili da interpretare per persone con invalidità cognitive o visive
13. Fornire chiari meccanismi di navigazione
	- Informazioni per l'orientamento, barre di navigazione, mappa del sito. Tutto quello che può servire ad aumentare la probabilità che una persona trovi quello che sta cercando nel sito
	- Chiari e coerenti meccanismi di navigazione sono importanti per le persone con invalidità e giovano a tutti gli utenti
14. Assicurarsi che i documenti siano chiari e semplici in modo da poter essere compresi più facilmente
	- Una disposizione coerente della pagina, una grafica riconoscibile e un linguaggio facile da capire, sono importanti per le persone con invalidità e giovano a tutti gli utenti
	- L'uso di un linguaggio chiaro e semplice promuove una comunicazione efficace. L'accesso alle informazioni scritte può essere difficile per le persone con disabilità cognitive o dell'apprendimento o persone di diversa madrelingua

# Accessibilità in pratica

### Il testo
- Usare il markup semantico: **in modo corretto**
- Il linguaggio usato deve essere il più possibile chiaro
- Da usare (*migliorano la leggibilità*):
	- esposizione per punti
	- Interlinea (*almeno 1.5em*)
- Da evitare:
	- testo scorrevole o lampeggiate
	- font troppo elaborati
	- sottolineatura per il testo che non costituisce l'ancora di un link
	- testo barrato se non strettamente necessario
	- Fare **Attenzione** alle _dimensioni_ e al *colore*

### Microformati
- [[HTML5]] ha introdotto diversi tag semantici, ma non erano ancora sufficienti
- I microformati sono un insieme di specifiche sulla marcatura di contenuti create per dare *semantica* (e *metadati*) non disponibili in HTML
	- ad esempio, *address* non è sufficiente per evidenziare informazioni di contatto
- L'antenato dei microformati è XFN con l'utilizzo di rel nei link per indicare la relazione con la pagina destinazione
- Esempio: *rel="me"* per indicare il link alle proprie pagine social
- In genere i microformati definiscono un insieme di valori per attributi
	- valori per l'attributo *class* (ex: per le informazioni di contatto)
	- valori per l'attributo *rel*
- Ci sono molti microformati diversi per esigenze diverse
- Sono supportati dai motorio di ricerca che spesso privilegiano i contenuti con microformati
- Esistono diversi interpreti di microformati per quasi tutti i linguaggi di programmazione

### Attributi data-*
- Per aggiungere ulteriore semantica [[HTML]] prevede degli attributi che permettono di inserire delle informazione definite dall'utente dentro la pagina
- sono dati che possono essere personalizzati per ogni pagina, e poi utilizzati tramite Javascript o CSS
- Il nome dell'attributo deve iniziare con data- non contenere alcuna lettera maiuscola, e almeno un carattere oltre il prefisso
- il valore può essere una qualsiasi stringa
- Di default, il browser li ignora

````HTML
<input type="password" name="pin" required="required" aria-required="true" data-msg-required="Per favore, inserisci la tua password" data-msg-invalid="formato non corretto">
````
- Gli attributi dati sono accessibili dalla libreria JS JQuery mediante la proprietà dataset di un elemento, automaticamente convertiti in camel case 
	`$field.dataset.msgRequired`
- Aumentano il disaccoppiamento e migliorano la mantenibilità.

### Accessibilità in pratica: i link
- I link sono elementi fondamentali per il web, perciò è molto importante che siano accessibili a tutti gli utenti
- Alle origini del web i link erano facilmente riconoscibili, perchè costituiti da parole (o frasi) scritte in blu e sottolineate
- Oggi il web designer può personalizzare come presentare un link
	- L'utente deve poter riconoscere i link già visitati
- Alcuni web designer, tra cui Jakob Nielsen, sostengono che non si debba variare il colore dei link per non disorientare i link già visitati
- Alcuni web designer, tra cui Jackob Nielsen, sostengono che non si debba variare il colore dei link per non disorientare gli utenti
- è importante una corretta definizione delle ancore dei link
	- clicca qui
	- prosegui
#### Personalizzazione dell'aspetto dei link
- Mai utilizzare convenzioni ben consolidate per scopi diversi
	- Coerenza vs. personalizzazione (*link tipizzati*)
#### Uniformità vs. differenziazione dei link
- I link devono essere facilmente riconoscibili
	- rappresentazione uniforme
- L'introduzione di alcune differenziazioni può aiutare l'utente a fare una previsione sulla destinazione e sui tempi necessari
	- link interni vs esterni
	- Link tipizzati
	- Indicare la dimensione del file nel caso di un download

- I link devono essere riconoscibili univocamente
	- Test ad occhi socchiusi (*Drue Miller*)
- Evitare i pop-up
- I link devono essere accessibili anche ad utenti con disabilità o dispositivi meno tecnologicamente avanzati
	- Utilizzo controllato di immagini
	- Definizione corretta della tabulazione
		- immaginare i bisogni degli utenti e stabilire un ordine di tabulazione in base a questi
	- Utilizzo di accessKey
		- Non esiste un modo visuale di far conoscere agli utenti le chiavi utilizzate
		- Possibilità di conflitti con le chiavi utilizzate da altri programmi

````HTML
<a href="http://wwww.server.com/path/doc.html" tabindex="1" accesskey="s"> Sorgente del link </a>

<a href="http://www.server.com/path/doc.html" tabindex="1" accesskey="s"> Sorgente del link (s) </a>
````

### Suggerimenti per gli screen-reader
- I link adiacenti devono essere separati da almeno uno spazio
- Un utente non deve perdere molto tempo nella lettura di tutte le possibilità offerte dal menù

````HTML
<a class="aiuti" href="#contenuto"> Salta la navigazione </a>
<nav id="menu"> ...tutto il menù...</nav>
<main id="contenuto">
	tutto il contenuto
</main>
````
````CSS
.aiuti{
	display:none;
}
.aiuti{
	visibility:hidden;
}
.aiuti{
	position:absolute;
	height:0;
	overflow:hidden;
}
/*ALTRI MODI: UTILIZZO DEI RIENTRI*/
.aiuti{
	text-indent:-999em;
}
.aiuti{
	position:absolute;
	left:-999em;
}
.aiuti{
	overflow:hidden;
	text-indent: 100%;
	white-space: no-wrap;
	width: 10px;
}
````

### Accessibilità in pratica: i bottoni
Ci sono 4 modi di creare un bottone (ma uno solo da preferire)
- `<input type = 'submit'/>`
- `<button type = "submit"/>`
- Utilizzo di a + CSS + Javascript
- Utilizzo di div + CSS + Javascript
Solo i primi 2 sono attivabili tramite lo spazio.
I **div** non ricevono il focus con i tab a meno di non introdurre un *tabindex* e richiedono maggior sforzo con javascript per permettergli di inviare dei moduli e interagire con la tastiera. Sia a che div richiedono l'attributo *role="button"* per essere accessibili. *Ha senso tutto questo lavoro in più?*

#### Nono introdurre fragilità!
*Potenziali problemi*:
- Il browser non supporta i CSS, oppure sono disattivati per migliorare le prestazioni o l'utente ha un foglio di stile personalizzato per accessibilità o altre preferenze
- Un problema di rete non rende disponibili CSS o Javascript
- Le regole CSS appaiono in una media query e il browser non le supporta
- Javascript è disattivato
- Un firewall ha bloccato le richieste del JavaScript
- Un errore JavaScript di terze parti, o un bug del codice, ha bloccato l'esecuzione del JavaScript
- Il browser, o la tecnologia assistiva, non supporta ARIA

### Accessibilità in pratica: le immagini
- Devono essere inserite con il tag *img* solo le immagini che costituiscono parte del contenuto
- Le immagini che riguardano il solo layout dovrebbero essere inserite come immagini di background
- Definire sempre attributi *alt* significativi
	- Logo
	- Alt vuoto per le immagini che riguardano il solo layout
	- Non fidatevi degli alt generati automaticamente
- Non usare mappe immagine, specialmente quelle lato server
- Controllare se il sito rimane accessibile anche senza immagini

## Image Replacement: alternative grafiche al testo
- Visto che non si può fare affidamento sui font installati sul computer dell'utente, spesso si utilizzano immagini al posto del testo per ottenere una grafica accattivante con grave danno all'accessibilità del sito web
- *Image Replacement*: è una tecnica usata per fornire alternative grafiche per il testo, rimpiazzandolo con delle immagini tramite CSS
- Vantaggi.
	- La pagina rimane accessibile
	- Viene preservata la grafica
	- Si utilizzano gli standard web e non soluzioni ad hoc proprietarie
	- è possibile modificare le immagini, se necessario, modificando solo il foglio di stile

#### Image Replacement: prima soluzione
- Idea di base nascondere il testo e collocare un'immagine nello sfondo del contenitore "vuoto"
	- I *browser* visualizzano l'*immagine*
	- gli *screen* reader leggono il *testo*
````HTML
<h1><span>Sifaka</span></h1>
````
````CSS
h1{
	background-image: url(...);
	width: largh. img;
	height: alt. img;
}

h1 span{
	display:block;
	height:0;
	overflow:hidden;
}
````
#### Seconda soluzione
````HTML
<h1>Sifaka</h1>
````
````CSS
h1{
	position:relative;
	width: largh. img;
	height: alt. img;
	font-size: 1px;	
	text-indent: -999em;
}
/*PROBLEMA: se le immagini sono disabilitate non si vede nulla*/
````
#### Terza soluzione
````HTML
<h1><span></span>Sifaka<h1>
````
````CSS
h1{
	position:relative;
	width: largh. img;
	height: alt. img,
	font-size: 50px;
}

h1 span{
	position:absolute;
	top:0;
	width: largh. img;
	height: alt. img;
	background-image: url(...);
}
````
- Lo span deve avere la stessa dimensione dell'immagine e questa non può avere sfondo trasparente
	- Problemi al ridimensionamento del layout
- http://mezzoblue.com/tests/revised-image-replacement
#### Quarta soluzione
````HTML
<h1 class="hide">Sifaka</h1>
````
````CSS
.hide{
	text-indent:100%;
	white-space:nowrap;
	overflow:hidden;
}
h1.hide{
	background-image: url(...);
}
````
### Non usare solo testo!
- Le immagini permettono di catturare meglio l'attenzione dell'utente
- Le infografiche possono aiutare le persone con disabilità cognitive a capire e memorizzare meglio il contenuto

### Accessibilità in pratica: le tabelle
- è sempre preferibile evitare l'uso delle tabelle per creare il layout di un sito. Se proprio necessario, usare tabelle semplici può aiutare l'accessibilità
- Il problema più rilevante riguarda la bidimensionalità delle tabelle: le associazioni righe-colonne sono facilmente rilevabili con gli occhi, ma difficilmente spiegabili facendo affidamento solo sull'udito perchè gli *screen-reader* linearizzano le tabelle.
- Alcuni accorgimenti che possono aiutare:
	- associare, una breve descrizione del contenuto della tabella (attributo *summary* in XHTML, *aria-describedby* in HTML5)
	- associare le intestazioni alle celle (attributo *scope*)
	- associare le celle alle intestazioni (attributo *headers*)
	- definire abbreviazioni per le intestazioni (attributo *abbr*)
![[Pasted image 20231120121300.png]]
````HTML
<table summary="La tabella contiene l'elenco dei libri della biblioteca. Ogni riga descrive un libro con titolo, autore, editore, data edizione e prezzo">
	<caption>Libri della Biblioteca</caption>
	<tr><th scope="col">Titolo</th><th scope="col">Autore</th>
		...
	</tr>
	<tr><td scope="row">Il mastino di Baskerville</td>
		<td xml:lang="en">Conan Doyle</td>
		<td> Fabbri Editore </td>
	</tr>
	<tr>...
	</tr>
</table>

<!--OPPURE-->

<table aria-desribedby="descr">
	<caption>Libri della Biblioteca</caption>
	<tr><th scope="col">Titolo</th><th scope="col">Autore</th>
		...
	</tr>
	<tr><td scope="row">Il mastino di Baskerville</td>
		<td xml:lang="en">Conan Doyle</td>
		<td> Fabbri Editore </td>
	</tr>
	<tr>...
	</tr>
</table>

<p id="descr">La tabella contiene l'elenco dei libri della biblioteca. Ogni riga descrive un libro con titolo, autore, editore, data edizione e prezzo</p>
````
![[Pasted image 20231120121937.png]]
````HTML
<table border="1">
	<tr><th></th>
		<th id="c1" abbr="Lun" axis="giorno">Lunedì</th>
		<th id="c2" abbr="Mar" axis="giorno">Martedì</th>
		<th id="c3" abbr="Mer" axis="giorno">Mercoledì</th>
		<th id="c4" abbr="Gio" axis="giorno">Giovedì</th>
		<th id="c5" abbr="Ven" axis="giorno">Venerdì</th>
	</tr>
	<tr><th id="m1" axis="materia"> Italiano</th>
		<td></td><td></td><td></td><td></td><td></td>
	</tr>
	<tr><td id="o1" axis="ora">8.00</td>
		<td headers="m1 c1 o1">1s</td>
		<td headers="m1 c2 o1"></td>
		<td headers="m1 c3 o1"></td>
		<td headers="m1 c4 o1">3d</td>
		...
</table>
````
### Tabelle responsive
**NB: nel Laboratorio usiamo le tabelle responsive che permettono di _adattare_ la tabella anche per i dispositivi mobili _Bisogna FARLO sempre per accessibilità_**
![[Pasted image 20231120123443.png]]
**L'idea (Aaron Gustafson)**
- Ogni cella ha un attributo *data-title* che riporta l'intestazione di colonna
- Negli schermi piccoli il CSS si preoccupa di:
	- Rendere *tr* e *td* elementi di blocco per visualizzarli uno per riga (`display:block;`)
	- Non visualizzare gli header (*thead*)
	- Aggiungere un'intestazione ad ogni cella prendendola dall'attributo *data-title* (con la proprietà content)
````HTML
<tr><th id="sheldon" xml:lang="en" headers="personaggio">Sheldon Cooper</th>
	<td headers="personaggio sheldon specializzazione" data-title="Specializzazione">Fisica</td>
	<td headers="personaggio sheldon qi" data-title="QI">183</td>
	<td class="centerText" conlspan="4" headers="sheldon presente in prima Stagione secondaStagione terzaStagione quartaStagione" data-title="Stagioni 1,2,3,4">Presente</td>
</tr>
...
````
````CSS
thead, tfoot{
 display: none;
}
tr, th, td {
	display:block;
	padding:0;
	white-space:normal;
}
th[data-title]:before, td[data-title]:before{
	content: attr(data-title)":\00A0"
	font-weight:bold;
}
th{
	background-color: #BD091B;
	color: #FFF;
}
td, th {
	border-top:none;
}
tr:first-child{
	border: 1px solid #000;
}
````
### Accessibilità in pratica: i form
- Per creare form accessibili è necessario:
	- corredare sempre i campi dei form con delle etichette (*label*). L'elemento label è particolarmente importante per check-box e pulsanti radio
	- raggruppare le voci con *optgroup* o *fieldset*
	- utilizzare *tabindex* e *accesskey* in modo appropriato nei tag *input, textarea, select*
	- utilizzare *title* per fornire informazioni aggiuntive
	- Fornire aiuti contestuali
	- Rendere gli errori reversibili
### Accessibilità in pratica: il colore
- Controllare sempre che la pagina sia accessibile agli utenti che non sono in grado di vedere il colore
- Se l'informazione è veicolata tramite il colore deve essere rinforzata
	- ex. grassetto o sottolineatura per i link
- Evitare i riferimenti al colore nel testo
	- ex. "*fare click sul pulsante giallo*", "*Troverete questa informazione sul box azzurro*"
- Attenzione agli schemi cromatici troppo armoniosi
	- il rapporto di contrasto tra testo e grafica sottostante deve essere di almento 4.5:1 o 3:1 per testo grande (*fanno eccezione logotipi ed elementi di pura decorazione*)
	- www.vischeck.com, https://color.a11y.com
![[Pasted image 20231120132122.png]]
#### Diversi tipi di contrasto
- Contrasto *chiaro-scuro*
- Contrasto di complementari
- Contrasto *caldo-freddo*
- Contrasto di saturazione
![[Pasted image 20231120132223.png]]
![[Pasted image 20231120132235.png]]
-> Guardare La _Color Universal Design Organization (**CUDO**) Palette_
-> oppure la *Palette di Brian Suda* che contiene colori riconoscibili dagli utenti con difficoltà nella percezione dei colori ma è adatta anche alla stampa dato che si traduce bene con i toni di grigio

## Strumenti per testare/scegliere i colori
- **Per testare i colori**
	- Color Oracle (https://colororacle.org/)
	- Color Contrast Accessibility Validator (https://color.a11y.com)
	- Color Contrast Analyzer (CCA)
- **Per aiutare nella scelta dei colori**
	- Color safe (http://colorsafe.co/)

## WAI-ARIA
- *W*eb *A*ccessibility *I*nitiative - *A*ccessible *R*ich *I*nternet *A*pplications (ARIA) è uno standard W3C
- è pensato per le pagine web particolarmente interattive, sviluppate con HTML5, Javascript e Ajax, per permettere la loro fruizione anche attraverso gli screenreader
- Definiscono *ruoli, stati* e *proprietà* per ogni widget di interazione
- Assegna un ruolo semantico ad ogni componente della pagina
- Non cambiano in alcun modo la pagina, nè il DOM, ma contribiscono a migliorare l'accessibilità
### Ruoli
- Ogni elmento HTML ha un ruolo implicito
	- Ex. link
- L'attributo *role* permette di rendere esplicito il ruolo di un elemento.
- Definisce qual'è la funzione di un elemento. In molti casi replica il valore semantico dei tag HTML5
	- Ex: *role="navigation" (< nav >), complementary (aside), main, contentinfo (copyright)*
- Oppure altri elementi della pagina
	- Ex: role="banner", "search", "tabgroup", "tab", ecc...
- Quando è possibile sono da preferire i tag HTML5
- alert: indica contenuti che vanno segnalati subito all'utente
- alert dialog: come il precedente ma il focus viene spostato su un elemento al suo interno
- presentation: elimina il significato semantico dell'elemento. Viene usato per nascondere elementi alle tecnologie assistive (ignorato su button e a)
- menubar, menu, menuitem
- img, math
- Lista completa ruoli (W3C editor draft):
	- https://www.w3.org/WAI/PF/aria/roles
### Stati
- Gli stati si definiscono con delle proprietà speciali che descrivono le condizioni correnti degli elementi
	- Ex *aria-disabled="true", aria-relevant="all"*
	- Gli stati, a differenza delle proprietà, possono variare durante il ciclo vitale di un'applicazione, in genere tramite JavaScript

# Regole ARIA
**Prima regola**: se puoi usare un elemento o un attributo HTML specifico, usa quello piuttosto di usare un elemento con significato diverso e aggiunge un ruolo ARIA
- `<main>` e non `<div role="main">`
**Seconda regola:** non cambiare la semantica se non sei davvero obbligato
- `<div role="tab"><h2> testo tab </h2></div>` e non mettere il ruolo nel h2
**Terza regola:** tutti i controlli interattivi *ARIA* devono essere usabili da tastiera
- Ex. assicurarsi che tutto ciò che ha un `role=button` sia raggiungibile da tastiera
**Quarta regola**: non usare `role="presentation" o aria-hidden="true"` su elementi che possono ricevere il focus altrimenti alcuni utenti potrebbero arrivare con il focus su elementi null
- utilizzare `tabindex="-1"`
**Quinta regola:** tutti gli elementi interattivi devono avere un'etichetta accessibile
- `<label>` oppure *aria-label*
La validazione richiede un validatore specifico e il doctype di HTML5
- http://validator.w3.org/nu/

### Accessibilità in pratica: i CAPTCHA
*C*ompletely *A*utomated *P*ublic *T*uring-test-to-tell *C*omputers and *H*umans *A*part:
Test sottoposto agli utenti per garantire la sicurezza di un servizio online discriminando esseri umani dai programmi informatici (bot), permettendo l'accesso ai primi e bloccando i secondi ... *in teoria* :(
-> non sono molto accessibili
![[Pasted image 20231120140939.png]]

## Accessibilità in pratica: regole generali
- il primo passo per raggiungere l'accessibilità di un sito web è utilizzare l'HTML in modo semanticamente corretto
- Utilizzare gli standard web e non soluzioni proprietarie
- In generale i layout fluidi o elastici per loro natura facilitano l'accessibilità di un sito web
- Evitare:
	- frame
	- applet
	- mappe immagine, specialmente lato server
	- tutto ciò che fa riferimento a caratteristiche spaziali (ex. i menù a cascata che devono essere visitati con i tab)
### Validazione dell'accessibilità
- Occorrono sia strumenti automatici che la revisione umana tramite test di utilizzo
	- I metodi automatici sono rapidi e convenienti ma non riescono a identificare tutti i problemi di accessibilità #copertaCorta
	- La revisione umana è più efficace ma costosa. Può assicurare la chiarezza di linguaggio e la facilità di navigazione
#### Alcuni metodi di validazione
- Usare uno strumento di accessibilità automatico e uno di validazione browser
- Validare la sintassi (HTML, CSS, etc.)
- Validare i fogli di stile
- Usare differenti browser grafici (*con suoni e immagini caricati/non caricati, senza mouse, con script, fogli di stile e script non caricati*) browser vecchi e nuovi
- Usare browser o emulatori solo testuali (**Links**)
- Usare uno screen reader, software per ipovedenti (magnifier), un display piccolo etc...
- Usare i controlli automatici di spelling e grammatica
- Rivedere la chiarezza e la semplicità del documento
- Invitare persone con disabilità a revisionare i documenti
##### Strumenti commerciali
- Firefox Web Developer Toolbar
- Chrome Device Emulation
- Silktide-> estensione Chrome che emula diversi tipi di disabilità
- Total validator
- Wave di Webaims
- ARC Toolkit
###### Che cosa devo testare?
Purtroppo le linee guida e le leggi, pur essendo molto chiare sugli obiettivi, non lo sono altrettanto sui test da fare

### Accesibilità e usabilità
- Garantire l'accessibilità da un punto di vista tecnico non è abbastanza per rendere un sito facile da utilizzare. La vera questione è se gli utenti possono ottenere quello che vogliono da un sito web in un tempo ragionevole e se la visita è piacevole (*J.Nielsen*)
- Accessibilità *non* è sinonimo di usabilità, ed è fondamentale sottolineare che non può esserci usabilità senza accessibilità. Un sito web progettato per ridurre le barriere all'accesso non ottiene, quale effetto secondario, un abbassamento delle barriere dovute a scarsa usabilità
#### Definire l'usabilità IEE & ISO
- _“La facilità con la quale un utente può imparare ad operare, a predisporre l’input
e a interpretare l’output di un sistema o di una componente”_
- _“L’efficacia, l’efficienza e la soddisfazione con la quale determinati utenti
raggiungono scopi specifici in determinati ambienti.” 

- **EFFICACIA**: l'accuratezza e la completezza con la quale determinati utenti raggiungono scopi specifici in determinati ambienti
- **EFFICIENZA:** rapporto tra le risorse impiegate e l'accuratezza e la completezza degli scopi raggiunti
- **SODDISFAZIONE**: il confort e l'accettabilità del sistema rispetto agli utenti e ad altri soggetti condizionati dal sistema stesso

#### Definire l'usabilità
- _“L’usabilità è la misura della qualità dell’esperienza dell’utente che interagisce
con qualcosa – un sito web, un’applicazione software tradizionale o qualsiasi altro
artefatto con il quale l’utente può operare con specifiche modalità.” [J. Nielsen]_

## Requisiti emergenti di web-usability (Visciola)
- Maggiore attenzione al fatto che il web è attualmente un contenitore di informazioni e servizi. 6 requisiti emergenti:
1. **Navigabilità:** esistenza di un sistema di navigazione che aiuti a orientarsi nel sito e a cercare informazioni
2. **Utilità attesa**: la disponibilità nel sito di informazioni che corrispondano alle aspettative degli utenti
3. **Completezza dei contenuti:** la presenza di informazioni a livello di dettaglio desiderabile per gli utenti
4. **Compresibilità delle informazioni**: la forma e la qualità con cui l'informazione viene presentata nel sito 
5. **Efficacia comunicativa:** misura la credibilità del sito, la pertinenza delle informazini rispetto al profilo del ssito
6. **Attrattività grafica:** la qualità del layout grafico del sito

