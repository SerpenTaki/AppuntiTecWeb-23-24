- Creato in risposta a XHTML 2, che sembrava fare le stesse cose della versione precedente del linguaggio in modo diverso, mentre si voleva qualcosa più orientato alle applicazioni web
- **WHATWG**: _Web Hypertext Application Tecnology Working Group_, coordinati da **Ian Hickson** 2004. 
	- Web Forms 2.0
	- Web Apps 1.0
- W3C HTML 5 Working Group: parte dalle specifiche prodotte dal **WHATWG**

## introduzione
- HTML5 è il primo linguaggio di Markup realizzato da produttori di browser e non da esperti di informatica
- è pensato per accelerare lo sviluppo di applicazioni web che vanno a rimpiazzate prodotti desktop
	- calendari
	- gestori di mail, documenti, foto
	- ...
- e tecnologie proprietarie
	- Microsoft Silverlight
	- Adobe Flex

#### Innovazioni introdotte
- Regole sintattiche meno stringenti
- Gestione  standard degli errori
- **canvas**: un'area di disegno interattiva
- **video, audio**: non rende necessaria la presenza di un plug-in
- Iterazione con le API
- Gestione della posizione tramite **GeoLocation API** del W3C
- Javascript multithread
- Pagine modificabili dall'utente
- Possibilità di usufruire delle pagine/applicazioni, anche in modalità off-line
- Possibilità di accedere in modo sicuro ad un database locale
- Non si parla più di elementi deprecati ma obsoleti


# Elementi di un sito Web (!!Importante!!)

- **Comportamento**: codice (*JS & php*)
- **Struttura**: testo (HTML)
- **Presentazione**: Immagini ([[CSS]])

è estremamente **importante** separare questi 3 elementi
```HTML
<html>
<head>
	<script>
	..
	</script>
	<style>
	...
	</style>
</head>
<body>

</body>
</html>
````

## La sintassi XHTML
- i tag e gli attributi sono case sensitive (tutto minuscolo)
- i tag devono sempre essere chiusi (anche se sono vuoti)
	- `<br/>` e non `<br>`
	- per compatibilità con i vecchi browser va usata la forma `<p></p>` per i tag non vuoti (anche se privi di contenuto)e `<br/>` per gli elementi vuoti
- i tag devono essere aperti e chiusi nell'ordine corretto
- I valori degli attributi vanno riportati tra virgolette doppie 
- tutti gli attributi devono avere un valore
- un elemento in linea non può contenere un elemento di blocco
I browser cercano di visualizzare *al meglio* codice non valido, ma questo può portare ad interpretazioni arbitrarie.

### HTML5
- Una delle critiche mosse a XHTML era la rigidità della sua sintassi
- HTML5 supporta sia la sintassi di tipo HTML che la sintassi di tipo XML
- Il problema del codice non valido, viene risolto istruendo i browser su come comportarsi in caso di codice non valido
	- definisce una gestione degli errori standard
	- obiettivo molto ambizioso e allo stato attuale non raggiunto -> usare sempre codice valido
#### Elementi che i Browser ignorano
- I browser ignorano completamente:
	- le interruzioni di linea non identificate con `<br/>` e non contenute in un tag `<pre>`
	- tabulazioni e spazi multipli
	- tag `<p>` nidificati
	- tag sconosciuti
	- commenti
		- ATTENZIONE: all'interno di un commento non è possibile inserire la stringa "--" (doppi trattini)
### Dichiarazione di tipo documento
````HTML
<!Doctype HTML PUBLIC"//W3C//DTD XHTML 1.0 Strict//EN" "http://www.w3.org/TR/xhtml1-strict.dtd">

<!DOCTYPE HTML>

````
- Questa prima riga viene solitamente generata in modo automatico dall'editor HTML specifico, non è obbligatoria, ed ha il compito di informare il browser che si tratta di un documento html relativo alle specifiche (in questo caso XHTML 1.0 Strict) e qual è la lingua primaria
- è necessaria quando si vuole validare la pagina web tramite un validatore
- Se non si specifica un doctype valido, i browser passano in modalità "*quirks mode*"
##### Namespace e lingua
**Namespace**: collezione di tipi di elementi e nomi di attributi
````HTML
<html xmlns="http://www.w3.org/1999/xhtml" xml:lang="it">

<html lang="it">
````
- per ragioni di accessibilità si deve definire la lingua principale del documento
- Si può fare lato server o con (xml:)lang 

- anche il content type può essere definito lato server tramite l'uso di uno script
- HTML5: <meta charset = "UTF-8" />

Il charset deve essere definito entro i primi 512 caratteri quindi il charset va definito per **Primo**
ad oggi si usa utf-8 che è quello più grande e rappresenta anche i caratteri cinesi e giapponesi ed è anche presente per tutti i browser .

**RICORDA VA DEFINITO PER PRIMO ALTRIMENTI SI LASCIA LA SCELTA AL BROWSER E POTREBBE ESSERE CHE SE ENTRI IN UN SITO ITALIANO IN DANIMARCA I CARATTERI SI SPUTTANANO**

### Intestazione
- La parte contenuta tra i tag <head> e </head> viene chiamata intestazione o semplicemente *head*
- In questa sezione si trovano tutti i tag che impartiscono direttive al browser quali: titolo (obbligatorio), comandi meta, richiami ai fogli di stile, script.
- Tutto ciò che si trova all'inteno della struttura head non sarà visualizzato ma interpretato dal browser. La sezione *head* quindi è una zona destinata ad uso esclusivo dei soli comandi che impartiscono direttive ben specifiche

###### Cosa va messo?
- **title** (_obbligatorio_), **link, meta, base, style** e **script**
- **link** definisce un collegamento ad una risorsa esterna ([[CSS]], shortcut icon, etc...)
	- attributi più comuni: **href , rel** (relazione)
- **base** definisce la posizione di base per i collegamenti

#### I tag META
- La sezione head contiene una serie di comandi, chiamati *MetaComandi*, che non producono alcuna variazione visiva sulla pagina, ma sono indispensabili per altre attività quali la validazione e la lettura da parte dei motori di ricerca.
- I metacomandi inseriscono informazioni aggiuntive sul contenuto del documento che si sta creando, come ad esempio l'autore
- Non esistono limitazioni sul numero di metatag inseriti
- ci sono 2 tipi di tag meta:
	- http-equiv (refresh o redirect, expires "usati per i carrelli amazon")
	- name (usati per inserire informazioni anche di terze parti) *google bombing*

### Tag meta name
- inseriscono informazioni riguardanti il documento
- è possibile creare valori propri
- **description**: breve descrizione dei contenuti della pagina web. è utile quando la pagina contiene poco testo (statistiche)
- **keywords**: lista di parole chiavi separate da una virgola
- **copyright**
- **author**
- **robots**: utilizzato per prevenire l'indicizzazione di una pagina. Valori: index, noindex, follow, nofollow, all, none
- **rating**: classificazione del contenuto

###### Introdotti da HTML5
Il tag **Viewport** può contenere nel content anche *initial-scale, minimum-scale, maximum-scale e user-scalable*

Tag viewport: con l'avvento dei cellulari i browser da telefono prendevano la pagina web facevano zoom out e la ficcavano nel telefono "illegibile", con wiew port si risolve questo problema e si evita di avere il testo e le immagini messe a cazzo


## Corpo del documento
- La parte contenuta tra i tag <body> e </body> viene chiamata corpo del documento o *body*
- Questa sezione contiene la pagina vera e propria o almento quello che si vedrà a video. Qui vengono inserite immagini, suoni, filmati, testo, link etc...
- La sezione *body* contiene tutti i tag che descrivono la *struttura* del documento *non* devono essere usati elementi relativi alla *presentazione visuale*
	- si devono usare gli elementi per il loro significato e non per come vengono visualizzati dai browser (``<em> vs <i>``)
### Gli attributi comuni
- Possono essere utilizzati nella maggior parte dei tag. Sono divisi in 3 classi
	- core
	- i18n
	- attributo evento
- Gli attributi *core* sono: *class* (specifica la classe di appartenenza),  *id* (_funziona come un'etichetta per fare riferimento ad un tag in modo univoco_), *title* (_aggiunge un titolo ad un elemento_) e *style* (istruzioni [[CSS]] in linea)
- Gli attributi *internationalization* (i18n) sono *dir* (direzione, itr o rtl) e *xml:lang*
- Gli attributi evento rappresentano gli eventi JavaScript: *onclick, ondbclick, on mouse down, onmouseup, etc..*

### Id vs class (domanda esame)
**class**: definisce un gruppo di appartenenza
**id**: definisce un elemento univoco: non ci possono essere più tag, se si trovano id uguali il validatore da errore
- In assenza di regole di stile ad essi associati, *div* e *span* non alterano in alcun modo la visualizzazione del contenuto
- *class* definisce un gruppo di appartenenza mentre *id* identifica un elemento in modo univoco
- Dare un *id* ad un elemento permette di usarlo:
	- come selettore in un foglio di stile
	- all'interno di uno script
	- come ancora di destinazione di un link
	- come strumento generico nel trattamento dei dati
- Un id deve cominciare con una lettera con il carattere *underscore*. Per utilizzarlo all'interno di Javascript non sono ammessi spazi, apostrofi e punteggiatura

#### I tag generalisti
- `<div>...</div>`
	- L'elemento `<div>` è un contenitore generico per l'associazione con fogli di stile e crea un nuovo blocco. Tutti gli attributi e le associazioni applicate al tag div saranno estese a tutto il blocco di codice interessato.
- `<span>...</span>`
	- L'elemento `<span>` non ha alcuna caratteristica se non quella di fare da supporto per gli stili. Diversamente da *div* è un elemento in linea

Attenzione a usare i div nella maniera corretta!! un div se io devo identificare un blocco che di suo ha una sua funzione, se io ho div come matriosche allora probabilmente sto sbagliando qualcosa, semantica del linguaggio
### Markup Strutturale
- HTML 5 introduce markup in grado di descrivere meglio la struttura interna di un documento
- Nuovi tag:
	- **header, footer**: intestazione e piè pagina di un documento. Possono essere usati più volte nella stessa pagina, anche all'interno delle sezioni. *footer* identifica le informazioni su chi ha scritto i contenuti
	- **main** contenuto principale
	- **nav**: contiene elementi di supporto alla navigazione. Può comparire anche dentro un header
	- **aside**: sidebar, contenuto a parte, supporto, Identifica una parte di contenuto ch epuò essere rimossa senza diminuire il significato della pagina, ma che è legata al contenuto del tag in cui è annidata
	- **Section**: per raggrupare contenuti sullo stesso tema o logicamente collegati
	- **article**: porzione di testo autocontenuto e indipendente del resto del documento che possa essere distribuito in modo autonomo

### Regole del Markup strutturale
- è bene non ricorrere a **section** o **article** per soli motivi di stile o di scripting, in tal caso **div** è preferibile
- **article, nav, section e aside** sono _sectioning element_, ovvero possono contenere **header, nav e footer**
- Per controllare se il documento è strutturato bene una buona possibilità è verificare il sommario generato automaticamente
	- https://gsnedders.html5.org/outliner/
- Se il browser non supporta il markup strutturale esiste una libreria JavaScript che la inerpreta per lui
 ````HTML
<div id = "header">
	<img src="..." alt="logo UniPD"/>
	<div id="headerText">
		<div id = "headerUtility">
			<form>...</form>
		</div>
		<h1> Corsi di laurea in informatica </h1>
		<h2> Sito dedicato ai corsi di laurea in ...</h2>
	</div>	
</div>
 ````
 ````HTML
<header role = "banner">
	<img src="" alt=""/>
	<div id = "headerText">
		<nav>
			<form>...</form>
		</nav>
		<h1> Corsi di laurea </h1>
	</div>
</header>
 ````
### Il testo
- il testo viene inserito tra i tag  `<p> e </p>`
-  `<p>` La lettera p sta per paragrafo.
- Per andare accapo all'interno di uno stesso paragrafo è possibile usare il tag  `<br/>`
-  `<hr/>` inserisce una linea orizzontale
- All'interno del codice html si possono inserire dei commenti che non vengono visualizzati dal browser.  `<!-- e -->`
###### Caratteri speciali
- Dato che le parentesi angolate servono a distinguere i tag xhtml dalle parole del testo, come faccio ad inserire una di queste nel testo della mia pagina?
- Lo stesso problema si pone con tutta una serie di caratteri speciali come lo spazio o le vocali accentate, che vengono indicate con dei codici
-  caratteri che per l'html vogliono dire altre robe ad esempio>< servono per la semantica di codice quindi bisogna definire delle entità,  
- &it, &gt;
#### Cosmesi del testo
- Ci sono 2 tipi di markup: *strutturale e di presentazione*
- All'interno del markup strutturale, possiamo distinguere una insieme di tag che condizionano in qualche modo il contenuto all'interno di essi
- **stili logici**: descrivono il significato, il contesto o l'uso dell'elemento che racchiudono
- Sostituiscono tag della prima formulazione di HTML troppo legati ad aspetti presentazionali
- L'aspetto di presentazione dipende dal browser utilizzato, tuttavia ci sono convenzioni comuni
- Per rendere una pagina più leggibile si fa spesso ricorso ad una specie di cosmesi del testo per dare enfasi ad una parte del paragrafo
	- `<em> </em>` = enfasi
	- `<strong> </strong>` = forte enfasi
- Il modo in cui vengono visualizzati può essere manipolato tramite un foglio di stile
- Sono pensati per sostituire `<i> e <b>`, in quanto migliorato l'accessibilità (sono leggibili da uno screen reader) e contribuiscono a separare contenuto e presentazione

## Intestazioni
- Esistono sei livelli di intestazione: **h1, h2, h3, h4, h5, h6**
- Si devono utilizzare rispettando l'ordine e pensando alla struttura del documento e non a come vengono visualizzati di default infatti la visualizzazione può essere modificata.
	- H1 è il più importante mentre h6 il meno importante, ma h6 è quello che va usato di più perchè h1 va ad indicizzare la pagina e viene riconosciuto subito dal testo
###### Regole per scrivere dei buoni titoli
- Scrivi un titolo unico per ogni pagina
- cerca di essere conciso e descrittivo
- Evita titoli vaghi e generici
- Utilizza la maiuscola per la prima lettera della frase o la prima lettera di ogni parola
- Crea contenuti degni di click ed evita i *clickbait*
- Pensa all'intento di ricerca
- Includi la parola chiave principale quando ha senso farlo
- Massimo 60 caratteri

### Citazioni
- Per riportare un passo e citare l'autore si devono usare i tag **blockquote, q o cite**
- **blockquote** introduce un'ampia citazione che occupa un intero blocco
- **q** introduce una citazione più ristretta in linea
- la fonte può essere indicata tramite gli attributi **cite** o **title** o con il tag `<cite>`
ATTENZIONE: in HTML5 **cite** indica il titolo di un lavoro (libro, film,....)

#### Abbreviazioni, acronimi indirizzi
- **abbr** indica le abbreviazioni 
- **address**: identifica un indirizzo
- **acronym** (solo XHTML) indica gli acronimi

- servono davvero questi tag?
	- Nell'obiettivo di spostarci sempre più verso un web semantico, è bene cercare di strutturare quanto più possibile il testo, aggiungendo informazioni su esso.
###### Altri tag per il testo
- **code**: permette di inserire del codice all'interno di HTML
- **var**: identifica delle variabili nel codice
- **samp**: identifica un particolare output di un programma
- **pre**: permette di inserire testo preformattato, dove spazi, tabulazioni e a capo hanno un valore
- **ins**: identifica un inserimento redazionale. Solitamente è visualizzato sottolineato
- **del**: identifica una cancellazione redazionale. Solitamente è visualizzata barrata
- Possono essere usati sia come elementi in linea che di blocco
###### Altri tag semantici
HTML5 introduce altri tag per caratterizzare altri dati contenuti in una pagina web
- **figure**
- **mark**
- **time** (_con l'attributo **datetime** che contiene la data o l'ora in formato XML_)
- **meter** per indicare una misura in scala che ha un (*min*) ed un massimo (*max*)
- **progress** per indicare un valore che sta cambiando
- **small** per indicare le note a piè pagina, i termini in piccolo dei contratti etc...

###### Elenchi non ordinati
- Elenchi puntati da utilizzare quando vogliamo dei punti per il nostro elenco, senza un ordine ben preciso. Si usa `<ul>` e al suo interno `<li>`
````HTML
Oggi devo comprare:
<ul>
	<li>Mele</li>
	<li>Pere</li>
	<li>Angurie</li>
	<li>Limoni</li>
</ul>
````
apparirà:
Oggi devo comprare
- Mele
- Pere
- Angurie
- Limoni
###### Elenchi ordinati
- Elenchi numerati da utilizzare quando vogliamo dei punti che abbiano una gerarchia o un ordine ben preciso. Si usa `<ol>` e al suo interno `<li>`
````HTML
<ol>
	<li> Prendi il martello </li>
	<li> Metti la mano sul tavolo </li>
	<li> Inizia a martellarti la mano </li>
</ol>
````
apparirà:
1. Prendi il martello
2. Metti la mano sul tavolo
3. Inizia a martellarti la mano

HTML5 aggiunge al tag `<ol>` i seguenti *attributi*:
- **reversed**
- **start**: indica il numero con cui parte la lista
- **type**: specifica il tipo di marcatore
Inoltre aggiunge al tag `<li>` l'attributo value che consente di impostare un numero arbitrario

###### Elenchi di definizioni
- Elenchi in cui non si usa alcun tipo di punto, utili per definire i termini.
- Si usa il tag `<dl>` per iniziare, il termine `<dt>` (*title*) indica il termine da definire nella definizione e per la definizione si usa `<dd>`
````HTML
<dl>
	<dt>Uomo</dt>
	<dd>Essere vivente, amante e desiderante </dd>
</dl>
````
- Ci possono essere zero p più `<dd>` per un unico `<dt>`
Questo tipo di elenco è anche utile per una eventuale barra di navigazione 
- deve essere definito un id per modificare il layout tramite [[CSS]]
## Immagini
Per inserire un'immagine si utilizza il tag `<img src="xxx.yyy"/>`, dove xxx è il nome dell'immagine e yyy la sua estensione.
````HTML
<body>
	<p>Questa è la mia prima pagina web</p>
	<img src="immagini.gif"/>
</body>
````
Attributi:
- **alt** = testo alternativo
- **longdesc**-> deprecato oggi si fa un URL ad una pagina con descrizione dell'immagine
	````HTML
	<a href="descr/smiling-cat.html">
		<img src="cat.jpg" alt = "smiling cat" />
	</a>
	````
- **width** (*larghezza*) ed **height** (*altezza*) fanno conoscere la precisa dimensione dell'immagine al browser prima di scaricarla
###### figure e figcaption
- **figure** e **figcaption** permettono di definire figure e didascalia
- Una figura non deve necessariamente contenere un'immagine
````HTML
<figure>
	<img src="figure.jpg"/>
	<figcaption> Didascalia della figura </figcaption>
</figure>
````
Un'immagine non ha bisogno dell'attributo **alt** se ha associata una didascalia!!!!
### Tag picture
- il tag picture permette di inserire immagini con diversi formati
- Viene usato per design responsivi
-  deve almeno avere un `<img>` e deve essere **messo alla _fine_**
- ma può avere più attributi source
- Serve ed è molto utile perchè possiamo tramite attributo _srcset_ e _media_ il tipo di immagine da usare a seconda della grandezza del display usato (questo è fatto per usare anche meno risorse e ul layout molto gradevole)
## Link
- Per inserire i link si usa il tag `<a>`, ancora.
- Sorgente del link può essere un pezzo di testo (*hot word*) ma anche elementi più complessi come le immagini (*thumbnail*). Destinazione può essere una pagina o una sua parrte.
````HTML
<a href="http://ind_server:8080/path/doc.html#frammento">
	Sorgente del link
</a>
````
- I riferimenti possono essere assoluti o relativi (tag **base**)
- **target** indica il frame di destinazione (*se non esiste apre una nuova finestra*). Nella verisione XHTML **Strict**, **HTML5** si
- HTML5: **media** (*media query*), **download**

### Accesso ad un frammento
- L'accesso ad un frammento avviene tramite la definizione di un **id**
````HTML 
<h1 id="title"/>
...
<a href="#title"> Vai alla sezione title </a>
````
## Accesso ai link da tastiera
- è molto importante che i link siano accessibili anche agli utenti non in grado di utilizzare il mouse
- **accesskey** e **tabindex** indicano rispettivamente un carattere per portare il focus sul link e l'ordine di tabulazione
````HTML
<a href="http://..." tabindex = "1" accesskey = "s">
	sorgente del link
</a>
````
!! NON BISOGNA ANDARE IN CONFLITTO CON LE COMBINAZIONI DEI PROGRAMMI!!

###### Link non ipertestuali
- Richiedono una configurazione del browser che deve aprire il programma corretto
- Mail:
	- *mailto:username@domain*
	- <a href="mailto:utente@dominio.it">scrivimi</a>
	- Esistono delle funzioni addizionali supportate solo da alcuni che permettono di preimpostare alcuni parametri
- FTP link
	- <a href="ftp:/7server/pathname">...</a>
- Altri
	- <a href="file://server/pathname">...</a>
	- <a href="news:newsgroup">..</a>

# Tabelle

- Le tabelle servono per tabulare colonne di dati. (**E solo per QUESTO motivo)**
- Purtroppo sono spesso usate come contenitori di testi e immagini portando a codice di bassa qualità 
- Una tabella si crea con il tag `<table>`. `<tr> e <td>` indicano, rispettivamente, le righe e le colonne. Intere tabelle possono essere a loro volta contenute in celle di altre tabelle, che vengono quindi nidificati come scatole cinesi.
````HTML
<table>
	<tr>
		<td> qui andrà messo il contenuto della tabella </td>
	</tr>
</table>
````
Nel passato lo scarso supporto del [[CSS]] da parte dei browser ha promosso l'uso di tabelle per l'impaginazione. Questa pratica ha portato a diversi problemi:
- accessibilità con dispositivi non visuali
- lentezza nel caricamento dei dati
- struttura e contenuto non separati, ma entrambi presenti nei dati

### Regole per le tabelle
- Non ci possono essere righe senza celle al suo interno.
- Le colonne non si definiscono in modo esplicito ma si definiscono le celle all'interno delle righe tramite gli elementi *td*.
- Si possono definire celle che occupano più di una colonna (*colspan*) o più di una riga (*rowspan*)
- è possibile creare delle intestazioni per le colonne (o per le righe) con gli elementi *th* al posto di *td*
- il tag *caption*, posto subito dopo il tag *table*, permette di inserire un titolo
- La struttura della tabella in passato veniva descritta nell'attributo *summary* oggi rimpiazzato da un riferimento contenuto in un *aria-describedby*

````HTML
<!--Esempio colspan-->
<table>
	<tr>
		<td colspan="2"> cella 1</td> <!--occupa 2 colonne-->
	</tr>
	<tr>
		<td>cella 2</td>
		<td>cella 3</td>
	</tr>
</table>
````
````HTML
<!--Esempio rowspan-->
<table>
	<tr>
		<td rowspan="2">cella 1</td> <!--occupa 2 righe-->
		<td>cella 2</td> 
	</tr>
	<tr>
		<td>cella 3</td>
	</tr>
</table>
````
è possibile raggruppare alcune righe suddividendo la tabella in header, body e footer. Quando la tabella viene interrotta in qualche modo header e footer vengono ripetuti (non IE).
````HTML
<table>
	<thead>
		<tr>..</tr><tr>..</tr><tr>..</tr>
	</thead>
	<tfoot><!--Notare come il foot sia definito prima del body-->
		<tr>..</tr><tr>..</tr><tr>..</tr>
	</tfoot>
	<tbody>
		<tr>..</tr><tr>..</tr><tr>..</tr>
	</tbody>
</table>
````
possiamo volendo definire una class="alternative" per dare maggiore visibilità alle righe
````HTML
<table>
	<thead>
		<tr><th>1 col</th><th>2 col</th><th>3 col</th></tr>
	</thead>
	<tbody>
		<tr><td>Dato 1</td><td>Dato 2</td><td>Dato 3</td></tr>
		<tr class="alternative"><td>Dato 4</td><td>Dato 5</td><td>..</td></tr>
		<tr>..</tr>
	</tbody>
</table>
````
#### Indirizzare le colonne
Sebbene le tabelle si costruiscano per righe, è possibile indirizzare le colonne, per creare effetti di layout ad esse associati
- **colgroup** consente di applicare attributi ad un set di colonne identificato dall'attributo *span* (simile a *rowspan* e *colspan*)
- **col** permette di selezionare una singola colonna

# I FORM
"*Se l'economia fa girare il mondo, allora i form fanno girare il Web*" *XHTML & CSS, P. Griffit*
````HTML
<form action="" method="post"> <!--elementi del form--> </form>
````
- L'attributo method può avere 2 valori, *get e post*
- Metodo **get**: è il predefinito. Viene utilizzato per leggere dati. Il browser allega la *stringa di query* all'url del programma CGI
	- http://servet/path/file.cgi?parametro=valore
	- limite alla lunghezza della stringa
	- vulnerabilità dell'accesso
- Metodo **post**: viene utilizzato per inviare dati. La stringa di query viene passata come input standard 
	- maggiore facilità di gestione
### Formato della stringa di query
- Contiene i dati inviati cliccando il pulsante *Submit*
- Il nome e il valore di ciascun elemento della form sono codificati come assegnamenti
- I caratteri speciali sono codificati sottoforma di numeri esadecimali preceduti da %
	- Ex. lo spazio è rappresentato %20: *Nome= Mario%20Rossi*
- Con il metodo **get** la pagina di destinazione può essere salvata come bookmark in modo da poter ripetere la query senza reinserire i dati
- Se si usa il metodo *get* la stringa viene inserita dal server in una variabile d'ambiente
- Se si usa il metodo *post* si deve leggere la stringa di query dall'input standard

### Campi e pulsanti dei form
- Gli elementi inseriti in una form si inseriscono con soli 3 tag:
	- input 
	- textarea
	- select
### Attributi per elementi dei form
- **name**: serve per identificare l'input inviato al server. Ogni elemento viene inviato come una coppia nome/valore. Il nome si ricava da questo attributo, il valore è l'input inserito dall'utente in quel campo.
- **readonly="readonly"**: i campi con questo attributo non sono editabili dall'utente.
- **disabled="disabled"**: i campi con questo attributo non sono editabile dall'utente. *il valore di questo campo non viene inviato al server*

### Il tag input
- Questo tag permette da solo di creare diversi elementi di una form a seconda del contenuto dell'attributo *type*:
	- **text**: una singola riga di testo con **maxlength** elementi
	- **password**: una riga di testo offuscata
	- **checkbox**: un semplice on/off
	- **radio**: per selezionare una o più opzioni
	- **submit**: pulsante per inviare i dati del modulo
	- **reset**: pulsante per inviare i dati del modulo
	- **hidden**: per dati  non visibili o non editabili
	- **file**: per caricare file
	- **button**: per richiamare script lato client
	- **image**

**ESEMPIO** testo e password
````HTML
<form action=""><fieldset>
	<legend>Text and Password</legend>
	<label for="username">Username:</label>
	<input name="username" id="username" value="20"/>
	<lavel for="password">Password:</label>
	<input type="password" name="password" id="password" value="Password" maxlength="20"/>
	</fieldset></form>
````
### Fieldset e label
- In caso di form molto lunghi, il tag **fieldset** permette di raggruppare elementi logicamente correlati: operazione in genere agevola la loro compilazione.
- Il tag *legend* permette di inserire una intestazione. è situato subito dopo il tag di apertura `<fieldset>`
- La visualizzazione predefinita riquadra l'insieme di elementi con un bordo con la legenda che interrompe il bordo superiore.
- Il tag *label* associa un'etichetta ad un campo del form non necessariamente adiacente con *id* il valore dell'attributo *for*

### Checkbox vs radio
- I pulsanti di scelta *radio* permettono la selezione di un'unica voce, mentre i pulsanti *checkbox* permettono una scelta multipla
- *checked='chechked'* permette di specificare lo stato iniziale del pulsante di scelta
- Se un pulsante *checkbox* non è selezionato non viene inviato al server, altrimenti viene inviato il valore *on* associato al nome del controllo oppure il valore dell'attributo *value*, se presente
- Per i pulsanti di tipo *radio* è obbligatorio definire l'attributo *value*, che viene inviato al server in caso di selezione

### hidden
- I tag input di tipi hidden non vengono visualizzati nel form e non possono in alcun modo interagire con l'utente
- Possono essere usati per:
	- passaggio dati in modo da non richiederli all'utente in una sequenza di form
	- salvataggio di informazioni calcolate sulla base dei dati inseriti dall'utente (ex. id)
	- definizione di variabili

### File
- consente all'utente di selezionare un file dal proprio computer
- Se viene usato un tag input di tipo *file*, il tag form di apertura deve contenere l'attributo `enctype = "multipart/form-data"` che comunica al server che si stanno inviando dati non solo testuali
- Non può essere usato con metodo `method="get"`

## Il tag textarea
- Permette all'utente di inserire testo più lungo di una riga
````HTML
<textarea rows="20" cols="40" name="message">
	scrivi qualcosa qui
</textarea>
````
- Gli attributi *rows* e *cols* sono **obbligatori** e *textarea* ha un tag di apertura e uno di chiusura


## Il tag select
- Permette di creare elenco di dati, in genere visualizzato come menù a tendina su cui effettuare una o più scelte
````HTML
<select name="book" id="book">
	<optgroup label="Campus">
		<option>The Outsider</option>
		<option>The Rebel</option>
	</optgroup>
	<optgroup label="Orwell">
		<option>Animal Farm</option>
		<option>1984</option>
	</optgroup>
````
- Per impostazione, viene visualizzata solo la prima opzione. Con l'attributo *size* si può modificare questa scelta
- Viene inviato al server la coppia nome del tag select/contenuto del tag option scelto, o valore del suo attributo value se presente


## Innovazioni per le form
- Al tag `<form>` vengono aggiunti i seguenti attributi
	- *target*: indica dove visualizzare la risposta
	- *autocomplete*
	- *novalidate*
- E i seguenti tag:
	- *keygen* per generare le chiavi per un sistema crittografico
	- *menu* per i menu contestuali
	- *output* che funge da segnaposto per i risultati di un calcolo
- Al tag `<input>` vengono aggiunti i seguenti valori per l'attributo *type*
	- *number* (inserisce 2 freccette per aumentare o diminuire il valore ma rimane editabile), *range*
	- *color*
	- *email*
	- *url*
	- *tel*
	- *search*
	- *datetime, datetime-local, date, month, time, week*

#### Nuovi attributi per i controlli
- required
- formnovalidate
- pattern: contiene un'espressione regolare per la validazione dell'input
- placeholder: contiene un suggerimento
- autocomplete, autofocus
- spellcheck
- min, max, step
- multiple

meglio mettere la label dopo la input. **Non usare la tabella per l'impaginazione** ora non sono più accettabili perchè oggi ci sono le grid e le flex che sono dedicate proprio per il layout della pagina.

## Tag "nocivi" P. Griffiths
- sono tag che si occupano di aspetti di presentazione o tag non validi
- Presentazionali: b, i, big, small, marquee, blink, u, tt, sub, sup, center, hr etc...
- Altri: applet e embed (si deve usare object), font, frame, frameset, iframe etc..

**Attenzione**: HTML5 permette l'uso di **iframe** (ingloba servizi di terze parti tipo la mappa di google maps) e di **small**

## Maggiori innovazioni 

### Canvas
- è un elemento bit-map che permette di disegnare degli elementi e quindi l'uso di immagini animate. Senza l'uso di flash !!!
- Deve essere usato in maniera appropriata (ad esempio non per disegnare un header)
- è necessario impostare dei fallback
**PRO**:
- unico modo per generare immagini dinamiche
- buona alternativa a SVG
**CONTRO:**
- se usate troppo appesantiscono il caricamento della pagina
- Non utilizzano il DOM
- Non sono accessibili perchè gli screen reader si basano su DOM

##### Cosa si può fare
- disegnare forma, testo, linee e curve
- Creare gradienti e pattern
- Copiare immagini, immagini di un video e altri canvas
- Manipolare i pixel
- Esportare il contenuto di un canvas in un file statico

#### Canvas & JavaScript
- Tutto ciò che viene fatto nelle canvas viene realizzato tramite JavaScript
	- Canvas 2D API

HTML5 permette la riproduzione di file audio in modo nativo

`<audio src="song.mp3" autoplay loop controls/>`

HTML5 permette di supportare la riproduzione di file audio/video in modo nativo 
`<video width="320" height="240" controls="controls" poster="img.jpg">`

## Lavorare in locale
- per salvare i dati di un client prima si potevano utilizzare i cookies ma questi erano molto limitati
- HTML5 offre 3 diverse alternative *Web Storage, Web SQL Database e IndexedDB*
	- **Web Storage** offre 2 oggetti sessionStorage e localStorage che memorizzano i dati sottoforma di coppie `<nome, valore>`
	- **Web SQL Database** è un database relazionale
	- **IndexedDB** si basa su una memorizzazione basata su oggetti indicizzati molto veloce ed efficiente

## Lavorare Offline: cache manifest
- La crescente diffusione dei dispositivi mobili richiede la necessità di sviluppare applicazioni che possono lavorare offline, ovvero senza un costante collegamento alla rete
	- Gmail, Calendar
- Il download delle risorse che saranno disponibili anche in assenza di rete avviene in modo trasparente all'utente
- Il file `. manifest` chiamato anche *cache manifest* elenca le risorse disponibili anche in assenza di connessione alla rete.
- La prima stringa deve contenere la stringa CACHE MANIFEST
- I commenti si esprimono con # e devono apparire su una riga a parte
- Il file è organizzato in sezioni:
1. sezione Cache:
	- pagine che posso lavorare in locale e continuare di interagire anche se la rete non c'è
2. sezione Network:
	- pagine che possono lavorare solo se c'è la rete internet
3. Fallback:
	- feedback per non avere un errore 404

