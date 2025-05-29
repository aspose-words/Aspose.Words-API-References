---
title: DocumentBuilder.Underline
linktitle: Underline
articleTitle: Underline
second_title: Aspose.Words para .NET
description: Descubra la propiedad Subrayado de DocumentBuilder para personalizar fácilmente los estilos de fuente. Mejore sus documentos con versátiles opciones de subrayado para una apariencia profesional.
type: docs
weight: 190
url: /es/net/aspose.words/documentbuilder/underline/
---
## DocumentBuilder.Underline property

Obtiene/establece el tipo de subrayado para la fuente actual.

```csharp
public Underline Underline { get; set; }
```

## Ejemplos

Muestra cómo formatear el texto insertado por un generador de documentos.

```csharp
Document doc = new Document();
DocumentBuilder builder = new DocumentBuilder(doc);

builder.Underline = Underline.Dash;
builder.Font.Color = Color.Blue;
builder.Font.Size = 32;

// El constructor aplica formato a su párrafo actual y a cualquier texto nuevo que agregue posteriormente.
builder.Writeln("Large, blue, and underlined text.");

doc.Save(ArtifactsDir + "DocumentBuilder.InsertUnderline.docx");
```

### Ver también

* enum [Underline](../../underline/)
* class [DocumentBuilder](../)
* espacio de nombres [Aspose.Words](../../../aspose.words/)
* asamblea [Aspose.Words](../../../)
