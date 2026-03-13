<h1> I cicli: </h1>

Per capire velocemente cosa siano i cicli, dobbiamo innanzitutto partire con un esempio: ipotizziamo di dover utilizzare svariate volte la funzione print():

```python
print("Questo sarebbe molto più semplice da fare utilizzando i cicli!")
print("Questo sarebbe molto più semplice da fare utilizzando i cicli!")
print("Questo sarebbe molto più semplice da fare utilizzando i cicli!")
print("Questo sarebbe molto più semplice da fare utilizzando i cicli!")
print("Questo sarebbe molto più semplice da fare utilizzando i cicli!")
```
Gli output in questo caso saranno righe di testo, identiche, in fila: "Questo sarebbe molto più semplice da fare utilizzando i cicli!" x5. <br>
Per adesso ne abbiamo scritte soltanto 5, ma immaginiamo di dover utilizzare print() per migliaia di elementi! <br>
È proprio qui che ci vengono in soccorso i cicli (in inglese "loop"), permettendoci di eseguire un blocco di codice ripetutamente. <br> <br>
Esistono diversi tipi di cicli/loop, ma i principali sono **for** e **while**.

<h2> I cicli for: </h2>

Il ciclo for è un particolare ciclo che eseguirà la nostra sezione di codice per un numero preimpostato di cicli. 
<br> Il for utilizza la struttura generale: 
<br> <img width="450" height="55" alt="image" src="https://github.com/user-attachments/assets/e9e21ad9-29ee-4244-a24e-7527ee2948f1" />
<br> L'indentazione del codice (nella seconda riga, dell'azione) è fondamentale! Il codice darebbe un'*IndentationError* altrimenti. Vediamo subito un esempio di ciclo for:

```python
# Lista della frutta disponibile in negozio:
frutta_negozio = ["Mele", "Pere", "Banane", "Mango", "Prugne"]

# Creiamo un ciclo for per avere come output tutto l'elenco della frutta:
for frutta_negozio in frutta_negozio:
  print(frutta_negozio)
```
Gli output in questo caso saranno:
``Mele``
``Pere``
``Banane``
``Mango``
``Prugne``
<br>È stato eseguito un print() per ogni elemento della lista!

<br>Il metodo utilizzato sopra è uno dei possibili modi, ma dobbiamo fare una precisazione: **il nome delle variabili temporanee è arbitrario e non dev'essere definito in precedenza**! Questo ci permette di assegnare qualsiasi nome alle nostre variabili temporanee, per rendere il codice più leggibile. Per es.:

```python
# Esempio nome variabile temporanea 1:

frutta_negozio = ["Mele", "Pere", "Banane", "Mango", "Prugne"]
# Creiamo un ciclo for per avere come output tutto l'elenco della frutta:
for frutta in frutta_negozio:
  print(frutta)
# L'output in questo caso sarà identico all'esempio precedente!

# Esempio nome variabile temporanea 2:
frutta_negozio = ["Mele", "Pere", "Banane", "Mango", "Prugne"]
# Creiamo un ciclo for per avere come output tutto l'elenco della frutta:
for f in frutta_negozio:
  print(f)
# L'output in questo caso sarà identico agli esempi precedenti!
```

<h2> La funzione range() nei cicli for: </h2>

Essa ci permette di creare una lista contenente tanti elementi quanto il numero inserito tra le parentesi. Per es., un "range(10)" genererà una lista con 10 elementi, contenente i numeri da 0 a 9. <br>
Nel caso dei cicli for, la funzione range() risulta utile nei momenti in cui non c'è una lista preesistente sulla quale basarsi per l'esecuzione ripetuta del blocco di codice. Vediamo subito un esempio:

```python
lista_20 = range(20)
for num in lista_20:
    print("Ciao!")
```
Gli output in questo caso saranno 20 righe ``Ciao!``. Possiamo anche impostarlo direttamente come:

```python
for num in range(20):
    print("Ciao!")
# Gli output in questo caso saranno identici all'esempio precedente.
```
Proviamo ora a utilizzare la variabile temporanea per tenere traccia dei vari step del programma:

```python
for saluto in range(5):
  print("Questo è il saluto numero: " + str(saluto))
```
Gli output in questo caso saranno:
``Questo è il saluto numero: 0``
``Questo è il saluto numero: 1``
``Questo è il saluto numero: 2``
``Questo è il saluto numero: 3``
``Questo è il saluto numero: 4``
<br>Se volessimo vedere un conteggio che parte da 1, dovremmo semplicemente addizionare 1 agli output:

```python
for saluto in range(5):
  print("Questo è il saluto numero: " + str(saluto + 1))
```
Gli output in questo caso saranno:
``Questo è il saluto numero: 1``
``Questo è il saluto numero: 2``
``Questo è il saluto numero: 3``
``Questo è il saluto numero: 4``
``Questo è il saluto numero: 5``
<h2> I cicli while: </h2>
I cicli while eseguono il blocco di codice fintantoché la condizione assegnata è vera. 
<br> La struttura generale è: 
<br> <img width="237" height="45" alt="image" src="https://github.com/user-attachments/assets/e4a90ed1-8592-48c7-9899-d2ea62b182e9" />
<br> Anche nei while, come nel caso dei for, l'indentazione è d'obbligo! Vediamo un es. di ciclo while:

```python
contatore = 1
while contatore <= 100:
    print(contatore)
    contatore += 1
```
Gli output in questo caso saranno i numeri da 1 a 100, ognuno nella sua propria riga.
<br> Esprimiamo a parole ciò che abbiamo scritto: "Finché il valore contenuto all'interno della variabile contatore sarà minore o uguale a 100, stampa quel valore come output e, dopo averlo fatto, incrementa il valore contenuto all'interno della variabile contatore di 1." 
<br> Il ciclo while nel nostro caso continuerà fino al numero 100, vista la condizione "minore o uguale a 100", ma una volta superato il 100 la condizione risulterà falsa e il ciclo non si eseguirà più. Vediamo un altro esempio:

```python
contatore = 30
while contatore >= 0:
    print(contatore)
    contatore -= 1
print("Ho finito di contare!")
```
Gli output in questo caso saranno i numeri da 30 a 0 in ordine decrescente, con la frase finale: ``"Ho finito di contare!"``, che verrà stampata come output soltanto dopo che il ciclo while avrà finito di eseguirsi ciclicamente.

<h2>Le Liste nei cicli while:</h2>
I cicli while non sono utili soltanto per contare, essi possono anche essere utilizzati per iterare gli elementi di una lista!

<br> Nel caso volessimo che gli elementi di una lista vengano esposti come output, ordinati uno dopo l'altro, dovremmo assicurarci di impostare in primis una variabile contenete la lunghezza **len** della nostra lista, e in secundis una variabile **index** impostata a 0, in modo tale da poterla incrementare all'interno del nostro ciclo while. Vediamo un esempio per schiarirci le idee:

```python
materie = ["Algebra", "Geometria", "Fisica", "Informatica", "Elettronica"]

len_materie = len(materie)
index = 0

while index < len_materie:
	print("Quest'ora si farà " + str(materie[index]) + ".")
	index += 1
```

In questo caso l'output sarà, su 5 righe distinte: 
``Quest'ora si farà Algebra.``
``Quest'ora si farà Geometria.`` 
``Quest'ora si farà Fisica.``
``Quest'ora si farà Informatica.`` 
``Quest'ora si farà Elettronica.``

<h2>Strutture di controllo nei cicli:</h2>

Le strutture di controllo non sono altre che **if**, **else** ed **elif**! Ricapitoliamo brevemente il loro funzionamento.
<br>
<br>Quando ci troviamo di fronte a due possibili "strade" da seguire, utilizziamo semplicemente l'if e l'else:
- **if**: esegue il blocco di codice se la determinata condizione è vera (*True*);
- **else**: esegue il blocco di codice se la determinata condizione è falsa o se tutte le condizioni precedenti sono false (*False*).
  
<br> Ma quando ci troviamo a dover inserire diverse possibilità, non solo 2, dobbiamo utilizzare l'elif:
- **elif** (else if): esegue il blocco di codice se e solo se la sua condizione è vera (*True*) e se l'if e gli eventuali elif precedenti hanno la condizione falsa (*False*).

<h2>Il break nei cicli:</h2>
Il break è fondamentale quando ci troviamo di fronte a liste contenenti molti elementi, per capirlo al meglio impostiamo subito un esempio. Voglio trovare, all'interno di una lista contenente i numeri da 0 a 100, il numero 39:

```python
# Imposto la lista velocemente con il range()
lista = range(0, 101)
# Imposto il ciclo for, in modo tale da trovare il numero target
for num in lista:
  if num == 39:
	# Se il numero 39 è presente, allora stampa l'output:
    print("Ho trovato il numero che ti interessa, esso è: " + str(num) + ".")
```
L'output in questo caso sarà: ``"Ho trovato il numero che ti interessa, esso è: 39."`` 
<br> Il problema di questo ciclo è in realtà un **problema invisibile**, non possiamo rendercene conto in base all'output. 
<br> La verità è che il nostro ciclo for, nonostante abbia trovato il numero bersaglio 39, continua a lavorare in background fino a quando giunge al termine dell'intera lista. Vediamolo utilizzando print() prima dell'if:

```python
lista = range(0, 101)
for num in lista:
  print(num)
  if num == 39:
    print("Ho trovato il numero che ti interessa, esso è: " + str(num) + ".")
```

L'output in questo caso saranno tutti i numeri fino al 39, poi la frase ``"Ho trovato il numero che ti interessa, esso è: 39."`` e poi tutti i numeri fino al 100! Questo potrebbe diventare un enorme spreco di risorse nel caso in cui ci fossero migliaia e migliaia di elementi presenti all'interno della lista!
<br> Per ovviare al problema, utilizziamo **break**: una volta che il programma incontra il break, il ciclo viene terminato immediatamente! Vediamolo subito:

```python
lista = range(0, 101)
for num in lista:
  print(num)
  if num == 39:
    print("Ho trovato il numero che ti interessa, esso è: " + str(num) + ".")
    break
```
Ora l'output saranno i numeri fino al 39, seguiti dalla frase ``"Ho trovato il numero che ti interessa, esso è: 39."``, abbiamo quindi visto come il break possa interrompere il ciclo una volta trovato il bersaglio, evitando sprechi di risorse!

<h2>Il continue nei cicli:</h2>
È fondamentale nel caso in cui volessimo far continuare il loop soltanto per determinati elementi della lista. Generalmente, come il break, viene utilizzato insieme a qualche condizionale (if, else, elif).
<br>Per es., se avessimo una lista contenenti numeri sia positivi che negativi, e volessimo far funzionare il ciclo soltanto per i numeri positivi:

```python
lista_numeri = range(0, 16)
lista_numeri_2 = range(-25, 0)
#Abbiamo creato due liste, una contenente i numeri positivi da 0 a 15, 
# l'altra i numeri negativi da -25 a 0.

lista_definitiva = list(lista_numeri) + list(lista_numeri_2)
#Uniamo le due liste

for n in list(lista_definitiva):
  if n >= 0:
    continue
  print(n)
#Abbiamo utilizzato il continue
```
Gli output in questo caso saranno i numeri negativi da -25 a -1 (inclusi), perché? <br> Perché, se andassimo a guardare bene l'impostazione del condizionale if, vedremmo che abbiamo posto come condizione "*se il numero è maggiore o uguale a 0*" e successivamente abbiamo utilizzato continue. Il **continue** altro non fa che **salta**re tutti gli **elementi** che **soddisfano** la nostra **condizione**! Quindi i numeri maggiori o uguali a 0 saranno saltati, lasciando in output solo i numeri che non rispettano tale condizione, ovvero da -25 a -1 (inclusi), perché la condizione sarà False!

<h2>I cicli annidati:</h2>
I cicli annidati vengono utilizzati quando vogliamo iterare dei dati su più dimensioni, per esempio all'interno di liste bidimensionali. Ipotizziamo di dover visualizzare alcuni rami di alcune materie, per es.:

```python
rami_materie = [["Algebra", "Geometria"], ["Meccanica", "Termodinamica"], ["Cybersecurity", "Intelligenza Artificiale"]]

for materie in rami_materie:
  print(materie)
```
Gli output in questo caso saranno: 
``['Algebra', 'Geometria']``
``['Meccanica', 'Termodinamica']``
``['Cybersecurity', 'Intelligenza Artificiale']``
<br>Ma se volessimo direttamente visualizzare l'elenco delle discipline, senza suddivisioni per materia principale? Allora dovremmo annidare i nostri cicli! Vediamolo con lo stesso esempio:

```python
rami_materie = [["Algebra", "Geometria"], ["Meccanica", "Termodinamica"], ["Cybersecurity", "Intelligenza Artificiale"]]

for materie in rami_materie:
  for discipline in materie:
    print(discipline)
```
Gli output in questo caso saranno:
``Algebra``
``Geometria``
``Meccanica``
``Termodinamica``
``Cybersecurity``
``Intelligenza Artificiale``
<br>Siamo riusciti in questo modo a stampare tutti gli elementi utilizzando i cicli annidati! <br><br> **ATTENZIONE:** Quando definiamo una variabile temporanea in un ciclo annidato, essa dev'essere diversa dalle variabili definite precedentemente, per evitare di incorrere in bug! <br> <br> Vediamo un esempio più complesso:

```python
liste_numeri = [[7, 9, 11], [20, 24, 28], [5, 25, 45]]
somma = 0
```
Abbiamo impostato questa lista bidimensionale contenente vari numeri, come potremmo ricavare la somma totale di tutti i numeri a nostra disposizione, utilizzando cicli annidati? <br> <br>Soluzione:

```python
liste_numeri = [[7, 9, 11], [20, 24, 28], [5, 25, 45]]
somma = 0

for lista in liste_numeri:
  for numero in lista:
    somma += numero
print(somma)
```
L'output in questo caso sarà ``174``, che è proprio la somma di tutti i numeri a nostra disposizione!
