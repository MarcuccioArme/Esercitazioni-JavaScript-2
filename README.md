# Esercitazioni-JavaScript-2
### Alcuni semplici esercizi per apprendere JavaScript

## Esercizio 1:
### "Frase palindroma"

Realizzare il codice JavaScript che consenta di valutare se una o più frasi (parole) caricate in input, sia (siano) “palindrome”.
<br> Con “palindroma” si definisce una frase (parola) che è possibile leggere da destra a sinistra e viceversa, SENZA CHE NE VENGA DISTORTO IL SIGNIFICATO.
<br> Ad es: “ IN AMOR IO DIFFIDO I ROMANI ”

<br> Lo script deve:
- caricare la (le) stringa (frase);
- visualizzare la frase “normale”;
- visualizzare la frase “letta al contrario”;
- riportare se la frase è o non è “Palindroma”;

### N.B.
Nel caso di inserimento di “frasi”, tenere conto degli “spazi” fra le singole “parole” che compongo la “frase” ...

### Suggerimento:
Utilizzare un ciclo (while, for,..) che, partendo dalla “lunghezza” della frase “normale” (quindi dalla sua fine), carichi in una nuova stringa, carattere per carattere “al contrario”, i caratteri che compongono la stringa “normale”.
<br> Questa nuova stringa sarà quella “letta al contrario”.
<br> Confrontare le due stringhe e riportare in output il risultato.

### Nota:
- La proprietà length contiene il numero di caratteri che compongono una stringa.
<br>Es: lungh_stringa = frase.length --> restituisce il numero di caratteri che compongono la stringa “frase”;

- La funzione "charAt" ha come parametro un numero intero e restituisce il carattere che si trova nella posizione specificata dal parametro.
<br>Es: carattere = frase.charAt(j) --> restituisce il carattere in posizione “j” nella stringa “frase”.

## Esercizio 2:
### "Controllo codice partita IVA"

Realizzare il codice JavaScript che consenta di inserire in un Form, la RAGIONE SOCIALE e la PARTITA IVA di un generico soggetto fiscale.
<br> Lo script deve verificare:
- che la Ragione Sociale NON SIA NULLA;
- che il codice Partita Iva inserito, NON SIA NULLO e SIA CORRETTO
<br> (verificare la correttezza, applicando l’algoritmo di controllo conosciuto).

<hr>

### Algoritmo risolutivo per verifica correttezza P.IVA.
La PARTITA IVA DEVE innanzitutto essere composta da 11 cifre numeriche.

<br> Es: 03828920722
<br>

- Si considerano SOLO le prime 10 cifre;
- Somma delle cifre poste nelle posizioni “DISPARI”:
<br> (posizioni 1/3/5/7/9)
<br> 0 + 8+ 8 + 2 + 7 = 25
- Somma delle cifre poste nelle posizioni “PARI”, ognuna moltipl. x 2:
<br> (posizioni 2/4/6/8/10)
<br> (se la cifra dopo il raddoppio risulta &gt;= 10, va complementata a 9, ossia deve essere sottratto 9 dalla cifra)
<br> (3 * 2) + (2 * 2) + (9 * 2) + (0 * 2) + (2* 2) = 6 + 4 + 18 + 0 + 4 = 6 + 4 + (18 – 9) + 0 + 4 = 23
- Somma TOTALE CIFRE “DISPARI” con TOTALE CIFRE “PARI”:
<br> 23 + 25 = 48
- Il valore ottenuto va arrotondato alla “decina superiore”:
<br> il valore 48 viene arrotondato a 50
- Calcolo della differenza fra valore arrotondato e valore ottenuto:
<br> 50 – 48 = 2;
- Il valore di quest’ultimo calcolo deve essere UGUALE all’ultima cifra (la cifra numero 11) della PARTITA IVA;
- Se risulta VERO dal controllo, la PARTITA IVA “è corretta”
- In caso contrario la PARTITA IVA “non è corretta”

## Esercitzio 3:
### "Calcolatrice"

Realizzare il codice JavaScript che consenta di visualizzare e utilizzare, una calcolatrice che svolga le 4 operazioni fondamentali (+ - * /).
<br> Lo script deve prevedere:
- la casella per visualizzare i valori inseriti ed il risultato
- i numeri da 0 a 9
- i simboli della 4 operazioni
- il simbolo dell’uguale (=)
- il tasto per “cancellare” (C) i valori inseriti e/o il risultato
Tali elementi devono essere inseriti in una tabella di 5 righe e 4 colonne.

### Esempio:
<img src="readmeSrc\calcolatrice.png" alt="Calcolatrice" width="30%" height="30%" style="margin: 1;">
