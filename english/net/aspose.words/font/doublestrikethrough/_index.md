---
title: Font.DoubleStrikeThrough
linktitle: DoubleStrikeThrough
articleTitle: DoubleStrikeThrough
second_title: Aspose.Words for .NET
description: Font DoubleStrikeThrough property. True if the font is formatted as double strikethrough text in C#.
type: docs
weight: 90
url: /net/aspose.words/font/doublestrikethrough/
---
## Font.DoubleStrikeThrough property

True if the font is formatted as double strikethrough text.

```csharp
public bool DoubleStrikeThrough { get; set; }
```

## Examples

Shows how to add a line strikethrough to text.

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

### See Also

* class [Font](../)
* namespace [Aspose.Words](../../../aspose.words/)
* assembly [Aspose.Words](../../../)
