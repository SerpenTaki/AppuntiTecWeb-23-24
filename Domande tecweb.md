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
