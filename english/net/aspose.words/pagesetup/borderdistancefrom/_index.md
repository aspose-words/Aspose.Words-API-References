---
title: PageSetup.BorderDistanceFrom
linktitle: BorderDistanceFrom
second_title: Aspose.Words for .NET API Reference
description: PageSetup BorderDistanceFrom property. Gets or sets a value that indicates whether the specified page border is measured from the edge of the page or from the text it surrounds in C#.
type: docs
weight: 40
url: /net/aspose.words/pagesetup/borderdistancefrom/
---
## PageSetup.BorderDistanceFrom property

Gets or sets a value that indicates whether the specified page border is measured from the edge of the page or from the text it surrounds.

```csharp
public PageBorderDistanceFrom BorderDistanceFrom { get; set; }
```

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

* enum [PageBorderDistanceFrom](../../pageborderdistancefrom/)
* class [PageSetup](../)
* namespace [Aspose.Words](../../pagesetup/)
* assembly [Aspose.Words](../../../)
