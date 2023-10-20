---
title: DownsampleOptions.Resolution
linktitle: Resolution
articleTitle: Resolution
second_title: Aspose.Words per .NET
description: DownsampleOptions Resolution proprietà. Specifica la risoluzione in pixel per pollice a cui eseguire il downsampling delle immagini in C#.
type: docs
weight: 30
url: /it/net/aspose.words.saving/downsampleoptions/resolution/
---
## DownsampleOptions.Resolution property

Specifica la risoluzione in pixel per pollice a cui eseguire il downsampling delle immagini.

```csharp
public int Resolution { get; set; }
```

## Osservazioni

Il valore predefinito è 220 ppi.

## Esempi

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

* class [DownsampleOptions](../)
* spazio dei nomi [Aspose.Words.Saving](../../../aspose.words.saving/)
* assemblea [Aspose.Words](../../../)
