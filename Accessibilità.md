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
14. 
