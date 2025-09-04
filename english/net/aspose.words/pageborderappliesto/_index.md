---
title: PageBorderAppliesTo Enum
linktitle: PageBorderAppliesTo
articleTitle: PageBorderAppliesTo
second_title: Aspose.Words for .NET
description: Discover the Aspose.Words.PageBorderAppliesTo enum to control page border printing across specific pages for enhanced document formatting.
type: docs
weight: 5090
url: /net/aspose.words/pageborderappliesto/
---
## PageBorderAppliesTo enumeration

Specifies which pages the page border is printed on.

```csharp
public enum PageBorderAppliesTo
```

### Values

| Name | Value | Description |
| --- | --- | --- |
| AllPages | `0` | Page border is shown on all pages of the section. |
| FirstPage | `1` | Page border is shown on the first page of the section only. |
| OtherPages | `2` | Page border is shown on all pages except the first page of the section. |

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
* property [BorderAppliesTo](../pagesetup/borderappliesto/)
* namespace [Aspose.Words](../../aspose.words/)
* assembly [Aspose.Words](../../)
