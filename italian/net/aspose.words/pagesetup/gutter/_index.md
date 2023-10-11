---
title: PageSetup.Gutter
second_title: Aspose.Words per .NET API Reference
description: PageSetup proprietà. Ottiene o imposta la quantità di spazio aggiuntivo aggiunto al margine per la rilegatura del documento.
type: docs
weight: 160
url: /it/net/aspose.words/pagesetup/gutter/
---
## PageSetup.Gutter property

Ottiene o imposta la quantità di spazio aggiuntivo aggiunto al margine per la rilegatura del documento.

```csharp
public double Gutter { get; set; }
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

// Un margine aggiunge spazi bianchi al margine sinistro o destro della pagina,
// che compensa la piegatura centrale delle pagine di un libro che invade il layout della pagina.
PageSetup pageSetup = doc.Sections[0].PageSetup;

// Determina quanto spazio hanno le nostre pagine per il testo all'interno dei margini e poi aggiungi un importo per riempire un margine.
Assert.AreEqual(470.30d, pageSetup.PageWidth - pageSetup.LeftMargin - pageSetup.RightMargin, 0.01d);

pageSetup.Gutter = 100.0d;

// Imposta la proprietà "RtlGutter" su "true" per posizionare il margine interno in una posizione più adatta per il testo da destra a sinistra.
pageSetup.RtlGutter = true;

// Imposta la proprietà "MultiplePages" su "MultiplePagesType.MirrorMargins" per alternare
// la posizione del lato sinistro/destro dei margini di ogni pagina.
pageSetup.MultiplePages = MultiplePagesType.MirrorMargins;

doc.Save(ArtifactsDir + "PageSetup.Gutter.docx");
```

### Guarda anche

* class [PageSetup](../)
* spazio dei nomi [Aspose.Words](../../pagesetup/)
* assemblea [Aspose.Words](../../../)


