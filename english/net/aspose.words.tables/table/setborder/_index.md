---
title: Table.SetBorder
linktitle: SetBorder
articleTitle: SetBorder
second_title: Aspose.Words for .NET
description: Customize your table's appearance with the SetBorder method—adjust line style, width, and color for a professional look. Enhance your design today!
type: docs
weight: 430
url: /net/aspose.words.tables/table/setborder/
---
## Table.SetBorder method

Sets the specified table border to the specified line style, width and color.

```csharp
public void SetBorder(BorderType borderType, LineStyle lineStyle, double lineWidth, Color color, 
    bool isOverrideCellBorders)
```

| Parameter | Type | Description |
| --- | --- | --- |
| borderType | BorderType | The table border to change. |
| lineStyle | LineStyle | The line style to apply. |
| lineWidth | Double | The line width to set (in points). |
| color | Color | The color to use for the border. |
| isOverrideCellBorders | Boolean | When `true`, causes all existing explicit cell borders to be removed. |

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

* enum [BorderType](../../../aspose.words/bordertype/)
* enum [LineStyle](../../../aspose.words/linestyle/)
* class [Table](../)
* namespace [Aspose.Words.Tables](../../../aspose.words.tables/)
* assembly [Aspose.Words](../../../)
