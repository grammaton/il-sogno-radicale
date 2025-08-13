# Classe LaTeX `gs.cls` - appunti personalizzati

Una classe LaTeX personalizzata per la creazione di appunti personalizzati con supporto completo per il testo greco antico e moderno.

## 🔧 Requisiti

### Compilatore
- **XeLaTeX** (obbligatorio)
- Non compatibile con pdfLaTeX o LaTeX tradizionale

### Font richiesti
I seguenti font devono essere installati sul sistema:
- **Alegreya** (Regular, Bold, Italic, BoldItalic)
- **AlegreyaSans** (Regular, Bold, Italic, BoldItalic)  
- **JetBrains Mono**
- **GFS Artemisia** (per il greco)

## 📦 Installazione

1. Scarica il file `gs.cls`
2. Posizionalo nella stessa directory del tuo documento LaTeX, oppure
3. Installalo nella tua distribuzione TeX locale

## 🚀 Utilizzo base

```latex
\documentclass{gs}

\title{I miei appunti di filosofia}
\author{Il tuo nome}
\date{\today}

\begin{document}

\maketitle

\section{Introduzione}
Questi sono i miei appunti di filosofia antica...

\end{document}
```

### Compilazione
```bash
xelatex documento.tex
```

## 📝 Comandi specializzati

### Testo greco
```latex
\greco{φιλοσοφία}  % Per inserire testo greco
```

### Enfasi filosofica
```latex
\concetto{essere}  % Per evidenziare concetti importanti
```

### Etimologie
```latex
\etimologia{filosofia}{\greco{φιλοσοφία}, "amore per la saggezza"}
```

### Citazioni filosofiche
```latex
\begin{citazionefilosofica}{Platone}
L'uomo è un animale sociale che tende naturalmente alla vita in comune.
\end{citazionefilosofica}
```

## 🎨 Personalizzazioni

La classe include:
- **Sezioni personalizzate** con numerazione e font sans-serif
- **Header e footer** eleganti con numerazione pagine
- **Hyperref configurato** automaticamente con metadati PDF
- **Supporto colori** per eventuali evidenziazioni

## 📐 Layout

- **Formato**: A4
- **Font size**: 12pt
- **Margini**: 2.5cm laterali, 3cm superiore/inferiore
- **Stile pagina**: Header con sezione corrente e numero pagina

## 🔍 Dettagli tecnici

### Pacchetti inclusi
- `fontspec`, `xunicode`, `xltxtra` per XeLaTeX
- `polyglossia` per supporto multilingue
- `amsmath`, `amsfonts`, `amssymb` per matematica
- `geometry` per layout
- `hyperref` per collegamenti
- `titlesec` per personalizzazione titoli
- `fancyhdr` per header/footer

### Configurazione automatica PDF
La classe configura automaticamente:
- Titolo e autore del PDF
- Parole chiave: "filosofia, appunti, greco"
- Segnalibri numerati e aperti
