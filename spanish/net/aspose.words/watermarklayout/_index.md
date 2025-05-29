---
title: WatermarkLayout Enum
linktitle: WatermarkLayout
articleTitle: WatermarkLayout
second_title: Aspose.Words para .NET
description: Descubra la enumeración Aspose.Words.WatermarkLayout para optimizar la posición de la marca de agua. Mejore el diseño de sus documentos con un control preciso del diseño y la personalización.
type: docs
weight: 7530
url: /es/net/aspose.words/watermarklayout/
---
## WatermarkLayout enumeration

Define el diseño de la marca de agua en relación con el centro de la marca de agua.

```csharp
public enum WatermarkLayout
```

### Valores

| Nombre | Valor | Descripción |
| --- | --- | --- |
| Horizontal | `0` | Diseño de marca de agua horizontal. Corresponde a 0 grados de rotación. |
| Diagonal | `315` | Diseño de marca de agua diagonal. Corresponde a 315 grados de rotación. |

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
