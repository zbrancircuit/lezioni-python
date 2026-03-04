<h1> Concetti di base, essenziali per comprendere tutto il resto: </h1>
<h3>La funzione print():</h3>
Mostra il determinato contenuto (inserito tra le parentesi () della funzione) come output, risultando fondamentale nella visualizzazione delle informazioni nel terminale.

```python
print("Ciao a tutti!")
```

<h3> Le STRINGHE: </h3>
Sono composte da caratteri, e si possono segnare con " o con ', a seconda delle esigenze, a patto che venga utilizzato lo stesso simbolo come apertura e chiusura. 
<br> <br> Es.: "Ciao" o 'Ciao', non "Ciao' o 'Ciao".    

<h3> Le VARIABILI: </h3>
Sono essenziali per mantenere e fare riferimento ai valori in tutta la nostra applicazione. Memorizzando un valore in una variabile, possiamo riutilizzarlo tutte le volte e nel modo che preferiamo durante il progetto. Sono come delle scatole con etichette, nella memoria del computer, dove l'etichetta rappresenta il nome della variabile mentre il contenuto della scatola è rappresentato dal valore contenuto (assegnato) nella variabile.
<br> <br> Es.:

```python
Colazione = "Fette di pane integrale con burro d'arachidi"
print("A colazione mangio " + Colazione + ".")
```
L'output in questo caso sarà: "A colazione mangio Fette di pane integrale con burro d'arachidi".

<h4> ATTENZIONE: </h4>
Il computer legge da destra verso sinistra e dall'alto verso il basso, quindi ogni singola volta che assegniamo un nuovo valore alla variabile rimpiazziamo completamente il vecchio valore!

<h3> Gli INTERI e i FLOAT: </h3>
- Un intero è un numero intero, cioè un numero che non ha parte frazionaria. Ad esempio, 5, -10 e 0 sono tutti esempi di interi. Python supporta interi di dimensioni arbitrarie, il che significa che non ci sono limiti predefiniti per quanto grande o piccolo può essere un intero;
<br>
- I float sono invece i numeri con la virgola. Ad esempio, 5.1, -10.7 e 0.5 sono tutti esempi di numeri restituiti da una funzione float.

```python
      int_1 = 27
      int_2 = 31
      float_1 = 7.6
      float_2 = 13.54
```

<h3> La funzione str(): </h3>
Converte un determinato valore in una stringa.
<br> <br> Es.:

```python
int_1 = 750
str_1 = str(int_1)
print(str_1)
```
Il risultato sarà la stringa di testo "750"!

<h3> La funzione int(): </h3>
Converte un determinato valore in un intero, eseguendo arrotondamento per eccesso o per difetto.
<br> <br> Es.:

```python
    float_1 = 750.4810457
    int_1 = int(float_1)
    print(int_1)
```
Il risultato sarà 750, un numero intero!
<h3> Le OPERAZIONI ARITMETICHE: </h3>
<h4>Addizione (+): </h4>

```python
      Addizione = 13 + 13
      print(Addizione)
```
Il risultato è 26!
<h4>Sottrazione (-): </h4>

```python
      Sottrazione = 26 - 13
      print(Sottrazione)
```
Il risultato è 13!
<h4>Moltiplicazione (*):</h4>

```python
      Moltiplicazione = 6 * 6
      print(Moltiplicazione)
```
Il risultato è 36!
<h4>Divisione (/): </h4>

```python
      Divisione = 45 / 5
      print(Divisione)
```
<h4>Potenze (**): </h4>

```python
      Potenza = 4 ** 4
      print(Potenza)
```
Il risultato è 9.0, 9 se usassimo int()!

<h4> Esempio mischiato: </h4>

```python
      Operazione_1 = 25 * 68 + 3 / 28 * 2
      print(int(Operazione_1))
```
Il risultato sarà 1700! Sarebbe stato 1700.2142857142858 se non avessimo utilizzato int()!

<h3>L'OPERATORE MODULO %:</h3>
Si segna con % ma non significa una percentuale. In Python, come nella maggior parte dei linguaggi di programmazione, ha un significato diverso: è chiamato "operatore modulo" e restituisce il resto della divisione tra l'operando di sinistra e quello di destra. In pratica, viene utilizzato per ottenere il resto di una divisione. La sintassi di base è: " a % b ".
<br> <br>Es. 1:

```python
      primo_valore = 269 % 10
      print(primo_valore)
```
Il risultato sarà 9, in quanto il resto della divisione è 9!
  
Es. 2:

```python
      secondo_valore = 270 % 10
      print(secondo_valore)
```
Il risultato sarà 0, perché la divisione non ha resto!

<h3>La CONCATENAZIONE di STRINGHE:</h3>
-

<h3>L'OPERATORE +=:</h3>
-

<h3>Le STRINGHE MULTILINEA:</h3>
-















  
