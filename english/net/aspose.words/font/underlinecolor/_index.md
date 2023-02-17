---
title: Font.UnderlineColor
second_title: Aspose.Words for .NET API Reference
description: Font property. Gets or sets the color of the underline applied to the font in C#.
type: docs
weight: 540
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
* namespace [Aspose.Words](../../font/)
* assembly [Aspose.Words](../../../)
