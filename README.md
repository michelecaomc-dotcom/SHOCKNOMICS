# ⚡ Shocknomics

Report e ricerche di **economia, geopolitica, energia, sport e mercati** — analisi indipendenti
costruite su dati pubblici, **scaricabili gratuitamente**. Il sito è organizzato in **edizioni mensili**:
l'Edizione 0 è Novembre 2026, le prossime si aggiungono a ritmo di mese.

🌍 **Site multilingua**: l'intera interfaccia (titoli, riassunti, pulsanti, condivisioni) è disponibile
in **Italiano, English, 中文 e हिन्दी** — i visitatori cambiano lingua con i pulsanti in alto
(scelta memorizzata nel browser). I PDF restano nella lingua originale di redazione.

## Struttura

```
report-site/
├── index.html    ← il sito completo (HTML + CSS + JS in un unico file)
├── pdfs/         ← i PDF delle edizioni, rinominati con data e titolo pulito
└── README.md     ← questo file
```

## Come pubblicare GRATIS su GitHub Pages (5 minuti)

1. **Crea un account gratuito** su [github.com](https://github.com/signup) (se non lo hai già).
2. **Crea un repository nuovo**: bottone `+` in alto a destra → `New repository`.
   - Nome consigliato: `shocknomics` (verrà pubblicato su `tuousername.github.io/shocknomics/`)
   - Visibilità: **Public** (necessario per Pages gratuito)
   - NON aggiungere README o .gitignore (li hai già qui)
   - Clicca `Create repository`
3. **Carica i file**: clicca `uploading an existing file` e **trascina il contenuto della
   cartella `report-site`** (il file `index.html` e la cartella `pdfs`).
4. Clicca `Commit changes`.
5. **Attiva GitHub Pages**: `Settings` → `Pages` → in `Build and deployment` scegli
   **Branch: `main`**, **Folder: `/ (root)`** → `Save`.
6. Attendi 1-2 minuti: il sito è live su `https://tuousername.github.io/shocknomics/`
7. **Fatto!** I pulsanti di condivisione usano automaticamente l'URL del sito pubblicato.

> 💡 Il sito è HTML puro, senza build né database. GitHub Pages è gratuito entro limiti
> molto generosi (~100 GB/mese di traffico soft-limit), più che sufficienti per i PDF.

## Come aggiungere l'edizione successiva (es. Dicembre 2026)

1. **PDF**: copia i nuovi report in `pdfs/` con il formato nome
   `AAAA-MM-GG_titolo-breve.pdf` (così compaiono già in ordine cronologico).
2. **Card**: in `index.html` duplica un blocco `<article class="card">…</article>` e cambia:
   - `id` (abbreviazione unica, es. `ed1-brent-2027`)
   - `data-cat` (categoria: `energia`, `metalli`, `azionario`, `sport` — o aggiungine una
     nuova chip nel menu e il colore in CSS)
   - titolo, riassunto, `meta` (pagine · dimensione), `href` del PDF
   - i `data-title` dei pulsanti di condivisione
3. **Edizione**: aggiorna il badge nell'header (`EDIZIONE 1 · DICEMBRE 2026`) e le
   statistiche (numero report e pagine). Se vuoi tenere tutte le edizioni visibili insieme,
   lascia tutto in unica pagina: il filtro categoria e la ricerca aiutano la navigazione.
4. Ricarica i file sul repository: il sito si aggiorna in 1-2 minuti.

> 📌 In futuro, se le edizioni crescono molto, si può passare a una pagina per edizione
> (`nove2026.html`, `dic2026.html`…) con la home che fa da indice. Per ora l'unica pagina
> con filtri è la soluzione più semplice ed efficace.

## Alternative gratuite

- **Netlify Drop**: [app.netlify.com/drop](https://app.netlify.com/drop) — trascini la
  cartella `report-site` ed è online in 30 secondi.
- **Cloudflare Pages** / **Vercel**: stesso funzionamento (drag & drop o Git).

## Note legali

Il footer riporta il disclaimer informativo (le analisi non costituiscono consulenza
finanziaria personalizzata, MiFID II). Prima di pubblicare controlla che nei PDF non ci
siano dati sensibili o non pubblicabili; in caso, rimuovili da `pdfs/` e la relativa card
da `index.html`.
