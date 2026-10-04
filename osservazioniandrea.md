# Osservazioni — Esercitazione 0

Gruppo:

Componenti (Andrea Giustiniani, Carlo Palatucci, giustiniani2260468-ai, palatucci2257570):

URL del repository condiviso: https://github.com/giustiniani2260468-ai/esercitazione-0-template.git

Chi ha usato la tastiera nello step 1 e nello step 2: Andrea ha usato la tastiera nello step 1, Carlo nello step 2. 

Compilate insieme le osservazioni e discutete le risposte: entrambi dovete
saper spiegare le prove svolte.

## Step 1 — Hello World: compilazione ed esecuzione

Comando di compilazione: gcc -std=c17 -Wall -Wextra -Wpedantic hello.c -o hello


Comando di esecuzione e risultato osservato:./hello

Che cosa ho capito su sorgente ed eseguibile: la sorgente è il codice in C (ovvero hello.c) l'eseguibile è invece hello cioè il sorgente dopo averlo compilato

Output richiesto e comportamento del programma prima della modifica: non stampa (non c'è printf), tuttavia la compilazione avviene con successo. 

Esito dopo la modifica e spiegazione della correzione: stampa (c'è printf)

## Step 1 — Git

Quali file ho incluso nel commit e perché: hello.c in quanto sorgente, osservazioni.md in quanto richiesto.

Come ho verificato che la versione provata sia presente su GitHub: ho controllato e aperto il repository online, aggiornando la pagina.

Che cosa ho osservato prima e dopo `git pull`, e perché non serve un nuovo clone: prima di 'git pull' osservazioni.md non è cambiato localmente, dopo git pull è invece cambiato. Non serve nuovamente clone, in quanto la repository in locale è già scaricata. 'git pull ' dunque aggiorna la copia in locale. 

## Step 2 — Eco: prima prova

Argomenti passati, comando e risultato: 
    char *testo = argv[1];
    int intero = atoi(argv[2]);
    double reale = atof(argv[3]);

    printf("%s %d %.6f\n", testo, intero, reale);

    il risultato è la stampa di una terna (testo, intero (attraverso atoi), reale (attraverso atof)) dipendente dalle stringhe di caratteri inserite dopo ./eco

Che cosa posso concludere: l'utilizzo di atoi e atof consente in maniera rapida di estrarre da stringhe rispettivamente interi e double, ma restituisce semplicemente 0 nel caso in cui non vi siano interi e double da estrarre. Le funzioni nella seconda prova di eco sono invece più dettagliate. Se si inseriscono più o meno di 4 argomenti, il programma ricorda cosa va inserito attraverso printf. 

## Step 2 — Eco: seconda prova

Argomenti passati, comando e risultato:
  char *testo = argv[1];
  int intero = leggi_intero(argv[2]);
  double reale = leggi_reale(argv[3]);
  printf("%s %d %.6f\n", testo, intero, reale);

Che cosa ho capito su testo, conversioni e stampa: gli elementi di argv non sono già numeri: sono stringhe di caratteri, passando 0012 come primo argomento esso rimarrà char *, come secondo e terzo assumerà il valore di intero (12) o double (12.000000). Si può passare un testo che contiene spazi come unico argomento usando "...". Se si scrive 1.25e1 come terzo argomento esso verrà stampato come richiesto, ovvero 12.500000, la rappresentazione usata e l'output del programma non sono dipendenti. In eco2.c, come osservabile nel codice nelle funzioni fornite, il programma risponde attraverso printf come "Il secondo argomento deve essere un intero in base 10", oppure "Il secondo argomento ha un valore fuori intervallo...", restituendo exit(2). 

## Step 2 — Risultato ed errori

Previsioni per l'esecuzione con argomenti validi e per quella con `dodici`: nel primo caso eco.txt è non vuoto e contiene l'output richiesto, inoltre, il return di main è 0. Nel secondo caso è vuoto e il valore di main è 2. 

Contenuto di `eco.txt`, messaggi nel terminale e codici di uscita osservati: la previsione è corretta. 

Come un controllo automatico può riconoscere un errore: ??????

## Step 2 — Parametri e calcolo fisico

Quando serve ricompilare e quando basta cambiare gli argomenti: nel caso in cui sia necessario cambiare parametro, non occorre ricompliare: basterà sfruttare gli argomenti della funzione main e delle funzioni fornite (oppure di quelle suggerite atof e atoi). Modificare una formula (e dunque non i valori da immetterci) richiederà invece di dover ricompilare il file.c. Si può pensare che, dove avremmo un tempo messo scanf, adesso non è più necessario ricompilare, mentre negli altri casi rimane cosa da fare. 

## Step 2 — Git

Come riconosco nella cronologia i commit dei due step:

Come ho verificato che la versione finale sia presente su GitHub:
