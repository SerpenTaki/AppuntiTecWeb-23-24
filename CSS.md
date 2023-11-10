# Cascading Style Sheet
Parliamo di **Presentazione**

- Il linguaggio CSS permette di applicare aspetti di visualizzazione a documenti HTML
- Consente di avere il pieno controllo degli aspetti visivi delle pagine web separando *presentazione* da *struttura*
- La lettera C (*cascading*) indica che l'informazione sul layout di un documenti può essere strutturata in più livelli e si trasmette, *a cascata*, da un livello a quelli inferiori

### Evoluzione del linguaggio CSS
- 1996: prima specifica del linguaggio CSS1
	- molto limitata
- 1998: definizione di CSS2
	- include funzionalità di posizionamento che permettono di rimpiazzare completamente tabelle e frame nella definizione del layout
- 2002 (circa) inizio definizione di CSS3 tuttora in corso
	- definizione dei moduli
- Attualmente non tutti i browser supportano la versione 3 perciò partiamo dalla versione CSS 2.1
## I fogli di stile 
- è un insieme di regole che indicano il tipo di formattazione da applicare.
- Può essere definito all'interno di un documento HTML, con l'attributo "style" per molti tag, oppure, esternamente in un documento esterno apposito (il foglio di stile vero e proprio), con suffisso .css, utilizzabile da più documenti HTML
### Vantaggi dell'uso del CSS
- Separazione della grafica dalla struttura dei documenti:
- controllo più preciso e completo dell'aspetto grafico
- Manutenzione grafica del sito molto più facile
- Dimensione dei file più ridotte
- Semplice da capire, rispetto a tutti gli attributi degli elementi

# !! NON MESCOLARE LA SEMANTICA CON LO STILE !!
-> Esempio VODAFONE E OMNITEL
-> Non chiamare le classi verde e robe che poi magari diventa rosso e coloriamo di rosso con una classe verde

#### Layout ibridi Tabelle + CSS
*sconsigliato*
- L'adozione delle tabelle per la definizione del layout produce uno schema abbastanza rigido in cui è possibile variare la dimensione di un elemento o nascondere un elemento strutturale
- Non è possibile invece spostare un elemento variando le relazioni spaziali alto-basso e destra-sinistra
#### Possibilità offerte dai layout CSS puri
- I layout CSS puri permettono maggiore libertà nella creazione del layout. Gli elementi possono essere:
	- Affiancanti orizzontalmente o verticalmente e indipendentemente dall'ordine in cui sono definiti
	- nascosti
	- sovrapposti
- L'ordine di definizione degli elementi deve tener conto di diversi fattori:
	- motori di ricerca
	- Dispositivi piccoli: smartphone, tablet

### Regole di sintassi
- Un foglio di stile è un insieme di regole di formattazione
- La sintassi di una regola è:
	- `selettore {blocco di dichiarazioni}`
- Dove il blocco di dichiarazione è un insieme di coppie:
##### 3 tipi di fogli di stile
- inline: non serve il selettore, ed è sconsigliato
	- quando servono? 
		- quando sto facendo esperimenti
- embedded nel preambolo del documento
	- nel tag style nella head
		- funzionano solo su una pagina ma non hanno molto senso
- Esterni:
	- nella head ho il tag link che mi reindirizza ad un file .css
		- possiamo creare fogli diversi anche per i diversi dispositivi.
### Problema del supporto ai nuovi dispositivi
- Usare il valore *handheld* per l'attributo media spesso non era sufficiente per identificare tutti i cellulari di nuova generazione (ed ora è obsoleto)
**Soluzione**:
- `media="screen and (max-width:480px), only screen and (max-device-width:480px)"`
## @ rule (At rule) import
````HTML
<html>
	<head>
		<style type="text/css">
			@import url("file.css")print; <!--indica il media a cui è destinato il foglio di stile->
		</style>
	</head>
	...testo del documento
</html>
````
è preferibile in alcune situazioni rispetto all'uso del tag *link* in quanto consente di nascondere completamente il css ai browser che non lo supportano
- La regola `@import` può essere usata anche dentro un file CSS
##### Soluzione migliore?
- Il tag *link* è compreso dalla maggioranza dei browser, mentre il metodo `@import` funziona solamente nei browser 5.0 e successivi
- il suggerimento è quindi:
	- utilizzare un foglio di stile collegato (*link*) per gli altri stili di base, che possono essere compresi da tutti
	- Utilizzare il metodo `@import` per gli stili sofisticati in modo da nasconderli ai browser più vecchi che farebbero solo confusione
- I fogli di stile incorporati (*embedded*) invece possono essere solo in fase di lavorazione
- Gli stili *in-line* non danno vantaggi sostanziali, ANZI **NON SEPARANO LA STRUTTURA DALL PRESENTAZIONE**

# Regole di applicazione
- Uno stile applicato ad un elemento viene applicato automaticamente anche a tutti i suoi sottoelementi
# Procedimento a cascata
#domandaDaEsame 
Dal basso verso l'alto ordine di applicazione dall'alto verso il basso come vanno messi

1. Impostazioni personali dell'utente
2. **Dichiarazioni definite con _!important_**
3. Impostazioni di stile *inline* definite dall'autore della pagina
4. Fogli di stile *embedded* definiti dall'autore
5. Fogli di stile esterni definiti dall'autore
6. Impostazioni di stile predefinite del browser
`selettore{ proprieta: valore !important; }`

# Selettori
Una classe di CSS è formata da selettori e tra graffe òe caratteristiche e i loro attributi
`selettore{proprietà}`
- **Selettori di tipo:** si riferiscono all'elemento da formattare `p {font-size: 1em}`
- **Selettori di attributo:** valori degli attributi *class* e *id*
````CSS
.grassetto {font-weight:bold} /*seleziona una classe*/
#pblue{color:blue} /*attributo id*/

p.grande{font-size: 2.5em} /*solo p con class="grande"*/
````
- Si possono applicare più classi ad un elemento HTML separandole con degli spazi
`<p class="grassetto grande">...</p>`
- **Selettore universale** `*{font weight:bold}`
- Raggruppamento di selettori
`h1, h2{color:blue; font-size:10pt; font-weight:bold;}`
- Figli e discendenti
	- selettore di discendenza: `p em{...}`
	- Ex: `#nav e #nav div a` la prima contiene la seconda
	- selettore di figli `body > p {..}`
- Selettori di adiacenza
	- `h1+h2{...}`: un'intestazione *h2* che segue immediatamente un elemento h1. Notare che h1 non è influenzato da questa regola

```CSS
header h1, h2 {...}
```
Gli stili qui di h1 contenuti in h1 e **TUTTI** gli h2 (*anche quelli fuori dall'header*) avranno quel tipo di stile da noi definito

**Selettori di attributo**:
`elementname[attributename=attributevale]`
- Permettono di selezionare un elemento sulla base del valore di un attributo dato
- Esempio:
	- `abbr[title]`: tutte le abbreviazioni che hanno attributo title indipendentemente dal valore
	- `abbr[title="mio titolo"]`: tutte le abbreviazioni con attributo title uguale alla stringa "mio titolo"
	- `abbr[title~="mio titolo]"`: tutte le abbreviazioni con attributo title contenente la stringa "mio titolo"

**Ereditarietà e Specificità** #domandaDaEsame 

**Ereditarietà**: ogni figlio eredita le impostazioni del padre
- Se vengono definite più regole con la stessa importanza per uno stesso elemento, l'ultima definita è quella che verrà applicata
````CSS
#nav a{color:orange;} (1,0,1)
a {color:blue} (0,0,1)
/*I link contenuti nell'elemento con id="nav" vengono colorati di arancio perchè la prima regola è più specifica */
````
**Specificità**
- 2 tipi quella con l'uso di important e quella senza uso di important.
` "numero di important"(num id, num attributi, num tag html)` ordine di forza con important si ha 4 elementi su cui calcolare la specificità
- *un id contro 10 classi vince un id*
- *si guardi l'esercizio fatto in classe 18/10/23*

### Pseudoclassi
- Non definisce un elemento ma un suo particolare stato
`a:link:hover{ font-size: 2em }`
`selettore:pseudoclasse{ dichiarazioni }`

Pseudoclasse | Risultato
-------------|-----------
:link | link non visitato
:visited|link visitato
:active|link attivo
:hover|vi si trova sopra il mouse
:focus | elemento attivo (tab)
:first|prima pag per media paginati
:left| pagine di sinistra
:right| pagine di destra
:first-child|prima occorrenza
:lang|seleziona una lingua

### Pseudoelementi
- **C**onsentono un controllo approfondito sui formati tipografici degli elementi dei blocchi
	- es. `p:first-letter {color:red}`

Pseudoelemento|Risultato
-----------|---------
:first-letter|prima lettera di un blocco
:first-line|prima riga di un blocco
:before|testo da aggiungere prima
:after|o dopo un elemento

### Sistemi di misura
- Esistono diverse unità di misura, si dividono in:
	- **relative**: ex, em, percentuale, rem, vh, vw (*oggi super usate*)
	- **assolute**: cm, mm, in, pt, px, pc (oggi è errore usarle se non per casi particolari come:*i bordi div in pixel e forse qualche immagine*)

Unità | Definizione | Esempio 
----------|----------|------
em| Altezza media del font usato|`h1{margin:0.5em}`
px| Numero di pixel nello schermo|`p{font-size:12px}`
in| Numero di pollici (*inch*) 1 in = 2,54cm|`p{font-size:0.5cm`
cm| Centimetri|`p{font-size:0.3cm}`
mm| Millimetri|`p{font-size:3mm}`
pt| Punti (*1pt = 1/72 pollici*)|`p{font-size:12pt}`
pc|Pica {*1 pc = 12 punti*}|`p{font-size: 1pc}`
%| valore percentuale relativo a quello dell'elemento principale| `p{line-height:120%}

### Definizione dei colori
- Colori predefiniti:
	- white, red, green
- Espressi con il formato RGB (Red, Green, Blue)
	- `#RRGGBB`
	- `#FFFFFF` rappresenta il bianco
- rgb(y,y,y) oppure rgb(y%, y%, y%)
	- rgb(255,0,0) o rgb(100%,0%,0%) rappresentano il rosso brillanti
- Ci sono una serie di colori che funzionano su tutti i browser
*abookapart*: libro per scegliere colori e contrasti

## Il testo: la scelta del carattere
- La proprietà *font-family* permette di specificare il tipo di carattere:
	- font-family: Arial, Helvetica, sans-serif
	- font-family: "Time New Roman", symbol
- Differentemente dalla carta stampata, dove il carattere scelto è un punto fisso, su web si deve tener conto che non sempre il carattere scelto è supportato: il browser può visualizzare solo font già installato
- **è buona norma fornire un elenco di font e non uno solo in modo tale da coprire il numero più ampio possibili di situazioni**

!!!**Evitare i font con le grazie come il _Times New Roman_**
--

### I font
possono essere divisi in 2 gruppi:
1. **Proporzionali**: ogni carattere occupa una diversa quantità di spazio
	- più facili da leggere
	- Times, Helvetica, Arial
2. **Lunghezza fissa**: ogni carattere usa la stessa quantità di spazio
	- possono favorire l'impaginazione quando c'è bisogno di incolonnare del testo
	-  Curier e Monaco
**è molto importante privilegiare la leggibilità rispetto ad un font più gradevole dal punto di vista stilistico**

#### Dimensione del testo
- La scelta tra unità di misura assolute o relative per la dimensione del testo di una pagina web è molto controversa
- in linea di principio la dimensione del testo dovrebbe essere specificata in em e non in pixel per questioni di accessibilità. Questa affermazioni però non è sempre vera.
- Se è previsto un foglio di stile per la stampa, questo può utilizzare dimensioni assolute come i pixel (*preferite dai designer provenienti dalla carta stampata*)

interline di 1,5em è il minimo e aiuta le persone con dislessia, inoltre ci sono dei font particolari per le persone con dislessia. [[Accessibilità]]

!!NON USARE MAI IL TAG UNDERLINE!!

##### Se l'autore non specifica font e dimensioni !
- Come per tutte le altre proprietà CSS, in mancanza di una definizione di carattere e dimensione, vengono utilizzate le impostazioni del browser e del sistema operativo (eventualmente modificabili dall’utente)
	- Risultato molto disomogeneo su diverse piattaforme hw/sw
- Lo stesso problema si verifica se il font scelto dall’autore non è presente nel sistema operativo
-  **Attenzione:** anche se il font è installato nel sistema operativo dell’utente, potrebbe essere lievemente dissimile da quello scelto. Inoltre, anche le dimensioni specificate portano in genere a risultati non proprio omogenei a seconda della piattaforma utilizzata

## Dare stile al testo
- Dimensione: `font-size`
- Interlinea: `line-height`
- Sovvrapposizione: `z-index`
- Corsivo: `font-style` (*valore più usato italic*)
- Livelli di grassetto: `font-weight` (bold, normal, border, lighter,...)
- Variante maiuscoletto. `font-variant` (*ex: small-caps*)
- Maiuscolo o minuscolo: `text-transform` (*uppercase, lowercase*)
- Decorazione: `text-decoration` (*underline, overline, line-through, none*)
- Colori: *color* e *background-color* specificano colore del testo e dello sfondo

### Definire tutto insieme: font
- Per ridurre la dimensione del foglio di stile è possibile specificare tutto insieme tramite la proprietà scorciatoia font:
````CSS
selettore{font: font-style font-variant font-weight font-size/line-height font-family}

p{font: italic small-caps bold 0.8em/1.5 arial, Helvetica, sans-serif}
````
**ATTENZIONE**: font reimposta le proprietà non specificate ai valori di default

### Incorporare font esterni
- La regola `@font-face` permette di scaricare ed utilizzare font personalizzati
`@font-face{<descrizione del font>}`
- La descrizione del font contiene delle coppie descrittore: valore dove descrittore può essere:
	- *font-family*: nome da associare al font
	- *src*: local(PERCORSO_LOCALE)/url(URL)
	- *font-style, font-weight, font-variant e font-stretch*
- Attenzione alle licenze d'uso e al supporto dei browser
#### Altri elementi per dare stile al testo
- Distanza tra le lettere: *letter-spacing*
- Distanza tra le parole: *word-spacing*
- Identazione: *text-indet*
- Allineamento orizzontale: *text-align*
- Allineamento verticale: *vertical-align*

## Le immagini e il CSS
- Il CSS può essere utilizzato per definire delle proprietà delle immagini
	- EX: img {border: 0;}
- Le dimensioni possono essere definite sia in HTML che in CSS
	- HTML: è più immediato, ma non consente una completa separazione di struttura e presentazione
	- CSS: completa separazione di layout e struttura, ma il CSS molto pesante (serve una regola per ogni immagine specifica)
- **Tutte le immagini con _sola_ finalità _presentazionale_, dovrebbero essere trattate con CSS**
### Le immagini di sfondo
- Per separare struttura da presentazione, una buona tecnica è inserire le immagini come background di div o altri elementi:
`body {background-image: url(images/miagif.gif);}` allinea l'immagine all'angolo sinistro del documento
##### Altre proprietà:
- *background-attachment:* stabilisce se l'immagine segue il contenuto nello scroll oppure no
- *background-repeat*
- *background-position*
#### Come per i font è possibile usare una scorciatoia per definire tutto insieme:
`selettore{background: background-color background-image background-repeat background-attachment background-position}`
`p{background: #fff url(images/mygif.gif) top left fixed norepeat;}`
**NB** : diversamente da font, l'ordine con cui vengono specificate le proprietà non è rilevante
### Efffetti per il layout: angoli curvi
- Tramite le immagini di sfondo possiamo ottenere diversi effetti di *layout*. Uno di questi è l'applicazione di angoli curvi ai paragrafi.
````HTML
<div><h1>SIFAKA</h1>
	<p><span><span>testo del paragrafo</span></span></p>
	<p><span><span>testo del paragrafo</span></span></p>
	<img src="images/sifaka.jpg" alt="Leaping sifaka"/>
	<p><span><span>testo del paragrafo</span></span></p>
</div>
````
Il CSS da applicare:
````CSS
div{width: 502px; margin:auto;}
p{width: 500px; color:black; padding-top: 30px;
	background:url(images/sifakaptop.gif) no-repeat;
}
p span{display:block; padding-bottom: 30px; 
	background:url(images/sifakabottom.gif) bottom no-repeat;
}
p span span{display: block; background: white; padding 0 30px;}
````
Questa versione di codice non funziona sempre quindi **Usare sempre gli standard**
````CSS
p{
	color: black;
	background-color: white;
	padding: 2em;
	-webkit-border-radius:2em;
	-moz-border-radius:2em;
	border-radius:2em;
}
/*http://border-radius.com/*
````
## Elenchi
- La proprietà *list-style-type* permette di modificare i punti elenco
	- i valori più usati: *none, disc, circle, square*
````HTML
<ul style="list-style-type:disc">
	<li> primo punto </li>
	<li style="list-style-type:square">secondo punto  </li>
</ul> /*cambia i puntini*/
````
Si possono modificare anche gli stili dei punti numerati
- *decimal. lower-roman, upper-roman*
*list-style-image*: per utilizzare un'immagine come punto elenco
#### La scorciatoia per gli elenchi
- *list-style* combina assieme *list-style-type, list-style-position* e *list-style-image*
- Gli elenchi possono anche essere mostrati in orizzontale: `li {display: inline;}`
- Questa proprietà è molto utile per la creazione dei tab

## Box model
- Rettangolo in cui viene visualizzato un elemento:
### Dimensioni di un elmento
- Con *width* ed *height* in realtà non definiamo le dimensioni di un elemento, ma solo del suo contenuto
	- **Ex**. un elemento di dimensioni 100x50 con bordo, padding e margine di 50px su tutti i lati, in realtà misura 400x350px
- Il CSS definisce anche *min-width* e *min-height*
- *overflow*: controlla la visualizzazione del contenuto che sporge dalla dimensione del box. Valori: *visible, hidden, scrool, auto.*
- Gli fondi, sia immagini che colori, occupano l'area del contenuto e del padding
#### Bordi
- Si possono definire:
	- larghezza: `border-top-width, border-right-width`,...
	- stile: `border-style (solid, dotted, dashed,...)`
	- colore: `border-color`
- è possibile utilizzare la proprietà *border* per definire tutti e tre gli elementi su tutti i lati o su uno solo (*border-top, border-right,...*)
````CSS
padding: 1em 1em 1em 1em; /*tutti i lati in senso orario a partire da top*/

padding: 1em; /*tutti i lati*/
border-width: 2px 4px; /*[top e bottom, left e right]*/
margin: 3px 2em 6px; /*[top, right e left, bottom]*
````
#### Margin collapsing
- Se 2 o più margini entrano in contatto lungo l'asse verticale, il più piccolo "collassa", non viene visualizzato
- Questo vale anche tra elementi che si contengono, viene visualizzato solo il margine con valore maggiore
- Per evitare il margin collapsing è necessario definire un bordo o un padding: questi fungono da barriere e i 2 margini non entrano più in contatto
## Display
- Gli elementi si dividono in 2 gruppi:
	- di blocco (*div, p....*)
	- di linea(*em, span..*)
- è possibile modificare questa caratteristica tramite la proprietà display
- *display:none* impedisce la visualizzazione
	- può essere usato per eliminare alcune parti dalla stampa
	- Non è utile per le pagine per i non vedenti visto che nasconde il blocco anche agli screen-reader
### Proprietà di position e float
Con la versione CSS2 dei fogli di stile è possibile abbandonare completamente l'uso delle tabelle perchè è possibile agire sulla disposizione degli elementi nella pagina.
- Le modalità sono stabilite tramite la proprietà *position*:
	- posizionamento statico
	- posizionamento relativo
	- posizionamento assoluto
	- posizionamento fisso (non supportato da IE 6)
- Proprietà *float*
**CSS3**
- Proprietà *flex*
- Proprietà *grid*

## Il posizionamento statico e relativo
- Il posizionamento *statico* (default) dispone il box secondo il flusso normale
- Il posizionamento *relativo* inizialmente calcola la posizione del box secondo il flusso normale, poi sposta il box delle proprietà top, bottom, right e left. Questo spostamento non ha effetti sul posizionamento dei box successivi.

## Il posizionamento assoluto e fisso
- Il posizionamento *assoluto* estrae i box dal flusso normale e li posiziona rispetto all'angolo superiore sinistro della pagina. I margini di questi box non collassano con gli altri.
- Il posizionamento *fisso* si comporta come il posizionamento assoluto, ma i box non scrollano con il resto della pagina.

### Le proprietà float
- Un box definito fluttuante, si sposta a destra o sinistra rispetto al suo contenitore, e fa in modo che il contenuto circostante gli fluisca intorno e prosegua sotto di esso
- Un box fluttuante si comporta come un box di blocco, indipendentemente dalla proprietà *display*
- La proprietà *clear* fa in modo che il box che la contiene prenda avvio da sotto il/i box fluttuante
	- *clear:right/left* si posiziona dopo tutti i box fluttuanti a destra/sinistra che lo precedono
	- *clear:both* si posiziona dopo tutti i box fluttuanti che lo procedono
- Nuovo in CSS3: *shape-outside*


# Novità del linguaggio CSS3

### Nuovi selettori di attributo
- `elem[attr]` applica la regola ai tag elem che hanno un attributo attr
- `elem[attr="value"]` applica la regola ai tag elem che hanno un attributo attr con valore value
- `elem[attr~="value"]` applica la regola ai tag elem che hanno un attributo attr uguale a una lista di parole separate da spazi che contiene la sottostringa value
- `elem[attr!="value"]` applica la regola ai tag elem che hanno un attributo attr uguale a una lista di parole separate da trattini. La prima parola deve essere uguale a value
- `elem[attr*="value"]` applica la regola ai tag elem che hanno un attributo attr che contiene la sottostringa value
- `elem[attr$="value"]` applica la regola ai tag elem che hanno un attributo attr che termina con la sottostringa value
#### Nuove Pseudoclassi
- `:target` agisce sull'ancora di un link, ovvero sulla destinazione del link alla sua attivazione
- `:enable, :disable, :checked` agiscono sugli input (radio, checkbox o option) delle form quando si trovano nei rispettivi stati
- `:not(selettore)`
- `:default`
...

#### In base alla posizione
- `:mth-child(n)` elemento che l'n-esimo figlio di suo padre
	- `li:nth-child(3)` tutti  i punti elenco che si in terza posizione (terzo figlio di un `ul`)
- `:nth-last-child(n)` elemento che è l'n-esimo figlio di suo padre cominciando a contare dall'ultimo 
- `:nth-of-type(n)` elemento che è l'n-esimo figlio dello stesso tipo di suo padre
- `:nth-last-of-type(n)` elemento che è l'n-esimo figlio dello stesso tipo di suo padre cominiciando a contare dall'ultimo
- `:only-child` elemento che è l'unico figlio di suo padre
- `:only-of-type` elemento che è l'unico figlio di suo padre di quel tipo
#### Esempi con i selettori di posizione
- I selettori di posizione permettono di selezionare più elementi allo stesso tempo
	- `:ntg-child(an+b)`
	- `:nth-child(odd)`
	- `:nth-child(even)`

### Variabili CSS
- Spesso nella definizione del layout ci sono caretteristiche comuni
- Per molto tempo il CSS non ha fornito supporto per le varibili
	- linguaggio di markup e non di programmazione
	- Nascono i preprocessori, che però richiedono i prefissi
- Si definiscono con `--nomeVariabile`
- Si usano con la funtzione `var(--nomeVariabile)`

**LE VARIABILI GLOBALI E LOCALI**
- si definiscono dentro il selettore `:root`
````CSS
:root{ /*definizione variabili globali*/
	--coloreTesto: black;
	--coloreSfondo: white;
	--link: blue;
	--linkVisitati: purple;
}

body{
	color: var(--coloreTesto); /*uso variabile globale*/
	background-color: var(--coloreSfondo);
}

#header h1{
	--coloreTesto: green; /*definizione variabile locale*/
	color: var(--coloreTesto); /*testo sarà verde non nero*/
}
````

### RGBA & opacity
- Il CSS3 definisce un nuovo modello di colori, *RGBA*, che permette di aggiungere il canale *Alpha per l'opacità espressa con valore compreso tra 0 e 1*. 1 vuol dire opaco mentre 0 la trasparenza
````CSS
.semiTrasparente{
	color: rgba(0,0,0,0.5);
}

.elem{
	opacity: 0.5;
}
````

### Le ombreggiature
Per l'ombreggiatura del testo è possibile specificare direzione, raggio della sfumatura e colore:
````CSS
p{
	text-shadow: 10px 10px 10px #999;
}
````
L'ombreggiatura di un elemento ha la stessa sintassi di quella del testo e vi aggiunge l'ingrandimento:
````CSS
.conOmbra{
	box-shadow: 10px 10px 10px 5px rgba(200,200,200,1);
}
````

### Inserire più immagini di sfondo
Lo standard CSS3 permette di inserire più immagini di sfondo tramite la proprietà background, separando i valori con una virgola

````CSS
body{
	background: url(img1.jpg) no-repeat top left,
	url(img2.jpg) repeat-x bottom left,
	url(img3.jpg) repeat-y top right;
}
````

### Transizioni
- CSS3 permette di definire anche delle transizioni. Queste proprietà non sono ancora completamente supportate da tutti i browser
- **transition-property**: la proprietà a cui applicare la transizione
- **transition-duration**: durata
- **transition-timing-function**: funzione che modella l'andamento della transizione (*ease, linear, ease-in, ease-out, ease-in-out, cubic-bezier*)

### Impaginazioni CSS3
- CSS3 definisce tre nuovi modelli di impaginazione
	- Multi-column layout
	- Flexible Box Layout
	- Grid Layout
- Il primo ha un buon supporto da parte di tutti i browser, gli altri è ben supportato sono nei browser più recenti (*attenzione alla retrocompatibilità!*)

### Colonne per il testo
````CSS
.classe{
	column-count:3;
}

.classe{
	column-width:300px;
}
````

-> Problema del layout multicolonna!!!

##### Prima soluzione: inline-block
````HTML
<ul class="cards">
	<li>
		<h2>Card 1</h2>
		<p>Setting item to <code> display: inline-block</code> can help us...</p>
	</li>
	<li>
		<h2>Card 2</h2>
		<p>Setting items to <code>display: inline-block</code> can help...</p>
		<p> This card now has some additional content. </p>
	</li>
</ul>
````
````CSS
.cards{
	margin: 0 -10px;
	padding: 0;
	list-style: none;
}

.cards li{
	display: inline-block;
	vertical-align:top;
	width: calc(33.3333% - 20px);
	background-color: #fff0f6;
	border: 1px solid #fcc2d7;
	margin: 0 10px 20px 10px;
	padding: 10px;
	border-radius: 5px;
}
````

##### Seconda soluzione: display-table
- Si divide la lista in tante liste quante sono le righe
- Si definisce una classe per le liste che identificano le righe
- Si aggiunge un contenitore che racchiuda tutte le liste

- **Giudizio negativo:** migliore risultato visivo ma non c'è più una netta separazione tra contenuto e presentazione
	- Questo tipo di layout è stato introdotto per venire incontro ai designer che erano abituati ad utilizzare le tabelle per il layout
````HTML
<div class="wrapper">
	<ul class="cards">
		<li> <h2>Card 1</h2> <p>...</p></li>
		<li> <h2>Card 2</h2> <p>...</p></li>...
	</ul>
	<ul class="cards">
		<li> <h2>Card 1</h2> <p>...</p></li>
		<li> <h2>Card 2</h2> <p>...</p></li>...
	</ul>
</div>
````
````CSS
.wrapper{
	display:table;
	border-spacing: 20px;
	margin: -20px;
}
.cards{
	margin:0; padding:0;
	list-style:none;
	display: table-row;
}
.cards li{
	display: table-cell;
	vertical-align:center;
	background-color: #fff0f6;
	border: 1px solid #fcc2d7;
	padding: 10px;
	border-radius: 5px;
}
````

## FlexBox (soluzione 3)
- Permettono di ottenere lo stesso risultato di prima senza modificare la struttura
- Il risultato si adatta meglio a qualsiasi dispositivo usato

````CSS
.cards{
	margin: 0 -10px;
	padding:0;
	list-style: none;
	display:flex;
	flex-wrap:wrap;
}

.cards li{
	background-color: green;
	border: 1px solid black;
	margin: 0 10px 20px 10px;
	padding: 10px;
	border-radius: 5px;
	flex: 1 1 200px;
}
````

#### Proprietà flex
- *flex-direction:* direzione degli elementi flex, per righe o per colonne.
- *flex-wrap:* permette di andare a capo
- *flex-basis:* definisce la larghezza (*seflex-direction:row*) o l'altezza (se G*flex-direction:column*) di un elemento. Se 0 lo spazio viene distribuito a seconda di flex grow.
- *flex-grow:* se uguale a >= 1 l'elemento può crescere per coprire lo spazio rimasto
- *flex-shrink:* se uguale a >= 1 l'elemento può occupare meno spazio di quello definito inizialmente
- *flex:* proprietà scorciatoia flex:flex-grow flex-shrink flex-basis

#### Allineamento
*align-items:* dove si allineano i vari elementi (*align-self* è riferito solo a sè stesso)
- *flex-start*: top del contenitore
- *flex-end*: bottom del contenitore
- *center*
- *stretch*: riempie il contenitore
*align-content*: richiede *flex-wrap: wrap* e agisce sull'asse y quando il contenitore è più alto dello spazio richiesto dal contenuto. Valore di default: *stretch*

Con tutte queste proprietà i layout flex e grid possono essere equivalenti, ma non è equivalente il supporto dei browser

#### Grid Layout
- Permette di creare una griglia bidimensionale in cui inserire degli elementi
- Sono strumenti molto potenti
- L'unità di misura utilizzata è *fr*, un'unità di misura creata appositamente per le griglie perchè si adatta al layout. è definita come una *frazione dello spazio disponibile*
````CSS
.cards{
	display: grid;
	grid-template-columns: 1fr 1fr 1fr;
	grid-gap: 20px;
}
````

##### Proprietà grid
*grid-template-columns*(*/rows/areas*): permette di definire template per righe/colonne/aree bidimensionali. In pratica si definisce il numero di righe/colonne *align-items, align-self*.
*justify-items, justify-self:* (valore di default *stretch*)
*repeat, auto-fill* (numero di colonne in base allo spazio da occupare, *auto-fit* espande le colonne per riempire tutta la riga)
````CSS
.wrapper{
	display: grid;
	grid-template-columns: repeat(auto-fill, 200px);
}
````

###### OSSERVAZIONI
- Il layout che usano *flex* e *grid* possono diventare molto complicati
	- è indispensabile che il codice sia valido
	- Attenzione a non eliminare le liste preferendo un insieme di div
	- Attenzione  che se l'ordine fisico è diverso dall'ordine visualizzato, la navigazione con tab segue l'ordine fisico
- **Problema del supporto:**
````CSS
@support(display:grid){
	//per i browser che supportano grid
	.container{
		display:grid;
	}
}
````

# Quanto costa il mio sito?

- Ogni volta che aggiungiamo immagini, aumentiamo il tempo di download, e quindi il rendering, del sito. Questo vuol dire aumentare i costi per l'utente finale
- https://whatdoesmysitecost.com/ permette di vedere il costo del sito nei diversi paesi del mondo
