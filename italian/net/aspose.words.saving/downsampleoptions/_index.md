---
title: Class DownsampleOptions
second_title: Aspose.Words per .NET API Reference
description: Aspose.Words.Saving.DownsampleOptions classe. Permette di specificare le opzioni di downsample.
type: docs
weight: 4970
url: /it/net/aspose.words.saving/downsampleoptions/
---
## DownsampleOptions class

Permette di specificare le opzioni di downsample.

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
| [Resolution](../../aspose.words.saving/downsampleoptions/resolution/) { get; set; } | Specifica la risoluzione in pixel per pollice a cui eseguire il downsampling delle immagini. |
| [ResolutionThreshold](../../aspose.words.saving/downsampleoptions/resolutionthreshold/) { get; set; } | Specifica la risoluzione soglia in pixel per pollice. Se la risoluzione di un'immagine nel documento è inferiore al valore soglia, l'algoritmo di downsampling non verrà applicato. Un valore pari a 0 significa che il controllo soglia non viene utilizzato e tutte le immagini le dimensioni possono essere ridotte vengono sottocampionate. |

### Esempi

Mostra come modificare la risoluzione delle immagini nel documento PDF.

```csharp
Document doc = new Document(MyDir + "Images.docx");

// Crea un oggetto "PdfSaveOptions" che possiamo passare al metodo "Save" del documento
// per modificare il modo in cui il metodo converte il documento in .PDF.
PdfSaveOptions options = new PdfSaveOptions();

// Per impostazione predefinita, Aspose.Words esegue il downsampling di tutte le immagini in un documento che salviamo in PDF a 220 ppi.
Assert.True(options.DownsampleOptions.DownsampleImages);
Assert.AreEqual(220, options.DownsampleOptions.Resolution);
Assert.AreEqual(0, options.DownsampleOptions.ResolutionThreshold);

doc.Save(ArtifactsDir + "PdfSaveOptions.DownsampleOptions.Default.pdf", options);

// Imposta la proprietà "Risoluzione" su "36" per eseguire il downsampling di tutte le immagini a 36 ppi.
options.DownsampleOptions.Resolution = 36;

// Imposta la proprietà "ResolutionThreshold" per applicare solo il downsampling
// immagini con una risoluzione superiore a 128 ppi.
options.DownsampleOptions.ResolutionThreshold = 128;

// In questa fase verrà eseguito il downsampling solo delle prime due immagini del documento.
doc.Save(ArtifactsDir + "PdfSaveOptions.DownsampleOptions.LowerResolution.pdf", options);
```

### Guarda anche

* spazio dei nomi [Aspose.Words.Saving](../../aspose.words.saving/)
* assemblea [Aspose.Words](../../)


