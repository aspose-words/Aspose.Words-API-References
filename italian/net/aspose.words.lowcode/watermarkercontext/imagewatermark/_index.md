---
title: WatermarkerContext.ImageWatermark
linktitle: ImageWatermark
articleTitle: ImageWatermark
second_title: Aspose.Words per .NET
description: Scopri come migliorare le tue immagini con la proprietà ImageWatermark di WatermarkContext, che ti consente di aggiungere immagini con filigrana personalizzate senza sforzo.
type: docs
weight: 20
url: /it/net/aspose.words.lowcode/watermarkercontext/imagewatermark/
---
## WatermarkerContext.ImageWatermark property

Byte dell'immagine da utilizzare come filigrana.

```csharp
public byte[] ImageWatermark { get; set; }
```

## Osservazioni

Se entrambi`ImageWatermark` E[`TextWatermark`](../textwatermark/) se specificati, la filigrana del testo sovrascrive la filigrana dell'immagine.

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

* class [WatermarkerContext](../)
* spazio dei nomi [Aspose.Words.LowCode](../../../aspose.words.lowcode/)
* assemblea [Aspose.Words](../../../)
