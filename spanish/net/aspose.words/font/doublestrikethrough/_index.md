---
title: Font.DoubleStrikeThrough
linktitle: DoubleStrikeThrough
articleTitle: DoubleStrikeThrough
second_title: Aspose.Words para .NET
description: Font DoubleStrikeThrough propiedad. Verdadero si la fuente tiene el formato de texto tachado doble en C#.
type: docs
weight: 90
url: /es/net/aspose.words/font/doublestrikethrough/
---
## Font.DoubleStrikeThrough property

Verdadero si la fuente tiene el formato de texto tachado doble.

```csharp
public bool DoubleStrikeThrough { get; set; }
```

## Ejemplos

Muestra cómo agregar una línea tachada al texto.

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
