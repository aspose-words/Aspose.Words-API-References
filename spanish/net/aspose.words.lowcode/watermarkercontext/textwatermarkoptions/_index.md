---
title: WatermarkerContext.TextWatermarkOptions
linktitle: TextWatermarkOptions
articleTitle: TextWatermarkOptions
second_title: Aspose.Words para .NET
description: Descubra opciones personalizables para marcas de agua de imágenes con la propiedad TextWatermarkOptions de WatermarkerContext para mejorar sus imágenes y proteger su contenido.
type: docs
weight: 50
url: /es/net/aspose.words.lowcode/watermarkercontext/textwatermarkoptions/
---
## WatermarkerContext.TextWatermarkOptions property

Opciones para la marca de agua de la imagen.

```csharp
public TextWatermarkOptions TextWatermarkOptions { get; }
```

## Ejemplos

Muestra cómo insertar texto de marca de agua en el documento usando el contexto.

```csharp
string doc = MyDir + "Big document.docx";
string watermarkText = "This is a watermark";

WatermarkerContext watermarkerContext = new WatermarkerContext();
watermarkerContext.TextWatermark = watermarkText;

watermarkerContext.TextWatermarkOptions.Color = Color.Red;

Watermarker.Create(watermarkerContext)
    .From(doc)
    .To(ArtifactsDir + "LowCode.WatermarkContextText.docx")
    .Execute();
```

Muestra cómo insertar texto de marca de agua en el documento desde la secuencia usando el contexto.

```csharp
string watermarkText = "This is a watermark";

using (FileStream streamIn = new FileStream(MyDir + "Document.docx", FileMode.Open, FileAccess.Read))
{
    WatermarkerContext watermarkerContext = new WatermarkerContext();
    watermarkerContext.TextWatermark = watermarkText;

    watermarkerContext.TextWatermarkOptions.Color = Color.Red;

    using (FileStream streamOut = new FileStream(ArtifactsDir + "LowCode.WatermarkContextTextStream.docx", FileMode.Create, FileAccess.ReadWrite))
        Watermarker.Create(watermarkerContext)
            .From(streamIn)
            .To(streamOut, SaveFormat.Docx)
            .Execute();
}
```

### Ver también

* class [TextWatermarkOptions](../../../aspose.words/textwatermarkoptions/)
* class [WatermarkerContext](../)
* espacio de nombres [Aspose.Words.LowCode](../../../aspose.words.lowcode/)
* asamblea [Aspose.Words](../../../)
