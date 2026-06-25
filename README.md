# Nucleo v2

**La prossima mossa con i tuoi soldi.** Tre schermate, un solo gesto: scorri.

## Novità v9 — feeling app nativa, fatto per dita grosse

Tarato su iPhone 13 mini (schermo piccolo), pensato per l'uso quotidiano senza pensieri.

- **Tutto a misura di dito:** ogni voce, tile e pulsante rispetta i target tattili iOS (≥44pt), con testo proporzionato e leggibile anche sullo schermo piccolo.
- **Feedback nativo alla pressione:** ogni elemento toccabile «affonda» leggermente come in un'app vera; niente lampeggi da pagina web.
- **Niente sensazione-browser:** nessuna selezione testo accidentale sulla chrome, scroll con inerzia, tab bar e fogli in vetro iOS, status bar pulita una volta aggiunta alla Home.
- **Tab bar grande e centrabile**, composer e tastierino più ampi, fogli (modifica rapida, nuovo obiettivo) in stile foglio modale iOS con maniglia.
- Light e dark mode nativi, rispetto di «riduci trasparenza/movimento».

## Novità v8 — una riga, una mossa

Il principio non è «l'app fa tutto al posto tuo» (sarebbe la strada per ripetere gli errori del passato), ma **minimo sforzo da parte tua, massima chiarezza per le tue decisioni**.

- **All'apertura vedi una sola cosa:** una frase che dice come stai e **una** mossa da fare oggi (un tap). Tutto il resto è dietro «Vedi i dettagli».
- **La mossa è sempre quella che conta davvero**, scelta dallo stato reale: registrare lo stipendio il giorno giusto, pagare la fissa in scadenza, tenere la barra se sei stretto, o mettere una quota in un obiettivo se hai margine.
- **Tu decidi, l'app prepara.** Niente automatismi sui soldi: la mossa la esegui tu con un tap, e puoi sempre annullare.
- **Crescita per attrito giusto:** vedere, scegliere, correggere — non delegare.

## Novità v7 — liquidità reale, fisse-promemoria, obiettivi multipli

- **Vedi la liquidità totale, sempre intatta.** «Hai in tutto» mostra ciò che possiedi davvero; «Impegnato» (fisse da pagare + programmate) è mostrato a parte, non nascosto; «Risparmi» è separato.
- **Le fisse non si auto-sottraggono più.** Sono un promemoria nella lista «da pagare»: contano sul conto **solo quando le paghi** (tocchi «Paga» → diventa un'uscita). Niente più budget che crolla in NERO per affitti già pagati. È la radice del vecchio «non funziona».
- **Interruttore tuo:** in ⚙︎ → «Come calcolo il budget» decidi se gli impegni riducono il «puoi spendere» o restano solo promemoria.
- **Budget su tre orizzonti:** al giorno, a settimana, a fine ciclo.
- **Obiettivi di risparmio multipli** (casa, viaggio, emergenza…): ognuno con saldo, traguardo e barra. Aggiungi con un tap; le entrate si proteggono verso l'obiettivo scelto.

## Novità v6 — tu comandi i numeri, l'IA solo consiglia

Il principio è cambiato dopo l'uso reale: **l'IA non tocca più un solo euro.**

- **Comunichi solo entrate e uscite.** `−15 benzina`, `+1097 stipendio`, `−7,50 bar`. Il `−` è un'uscita, il `+` un'entrata. Tutto qui.
- **L'IA è in sola lettura.** Risponde alle domande («come sto messo?»), legge gli scontrini e ti *dice cosa scrivere*, ma non registra e non modifica niente. Niente più numeri inventati o doppi conteggi: i calcoli li fa il codice, sempre uguali.
- **I numeri sono tuoi.** Tocca **Sul conto**, **Risparmi**, **Ticket** direttamente nella schermata Oggi (o il link **Correggi**) e li sistemi a mano in un attimo, con scorciatoie ±10/±50. Quando app e realtà divergono, riallinei in 10 secondi.
- Accantonamenti e spese programmate restano disponibili ma **facoltativi**, mai imposti.

## Novità v5 — comunicazione, flussi a un tap, soldi sempre visibili

Nate dall'uso reale (un backup di una giornata storta):

- **Una conferma sola, con un tap.** Niente più «Confermo?» → «Conferma». Quando chiedi un'azione sui soldi, Nucleo mostra **una chip**: la tocchi una volta e l'azione è fatta, con un **Annulla** discreto per qualche secondo. Vale per accantonamenti, protezione delle entrate, stipendio.
- **Spese programmate (la novità chiave).** «Metti da parte 300 per il meccanico» non è una spesa già uscita: Nucleo la **accantona, la toglie dal budget e te la ricorda** in una sezione dedicata a sinistra. Quando paghi, tocchi **Pagata** e diventa spesa reale. (Prima questa cosa veniva registrata come spesa subito — sbagliato.)
- **A sinistra vedi DOVE sono i tuoi soldi.** Una «mappa del denaro» in tre blocchi: **Libero** (spendibile), **Risparmi 🔒** (il fondo, finalmente visibile), **Programmato 📌** (messo da parte per spese future). Più la sezione Risparmi con totale e obiettivo.
- **Stipendio in un colpo.** Se l'importo reale è diverso dal previsto, scrivi «stipendio 1097» e registra quello, riapre il ciclo, riporta le fisse «da pagare» ed esce dall'emergenza — un'azione sola.
- **Niente JSON in chat.** Risolto il bug per cui a volte appariva il codice grezzo della risposta IA.

## Allineamento alle Apple Human Interface Guidelines (iOS 26 · Liquid Glass)

L'interfaccia segue le HIG attuali e i tre principi di iOS 26 — **Hierarchy, Harmony, Consistency**:

- **Liquid Glass solo sulla navigazione.** Materiale translucido con blur+saturate (lensing), highlight speculare e hairline rifrattiva applicato esclusivamente al *livello che galleggia sopra il contenuto*: nav bar in alto, **tab bar inset a capsula** in basso (Oggi · Parla · Storico), e composer della chat. Il contenuto scorre sotto il vetro e resta su superfici opache → gerarchia per profondità, non per rumore.
- **Tipografia di sistema SF Pro** con le text style iOS (Large Title 34, Body 17, Subheadline 15, Footnote 13, Caption) e numeri tabulari.
- **Colori semantici** (system grouped backgrounds, label/secondary/tertiary, separator) in **light e dark** automatici. Il tint segue il semaforo, mappato sui **System Colors** Apple (systemGreen/Yellow/Red/Gray).
- **Inset grouped lists**, **segmented control**, sheet di impostazioni in stile `UISheetPresentationController`.
- **Touch target ≥ 44pt**, safe area insets su notch e home indicator.
- **Accessibilità HIG:** rispetto di `prefers-reduced-transparency` (il vetro diventa opaco) e `prefers-reduced-motion` (niente animazioni).

```
←  OGGI & MOSSE          CONVERSAZIONE          STORICO & GRAFICO  →
   budget, semaforo,     parli, alleghi,        andamento 30 gg,
   task spuntabili       Nucleo registra        categorie, pattern
```

## Le tre schermate

**Centro (principale) — Conversazione.** Scrivi come parli: `7,50 bar per noia`, `+80 vendita usato`, `accantona 50`, `quanto posso spendere?`. Nucleo capisce, ti mostra una card di conferma modificabile e registra. Col **＋** alleghi file: foto di scontrini (con IA) o CSV bancari (anche senza IA).

**Sinistra — Oggi & mosse.** Budget gigante, semaforo che tinge tutta l'app, e le azioni del giorno come **task spuntabili**. L'IA può aggiungerne di sue.

**Destra — Storico.** Grafico SVG dell'andamento del denaro disponibile (ultimi 30 giorni), spese per categoria, pattern rilevati, lista movimenti.

## IA integrata (opzionale ma consigliata)

In ⚙ → Intelligenza incolli una **API key Anthropic** (resta solo sul telefono, chiamata diretta dal browser). Con la chiave:
- conversazione libera in linguaggio naturale
- lettura **foto di scontrini** → registrazione automatica
- interpretazione di **qualsiasi CSV** bancario
- l'IA può registrare movimenti, accantonare, aggiungere task, cambiare modalità — sempre confermando con te

Senza chiave, il **parser locale** capisce comunque importi, categorie (per parole chiave), metodo, comandi e domande base. Tutto funziona offline.

## Apprendimento («human learning»)

Nucleo si personalizza nel tempo, in due strati:
1. **Vocabolario appreso**: quando correggi una categoria nella card di conferma, memorizza l'associazione (es. `«esselunga» → cibo`) e da lì in poi categorizza da solo. Visibile e cancellabile in ⚙ → «Cosa ha imparato su di te».
2. **Note di profilo**: l'IA salva abitudini osservate («spende per noia la sera») e le riceve a ogni conversazione, quindi i consigli diventano sempre più tuoi.

Più i pattern classici: fascia oraria impulsiva, categoria evitabile più pesante, spese emotive.

## Deploy su GitHub Pages

1. Repo nuovo (es. `nucleo`), carica i 6 file nella root: `index.html`, `manifest.webmanifest`, `sw.js`, `icon-192.png`, `icon-512.png`, `apple-touch-icon.png`
2. Settings → Pages → Deploy from a branch → `main` / root
3. Online su `https://TUOUSERNAME.github.io/nucleo/`

## Su iPhone

Apri l'URL in **Safari** → Condividi → **Aggiungi a Home**. App a schermo intero, offline, con icona.

## Note

- Dati in localStorage: fai «Esporta backup» ogni tanto (⚙ → Dati).
- Il giorno dello stipendio Nucleo te lo chiede in chat e riapre il ciclo.
- La chiamata IA usa l'header `anthropic-dangerous-direct-browser-access`: la chiave non passa da nessun server tuo, ma non condividere l'URL con la chiave salvata su dispositivi altrui.
