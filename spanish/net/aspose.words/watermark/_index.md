---
title: Watermark Class
linktitle: Watermark
articleTitle: Watermark
second_title: Aspose.Words para .NET
description: Descubra la clase Aspose.Words.Watermark para agregar y personalizar fácilmente marcas de agua en sus documentos, mejorando el profesionalismo y la marca.
type: docs
weight: 7520
url: /es/net/aspose.words/watermark/
---
## Watermark class

Representa la clase para trabajar con marca de agua del documento.

Para obtener más información, visite el[Trabajar con marca de agua](https://docs.aspose.com/words/net/working-with-watermark/) Artículo de documentación.

```csharp
public sealed class Watermark
```

## Propiedades

| Nombre | Descripción |
| --- | --- |
| [Type](../../aspose.words/watermark/type/) { get; } | Obtiene el tipo de marca de agua. |

## Métodos

| Nombre | Descripción |
| --- | --- |
| [Remove](../../aspose.words/watermark/remove/)() | Elimina la marca de agua. |
| [SetImage](../../aspose.words/watermark/setimage/#setimage)(*Image*) | Agrega una marca de agua de imagen al documento. |
| [SetImage](../../aspose.words/watermark/setimage/#setimage_1)(*Image, [ImageWatermarkOptions](../imagewatermarkoptions/)*) | Agrega una marca de agua de imagen al documento. |
| [SetImage](../../aspose.words/watermark/setimage/#setimage_2)(*Stream, [ImageWatermarkOptions](../imagewatermarkoptions/)*) | Agrega una marca de agua de imagen al documento. |
| [SetImage](../../aspose.words/watermark/setimage/#setimage_3)(*string, [ImageWatermarkOptions](../imagewatermarkoptions/)*) | Agrega una marca de agua de imagen al documento. |
| [SetText](../../aspose.words/watermark/settext/#settext)(*string*) | Agrega una marca de agua de texto al documento. |
| [SetText](../../aspose.words/watermark/settext/#settext_1)(*string, [TextWatermarkOptions](../textwatermarkoptions/)*) | Agrega una marca de agua de texto al documento. |

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
