---
title: Font.HighlightColor
linktitle: HighlightColor
articleTitle: HighlightColor
second_title: Aspose.Words for .NET
description: Discover the Font HighlightColor property—easily customize your text's highlight color for enhanced readability and visual appeal. Elevate your design!
type: docs
weight: 150
url: /net/aspose.words/font/highlightcolor/
---
## Font.HighlightColor property

Gets or sets the highlight (marker) color.

```csharp
public Color HighlightColor { get; set; }
```

## Examples

Shows how to format a run of text using its font property.

```csharp
Document doc = new Document();
Run run = new Run(doc, "Hello world!");

Aspose.Words.Font font = run.Font;
font.Name = "Courier New";
font.Size = 36;
font.HighlightColor = Color.Yellow;

doc.FirstSection.Body.FirstParagraph.AppendChild(run);
doc.Save(ArtifactsDir + "Font.CreateFormattedRun.docx");
```

### See Also

* class [Font](../)
* namespace [Aspose.Words](../../../aspose.words/)
* assembly [Aspose.Words](../../../)
