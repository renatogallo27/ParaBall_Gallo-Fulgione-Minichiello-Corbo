# **Gruppo coniche**

*Il nostro gruppo è formato da Gallo, Fulgione, Minichiello, Corbo.*

## **Ruoli**

- Gallo: **Gestione e realizzazione del software, gestione del ReadMe e del changelog, addetto ai preconcetti
  matematici, addetto alla realizzazione del gioco e alla stesura della documentazione.**
- Corbo: **Gestione e realizzazione del software, addetto ad aggiornare il file .md, addetto alla realizzazione del gioco e alla stesura della documentazione.**
- Minichiello: **Addetto ad aggiornare il file .md e alla realizzazione del gioco.**
- Fulgione: **Gestione e realizzazione del software, addetto ad aggiornare il file .md., addetto alla creazione del diagramma di flusso e alla stesura della documentazione.**

## **Organizzazione del gruppo**

Questo è uno dei due gruppi nei quali è stato diviso il gruppo originario "https://github.com/renatogallo27/gruppo-coniche-G-C-P-C-F-M-T-D". 
Abbiamo ereditato le classi retta e parabola, ma il gioco che proporremo sarà diverso. 

***

# Tennis ball

## **Descrizione del gioco**

### *Abstract*

È un gioco arcade 2D. Gli sprite presenti nel gioco sono una pallina da tennis ed un cestino della spazzatura. 
Il gioco è diviso in livelli e in ognuno di questi il cestino della spazzatura viene generato in una posizione casuale.
L'obiettivo del giocatore è mandare la pallina all'interno del cestino e per farlo deve inserire dei valori a,b e c di una parabola, i cui punti andranno a rappresentare la traiettoria del moto compiuto dalla pallina. Completato l'obiettivo con successo si passerà al livello successivo. 
Il giocatore all'inizio del gioco ha a disposizione 3 vite, che possono aumentare durante il corso della partita. 
I primi due livelli del gioco sono di prova e servono per far ambientare il giocatore sul variare dei parametri che deve inserire.  
In caso il giocatore non dovesse completare l'obiettivo perderà una vita e passerà al livello successivo. Terminate le vite terminerà anche il gioco.   

### *Interfaccia*



### *Requisiti*

#### *Concetti teorici*

Conoscenza delle caratteristiche della conica parabola, della forma della sua equazione e delle [relazioni tra coefficienti dell'equazione e grafico.](http://spuntieappunti.altervista.org/appunti/parabola/relazioni.shtml) 

#### *Software*

Bisogna possedere python3.9 e un suo interprete sul proprio computer.

#### *Moduli python*

Bisogna avere installati sul proprio computer i moduli python: pygame, pgzero, random,
(possibili altri moduli che probabilmente ci serviranno ma di cui adesso non siamo a conoscenza).

## *Preconcetti matematici*

### *Tutti i metodi della classe retta:*

#### *eqImplicita:*

	in base ai valori dei parametri (a, b, c) ricava l’equazione implicita del tipo 
	ax + by + c = 0.

#### *eqEsplicita:*

	in base al valore dei parametri (a, b, c) ricava l’equazione esplicita del tipo 
	y = (-a/b)x + (-c/b) dove (-a/b) è il coefficiente angolare e (-c/b) è l’intercetta.

#### *trovaY:*

	presi i valori di a, b, c e x trova il valore di y. Questo metodo è implementato nel
	metodo “punti”.

#### *punti:*

    l’utente inserisce un range di valori di x e il metodo trova i corrispondenti valori di y
    attraverso il metodo “trovaY”. Successivamente inserisce le coordinate dei punti
    trovati in quel range di x all’interno di una lista di tuple

#### *m (coefficiente angolare):*

	dati i valori dei parametri (a, b) ricava il valore del coefficiente angolare (m) tramite 	la formula m = -a/b.

#### *intersezione:*

    se coefficiente angolare (m) e intercetta (q) delle due equazioni sono uguali allora le rette sono coincidenti (hanno tutti i punti in comune).
    Se il coefficiente angolare è uguale mentre l’intercetta è diversa allora non ci sono punti di intersezione in quanto le rette sono parallele.
    Se il coefficiente angolare è diverso metti a sistema le due equazioni ricavando il
    punto d’intersezione tra le due rette.

### *Tutti i metodi della classe parabola:*

#### *fuoco:*

    Se l’asse di simmetria della parabola è parallelo all’asse delle ordinate allora le
    coordinate del fuoco saranno (-b/2a ; 1-Δ/4a);
    Se l’asse di simmetria della parabola è parallelo all’asse delle ascisse allora le
    coordinate del fuoco saranno (1-Δ/4a ; -b/2a).

#### *direttrice:*

	Se l’asse di simmetria della parabola è parallelo all’asse delle ordinate allora l’
    equazione della direttrice sarà y = -1-Δ/4a;
    Se l’asse di simmetria della parabola è parallelo all’asse delle ascisse allora l’
    equazione della direttrice sarà x = -1-Δ/4a.

#### *trovaY:*

	presi i valori di a, b, c e x trova il valore/valori (a seconda dell’asse di simmetria) di y.
    Questo metodo è implementato nel metodo “punti”.

#### *trovaX:*

	presi i valori di a, b, c e y trova il valore/valori (a seconda dell’asse di simmetria) di x.
    Questo metodo è implementato nel metodo “punti”.

#### *punti:*

	Se l’asse della parabola è parallelo all’asse delle ordinate:
    l’utente inserisce un range di valori di x e il metodo trova il corrispondente 
    valore di y per ogni x attraverso il metodo “trovaY”. Successivamente inserisce le coordinate dei punti trovati in quel range di x all’interno di una lista di tuple;
	Se l’asse della parabola è parallelo all’asse delle ascisse:
    l’utente inserisce un range di valori di y e il metodo trova il corrispondente 
    valore di x per ogni y attraverso il metodo “trovaX”. Successivamente inserisce le coordinate dei punti trovati in quel range di y all’interno di una lista di tuple.
