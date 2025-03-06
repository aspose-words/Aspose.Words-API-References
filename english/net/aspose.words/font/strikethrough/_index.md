---
title: Font.StrikeThrough
linktitle: StrikeThrough
articleTitle: StrikeThrough
second_title: Aspose.Words for .NET
description: Discover the Font StrikeThrough property. Easily format text with strikethrough for clear visual emphasis in your designs. Enhance readability today!
type: docs
weight: 400
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
* namespace [Aspose.Words](../../../aspose.words/)
* assembly [Aspose.Words](../../../)
