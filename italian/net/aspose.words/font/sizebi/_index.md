---
title: Font.SizeBi
linktitle: SizeBi
articleTitle: SizeBi
second_title: Aspose.Words per .NET
description: Regola facilmente la dimensione del carattere in punti per i documenti da destra a sinistra. Migliora la leggibilità e il design con la nostra proprietà Font SizeBi, facile da usare!
type: docs
weight: 360
url: /it/net/aspose.words/font/sizebi/
---
## Font.SizeBi property

Ottiene o imposta la dimensione del carattere in punti utilizzata in un documento con scrittura da destra a sinistra.

```csharp
public double SizeBi { get; set; }
```

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
