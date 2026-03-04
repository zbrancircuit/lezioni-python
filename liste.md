<h1>Le liste</h1>

Le liste possono contenere **interi**, **float**, **stringhe**, **booleani** e qualsiasi altro tipo di elemento:
<br> <br> Es.:

```python
lista = ["a", 120, "b", 40, "c", 61, "d", 73.7, "e", True, "f", False, "g"]
print(lista)
```
In questo caso l'output sarà: ['a', 120, 'b', 40, 'c', 61, 'd', 73.7, 'e', True, 'f', False, 'g']

<h2>Il metodo .append()</h2>
Si utilizza per aggiungere elementi alla lista, per es.:

```python
lista = [1, 2, 3, 4]
lista.append(5)
print(lista)
```
    
L'output in questo caso sarà [1, 2, 3, 4, 5], abbiamo effettivamente aggiunto "5" alla fine della lista.

<h2>Il metodo .remove()</h2>
Si utilizza per rimuovere elementi dalla lista, per es.:

```python
lista = [1, 2, 3, 4, 5]
lista.remove(5)
print(lista)
```
L'output in questo caso sarà [1, 2, 3, 4], abbiamo effettivamente rimosso "5" dalla lista.

```python
ordini = ["Mele", "Pane", "Fagioli", "Piselli"]
#L'articolo "Fagioli" viene eliminato dall'ordine:
ordini.remove("Fagioli")
print(ordini)
```
L'output in questo caso sarà: ['Mele', 'Pane', 'Piselli'], abbiamo rimosso "Fagioli" dalla lista.
<h2> Concatenazione di liste </h2>

Quando vogliamo aggiungere molteplici elementi a una lista, possiamo utilizzare + per concatenare due liste, vediamolo con un esempio:

```python
#Ordini iniziali:
ordini = ["rose", "tulipani", "giacinti"]
#Nuovi ordini:
nuovi_ordini = ["lavande", "margherite"]
#Ordini totali:
totale_ordini = ordini + nuovi_ordini
print(totale_ordini)
```
L'output in questo caso sarà: ['rose', 'tulipani', 'giacinti', 'lavande', 'margherite']

<h2> Accedere agli elementi delle liste </h2>

In Python, per accedere agli elementi di una lista, si utilizza l’operatore di indicizzazione `[]`, dove l’indice parte da 0 per il primo elemento. Impostiamo un esempio:

```python
#I nostri lavoratori:
assunti = ["Michele", "Paola", "Rossana", "Luciano", "Maurizio"]
```

Il quarto lavoratore avrà indice 4-1 = 3, in quanto si inizia a contare includendo lo 0:

```python
assunti = ["Michele", "Paola", "Rossana", "Luciano", "Maurizio"]
quarto_assunto = assunti[3]
print(quarto_assunto)
```

L'output in questo caso sarà "Luciano". Di conseguenza il primo assunto avrà indice 0:

```python
assunti = ["Michele", "Paola", "Rossana", "Luciano", "Maurizio"]
print(assunti[0])
```

L'output in questo caso sarà "Michele".

<h3>Indici positivi e negativi</h3>

Gli indici **positivi** sono ordinati dal primo verso l'ultimo elemento, mentre i **negativi** dall'ultimo al primo. Iniziamo con un indice negativo:

```python
lista_spesa = ["pane", "arachidi", "polpette vegane", "banane", "iceberg"]
ultimo_elemento = lista_spesa[-1]
print(ultimo_elemento)
```
L'output in questo caso sarà "iceberg". Proviamo utilizzando un indice positivo:

```python
lista_spesa = ["pane", "arachidi", "polpette vegane", "banane", "iceberg"]
ultimo_elemento = lista_spesa[4]
print(ultimo_elemento)
```
L'output in questo caso sarà nuovamente "iceberg", i due output combaciano, cambia solo la sintassi!

<h2>Modificare gli elementi delle liste</h2>
Per modificare un determinato elemento all'interno di una lista, dobbiamo semplicemente assegnare un diverso valore a quel determinato indice:

```python
#Lista d'attesa
attesa = ["Giovanni", "Paolo", "Riccardo", "Letizia"]
#Qualcuno va via, cedendo il posto a qualcun altro:
attesa[1] = "Roberto"
print(attesa)
```
L'output in questo caso sarà: ['Giovanni', 'Roberto', 'Riccardo', 'Letizia']. 
<br> Possiamo svolgere la stessa operazione ma utilizzando l'indice negativo:

```python
attesa = ["Giovanni", "Paolo", "Riccardo", "Letizia"]
attesa[-1] = "Alessandro"
print(attesa)
```
L'output in questo caso sarà: ['Giovanni', 'Roberto', 'Riccardo', 'Alessandro'].

<h2>Il metodo .insert()</h2>
Viene utilizzato per aggiungere un determinato elemento a uno specifico indice di una lista:

```python
alimenti = ["Mango", "Banana", "Cioccolato"]
#Vediamo il funzionamento di .insert():
alimenti.insert(0, "Ananas")
print(alimenti)
```
L'output in questo caso sarà: ['Ananas', 'Mango', 'Banana', 'Cioccolato']. Possiamo utilizzare anche indici negativi:

```python
alimenti = ["Mango", "Banana", "Cioccolato"]
alimenti.insert(-2, "Pane")
print(alimenti)
```
L'output in questo caso sarà: ['Ananas', 'Mango', 'Pane', 'Banana', 'Cioccolato'].
<br>
Se volessimo utilizzare gli indici negativi dobbiamo fare attenzione: l'indice `[-1]` ci permette di aggiungere l'elemento **1 posto prima dell'ultimo elemento**, non possiamo quindi servirci dell'indice negativo per aggiungere un elemento conclusivo alla lista!

<h2>Il metodo .pop()</h2>
Viene utilizzato per rimuovere un determinato elemento utilizzando il suo indice specifico. Proviamo prima il metodo .pop() vuoto:

```python
argomenti_data_science = ["Machine Learning", "SQL", "Algorithms", "Statistics", "Python"]
argomenti_data_science.pop()
print(argomenti_data_science)
```
L'output in questo caso sarà: ['Machine Learning', 'SQL', 'Algorithms', 'Statistics']. Un .pop() vuoto va a rimuovere l'ultimo elemento della lista!
<br> Proviamo ora con l'indice:

```python
argomenti_data_science = ["Machine Learning", "SQL", "Algorithms", "Statistics", "Python"]
argomenti_data_science.pop(3)
print(argomenti_data_science)
```
L'output in questo caso sarà: ['Machine Learning', 'SQL', 'Algorithms']. Abbiamo rimosso l'indice 3, quindi il quarto elemento della lista!
<br>Proviamo ora con l'indice negativo:

```python
argomenti_data_science = ["Machine Learning", "SQL", "Algorithms", "Statistics", "Python"]
argomenti_data_science.pop(-2)
print(argomenti_data_science)
```
L'output in questo caso sarà: ['Machine Learning', 'Algorithms'].

<h2> Le liste bidimensionali (2D) </h2>

Certe **liste possono contenere altre liste**: è il caso delle liste bidimensionali!

```python
tris = [
          ["X", "O", "X"],
          ["O", "X", "O"],
          ["O", "O", "X"] 
       ]
print(tris)
```
L'output in questo caso sarà: [['X', 'O', 'X'], ['O', 'X', 'O'], ['O', 'O', 'X']].
Ma come facciamo ad **accedere** agli elementi delle liste 2D? Beh, nello stesso modo delle liste normali: dobbiamo indicare innanzitutto l'indice della lista e, successivamente, l'indice dell'elemento in tale lista:

```python
voti_alunni = [["A", 9], ["B", 8.5], ["C", 6.5], ["D", 7]]
voto_B = voti_alunni[1][1]
print(voto_B)
```
L'output in questo caso sarà "8.5", corretto! Vediamo ora il voto di "C", questa volta utilizzando indici negativi:

```python
voti_alunni = [["A", 9], ["B", 8.5], ["C", 6.5], ["D", 7]]
voto_C = voti_alunni[-2][-1]
print(voto_C)
```
L'output in questo caso sarà "7", corretto!
<br>
<br>
Il ragionamento sarà lo stesso anche nel **modificare** una lista bidimensionale:

```python
voti_alunni = [["A", 9], ["B", 8.5], ["C", 6.5], ["D", 7]]
voti_alunni[2][1] = 10
print(voti_alunni)
```
L'output in questo caso sarà: [['A', 9], ['B', 8.5], ['C', 10], ['D', 7]]. Abbiamo modificato il voto di C, facendolo passare da 6.5 a 10!
<br> Vediamo utilizzando indici negativi:

```python
voti_alunni = [["A", 9], ["B", 8.5], ["C", 6.5], ["D", 7]]
voti_alunni[-3][-1] = 6
print(voti_alunni)
```
L'output in questo caso sarà: [['A', 9], ['B', 6], ['C', 10], ['D', 7]]. Abbiamo modificato il voto di B, facendolo passare da 8.5 a 6!

<h2> Le liste consecutive, la funzione range()</h2>

-
