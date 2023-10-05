---
title: Section.PageSetup
linktitle: PageSetup
articleTitle: PageSetup
second_title: Aspose.Words for .NET
description: Section PageSetup property. Returns an object that represents page setup and section properties in C#.
type: docs
weight: 50
url: /net/aspose.words/section/pagesetup/
---
## Section.PageSetup property

Returns an object that represents page setup and section properties.

```csharp
public PageSetup PageSetup { get; }
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

* class [PageSetup](../../pagesetup/)
* class [Section](../)
* namespace [Aspose.Words](../../../aspose.words/)
* assembly [Aspose.Words](../../../)
