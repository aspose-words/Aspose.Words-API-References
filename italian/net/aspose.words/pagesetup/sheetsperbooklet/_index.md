---
title: PageSetup.SheetsPerBooklet
linktitle: SheetsPerBooklet
articleTitle: SheetsPerBooklet
second_title: Aspose.Words per .NET
description: Scopri la proprietà PageSetup SheetsPerBooklet per gestire facilmente il conteggio delle pagine degli opuscoli, migliorando il layout del documento e l'efficienza di stampa.
type: docs
weight: 400
url: /it/net/aspose.words/pagesetup/sheetsperbooklet/
---
## PageSetup.SheetsPerBooklet property

Restituisce o imposta il numero di pagine da includere in ogni opuscolo.

```csharp
public int SheetsPerBooklet { get; set; }
```

## Esempi

Mostra come configurare un documento che può essere stampato come piega a libro.

```csharp
Document doc = new Document();

// Inserisci testo che si estenda su 16 pagine.
DocumentBuilder builder = new DocumentBuilder(doc);
builder.Writeln("My Booklet:");

for (int i = 0; i < 15; i++)
{
    builder.InsertBreak(BreakType.PageBreak);
    builder.Write($"Booklet face #{i}");
}

// Configurare la proprietà "PageSetup" della prima sezione per stampare il documento sotto forma di piega a libro.
// Quando stampiamo questo documento su entrambi i lati, possiamo prendere le pagine per impilarle
// e piegali tutti a metà contemporaneamente. Il contenuto del documento si allineerà formando una piega a libro.
PageSetup pageSetup = doc.Sections[0].PageSetup;
pageSetup.MultiplePages = MultiplePagesType.BookFoldPrinting;

// Possiamo specificare il numero di fogli solo in multipli di 4.
pageSetup.SheetsPerBooklet = 4;

doc.Save(ArtifactsDir + "PageSetup.Booklet.docx");
```

### Guarda anche

* class [PageSetup](../)
* spazio dei nomi [Aspose.Words](../../../aspose.words/)
* assemblea [Aspose.Words](../../../)
