---
title: PageSetup.SheetsPerBooklet
second_title: Aspose.Words per .NET API Reference
description: PageSetup proprietà. Restituisce o imposta il numero di pagine da includere in ciascun booklet.
type: docs
weight: 400
url: /it/net/aspose.words/pagesetup/sheetsperbooklet/
---
## PageSetup.SheetsPerBooklet property

Restituisce o imposta il numero di pagine da includere in ciascun booklet.

```csharp
public int SheetsPerBooklet { get; set; }
```

### Esempi

Mostra come configurare un documento che può essere stampato come piega a libro.

```csharp
Document doc = new Document();

// Inserisci testo che si estende su 16 pagine.
DocumentBuilder builder = new DocumentBuilder(doc);
builder.Writeln("My Booklet:");

for (int i = 0; i < 15; i++)
{
    builder.InsertBreak(BreakType.PageBreak);
    builder.Write($"Booklet face #{i}");
}

// Configura la proprietà "PageSetup" della prima sezione per stampare il documento sotto forma di piegatura del libro.
// Quando stampiamo questo documento su entrambi i lati, possiamo prendere le pagine per impilarle
// e piegali tutti al centro contemporaneamente. Il contenuto del documento si allineerà in una piega a libro.
PageSetup pageSetup = doc.Sections[0].PageSetup;
pageSetup.MultiplePages = MultiplePagesType.BookFoldPrinting;

// Possiamo specificare il numero di fogli solo in multipli di 4.
pageSetup.SheetsPerBooklet = 4;

doc.Save(ArtifactsDir + "PageSetup.Booklet.docx");
```

### Guarda anche

* class [PageSetup](../)
* spazio dei nomi [Aspose.Words](../../pagesetup/)
* assemblea [Aspose.Words](../../../)


