---
title: Border.DistanceFromText
linktitle: DistanceFromText
articleTitle: DistanceFromText
second_title: Aspose.Words for .NET
description: Discover the Border DistanceFromText property to easily adjust border spacing from text or page edges in points for enhanced layout control.
type: docs
weight: 20
url: /net/aspose.words/border/distancefromtext/
---
## Border.DistanceFromText property

Gets or sets distance of the border from text or from the page edge in points.

```csharp
public double DistanceFromText { get; set; }
```

## Remarks

Has no effect and will be automatically reset to zero for borders of table cells.

## Examples

Shows how to create a wide blue band border at the top of the first page.

```csharp
Document doc = new Document();

PageSetup pageSetup = doc.Sections[0].PageSetup;
pageSetup.BorderAlwaysInFront = false;
pageSetup.BorderDistanceFrom = PageBorderDistanceFrom.PageEdge;
pageSetup.BorderAppliesTo = PageBorderAppliesTo.FirstPage;

Border border = pageSetup.Borders[BorderType.Top];
border.LineStyle = LineStyle.Single;
border.LineWidth = 30;
border.Color = Color.Blue;
border.DistanceFromText = 0;

doc.Save(ArtifactsDir + "PageSetup.PageBorderProperties.docx");
```

### See Also

* class [Border](../)
* namespace [Aspose.Words](../../../aspose.words/)
* assembly [Aspose.Words](../../../)
