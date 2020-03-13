# presympto
database application to collect data about pre-symptomatic COVID-19 cases

## Premesse (background)
Ciò che caratterizza le gestione attuale (13-mar-2020) dei dati dell'epidemia di Covid-19 è la totale assenza di dati 
dei pazienti cosiddetti *asintomatici*.

Quindi nessuno sa quanti siano in realtà stati già infettati ma non sono conteggiati nelle cifre ufficiali.

Tuttavia è lecito attendersi che a fronte di circa 15000 casi (al momento in cui scrivo) noti, questi cosiddetti 
*asintomatici* siano molti di più, magari 10-100 volte di più.

E' altrettanto lecito attendersi che questi casi evolveranno, in percentuali consistenti, in casi conclamati, e 
bisognosi di cure; ma nessuno sa in quale misura, e in quanti giorni, proprio perchè non c'è (per quanto mi consta) 
nessuna iniziativa che ha l'obbiettivo di raccogliere dati prima che il paziente diventi critico.

## Oggetto
Per questo motivo definiamo che l'oggetto di questo progetto è la **raccolta di dati sui pazienti PRE-SINTOMATICI**, 
con ciò intendendo quelli che ancora non sono stati registrati in un trattamento nè domiciliare nè ospedaliero.
Si pensi a chi ha chimato il medico di famiglia, e non rientrando nei criteri (ad esempio: "tosse AND ( febbre OR 
difficoltà respiratorie)" non è stato registrato in alcun modo.

## Idea
L'idea è mettere a disposizione una varietà di interfacce (web, mobile app, e poi eventualmente grazie all'aiuto di 
volontari, ad esempio studenti di medicina, anche un numero verde) per raccogliere con frequenza almeno quotidiana dati 
sui pre-sintomi di *chi sente di aver qualcosa di non grave ma forse importante da segnalare e tenere monitorato non 
come singolo ma insieme alla collettività*. 

## Scopi
Ci sono un buon numero di buone ragioni per fare questo:
- aiutare a prevedere e gestire il numero di ospedalizzazioni dei giorni successivi
- comprendere come si evolvono i sintomi prima dell'aggravarsi del quadro
   - avremmo a disposizione grndi quantità di dati su cui applicare modelli AI supervisionati e non 
- evidenziare comportamenti efficaci nel trattamento domiciliare
- unire gli sforzi a livello internazionale, a beneficio dei paesi che hanno qualche settimana di ritardo rispetto a noi
- mettere a disposizione di questi pre-pazienti un canale di comunicazione dedicato e laddove necessario personalizzato 
per conoscere situazioni e disporre indicazioni
- dare inizio a un nuovo approccio di medicina "preventiva" che possa tornare utile in futuro per altre patologie

## Difficoltà / Criticità
Ci sono diverse difficoltà da superare:
- implementare una web/database application nel giro di **pochissimi giorni**, 
   - mantenendo la flessibilità necessaria per farla evolvere
   - raggiungendo fasce di utenza le più ampie possibili
   - ...
- ottenere il massimo dell'**obbiettività** possibile (in senso medico) 
   - perchè il sistema non soffra di ipocondrie e autosuggestioni
   - utilizzando medici nel ruolo di mediatori/revisori delle info raccolte
   - coordinandosi con il SSN e i medici di famiglia
   - ...
- garantire gli utenti/pazienti rispetto alla **gestione dei dati personali**
   - l'interfaccia open-data potrebbe trattare i pazienti in modo anonimo / aggregato
   - i dati personali sarebbero resi accessibili solo al SSN e alle forze dell'ordine 
   - e al SSN 
   - ...

## Risorse 
Ci sono anche risorse presumibilmente disponibili
- schiere di informatici che sono a casa
- schiere di avvocati che sono a casa
- schiere di studenti di medici non infettivologi, non internisti (es. ortopedici) e comunque non direttamente 
coinvolti nell'attuale emergenza, anzi magari col reparto chiuso, e finanche studenti di medicina 
- probabilmente aziende o fornitori di SAAS (Google, AWS) che potrebbero mettere a disposizione risorse informatiche 
remotizzate, chissà, magari anche in modo gratuito
- schiere di diretti interessati presumibilmente disponibili a donare qualche € per sostenere l'iniziativa ()
- immagino anche professionisti metodologi ospedalieri o di aziende farmaceutiche (statistici ecc.) ...

Noi dovremo "solo" **mettere in moto l'ingranaggio** nel modo giusto (OpenSource / Free software) e gestire l'evoluzione del progetto *à la Linus Torvalds*
