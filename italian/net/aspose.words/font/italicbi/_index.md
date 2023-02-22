---
title: Font.ItalicBi
second_title: Aspose.Words per .NET API Reference
description: Font proprietà. Vero se il testo da destra a sinistra è formattato in corsivo.
type: docs
weight: 170
url: /it/net/aspose.words/font/italicbi/
---
## Font.ItalicBi property

Vero se il testo da destra a sinistra è formattato in corsivo.

```csharp
public bool ItalicBi { get; set; }
```

### Esempi

Mostra come definire set separati di impostazioni dei caratteri per il testo da destra a sinistra e da destra a sinistra.

```csharp
Document doc = new Document();
DocumentBuilder builder = new DocumentBuilder(doc);

// Definisci una serie di impostazioni dei caratteri per il testo da sinistra a destra.
builder.Font.Name = "Courier New";
builder.Font.Size = 16;
builder.Font.Italic = false;
builder.Font.Bold = false;
builder.Font.LocaleId = new CultureInfo("en-US", false).LCID;

// Definisci un altro set di impostazioni dei caratteri per il testo da destra a sinistra.
builder.Font.NameBi = "Andalus";
builder.Font.SizeBi = 24;
builder.Font.ItalicBi = true;
builder.Font.BoldBi = true;
builder.Font.LocaleIdBi = new CultureInfo("ar-AR", false).LCID;

// Possiamo usare il flag Bidi per indicare se il testo che stiamo per aggiungere
// con il generatore di documenti è da destra a sinistra. Quando aggiungiamo del testo con questo flag impostato su true,
// verrà formattato utilizzando il set di impostazioni dei caratteri da destra a sinistra.
builder.Font.Bidi = true;
builder.Write("مرحبًا");

// Imposta il flag su false, quindi aggiungi il testo da sinistra a destra.
// Il generatore di documenti li formatterà utilizzando il set di impostazioni dei caratteri da sinistra a destra.
builder.Font.Bidi = false;
builder.Write(" Hello world!");

doc.Save(ArtifactsDir + "Font.Bidi.docx");
```

### Guarda anche

* class [Font](../)
* spazio dei nomi [Aspose.Words](../../font/)
* assemblea [Aspose.Words](../../../)


