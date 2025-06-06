---
title: TextWatermarkOptions.Color
linktitle: Color
articleTitle: Color
second_title: Aspose.Words para .NET
description: Personaliza tus TextWatermarkOptions con la propiedad Color para mejorar la visibilidad. Define tu color de fuente preferido para un toque personal. El valor predeterminado es Plata.
type: docs
weight: 20
url: /es/net/aspose.words/textwatermarkoptions/color/
---
## TextWatermarkOptions.Color property

Obtiene o establece el color de la fuente. El valor predeterminado esSilver .

```csharp
public Color Color { get; set; }
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

* class [TextWatermarkOptions](../)
* espacio de nombres [Aspose.Words](../../../aspose.words/)
* asamblea [Aspose.Words](../../../)
