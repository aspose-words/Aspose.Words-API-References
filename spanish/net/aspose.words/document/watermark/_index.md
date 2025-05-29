---
title: Document.Watermark
linktitle: Watermark
articleTitle: Watermark
second_title: Aspose.Words para .NET
description: Proteja sus documentos con nuestra función de marca de agua personalizable. ¡Mejore la protección y garantice la autenticidad sin esfuerzo!
type: docs
weight: 500
url: /es/net/aspose.words/document/watermark/
---
## Document.Watermark property

Proporciona acceso a la marca de agua del documento.

```csharp
public Watermark Watermark { get; }
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

* class [Watermark](../../watermark/)
* class [Document](../)
* espacio de nombres [Aspose.Words](../../../aspose.words/)
* asamblea [Aspose.Words](../../../)
