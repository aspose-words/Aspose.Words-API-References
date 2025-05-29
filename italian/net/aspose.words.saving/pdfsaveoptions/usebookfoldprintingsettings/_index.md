---
title: PdfSaveOptions.UseBookFoldPrintingSettings
linktitle: UseBookFoldPrintingSettings
articleTitle: UseBookFoldPrintingSettings
second_title: Aspose.Words per .NET
description: Scopri la proprietà UseBookFoldPrintingSettings di PdfSaveOptions per salvare facilmente i documenti in un layout di opuscolo per una maggiore efficienza di stampa.
type: docs
weight: 320
url: /it/net/aspose.words.saving/pdfsaveoptions/usebookfoldprintingsettings/
---
## PdfSaveOptions.UseBookFoldPrintingSettings property

Ottiene o imposta un valore booleano che indica se il documento deve essere salvato utilizzando un layout di stampa opuscolo, se specificato tramite[`MultiplePages`](../../../aspose.words/pagesetup/multiplepages/) .

```csharp
public bool UseBookFoldPrintingSettings { get; set; }
```

## Osservazioni

Se questa opzione è specificata,[`PageSet`](../../fixedpagesaveoptions/pageset/) viene ignorato durante il salvataggio. Questo comportamento corrisponde a MS Word. Se le impostazioni di stampa con piega a libro non sono specificate nell'impostazione della pagina, questa opzione non avrà effetto.

## Esempi

Mostra come salvare un documento in formato PDF sotto forma di piega a libro.

```csharp
Document doc = new Document(MyDir + "Paragraphs.docx");

// Creiamo un oggetto "PdfSaveOptions" che possiamo passare al metodo "Save" del documento
// per modificare il modo in cui quel metodo converte il documento in .PDF.
PdfSaveOptions options = new PdfSaveOptions();

// Imposta la proprietà "UseBookFoldPrintingSettings" su "true" per organizzare il contenuto
// nel PDF di output in un modo che ci aiuti a utilizzarlo per creare un opuscolo.
// Impostare la proprietà "UseBookFoldPrintingSettings" su "false" per eseguire il rendering del PDF normalmente.
options.UseBookFoldPrintingSettings = renderTextAsBookfold;

// Se stiamo rendendo il documento come un opuscolo, dobbiamo impostare "MultiplePages"
// proprietà degli oggetti di impostazione pagina di tutte le sezioni su "MultiplePagesType.BookFoldPrinting".
if (renderTextAsBookfold)
    foreach (Section s in doc.Sections)
    {
        s.PageSetup.MultiplePages = MultiplePagesType.BookFoldPrinting;
    }

// Una volta stampato questo documento su entrambi i lati delle pagine, possiamo piegare tutte le pagine a metà contemporaneamente,
// e i contenuti si allineeranno in modo da creare un opuscolo.
doc.Save(ArtifactsDir + "PdfSaveOptions.SaveAsPdfBookFold.pdf", options);
```

### Guarda anche

* class [PdfSaveOptions](../)
* spazio dei nomi [Aspose.Words.Saving](../../../aspose.words.saving/)
* assemblea [Aspose.Words](../../../)
