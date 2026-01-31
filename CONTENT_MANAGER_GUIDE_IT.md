# Guida per il Content Manager - Agriturismo Mausset

Benvenuto! Questa guida ti aiuterà a gestire i contenuti del sito web Agriturismo Mausset utilizzando Sveltia CMS.

## Accesso al Sistema di Gestione Contenuti (CMS)

**URL del CMS:** https://mausset.valpellice.site/admin/

Il CMS fornisce un'interfaccia user-friendly per modificare i contenuti del sito web multilingue senza necessità di conoscenze tecniche.

---

## Primo Accesso

### Passo 1: Naviga al CMS
Apri il tuo browser e vai a: **https://mausset.valpellice.site/admin/**

### Passo 2: Scegli il Metodo di Accesso
Vedrai due opzioni di login:
- **"Sign In with GitHub"** - Richiede un account GitHub (non consigliato per te)
- **"Sign In with GitHub Using Token"** - Usa questa opzione

### Passo 3: Inserisci il Tuo Token di Accesso
1. Clicca su **"Sign In with GitHub Using Token"**
2. Apparirà un campo di testo
3. Incolla il Token di Accesso Personale che hai ricevuto (è una lunga stringa che inizia con `ghp_`)
4. Clicca su **"Sign in"**

### Passo 4: Sei Dentro!
Il pannello di controllo del CMS si caricherà, mostrando tutte le collezioni di contenuti disponibili in quattro lingue.

---

## Importante: Archiviazione e Sicurezza del Token

### Come Funziona l'Archiviazione del Token
- Il tuo token viene salvato nella memoria locale del browser
- Devi inserirlo **una sola volta per browser**
- Persiste anche dopo aver chiuso il browser
- Funziona indefinitamente a meno che il token non scada

### Quando Devi Reinserire il Token
- Utilizzando un browser diverso (Chrome, Firefox, Safari, ecc.)
- Utilizzando un dispositivo diverso (laptop, tablet, telefono)
- Utilizzando la modalità navigazione in incognito/privata
- Dopo aver cancellato la cache/dati del browser
- Se il token scade (controlla la data di scadenza)

### Best Practice di Sicurezza
- ✅ Mantieni il tuo token confidenziale - è come una password
- ✅ Non condividerlo con nessun altro
- ✅ Non pubblicarlo o includerlo in screenshot
- ✅ Conservalo in modo sicuro (consigliato un password manager)
- ⚠️ Su un computer condiviso, usa la modalità incognito così il token non viene salvato
- ⚠️ Chiunque abbia accesso al tuo browser può usare il CMS se sei loggato

---

## Utilizzo del CMS - Sito Multilingue

### Collezioni di Contenuti Disponibili

Il sito supporta **quattro lingue**:
- 🇮🇹 **Italiano** (IT) - Pagine nella directory principale
- 🇬🇧 **Inglese** (EN) - Pagine in `/en/`
- 🇩🇪 **Tedesco** (DE) - Pagine in `/de/`
- 🇫🇷 **Francese** (FR) - Pagine in `/fr/`

**1. Blog Posts (Articoli del Blog)**
- Crea nuovi articoli
- Modifica articoli esistenti
- Aggiungi categorie e tag
- Programma le date di pubblicazione

**2. Pages (Italian) - Pagine in Italiano**
- Home (Pagina Iniziale)
- About (Chi Siamo)
- Contact (Contatti)
- Prodotti (I nostri prodotti)
- Spazi (Gli spazi)
- Stanze (Le camere)
- Animali (I nostri animali)
- Prezzi
- Regina (Regina di miele)
- Past (Storia)

**3. Pages (English) - Pagine in Inglese**
Stesse pagine disponibili in inglese nella directory `/en/`

**4. Pages (German) - Pagine in Tedesco**
Stesse pagine disponibili in tedesco nella directory `/de/`

**5. Pages (French) - Pagine in Francese**
Stesse pagine disponibili in francese nella directory `/fr/`

### Gestione dei Contenuti Multilingue

**Importante:** Ogni lingua ha la propria collezione separata. Quando aggiorni contenuti:
1. Seleziona la lingua appropriata dalla sidebar
2. Modifica la pagina in quella lingua
3. Ripeti per altre lingue se necessario

**Suggerimento:** È buona prassi mantenere i contenuti sincronizzati tra le lingue, ma ogni lingua è indipendente.

### Apportare Modifiche

1. **Seleziona la lingua** dalla sidebar (Pages Italian, Pages English, ecc.)
2. **Seleziona una pagina** da modificare
3. **Modifica il contenuto** utilizzando l'editor visuale
4. **Campi disponibili:**
   - **Title:** Titolo della pagina
   - **Tagline:** Sottotitolo opzionale
   - **Icon:** Icona FontAwesome (es. `fa-home`, `fa-leaf`, `fa-bed`)
   - **Group:** Dove appare la pagina (`navigation` o `footer`)
   - **Body:** Contenuto principale in Markdown
5. **Aggiungi immagini** caricandole o selezionandole dalla libreria media
6. **Salva le modifiche** - clicca sul pulsante **"Save"**
7. **Pubblica** - Le modifiche vengono salvate nel repository

### Visualizzare il Sito Pubblicato

Dopo aver salvato, clicca sul pulsante **"View on Live Site"** per vedere le tue modifiche nella pagina web reale.

### Workflow di Pubblicazione

- **Draft (Bozza):** Lavoro in corso, non visibile sul sito
- **Published (Pubblicato):** Le modifiche sono salvate e appariranno sul sito web

**Importante:** Dopo il salvataggio, il sito web si ricostruisce automaticamente (richiede 1-2 minuti). Le tue modifiche saranno live poco dopo la pubblicazione.

---

## Suggerimenti per la Modifica dei Contenuti

### Formattazione del Testo
- Usa la barra degli strumenti dell'editor per la formattazione
- **Grassetto**, *corsivo*, elenchi, titoli sono tutti supportati
- Funziona anche la sintassi Markdown se la conosci

### Aggiungere Immagini
1. Clicca sul pulsante immagine o trascina e rilascia
2. Le immagini sono archiviate in `assets/images/`
3. Usa nomi di file descrittivi
4. Ottimizza le immagini prima del caricamento (comprimi file grandi)

### Icone FontAwesome
Il campo "Icon" accetta nomi di icone FontAwesome:
- `fa-home` - Casa
- `fa-info-circle` - Informazioni
- `fa-envelope` - Contatti
- `fa-leaf` - Natura/prodotti
- `fa-bed` - Camere
- `fa-paw` - Animali
- `fa-euro-sign` - Prezzi

Cerca altre icone su: https://fontawesome.com/icons

### Campo Group (Gruppo)
- **navigation:** La pagina appare nel menu principale
- **footer:** La pagina appare nel footer del sito
- Lascia vuoto per pagine che non devono apparire nei menu

---

## Risoluzione dei Problemi

### "Failed to load" o "Cannot connect"
- Controlla la tua connessione internet
- Verifica di essere loggato (aggiorna la pagina)
- Il token potrebbe essere scaduto - reinseriscilo

### Le Modifiche Non Appaiono
- Aspetta 2-3 minuti per la ricostruzione del sito
- Cancella la cache del browser (Ctrl+F5 o Cmd+Shift+R)
- Controlla di aver cliccato "Save" e che lo stato sia "Published"

### Token di Accesso Perso
- Contatta l'amministratore del sito per generare un nuovo token
- Il vecchio token verrà revocato quando ne viene emesso uno nuovo

### Hai Bisogno di Aiuto?
Contatta l'amministratore del sito web se incontri problemi o hai domande.

---

## Riferimento Rapido

| Azione | Come Fare |
|--------|-----------|
| Login | https://mausset.valpellice.site/admin/ → "Sign In with Token" |
| Crea Articolo | Blog Posts → New Post |
| Modifica Pagina IT | Pages (Italian) → Seleziona pagina → Edit |
| Modifica Pagina EN | Pages (English) → Seleziona pagina → Edit |
| Modifica Pagina DE | Pages (German) → Seleziona pagina → Edit |
| Modifica Pagina FR | Pages (French) → Seleziona pagina → Edit |
| Aggiungi Immagine | Pulsante Upload nell'editor |
| Visualizza Live | Pulsante "View on Live Site" |
| Salva e Pubblica | Save → Status: Published |
| Logout | Clicca icona profilo → Sign out |

---

## Informazioni sul Sito Web

- **Sito Web Pubblico:** https://mausset.valpellice.site
- **Pannello Admin CMS:** https://mausset.valpellice.site/admin/
- **Hosting:** Netlify
- **Repository Contenuti:** GitHub (tutte le modifiche sono versionizzate)
- **Lingue Supportate:** Italiano, Inglese, Tedesco, Francese

---

## Struttura delle Lingue

```
/ (root)          → Italiano (IT)
/en/              → Inglese (EN)
/de/              → Tedesco (DE)
/fr/              → Francese (FR)
```

Ogni lingua ha le stesse pagine disponibili, gestite separatamente nel CMS per mantenere contenuti indipendenti e tradotti.

---

*Ultimo aggiornamento: 31 Gennaio 2026*
