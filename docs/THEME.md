# Tema CyberLions

Il sito continua a essere generato dal template standard di Upptime. Il restyling
usa esclusivamente le opzioni di presentazione di `.upptimerc.yml` e i file in
`assets/`, senza modificare workflow, monitor o dati storici.

## Identità visiva

Palette e immagini provengono dal repository del sito principale
`CyberLions-Italian-Community.github.io`:

- fondo `#131211`, superfici `#1b1917`, bordi `#39342f`;
- testo `#f0eee7`, testo secondario `#b8b2a9`, oro `#d6af70`;
- font di sistema e Instrument Serif corsivo per il titolo;
- logo completo, emblema e favicon della community.

Verde, ambra e rosso continuano a distinguere i diversi stati dei servizi.
La griglia mostra tre colonne su desktop, due su tablet e una su mobile.
I selettori temporali nativi sono accessibili anche tramite tastiera.

## File da modificare

- `assets/cyberlions.css`: tema, layout responsive e stili delle pagine interne.
- `.upptimerc.yml`: titolo, introduzione, navigazione, footer, lingua italiana,
  caricamento del CSS e colori dei grafici.
- `assets/cyberlions-logo.png`, `cyberlions-emblem.png`, `favicon.ico`: immagini
  locali, disponibili anche quando il sito principale non è raggiungibile.

Le regole CSS si appoggiano alla struttura standard di Upptime (`#sapper`,
`.live-status`, `.graph`, `form.r`), senza usare le classi generate da Svelte.
Il nome del sito nella navigazione è nascosto visivamente ma resta disponibile
alle tecnologie assistive.

Il font serif viene caricato da Google Fonts come sul sito principale; in caso di
mancato caricamento viene usato Georgia. Non sono stati aggiunti script.

## Anteprime e verifiche

[Desktop](previews/desktop.png) · [Mobile](previews/mobile.png)

Le immagini sono anteprime locali, non un resoconto dello stato attuale. Usano
il template Upptime 1.17.0, i nove servizi di `history/summary.json`, icone locali
di prova e un incidente di esempio. Le risposte API sono simulate solo durante
la verifica, senza modificare quelle del sito pubblicato.

Controlli effettuati nel browser:

- larghezze 320, 390, 640, 768, 1000 e 1440 px, senza overflow orizzontale;
- presenza dei nove servizi e cambio dei periodi tramite clic e tastiera;
- navigazione verso cronologia, grafico e dettaglio incidente;
- visualizzazione di interruzioni, prestazioni degradate, manutenzioni ed errori;
- assenza di errori JavaScript durante questi percorsi.

La configurazione dei monitor (`sites`), proprietario e repository è stata
confrontata con la versione precedente ed è invariata.
Anche `npm run export` del template è riuscito; nell’output sono stati verificati
lingua, dominio, riferimenti al tema e copia degli asset come nel workflow esistente.

## Pubblicazione

I file sono pronti per essere committati e inviati al repository. Il workflow
esistente **Static Site CI** parte sui cambiamenti in `assets/**`, genera il sito
e lo pubblica su GitHub Pages. Può anche essere avviato manualmente da Actions.
I soli cambiamenti alla configurazione possono richiedere l’avvio manuale o
l’esecuzione programmata del workflow.

Non modificare manualmente i workflow o le pagine generate: Upptime li aggiorna
automaticamente. Dopo un aggiornamento del template, controllare la home e una
pagina di cronologia per verificare che la struttura CSS sia ancora compatibile.
