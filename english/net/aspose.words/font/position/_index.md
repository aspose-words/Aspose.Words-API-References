---
title: Font.Position
linktitle: Position
articleTitle: Position
second_title: Aspose.Words for .NET
description: Font Position property. Gets or sets the position of text in points relative to the base line. A positive number raises the text and a negative number lowers it in C#.
type: docs
weight: 300
url: /net/aspose.words/font/position/
---
## Font.Position property

Gets or sets the position of text (in points) relative to the base line. A positive number raises the text, and a negative number lowers it.

```csharp
public double Position { get; set; }
```

## Examples

Shows how to format text to offset its position.

```csharp
Document doc = new Document();
Paragraph para = (Paragraph)doc.GetChild(NodeType.Paragraph, 0, true);

// Raise this run of text 5 points above the baseline.
Run run = new Run(doc, "Raised text. ");
run.Font.Position = 5;
para.AppendChild(run);

// Lower this run of text 10 points below the baseline.
run = new Run(doc, "Lowered text. ");
run.Font.Position = -10;
para.AppendChild(run);

// Add a run of normal text.
run = new Run(doc, "Text in its default position. ");
para.AppendChild(run);

// Add a run of text that appears as subscript.
run = new Run(doc, "Subscript. ");
run.Font.Subscript = true;
para.AppendChild(run);

// Add a run of text that appears as superscript.
run = new Run(doc, "Superscript.");
run.Font.Superscript = true;
para.AppendChild(run);

doc.Save(ArtifactsDir + "Font.PositionSubscript.docx");
```

### See Also

* class [Font](../)
* namespace [Aspose.Words](../../../aspose.words/)
* assembly [Aspose.Words](../../../)
