---
title: WatermarkerContext Class
linktitle: WatermarkerContext
articleTitle: WatermarkerContext
second_title: Aspose.Words para .NET
description: Descubra la clase Aspose.Words.LowCode.WatermarkerContext para crear marcas de agua en sus documentos de forma fluida. Mejore sus documentos con facilidad y eficiencia.
type: docs
weight: 4450
url: /es/net/aspose.words.lowcode/watermarkercontext/
---
## WatermarkerContext class

Contexto del marcador de agua del documento.

```csharp
public class WatermarkerContext : ProcessorContext
```

## Constructores

| Nombre | Descripción |
| --- | --- |
| [WatermarkerContext](watermarkercontext/)() | Constructor predeterminado |

## Propiedades

| Nombre | Descripción |
| --- | --- |
| [FontSettings](../../aspose.words.lowcode/processorcontext/fontsettings/) { get; set; } | Configuración de fuentes utilizada por el procesador. |
| [ImageWatermark](../../aspose.words.lowcode/watermarkercontext/imagewatermark/) { get; set; } | Bytes de imagen que se utilizarán como marca de agua. |
| [ImageWatermarkOptions](../../aspose.words.lowcode/watermarkercontext/imagewatermarkoptions/) { get; } | Opciones para la marca de agua de texto. |
| [LayoutOptions](../../aspose.words.lowcode/processorcontext/layoutoptions/) { get; } | Opciones de diseño de documento utilizadas por el procesador. |
| [TextWatermark](../../aspose.words.lowcode/watermarkercontext/textwatermark/) { get; set; } | Texto que se utilizará como marca de agua. |
| [TextWatermarkOptions](../../aspose.words.lowcode/watermarkercontext/textwatermarkoptions/) { get; } | Opciones para la marca de agua de la imagen. |
| [WarningCallback](../../aspose.words.lowcode/processorcontext/warningcallback/) { get; set; } | Devolución de llamada de advertencia utilizada por el procesador. |

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

* class [ProcessorContext](../processorcontext/)
* espacio de nombres [Aspose.Words.LowCode](../../aspose.words.lowcode/)
* asamblea [Aspose.Words](../../)
