---
title: ParagraphFormat.RightIndent
linktitle: RightIndent
articleTitle: RightIndent
second_title: Aspose.Words para .NET
description: Descubre cómo ajustar fácilmente la sangría derecha de tus párrafos con la propiedad ParagraphFormat RightIndent. ¡Mejora el formato de tus documentos hoy mismo!
type: docs
weight: 280
url: /es/net/aspose.words/paragraphformat/rightindent/
---
## ParagraphFormat.RightIndent property

Obtiene o establece el valor (en puntos) que representa la sangría derecha del párrafo.

```csharp
public double RightIndent { get; set; }
```

## Ejemplos

Muestra cómo configurar el formato de párrafo para crear texto descentrado.

```csharp
Document doc = new Document();
DocumentBuilder builder = new DocumentBuilder(doc);

// Centra todo el texto que escribe el generador de documentos y configura sangrías.
// La configuración de sangría a continuación creará un cuerpo de texto que se ubicará asimétricamente en la página.
// El "centro" al que alineamos el texto será la mitad del cuerpo del texto, no la mitad de la página.
ParagraphFormat paragraphFormat = builder.ParagraphFormat;
paragraphFormat.Alignment = ParagraphAlignment.Center;
paragraphFormat.LeftIndent = 100;
paragraphFormat.RightIndent = 50;
paragraphFormat.SpaceAfter = 25;

builder.Writeln(
    "This paragraph demonstrates how left and right indentation affects word wrapping.");
builder.Writeln(
    "The space between the above paragraph and this one depends on the DocumentBuilder's paragraph format.");

doc.Save(ArtifactsDir + "DocumentBuilder.SetParagraphFormatting.docx");
```

### Ver también

* class [ParagraphFormat](../)
* espacio de nombres [Aspose.Words](../../../aspose.words/)
* asamblea [Aspose.Words](../../../)
