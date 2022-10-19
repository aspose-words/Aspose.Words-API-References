---
title: CellFormat
second_title: Aspose.Words for Java API Reference
description: Represents all formatting for a table cell.
type: docs
weight: 50
url: /java/com.aspose.words/cellformat/
---

**Inheritance:**
java.lang.Object
```
public class CellFormat
```

Represents all formatting for a table cell.

To learn more, visit the **Working with Tables** documentation article.
## Methods

| Method | Description |
| --- | --- |
| [clearFormatting()](#clearFormatting--) | Resets to default cell formatting. |
| [setPaddings(double leftPadding, double topPadding, double rightPadding, double bottomPadding)](#setPaddings-double-double-double-double-) | Sets the amount of space (in points) to add to the left/top/right/bottom of the contents of cell. |
| [getLeftPadding()](#getLeftPadding--) | Gets the amount of space (in points) to add to the left of the contents of cell. |
| [setLeftPadding(double value)](#setLeftPadding-double-) | Sets the amount of space (in points) to add to the left of the contents of cell. |
| [getRightPadding()](#getRightPadding--) | Gets the amount of space (in points) to add to the right of the contents of cell. |
| [setRightPadding(double value)](#setRightPadding-double-) | Sets the amount of space (in points) to add to the right of the contents of cell. |
| [getTopPadding()](#getTopPadding--) | Gets the amount of space (in points) to add above the contents of cell. |
| [setTopPadding(double value)](#setTopPadding-double-) | Sets the amount of space (in points) to add above the contents of cell. |
| [getBottomPadding()](#getBottomPadding--) | Gets the amount of space (in points) to add below the contents of cell. |
| [setBottomPadding(double value)](#setBottomPadding-double-) | Sets the amount of space (in points) to add below the contents of cell. |
| [getBorders()](#getBorders--) | Gets collection of borders of the cell. |
| [getShading()](#getShading--) | Returns a Shading object that refers to the shading formatting for the cell. |
| [getVerticalAlignment()](#getVerticalAlignment--) | Gets the vertical alignment of text in the cell. |
| [setVerticalAlignment(int value)](#setVerticalAlignment-int-) | Sets the vertical alignment of text in the cell. |
| [getWidth()](#getWidth--) | Gets the width of the cell in points. |
| [setWidth(double value)](#setWidth-double-) | Gets the width of the cell in points. |
| [getPreferredWidth()](#getPreferredWidth--) | Gets the preferred width of the cell. |
| [setPreferredWidth(PreferredWidth value)](#setPreferredWidth-com.aspose.words.PreferredWidth-) | Sets the preferred width of the cell. |
| [getVerticalMerge()](#getVerticalMerge--) | Specifies how the cell is merged with other cells vertically. |
| [setVerticalMerge(int value)](#setVerticalMerge-int-) | Specifies how the cell is merged with other cells vertically. |
| [getHorizontalMerge()](#getHorizontalMerge--) | Specifies how the cell is merged horizontally with other cells in the row. |
| [setHorizontalMerge(int value)](#setHorizontalMerge-int-) | Specifies how the cell is merged horizontally with other cells in the row. |
| [getOrientation()](#getOrientation--) | Gets the orientation of text in a table cell. |
| [setOrientation(int value)](#setOrientation-int-) | Sets the orientation of text in a table cell. |
| [getFitText()](#getFitText--) | If true, fits text in the cell, compressing each paragraph to the width of the cell. |
| [setFitText(boolean value)](#setFitText-boolean-) | If true, fits text in the cell, compressing each paragraph to the width of the cell. |
| [getWrapText()](#getWrapText--) | If true, wrap text for the cell. |
| [setWrapText(boolean value)](#setWrapText-boolean-) | If true, wrap text for the cell. |
| [getDirectBorderAttr(int key)](#getDirectBorderAttr-int-) |  |
| [fetchInheritedBorderAttr(int key)](#fetchInheritedBorderAttr-int-) |  |
| [setBorderAttr(int key, Object value)](#setBorderAttr-int-java.lang.Object-) |  |
| [fetchInheritedShadingAttr(int key)](#fetchInheritedShadingAttr-int-) |  |
### clearFormatting() {#clearFormatting--}
```
public void clearFormatting()
```


Resets to default cell formatting. Does not change the width of the cell.

### setPaddings(double leftPadding, double topPadding, double rightPadding, double bottomPadding) {#setPaddings-double-double-double-double-}
```
public void setPaddings(double leftPadding, double topPadding, double rightPadding, double bottomPadding)
```


Sets the amount of space (in points) to add to the left/top/right/bottom of the contents of cell.

**Parameters:**
| Parameter | Type | Description |
| --- | --- | --- |
| leftPadding | double |  |
| topPadding | double |  |
| rightPadding | double |  |
| bottomPadding | double |  |

### getLeftPadding() {#getLeftPadding--}
```
public double getLeftPadding()
```


Gets the amount of space (in points) to add to the left of the contents of cell.

**Returns:**
double - The amount of space (in points) to add to the left of the contents of cell.
### setLeftPadding(double value) {#setLeftPadding-double-}
```
public void setLeftPadding(double value)
```


Sets the amount of space (in points) to add to the left of the contents of cell.

**Parameters:**
| Parameter | Type | Description |
| --- | --- | --- |
| value | double | The amount of space (in points) to add to the left of the contents of cell. |

### getRightPadding() {#getRightPadding--}
```
public double getRightPadding()
```


Gets the amount of space (in points) to add to the right of the contents of cell.

**Returns:**
double - The amount of space (in points) to add to the right of the contents of cell.
### setRightPadding(double value) {#setRightPadding-double-}
```
public void setRightPadding(double value)
```


Sets the amount of space (in points) to add to the right of the contents of cell.

**Parameters:**
| Parameter | Type | Description |
| --- | --- | --- |
| value | double | The amount of space (in points) to add to the right of the contents of cell. |

### getTopPadding() {#getTopPadding--}
```
public double getTopPadding()
```


Gets the amount of space (in points) to add above the contents of cell.

**Returns:**
double - The amount of space (in points) to add above the contents of cell.
### setTopPadding(double value) {#setTopPadding-double-}
```
public void setTopPadding(double value)
```


Sets the amount of space (in points) to add above the contents of cell.

**Parameters:**
| Parameter | Type | Description |
| --- | --- | --- |
| value | double | The amount of space (in points) to add above the contents of cell. |

### getBottomPadding() {#getBottomPadding--}
```
public double getBottomPadding()
```


Gets the amount of space (in points) to add below the contents of cell.

**Returns:**
double - The amount of space (in points) to add below the contents of cell.
### setBottomPadding(double value) {#setBottomPadding-double-}
```
public void setBottomPadding(double value)
```


Sets the amount of space (in points) to add below the contents of cell.

**Parameters:**
| Parameter | Type | Description |
| --- | --- | --- |
| value | double | The amount of space (in points) to add below the contents of cell. |

### getBorders() {#getBorders--}
```
public BorderCollection getBorders()
```


Gets collection of borders of the cell.

**Returns:**
[BorderCollection](../../com.aspose.words/bordercollection) - Collection of borders of the cell.
### getShading() {#getShading--}
```
public Shading getShading()
```


Returns a Shading object that refers to the shading formatting for the cell.

**Returns:**
[Shading](../../com.aspose.words/shading) - A Shading object that refers to the shading formatting for the cell.
### getVerticalAlignment() {#getVerticalAlignment--}
```
public int getVerticalAlignment()
```


Gets the vertical alignment of text in the cell.

**Returns:**
int - The vertical alignment of text in the cell. The returned value is one of [CellVerticalAlignment](../../com.aspose.words/cellverticalalignment) constants.
### setVerticalAlignment(int value) {#setVerticalAlignment-int-}
```
public void setVerticalAlignment(int value)
```


Sets the vertical alignment of text in the cell.

**Parameters:**
| Parameter | Type | Description |
| --- | --- | --- |
| value | int | The vertical alignment of text in the cell. The value must be one of [CellVerticalAlignment](../../com.aspose.words/cellverticalalignment) constants. |

### getWidth() {#getWidth--}
```
public double getWidth()
```


Gets the width of the cell in points.

The width is calculated by Aspose.Words on document loading and saving. Currently, not every combination of table, cell and document properties is supported. The returned value may not be accurate for some documents. It may not exactly match the cell width as calculated by MS Word when the document is opened in MS Word.

Setting this property is not recommended. There is no guarantee that the cell will actually have the set width. The width may be adjusted to accommodate cell contents in an auto-fit table layout. Cells in other rows may have conflicting width settings. The table may be resized to fit into the container or to meet table width settings. Consider using [getPreferredWidth()](../../com.aspose.words/cellformat\#getPreferredWidth--) / [setPreferredWidth(com.aspose.words.PreferredWidth)](../../com.aspose.words/cellformat\#setPreferredWidth-com.aspose.words.PreferredWidth-) for setting the cell width. Setting this property sets [getPreferredWidth()](../../com.aspose.words/cellformat\#getPreferredWidth--) / [setPreferredWidth(com.aspose.words.PreferredWidth)](../../com.aspose.words/cellformat\#setPreferredWidth-com.aspose.words.PreferredWidth-) implicitly since version 15.8.

**Returns:**
double - The width of the cell in points.
### setWidth(double value) {#setWidth-double-}
```
public void setWidth(double value)
```


Gets the width of the cell in points.

The width is calculated by Aspose.Words on document loading and saving. Currently, not every combination of table, cell and document properties is supported. The returned value may not be accurate for some documents. It may not exactly match the cell width as calculated by MS Word when the document is opened in MS Word.

Setting this property is not recommended. There is no guarantee that the cell will actually have the set width. The width may be adjusted to accommodate cell contents in an auto-fit table layout. Cells in other rows may have conflicting width settings. The table may be resized to fit into the container or to meet table width settings. Consider using [getPreferredWidth()](../../com.aspose.words/cellformat\#getPreferredWidth--) / [setPreferredWidth(com.aspose.words.PreferredWidth)](../../com.aspose.words/cellformat\#setPreferredWidth-com.aspose.words.PreferredWidth-) for setting the cell width. Setting this property sets [getPreferredWidth()](../../com.aspose.words/cellformat\#getPreferredWidth--) / [setPreferredWidth(com.aspose.words.PreferredWidth)](../../com.aspose.words/cellformat\#setPreferredWidth-com.aspose.words.PreferredWidth-) implicitly since version 15.8.

**Parameters:**
| Parameter | Type | Description |
| --- | --- | --- |
| value | double | The width of the cell in points. |

### getPreferredWidth() {#getPreferredWidth--}
```
public PreferredWidth getPreferredWidth()
```


Gets the preferred width of the cell.

The preferred width (along with the table's Auto Fit option) determines how the actual width of the cell is calculated by the table layout algorithm. Table layout can be performed by Aspose.Words when it saves the document or by Microsoft Word when it displays the document.

The preferred width can be specified in points or in percent. The preferred width can also be specified as "auto", which means no preferred width is specified.

The default value is [PreferredWidth.AUTO](../../com.aspose.words/preferredwidth\#AUTO).

**Returns:**
[PreferredWidth](../../com.aspose.words/preferredwidth) - The preferred width of the cell.
### setPreferredWidth(PreferredWidth value) {#setPreferredWidth-com.aspose.words.PreferredWidth-}
```
public void setPreferredWidth(PreferredWidth value)
```


Sets the preferred width of the cell.

The preferred width (along with the table's Auto Fit option) determines how the actual width of the cell is calculated by the table layout algorithm. Table layout can be performed by Aspose.Words when it saves the document or by Microsoft Word when it displays the document.

The preferred width can be specified in points or in percent. The preferred width can also be specified as "auto", which means no preferred width is specified.

The default value is [PreferredWidth.AUTO](../../com.aspose.words/preferredwidth\#AUTO).

**Parameters:**
| Parameter | Type | Description |
| --- | --- | --- |
| value | [PreferredWidth](../../com.aspose.words/preferredwidth) | The preferred width of the cell. |

### getVerticalMerge() {#getVerticalMerge--}
```
public int getVerticalMerge()
```


Specifies how the cell is merged with other cells vertically.

Cells can only be merged vertically if their left and right boundaries are identical.

When cells are vertically merged, the display areas of the merged cells are consolidated. The consolidated area is used to display the contents of the first vertically merged cell and all other vertically merged cells must be empty.

**Returns:**
int - The corresponding  int  value. The returned value is one of [CellMerge](../../com.aspose.words/cellmerge) constants.
### setVerticalMerge(int value) {#setVerticalMerge-int-}
```
public void setVerticalMerge(int value)
```


Specifies how the cell is merged with other cells vertically.

Cells can only be merged vertically if their left and right boundaries are identical.

When cells are vertically merged, the display areas of the merged cells are consolidated. The consolidated area is used to display the contents of the first vertically merged cell and all other vertically merged cells must be empty.

**Parameters:**
| Parameter | Type | Description |
| --- | --- | --- |
| value | int | The corresponding  int  value. The value must be one of [CellMerge](../../com.aspose.words/cellmerge) constants. |

### getHorizontalMerge() {#getHorizontalMerge--}
```
public int getHorizontalMerge()
```


Specifies how the cell is merged horizontally with other cells in the row.

**Returns:**
int - The corresponding  int  value. The returned value is one of [CellMerge](../../com.aspose.words/cellmerge) constants.
### setHorizontalMerge(int value) {#setHorizontalMerge-int-}
```
public void setHorizontalMerge(int value)
```


Specifies how the cell is merged horizontally with other cells in the row.

**Parameters:**
| Parameter | Type | Description |
| --- | --- | --- |
| value | int | The corresponding  int  value. The value must be one of [CellMerge](../../com.aspose.words/cellmerge) constants. |

### getOrientation() {#getOrientation--}
```
public int getOrientation()
```


Gets the orientation of text in a table cell.

**Returns:**
int - The orientation of text in a table cell. The returned value is one of [TextOrientation](../../com.aspose.words/textorientation) constants.
### setOrientation(int value) {#setOrientation-int-}
```
public void setOrientation(int value)
```


Sets the orientation of text in a table cell.

**Parameters:**
| Parameter | Type | Description |
| --- | --- | --- |
| value | int | The orientation of text in a table cell. The value must be one of [TextOrientation](../../com.aspose.words/textorientation) constants. |

### getFitText() {#getFitText--}
```
public boolean getFitText()
```


If true, fits text in the cell, compressing each paragraph to the width of the cell.

**Returns:**
boolean - The corresponding  boolean  value.
### setFitText(boolean value) {#setFitText-boolean-}
```
public void setFitText(boolean value)
```


If true, fits text in the cell, compressing each paragraph to the width of the cell.

**Parameters:**
| Parameter | Type | Description |
| --- | --- | --- |
| value | boolean | The corresponding  boolean  value. |

### getWrapText() {#getWrapText--}
```
public boolean getWrapText()
```


If true, wrap text for the cell.

**Returns:**
boolean - The corresponding  boolean  value.
### setWrapText(boolean value) {#setWrapText-boolean-}
```
public void setWrapText(boolean value)
```


If true, wrap text for the cell.

**Parameters:**
| Parameter | Type | Description |
| --- | --- | --- |
| value | boolean | The corresponding  boolean  value. |

### getDirectBorderAttr(int key) {#getDirectBorderAttr-int-}
```
public Object getDirectBorderAttr(int key)
```




**Parameters:**
| Parameter | Type | Description |
| --- | --- | --- |
| key | int |  |

**Returns:**
java.lang.Object
### fetchInheritedBorderAttr(int key) {#fetchInheritedBorderAttr-int-}
```
public Object fetchInheritedBorderAttr(int key)
```




**Parameters:**
| Parameter | Type | Description |
| --- | --- | --- |
| key | int |  |

**Returns:**
java.lang.Object
### setBorderAttr(int key, Object value) {#setBorderAttr-int-java.lang.Object-}
```
public void setBorderAttr(int key, Object value)
```




**Parameters:**
| Parameter | Type | Description |
| --- | --- | --- |
| key | int |  |
| value | java.lang.Object |  |

### fetchInheritedShadingAttr(int key) {#fetchInheritedShadingAttr-int-}
```
public Object fetchInheritedShadingAttr(int key)
```




**Parameters:**
| Parameter | Type | Description |
| --- | --- | --- |
| key | int |  |

**Returns:**
java.lang.Object
