---
title: Font.LineSpacing
linktitle: LineSpacing
articleTitle: LineSpacing
second_title: Aspose.Words for .NET
description: Discover the Font LineSpacing property, which provides the precise line spacing in points, enhancing your text's readability and design.
type: docs
weight: 190
url: /net/aspose.words/font/linespacing/
---
## Font.LineSpacing property

Returns line spacing of this font (in points).

```csharp
public double LineSpacing { get; }
```

## Examples

Shows how to get a font's line spacing, in points.

```csharp
Document doc = new Document();
DocumentBuilder builder = new DocumentBuilder(doc);

// Set different fonts for the DocumentBuilder and verify their line spacing.
builder.Font.Name = "Calibri";
Assert.AreEqual(14.6484375d, builder.Font.LineSpacing);

builder.Font.Name = "Times New Roman";
Assert.AreEqual(13.798828125d, builder.Font.LineSpacing);
```

### See Also

* class [Font](../)
* namespace [Aspose.Words](../../../aspose.words/)
* assembly [Aspose.Words](../../../)
