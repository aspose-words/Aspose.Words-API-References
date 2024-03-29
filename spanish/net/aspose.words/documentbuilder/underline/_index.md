---
title: DocumentBuilder.Underline
linktitle: Underline
articleTitle: Underline
second_title: Aspose.Words para .NET
description: DocumentBuilder Underline propiedad. Obtiene/establece el tipo de subrayado para la fuente actual en C#.
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

Muestra cómo dar formato al texto insertado por un generador de documentos.

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
