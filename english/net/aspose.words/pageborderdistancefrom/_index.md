---
title: PageBorderDistanceFrom Enum
linktitle: PageBorderDistanceFrom
second_title: Aspose.Words for .NET API Reference
description: Aspose.Words.PageBorderDistanceFrom enum. Specifies the positioning of the page border relative to the page margin in C#.
type: docs
weight: 4140
url: /net/aspose.words/pageborderdistancefrom/
---
## PageBorderDistanceFrom enumeration

Specifies the positioning of the page border relative to the page margin.

```csharp
public enum PageBorderDistanceFrom
```

### Values

| Name | Value | Description |
| --- | --- | --- |
| Text | `0` | Border position is measured from the page margin. |
| PageEdge | `1` | Border position is measured from the page edge. |

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

* class [PageSetup](../pagesetup/)
* property [BorderDistanceFrom](../pagesetup/borderdistancefrom/)
* namespace [Aspose.Words](../../aspose.words/)
* assembly [Aspose.Words](../../)
