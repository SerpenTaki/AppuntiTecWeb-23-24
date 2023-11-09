# Il linguaggio HTML

- HTML (HyperText Markup Language) è un linguaggio per la costruzione di ipertesti. è un linguaggio di markup: descrive in modo molto preciso al browser come deve apparire una pagina web
	- 1992: prima versione HTML
	- 1994: HTML 3.0 diventa uno standard
	- 1997: Recommendation HTML 4.01 del W3C
- Elasticità e la semplicità di HTML ha favorito lo svilluparsi di editor WYS/WYG che hanno portato a risultati graficamente molto accattivanti, ma di bassa qualità (tecnica del :"_costruisci adesso paga il prezzo più tardi_")
	- pagine non accessibili, spreco di banda, code forking

## La guerra dei browser
- HTML appartiene alla famiglia dei linguaggi **SGML** (non *XML*) ma è molto più semplice.
	- inizialmente non permetteva frame né immagini
- Per prendersi più utenti, i browser hanno cominciato ad inserire nel linguaggio nuovi tag proprietari
	- **img** (_Netscape_) vs **object** (_MS Internet Explorer_)
	- **blink** (Netscape) *testo lampeggiante*
	- **marquee** (IE) *testo scorrevole*
- La guerra tra browser ha portato un arricchimento delle possibilità offerte ma anche problemi di incompatibilità
- HTML 4.01 non risolve del tutto il problema

1998: Il W3C lancia il *Web Standard Project* (**WaSP**) per spingere Netscape, Microsoft e le altre case produttrici di browser a supportare pienamente gli standard
- Successivamente il WaSP si pone anche l'obiettivo di far produrre codice valido agli editor
2000: IE5 per MacOS supporta bene gli standard XHTML, CSS e XML
2001: campagna per aggiornamento browser eliminare: Netscape 4, IE4 etc...

Gennaio 2000: viene definito lo standard XHTML 1.0 successivamente revisionato nel 2002
Luglio 2006: XHTML 2.0 Working draft
- non retrocompatibile
Luglio 2008: diventa raccomandazione XHTML Basic 1.1, una versione pensata per i dispositivi palmari o cellulari

### Problemi di HTML
- crescita disordinata
	- incompatibilità
- Contenuto e aspetto non vengono considerati separatamente
- Numero notevole di pagine web presenti oggi rende difficile qualunque modifica al linguaggio HTML che non sia retrocompatibile

## XHTML 1.1
- **XHTML 1.0** scritto per tradurre il linguaggio HTML in un linguaggio XML
- **XHTML 1.1** elimina definitivamente tutti gli elementi di presentazione
	- il linguaggio viene frammentato in diversi moduli indipendenti. Ogni modulo definisce una caratteristica del linguaggio
		- struttura: head, body, title,...
		- testo
		- form,...
	- ogni modulo viene richiamato solo se necessario

### XHTML vs HTML
- **XHTML** è l'evoluzione del linguaggio HTML. XHTML 1.0 è la versione successiva di HTML 4.01 quindi lo standard corrente
- XHTML è HTML riformulato come XML quindi è più coerente e aiuta lo sviluppo di codice valido. Questo elimina parte dei problemi di presentazione di HTML
- Essendo un linguaggio XML è interpretabile
- Elimina il problema del *code forking* perchè supportato da diversi tipi di dispositivi
	- browser
	- browser per dispositivi mobili
	- screen reader
- I vecchi browser lo supportano abbastanza bene

### XHTML Strict vs XHTML transitional
- **XHTML Transitional**: è la forma transitoria creata per facilitare il passaggio ai nuovi standard da parte degli sviluppatori
- **XHTML Strict**: è la forma più pura che aiuta a produrre codice in cui struttura e presentazione sono fortemente separati
	- svantaggi: non sempre supportato dai vecchi browser

[[HTML5]]

