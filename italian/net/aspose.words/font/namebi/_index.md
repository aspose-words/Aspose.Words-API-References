---
title: Font.NameBi
linktitle: NameBi
articleTitle: NameBi
second_title: Aspose.Words per .NET
description: Scopri come impostare e personalizzare facilmente i nomi dei font per i documenti in lingue da destra a sinistra, migliorando la leggibilità e il design. Ottimizza il tuo testo oggi stesso!
type: docs
weight: 250
url: /it/net/aspose.words/font/namebi/
---
## Font.NameBi property

Restituisce o imposta il nome del font in un documento in una lingua con scrittura da destra a sinistra.

```csharp
public string NameBi { get; set; }
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

* property [Name](../name/)
* class [Font](../)
* spazio dei nomi [Aspose.Words](../../../aspose.words/)
* assemblea [Aspose.Words](../../../)
