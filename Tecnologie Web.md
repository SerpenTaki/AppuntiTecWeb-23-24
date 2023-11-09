#### Storia
- 1969: il Dipartimento della difesa Americana crea il primo nodo di **ARPAnet** all'UCLA
- '70-'80: Nascita di numerose piccole reti per il trasferimento di file e di posta elettronica. Sono per lo più reti "private"
- 1986: viene creata **NSFnet**, una rete che collegava 5 uni americane, nel 1990 sostituisce ARPAnet per tutti gli usi non militari
- 1990: Tim Berners-Lee inventa il **Web**
- 1992: NSFnet collega circa un milione di computer in tutto il mondo e viene definita la prima versione di HTML
- 1995: si inizia ad usare il nome **Internet** per la parte pubblica di NSFnet
### Internet
- INTERconnected NETworks: reti (di reti) interconesse
- è un insieme di reti eterogenee e connesse in maniera lasca
- Garantisce attraverso il protocollo TCP/IP, una comunicazione affidabile ma non efficiente -> *best effort*
- ISP (*Internet Service Provider*): chi fornisce il servizio di connessione
	- sono a loro volta connessi a fornitori di servizi di comunicazione di più alto livello

-> è importante ricordare che Internet e Web non sono la stessa cosa:
- **Internet** è un infrastruttura tecnologica che permette di far comunicare i diversi computer ( la rete fisica)
- il **Web** è l'insieme di software e protocolli installati sui diversi computer. In senso astratto è un insieme di documenti collegati tra loro.
## HyperText Transfer Protocol
- Nato al CERN, a Ginevra, da Tim Berners-Lee (giu 1999)
- Usato inizialmente per diffondere documentazione di tipo scientifico, in ambito bibliotecario
- Stabilisce una *connessione* tra client e server per lo scambio di documenti
- Ogni documento è identificato da un URL: `http://www.server.net/doc.html`
- I collegamenti possono essere interni ai documenti, fra documenti dello stesso server, fra documenti di server diversi.

#### Richiesta dal cliente Web
- L'utente seleziona un indirizzo URL e lo invia al server
- `GET //www.unipd.it/inf/index.html HTTP/1.1`

- Altri metodi:
	- **POST**: esegue il documento specificato
	- **HEAD**: restituisce l'informazione relativa all'intestazione
	- **PUT**: sostituisce il documento specificato con i dati allegati
	- **DELETE**: elimina il documento specificato
Riceve un documento [[HTML]] e lo visualizza sullo schermo dell'utente interpretando i comandi di marcatura

**Risposta dal server Web**
- riceve una richiesta da un browser 

Versione Http | codice di stato | spiegazione testuale
--------------- | ---------------- | ----------------------
`http/1.1` | 200 | ok

- Dall'URL individua il documento da restituire
- Lo legge dal disco e lo ritrasmette al cliente

Prima cifra | Categoria
----------- | ---------
1|Informativa
2|Successo
3|Reindirizzo
4|Errore del client (404)
5|Errore del server

- La modalità descritta prima si applica in caso di pagine statiche
- Una pagina, o parte di essa potrebbe essere dinamica: in questo caso il server crea "al volo" la pagina richiesta dall'utente sulla base dei dati forniti
## Il W3C
- Il **World Wide Web Consortium (W3C)** è un organismo indipendente che comprende le maggiori ditte produttrici di software per la rete, es.. Google, Intel , Apple, Microsoft...
- Si occupa di proporre standard a largo spettro che comprendono un gran numero di tecnologie ed iniziative che riguardano il Web
	- [HTML], XHTML, CSS, WAI,...
- Le proposte (**_Candidate Recommendation_**) vengono messe a disposizione su Web per raccogliere il numero più alto di contributi. Successivamente diventano standard (_**Recommendation**_)
##### Cosa offre?
- La definizione dello standard **_recommendation_**
- una suit di test per l'implementazione (*testsuite*)
- un servizio di validazione
Tutto offerto in modo gratuito proprio per promulgare l'utilizzo e la diffusione dello standard in oggetto

### L'alba del Web Design
- All'inizio i designer provenivano dall'editoria cartacea
	- output cartaceo fisso: un giornale può essere pensato come un file PDF
- Nell'editoria su web entrano in gioco nuove variabili
	- Sistema Operativo (tipi e font supportati)
	- caratteristiche del dispositivo (schermo, connessione, etc)
	- browser(standard supportati, bug)
- Progettazione per l'ignoto
	- **Far Web** (come luke4316)

#### Dogmi del design tradizionale
- Inalterabilità del carattere tipografico
- Inalterabilità del colore
- Inalterabilità della composizione
// molto pdf
invece:
- variabilità del modello e della versione del browser
- Variabilità del dispositivo utilizzato
- Velocità di connessione
- Preferenze utente
Portano a:
- caratteri varibili
- colori variabili
- composizione variabile

###### Regole generali
- non pretendere di avere l'assoluto controllo sull'output finale
- non cercare di ottenere un'uguaglianza pixel a pixel sui diversi dispositivi nelle diverse situazioni
- **Preferisci**:
	- Design fluidi
	- Accessibilità vs. design visuale accattivante




