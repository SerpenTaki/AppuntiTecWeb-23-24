# Search Engine Optimization
- Tutto quello che facciamo parte da una ricerca
	- Una risposta alla domanda che abbiamo
	- Se vogliamo acquistare qualcosa
- Si definisce **SEO** tutte le attività di ottimizzazione di un sito web volte a migliorarne il posizionamento nelle pagine dei risultati dei motori di ricerca (Google, Bing)
- **SERP**: *S*earch *E*ngine *R*esponse *P*age

### Ottimizzazione di un sito
- Processo di ottimizzazione di un sito web si può dividere in tre fasi (*non necessariamente sequenziali*):
	1. Ottimizzazione tecnica -> questa attività permette ai motori di ricerca di *accedere* e *indicizzare* i contenuti
	2. Creazione dei contenuti
	3. Promozione dei contenuti -> tutte le attività volte alla raccolta di link da siti autorevoli

# Fattori importanti per il posizionamento
- I fattori che influenzano il posizionamento si dividono in 2 categorie
	1. Fattori Interni *Comunque importanti da non sottovalutare*
	2. Fattori Esterni
		- Inbound link
		- Link Baiting
		- Link popularity

### Fattori Interni
- **Utilizzo delle keyword nel tag title**
- **Meta tag description**
- **Utilizzo corretto delle intestazioni (_h1, h2..._)**
- **Attributo alt**
- **Velocità di caricamento**
- **Qualità di scrittura del codice**
- **Eliminazione di link errati**
- **Mai contenuti duplicati**
- **Ancora del link attinente al testo**
- **_Social sign_**
#### Effetti
- Con la sola aggiunta dei metatag *"keywords" "description* alcune pagine che non figuravano nemmeno tra le prime 30 posizioni sono balzate e si sono mantenute in *prima*.
![[Pasted image 20231120094334.png]]
- Purtroppo questi miglioramenti erano visibili solo su *Yahoo!*

*Diana A smith* sito fatto in css, opere rifatte in css
#### Titoli unici
![[Pasted image 20231120094546.png]]
### Ottimizzazione di title e description
- Ottimizzazione del metatag title:
	- Massimo 55 char, spazi inclusi
	- Inserire una parola chiave all'inizio
	- Scrivere in modo accattivante
- Ottimizzazione del metatag description
	- Massimo 145 caratteri, spazi inclusi
	- Deve essere breve, meglio se include una *call to action*
	- Deve contenere delle parole chiave
## Formattazione Corretta del testo
- Esistono 6 livelli di intestazione: *h1, h2, h3, h4, h5, h6*
- Si devono utilizzare rispettando l'ordine e pensando alla struttura del documento e non a come vengono visualizzati di default. La visualizzazione infatti può essere modificata
- Un corretto uso delle intestazioni facilita:
	- la comprensione della struttura del documento sia agli screen reader che ai motori di ricerca
	- La navigazione da parte di tutti gli utenti, in particolare gli utenti non vedenti
- La marcatura del testo ha generato, nel tempo, molte cattive abitudini:
	- uso del tag `</br>`
	- modifiche allo stile dei paragrafi per simulare le intestazioni, 
	- ...
- La marcatura del testo deve corrispondere al significato semantico dell'elemento in essa racchiuso
````HTML
<body>
	<p class="titolo">...</p>
	<p>...</p>
	<p class="sottotitolo">...</p>
</body>
````

Google offre uno strumento che permette di vedere la velocità di caricamento: *PageSpeed Insights*
[[HTML5#Cosmesi del testo]]
[[HTML5#Citazioni]]
[[HTML5#Abbreviazioni, acronimi indirizzi]]

![[Pasted image 20231120095828.png]]
### Elenchi e navigazione
- Una barra di navigazione è essenzialmente un elenco di link
````HTML
<ul>
	<li>HOME</li>
	<li>Azienda</li>
	<li>Prodotti</li>
</ul>
````
- Deve essere definito un id per modificare il layout tramite CSS
#### Consigli per l'alberatura
- La struttura del sito deve essere il più possibile piatta, in modo che tutte le pagine siano raggiungibili in pochi click
- In alternativa le pagine più rilevanti devono essere ai livelli superiori dell'albero di navigazione in modo che ricevano più collegamenti
- Una struttura il più possibile piatta migliora anche l'esperienza utente
	- mappa mentale

## Fattori Esterni
- Inbound link
- Link baiting
- Link popularity
- ##### Attenzione!
	- i motori di ricerca hanno subito negli anni molti attacchi, quindi si sono fatti sempre più furbi
	- Se si tenta di manipolare malamente i fattori sia interni ma soprattutto esterni si rischia di essere bannati (*minimo 6 mesi*)

## Conclusioni
- Il processo di SEO è un processo complesso che coinvolge molti fattori di un sito web 
	- Se considerato fin dalle prime fasi di sviluppo e [[Progettazione di un sito Web]] è più semplice
- SEO è un processo continuo, in cui i risultati positivi di un web designer diventano i risultati negativi di un altro

