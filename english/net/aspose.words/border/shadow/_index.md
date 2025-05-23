---
title: Border.Shadow
linktitle: Shadow
articleTitle: Shadow
second_title: Aspose.Words for .NET
description: Discover the Border Shadow property to enhance your design! Control shadow effects for borders and elevate your UI with stunning visuals.
type: docs
weight: 60
url: /net/aspose.words/border/shadow/
---
## Border.Shadow property

Gets or sets a value indicating whether the border has a shadow.

```csharp
public bool Shadow { get; set; }
```

## Remarks

In Microsoft Word, for a border to have a shadow, the borders on all four sides (left, top, right and bottom) should be of the same type, width, color and all should have the Shadow property set to `true`.

## Examples

Shows how to create green wavy page border with a shadow.

```csharp
Document doc = new Document();
PageSetup pageSetup = doc.Sections[0].PageSetup;

pageSetup.Borders.LineStyle = LineStyle.DoubleWave;
pageSetup.Borders.LineWidth = 2;
pageSetup.Borders.Color = Color.Green;
pageSetup.Borders.DistanceFromText = 24;
pageSetup.Borders.Shadow = true;

doc.Save(ArtifactsDir + "PageSetup.PageBorders.docx");
```

### See Also

* class [Border](../)
* namespace [Aspose.Words](../../../aspose.words/)
* assembly [Aspose.Words](../../../)
