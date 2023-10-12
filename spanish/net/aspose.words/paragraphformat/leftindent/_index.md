---
title: ParagraphFormat.LeftIndent
second_title: Referencia de API de Aspose.Words para .NET
description: ParagraphFormat propiedad. Obtiene o establece el valor en puntos que representa la sangría izquierda del párrafo.
type: docs
weight: 180
url: /es/net/aspose.words/paragraphformat/leftindent/
---
## ParagraphFormat.LeftIndent property

Obtiene o establece el valor (en puntos) que representa la sangría izquierda del párrafo.

```csharp
public double LeftIndent { get; set; }
```

### Ejemplos

Muestra cómo configurar el formato de párrafo para crear texto descentrado.

```csharp
Document doc = new Document();
DocumentBuilder builder = new DocumentBuilder(doc);

// Centrar todo el texto que escribe el creador de documentos y configurar sangrías.
// La siguiente configuración de sangría creará un cuerpo de texto que se ubicará asimétricamente en la página.
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
* espacio de nombres [Aspose.Words](../../paragraphformat/)
* asamblea [Aspose.Words](../../../)


