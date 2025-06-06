---
title: TableAlignment Enum
linktitle: TableAlignment
articleTitle: TableAlignment
second_title: Aspose.Words for .NET
description: Discover Aspose.Words.Tables.TableAlignment enum for optimal inline table alignment. Enhance your document formatting with precision and ease.
type: docs
weight: 7210
url: /net/aspose.words.tables/tablealignment/
---
## TableAlignment enumeration

Specifies alignment for an inline table.

```csharp
public enum TableAlignment
```

### Values

| Name | Value | Description |
| --- | --- | --- |
| Left | `0` | The table is aligned to the left. |
| Center | `1` | The table is centered. |
| Right | `2` | The table is aligned to the right. |

## Examples

Shows how to apply an outline border to a table.

```csharp
Document doc = new Document(MyDir + "Tables.docx");
Table table = doc.FirstSection.Body.Tables[0];

// Align the table to the center of the page.
table.Alignment = TableAlignment.Center;

// Clear any existing borders and shading from the table.
table.ClearBorders();
table.ClearShading();

// Add green borders to the outline of the table.
table.SetBorder(BorderType.Left, LineStyle.Single, 1.5, Color.Green, true);
table.SetBorder(BorderType.Right, LineStyle.Single, 1.5, Color.Green, true);
table.SetBorder(BorderType.Top, LineStyle.Single, 1.5, Color.Green, true);
table.SetBorder(BorderType.Bottom, LineStyle.Single, 1.5, Color.Green, true);

// Fill the cells with a light green solid color.
table.SetShading(TextureIndex.TextureSolid, Color.LightGreen, Color.Empty);

doc.Save(ArtifactsDir + "Table.SetOutlineBorders.docx");
```

### See Also

* namespace [Aspose.Words.Tables](../../aspose.words.tables/)
* assembly [Aspose.Words](../../)
