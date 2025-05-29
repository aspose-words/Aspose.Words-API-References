---
title: WatermarkType Enum
linktitle: WatermarkType
articleTitle: WatermarkType
second_title: Aspose.Words para .NET
description: Descubra la enumeración Aspose.Words.WatermarkType para personalizar fácilmente las marcas de agua en sus documentos. ¡Mejore sus proyectos con opciones versátiles de marcas de agua!
type: docs
weight: 7540
url: /es/net/aspose.words/watermarktype/
---
## WatermarkType enumeration

Especifica el tipo de marca de agua.

```csharp
public enum WatermarkType
```

### Valores

| Nombre | Valor | Descripción |
| --- | --- | --- |
| Text | `0` | Indica que el texto se utilizará como marca de agua. |
| Image | `1` | Indica que la imagen se utilizará como marca de agua. |
| None | `2` | Indica que no hay marca de agua establecida. |

## Ejemplos

Muestra cómo crear una marca de agua de texto.

```csharp
Document doc = new Document();

//Agrega una marca de agua de texto simple.
doc.Watermark.SetText("Aspose Watermark");

// Si deseamos editar el formato del texto usándolo como marca de agua,
// Podemos hacerlo pasando un objeto TextWatermarkOptions al crear la marca de agua.
TextWatermarkOptions textWatermarkOptions = new TextWatermarkOptions();
textWatermarkOptions.FontFamily = "Arial";
textWatermarkOptions.FontSize = 36;
textWatermarkOptions.Color = Color.Black;
textWatermarkOptions.Layout = WatermarkLayout.Diagonal;
textWatermarkOptions.IsSemitrasparent = false;

doc.Watermark.SetText("Aspose Watermark", textWatermarkOptions);

doc.Save(ArtifactsDir + "Document.TextWatermark.docx");

//Podemos eliminar una marca de agua de un documento como este.
if (doc.Watermark.Type == WatermarkType.Text)
    doc.Watermark.Remove();
```

### Ver también

* espacio de nombres [Aspose.Words](../../aspose.words/)
* asamblea [Aspose.Words](../../)
