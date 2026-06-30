# Nucleo v3 — contabile, non amico

**Riporti entrate e uscite, le vedi, le correggi. Punto.**




## Novità v13 — Resilienza dei dati (non perdere mai tutto)

I dati di Nucleo vivono sul telefono. Se Safari pulisce i dati del sito, sparirebbero. Tre difese:

- **Copia di sicurezza interna automatica.** A ogni salvataggio Nucleo scrive una seconda copia. Se il dato principale si corrompe (illeggibile), all'avvio **recupera dalla copia e ripara** — niente più dati persi per corruzione.
- **Storage persistente.** All'avvio l'app chiede al browser di non cancellare i suoi dati (best-effort: riduce gli sfratti automatici di Safari).
- **Backup off-device in un tap.** ⚙︎ → Backup e ripristino → **Salva una copia**: iOS apre il foglio di condivisione, scegli «Salva su File» → **iCloud Drive**. La ritrovi anche cambiando telefono. **Ripristina** ricarica una copia in un tap.
- **Promemoria discreto** sul Registro se non fai un backup da oltre 7 giorni, dopo 20+ movimenti nuovi, o se non l'hai mai fatto. Ha priorità sul promemoria di riconciliazione (perdere tutto è peggio di una piccola deriva).

Nota onesta: nessun backup automatico off-device è possibile in una PWA (il browser non può scrivere su File/iCloud senza un tuo tap). Per questo il backup resta un gesto tuo — ma reso facile e ricordato.


## Novità v12 — Riconciliazione (chiudere il cerchio della fiducia)

Il problema ricorrente ("le spese a puttane") nasceva da una cosa sola: l'app poteva derivare in silenzio dalla realtà della banca. La riconciliazione lo rende impossibile.

- **Tocca «Saldo conto» (o «Correggi»)** → ti chiede *quanto c'è davvero in banca adesso*.
- Mostra lo **scarto in tempo reale** ("la banca ha X in più/meno dell'app") e, con un tap, **allinea**.
- La differenza non sparisce: viene scritta come **riga di aggiustamento** nel registro (⚖️), tracciabile e reversibile come ogni altro movimento. Niente più sovrascritture silenziose.
- Gli aggiustamenti **non** contano come entrate/uscite del ciclo né nelle statistiche: sono solo allineamenti.
- **Promemoria discreto** sul Registro se non riconcili da oltre due settimane (o non l'hai mai fatto). Informa, non assilla.

Come ripartire pulito col tuo conto incasinato: apri il Registro → **Riconcilia** → scrivi il saldo reale della banca → Allinea. In un tap i conti tornano veri, e la differenza resta segnata.


## Novità v11 — estratti banca/Satispay + salute finanziaria

**Import resoconti (⚙︎ → Estratti banca / Satispay).** Esporti i movimenti in **CSV** dall'app della banca o di Satispay e li carichi qui. Nucleo riconosce le colonne (data, importo, descrizione; anche formati Dare/Avere) e ti mostra **una riga per movimento da spuntare**: tieni quelle giuste, scarti le altre, sistemi la categoria, poi premi Importa. Niente viene scritto prima della tua conferma.
- I movimenti importati sono **storico**: popolano il registro e i totali del ciclo ma **non toccano il saldo** (la banca lo riflette già). Così non si creano doppioni.
- **Niente collegamento in tempo reale:** una PWA non può accedere ai conti (serve un intermediario PSD2 con licenza; Satispay non ha API pubblica). Onestà sopra le promesse.
- Excel: esporta in CSV (l'app resta leggera e offline).

**Salute finanziaria (Storico).** Due numeri che contano per un lavoratore dipendente:
- **Mesi di autonomia** = risparmi ÷ spesa media mensile (il tuo cuscinetto reale).
- **Tasso di risparmio** del ciclo.
Con una nota tarata sulla fascia (sotto 1 mese / 1–3 / 3–6 / oltre 6). Sono strumenti e stime, non consulenza fiscale.


## Come funziona
- **Registro (schermata centrale, è la casa):** la lista di tutti i movimenti, dal più recente. In alto: entrate del ciclo, uscite del ciclo, saldo. Ogni riga si tocca per **modificarla o eliminarla** — così togli i doppioni e gli errori da te.
- **＋ Aggiungi → tastierino:** Uscita/Entrata, importo col tastierino numerico, categoria, metodo (carta/contanti/ticket), nota. Veloce, niente chat.
- **📷 Scansiona:** la fotocamera legge il totale dello scontrino e lo precompila (richiede la chiave IA in ⚙︎; senza, scrivi tu l'importo).
- **Oggi:** cruscotto freddo — quanto puoi spendere, liquidità (hai in tutto / impegnato / risparmi), fisse da pagare, obiettivi. Nessun suggerimento, nessun "amico".
- **Storico:** andamento e categorie.

## Coerenza dei numeri
Ogni movimento ha un effetto preciso sul saldo. Quando **modifichi o elimini** una riga, l'effetto viene **invertito esattamente**: il saldo resta sempre giusto. Il bug per cui le spese "andavano a puttane" nasceva dal non poter correggere le righe: ora puoi.

L'IA non conta i soldi: serve solo per lo scanner scontrini, se la attivi.

## Sistemare i tuoi dati incasinati
Apri il Registro, tocca le righe doppie o di prova e premi **Elimina movimento**: il saldo si ricorregge da solo. In alternativa tocca **Saldo conto** e scrivi il valore reale della banca: è l'ancora di verità.
