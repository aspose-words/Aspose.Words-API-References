---
title: DownsampleOptions.Resolution
linktitle: Resolution
articleTitle: Resolution
second_title: Aspose.Words per .NET
description: Ottimizza la qualità dell'immagine con la proprietà Risoluzione DownsampleOptions, definendo i pixel per pollice ideali per risultati di downsampling superiori.
type: docs
weight: 30
url: /it/net/aspose.words.saving/downsampleoptions/resolution/
---
## DownsampleOptions.Resolution property

Specifica la risoluzione in pixel per pollice a cui le immagini devono essere sottocampionate.

```csharp
public int Resolution { get; set; }
```

## Osservazioni

Il valore predefinito è 220 ppi.

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

* class [DownsampleOptions](../)
* spazio dei nomi [Aspose.Words.Saving](../../../aspose.words.saving/)
* assemblea [Aspose.Words](../../../)
