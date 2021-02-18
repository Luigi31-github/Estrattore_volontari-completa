# Estrattore_volontari-completa
Estrae volontari da una lista di nomi in modo pseudo casuale:
 
Ad ogni alunno è associato un punteggio e un valore vero/falso per ogni materia
in base al punteggio di ogni alunno aggiunge a una lista più volte il nome dell'alunno poi la lista viene mischiato e si prendono i primi nomi
il numero di nomi presi è scritto .... devo finire


il programma è molto intuitivo quindi anche senza capire nulla di c++ è facile da usare però è necessario fare alcune modifiche:
come le materie, i nomi degli alunni e i punteggi iniziali e di quanto aumentarli o di minuirli --->qua sotto c'è scritto cosa modificare su ogni file 
  
Intestazione.h
riga 9 c'è la lista delle materie---->dopo averle modificate è necessario modificare anche quelle a riga 20
riga 10 i nomi degli alunni, sono 27 di default
riga 12 sostituire i valori nelle parentesi quadre con prima il numero di studenti e poi il numero di materie
riga 20 se i nomi delle materie sono stati modificati vanno modificati anche qua

Origine.cpp
riga 64   diminuzione punteggio volontari---->per modificarlo basta cambiare il valore nelle parentesi dopo modifica punteggio
riga 122  diminuzione punteggio estratti---->per modificarlo basta cambiare il valore nelle parentesi dopo modifica punteggio
riga 146  aumento punteggio a tutti gli altri---->per modificarlo basta cambiare il valore nelle parentesi dopo modifica punteggio

Dati.txt
ci sono 28 righe di default, se si sono fatte modifiche precedenti si deve cambiare:
  le prime 27 rappresentano gli studenti quindi ---->cancellare o aggiungere linee in base al numero di studenti
  in ogni riga ci sono 11 0 che rappresentano se si è stati interrogati o meno(0=no,1=si)---->cambiare il numero di 0 in base al numero di materie
  l'ultima riga rappresenta il numero di estrazione quindi va lasciata così
  riga 75 if (linea==27)---->il numero 27 va sostituito il numero di righe-1 che corrisponde al numero di studenti
  il primo numero su ogni riga rappresenta il punteggio iniziale---->se si desidera cambiarlo basta scrivere al suo posto il nuovo punteggio iniziale 
