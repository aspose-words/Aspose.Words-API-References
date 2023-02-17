---
title: Table.SetShading
second_title: Aspose.Words for .NET API Reference
description: Table method. Sets shading to the specified values on whole table in C#.
type: docs
weight: 430
url: /net/aspose.words.tables/table/setshading/
---
## Table.SetShading method

Sets shading to the specified values on whole table.

```csharp
public void SetShading(TextureIndex texture, Color foregroundColor, Color backgroundColor)
```

| Parameter | Type | Description |
| --- | --- | --- |
| texture | TextureIndex | The texture to apply. |
| foregroundColor | Color | The color of the texture. |
| backgroundColor | Color | The color of the background fill. |

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

* enum [TextureIndex](../../../aspose.words/textureindex/)
* class [Table](../)
* namespace [Aspose.Words.Tables](../../table/)
* assembly [Aspose.Words](../../../)
