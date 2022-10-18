---
title: Table
second_title: Aspose.Words for Java API Reference
description: Represents a table in a Word document.
type: docs
weight: 548
url: /java/com.aspose.words/table/
---

**Inheritance:**
java.lang.Object, [com.aspose.words.Node](../../com.aspose.words/node), [com.aspose.words.CompositeNode](../../com.aspose.words/compositenode)
```
public class Table extends CompositeNode
```

Represents a table in a Word document.

To learn more, visit the **Working with Tables** documentation article.

**Table** is a block-level node and can be a child of classes derived from **Story** or **InlineStory**.

**Table** can contain one or more **Row** nodes.

A minimal valid table needs to have at least one **Row**.
## Constructors

| Constructor | Description |
| --- | --- |
| [Table(DocumentBase doc)](#Table-com.aspose.words.DocumentBase-) | Initializes a new instance of the **Table** class. |
## Methods

| Method | Description |
| --- | --- |
| [convertToHorizontallyMergedCells()](#convertToHorizontallyMergedCells--) | Converts cells horizontally merged by width to cells merged by [CellFormat.getHorizontalMerge()](../../com.aspose.words/cellformat\#getHorizontalMerge--) / [CellFormat.setHorizontalMerge(int)](../../com.aspose.words/cellformat\#setHorizontalMerge-int-). |
| [getNodeType()](#getNodeType--) | Returns **NodeType.Table**. |
| [getFirstRow()](#getFirstRow--) | Returns the first **Row** node in the table. |
| [getLastRow()](#getLastRow--) | Returns the last **Row** node in the table. |
| [getRows()](#getRows--) | Provides typed access to the rows of the table. |
| [accept(DocumentVisitor visitor)](#accept-com.aspose.words.DocumentVisitor-) | Accepts a visitor. |
| [ensureMinimum()](#ensureMinimum--) | If the table has no rows, creates and appends one **Row**. |
| [getAlignment()](#getAlignment--) | Specifies how an inline table is aligned in the document. |
| [setAlignment(int value)](#setAlignment-int-) | Specifies how an inline table is aligned in the document. |
| [getAllowAutoFit()](#getAllowAutoFit--) | Allows Microsoft Word and Aspose.Words to automatically resize cells in a table to fit their contents. |
| [setAllowAutoFit(boolean value)](#setAllowAutoFit-boolean-) | Allows Microsoft Word and Aspose.Words to automatically resize cells in a table to fit their contents. |
| [getPreferredWidth()](#getPreferredWidth--) | Gets the table preferred width. |
| [setPreferredWidth(PreferredWidth value)](#setPreferredWidth-com.aspose.words.PreferredWidth-) | Sets the table preferred width. |
| [getBidi()](#getBidi--) | Gets whether this is a right-to-left table. |
| [setBidi(boolean value)](#setBidi-boolean-) | Sets whether this is a right-to-left table. |
| [getLeftPadding()](#getLeftPadding--) | Gets the amount of space (in points) to add to the left of the contents of cells. |
| [setLeftPadding(double value)](#setLeftPadding-double-) | Sets the amount of space (in points) to add to the left of the contents of cells. |
| [getRightPadding()](#getRightPadding--) | Gets the amount of space (in points) to add to the right of the contents of cells. |
| [setRightPadding(double value)](#setRightPadding-double-) | Sets the amount of space (in points) to add to the right of the contents of cells. |
| [getTopPadding()](#getTopPadding--) | Gets the amount of space (in points) to add above the contents of cells. |
| [setTopPadding(double value)](#setTopPadding-double-) | Sets the amount of space (in points) to add above the contents of cells. |
| [getBottomPadding()](#getBottomPadding--) | Gets the amount of space (in points) to add below the contents of cells. |
| [setBottomPadding(double value)](#setBottomPadding-double-) | Sets the amount of space (in points) to add below the contents of cells. |
| [getCellSpacing()](#getCellSpacing--) | Gets the amount of space (in points) between the cells. |
| [setCellSpacing(double value)](#setCellSpacing-double-) | Sets the amount of space (in points) between the cells. |
| [getAllowCellSpacing()](#getAllowCellSpacing--) | Gets the "Allow spacing between cells" option. |
| [setAllowCellSpacing(boolean value)](#setAllowCellSpacing-boolean-) | Sets the "Allow spacing between cells" option. |
| [getLeftIndent()](#getLeftIndent--) | Gets the value that represents the left indent of the table. |
| [setLeftIndent(double value)](#setLeftIndent-double-) | Sets the value that represents the left indent of the table. |
| [getStyleOptions()](#getStyleOptions--) | Gets bit flags that specify how a table style is applied to this table. |
| [setStyleOptions(int value)](#setStyleOptions-int-) | Sets bit flags that specify how a table style is applied to this table. |
| [getStyle()](#getStyle--) | Gets the table style applied to this table. |
| [setStyle(Style value)](#setStyle-com.aspose.words.Style-) | Sets the table style applied to this table. |
| [getStyleName()](#getStyleName--) | Gets the name of the table style applied to this table. |
| [setStyleName(String value)](#setStyleName-java.lang.String-) | Sets the name of the table style applied to this table. |
| [getStyleIdentifier()](#getStyleIdentifier--) | Gets the locale independent style identifier of the table style applied to this table. |
| [setStyleIdentifier(int value)](#setStyleIdentifier-int-) | Sets the locale independent style identifier of the table style applied to this table. |
| [getTextWrapping()](#getTextWrapping--) | Gets [getTextWrapping()](../../com.aspose.words/table\#getTextWrapping--) / [setTextWrapping(int)](../../com.aspose.words/table\#setTextWrapping-int-) for table. |
| [setTextWrapping(int value)](#setTextWrapping-int-) | Sets [getTextWrapping()](../../com.aspose.words/table\#getTextWrapping--) / [setTextWrapping(int)](../../com.aspose.words/table\#setTextWrapping-int-) for table. |
| [getTitle()](#getTitle--) | Gets title of this table. |
| [setTitle(String value)](#setTitle-java.lang.String-) | Sets title of this table. |
| [getDescription()](#getDescription--) | Gets description of this table. |
| [setDescription(String value)](#setDescription-java.lang.String-) | Sets description of this table. |
| [getDistanceLeft()](#getDistanceLeft--) | Gets distance between table left and the surrounding text, in points. |
| [getDistanceRight()](#getDistanceRight--) | Gets distance between table right and the surrounding text, in points. |
| [getDistanceTop()](#getDistanceTop--) | Gets distance between table top and the surrounding text, in points. |
| [getDistanceBottom()](#getDistanceBottom--) | Gets distance between table bottom and the surrounding text, in points. |
| [getRelativeHorizontalAlignment()](#getRelativeHorizontalAlignment--) | Gets floating table relative horizontal alignment. |
| [setRelativeHorizontalAlignment(int value)](#setRelativeHorizontalAlignment-int-) | Sets floating table relative horizontal alignment. |
| [getRelativeVerticalAlignment()](#getRelativeVerticalAlignment--) | Gets floating table relative vertical alignment. |
| [setRelativeVerticalAlignment(int value)](#setRelativeVerticalAlignment-int-) | Sets floating table relative vertical alignment. |
| [getHorizontalAnchor()](#getHorizontalAnchor--) | Gets the base object from which the horizontal positioning of floating table should be calculated. |
| [setHorizontalAnchor(int value)](#setHorizontalAnchor-int-) | Gets the base object from which the horizontal positioning of floating table should be calculated. |
| [getVerticalAnchor()](#getVerticalAnchor--) | Gets the base object from which the vertical positioning of floating table should be calculated. |
| [setVerticalAnchor(int value)](#setVerticalAnchor-int-) | Gets the base object from which the vertical positioning of floating table should be calculated. |
| [getAbsoluteHorizontalDistance()](#getAbsoluteHorizontalDistance--) | Gets absolute horizontal floating table position specified by the table properties, in points. |
| [setAbsoluteHorizontalDistance(double value)](#setAbsoluteHorizontalDistance-double-) | Sets absolute horizontal floating table position specified by the table properties, in points. |
| [getAbsoluteVerticalDistance()](#getAbsoluteVerticalDistance--) | Gets absolute vertical floating table position specified by the table properties, in points. |
| [setAbsoluteVerticalDistance(double value)](#setAbsoluteVerticalDistance-double-) | Sets absolute vertical floating table position specified by the table properties, in points. |
| [getAllowOverlap()](#getAllowOverlap--) | Gets whether a floating table shall allow other floating objects in the document to overlap its extents when displayed. |
| [setBorders(int lineStyle, double lineWidth, Color color)](#setBorders-int-double-java.awt.Color-) |  |
| [setBorder(int borderType, int lineStyle, double lineWidth, Color color, boolean isOverrideCellBorders)](#setBorder-int-int-double-java.awt.Color-boolean-) |  |
| [clearBorders()](#clearBorders--) | Removes all table and cell borders on this table. |
| [setShading(int texture, Color foregroundColor, Color backgroundColor)](#setShading-int-java.awt.Color-java.awt.Color-) |  |
| [clearShading()](#clearShading--) | Removes all shading on the table. |
| [autoFit(int behavior)](#autoFit-int-) |  |
### Table(DocumentBase doc) {#Table-com.aspose.words.DocumentBase-}
```
public Table(DocumentBase doc)
```


Initializes a new instance of the **Table** class.

When **Table** is created, it belongs to the specified document, but is not yet part of the document and **ParentNode** is null.

To append **Table** to the document use InsertAfter or InsertBefore on the story where you want the table inserted.

**Parameters:**
| Parameter | Type | Description |
| --- | --- | --- |
| doc | [DocumentBase](../../com.aspose.words/documentbase) | The owner document. |

### convertToHorizontallyMergedCells() {#convertToHorizontallyMergedCells--}
```
public void convertToHorizontallyMergedCells()
```


Converts cells horizontally merged by width to cells merged by [CellFormat.getHorizontalMerge()](../../com.aspose.words/cellformat\#getHorizontalMerge--) / [CellFormat.setHorizontalMerge(int)](../../com.aspose.words/cellformat\#setHorizontalMerge-int-).

Table cells can be horizontally merged either using merge flags [CellFormat.getHorizontalMerge()](../../com.aspose.words/cellformat\#getHorizontalMerge--) / [CellFormat.setHorizontalMerge(int)](../../com.aspose.words/cellformat\#setHorizontalMerge-int-) or using cell width [CellFormat.getWidth()](../../com.aspose.words/cellformat\#getWidth--) / [CellFormat.setWidth(double)](../../com.aspose.words/cellformat\#setWidth-double-).

When table cell is merged by width property [CellFormat.getHorizontalMerge()](../../com.aspose.words/cellformat\#getHorizontalMerge--) / [CellFormat.setHorizontalMerge(int)](../../com.aspose.words/cellformat\#setHorizontalMerge-int-) is meaningless but sometimes having merge flags is more convenient way.

Use this method to transforms table cells horizontally merged by width to cells merged by merge flags.

### getNodeType() {#getNodeType--}
```
public int getNodeType()
```


Returns **NodeType.Table**.

**Returns:**
int - **NodeType.Table**. The returned value is one of [NodeType](../../com.aspose.words/nodetype) constants.
### getFirstRow() {#getFirstRow--}
```
public Row getFirstRow()
```


Returns the first **Row** node in the table.

**Returns:**
[Row](../../com.aspose.words/row) - The first **Row** node in the table.
### getLastRow() {#getLastRow--}
```
public Row getLastRow()
```


Returns the last **Row** node in the table.

**Returns:**
[Row](../../com.aspose.words/row) - The last **Row** node in the table.
### getRows() {#getRows--}
```
public RowCollection getRows()
```


Provides typed access to the rows of the table.

**Returns:**
[RowCollection](../../com.aspose.words/rowcollection) - The corresponding [RowCollection](../../com.aspose.words/rowcollection) value.
### accept(DocumentVisitor visitor) {#accept-com.aspose.words.DocumentVisitor-}
```
public boolean accept(DocumentVisitor visitor)
```


Accepts a visitor.

Enumerates over this node and all of its children. Each node calls a corresponding method on DocumentVisitor.

For more info see the Visitor design pattern.

**Parameters:**
| Parameter | Type | Description |
| --- | --- | --- |
| visitor | [DocumentVisitor](../../com.aspose.words/documentvisitor) | The visitor that will visit the nodes. |

**Returns:**
boolean - True if all nodes were visited; false if DocumentVisitor stopped the operation before visiting all nodes. Calls DocumentVisitor.VisitTableStart, then calls Accept for all child nodes of the section and calls DocumentVisitor.VisitTableEnd at the end.
### ensureMinimum() {#ensureMinimum--}
```
public void ensureMinimum()
```


If the table has no rows, creates and appends one **Row**.

### getAlignment() {#getAlignment--}
```
public int getAlignment()
```


Specifies how an inline table is aligned in the document.

The default value is [TableAlignment.LEFT](../../com.aspose.words/tablealignment\#LEFT).

**Returns:**
int - The corresponding  int  value. The returned value is one of [TableAlignment](../../com.aspose.words/tablealignment) constants.
### setAlignment(int value) {#setAlignment-int-}
```
public void setAlignment(int value)
```


Specifies how an inline table is aligned in the document.

The default value is [TableAlignment.LEFT](../../com.aspose.words/tablealignment\#LEFT).

**Parameters:**
| Parameter | Type | Description |
| --- | --- | --- |
| value | int | The corresponding  int  value. The value must be one of [TableAlignment](../../com.aspose.words/tablealignment) constants. |

### getAllowAutoFit() {#getAllowAutoFit--}
```
public boolean getAllowAutoFit()
```


Allows Microsoft Word and Aspose.Words to automatically resize cells in a table to fit their contents.

The default value is  true .

**M:Aspose.Words.Tables.Table.AutoFit(Aspose.Words.Tables.AutoFitBehavior)**

**Returns:**
boolean - The corresponding  boolean  value.
### setAllowAutoFit(boolean value) {#setAllowAutoFit-boolean-}
```
public void setAllowAutoFit(boolean value)
```


Allows Microsoft Word and Aspose.Words to automatically resize cells in a table to fit their contents.

The default value is  true .

**M:Aspose.Words.Tables.Table.AutoFit(Aspose.Words.Tables.AutoFitBehavior)**

**Parameters:**
| Parameter | Type | Description |
| --- | --- | --- |
| value | boolean | The corresponding  boolean  value. |

### getPreferredWidth() {#getPreferredWidth--}
```
public PreferredWidth getPreferredWidth()
```


Gets the table preferred width.

The default value is [PreferredWidth.AUTO](../../com.aspose.words/preferredwidth\#AUTO).

**Returns:**
[PreferredWidth](../../com.aspose.words/preferredwidth) - The table preferred width.
### setPreferredWidth(PreferredWidth value) {#setPreferredWidth-com.aspose.words.PreferredWidth-}
```
public void setPreferredWidth(PreferredWidth value)
```


Sets the table preferred width.

The default value is [PreferredWidth.AUTO](../../com.aspose.words/preferredwidth\#AUTO).

**Parameters:**
| Parameter | Type | Description |
| --- | --- | --- |
| value | [PreferredWidth](../../com.aspose.words/preferredwidth) | The table preferred width. |

### getBidi() {#getBidi--}
```
public boolean getBidi()
```


Gets whether this is a right-to-left table.

When  true , the cells in this row are laid out right to left.

The default value is  false .

**Returns:**
boolean - Whether this is a right-to-left table.
### setBidi(boolean value) {#setBidi-boolean-}
```
public void setBidi(boolean value)
```


Sets whether this is a right-to-left table.

When  true , the cells in this row are laid out right to left.

The default value is  false .

**Parameters:**
| Parameter | Type | Description |
| --- | --- | --- |
| value | boolean | Whether this is a right-to-left table. |

### getLeftPadding() {#getLeftPadding--}
```
public double getLeftPadding()
```


Gets the amount of space (in points) to add to the left of the contents of cells.

**Returns:**
double - The amount of space (in points) to add to the left of the contents of cells.
### setLeftPadding(double value) {#setLeftPadding-double-}
```
public void setLeftPadding(double value)
```


Sets the amount of space (in points) to add to the left of the contents of cells.

**Parameters:**
| Parameter | Type | Description |
| --- | --- | --- |
| value | double | The amount of space (in points) to add to the left of the contents of cells. |

### getRightPadding() {#getRightPadding--}
```
public double getRightPadding()
```


Gets the amount of space (in points) to add to the right of the contents of cells.

**Returns:**
double - The amount of space (in points) to add to the right of the contents of cells.
### setRightPadding(double value) {#setRightPadding-double-}
```
public void setRightPadding(double value)
```


Sets the amount of space (in points) to add to the right of the contents of cells.

**Parameters:**
| Parameter | Type | Description |
| --- | --- | --- |
| value | double | The amount of space (in points) to add to the right of the contents of cells. |

### getTopPadding() {#getTopPadding--}
```
public double getTopPadding()
```


Gets the amount of space (in points) to add above the contents of cells.

**Returns:**
double - The amount of space (in points) to add above the contents of cells.
### setTopPadding(double value) {#setTopPadding-double-}
```
public void setTopPadding(double value)
```


Sets the amount of space (in points) to add above the contents of cells.

**Parameters:**
| Parameter | Type | Description |
| --- | --- | --- |
| value | double | The amount of space (in points) to add above the contents of cells. |

### getBottomPadding() {#getBottomPadding--}
```
public double getBottomPadding()
```


Gets the amount of space (in points) to add below the contents of cells.

**Returns:**
double - The amount of space (in points) to add below the contents of cells.
### setBottomPadding(double value) {#setBottomPadding-double-}
```
public void setBottomPadding(double value)
```


Sets the amount of space (in points) to add below the contents of cells.

**Parameters:**
| Parameter | Type | Description |
| --- | --- | --- |
| value | double | The amount of space (in points) to add below the contents of cells. |

### getCellSpacing() {#getCellSpacing--}
```
public double getCellSpacing()
```


Gets the amount of space (in points) between the cells.

**Returns:**
double - The amount of space (in points) between the cells.
### setCellSpacing(double value) {#setCellSpacing-double-}
```
public void setCellSpacing(double value)
```


Sets the amount of space (in points) between the cells.

**Parameters:**
| Parameter | Type | Description |
| --- | --- | --- |
| value | double | The amount of space (in points) between the cells. |

### getAllowCellSpacing() {#getAllowCellSpacing--}
```
public boolean getAllowCellSpacing()
```


Gets the "Allow spacing between cells" option.

**Returns:**
boolean - The "Allow spacing between cells" option.
### setAllowCellSpacing(boolean value) {#setAllowCellSpacing-boolean-}
```
public void setAllowCellSpacing(boolean value)
```


Sets the "Allow spacing between cells" option.

**Parameters:**
| Parameter | Type | Description |
| --- | --- | --- |
| value | boolean | The "Allow spacing between cells" option. |

### getLeftIndent() {#getLeftIndent--}
```
public double getLeftIndent()
```


Gets the value that represents the left indent of the table.

**Returns:**
double - The value that represents the left indent of the table.
### setLeftIndent(double value) {#setLeftIndent-double-}
```
public void setLeftIndent(double value)
```


Sets the value that represents the left indent of the table.

**Parameters:**
| Parameter | Type | Description |
| --- | --- | --- |
| value | double | The value that represents the left indent of the table. |

### getStyleOptions() {#getStyleOptions--}
```
public int getStyleOptions()
```


Gets bit flags that specify how a table style is applied to this table.

**Returns:**
int - Bit flags that specify how a table style is applied to this table. The returned value is a bitwise combination of [TableStyleOptions](../../com.aspose.words/tablestyleoptions) constants.
### setStyleOptions(int value) {#setStyleOptions-int-}
```
public void setStyleOptions(int value)
```


Sets bit flags that specify how a table style is applied to this table.

**Parameters:**
| Parameter | Type | Description |
| --- | --- | --- |
| value | int | Bit flags that specify how a table style is applied to this table. The value must be a bitwise combination of [TableStyleOptions](../../com.aspose.words/tablestyleoptions) constants. |

### getStyle() {#getStyle--}
```
public Style getStyle()
```


Gets the table style applied to this table.

**Returns:**
[Style](../../com.aspose.words/style) - The table style applied to this table.
### setStyle(Style value) {#setStyle-com.aspose.words.Style-}
```
public void setStyle(Style value)
```


Sets the table style applied to this table.

**Parameters:**
| Parameter | Type | Description |
| --- | --- | --- |
| value | [Style](../../com.aspose.words/style) | The table style applied to this table. |

### getStyleName() {#getStyleName--}
```
public String getStyleName()
```


Gets the name of the table style applied to this table.

**Returns:**
java.lang.String - The name of the table style applied to this table.
### setStyleName(String value) {#setStyleName-java.lang.String-}
```
public void setStyleName(String value)
```


Sets the name of the table style applied to this table.

**Parameters:**
| Parameter | Type | Description |
| --- | --- | --- |
| value | java.lang.String | The name of the table style applied to this table. |

### getStyleIdentifier() {#getStyleIdentifier--}
```
public int getStyleIdentifier()
```


Gets the locale independent style identifier of the table style applied to this table.

**Returns:**
int - The locale independent style identifier of the table style applied to this table. The returned value is one of [StyleIdentifier](../../com.aspose.words/styleidentifier) constants.
### setStyleIdentifier(int value) {#setStyleIdentifier-int-}
```
public void setStyleIdentifier(int value)
```


Sets the locale independent style identifier of the table style applied to this table.

**Parameters:**
| Parameter | Type | Description |
| --- | --- | --- |
| value | int | The locale independent style identifier of the table style applied to this table. The value must be one of [StyleIdentifier](../../com.aspose.words/styleidentifier) constants. |

### getTextWrapping() {#getTextWrapping--}
```
public int getTextWrapping()
```


Gets [getTextWrapping()](../../com.aspose.words/table\#getTextWrapping--) / [setTextWrapping(int)](../../com.aspose.words/table\#setTextWrapping-int-) for table.

**Returns:**
int - \{[getTextWrapping()](../../com.aspose.words/table\#getTextWrapping--) / [setTextWrapping(int)](../../com.aspose.words/table\#setTextWrapping-int-) for table. The returned value is one of [TextWrapping](../../com.aspose.words/textwrapping) constants.
### setTextWrapping(int value) {#setTextWrapping-int-}
```
public void setTextWrapping(int value)
```


Sets [getTextWrapping()](../../com.aspose.words/table\#getTextWrapping--) / [setTextWrapping(int)](../../com.aspose.words/table\#setTextWrapping-int-) for table.

**Parameters:**
| Parameter | Type | Description |
| --- | --- | --- |
| value | int | \{[getTextWrapping()](../../com.aspose.words/table\#getTextWrapping--) / [setTextWrapping(int)](../../com.aspose.words/table\#setTextWrapping-int-) for table. The value must be one of [TextWrapping](../../com.aspose.words/textwrapping) constants. |

### getTitle() {#getTitle--}
```
public String getTitle()
```


Gets title of this table. It provides an alternative text representation of the information contained in the table.

The default value is an empty string.

This property is meaningful for ISO/IEC 29500 compliant DOCX documents ( [OoxmlCompliance](../../com.aspose.words/ooxmlcompliance)). When saved to pre-ISO/IEC 29500 formats, the property is ignored.

**Returns:**
java.lang.String - Title of this table.
### setTitle(String value) {#setTitle-java.lang.String-}
```
public void setTitle(String value)
```


Sets title of this table. It provides an alternative text representation of the information contained in the table.

The default value is an empty string.

This property is meaningful for ISO/IEC 29500 compliant DOCX documents ( [OoxmlCompliance](../../com.aspose.words/ooxmlcompliance)). When saved to pre-ISO/IEC 29500 formats, the property is ignored.

**Parameters:**
| Parameter | Type | Description |
| --- | --- | --- |
| value | java.lang.String | Title of this table. |

### getDescription() {#getDescription--}
```
public String getDescription()
```


Gets description of this table. It provides an alternative text representation of the information contained in the table.

The default value is an empty string.

This property is meaningful for ISO/IEC 29500 compliant DOCX documents ( [OoxmlCompliance](../../com.aspose.words/ooxmlcompliance)). When saved to pre-ISO/IEC 29500 formats, the property is ignored.

**Returns:**
java.lang.String - Description of this table.
### setDescription(String value) {#setDescription-java.lang.String-}
```
public void setDescription(String value)
```


Sets description of this table. It provides an alternative text representation of the information contained in the table.

The default value is an empty string.

This property is meaningful for ISO/IEC 29500 compliant DOCX documents ( [OoxmlCompliance](../../com.aspose.words/ooxmlcompliance)). When saved to pre-ISO/IEC 29500 formats, the property is ignored.

**Parameters:**
| Parameter | Type | Description |
| --- | --- | --- |
| value | java.lang.String | Description of this table. |

### getDistanceLeft() {#getDistanceLeft--}
```
public double getDistanceLeft()
```


Gets distance between table left and the surrounding text, in points.

**Returns:**
double - Distance between table left and the surrounding text, in points.
### getDistanceRight() {#getDistanceRight--}
```
public double getDistanceRight()
```


Gets distance between table right and the surrounding text, in points.

**Returns:**
double - Distance between table right and the surrounding text, in points.
### getDistanceTop() {#getDistanceTop--}
```
public double getDistanceTop()
```


Gets distance between table top and the surrounding text, in points.

**Returns:**
double - Distance between table top and the surrounding text, in points.
### getDistanceBottom() {#getDistanceBottom--}
```
public double getDistanceBottom()
```


Gets distance between table bottom and the surrounding text, in points.

**Returns:**
double - Distance between table bottom and the surrounding text, in points.
### getRelativeHorizontalAlignment() {#getRelativeHorizontalAlignment--}
```
public int getRelativeHorizontalAlignment()
```


Gets floating table relative horizontal alignment.

**Returns:**
int - Floating table relative horizontal alignment. The returned value is one of [HorizontalAlignment](../../com.aspose.words/horizontalalignment) constants.
### setRelativeHorizontalAlignment(int value) {#setRelativeHorizontalAlignment-int-}
```
public void setRelativeHorizontalAlignment(int value)
```


Sets floating table relative horizontal alignment.

**Parameters:**
| Parameter | Type | Description |
| --- | --- | --- |
| value | int | Floating table relative horizontal alignment. The value must be one of [HorizontalAlignment](../../com.aspose.words/horizontalalignment) constants. |

### getRelativeVerticalAlignment() {#getRelativeVerticalAlignment--}
```
public int getRelativeVerticalAlignment()
```


Gets floating table relative vertical alignment.

**Returns:**
int - Floating table relative vertical alignment. The returned value is one of [VerticalAlignment](../../com.aspose.words/verticalalignment) constants.
### setRelativeVerticalAlignment(int value) {#setRelativeVerticalAlignment-int-}
```
public void setRelativeVerticalAlignment(int value)
```


Sets floating table relative vertical alignment.

**Parameters:**
| Parameter | Type | Description |
| --- | --- | --- |
| value | int | Floating table relative vertical alignment. The value must be one of [VerticalAlignment](../../com.aspose.words/verticalalignment) constants. |

### getHorizontalAnchor() {#getHorizontalAnchor--}
```
public int getHorizontalAnchor()
```


Gets the base object from which the horizontal positioning of floating table should be calculated. Default value is [RelativeHorizontalPosition.COLUMN](../../com.aspose.words/relativehorizontalposition\#COLUMN).

**Returns:**
int - The base object from which the horizontal positioning of floating table should be calculated. The returned value is one of [RelativeHorizontalPosition](../../com.aspose.words/relativehorizontalposition) constants.
### setHorizontalAnchor(int value) {#setHorizontalAnchor-int-}
```
public void setHorizontalAnchor(int value)
```


Gets the base object from which the horizontal positioning of floating table should be calculated. Default value is [RelativeHorizontalPosition.COLUMN](../../com.aspose.words/relativehorizontalposition\#COLUMN).

**Parameters:**
| Parameter | Type | Description |
| --- | --- | --- |
| value | int | The base object from which the horizontal positioning of floating table should be calculated. The value must be one of [RelativeHorizontalPosition](../../com.aspose.words/relativehorizontalposition) constants. |

### getVerticalAnchor() {#getVerticalAnchor--}
```
public int getVerticalAnchor()
```


Gets the base object from which the vertical positioning of floating table should be calculated. Default value is [RelativeVerticalPosition.MARGIN](../../com.aspose.words/relativeverticalposition\#MARGIN).

**Returns:**
int - The base object from which the vertical positioning of floating table should be calculated. The returned value is one of [RelativeVerticalPosition](../../com.aspose.words/relativeverticalposition) constants.
### setVerticalAnchor(int value) {#setVerticalAnchor-int-}
```
public void setVerticalAnchor(int value)
```


Gets the base object from which the vertical positioning of floating table should be calculated. Default value is [RelativeVerticalPosition.MARGIN](../../com.aspose.words/relativeverticalposition\#MARGIN).

**Parameters:**
| Parameter | Type | Description |
| --- | --- | --- |
| value | int | The base object from which the vertical positioning of floating table should be calculated. The value must be one of [RelativeVerticalPosition](../../com.aspose.words/relativeverticalposition) constants. |

### getAbsoluteHorizontalDistance() {#getAbsoluteHorizontalDistance--}
```
public double getAbsoluteHorizontalDistance()
```


Gets absolute horizontal floating table position specified by the table properties, in points. Default value is 0.

**Returns:**
double - Absolute horizontal floating table position specified by the table properties, in points.
### setAbsoluteHorizontalDistance(double value) {#setAbsoluteHorizontalDistance-double-}
```
public void setAbsoluteHorizontalDistance(double value)
```


Sets absolute horizontal floating table position specified by the table properties, in points. Default value is 0.

**Parameters:**
| Parameter | Type | Description |
| --- | --- | --- |
| value | double | Absolute horizontal floating table position specified by the table properties, in points. |

### getAbsoluteVerticalDistance() {#getAbsoluteVerticalDistance--}
```
public double getAbsoluteVerticalDistance()
```


Gets absolute vertical floating table position specified by the table properties, in points. Default value is 0.

**Returns:**
double - Absolute vertical floating table position specified by the table properties, in points.
### setAbsoluteVerticalDistance(double value) {#setAbsoluteVerticalDistance-double-}
```
public void setAbsoluteVerticalDistance(double value)
```


Sets absolute vertical floating table position specified by the table properties, in points. Default value is 0.

**Parameters:**
| Parameter | Type | Description |
| --- | --- | --- |
| value | double | Absolute vertical floating table position specified by the table properties, in points. |

### getAllowOverlap() {#getAllowOverlap--}
```
public boolean getAllowOverlap()
```


Gets whether a floating table shall allow other floating objects in the document to overlap its extents when displayed. Default value is  true .

**Returns:**
boolean - Whether a floating table shall allow other floating objects in the document to overlap its extents when displayed.
### setBorders(int lineStyle, double lineWidth, Color color) {#setBorders-int-double-java.awt.Color-}
```
public void setBorders(int lineStyle, double lineWidth, Color color)
```




**Parameters:**
| Parameter | Type | Description |
| --- | --- | --- |
| lineStyle | int |  |
| lineWidth | double |  |
| color | java.awt.Color |  |

### setBorder(int borderType, int lineStyle, double lineWidth, Color color, boolean isOverrideCellBorders) {#setBorder-int-int-double-java.awt.Color-boolean-}
```
public void setBorder(int borderType, int lineStyle, double lineWidth, Color color, boolean isOverrideCellBorders)
```




**Parameters:**
| Parameter | Type | Description |
| --- | --- | --- |
| borderType | int |  |
| lineStyle | int |  |
| lineWidth | double |  |
| color | java.awt.Color |  |
| isOverrideCellBorders | boolean |  |

### clearBorders() {#clearBorders--}
```
public void clearBorders()
```


Removes all table and cell borders on this table.

### setShading(int texture, Color foregroundColor, Color backgroundColor) {#setShading-int-java.awt.Color-java.awt.Color-}
```
public void setShading(int texture, Color foregroundColor, Color backgroundColor)
```




**Parameters:**
| Parameter | Type | Description |
| --- | --- | --- |
| texture | int |  |
| foregroundColor | java.awt.Color |  |
| backgroundColor | java.awt.Color |  |

### clearShading() {#clearShading--}
```
public void clearShading()
```


Removes all shading on the table.

### autoFit(int behavior) {#autoFit-int-}
```
public void autoFit(int behavior)
```




**Parameters:**
| Parameter | Type | Description |
| --- | --- | --- |
| behavior | int |  |

