<span class="bigTitle">JavaScript per Gatti</span>
## Un'introduzione per programmatori alle prime armi <span class="right">![cat](images/substack-cats.png)</span>
### *Così facile che potrebbe farcela anche il tuo umano di compagnia!*

JavaScript è un linguaggio di programmazione, ovvero un modo per dare istruzioni a un computer. Proprio come si controllano gli umani con soffi e miagolii, si controllano i computer con istruzioni scritte in un linguaggio di programmazione. Tutti i browser web capiscono JavaScript e puoi approfittarne per far fare alle pagine web cose pazzesche!

JavaScript è nato come un modo per rendere le pagine web più interattive. Oggi JavaScript gira in molti più posti che nei soli browser &mdash; funziona su server web, telefoni e persino robot! Questa pagina ti insegnerà le basi di JavaScript in modo che tu possa partire in men che non si dica*.

\* *Tempo reale: più di zero. Probabilmente un'ora o due. Inoltre, essendo un gatto, è più probabile che tu resti sdraiato al sole piuttosto che correre*

JavaScript per Gatti è distribuito con licenza [CC0](https://creativecommons.org/publicdomain/zero/1.0/deed.it)

*Questa è una traduzione italiana non ufficiale di [JavaScript for Cats](https://github.com/max-mapper/javascript-for-cats) di [@maxogden](http://twitter.com/maxogden). Il repository di questa traduzione si trova [qui](https://github.com/lucanenni/javascript-for-cats-it).*

## Indice

- [La console](#basics)
- [Stringhe](#strings)
- [Valori e variabili](#values)
- [Usare le funzioni](#functions)
- [Funzioni integrate in JS](#standard-library)
- [Scaricare nuove funzioni JS](#third-party-javascript)
- [Scrivere nuove funzioni](#writing-functions)
- [Cicli](#loops)
- [Array](#arrays)
- [Oggetti](#objects)
- [Callback](#callbacks)
- [Letture consigliate](#recommended-reading)

## Non fare il gatto pauroso

<span class="right">![cat](images/yarnify.png)</span>

Atterrerai sempre in piedi &mdash; anche mentre programmi! A differenza di [uno zampone su un bicchiere d'acqua](images/dealwithit.gif) sul tuo portatile, _nulla_ in questi tutorial danneggerà il tuo computer in alcun modo, anche se sbagli a digitare un comando o clicchi sul pulsante sbagliato. Come i gatti, anche i programmatori sbagliano di continuo: parole scritte male, virgolette o parentesi dimenticate, funzioni di base (e gomitoli, laser) di cui ci si scorda il funzionamento. Ai programmatori interessa più farlo funzionare _prima o poi_ che farlo funzionare al primo colpo. Il modo migliore per imparare è sbagliare!

Quindi non fare il gatto pauroso! La cosa peggiore che possa capitarti è dover ricaricare questa pagina nel browser se resti bloccato. Ma non preoccuparti, capiterà molto raramente.

## <a id="basics" href="#basics">#</a> Le basi

C'è del JavaScript in esecuzione su questa pagina proprio ora. Giochiamoci un po'. Per semplicità darò per scontato che tu stia usando Google Chrome per leggere questa pagina (se non è così, probabilmente è più comodo per entrambi se segui usando Chrome).

Prima di tutto, fai clic con il tasto destro in un punto qualsiasi dello schermo e scegli **Ispeziona**, poi clicca sulla scheda **Console**. Dovresti vedere un affare simile a questo:

![console](images/console.gif)

Questa è una console, conosciuta anche come "riga di comando" o "terminale". In pratica è un modo per digitare una cosa alla volta in un computer e ottenere subito la risposta del computer. Sono strumenti utilissimi per imparare (io uso ancora la console quasi ogni giorno mentre programmo).

La console fa delle cose piuttosto interessanti. Qui ho iniziato a digitare qualcosa e la console mi sta aiutando dandomi una lista di tutte le cose possibili che potrei continuare a digitare! Un'altra cosa che potresti fare è digitare `1 + 1` nella console e poi premere il tasto `Invio` per vedere cosa succede.

Usare la console è una parte molto importante dell'apprendimento di JavaScript. Se non sai se qualcosa funziona o qual è il comando per fare una certa cosa, vai nella console e scoprilo! Ecco un esempio:

### <a id="strings" href="#strings">#</a> Stringhe

Dato che sono un gatto voglio sostituire ogni occorrenza della parola `cane` su Internet con `quei maledetti cani`. Prima vai nella tua console e digita qualche frase che contenga la parola `cane` almeno una volta. In JavaScript un insieme di lettere, numeri, parole o qualsiasi altra cosa è chiamato **Stringa** (come in una *stringa* di caratteri). Le stringhe devono iniziare E finire con delle virgolette. Singole `'` o doppie `"` vanno bene entrambe, basta solo che usi le stesse all'inizio e alla fine.

![console](images/console-strings.gif)

Visto quel brutto messaggio d'errore? Non preoccuparti, non hai infranto nessuna legge. SyntaxError ILLEGAL è solo il modo in cui suona quando i robot ti dicono che il tuo programma ha un problema. Le prime due frasi avevano virgolette corrispondenti all'inizio e alla fine, ma quando ho mescolato virgolette singole e doppie la console si è agitata.

Ok, per sistemare una di queste frasi (sostituendo `cane` con la nostra versione potenziata) dobbiamo prima salvare la frase originale in modo da poterla richiamare più tardi quando faremo la nostra magia di sostituzione. Hai notato come la stringa viene ripetuta in rosso quando la digitiamo nella console? Questo perché non abbiamo detto di salvare la frase da nessuna parte, quindi ce la restituisce e basta (oppure ci restituisce un Errore se abbiamo sbagliato qualcosa).

### <a id="values" href="#values">#</a> Valori e variabili

I **Valori** sono i componenti più semplici in JavaScript. `1` è un valore, `true` è un valore, `"ciao"` è un valore, `function() {}` è un valore, e la lista continua! Ci sono diversi **tipi** di valori in JavaScript ma non serve vederli tutti subito &mdash; li imparerai naturalmente più programmi!

Per conservare i valori usiamo delle cose chiamate **variabili**. La parola "variabile" significa "che può cambiare" e viene usata perché le variabili possono contenere molti tipi diversi di valori e possono cambiare il loro valore molte volte. Sono un po' come cassette della posta. Mettiamo qualcosa in una variabile, come la nostra frase, e poi diamo alla variabile un indirizzo che possiamo usare per ritrovare la frase più tardi. Nella vita reale le cassette della posta devono avere un numero di casella postale, ma in JavaScript di solito si usano semplicemente lettere minuscole o numeri senza spazi.

![console](images/console-variables.gif)

`var` è l'abbreviazione di variabile e il simbolo `=` significa *salva la cosa a destra dentro la cosa a sinistra*. Inoltre, come puoi vedere, ora che stiamo salvando la nostra frase in una variabile la console non restituisce subito la frase, ma ci dà `undefined`, che significa *non c'era nulla da restituire*.

Se digiti semplicemente il nome di una variabile nella console, verrà stampato il valore contenuto in quella variabile. Una nota sulle variabili: per impostazione predefinita scompaiono quando cambi pagina. Se premessi il pulsante Ricarica in Chrome, per esempio, la mia variabile `fraseCane` verrebbe cancellata e sarebbe come se non fosse mai esistita. Ma non preoccupartene troppo per ora &mdash; puoi semplicemente premere le frecce su o giù sulla tastiera mentre sei nella console per scorrere tutto ciò che hai digitato di recente.

### <a id="functions" href="#functions">#</a> Funzioni

Ora che abbiamo la nostra frase salvata in una variabile, cambiamo una parola al suo interno! Possiamo farlo eseguendo una *funzione*. Le *funzioni* sono un tipo di valore che, appunto, svolgono una specifica *funzione* (cioè scopo o azione) per noi. Chiamarle "azioni" suonava strano, immagino, quindi hanno scelto la parola "funzione" invece.

JavaScript ha una funzione chiamata `replace` che fa esattamente quello che vogliamo! Le funzioni accettano un numero qualsiasi di valori tra le parentesi (zero, uno o molti) e restituiscono o niente (`undefined`) o la stringa modificata. La funzione `replace` è disponibile su qualsiasi stringa e accetta due valori: i caratteri da togliere e i caratteri da mettere al loro posto. Diventa confuso descrivere queste cose a parole, quindi ecco un esempio visivo:

![console](images/console-replace.gif)

Hai notato come il valore di `fraseCane` resti lo stesso anche dopo aver eseguito `replace` su di esso? Questo perché la funzione `replace` (come la maggior parte delle funzioni JavaScript) prende il valore che le diamo e restituisce un **nuovo valore**, senza modificare il valore che le abbiamo passato. Dato che non abbiamo salvato il risultato (non c'è un `=` a sinistra della funzione replace), la console si è limitata a stamparne il valore di ritorno.

### <a id="standard-library" href="#standard-library">#</a> La "libreria standard"

Ti starai chiedendo quali altre funzioni siano disponibili in JavaScript. La risposta: TANTISSIME. Ci sono un sacco di **librerie standard integrate** su cui puoi documentarti su MDN (un sito gestito da Mozilla pieno di informazioni utili sulle tecnologie web). Per esempio [ecco la pagina MDN sull'oggetto Math di JavaScript](https://developer.mozilla.org/it/docs/Web/JavaScript/Reference/Global_Objects/Math).

### <a id="third-party-javascript" href="#third-party-javascript">#</a> JavaScript di terze parti

Esiste anche molto codice JavaScript disponibile che **non è integrato**. Il JavaScript proveniente da terze parti viene solitamente chiamato "libreria" o "plugin". Una delle mie preferite si chiama **Underscore.js**. Andiamo a prenderla e carichiamola nella nostra pagina! Prima vai sul sito di Underscore, [http://underscorejs.org/](http://underscorejs.org/), clicca sul link di download (di solito uso le versioni di sviluppo perché sono più facili da leggere, ma entrambe offrono le stesse funzionalità di base), poi copia tutto il codice negli appunti (puoi usare Seleziona tutto dal menu Modifica per selezionare tutto). Poi incollalo nella console e premi invio. Ora il tuo browser ha una nuova variabile: `_`. Underscore ti offre un sacco di funzioni utili con cui giocare. Impareremo di più su come usarle più avanti.

![console](images/underscore.gif)

### <a id="writing-functions" href="#writing-functions">#</a> Creare nuove funzioni

Non sei limitato a usare le funzioni altrui &mdash; puoi anche scriverle tu. È abbastanza facile! Creiamo una funzione chiamata `rendiPiuEsaltante` che aggiunge un po' di punti esclamativi alla fine di una stringa.

    function rendiPiuEsaltante(stringa) {
      return stringa + '!!!!'
    }

Nella mia testa la leggo ad alta voce così: "c'è una funzione chiamata 'rendi più esaltante' che prende una stringa e restituisce una nuova copia di quella stringa con un po' di punti esclamativi alla fine". Ecco come scriveremmo questo nella console manualmente se non stessimo usando una funzione:

![console](images/custom-function-manually.gif)

L'espressione `stringa + '!!!!'` restituisce una nuova stringa e la nostra variabile chiamata `stringa` rimane com'era prima (dato che non l'abbiamo mai aggiornata con `=`).

Usiamo la nostra funzione invece di farlo manualmente. Prima, incolla la funzione nella console e poi **chiama** la funzione **passandole** una stringa:

![console](images/custom-function-call.gif)

Potresti anche chiamare la stessa funzione passandole una variabile che punta a una stringa (nell'esempio sopra abbiamo semplicemente digitato la stringa direttamente come valore invece di salvarla prima in una variabile):

![console](images/custom-function-call-variable.gif)

La riga `rendiPiuEsaltante(frase)` è equivalente a scrivere `frase + '!!!!'`. E se volessimo **modificare sul posto** (cioè aggiornare) il valore di frase? Basta salvare il valore restituito dalla funzione di nuovo nella variabile `frase`:

    var frase = "ora di fare un pisolino"
    frase = rendiPiuEsaltante(frase)

Ora `frase` avrà i punti esclamativi al suo interno! Nota che devi usare `var` solo quando stai **inizializzando** una variabile &mdash; la prima volta che la usi. Dopodiché non dovresti usare `var` a meno che tu non voglia reinizializzare (resettare/svuotare) la variabile.

Cosa succederebbe se togliessimo l'istruzione `return` dalla nostra funzione?

![console](images/custom-function-no-return.gif)

Perché `frase` è vuota? Perché le funzioni restituiscono `undefined` per impostazione predefinita! Puoi scegliere di restituire un valore facendo un `return` di qualcosa. Le funzioni dovrebbero prendere un valore e, se cambiano il valore o ne creano uno nuovo che dovrà essere usato in seguito, fare `return` di un valore (curiosità: un termine altisonante per questo stile è *programmazione funzionale*). Ecco un'altra funzione che non restituisce nulla ma usa un metodo diverso per mostrarci il risultato:

```js
function urlaLa(stringa) {
  stringa = stringa.toUpperCase()
  stringa = rendiPiuEsaltante(stringa)
  console.log(stringa)
}
```

Questa funzione, `urlaLa`, usa la nostra funzione precedente `rendiPiuEsaltante` così come il metodo integrato delle stringhe [toUpperCase](https://developer.mozilla.org/it/docs/Web/JavaScript/Reference/Global_Objects/String/toUpperCase). I metodi sono semplicemente un nome per una funzione quando appartiene a qualcosa &mdash; in questo caso `toUpperCase` è una funzione che appartiene a `String`, quindi possiamo chiamarla sia metodo *sia* funzione. `rendiPiuEsaltante`, invece, non appartiene a nessuno, quindi sarebbe tecnicamente scorretto chiamarla metodo (confuso, lo so).

L'ultima riga della funzione è un'altra funzione integrata che si limita a prendere qualsiasi valore le venga passato e a stamparlo nella console.

![console](images/custom-function-console-log.gif)

Quindi c'è qualcosa di sbagliato nella funzione `urlaLa` qui sopra? Dipende! Ecco i due tipi principali di funzioni:

  - funzioni che modificano o creano valori e li restituiscono
  - funzioni che prendono dei valori ed eseguono un'azione che non può essere restituita

`console.log` è un esempio del secondo tipo di funzione: stampa cose nella tua console &mdash; un'azione che puoi vedere con i tuoi occhi ma che non può essere rappresentata come un valore JavaScript. La mia regola personale è cercare di tenere separati questi due tipi di funzioni, quindi ecco come riscriverei la funzione `urlaLa`:

```js
function urlaLa(stringa) {
  stringa = stringa.toUpperCase()
  return rendiPiuEsaltante(stringa)
}

console.log(urlaLa("non temo nessun umano"))
```

In questo modo `urlaLa` diventa più **generica**, nel senso che fa solo una o due piccole cose semplici e non sa nulla su come stamparsi da sola nella console &mdash; quella parte può sempre essere programmata dopo, fuori dalla definizione della funzione.

### <a id="loops" href="#loops">#</a> Cicli

Ora che abbiamo qualche abilità di base sotto la cintura (*nota dell'autore: i gatti indossano mai le cinture?*) possiamo iniziare a essere pigri. Cosa?! Sì, esatto: programmare significa essere pigri. Larry Wall, l'inventore del linguaggio di programmazione Perl, definì la pigrizia come la [virtù più importante](http://c2.com/cgi/wiki?LazinessImpatienceHubris) di un buon programmatore. Se i computer non esistessero dovresti fare a mano ogni genere di compito noioso, ma se impari a programmare puoi startene sdraiato al sole tutto il giorno mentre un computare da qualche parte esegue i tuoi programmi al posto tuo. È uno stile di vita glorioso pieno di relax!

I cicli sono uno dei modi più importanti per sfruttare la potenza di un computer. Ricordi `Underscore.js` di prima? Assicurati di averlo caricato nella pagina (ricorda: puoi semplicemente premere la freccia su sulla tastiera un paio di volte e poi premere `Invio` per ricaricarlo se ne hai bisogno) e prova a copiare/incollare questo nella tua console:

```js
function stampaUnNumero(unNumero) {
  console.log(unNumero)
}
_.times(10, stampaUnNumero)
```

Questo codice usa il metodo [times](http://underscorejs.org/#times) di Underscore, che prende 1 numero e 1 funzione e poi parte da 0 e, per 10 passi, conta salendo di 1, chiamando la funzione con il numero a ogni passo.

![console](images/times-loop.png)

Se dovessimo scrivere manualmente cosa fa `times` nel codice sopra, sarebbe così:

```js
stampaUnNumero(0)
stampaUnNumero(1)
stampaUnNumero(2)
stampaUnNumero(3)
stampaUnNumero(4)
stampaUnNumero(5)
stampaUnNumero(6)
stampaUnNumero(7)
stampaUnNumero(8)
stampaUnNumero(9)
```

Ma i gatti si rifiutano di fare lavoro manuale non necessario come questo, quindi dobbiamo sempre chiederci: *"sto facendo questo nel modo più pigro possibile?"*.

Allora perché si chiama "ciclo" (loop)? Pensala così: se dovessimo scrivere una lista di 10 numeri (da 0 a 9) usando un Array JavaScript, sarebbe così:

```js
var zeroAlDieci = [0, 1, 2, 3, 4, 5, 6, 7, 8, 9]
```

Quello che `times` fa realmente è visitare ogni numero e ripetere un compito: nell'esempio sopra il compito era chiamare la funzione `stampaUnNumero` con il numero corrente. Ripetere compiti in questo modo si chiama *ciclare (loop) sull'*Array.

### <a id="arrays" href="#arrays">#</a> Array

Li ho già nominati un paio di volte, ma dedichiamo un minuto a impararli meglio. Immagina di dover tenere traccia di tutti i tuoi amici. Bene, un Array andrà benissimo. Pensa a un Array come a una lista ordinata in cui puoi tenere *tonnellate* di roba.

Ecco come se ne crea uno:

```js
var mieiAmiciGatti = ["bill", "tabby", "ceiling"]
```

Fantastico! Ora hai una lista dei tuoi amici gatti.

Gli elementi (così si chiama un singolo elemento in un array) memorizzati negli array partono da 0 e salgono da lì. Quindi `mieiAmiciGatti[0]` restituisce `bill` e `mieiAmiciGatti[1]` restituisce `tabby`... e così via.

Per tirare fuori gli amici dal tuo nuovissimo Array puoi semplicemente accedere direttamente a un elemento così:

```js
console.log(mieiAmiciGatti[0])
```

![console](images/array-access.png)

Se hai fatto un nuovo amico gatto all'ultimo club per gatti alla moda l'altra sera e vuoi aggiungerlo alla tua lista, è semplicissimo: `mieiAmiciGatti.push("gatto super trendy")`.

Per controllare che il nuovo gatto sia entrato nel tuo array puoi usare `.length`:

![console](images/array-push-length.png)

Hai notato come `push` abbia restituito la lunghezza? Comodo! Nota anche che gli array **preservano sempre l'ordine**, il che significa che ricorderanno l'ordine in cui hai aggiunto o definito le cose. Non tutto in JavaScript preserva l'ordine, quindi ricordati questa proprietà speciale degli Array!

### <a id="objects" href="#objects">#</a> Oggetti

Gli array vanno bene per le liste, ma per altri compiti possono essere scomodi da gestire. Considera il nostro array di amici gatti. E se volessi salvare più di soli nomi?

```js
var mieiAmiciGatti = ["bill", "tabby", "ceiling"]
var cognomi = ["il gatto", "gatto", "gatto"]
var indirizzi = ["Il Vicolo", "Casa della Nonna", "Soffitta"]
```

A volte è comodo avere tutti gli indirizzi o i nomi in un'unica variabile. Ma a volte hai in mente un gatto specifico, diciamo Bill, e vuoi solo cercare l'indirizzo di quel gatto. Con gli array serve un sacco di lavoro perché non puoi semplicemente dire "ehi array, dammi l'indirizzo di Bill" perché "Bill" è in un array e il suo indirizzo è in un array completamente diverso.

![console](images/array-lookup.png)

Questo può essere fragile perché se i nostri array cambiano e aggiungiamo un nuovo gatto all'inizio, dovremmo anche aggiornare la nostra variabile `posizioneBill` per farla puntare alla nuova posizione delle informazioni di Bill negli array! Ecco un modo più facile da mantenere per salvare informazioni come queste usando gli oggetti:

```js
var primoGatto = { nome: "bill", cognome: "il gatto", indirizzo: "Il Vicolo" }
var secondoGatto = { nome: "tabby", cognome: "gatto", indirizzo: "Casa della Nonna" }
var terzoGatto = { nome: "ceiling", cognome: "gatto", indirizzo: "Soffitta" }
```

Perché dovremmo farlo in questo modo? Perché ora abbiamo una variabile per ogni gatto che possiamo usare per ottenere i valori di quel gatto in modo più comodo e leggibile.

![console](images/object-lookup.png)

Puoi pensare agli Oggetti come alle chiavi su un portachiavi. Ognuna è per una porta specifica e se hai delle belle etichette sulle tue chiavi puoi aprire le porte molto velocemente. Infatti, le cose a sinistra dei `:` si chiamano **chiavi** (conosciute anche come **proprietà**) e le cose a destra sono **valori**.

```js
// un oggetto con una singola chiave 'nome' e un singolo valore 'bill'
{ nome: 'bill' }
```

Allora perché mai dovresti usare gli array se puoi semplicemente mettere i tuoi dati negli oggetti? Perché gli oggetti non ricordano l'ordine delle chiavi che hai impostato. Potresti inserire un oggetto così:

```js
{ data: "20/10/2012", diario: "oggi ho dormito un po'", nome: "Carlo" }
```

Ma il computer potrebbe restituirtelo così:

```js
{ diario: "oggi ho dormito un po'", nome: "Carlo", data: "20/10/2012" }
```

Oppure così!

```js
{ nome: "Carlo", diario: "oggi ho dormito un po'", data: "20/10/2012" }
```

Quindi non puoi mai fidarti dell'ordine delle chiavi negli oggetti. Se vuoi fare le cose davvero in grande puoi creare un array pieno di oggetti, o un oggetto pieno di array!

```js
var registroUmore = [
  {
    data: "20/10/2012",
    umore: "sballato dall'erba gatta"
  },
  {
    data: "21/10/2012",
    umore: "spiazzato"
  },
  {
    data: "22/10/2012",
    umore: "facendo le fusa"
  }
]

// ordinati dal meno al più preferito
var preferiti = {
  premi: ["avvistamento di uccellini", "grattino sulla pancia", "erba gatta"],
  postiPerIlPisolino: ["divano", "fioriera", "faccia dell'umano"]
}
```

Quando combini cose diverse così stai creando **strutture dati**, proprio come i lego!

### <a id="callbacks" href="#callbacks">#</a> Callback

Le callback non sono davvero una funzionalità di JavaScript come `Object` o `Array`, ma piuttosto un certo modo di usare le funzioni. Per capire perché le callback sono utili devi prima imparare cos'è la programmazione asincrona (spesso abbreviata in "async"). Il codice asincrono è per definizione codice scritto in un modo che non è sincrono. Il codice sincrono è facile da capire e da scrivere. Ecco un esempio per illustrarlo:

```js
var foto = scarica('http://foo-chan.com/images/sp.jpg')
caricaFotoTweet(foto, '@maxogden')
```

Questo [pseudocodice](http://simple.wikipedia.org/wiki/Pseudocode) sincrono scarica un'adorabile foto di gatto e poi carica la foto su twitter, taggando `@maxogden` nel tweet con la foto. Abbastanza semplice!

(*nota dell'autore: io, @maxogden, accetto volentieri tweet casuali con foto di gatti*)

Questo codice è sincrono perché, affinché la foto venga caricata nel tweet, il download della foto deve essere completato. Questo significa che la riga 2 non può essere eseguita finché il compito alla riga 1 non è completamente finito. Se dovessimo effettivamente implementare questo pseudocodice, vorremmo assicurarci che `scarica` "bloccasse" l'esecuzione finché il download non fosse terminato, il che significa che impedirebbe l'esecuzione di *qualsiasi* altro JavaScript finché non avesse finito, e poi, al completamento del download, sbloccherebbe l'esecuzione JavaScript e la riga 2 verrebbe eseguita.

Il codice sincrono va bene per le cose che accadono velocemente, ma è terribile per cose che richiedono salvataggio, caricamento, download o upload. E se il server da cui stai scaricando la foto è lento, o la connessione internet che stai usando è lenta, o il computer su cui stai eseguendo il codice ha troppe schede aperte con video di gatti su youtube ed è lento? Significa che potrebbero volerci potenzialmente minuti di attesa prima che la riga 2 venga eseguita. Nel frattempo, dato che tutto il JavaScript nella pagina viene bloccato dall'esecuzione mentre il download è in corso, la pagina web si bloccherebbe completamente e diventerebbe non reattiva finché il download non è terminato.

Bloccare l'esecuzione va evitato a tutti i costi, specialmente quando ciò fa bloccare o diventare non reattivo il tuo programma. Supponiamo che la foto sopra impieghi un secondo a scaricarsi. Per illustrare quanto sia lungo un secondo per un computer moderno, ecco un programma che misura quanti compiti JavaScript riesce a elaborare in un secondo.

```js
function misuraVelocitaCiclo() {
  var conteggio = 0
  function aggiungiUno() { conteggio = conteggio + 1 }

  // Date.now() restituisce un numero grande che rappresenta il numero
  // di millisecondi trascorsi dal 1 gennaio 1970
  var adesso = Date.now()

  // Continua a ciclare finché Date.now() non è 1000 millisecondi (1 secondo)
  // o più nel futuro rispetto a quando abbiamo iniziato a ciclare.
  // A ogni ciclo, chiama aggiungiUno
  while (Date.now() - adesso < 1000) aggiungiUno()

  // Finalmente sono passati >= 1000ms, quindi stampiamo il conteggio totale
  console.log(conteggio)
}

misuraVelocitaCiclo()
```

Copia e incolla il codice sopra nella tua console JavaScript e dopo un secondo dovrebbe stampare un numero. Sul mio computer ho ottenuto `8527360`, circa **8,5 milioni**. In un secondo JavaScript può chiamare la funzione `aggiungiUno` 8,5 milioni di volte! Quindi se hai codice sincrono per scaricare una foto, e il download della foto impiega un secondo, significa che stai potenzialmente impedendo che accadano 8,5 milioni di operazioni mentre l'esecuzione JavaScript è bloccata.

Alcuni linguaggi hanno una funzione chiamata `sleep` che blocca l'esecuzione per un certo numero di secondi. Per esempio, ecco del codice [`bash`](http://en.wikipedia.org/wiki/Bash_%28Unix_shell%29) eseguito in `Terminal.app` su Mac OS che usa `sleep`. Quando esegui il comando `sleep 3 && echo 'ho finito di dormire'` blocca per 3 secondi prima di stampare `ho finito di dormire`.

![console](images/bash-sleep.png)

JavaScript non ha una funzione `sleep`. Dato che sei un gatto probabilmente ti starai chiedendo: "Perché sto imparando un linguaggio di programmazione che non prevede il dormire?". Ma resta con me. Invece di affidarsi a `sleep` per aspettare che le cose accadano, il design di JavaScript incoraggia l'uso delle funzioni. Se devi aspettare che il compito A finisca prima di fare il compito B, metti tutto il codice del compito B in una funzione e chiami quella funzione solo quando A è finito.

Per esempio, questo è codice in stile bloccante:

```js
a()
b()
```

E questo è in stile non bloccante:

```js
a(b)
```

Nella versione non bloccante `b` è una callback di `a`. Nella versione bloccante `a` e `b` vengono entrambe chiamate/invocate (hanno entrambe `()` dopo di loro, il che esegue le funzioni immediatamente). Nella versione non bloccante noterai che viene invocata solo `a`, mentre `b` viene semplicemente passata ad `a` come argomento.

Nella versione bloccante non c'è una relazione esplicita tra `a` e `b`. Nella versione non bloccante diventa compito di `a` fare ciò che deve fare e poi chiamare `b` quando ha finito. Usare le funzioni in questo modo si chiama callback perché la tua funzione di callback, in questo caso `b`, viene chiamata più tardi quando `a` ha completamente finito.

Ecco un'implementazione pseudocodice di come potrebbe essere `a`:

```js
function a(fatto) {
  scarica('https://pbs.twimg.com/media/B4DDWBrCEAA8u4O.jpg:large', function downloadCompletato(errore, png) {
    // gestisci l'errore se ce n'è stato uno
    if (err) console.log('uh-oh!', errore)

    // chiama fatto quando hai finito
    fatto()
  })
}
```

Ripensa al nostro esempio non bloccante, `a(b)`, in cui chiamiamo `a` e passiamo `b` come primo argomento. Nella definizione della funzione `a` qui sopra, l'argomento `fatto` *è* la nostra funzione `b` che abbiamo passato. Questo comportamento è qualcosa che all'inizio è difficile da capire fino in fondo. Quando chiami una funzione, gli argomenti che passi non avranno gli stessi nomi di variabile quando sono dentro la funzione. In questo caso quello che chiamiamo `b` viene chiamato `fatto` dentro la funzione. Ma `b` e `fatto` sono solo nomi di variabile che puntano alla stessa funzione sottostante. Di solito le funzioni di callback vengono etichettate con qualcosa come `fatto` o `callback` per rendere chiaro che sono funzioni che dovrebbero essere chiamate quando la funzione corrente ha finito.

Quindi, finché `a` fa il suo lavoro e chiama `b` quando ha finito, sia `a` che `b` vengono chiamate sia nella versione non bloccante che in quella bloccante. La differenza è che nella versione non bloccante non dobbiamo interrompere l'esecuzione di JavaScript. In generale, lo stile non bloccante è quando scrivi ogni funzione in modo che possa terminare il prima possibile, senza mai bloccare.

Per ribadire ulteriormente il concetto: se `a` impiega un secondo a completarsi, e usi la versione bloccante, significa che puoi fare solo una cosa. Se usi la versione non bloccante (cioè usi le callback) puoi fare *letteralmente milioni* di altre cose in quello stesso secondo, il che significa che puoi finire il tuo lavoro milioni di volte più velocemente e dormire il resto della giornata.

Ricorda: programmare significa essere pigri, e dovresti essere tu a dormire, non il tuo computer.

Spero che ora tu possa vedere che le callback sono semplicemente funzioni che chiamano altre funzioni dopo un qualche compito asincrono. Esempi comuni di compiti asincroni sono cose come leggere una foto, scaricare una canzone, caricare un'immagine, parlare con un database, aspettare che un utente prema un tasto o clicchi su qualcosa, eccetera. Qualsiasi cosa che richieda tempo. JavaScript è davvero bravo a gestire compiti asincroni come questi, purché tu ti prenda il tempo di imparare a usare le callback e a evitare che il tuo JavaScript venga bloccato.

## La fine!

Questo è solo l'inizio della tua relazione con JavaScript! Non puoi impararlo tutto in una volta, ma dovresti trovare quello che funziona per te e provare a imparare tutti i concetti qui presenti.

Ti consiglierei di tornare di nuovo domani e ripassare tutto da capo! Potrebbero volerci un po' di ripassi prima che tu capisca tutto (programmare è difficile). Cerca solo di evitare di leggere questa pagina in stanze che contengono oggetti luccicanti . . . possono essere incredibilmente distraenti.

Hai un altro argomento che vorresti veder trattato? Apri una issue per suggerirlo [su github](http://github.com/max-mapper/javascript-for-cats) (repository originale in inglese), oppure [su questo repository](https://github.com/lucanenni/javascript-for-cats-it/issues) per segnalazioni sulla traduzione italiana.

### <a id="recommended-reading" href="#recommended-reading">#</a> Letture consigliate

  JavaScript per Gatti salta molti dettagli che non sono importanti per iniziare (i gatti non sono famosi per la loro capacità di concentrazione), ma se senti il bisogno di approfondire, dai un'occhiata a questi:

  - [NodeSchool.io](http://nodeschool.io/) è un software educativo open source guidato dalla comunità che insegna varie competenze di sviluppo web in un formato interattivo e autogestito. Ho contribuito a creare NodeSchool! Purtroppo ha meno gatti di questa pagina.
  - [Eloquent Javascript](http://eloquentjavascript.net/) è un libro gratuito che ti insegna JavaScript! È piuttosto buono! Specialmente il capitolo su [valori, variabili e flusso di controllo](http://eloquentjavascript.net/chapter2.html)
  - La [Guida JavaScript di Mozilla](https://developer.mozilla.org/it/docs/Web/JavaScript/Guide) ha anche un bel capitolo introduttivo chiamato [valori, variabili e letterali](https://developer.mozilla.org/it/docs/Web/JavaScript/Guide/Grammar_and_types)
  - La [guida di stile JS `standard`](https://github.com/feross/standard) è un linter per lo stile JS "a configurazione zero" che uso io
  - [Let's Write Code di @shama](https://github.com/shama/letswritecode), un'ottima serie di tutorial di programmazione su YouTube fatta da un mio amico

<hr>
### <a id="satisfied-customers" href="#satisfied-customers">#</a> Clienti soddisfatti
<center>![satisfied customer](images/customers5.jpg)</center>
<center>![satisfied customer](images/customers1.png)</center>
<center>![satisfied customer](images/customers2.png)</center>
<center>![satisfied customer](images/customers3.png)</center>
<center>![satisfied customer](images/customers4.png)</center>

*JSForCats.com è un lavoro d'amore e un progetto in corso di [@maxogden](http://twitter.com/maxogden). Se vuoi contribuire e migliorare questo tutorial c'è un repository Github [proprio qui](http://github.com/max-mapper/javascript-for-cats).*

*Questa traduzione italiana è mantenuta in [questo repository](https://github.com/lucanenni/javascript-for-cats-it). Contributi e correzioni sono benvenuti!*

*Nota di manutenzione (14/08/2026): aggiornate le dipendenze di build (`marked`, `mustache`) per correggere vulnerabilità di sicurezza note (ReDoS in `marked`, XSS in `mustache`); adeguato `render.js` alla nuova API di `marked`. Rimossa la cartella `javascripts/` (rainbow.js e altri script di syntax highlighting mai effettivamente caricati dalla pagina). Deploy automatico: una GitHub Action renderizza il sito ad ogni push su `master` e lo pubblica tramite il meccanismo ufficiale di GitHub Pages (nessun branch `gh-pages`, nessuna credenziale git di mezzo). Nessuna modifica al contenuto del tutorial.*
<center>![console](images/awesome.jpg)</center>
