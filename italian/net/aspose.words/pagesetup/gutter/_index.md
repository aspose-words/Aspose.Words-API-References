---
title: PageSetup.Gutter
linktitle: Gutter
articleTitle: Gutter
second_title: Aspose.Words per .NET
description: Regola le impostazioni di rilegatura di PageSetup per ottimizzare i margini del documento per la rilegatura. Migliora il tuo layout con margini perfetti per risultati professionali.
type: docs
weight: 160
url: /it/net/aspose.words/pagesetup/gutter/
---
## PageSetup.Gutter property

Ottiene o imposta la quantità di spazio extra aggiunto al margine per la rilegatura del documento.

```csharp
public double Gutter { get; set; }
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

Mostra come impostare i margini di rilegatura.

```csharp
Document doc = new Document();

// Inserisci testo che si estende su più pagine.
DocumentBuilder builder = new DocumentBuilder(doc);
for (int i = 0; i < 6; i++)
{
    builder.Write("Lorem ipsum dolor sit amet, consectetur adipiscing elit, " +
                  "sed do eiusmod tempor incididunt ut labore et dolore magna aliqua.");
    builder.InsertBreak(BreakType.PageBreak);
}

// Una rilegatura aggiunge spazi vuoti al margine sinistro o destro della pagina,
// che compensa la piegatura centrale delle pagine di un libro, invadendo l'impaginazione della pagina stessa.
PageSetup pageSetup = doc.Sections[0].PageSetup;

 // Determina quanto spazio le nostre pagine hanno a disposizione per il testo all'interno dei margini e poi aggiungi un importo per riempire un margine.
Assert.AreEqual(470.30d, pageSetup.PageWidth - pageSetup.LeftMargin - pageSetup.RightMargin, 0.01d);

pageSetup.Gutter = 100.0d;

// Imposta la proprietà "RtlGutter" su "true" per posizionare il gutter in una posizione più adatta per il testo da destra a sinistra.
pageSetup.RtlGutter = true;

// Imposta la proprietà "MultiplePages" su "MultiplePagesType.MirrorMargins" per alternare
// la posizione dei margini sul lato sinistro/destro di ogni pagina.
pageSetup.MultiplePages = MultiplePagesType.MirrorMargins;

doc.Save(ArtifactsDir + "PageSetup.Gutter.docx");
```

### Guarda anche

* class [PageSetup](../)
* spazio dei nomi [Aspose.Words](../../../aspose.words/)
* assemblea [Aspose.Words](../../../)
