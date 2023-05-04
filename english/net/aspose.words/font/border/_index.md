---
title: Font.Border
linktitle: Border
articleTitle: Border
second_title: Aspose.Words for .NET
description: Font Border property. Returns a Border object that specifies border for the font in C#.
type: docs
weight: 60
url: /net/aspose.words/font/border/
---
## Font.Border property

Returns a [`Border`](../../border/) object that specifies border for the font.

```csharp
public Border Border { get; }
```

## Examples

Shows how to insert a string surrounded by a border into a document.

```csharp
Document doc = new Document();
DocumentBuilder builder = new DocumentBuilder(doc);

builder.Font.Border.Color = Color.Green;
builder.Font.Border.LineWidth = 2.5d;
builder.Font.Border.LineStyle = LineStyle.DashDotStroker;

builder.Write("Text surrounded by green border.");

doc.Save(ArtifactsDir + "Border.FontBorder.docx");
```

### See Also

* class [Border](../../border/)
* class [Font](../)
* namespace [Aspose.Words](../../font/)
* assembly [Aspose.Words](../../../)
