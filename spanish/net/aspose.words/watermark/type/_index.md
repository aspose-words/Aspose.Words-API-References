---
title: Watermark.Type
linktitle: Type
articleTitle: Type
second_title: Aspose.Words para .NET
description: Descubre la propiedad Tipo de marca de agua para mejorar tu diseño con marcas de agua personalizables para tu marca y protección. ¡Mejora tus imágenes hoy mismo!
type: docs
weight: 10
url: /es/net/aspose.words/watermark/type/
---
## Watermark.Type property

Obtiene el tipo de marca de agua.

```csharp
public WatermarkType Type { get; }
```

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

* enum [WatermarkType](../../watermarktype/)
* class [Watermark](../)
* espacio de nombres [Aspose.Words](../../../aspose.words/)
* asamblea [Aspose.Words](../../../)
