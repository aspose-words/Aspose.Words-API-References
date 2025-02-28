---
title: PageSetup.Borders
linktitle: Borders
articleTitle: Borders
second_title: Aspose.Words for .NET
description: Discover the PageSetup Borders property to easily access and customize your page borders for a polished, professional look in your documents.
type: docs
weight: 50
url: /net/aspose.words/pagesetup/borders/
---
## PageSetup.Borders property

Gets a collection of the page borders.

```csharp
public BorderCollection Borders { get; }
```

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

* class [BorderCollection](../../bordercollection/)
* class [PageSetup](../)
* namespace [Aspose.Words](../../../aspose.words/)
* assembly [Aspose.Words](../../../)
