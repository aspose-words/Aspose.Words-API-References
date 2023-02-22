---
title: DownsampleOptions.Resolution
second_title: Aspose.Words per .NET API Reference
description: DownsampleOptions proprietà. Specifica la risoluzione in pixel per pollice a cui le immagini devono essere sottocampionate.
type: docs
weight: 30
url: /it/net/aspose.words.saving/downsampleoptions/resolution/
---
## DownsampleOptions.Resolution property

Specifica la risoluzione in pixel per pollice a cui le immagini devono essere sottocampionate.

```csharp
public int Resolution { get; set; }
```

### Osservazioni

Il valore predefinito è 220 ppi.

### Esempi

Mostra come modificare la risoluzione delle immagini nel documento PDF.

```csharp
Document doc = new Document(MyDir + "Images.docx");

// Crea un oggetto "PdfSaveOptions" che possiamo passare al metodo "Save" del documento
// per modificare il modo in cui quel metodo converte il documento in .PDF.
PdfSaveOptions options = new PdfSaveOptions();

// Per impostazione predefinita, Aspose.Words esegue il downsampling di tutte le immagini in un documento che salviamo in PDF a 220 ppi.
Assert.True(options.DownsampleOptions.DownsampleImages);
Assert.AreEqual(220, options.DownsampleOptions.Resolution);
Assert.AreEqual(0, options.DownsampleOptions.ResolutionThreshold);

doc.Save(ArtifactsDir + "PdfSaveOptions.DownsampleOptions.Default.pdf", options);

// Imposta la proprietà "Risoluzione" su "36" per eseguire il downsamp di tutte le immagini a 36 ppi.
options.DownsampleOptions.Resolution = 36;

// Imposta la proprietà "ResolutionThreshold" per applicare solo il downsampling
// immagini con una risoluzione superiore a 128 ppi.
options.DownsampleOptions.ResolutionThreshold = 128;

// Solo le prime due immagini del documento verranno sottocampionate in questa fase.
doc.Save(ArtifactsDir + "PdfSaveOptions.DownsampleOptions.LowerResolution.pdf", options);
```

### Guarda anche

* class [DownsampleOptions](../)
* spazio dei nomi [Aspose.Words.Saving](../../downsampleoptions/)
* assemblea [Aspose.Words](../../../)


