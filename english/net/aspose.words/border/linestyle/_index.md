---
title: Border.LineStyle
linktitle: LineStyle
second_title: Aspose.Words for .NET API Reference
description: Border LineStyle property. Gets or sets the border style in C#.
type: docs
weight: 40
url: /net/aspose.words/border/linestyle/
---
## LineStyle property

Gets or sets the border style.

```csharp
public LineStyle LineStyle { get; set; }
```

## Remarks

If you set line style to none, then line width is automatically changed to zero.

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

* enum [LineStyle](../../linestyle/)
* class [Border](../)
* namespace [Aspose.Words](../../border/)
* assembly [Aspose.Words](../../../)
