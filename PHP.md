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
