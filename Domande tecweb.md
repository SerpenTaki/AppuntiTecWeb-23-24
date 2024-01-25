##### Qual è il numero massimo di voci in menù?
Ideale non più di 7, massimo 10. Fino a 7 c'è una certa complessità da parte dell'utente con un numero maggiore di voci la navigazione inizia ad essere complicata e troppo difficile. Inoltre una modifica in profondità *come avviene nei menù a tendina* è facile mentre una modifica in larghezza richiede spazio e se non lo possiedo diventa problematico. Quindi si fanno categorie molto molto ampie, cercando di scongiurare il problema di doverne aggiungerne altre...
##### Quanto può essere profonda una struttura organizzativa gerarchica?
Al massimo 5. La profondità corrisponde al numero di click che servono per passare dalla home alla pagina che ci interessa. Poco profonde e "ragionevolmente" ampia sarebbe l'ideale. Per controllare il numero di click viene fatto un albero della pagina web, si parte dalla home e poi si trovano le pagine collegabili. A mano a mano che si scende i figli rappresentano i link cliccabili in quella determinata pagina. Un albero rappresenta il numero di click nel sito che mi servono per passare dalla home alla foglia.
##### Fare degli esempi di schemi organizzativi ambigui
[[Principi di Web Design#Schemi organizzativi ambigui]]
- Schemi per argomento (*topic*)
- Schemi orientati al compito (*task*)
- Schemi specifici per audience
- Schemi metaforici (*metaphor driven*)
- Schemi ibridi
##### Discutere i metodi utilizzati per rendere una tabella accessibile
[[Accessibilità#Accessibilità in pratica le tabelle]]
##### Differenza tra id e class
L'id permette di definire un'identificatore univoco per un elemento all'interno di una pagina mentre class consente di definire delle classi ed applicarle ad un particolare elemento della pagina. Id può essere usato come ancora di un link e non può iniziare con un numero; generalmente inizia con *underscore* o con una lettera e può essere usato per specificare uno specifico elemento all'interno di un URL. In una pagina di `id` c'è ne deve essere sempre solo **UNO** mentre la class può apparire più volte....
`id` ha un valore maggiore rispetto a class nel calcolo delle specificità. Normalmente `id` viene usato per indicizzare un singolo elemento e quindi a livello di stile specializza ulteriormente la composizione e la separazione *struttura-contenuto* qualora si voglia indicare altro a livello estetico; la classe permette, per lo stesso motivo di considerare gruppi di elementi e modularizzare la costruzione della pagina web sulla base delle esigenze che si hanno.
##### Quali sono le 3 domande più importanti alle quali devo saper rispondere, pena fenomeno del disorientamento?
1) dove sono?
2) di cosa si tratta?
3) dove posso andare?
[[Principi di Web Design#Creazione del contesto tramite impaginazione]]
4) Come sono arrivato fin qui?
5) Da chi è gestita la pagina?
6) Dove posso trovare informazioni più approfondite?
7) Altre informazioni relative al particolare sito web
L'eccesso di collegamenti e di cammini esplorativi può scoraggiare l'utente e fargli perdere di vista lo scopo della ricerca. Il disorientamento è diretta conseguenza dell'avere troppi stimoli (cioè il sovraccarico cognitivo) e occorre sempre domandarsi se in ogni pagina in cui l'utente può rispondersi alle domande precedenti.
##### Le WCAG richiedono di identificare in modo diverso i link visitati da quelli non visitati?
**VERO**, in quanto occorre come informazione aggiuntiva alla domanda "*dove sono?*" tale da aiutare l'utente a distinguere cosa ha guardato da cosa non ha guardato. Il loro colore viene segnato come "convenzione interna" qualora ridefinito dal proprio sito, in quanto abitua l'utente ad una particolare abitudine all'interno del proprio sito; se modificato tale comportamento deve rimanere vero su tutte le pagine.
##### È buona regola segnalare i link che portano ad elementi diversi da pagine web (es pdf.)
Si è una buona regola segnalare i link che portano ad elementi diversi da pagine web, come ad esempio file PDF, in modo che gli utenti siano consapevoli di ciò a cui stanno per accedere e possano decidere se vogliono o meno seguire il link. Ciò può essere fatto utilizzando descrizioni appropriate o utilizzando icone specifiche per tipi di file diversi; l'importante è non tradire le aspettative dell'utente, pertanto devo rispettare quanto sto offrendo allo stesso in quel momento.
##### Le convenzioni interne devono sempre essere rispettate per evitare di disorientare l'utente:
**VERO**, in quanto contribuiscono a familiarizzare con l'utente, creando uno schema mentale utile, tale da farsi una mappa del come navigarlo ed essere invogliato inconsciamente nel suo utilizzo. Ad esempio i link: quelli visitati hanno un colore, quelli non visitati ne hanno un altro.
##### È buona norma segnalare i link che portano a pagine in lingua diversa da quella del sito utilizzando le bandiere nazionali?
**FALSO**. Le bandiere rappresentano il paese non la lingua; È preferibile inserire le iniziali della lingua; Per questo è importante utilizzare un metodo alternativo per segnalare la lingua della pagina, come ad esempio l'utilizzo di codici ISO delle lingue, o di scrittura in caratteri diversi per le lingue diverse. In generale è importante evitare di utilizzare elementi che possono essere percepiti come offensivi o discriminatori e garantire la massima accessibilità per tutti gli utenti.
##### Nascondere anche parzialmente le informazioni del menù con un menù a tendina non è corretto:
**Vero**: nascondere parzialmente le informazioni del menù con un menù a tendina può essere considerato scorretto in alcuni casi, perchè può rendere difficile per gli utenti trovare le informazioni di cui hanno bisogno. In generale è importante che il contenuto sia facilmente accessibile e navigabile per gli utenti. Ciò significa che le informazioni dovrebbero essere organizzate in modo logico e facilmente comprensibile, e che gli utenti non dovrebbero dover fare click su troppi elementi per trovare ciò che stanno cercando. Tuttavia in alcuni casi l'utilizzo di un menù a tendina può essere utile per rendere il layout più pulito e ordinato; sconsigliato innestare tendine che ne aprono altre (*più livelli di tendine*)
##### Che cosa sono le convenzioni interne di un sito web e le convenzioni esterne?
- **Interne**: regole che valgono dentro al nostro sito e non in quello degli altri. Se sono molto particolari vanno spiegate. Queste non devono mai essere rotte.
- **Esterne**: regole generali valide per tutti i siti. *posizione dei link, degli oggetti, link sottolineati*. Tutto il bagaglio culturale che l'utente ha appreso durante la sua esperienza da navigatore.
#### Un test dell'accessibilità può essere fatto in modo esaustivo?
**FALSO**, un test completo per verificare l'accessibilità di una pagina web può essere complesso e richiedere tempo, poichè ci sono molte considerazioni da tenere in conto. Tuttavia è possibile effettuare una serie di controlli per verificare che la pagina soddisfi i criteri di accessibilità.
*Alcune robe da verificare*:
- Utilizzo di etichette e descrizioni appropriate per gli elementi dell'interfaccia utente
- Utilizzo di un contrasto adeguato tra il testo e lo sfondo
- Supporto per la navigazione tramite tastiera
- Possibilità di ingrandire il testo senza che venga compromessa la leggibilità
- Utilizzo di tecnologie assistive come screen reader
- Possibilità di effettuare test su diverse piattaforme e dispositivi
Si comprende che ci sono molti fattori da tenere in considerazione, oltre al fatto che il sito si evolve e occorre costruire pagine in modo tale da essere accessibili sin da subito per facilitare questo processo. Non si può mai sapere per certo se quanto fatto basti effettivamente.
### Mettere in ordine di applicazione gli stili CSS
1. Impostazioni predefinite dal browser
2. Fogli di stile esterni definiti dall'autore (*i file .css*)
3. Fogli di stile embedded definiti dall'autore
4. Dichiarazione di stile definite *in-line* definite dell'autore della pagina
	1. dichiarazioni segnate con marcatura *!important* se presenti
5. Impostazioni personalizzate dell'utente
*L'ordine di priorità di queste è inverso!*
##### Come deve essere il contenuto del tag *title* per essere considerato corretto?
Il contenuto del tag title deve essere dal *particolare al generale*: avendo pochi caratteri a disposizione solo i primi del titolo sarebbero visibili e quindi potrei comunque preservare il contenuto informativo, composto del titolo della pagina/nome del sito e la descrizione della pagina stessa. Esso viene anche utilizzato dai motori di ricerca per comprendere l'argomento della pagina; per questo motivo, dovrebbe stare entro i 70 caratteri al fine di evitare di essere troncato nelle query di ricerca.
##### Il contenuto del tag *description* influenza ricerca SERP? / il contenuto del metatag *description* influenza il posizionamento di una pagina web nelle pagine di risposta dei motori di ricerca?
**NO**, poichè i metatag `description` vengono usati dai motori di ricerca per produrre la descrizione che appare sotto al titolo della pagina nella lista dei risultati prodotta a seguito di una query e influenza la visualizzazione dei risultati non tanto il posizionamento.
#### Che cosa si intende per *responsive Web*?
Detto anche layout a variabilità controllata, identifica i cosiddetti punti di rottura/controllo/breakpoints per definire precisamente gli intervalli di variabilità in cui lo schermo cambia e quindi adattarsi alle varie dimensioni. In particolare ha l'obiettivo di rendere l'esperienza utente ottimale in modo fluido e non dipendente dal dispositivo dell'utente. Questo assicura il contenuto sia sempre leggibile e navigabile.
##### Un tag *input* può essere figlio di un tag *form* (in XHTML)?
**Falso**, in quanto un tag input non può essere figlio diretto di un tag form, può invece comparire correttamente all'interno di un altro tag che possa essere figlio diretto di form, come *fieldset* o *div*.
Di fatto, un elemento come *form* in XHTML può contenere solo elementi di blocco, cosa che *input* non è. Viene consigliato di riportare gli elementi nel *fieldset*; quindi, anche per XHTML5, a domanda si risponda *falso*, dato che è meglio metterlo dentro un tag descrittivo.
#### Le tabelle non andrebbero mai usate per svolgere compiti di layout
**Vero**, dato che questo andrebbe contro il principio di separazione tra struttura e presentazione;
Andrebbero utilizzate solo quando i dati da presentare devono essere riportati in forma tabellare. Si consideri inoltre che possono dare problemi per l'accessibilità.
#### Le tabelle sono un ostacolo alla facile comprensione per le persone con disabilità, quindi andrebbero evitate ove possibile
**Vero**, dato che spesso vengono utilizzate in modo improprio per motivi di layout. Si devono utilizzare quando si ha bisogno di dati in formato tabellare o comunque per organizzare più facilmente le informazioni e renderle comprensibili; normalmente se si intende usarle occorre sfruttarle in modo accessibile (*usando i tag semantici `thead/tbody/tfoot`, usando`scope`oppure gli `headers`, usando il tag `summary`oppure id e un `aria-describedby`usare le abbreviazioni e attribiti lang quando utile...*)
##### I titoli delle pagine contengono informazioni che vanno dal generare al particolare
**Falso**, perchè potrebbe causare problemi di accessibilità; il flusso di informazioni dovrebbe andare dal particolare al generale. Questo aiuta gli utenti a comprendere rapidamente il contenuto della pagina e a orientarsi all'interno del sito ed è anche utile per i motori di ricerca. Inoltre se abbiamo pochi caratteri a disposizione, solo i primi caratteri del titolo sarebbero visibili e quindi andando dallo specifico al generico andrei comunque a "*preservare*" il contenuto informativo.
##### Descrivere la differenza di utilizzo dei metodi GET e POST in una form
[[PHP#HTML per i form]]
**Metodo GET**: è il predefinito. Viene utilizzato per leggere dati. Il browser allega la *stringa di query* all'interno dello stesso *URL*. In questo modo, *chiunque* abbia accesso a questo vede i dati.
- `http://server/path/file.cgi?parametro=valore` (*coppia chiave-valore messo dall'utente*)
- Se si usa il metodo GET la stringa viene inserita dal server in una variabile d'ambiente
- **VANTAGGI**:
	- è possibile fare cache con `get`, sottoforma di *bookmark/segnalibro al link* (perchè i dati, inseriti una serie di volte, possono essere reinseriti allo stesso modo)
	- sono richieste facili da costruire e facilmente condivisibili
- **SVANTAGGI:**
	- limite alla lunghezza della stringa oppure alla lunghezza massima dell'URL
	- devono essere usati solo per recuperare dati e non per modificare i dati sul server, poichè non sono idempotenti (*cioè più richieste identiche possono avere effetti diversi sul server*).
**METODO POST**: viene usato per inviare dati. La stringa di query viene passata come input standard nel *corpo* della richiesta e non è visibile.
- Se si usa il metodo POST si deve leggere la stringa di query dall'input standard nel *corpo* della richiesta e non è visibile.
- **VANTAGGI**:
	- Si possono inviare grandi quantità di dati
	- Sono più sicure, dato che i dati sono non sono visibili negli URL
	- Possono essere usate per modificare tanti dati sul server essendo che sono idempotenti
	- I dati vengono mandati ogni volta (*il browser avviserà l'utente che i dati saranno inviati*)
	- Possono codificare dati in binario.
- **SVANTAGGI**:
	- Sono più complesse da gestire e richiedono più risorse
	- NON vengono salvate in cache e sono anche più lente delle GET
	- Non è possibile salvarle come segnalibro
##### La separazione tra struttura, contenuto e presentazione aiuta il posizionamento nelle pagine SERP
**FALSO**, in quanto non è possibile separare struttura e contenuto, ma si ha tra struttura, presentazione e comportamento; ciò aiuta il posizionamento delle pagine dato che i browser interpretando le informazioni/metadati HTML, sono in grado di valutare "meglio" pagine con tale separazione. Nello specifico una buona presentazione certamente aiuta a livello di formattazione e di esperienza utente, specie quando si adatta a vari dispositivi sulla base del Web Design Adattivo e un buon comportamento, cha a livello di caricamento di pagine e facilità d'uso, influisce a livello di permanenza dell'utente e come primo impatto.
##### L'uso del menù a scomparsa non influisce sull'accessibilità di un sito.
**FALSO**, l'uso dei menù a scomparsa può causare problemi di accessibilità tra cui:
1. se il menù è di scarsa qualità non tutte le sue voci possono essere raggiungibili mediante TAB
2. un menù non ben evidenziato può portare certi utenti a perdere informazioni importanti per la buona fruizione del contenuto. Di fatto oltre a perdere il focus l'ottica usabilità ne è compromessa; la navigazione da tastiera e l'evidenziazione fanno in modo che il contenuto possano essere più facilmente raggiunti.
##### Descrivi quali sono i vantaggi di inserire le dimensioni di un immagine in HTML o CSS
**HTML** :
- Fa conoscere la dimensione dell'immagine al browser (senza scaricarla)
- Ottimizza il caricamento/rendering della pagina, in quanto la specifica delle dimensioni permette al browser di riservare lo spazio necessario per visualizzare l'immagine prima del suo caricamento completo
**CSS**:
- Separazione tra struttura e presentazione definendo attributi custom/personalizzati all'immagine come voluto.
###### L'attributo id si differenzia da class **SOLO** perchè permette di identificare un unico elemento e non un insieme di elementi?
NO (*attenzione al solo nella domanda*)
#### Metodo get nei V/F
- permette di reinviare gli stessi dati al server senza ricompilare la form
- ha un limite nella lunghezza della query string
##### HTML5 definisce una gestione standard degli errori quindi ora non è più importante che il codice HTML sia valido
**FALSO**, tuttora è un problema non ancora risolto. NON esiste infatti un metodo universale di gestione degli errori, dato che i browser stessi e anche i singoli dispositivi (*a seconda della loro età*) possono non interpretare correttamente contenuto non valido e potrebbe comportare problemi al sito per come lo si era pensato
##### Nel caso di specificità con lo stesso valore cosa succede?
Si prende per buona quella definita per ultima
###### Cose utili:
- *struttura/contenuto e presentazione separati*: avvantaggiano nei motori di ricerca e diminuiscono il peso del sito
- *struttura/contenuto e comportamento separati*: non avvantaggiano nei motori di ricerca nè diminuiscono il peso del sito
- *presentazione e comportamento separati:* avvantaggiano nei motori di ricerca e diminuiscono il peso del sito.
Si ha infatti: **Struttura _(HTML)_**, **Presentazione _(CSS)_** e **Comportamento _(PHP, JS)_**.
Il discorso della separazione è perchè tu non vada ad usare JS per fare struttura (*che non verrebbe vista*), o HTML per mettere colori o stili (*che sporcano la leggibiità e manutentibilità del codice*). Di base aggiungere script vari appesantisce il sito ed inoltre c'è il rischio che alcuni browser non riescano a leggerli quindi è meglio separarli così in quel caso la pagina resta accessibile. *NON POSSO* separare struttura e contenuto perchè quest'ultimo è parte integrante della struttura.
### Prova a dare una definizione di accessibilità
L'accessibilità è un insieme di proprietà e regole da seguire per tutelare le varie categorie di utenti, in particolare quelli diversamente abili, rendendoli più facilmente usabile per tutte le categorie da diversi tipi di dispositivi. Più formalmente:"*usabilità di un prodotto/servizio/strumento* per persone con ampio raggio di capacità". Bisogna pensarci dal *primo momento* seguendo buone regole di progettazione; implementarla dopo può essere costoso in termini di tempo e denaro.

#pagina12

##### La validazione del codice HTML e CSS di un sito web è condizione necessaria per garantire la sua accessibilità -> VERO
- È condizione necessaria non sufficiente poichè per arrivare una validazione esaustiva dell'accessibilità di una pagina servono altri controlli (*controllo umano ad esempio*) che si differenziano in base a scopo e contesto.
##### L'uso dei colori non influenza l'accessibilità del sito -> FALSO
L'informazione non dovrebbe mai essere veicolata univocamente attraverso il colore e per questo motivo alcune precauzioni devono essere adottate per garantire che le informazioni siano accessibili a tutti gli utenti, compresi coloro che hanno difficoltà a vedere i colori:
- Ad esempio: è importante assicurarsi che il testo abbia un contrasto sufficiente rispetto allo sfondo per essere facilmente leggibile, e che ci siano alternative testuali per le informazioni presentate solo attraverso i colori. Inoltre è importante testare il sito con diversi sistemi di aiuto per la vista per garantire che le informazioni siano accessibili a tutti gli utenti
#### domanda su. PHP e JS
- Un indirizzo email non si controlla
	- potrebbe non essere corretta perchè non tiene conto di tutte le regole di sintassi valide per gli indirizzi email. Alcune ragioni per cui questa regex potrebbe non essere corretta sono:
		- non verifica se il nome utente (*la parte prima la "@"*) è lungo almeno un carattere e non contiene caratteri non validi come spazi o caratteri speciali
		- Non verifica se il dominio (*la parte dopo la @"*) è lungo almeno 2 caratteri e non contiene caratteri non validi come spazi e caratteri speciali
		- non verifica se il TLD (*estensopne del dominio*) è lungo almeno 2 caratteri e on contiene caratteri non validi
		- Non verifica se l'indirizzo email contiene caratteri di commento come + o . prima della @
		- Non verifica se l'indirizzo email contiene il carattere di coomento. alla fine del nome utente o del dominio
		- Non verifica se l'indirizzo email contiene caratteri di commento ripetuti come ".." o "--"

###### Convenzioni:
INTERNE: sempre rispettate
ESTERNE: possono essere rotte se questo ha un tonaconto (*colore dei link*)


## Metafora della pesca:
- Tiro perfetto -> L'utente sa esattamente cosa sta cercando
- Trappola per aragoste -> L'utente ha un'idea abbastanza chiara ma si aspetta di imparare qualcosa durante la ricerca
- Pesca con la rete a strascico -> L'utente non lascia intentata nessuna possibilità
- Boa di segnalazione -> L'utente vuole ritrovare in un secondo momento qualcosa che ha già letto
#### È sempre possibile usare uno schema esatto per il menù principale -> FALSO
Gli schemi esatti servono quando l'utente sa esattamente cosa sta cercando; L'organizzazione della struttura organizzativa, cioè come i collegamenti sono organizzati tra loro, dipende dal contesto che si vuole creare. Normalmente, una buona strategia può essere quella di adottare uno schema ibrido; si pensi ai siti di notizie, che hanno i principali fatti in ordine cronologico (*schema esatto*) ma organizzazione in categorie contestuali ai fatti più rilevanti o a tematiche di raggruppamento (ambiguo, perchè dipendente dal contesto), per meglio adattarsi alle esigenze dell'utente.
##### È sempre possibile adottare uno schema ambiguo per il menù principale-> SI
Di fatto gli schemi ambigui si adattano al fatto che l'utente non abbia completa conoscenza di ciò che vuole, pertanto questo tipo di schema organizzativo, cioè come sono riportate le informazioni, va sempre bene.
###### Fai un esempio di schema adatto alla navigazione principale specificandone contesta e tipologia
- Schema esatto: ricette ordinate alfabeticamente
- Schema ambiguo: Sito con categorie ordinate per area privato/area azienda, suddivisione per argomenti degli articoli di giornale
### altre domande
- Quale struttura organizzativa è più adatta per la navigazione principale? -> *gerarchia*
- Come deve essere una gerarchia? -> *Deve essere ampia o molto profonda*
#### Quali sono i pregi e i difetti di avere una gerarchia molto ampia o molto profonda?
**AMPIEZZA**
- **PRO**: Buona divisione informazioni e buona varietà, meno click per trovare info, con possibilità e specializzazione per le varie scelte
- **CONTRO**: possibile sovraccarico cognitivo e tempo di caricamento lungo (ci sono tanti contenuti)
**PROFONDITÀ**
- **PRO**: Struttura più organizzata e focalizzata su poche informazioni, accedendo a cose specifiche
- **CONTRO:** Gli utenti possono avere difficoltà a trovare ciò che stanno cercando

#### Datemi una definizione di area sicura
Pixel disponibili per visualizzare l'informazione iniziale di una qualsiasi pagina web *senza scroll* da ogni dispositivo; da questa distinguiamo l'area visibile, cioè la prima vista al caricamento di una pagina. Questi pixel dipendono dal tipo di dispositivo e dalle sue dimensioni/impostazioni; per la stampa corrisponde ai punti di schermo stampabili su supporto cartaceo.
- Di fatto, "above the fold" ed "area sicura" sono la stessa cosa e sono un fattore di grande impatto come prima impressione per l'utente web.
###### Cosa mettere "above the fold"
- tutto, ma non è realistico
	- identidicazione del sito: titolo, logo
	- Parte di navigazione principale: menù o menù hamburger
	- Contenuti informativi più importanti

#### Per la progettazione di un interfaccia mobile si deve considerare un utente come?
poco attento, magari con le mani occupate o in movimento; pensarlo come un occhio e un pollice. *Quindi sarebbe meglio per telefono fare pulsanti grandi e testi grandi*

### Associa ad ogni punto di controllo che hanno uno schermo uguale o inferiore a quel numero di pixel:
- 320px: *piccoli schermi, telefoni usati in modalità portrait*
- 480px: *piccoli schermi, telefoni usati in modalità landscape*
- 600px: *piccoli tablet usati in portrait*
- 768px: *tablet da 10 pollici usati in portrait*
- 1024px: *tablet usati in landscape, piccoli desktop o portatili, o una finestra che occupa non tutto lo schermo*
- 1200px: *schermi grandi, computer ad alta definizione desktop*
#### Il layout a schede va incontro a problemi di manutenzione nel tempo
- Con l'aumentare del numero di schede, può diventare difficile per gli utenti navigare e trovare i contenuti che stanno cercando. Ciò può generare confusione e frustazione e può richiedere uno sforzo significativo per riorganizzare ristrutturare il layout a schede al fine di renderlo più facile da usare
- Quando i contenuti vengono aggiunti, rimossi o modificati, può essere necessario aggiornare il layout a schede per riflettere tali cambiamenti. Ciò può comportare l'aggiornamento delle etichette e del contenuto delle singole schede, nonchè l'aggiunta o la rimozione di schede, se necessario. Questo richiede tempo e un'attenta cura nei dettagli per garantire che il layout a schede rimanga organizzato e facile da usare.
- Possono incorrere in problemi di manutenzione se non sono progettati tenendo conto dell'accessibilità. Ad esempio, i layout a schede possono non essere facilmente navigabili dagli utenti con disabilità visive o non funzionare bene su tutti i dispositivi con schermi piccoli. In questi casi, potrebbe essere necessario uno sforzo significativo per rendere il layout a schede più accessibile a una gamma di utenti più ampia.
#### La divisione tra contenuto e presentazione diminuisce il peso totale di un sito web?
VERO, in quanto consente di separare e ottimizzare i contenuti e le presentazioni in modo indipendente.
Quando il contenuto e la presentazione sono combinati nello stesso file o documento, può essere più difficile ottimizzare ogni aspetto del sito web per le prestazioni. Ad esempio, il contenuto può essere ottimizzato per la leggibilità e la chiarezza, ma la presentazione può non essere ottimizzata per garantire tempi di caricamento rapidi o un uso efficiente delle risorse. Se invece si struttura tutto in modo definito è possibile modificare i singoli moduli e quindi le unità di queste 3 componenti migliorando la definizione di quanto presente in una pagina web.
#### La divisione tra contenuto e layout influenza il pagerank nei motori di ricerca?
**VERO**: è sempre buona norma dividere contenuto e presentazione; questo ha un effetto anche sul posizionamento del sito web perchè i motori di ricerca raccolgono in modo automatico il contenuto della pagina al fine della creazione dei loro indici (*una buona separazione favorisce quindi un miglior posizionamento*)
##### Dare una definizione di linguaggio di markup, descriverne le principali caratteristiche e fornire alcuni esempi di linguaggi markup conosciuti (evidenziando in modo opportuno le differenze)
è un linguaggio formato da regole che forniscono i meccanismi di rappresentazioni (*strutturali semantici e prestazionali*) di un dato strutturato, generalmente un documento quale ad esempio una pagina web. Il linguaggio individua delle parole chiave dette tag (*marcatori*) attraverso cui è possibile esplicitare il significato/funzione di una particolare area di testo.
**Esistono 2 tipi di markup**:
- **STRUTTURALE**: in cui possiamo distinguere *tag* che condizionano in qualche modo il contenuto all'interno di essi. Qui si adottano degli *stili logici*, i quali descrivono il significato, il contesto o l'uso dell'elemento che racchiudono. Questi tag sono principalmente semantici `<h1>, <p>, <ul>, <li>,...`
- **PRESENTAZIONE**: che dipende dal browser utilizzato, tuttavia ci sono delle convenzioni comuni. Esso utilizza etichette/tag CSS come *font-size, color...* per descrivere e definire l'aspetto visivo di ogni pagina.

La distinzione tra i 2 è importante perchè permette di separare la logica del contenuto dalla logica della presentazione, rendendo più facile la manutenzione e la modifica del sito. Inoltre il markup strutturale consente ai motori di ricerca e ai dispositivi di accessibilità di comprendere meglio il contenuto di una pagina, mentre il markup di presentazione consente di adattare l'aspetto visivo del sito a diverse risoluzioni e dispositivi
### Dare una breve descrizione del DOM (*Document Object Model*) in particolare si indichi come questo viene rappresentato e quali sono le sue funzioni principali:
È uno standard del W3C che definisce un modello standard per l'accesso dinamico al contenuto di un documento, consentendone la visualizzazione e l'aggiornamento di contenuto/struttura/presentazione, attraverso un'interfaccia neutrale rispetto ad uno specifico linguaggio di programmazione o scripting. Un esempio classico di utilizzo è l'accesso ad una particolare pagina XHTML. che verrà rappresentata come un albero a valle del "*parsing*" della pagina stessa e che potrà essere visitata o modificata tramite metodi di accesso a ciascun nodo dell'albero.
#### Descrivere la differenza tra linguaggi server side e client side
I linguaggi lato server sono linguaggi di programmazione che vengono eseguiti su un server piuttosto che in un web browser. Vengono utilizzati per costruire siti e applicazioni web dinamiche e sono responsabili dell'elaborazione delle richieste lato server, dell'interazione con i database. Lo scripting lato server è una tecnica utilizzata nello sviluppo web che prevede l'impiego di script su un server web che produce una risposta personalizzata per ogni richiesta dell'utente client al sito web.
PHP, ASP, RUBY

I linguaggi lato client sono linguaggi di programmazione che eseguiti in un browser web piuttosto che su un server. Sono responsabili della gestione delle richieste e delle interazioni sul lato client e sono utilizzati per costruire applicazioni web interrattive e reattive.
ALCUNI LINGUAGGI SONO CSS, C++ e JS

In generale i linguaggi lato server sono utilizzati per gestire la logica e le funzionalità del *back-end* di un sito o di una applicazione web mentre i linguaggi lato client sono usati per gestire il *front-end* e l'interfaccia utente entrambi sono importanti per costruire un'applicazione web funzionale e facile da usare e spesso lavorano insieme per fornire un'esperienza utente senza soluzione di continuità-

#### che livello di accessibilità WCAG richiede la legge italiana ed europea? -> AA (doppia A)
### UN attributo aria-label può essere usato per associare un'etichetta ad un tag input 
**NO** è possibile farlo ma è scorretto, per il tag input esiste già il label che è semanticamente corretto, ma aria-label è il modo di farlo se non avessi nessun altro modo (*aria serve solo a dare semantica solo quando non è altrimenti possibile, in tutti gli altri casi usare i tag semantici*)

