---
title: WatermarkerContext.ImageWatermarkOptions
linktitle: ImageWatermarkOptions
articleTitle: ImageWatermarkOptions
second_title: Aspose.Words para .NET
description: Descubra las opciones de marca de agua de texto personalizables con WatermarkerContext para mejorar sus imágenes y proteger la identidad de su marca de manera efectiva.
type: docs
weight: 30
url: /es/net/aspose.words.lowcode/watermarkercontext/imagewatermarkoptions/
---
## WatermarkerContext.ImageWatermarkOptions property

Opciones para la marca de agua de texto.

```csharp
public ImageWatermarkOptions ImageWatermarkOptions { get; }
```

## Ejemplos

Muestra cómo insertar una imagen de marca de agua en el documento usando el contexto.

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

Muestra cómo insertar una imagen de marca de agua en el documento desde una secuencia usando el contexto.

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

### Ver también

* class [ImageWatermarkOptions](../../../aspose.words/imagewatermarkoptions/)
* class [WatermarkerContext](../)
* espacio de nombres [Aspose.Words.LowCode](../../../aspose.words.lowcode/)
* asamblea [Aspose.Words](../../../)
