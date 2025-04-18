---
title: PageSetup.BorderAppliesTo
linktitle: BorderAppliesTo
articleTitle: BorderAppliesTo
second_title: Aspose.Words for .NET
description: Discover how the PageSetup BorderAppliesTo property enhances your document layout by controlling page border printing for a polished, professional look.
type: docs
weight: 30
url: /net/aspose.words/pagesetup/borderappliesto/
---
## PageSetup.BorderAppliesTo property

Specifies which pages the page border is printed on.

```csharp
public PageBorderAppliesTo BorderAppliesTo { get; set; }
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

* enum [PageBorderAppliesTo](../../pageborderappliesto/)
* class [PageSetup](../)
* namespace [Aspose.Words](../../../aspose.words/)
* assembly [Aspose.Words](../../../)
