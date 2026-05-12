# KTS Advisory — Sito Web

Sito multi-page per **KTS Advisory**, boutique advisory indipendente con sede a Milano.

---

## Struttura dei file

```
kts-advisory/
├── index.html        → Home
├── about.html        → Chi Siamo
├── attivita.html     → Attività
├── approccio.html    → Approccio
├── contatti.html     → Contatti
└── README.md         → Questo file
```

---

## Come visualizzare in locale

1. Scarica tutti i file nella stessa cartella
2. Apri `index.html` con un browser (doppio click)
3. La navigazione tra le pagine funziona automaticamente

> I link tra le pagine usano percorsi relativi — tutti i file devono stare nella stessa cartella.

---

## Come pubblicare online

### Netlify Drop (consigliato — 5 minuti)
1. Vai su [netlify.com/drop](https://netlify.com/drop)
2. Trascina l'intera cartella nella pagina
3. Il sito è online istantaneamente
4. Per collegare un dominio personalizzato: **Site settings → Domain management → Add domain**

### Vercel
1. Crea un account su [vercel.com](https://vercel.com)
2. Clicca **Add New → Project**
3. Carica i file o importa da GitHub
4. Deploy automatico con HTTPS incluso

### GitHub Pages
1. Crea un repository su GitHub
2. Carica tutti i file nella root del repository
3. Vai su **Settings → Pages → Source: main branch**
4. Il sito sarà disponibile su `username.github.io/nome-repo`

---

## Dominio personalizzato

Acquista il dominio (es. `ktsadvisory.com`) su:
- [Namecheap](https://namecheap.com) — consigliato, ~10€/anno
- [Register.it](https://register.it) — alternativa italiana

Dopo l'acquisto, segui le istruzioni del tuo hosting per collegare i DNS.

---

## Brand & Design

| Elemento | Valore |
|---|---|
| Background principale | `#F3EFE8` (avorio caldo) |
| Testo | `#161616` (carbon) |
| Accento | `#B08A4A` (brass) |
| Secondario | `#8B847C` (greige) |
| Sfondi scuri | `#1B1B1B` |
| Serif | Cormorant Garamond |
| Sans-serif | DM Sans |

---

## Come aggiornare i contenuti

I testi sono direttamente nell'HTML di ogni pagina. Per modificarli:

1. Apri il file corrispondente con un editor di testo (es. VS Code, Notepad++)
2. Cerca il testo da modificare con **Ctrl+F**
3. Modifica e salva
4. Ricarica la pagina nel browser per vedere le modifiche

Per aggiornare il sito online dopo una modifica, ri-carica i file sull'hosting (su Netlify basta trascinare di nuovo la cartella su netlify.com/drop).

---

## Aggiungere immagini reali

Attualmente il lato destro dell'hero e alcune sezioni usano sfondi geometrici generati in CSS. Per sostituirli con immagini reali:

1. Aggiungi l'immagine nella cartella (es. `hero.jpg`)
2. Sostituisci il blocco `hero-img-placeholder` con:

```html
<img src="hero.jpg" alt="" class="hero-img">
```

Le immagini consigliate per il brand KTS sono di tipo **architettonico**: cemento, luce naturale, geometrie pulite. Niente stock fotografico generico.

---

## Note tecniche

- Nessuna dipendenza esterna oltre Google Fonts (caricati via CDN)
- Nessun JavaScript framework — vanilla JS puro
- Compatibile con tutti i browser moderni
- Font: caricati da Google Fonts (richiede connessione internet)
- Form contatti: attualmente frontend only — per ricevere le email integrare con [Netlify Forms](https://docs.netlify.com/forms/setup/) o [Formspree](https://formspree.io)

---

## Integrare il form contatti (ricevere email reali)

### Con Netlify Forms (gratuito)
Aggiungi `netlify` al tag del form in `contatti.html`:

```html
<!-- Sostituisci il div id="form-wrap" con un vero form -->
<form name="contatti" method="POST" data-netlify="true">
```

Netlify intercetta automaticamente le submission e le invia via email.

### Con Formspree
1. Crea un account su [formspree.io](https://formspree.io)
2. Crea un nuovo form e copia l'endpoint
3. Aggiungi `action="https://formspree.io/f/XXXXX" method="POST"` al form

---

*KTS Advisory — Struttura. Visione. Risultato.*
