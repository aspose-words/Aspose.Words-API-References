---
title: DownsampleOptions Class
linktitle: DownsampleOptions
articleTitle: DownsampleOptions
second_title: Aspose.Words per .NET
description: Scopri la classe Aspose.Words.Saving.DownsampleOptions per personalizzare facilmente il downsampling delle immagini per ottimizzare la qualità e le prestazioni dei documenti.
type: docs
weight: 5720
url: /it/net/aspose.words.saving/downsampleoptions/
---
## DownsampleOptions class

Consente di specificare le opzioni di downsample.

Per saperne di più, visita il[Salva un documento](https://docs.aspose.com/words/net/save-a-document/) articolo di documentazione.

```csharp
public class DownsampleOptions
```

## Costruttori

| Nome | Descrizione |
| --- | --- |
| [DownsampleOptions](downsampleoptions/)() | Default_Costruttore |

## Proprietà

| Nome | Descrizione |
| --- | --- |
| [DownsampleImages](../../aspose.words.saving/downsampleoptions/downsampleimages/) { get; set; } | Specifica se le immagini devono essere sottocampionate. |
| [Resolution](../../aspose.words.saving/downsampleoptions/resolution/) { get; set; } | Specifica la risoluzione in pixel per pollice a cui le immagini devono essere sottocampionate. |
| [ResolutionThreshold](../../aspose.words.saving/downsampleoptions/resolutionthreshold/) { get; set; } | Specifica la risoluzione di soglia in pixel per pollice. Se la risoluzione di un'immagine nel documento è inferiore al valore di soglia, l'algoritmo di downsampling non verrà applicato. Un valore pari a 0 indica che il controllo della soglia non viene utilizzato e tutte le immagini di cui è possibile ridurre le dimensioni vengono sottoposte a downsampling. |

## Esempi

Mostra come modificare la risoluzione delle immagini nel documento PDF.

```csharp
Document doc = new Document(MyDir + "Images.docx");

// Creiamo un oggetto "PdfSaveOptions" che possiamo passare al metodo "Save" del documento
// per modificare il modo in cui quel metodo converte il documento in .PDF.
PdfSaveOptions options = new PdfSaveOptions();

// Per impostazione predefinita, Aspose.Words riduce a 220 ppi tutte le immagini in un documento che salviamo in PDF.
Assert.True(options.DownsampleOptions.DownsampleImages);
Assert.AreEqual(220, options.DownsampleOptions.Resolution);
Assert.AreEqual(0, options.DownsampleOptions.ResolutionThreshold);

doc.Save(ArtifactsDir + "PdfSaveOptions.DownsampleOptions.Default.pdf", options);

// Impostare la proprietà "Risoluzione" su "36" per ridurre il campionamento di tutte le immagini a 36 ppi.
options.DownsampleOptions.Resolution = 36;

// Imposta la proprietà "ResolutionThreshold" per applicare il downsampling solo a
// immagini con una risoluzione superiore a 128 ppi.
options.DownsampleOptions.ResolutionThreshold = 128;

// In questa fase, solo le prime due immagini del documento verranno sottocampionate.
doc.Save(ArtifactsDir + "PdfSaveOptions.DownsampleOptions.LowerResolution.pdf", options);
```

### Guarda anche

* spazio dei nomi [Aspose.Words.Saving](../../aspose.words.saving/)
* assemblea [Aspose.Words](../../)
