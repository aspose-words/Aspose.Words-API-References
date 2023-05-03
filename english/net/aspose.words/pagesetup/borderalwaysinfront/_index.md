---
title: PageSetup.BorderAlwaysInFront
linktitle: BorderAlwaysInFront
second_title: Aspose.Words for .NET API Reference
description: PageSetup BorderAlwaysInFront property. Specifies where the page border is positioned relative to intersecting texts and objects in C#.
type: docs
weight: 20
url: /net/aspose.words/pagesetup/borderalwaysinfront/
---
## BorderAlwaysInFront property

Specifies where the page border is positioned relative to intersecting texts and objects.

```csharp
public bool BorderAlwaysInFront { get; set; }
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

* class [PageSetup](../)
* namespace [Aspose.Words](../../pagesetup/)
* assembly [Aspose.Words](../../../)
