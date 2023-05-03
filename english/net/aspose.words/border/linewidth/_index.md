---
title: Border.LineWidth
linktitle: LineWidth
second_title: Aspose.Words for .NET API Reference
description: Border LineWidth property. Gets or sets the border width in points in C#.
type: docs
weight: 50
url: /net/aspose.words/border/linewidth/
---
## LineWidth property

Gets or sets the border width in points.

```csharp
public double LineWidth { get; set; }
```

## Remarks

If you set line width greater than zero when line style is none, the line style is automatically changed to single line.

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

* class [Border](../)
* namespace [Aspose.Words](../../border/)
* assembly [Aspose.Words](../../../)
