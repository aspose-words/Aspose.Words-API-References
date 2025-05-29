---
title: WatermarkerContext.ImageWatermarkOptions
linktitle: ImageWatermarkOptions
articleTitle: ImageWatermarkOptions
second_title: Aspose.Words per .NET
description: Scopri le opzioni personalizzabili di filigrana di testo con WatermarkerContext per migliorare le tue immagini e proteggere efficacemente l'identità del tuo marchio.
type: docs
weight: 30
url: /it/net/aspose.words.lowcode/watermarkercontext/imagewatermarkoptions/
---
## WatermarkerContext.ImageWatermarkOptions property

Opzioni per la filigrana di testo.

```csharp
public ImageWatermarkOptions ImageWatermarkOptions { get; }
```

## Esempi

Mostra come inserire un'immagine di filigrana nel documento utilizzando il contesto.

```csharp
string doc = MyDir + "Document.docx";
string watermarkImage = ImageDir + "Logo.jpg";

WatermarkerContext watermarkerContext = new WatermarkerContext();
watermarkerContext.ImageWatermark = File.ReadAllBytes(watermarkImage);

watermarkerContext.ImageWatermarkOptions.Scale = 50;

Watermarker.Create(watermarkerContext)
    .From(doc)
    .To(ArtifactsDir + "LowCode.WatermarkContextImage.docx")
    .Execute();
```

Mostra come inserire un'immagine di filigrana nel documento da un flusso utilizzando il contesto.

```csharp
string watermarkImage = ImageDir + "Logo.jpg";

using (FileStream streamIn = new FileStream(MyDir + "Document.docx", FileMode.Open, FileAccess.Read))
{
    WatermarkerContext watermarkerContext = new WatermarkerContext();
    watermarkerContext.ImageWatermark = File.ReadAllBytes(watermarkImage);

    watermarkerContext.ImageWatermarkOptions.Scale = 50;

    using (FileStream streamOut = new FileStream(ArtifactsDir + "LowCode.WatermarkContextImageStream.docx", FileMode.Create, FileAccess.ReadWrite))
        Watermarker.Create(watermarkerContext)
            .From(streamIn)
            .To(streamOut, SaveFormat.Docx)
            .Execute();
}
```

### Guarda anche

* class [ImageWatermarkOptions](../../../aspose.words/imagewatermarkoptions/)
* class [WatermarkerContext](../)
* spazio dei nomi [Aspose.Words.LowCode](../../../aspose.words.lowcode/)
* assemblea [Aspose.Words](../../../)
