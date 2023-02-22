---
title: Enum WatermarkType
second_title: Referencia de API de Aspose.Words para .NET
description: Aspose.Words.WatermarkType enumeración. Especifica el tipo de marca de agua.
type: docs
weight: 6380
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
| None | `2` | Indica que la marca de agua no está establecida. |

### Ejemplos

Muestra cómo crear una marca de agua de texto.

```csharp
Document doc = new Document();

// Agregue una marca de agua de texto sin formato.
doc.Watermark.SetText("Aspose Watermark");

// Si deseamos editar el formato del texto usándolo como marca de agua,
// podemos hacerlo pasando un objeto TextWatermarkOptions al crear la marca de agua.
TextWatermarkOptions textWatermarkOptions = new TextWatermarkOptions();
textWatermarkOptions.FontFamily = "Arial";
textWatermarkOptions.FontSize = 36;
textWatermarkOptions.Color = Color.Black;
textWatermarkOptions.Layout = WatermarkLayout.Diagonal;
textWatermarkOptions.IsSemitrasparent = false;

doc.Watermark.SetText("Aspose Watermark", textWatermarkOptions);

doc.Save(ArtifactsDir + "Document.TextWatermark.docx");

// Podemos eliminar una marca de agua de un documento como este.
if (doc.Watermark.Type == WatermarkType.Text)
    doc.Watermark.Remove();
```

### Ver también

* espacio de nombres [Aspose.Words](../../aspose.words/)
* asamblea [Aspose.Words](../../)


