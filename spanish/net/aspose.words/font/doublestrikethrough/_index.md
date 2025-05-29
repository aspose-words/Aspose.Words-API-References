---
title: Font.DoubleStrikeThrough
linktitle: DoubleStrikeThrough
articleTitle: DoubleStrikeThrough
second_title: Aspose.Words para .NET
description: Descubra la propiedad Font DoubleStrikeThrough. Formatee fácilmente el texto con doble tachado para mejorar la claridad y el estilo de sus documentos.
type: docs
weight: 90
url: /es/net/aspose.words/font/doublestrikethrough/
---
## Font.DoubleStrikeThrough property

Verdadero si la fuente está formateada como texto tachado doble.

```csharp
public bool DoubleStrikeThrough { get; set; }
```

## Ejemplos

Muestra cómo agregar un tachado de línea al texto.

```csharp
Document doc = new Document();
Paragraph para = (Paragraph)doc.GetChild(NodeType.Paragraph, 0, true);

Run run = new Run(doc, "Text with a single-line strikethrough.");
run.Font.StrikeThrough = true;
para.AppendChild(run);

para = (Paragraph)para.ParentNode.AppendChild(new Paragraph(doc));

run = new Run(doc, "Text with a double-line strikethrough.");
run.Font.DoubleStrikeThrough = true;
para.AppendChild(run);

doc.Save(ArtifactsDir + "Font.StrikeThrough.docx");
```

### Ver también

* class [Font](../)
* espacio de nombres [Aspose.Words](../../../aspose.words/)
* asamblea [Aspose.Words](../../../)
