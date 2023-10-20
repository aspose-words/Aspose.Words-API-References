---
title: PageSetup.RtlGutter
linktitle: RtlGutter
articleTitle: RtlGutter
second_title: Aspose.Words per .NET
description: PageSetup RtlGutter proprietà. Ottiene o imposta se Microsoft Word utilizza i margini interni per la sezione in base a una lingua da destra a sinistra o da sinistra a destra in C#.
type: docs
weight: 380
url: /it/net/aspose.words/pagesetup/rtlgutter/
---
## PageSetup.RtlGutter property

Ottiene o imposta se Microsoft Word utilizza i margini interni per la sezione in base a una lingua da destra a sinistra o da sinistra a destra.

```csharp
public bool RtlGutter { get; set; }
```

## Esempi

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
* spazio dei nomi [Aspose.Words](../../../aspose.words/)
* assemblea [Aspose.Words](../../../)
