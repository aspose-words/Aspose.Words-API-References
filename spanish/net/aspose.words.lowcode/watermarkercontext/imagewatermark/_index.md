---
title: WatermarkerContext.ImageWatermark
linktitle: ImageWatermark
articleTitle: ImageWatermark
second_title: Aspose.Words para .NET
description: Descubra cómo mejorar sus imágenes con la propiedad ImageWatermark de WatermarkerContext, que le permite agregar imágenes de marca de agua personalizadas sin esfuerzo.
type: docs
weight: 20
url: /es/net/aspose.words.lowcode/watermarkercontext/imagewatermark/
---
## WatermarkerContext.ImageWatermark property

Bytes de imagen que se utilizarán como marca de agua.

```csharp
public byte[] ImageWatermark { get; set; }
```

## Observaciones

Si ambos`ImageWatermark` y[`TextWatermark`](../textwatermark/) Se especifican, la marca de agua de texto anula la marca de agua de imagen.

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

* class [WatermarkerContext](../)
* espacio de nombres [Aspose.Words.LowCode](../../../aspose.words.lowcode/)
* asamblea [Aspose.Words](../../../)
