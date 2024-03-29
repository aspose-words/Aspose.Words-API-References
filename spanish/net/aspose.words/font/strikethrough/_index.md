---
title: Font.StrikeThrough
linktitle: StrikeThrough
articleTitle: StrikeThrough
second_title: Aspose.Words para .NET
description: Font StrikeThrough propiedad. Verdadero si la fuente tiene el formato de texto tachado en C#.
type: docs
weight: 390
url: /es/net/aspose.words/font/strikethrough/
---
## Font.StrikeThrough property

Verdadero si la fuente tiene el formato de texto tachado.

```csharp
public bool StrikeThrough { get; set; }
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
