---
title: PsSaveOptions.SaveFormat
linktitle: SaveFormat
articleTitle: SaveFormat
second_title: Aspose.Words per .NET
description: Scopri la proprietà SaveFormat di PsSaveOptions per specificare facilmente il formato di salvataggio del tuo documento. Ottimizza il tuo flusso di lavoro con opzioni di salvataggio flessibili!
type: docs
weight: 20
url: /it/net/aspose.words.saving/pssaveoptions/saveformat/
---
## PsSaveOptions.SaveFormat property

Specifica il formato in cui il documento verrà salvato se viene utilizzato questo oggetto di opzioni di salvataggio. Può essere soloPs .

```csharp
public override SaveFormat SaveFormat { get; set; }
```

## Esempi

Mostra come salvare un documento nel formato Postscript sotto forma di piega a libro.

```csharp
Document doc = new Document(MyDir + "Paragraphs.docx");

// Creiamo un oggetto "PsSaveOptions" che possiamo passare al metodo "Save" del documento
// per modificare il modo in cui quel metodo converte il documento in PostScript.
// Imposta la proprietà "UseBookFoldPrintingSettings" su "true" per organizzare il contenuto
// nel documento Postscript di output in un modo che ci aiuti a trasformarlo in un opuscolo.
// Impostare la proprietà "UseBookFoldPrintingSettings" su "false" per salvare il documento normalmente.
PsSaveOptions saveOptions = new PsSaveOptions
{
    SaveFormat = SaveFormat.Ps,
    UseBookFoldPrintingSettings = renderTextAsBookFold
};

// Se stiamo rendendo il documento come un opuscolo, dobbiamo impostare "MultiplePages"
// proprietà degli oggetti di impostazione pagina di tutte le sezioni su "MultiplePagesType.BookFoldPrinting".
foreach (Section s in doc.Sections)
{
    s.PageSetup.MultiplePages = MultiplePagesType.BookFoldPrinting;
}

// Una volta stampato questo documento su entrambi i lati delle pagine, possiamo piegare tutte le pagine a metà contemporaneamente,
// e i contenuti si allineeranno in modo da creare un opuscolo.
doc.Save(ArtifactsDir + "PsSaveOptions.UseBookFoldPrintingSettings.ps", saveOptions);
```

### Guarda anche

* enum [SaveFormat](../../../aspose.words/saveformat/)
* class [PsSaveOptions](../)
* spazio dei nomi [Aspose.Words.Saving](../../../aspose.words.saving/)
* assemblea [Aspose.Words](../../../)
