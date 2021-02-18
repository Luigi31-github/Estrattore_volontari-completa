# Estrattore_volontari-completa
Estrae volontari da una lista di nomi in modo pseudo casuale: la probabilità di essere estratti varia in base alla grandezza del punteggio assocato ad ogni nome

FUNZIONAMENTO:
il programma legge i dati scritti nel file Dati.txt e associa ad ogni alunno un punteggio eun valore vero/falso per ogni materia
il programma chiede prima la materia per la quale estrarre (deve essere scritta nello stesso modo di quelle elencate nel file Intestazione.h)
poi chiede se ci sono eventuali volontari (deve essere scritto il numero dell'elenco di chi va volontario) poi ne modifica il punteggio e lo segna interrogato
chiede se si vuole estrarre e crea una lista con più volte il nome di ogni alunno non interrogato alla materia in base al punteggio associato e mischia la lista
chiede il numero di estratti e prende i primi nomi della lista, li segna interrogati, modifica il loro punteggio e quello di tutti i non estratti e i non volonatari
finita l'estrazione chiede se si vuole estrarre di nuovo con questa materia in caso afferamtivo ricrea la lista e chiede il numero di interrogati
in caso negativo chiede se si vuole estrarre con un'altra materia se sì riparte dall'inizio chiedendo la materia, poi i volontari ecc...
in caso negativo il programma registra tutti i cambiamenti nel file Dati.txt e il programma finisce

CAMBIAMENTI PER ADDATTARE IL PROGRAMMA ALLE PROPRIE ESIGENZE:
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
ci sono 28 righe di default, se si sono fatte modifiche (numero di materie, di alunni, punteggio) si deve cambiare:
  le prime 27 rappresentano gli studenti quindi ---->cancellare o aggiungere linee in base al numero di studenti
  in ogni riga ci sono 11 0 che rappresentano se si è stati interrogati o meno(0=no,1=si)---->cambiare il numero di 0 in base al numero di materie
  l'ultima riga rappresenta il numero di estrazione quindi va lasciata così
  riga 75 if (linea==27)---->il numero 27 va sostituito il numero di righe-1 che corrisponde al numero di studenti
  il primo numero su ogni riga rappresenta il punteggio iniziale---->se si desidera cambiarlo basta scrivere al suo posto il nuovo punteggio iniziale 
