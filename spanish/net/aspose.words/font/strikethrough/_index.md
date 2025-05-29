---
title: Font.StrikeThrough
linktitle: StrikeThrough
articleTitle: StrikeThrough
second_title: Aspose.Words para .NET
description: Descubra la propiedad Tachado de fuente. Tache fácilmente el texto para lograr un énfasis visual claro en sus diseños. ¡Mejore la legibilidad hoy mismo!
type: docs
weight: 400
url: /es/net/aspose.words/font/strikethrough/
---
## Font.StrikeThrough property

Verdadero si la fuente está formateada como texto tachado.

```csharp
public bool StrikeThrough { get; set; }
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
