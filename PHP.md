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
...

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
