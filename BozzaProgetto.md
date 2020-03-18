## Oggetto principale: 
- raccogliere e mettere a disposizione dati dei PRE-SINTOMI, o EARLY-SYMPTOMS
- utilizzo più diretto possibile (webapp, mobile app) da parte della popolazione, 
eventualmente coadiuvato da call center per le fasce poco alfabetizzate informaticamente
- collegamento con dati di contact tracing contact network (basato su Graph db, e.g. *Neo4j*)

## Caratteristiche distintive (vantaggio competitivo, necessario se vogliamo che il progetto prenda piede)
- APPROCCIO PREVENTIVO (hyp: nessuno finora raccoglie i dati di cosa sente la popolazione
 fino a che un medico non registra la persona come paziente, inserendola in trattamento ospedalizzato 
 o domiciliare. Noi ipotizziamo che ci sia del VALORE inespresso, e pronto da (rac)cogliere, nei sintomi 
 che i singoli cittadini potrebbero raccontare, anche PRIMA che determinino una patologia secondo le griglie definite.
 In altre parole: sintomi non significativi rispetto alle griglie usate per la diagnosi e la terapia, sono invece 
 significativi per la prevenzione se coinvolgono un gran numero di poetnziali pazienti (o pre-pazienti). Questo 
 specialmente in condizioni di emergenza crescente, quando è necessario stringere i criteri di ospedalizzazione e 
 riservare le risorse (scarse) disponibili al trattamento dei casi urgenti, sottraendole di fatto allo studio delle 
 modalità con cui insorge la malattia. 
   - APPROCCIO PROATTIVO Il sistema può anche fornire informazioni, circa particolari sintomi da verificare, e sulle 
   manovre diagnostiche più appropriate per mettere in luce o oggettivare i sintomi (es. dolari localizzati, colorito, 
   manovre di palpazione, ecc.), mediante apposite istruzioni anche audio/video.
- OPEN DATA. Vogliamo raccogliere, persistere, e rendere disponibili i dati dei sintomi pre-malattia, sotto forma di 
 database strutturato e organizzato, APERTO, senza necessariamente proporre delle analisi. Anzi proprio lasciando i 
 dati a disposizione di chi (mondo accademico, centri di ricerca?) titolato a farne uso.
- INTEGRAZIONE / Integrabilità con altre tipologie di dati / database. Ad esempio contact-tracing, geo-localizzazione, 
 basato sui terminali degli utenti (dati raccolti dopo la registrazione al portale) o su basi dati preesistenti, dati 
 diagnostici (tamponi, visite mediche, esami obbiettivi e per immagini ecc.), e cartelle cliniche per gli utenti che 
 evolvono in ospedalizzati o viceversa sperabilmente nella maggior parte dei casi guariscono spontaneamente.

## Sketch / flusso di processo

### Input Layer: 
- Web app + mobile app (+ call center). L'utente (pre-paziente) si registra e inserisce i suoi dati 
anagrafici, la storia clinica che ritiene rilevante, i sintomi recenti e la loro evoluzione temporale. Il sistema non 
è chiuso, ma aperto alle "novità": oltre alla lista di sintomi più rilevanti per le autorità mediche, propone anche i 
sintomi "diversi/originali" a partire dai più gettonati nei vari intorni dell'utente (lavorativo, relazionale, 
scolastico (tramite eventualmente i figli), geografico) ed infine campi di testo libero
- Revision Layer. Utenti di categoria "medici" e/o "triagisti", remotizzati rivedono questo materiale man mano che viene 
inserito, uniformando le osservazioni di pazienti diversi, magari anche raggiungendoli telefonicamente, classificandoli 
per _rilevanza_ (concetto distinto dall'urgenza)
- Legal Layer. In qualche modo l'utente paziente (e anche il medico) devono conoscere il loro diritti rispetto al 
software ed eventualmemte concedere l'uso dei propri dati personali, contatti eccetera ai fini del trattamento medico 
proprio e della collettività ecc. Va assicurato che i dati che vengono resi pubblici non contengano l'identificabilità 
del paziente e forse nemmeno delle zone geografiche o altri elementi di tracciamento (es. scuola, paese, parrocchia 
ecc.) ma che questi vengano sempre esportati in modo anonimo / codificato

### DB Layer:
--CARLA-- coprire gli aspetti fondanti 
- della piataforma / struttura (es GraphDB/NOSQL) 
- delle interfacce di estrazione dati (estrazioni raw))
- delle elaborazioni/analisi di base (estrazioni "aggregate", pre-elaborate, clusterizzate, ...)
- probabilmente bisognerebbe mettere a disposizione anche un buon numero di esperti per formare o adiuvare chi deve 
fare estrazioni ad hoc. 
Tutto questo lo immagino molto versatile, e prederebbe forma mano a mnao che il progetto evolve insieme 
alla pandemia

#### App Layer
Concettualmente è abbastanza banale, ma ovviamente drenerà parecchio effort far sì che sia utilizzabile e adattabile, 
ma credo che in RIOS abbiamo molti esperti.
Il core è un questionario, che include dei branch, e delle informazioni verso chi lo sta compilando. Bisogna che 
sia ben gestita la complessità di un sintomo (localizzazione, durata, frequenza, acutezza dolore, le circostanze con cui si 
manifesta) (es. freddo, palpazione, orari del giorno) la sequenza, la sequenza dei sintomi attraverso più giorni, e visualizzata in modo immediato
A monte ci stanno la registrazione, con tutta la parte legale
Sotto una gestione sicura dei dati, che copre l'interfaccia, ma anche il db.