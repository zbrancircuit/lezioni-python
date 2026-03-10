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
Quando vogliamo generare una lista di numeri, al posto di scriverli tutti, possiamo utilizzare la funzione range().

Se inseriamo **UN INPUT**: questa funzione prenderà il numero inserito come input e creerà una lista che andrà da 0 fino al numero prima di quello inserito come input. 
<br>
**Attenzione**: quando vogliamo eseguire il print della nostra variabile range, dobbiamo trasformarla in una lista utilizzando la funzione list(). Per es.:

```python
#Esempio da 0 a 8
zero_a_8 = range(9)
print(list(zero_a_8))
```
L'output in questo caso sarà: [0, 1, 2, 3, 4, 5, 6, 7, 8] Abbiamo dovuto mettere un indice grande con un numero in più rispetto all'ultimo numero desiderato nella lista!
<br>

Se invece inseriamo **DUE INPUT**: possiamo far sì che la nostra lista vada dal numero inserito come primo input _fino al numero prima di quello inserito come secondo input_! Per es.:

```python
#Esempio da 5 a 15
range_5_15 = range(5, 16)
print(list(range_5_15))
```
L'output in questo caso sarà: [5, 6, 7, 8, 9, 10, 11, 12, 13, 14, 15]. Sempre attenzione all'indice del numero finale, nel caso del primo non possiamo confonderci!
<br>

Se invece inseriamo **TRE INPUT**: possiamo creare una lista che "salta" determinati numeri. Per es., se creassimo una lista con gli input range(2, 9, 2), avremmo una lista nella quale si salterà di 2 da un numero al prossimo! Quindi l'ordine sarà: numero d'inizio, numero finale (non incluso nel range, il range si ferma come al solito al numero prima!) e il numero di "salti" che deve fare. Vediamolo meglio con un es.:

```python
#Da 0 a 40 facendo salti di 5 tra ogni numero
range1 = range (0, 40, 5)
print(list(range1))
```
L'output in questo caso sarà: [0, 5, 10, 15, 20, 25, 30, 35] Vale la solita regola per il numero finale!

<h2> La funzione len(): </h2>
Molto semplice, la utilizziamo quando vogliamo sapere il numero di elementi all'interno di una lista. Una volta applicato a una lista questo metodo ci mostrerà in output il numero di elementi presenti. Per es.:

```python
#Esempio con print:
lista = [1, 2, 3, 4, 5, 6, 7, 8, 9, 10]
print(len(lista)) #Attenzione alla sintassi!
```
L'output in questo caso sarà "10".

```python
#Esempio con variabile:
inventario =["letto matrimoniale", "letto singolo", "cuscino", "cuscino", "cuscino", "letto matrimoniale", "letto singolo", "divano", "divano", "cuscino"]
inventario_len = len(inventario)
```
In questo caso il valore scritto nella variabile "inventario_len" sarà "10".

<h2> Il processo di splicing: </h2>

Viene utilizzato quando vogliamo estrarre, da una lista, soltanto una porzione di essa. Dividere la lista in questo modo prende il nome di splicing. La sintassi basilare è **lista[start:end]**, dove start è l'indice del primo elemento che vogliamo includere nella nostra selezione, mentre end è l'indice dell'ultimo elemento che vogliamo aggiungere +1 (sempre l'antica regoletta). Per es.:

```python
#Esempio 1:
lista = ["a", "b", "c", "d", "e", "f", "g"]
esempio_slice = lista[1:6]
print(esempio_slice)
# L'output in questo caso sarà: ['b', 'c', 'd', 'e', 'f']

#Esempio 2:
lista = ["a", "b", "c", "d", "e", "f", "g"]
esempio_slice = lista[2:4]
print(esempio_slice)
# L'output in questo caso sarà: ['c', 'd']
```

Possiamo anche utilizzare la sintassi **lista[:n]**, positiva, che ci andrà a selezionare *i primi n elementi della lista*; o la sintassi **lista[-n:]**, negativa, che ci andrà a selezionare *gli ultimi n elementi della lista*. Per es.:
```python
#Esempio 1:
frutta = ["mele", "ciliegie", "ananas", "arance", "mango"]
print(frutta[:3])
#L'output in questo caso sarà: ['mele', 'ciliegie', 'ananas']

#Esempio 2:
frutta = ["mele", "ciliegie", "ananas", "arance", "mango"]
print(frutta[-3:])
# L'output in questo caso sarà: ['ananas', 'arance', 'mango']
```

Esiste anche la sintassi **lista[:-n]** (con i : prima del -n) che ci mostrerà *tutti tranne gli n ultimi elementi della lista*. Per es.:
```python
frutta = ["mele", "ciliegie", "ananas", "arance", "mango"]
print(frutta[:-3])
# L'output in questo caso sarà: ['mele', 'ciliegie']
```
<h2> Il metodo count(): </h2>

Possiamo utilizzare questo metodo quando desideriamo sapere quante volte un elemento n appare all'interno di una **lista**. Per es.:

```python
#Esempio lista 1:
lista = [1, 2, "n", 4, 5, "n", "n", 8, 9, 10, "n", 11, "n", 12]
num_n = lista.count("n")
print(num_n)
#L'output in questo caso sarà "5"!

#Esempio lista 2:
voti = ["Jake", "Jake", "Laura", "Laura", "Laura", "Jake", "Jake", "Jake", "Laura", "Claudio", "Claudio", "Jake", "Jake", "Claudio", "Laura", "Claudio", "Jake", "Jake", "Claudio", "Laura"]
num_voti_jake = voti.count("Jake")
print(num_voti_jake)
#L'output in questo caso sarà "9"!
```

Possiamo anche utilizzare questo metodo per contare le apparizioni degli elementi all'interno di **liste bidimensionali**! Per es.:

```python
#Esempio lista bidimensionale:
collezione_numerica = [[100, 200], [100, 200], [475, 29], [34, 34]]
num_paio = collezione_numerica.count([100, 200])
print(num_paio)
#L'output in questo caso sarà "2"!
```

<h2> Il metodo sort(): </h2>

Possiamo utilizzare questo metodo per ordinare gli elementi di una lista. Il metodo sort() non ha bisogno di essere assegnato a una variabile, in quanto modifica direttamente la lista! Per es.:

```python
#Esempio 1:
lettere = ["f", "b", "d", "a", "e", "c"]
lettere.sort()
print(lettere)
# L'output in questo caso sarà: ['a', 'b', 'c', 'd', 'e', 'f']

#Esempio 2:
indirizzi = ["221 B St.", "42 W. Way", "12 Grimmauld", "742 Terrace", "1600 Ave", "10 St."]
indirizzi.sort()
print(indirizzi)
# L'output in questo caso sarà: ['10 St.', '12 Grimmauld', '1600 Ave', '221 B St.', '42 W. Way', '742 Terrace']

#Esempio 3:
nomi = ["Riccardo", "Valentina", "Federica", "Alberto", "Silvio"]
nomi.sort()
print(nomi)
# L'output in questo caso sarà: ['Alberto', 'Federica', 'Riccardo', 'Silvio', 'Valentina']
```

Possiamo anche andare al contrario utilizzando **"reverse = True"**, per es.:

```python
#Esempio 1:
lettere = ["f", "b", "d", "a", "e", "c"]
lettere.sort(reverse = True)
print(lettere)
# L'output in questo caso sarà: ['f', 'e', 'd', 'c', 'b', 'a'] 


#Esempio 2:
città = ["Londra", "Parigi", "Roma", "Los Angeles", "New York"]
città.sort(reverse = True)
print(città)
# L'output in questo caso sarà: ['Roma', 'Parigi', 'New York', 'Los Angeles', 'Londra']
```

<h2> La funzione sorted(): </h2>

La funzione sorted() differisce dal metodo sort() per due ragioni: 
- Viene inserita prima di una lista, non dopo (come ogni funzione built-in);
- Genera una nuova lista invece di modificarne una già esistente.
<br> Vediamola in pratica con un es.:

```python
# Prendiamo come esempio una lista di giochi:
giochi = ["Portal", "Minecraft", "Pacman", "Tetris", "The Sims", "Pokemon"]

# Utilizziamo ila funzione sorted:
giochi_sorted = sorted(giochi)
# E' stata così creata una nuova lista, ordinata, vediamolo nell'output:

print(giochi)
# L'output in questo caso sarà: ['Portal', 'Minecraft', 'Pacman', 'Tetris', 'The Sims', 'Pokemon']

print(giochi_sorted)
# Mentre l'output in questo caso sarà: ['Minecraft', 'Pacman', 'Pokemon', 'Portal', 'Tetris', 'The Sims']
```

<h2> Le tuple: </h2>

La tupla è una lista di valori separati da virgole, simile a una normale lista, ma che è **immutabile**: una volta definita una tupla essa non può essere modificata, né possono essere aggiunti nuovi elementi! Si segnano con le parentesi tonde (), per es.:

```python
tupla = ("a", "b", "c", "d", "e")
```
Se provassimo a usare il metodo .pop() su una tupla avremmo un errore in quanto essa non può essere modificata:
<img width="580" height="135" alt="image" src="https://github.com/user-attachments/assets/9ad6edba-8acd-4605-96aa-00f558be3964" />

<h2> La funzione zip(): </h2>

La funzione zip() ci permette di combinare rapidamente insiemi di dati associati senza dover fare affidamento su liste multi-dimensionali, essa prende due (o più) liste come input e ci restituisce un oggetto tupla contenente tali elementi, in ordine di posizione. Per es.:

```python
lettere = ["a", "b", "c", "d", "e"]
nomi = ["Anna", "Bruno", "Ciro", "Daniele", "Elena"]

lettere_e_nomi = zip(lettere, nomi)
print(lettere_e_nomi)
```
L'output in questo caso sarà: **<zip object at 0x7f1631e86b48>**. Questo output ci mostra la posizione dell'oggetto nella nostra memoria, non gli elementi al suo interno! Possiamo però convertire quest'oggetto in una lista utilizzando la funzione già nota:

```python
lista_visibile = list(lettere_e_nomi)
print(lista_visibile)
```
L'output in questo caso sarà: [('a', 'Anna'), ('b', 'Bruno'), ('c', 'Ciro'), ('d', 'Daniele'), ('e', 'Elena')]
