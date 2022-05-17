---
title: Table
second_title: Aspose.Words for .NET API Reference
description: 
type: docs
weight: 5990
url: /net/aspose.words.tables/table/
---
## Table class

Represents a table in a Word document.

```csharp
public class Table : CompositeNode
```

## Constructors

| Name | Description |
| --- | --- |
| [Table](table)(DocumentBase) | Initializes a new instance of the **Table** class. |

## Properties

| Name | Description |
| --- | --- |
| [AbsoluteHorizontalDistance](absolutehorizontaldistance) { get; set; } | Gets or sets absolute horizontal floating table position specified by the table properties, in points. Default value is 0. |
| [AbsoluteVerticalDistance](absoluteverticaldistance) { get; set; } | Gets or sets absolute vertical floating table position specified by the table properties, in points. Default value is 0. |
| [Alignment](alignment) { get; set; } | Specifies how an inline table is aligned in the document. |
| [AllowAutoFit](allowautofit) { get; set; } | Allows Microsoft Word and Aspose.Words to automatically resize cells in a table to fit their contents. |
| [AllowCellSpacing](allowcellspacing) { get; set; } | Gets or sets the "Allow spacing between cells" option. |
| [AllowOverlap](allowoverlap) { get; } | Gets whether a floating table shall allow other floating objects in the document to overlap its extents when displayed. Default value is `true`. |
| [Bidi](bidi) { get; set; } | Gets or sets whether this is a right-to-left table. |
| [BottomPadding](bottompadding) { get; set; } | Gets or sets the amount of space (in points) to add below the contents of cells. |
| [CellSpacing](cellspacing) { get; set; } | Gets or sets the amount of space (in points) between the cells. |
| [Description](description) { get; set; } | Gets or sets description of this table. It provides an alternative text representation of the information contained in the table. |
| [DistanceBottom](distancebottom) { get; } | Gets distance between table bottom and the surrounding text, in points. |
| [DistanceLeft](distanceleft) { get; } | Gets distance between table left and the surrounding text, in points. |
| [DistanceRight](distanceright) { get; } | Gets distance between table right and the surrounding text, in points. |
| [DistanceTop](distancetop) { get; } | Gets distance between table top and the surrounding text, in points. |
| [FirstRow](firstrow) { get; } | Returns the first **Row** node in the table. |
| [HorizontalAnchor](horizontalanchor) { get; set; } | Gets the base object from which the horizontal positioning of floating table should be calculated. Default value is Column. |
| [LastRow](lastrow) { get; } | Returns the last **Row** node in the table. |
| [LeftIndent](leftindent) { get; set; } | Gets or sets the value that represents the left indent of the table. |
| [LeftPadding](leftpadding) { get; set; } | Gets or sets the amount of space (in points) to add to the left of the contents of cells. |
| override [NodeType](nodetype) { get; } | Returns **NodeType.Table**. |
| [PreferredWidth](preferredwidth) { get; set; } | Gets or sets the table preferred width. |
| [RelativeHorizontalAlignment](relativehorizontalalignment) { get; set; } | Gets or sets floating table relative horizontal alignment. |
| [RelativeVerticalAlignment](relativeverticalalignment) { get; set; } | Gets or sets floating table relative vertical alignment. |
| [RightPadding](rightpadding) { get; set; } | Gets or sets the amount of space (in points) to add to the right of the contents of cells. |
| [Rows](rows) { get; } | Provides typed access to the rows of the table. |
| [Style](style) { get; set; } | Gets or sets the table style applied to this table. |
| [StyleIdentifier](styleidentifier) { get; set; } | Gets or sets the locale independent style identifier of the table style applied to this table. |
| [StyleName](stylename) { get; set; } | Gets or sets the name of the table style applied to this table. |
| [StyleOptions](styleoptions) { get; set; } | Gets or sets bit flags that specify how a table style is applied to this table. |
| [TextWrapping](textwrapping) { get; set; } | Gets or sets [`TextWrapping`](./textwrapping) for table. |
| [Title](title) { get; set; } | Gets or sets title of this table. It provides an alternative text representation of the information contained in the table. |
| [TopPadding](toppadding) { get; set; } | Gets or sets the amount of space (in points) to add above the contents of cells. |
| [VerticalAnchor](verticalanchor) { get; set; } | Gets the base object from which the vertical positioning of floating table should be calculated. Default value is Margin. |

## Methods

| Name | Description |
| --- | --- |
| override [Accept](accept)(DocumentVisitor) | Accepts a visitor. |
| [AutoFit](autofit)(AutoFitBehavior) | Resizes the table and cells according to the specified auto fit behavior. |
| [ClearBorders](clearborders)() | Removes all table and cell borders on this table. |
| [ClearShading](clearshading)() | Removes all shading on the table. |
| [ConvertToHorizontallyMergedCells](converttohorizontallymergedcells)() | Converts cells horizontally merged by width to cells merged by [`HorizontalMerge`](../cellformat/horizontalmerge). |
| [EnsureMinimum](ensureminimum)() | If the table has no rows, creates and appends one **Row**. |
| [SetBorder](setborder)(BorderType, LineStyle, double, Color, bool) | Sets the specified table border to the specified line style, width and color. |
| [SetBorders](setborders)(LineStyle, double, Color) | Sets all table borders to the specified line style, width and color. |
| [SetShading](setshading)(TextureIndex, Color, Color) | Sets shading to the specified values on whole table. |

### Remarks

**Table** is a block-level node and can be a child of classes derived from **Story** or **InlineStory**.

**Table** can contain one or more **Row** nodes.

A minimal valid table needs to have at least one **Row**.

### See Also

* class [CompositeNode](../../aspose.words/compositenode)
* namespace [Aspose.Words.Tables](../../aspose.words.tables)
* assembly [Aspose.Words](../../)

<!-- DO NOT EDIT: generated by xmldocmd for Aspose.Words.dll -->
