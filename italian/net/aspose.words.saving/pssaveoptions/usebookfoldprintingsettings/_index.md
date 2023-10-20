---
title: PsSaveOptions.UseBookFoldPrintingSettings
linktitle: UseBookFoldPrintingSettings
articleTitle: UseBookFoldPrintingSettings
second_title: Aspose.Words per .NET
description: PsSaveOptions UseBookFoldPrintingSettings proprietà. Ottiene o imposta un valore booleano che indica se il documento deve essere salvato utilizzando un layout di stampa booklet se specificato tramiteMultiplePages  in C#.
type: docs
weight: 30
url: /it/net/aspose.words.saving/pssaveoptions/usebookfoldprintingsettings/
---
## PsSaveOptions.UseBookFoldPrintingSettings property

Ottiene o imposta un valore booleano che indica se il documento deve essere salvato utilizzando un layout di stampa booklet, se specificato tramite[`MultiplePages`](../../../aspose.words/pagesetup/multiplepages/) .

```csharp
public bool UseBookFoldPrintingSettings { get; set; }
```

## Osservazioni

Se questa opzione è specificata,[`PageSet`](../../fixedpagesaveoptions/pageset/) viene ignorato durante il salvataggio. Questo comportamento corrisponde a MS Word. Se le impostazioni di stampa della piegatura del libro non sono specificate nell'impostazione della pagina, questa opzione non avrà alcun effetto.

## Esempi

Mostra come salvare un documento nel formato Postscript sotto forma di piegatura di un libro.

```csharp
Document doc = new Document(MyDir + "Paragraphs.docx");

// Crea un oggetto "PsSaveOptions" che possiamo passare al metodo "Save" del documento
// per modificare il modo in cui il metodo converte il documento in PostScript.
// Imposta la proprietà "UseBookFoldPrintingSettings" su "true" per organizzare i contenuti
// nel documento Postscript di output in modo da aiutarci a ricavarne un opuscolo.
// Imposta la proprietà "UseBookFoldPrintingSettings" su "false" per salvare normalmente il documento.
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

// Una volta stampato questo documento su entrambi i lati delle pagine, possiamo piegare tutte le pagine al centro contemporaneamente,
// e i contenuti si allineeranno in modo da creare un opuscolo.
doc.Save(ArtifactsDir + "PsSaveOptions.UseBookFoldPrintingSettings.ps", saveOptions);
```

### Guarda anche

* class [PsSaveOptions](../)
* spazio dei nomi [Aspose.Words.Saving](../../../aspose.words.saving/)
* assemblea [Aspose.Words](../../../)
