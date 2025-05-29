---
title: Font.Bidi
linktitle: Bidi
articleTitle: Bidi
second_title: Aspose.Words per .NET
description: Scopri la proprietà Font Bidi, controlla le caratteristiche del testo da destra a sinistra per migliorare la leggibilità e l'esperienza utente nei tuoi progetti web.
type: docs
weight: 30
url: /it/net/aspose.words/font/bidi/
---
## Font.Bidi property

Specifica se il contenuto di questa esecuzione deve avere caratteristiche da destra a sinistra.

```csharp
public bool Bidi { get; set; }
```

## Osservazioni

Questa proprietà, se attiva, non deve essere utilizzata con testo fortemente da sinistra a destra. Qualsiasi comportamento in tale condizione non è specificato. Questa proprietà, se disattivata, non deve essere utilizzata con testo fortemente da destra a sinistra. Qualsiasi comportamento in tale condizione non è specificato.

Quando viene visualizzato il contenuto di questa esecuzione, tutti i caratteri devono essere trattati come caratteri di script complessi per scopi di formattazione. Ciò significa che[`BoldBi`](../boldbi/) ,[`ItalicBi`](../italicbi/) ,[`SizeBi`](../sizebi/) e verrà utilizzato il nome del font corrispondente durante il rendering di questa esecuzione.

Inoltre, quando viene visualizzato il contenuto di questa esecuzione, questa proprietà agisce come un override da destra a sinistra per characters che sono classificati come "tipi deboli" e "tipi neutri".

## Esempi

Mostra come definire set separati di impostazioni dei caratteri per il testo da destra a sinistra e per il testo da destra a sinistra.

```csharp
Document doc = new Document();
DocumentBuilder builder = new DocumentBuilder(doc);

// Definisci un set di impostazioni del carattere per il testo da sinistra a destra.
builder.Font.Name = "Courier New";
builder.Font.Size = 16;
builder.Font.Italic = false;
builder.Font.Bold = false;
builder.Font.LocaleId = new CultureInfo("en-US", false).LCID;

// Definisci un altro set di impostazioni del font per il testo da destra a sinistra.
builder.Font.NameBi = "Andalus";
builder.Font.SizeBi = 24;
builder.Font.ItalicBi = true;
builder.Font.BoldBi = true;
builder.Font.LocaleIdBi = new CultureInfo("ar-AR", false).LCID;

// Possiamo usare il flag Bidi per indicare se il testo che stiamo per aggiungere
// con il generatore di documenti è da destra a sinistra. Quando aggiungiamo testo con questo flag impostato su true,
// verrà formattato utilizzando il set di impostazioni dei caratteri da destra a sinistra.
builder.Font.Bidi = true;
builder.Write("مرحبًا");

// Imposta il flag su false, quindi aggiungi il testo da sinistra a destra.
// Il generatore di documenti formatterà questi utilizzando il set di impostazioni dei font da sinistra a destra.
builder.Font.Bidi = false;
builder.Write(" Hello world!");

doc.Save(ArtifactsDir + "Font.Bidi.docx");
```

### Guarda anche

* class [Font](../)
* spazio dei nomi [Aspose.Words](../../../aspose.words/)
* assemblea [Aspose.Words](../../../)
