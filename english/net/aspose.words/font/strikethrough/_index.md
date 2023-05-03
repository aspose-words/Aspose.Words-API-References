---
title: Font.StrikeThrough
linktitle: StrikeThrough
articleTitle: StrikeThrough
second_title: Aspose.Words for .NET API Reference
description: Font StrikeThrough property. True if the font is formatted as strikethrough text in C#.
type: docs
weight: 390
url: /net/aspose.words/font/strikethrough/
---
## Font.StrikeThrough property

True if the font is formatted as strikethrough text.

```csharp
public bool StrikeThrough { get; set; }
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
* namespace [Aspose.Words](../../font/)
* assembly [Aspose.Words](../../../)
