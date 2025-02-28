---
title: Font.UnderlineColor
linktitle: UnderlineColor
articleTitle: UnderlineColor
second_title: Aspose.Words for .NET
description: Discover the Font UnderlineColor property to easily customize your font's underline color for enhanced text styling and visual appeal.
type: docs
weight: 550
url: /net/aspose.words/font/underlinecolor/
---
## Font.UnderlineColor property

Gets or sets the color of the underline applied to the font.

```csharp
public Color UnderlineColor { get; set; }
```

## Examples

Shows how to configure the style and color of a text underline.

```csharp
Document doc = new Document();
DocumentBuilder builder = new DocumentBuilder(doc);

builder.Font.Underline = Underline.Dotted;
builder.Font.UnderlineColor = Color.Red;

builder.Writeln("Underlined text.");

doc.Save(ArtifactsDir + "Font.Underlines.docx");
```

### See Also

* class [Font](../)
* namespace [Aspose.Words](../../../aspose.words/)
* assembly [Aspose.Words](../../../)
