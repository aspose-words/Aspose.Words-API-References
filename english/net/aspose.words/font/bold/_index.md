---
title: Bold
second_title: Aspose.Words for .NET API Reference
description: Font property. True if the font is formatted as bold in C#.
type: docs
weight: 40
url: /net/aspose.words/font/bold/
---
## Font.Bold property

True if the font is formatted as bold.

```csharp
public bool Bold { get; set; }
```

## Examples

Shows how to insert formatted text using DocumentBuilder.

```csharp
Document doc = new Document();
DocumentBuilder builder = new DocumentBuilder(doc);

// Specify font formatting, then add text.
Aspose.Words.Font font = builder.Font;
font.Size = 16;
font.Bold = true;
font.Color = Color.Blue;
font.Name = "Courier New";
font.Underline = Underline.Dash;

builder.Write("Hello world!");
```

### See Also

* class [Font](../)
* namespace [Aspose.Words](../../font/)
* assembly [Aspose.Words](../../../)
