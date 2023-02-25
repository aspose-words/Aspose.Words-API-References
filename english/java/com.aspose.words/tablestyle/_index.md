---
title: TableStyle
linktitle: TableStyle
second_title: Aspose.Words for Java API Reference
description: Represents a table style in Java.
type: docs
weight: 558
url: /java/com.aspose.words/tablestyle/
---

**Inheritance:**
java.lang.Object, [com.aspose.words.Style](../../com.aspose.words/style/)
```
public class TableStyle extends Style
```

Represents a table style.

To learn more, visit the [ Working with Tables ][Working with Tables] documentation article.


[Working with Tables]: https://docs.aspose.com/words/java/working-with-tables/
## Methods

| Method | Description |
| --- | --- |
| [clearCellAttrs()](#clearCellAttrs) |  |
| [clearParaAttrs()](#clearParaAttrs) |  |
| [clearRowAttrs()](#clearRowAttrs) |  |
| [clearRunAttrs()](#clearRunAttrs) |  |
| [equals(Style style)](#equals-com.aspose.words.Style) | Compares with the specified style. |
| [equals(Object arg0)](#equals-java.lang.Object) |  |
| [fetchCellAttr(int key)](#fetchCellAttr-int) |  |
| [fetchInheritedBorderAttr(int key)](#fetchInheritedBorderAttr-int) |  |
| [fetchInheritedCellAttr(int key)](#fetchInheritedCellAttr-int) |  |
| [fetchInheritedParaAttr(int key)](#fetchInheritedParaAttr-int) |  |
| [fetchInheritedRowAttr(int key)](#fetchInheritedRowAttr-int) |  |
| [fetchInheritedRunAttr(int key)](#fetchInheritedRunAttr-int) |  |
| [fetchInheritedShadingAttr(int key)](#fetchInheritedShadingAttr-int) |  |
| [fetchParaAttr(int key)](#fetchParaAttr-int) |  |
| [fetchRowAttr(int key)](#fetchRowAttr-int) |  |
| [getAliases()](#getAliases) | Gets all aliases of this style. |
| [getAlignment()](#getAlignment) | Specifies the alignment for the table style. |
| [getAllowBreakAcrossPages()](#getAllowBreakAcrossPages) | Gets a flag indicating whether text in a table row is allowed to split across a page break. |
| [getAutomaticallyUpdate()](#getAutomaticallyUpdate) | Specifies whether this style is automatically redefined based on the appropriate value. |
| [getBaseStyleName()](#getBaseStyleName) | Gets/sets the name of the style this style is based on. |
| [getBidi()](#getBidi) | Gets whether this is a style for a right-to-left table. |
| [getBorders()](#getBorders) | Gets the collection of default cell borders for the style. |
| [getBottomPadding()](#getBottomPadding) | Gets the amount of space (in points) to add below the contents of table cells. |
| [getBuiltIn()](#getBuiltIn) | True if this style is one of the built-in styles in MS Word. |
| [getCellSpacing()](#getCellSpacing) | Gets the amount of space (in points) between the cells. |
| [getClass()](#getClass) |  |
| [getColumnStripe()](#getColumnStripe) | Gets a number of columns to include in the banding when the style specifies odd/even columns banding. |
| [getConditionalStyles()](#getConditionalStyles) | Collection of conditional styles that may be defined for this table style. |
| [getDirectBorderAttr(int key)](#getDirectBorderAttr-int) |  |
| [getDirectCellAttr(int key)](#getDirectCellAttr-int) |  |
| [getDirectParaAttr(int key)](#getDirectParaAttr-int) |  |
| [getDirectParaAttr(int key, int revisionsView)](#getDirectParaAttr-int-int) |  |
| [getDirectRowAttr(int key)](#getDirectRowAttr-int) |  |
| [getDirectRunAttr(int key)](#getDirectRunAttr-int) |  |
| [getDirectRunAttr(int key, int revisionsView)](#getDirectRunAttr-int-int) |  |
| [getDocument()](#getDocument) | Gets the owner document. |
| [getFont()](#getFont) | Gets the character formatting of the style. |
| [getLeftIndent()](#getLeftIndent) | Gets the value that represents the left indent of a table. |
| [getLeftPadding()](#getLeftPadding) | Gets the amount of space (in points) to add to the left of the contents of table cells. |
| [getLinkedStyleName()](#getLinkedStyleName) | Gets the name of the [Style](../../com.aspose.words/style/) linked to this one. |
| [getList()](#getList) | Gets the list that defines formatting of this list style. |
| [getListFormat()](#getListFormat) | Provides access to the list formatting properties of a paragraph style. |
| [getName()](#getName) | Gets the name of the style. |
| [getNextParagraphStyleName()](#getNextParagraphStyleName) | Gets/sets the name of the style to be applied automatically to a new paragraph inserted after a paragraph formatted with the specified style. |
| [getParagraphFormat()](#getParagraphFormat) | Gets the paragraph formatting of the style. |
| [getRightPadding()](#getRightPadding) | Gets the amount of space (in points) to add to the right of the contents of table cells. |
| [getRowStripe()](#getRowStripe) | Gets a number of rows to include in the banding when the style specifies odd/even row banding. |
| [getShading()](#getShading) | Gets a [Shading](../../com.aspose.words/shading/) object that refers to the shading formatting for table cells. |
| [getStyleIdentifier()](#getStyleIdentifier) | Gets the locale independent style identifier for a built-in style. |
| [getStyles()](#getStyles) | Gets the collection of styles this style belongs to. |
| [getTopPadding()](#getTopPadding) | Gets the amount of space (in points) to add above the contents of table cells. |
| [getType()](#getType) | Gets the style type (paragraph or character). |
| [getVerticalAlignment()](#getVerticalAlignment) | Specifies the vertical alignment for the cells. |
| [hashCode()](#hashCode) |  |
| [isHeading()](#isHeading) | True when the style is one of the built-in Heading styles. |
| [isQuickStyle()](#isQuickStyle) | Specifies whether this style is shown in the Quick Style gallery inside MS Word UI. |
| [isQuickStyle(boolean value)](#isQuickStyle-boolean) | Specifies whether this style is shown in the Quick Style gallery inside MS Word UI. |
| [notify()](#notify) |  |
| [notifyAll()](#notifyAll) |  |
| [remove()](#remove) | Removes the specified style from the document. |
| [removeParaAttr(int key)](#removeParaAttr-int) |  |
| [removeRunAttr(int key)](#removeRunAttr-int) |  |
| [resetToDefaultAttrs()](#resetToDefaultAttrs) |  |
| [setAlignment(int value)](#setAlignment-int) | Specifies the alignment for the table style. |
| [setAllowBreakAcrossPages(boolean value)](#setAllowBreakAcrossPages-boolean) | Sets a flag indicating whether text in a table row is allowed to split across a page break. |
| [setAutomaticallyUpdate(boolean value)](#setAutomaticallyUpdate-boolean) | Specifies whether this style is automatically redefined based on the appropriate value. |
| [setBaseStyleName(String value)](#setBaseStyleName-java.lang.String) | Gets/sets the name of the style this style is based on. |
| [setBidi(boolean value)](#setBidi-boolean) | Sets whether this is a style for a right-to-left table. |
| [setBorderAttr(int key, Object value)](#setBorderAttr-int-java.lang.Object) |  |
| [setBottomPadding(double value)](#setBottomPadding-double) | Sets the amount of space (in points) to add below the contents of table cells. |
| [setCellAttr(int key, Object value)](#setCellAttr-int-java.lang.Object) |  |
| [setCellSpacing(double value)](#setCellSpacing-double) | Sets the amount of space (in points) between the cells. |
| [setColumnStripe(int value)](#setColumnStripe-int) | Sets a number of columns to include in the banding when the style specifies odd/even columns banding. |
| [setLeftIndent(double value)](#setLeftIndent-double) | Sets the value that represents the left indent of a table. |
| [setLeftPadding(double value)](#setLeftPadding-double) | Sets the amount of space (in points) to add to the left of the contents of table cells. |
| [setName(String value)](#setName-java.lang.String) | Sets the name of the style. |
| [setNextParagraphStyleName(String value)](#setNextParagraphStyleName-java.lang.String) | Gets/sets the name of the style to be applied automatically to a new paragraph inserted after a paragraph formatted with the specified style. |
| [setParaAttr(int key, Object value)](#setParaAttr-int-java.lang.Object) |  |
| [setRightPadding(double value)](#setRightPadding-double) | Sets the amount of space (in points) to add to the right of the contents of table cells. |
| [setRowAttr(int key, Object value)](#setRowAttr-int-java.lang.Object) |  |
| [setRowStripe(int value)](#setRowStripe-int) | Sets a number of rows to include in the banding when the style specifies odd/even row banding. |
| [setRunAttr(int key, Object value)](#setRunAttr-int-java.lang.Object) |  |
| [setTopPadding(double value)](#setTopPadding-double) | Sets the amount of space (in points) to add above the contents of table cells. |
| [setVerticalAlignment(int value)](#setVerticalAlignment-int) | Specifies the vertical alignment for the cells. |
| [toString()](#toString) |  |
| [wait()](#wait) |  |
| [wait(long arg0)](#wait-long) |  |
| [wait(long arg0, int arg1)](#wait-long-int) |  |
### clearCellAttrs() {#clearCellAttrs}
```
public void clearCellAttrs()
```




### clearParaAttrs() {#clearParaAttrs}
```
public void clearParaAttrs()
```




### clearRowAttrs() {#clearRowAttrs}
```
public void clearRowAttrs()
```




### clearRunAttrs() {#clearRunAttrs}
```
public void clearRunAttrs()
```




### equals(Style style) {#equals-com.aspose.words.Style}
```
public boolean equals(Style style)
```


Compares with the specified style. Styles Istds are compared for built-in styles only. Styles defaults are not included in comparison. Base style, linked style and next paragraph style are recursively compared.

**Parameters:**
| Parameter | Type | Description |
| --- | --- | --- |
| style | [Style](../../com.aspose.words/style/) |  |

**Returns:**
boolean
### equals(Object arg0) {#equals-java.lang.Object}
```
public boolean equals(Object arg0)
```




**Parameters:**
| Parameter | Type | Description |
| --- | --- | --- |
| arg0 | java.lang.Object |  |

**Returns:**
boolean
### fetchCellAttr(int key) {#fetchCellAttr-int}
```
public Object fetchCellAttr(int key)
```




**Parameters:**
| Parameter | Type | Description |
| --- | --- | --- |
| key | int |  |

**Returns:**
java.lang.Object
### fetchInheritedBorderAttr(int key) {#fetchInheritedBorderAttr-int}
```
public Object fetchInheritedBorderAttr(int key)
```




**Parameters:**
| Parameter | Type | Description |
| --- | --- | --- |
| key | int |  |

**Returns:**
java.lang.Object
### fetchInheritedCellAttr(int key) {#fetchInheritedCellAttr-int}
```
public Object fetchInheritedCellAttr(int key)
```




**Parameters:**
| Parameter | Type | Description |
| --- | --- | --- |
| key | int |  |

**Returns:**
java.lang.Object
### fetchInheritedParaAttr(int key) {#fetchInheritedParaAttr-int}
```
public Object fetchInheritedParaAttr(int key)
```




**Parameters:**
| Parameter | Type | Description |
| --- | --- | --- |
| key | int |  |

**Returns:**
java.lang.Object
### fetchInheritedRowAttr(int key) {#fetchInheritedRowAttr-int}
```
public Object fetchInheritedRowAttr(int key)
```




**Parameters:**
| Parameter | Type | Description |
| --- | --- | --- |
| key | int |  |

**Returns:**
java.lang.Object
### fetchInheritedRunAttr(int key) {#fetchInheritedRunAttr-int}
```
public Object fetchInheritedRunAttr(int key)
```




**Parameters:**
| Parameter | Type | Description |
| --- | --- | --- |
| key | int |  |

**Returns:**
java.lang.Object
### fetchInheritedShadingAttr(int key) {#fetchInheritedShadingAttr-int}
```
public Object fetchInheritedShadingAttr(int key)
```




**Parameters:**
| Parameter | Type | Description |
| --- | --- | --- |
| key | int |  |

**Returns:**
java.lang.Object
### fetchParaAttr(int key) {#fetchParaAttr-int}
```
public Object fetchParaAttr(int key)
```




**Parameters:**
| Parameter | Type | Description |
| --- | --- | --- |
| key | int |  |

**Returns:**
java.lang.Object
### fetchRowAttr(int key) {#fetchRowAttr-int}
```
public Object fetchRowAttr(int key)
```




**Parameters:**
| Parameter | Type | Description |
| --- | --- | --- |
| key | int |  |

**Returns:**
java.lang.Object
### getAliases() {#getAliases}
```
public String[] getAliases()
```


Gets all aliases of this style. If style has no aliases then empty array of string is returned.

**Returns:**
java.lang.String[] - All aliases of this style.
### getAlignment() {#getAlignment}
```
public int getAlignment()
```


Specifies the alignment for the table style. The default value is [TableAlignment.LEFT](../../com.aspose.words/tablealignment/\#LEFT).

**Returns:**
int - The corresponding  int  value. The returned value is one of [TableAlignment](../../com.aspose.words/tablealignment/) constants.
### getAllowBreakAcrossPages() {#getAllowBreakAcrossPages}
```
public boolean getAllowBreakAcrossPages()
```


Gets a flag indicating whether text in a table row is allowed to split across a page break. The default value is  true .

**Returns:**
boolean - A flag indicating whether text in a table row is allowed to split across a page break.
### getAutomaticallyUpdate() {#getAutomaticallyUpdate}
```
public boolean getAutomaticallyUpdate()
```


Specifies whether this style is automatically redefined based on the appropriate value.

If the property value is set to true, MS Word automatically redefines the current style when the appropriate paragraph formatting has been changed.

AutomaticallyUpdate property is applicable to paragraph styles only.

The default value is  false .

**Returns:**
boolean - The corresponding  boolean  value.
### getBaseStyleName() {#getBaseStyleName}
```
public String getBaseStyleName()
```


Gets/sets the name of the style this style is based on. This will be an empty string if the style is not based on any other style and it can be set to an empty string.

**Returns:**
java.lang.String - The corresponding java.lang.String value.
### getBidi() {#getBidi}
```
public boolean getBidi()
```


Gets whether this is a style for a right-to-left table.

When  true , the cells in rows are laid out right to left.

The default value is  false .

**Returns:**
boolean - Whether this is a style for a right-to-left table.
### getBorders() {#getBorders}
```
public BorderCollection getBorders()
```


Gets the collection of default cell borders for the style.

**Returns:**
[BorderCollection](../../com.aspose.words/bordercollection/) - The collection of default cell borders for the style.
### getBottomPadding() {#getBottomPadding}
```
public double getBottomPadding()
```


Gets the amount of space (in points) to add below the contents of table cells.

**Returns:**
double - The amount of space (in points) to add below the contents of table cells.
### getBuiltIn() {#getBuiltIn}
```
public boolean getBuiltIn()
```


True if this style is one of the built-in styles in MS Word.

**Returns:**
boolean - The corresponding  boolean  value.
### getCellSpacing() {#getCellSpacing}
```
public double getCellSpacing()
```


Gets the amount of space (in points) between the cells.

**Returns:**
double - The amount of space (in points) between the cells.
### getClass() {#getClass}
```
public final native Class<?> getClass()
```




**Returns:**
java.lang.Class<?>
### getColumnStripe() {#getColumnStripe}
```
public int getColumnStripe()
```


Gets a number of columns to include in the banding when the style specifies odd/even columns banding.

**Returns:**
int - A number of columns to include in the banding when the style specifies odd/even columns banding.
### getConditionalStyles() {#getConditionalStyles}
```
public ConditionalStyleCollection getConditionalStyles()
```


Collection of conditional styles that may be defined for this table style.

**Returns:**
[ConditionalStyleCollection](../../com.aspose.words/conditionalstylecollection/) - The corresponding [ConditionalStyleCollection](../../com.aspose.words/conditionalstylecollection/) value.
### getDirectBorderAttr(int key) {#getDirectBorderAttr-int}
```
public Object getDirectBorderAttr(int key)
```




**Parameters:**
| Parameter | Type | Description |
| --- | --- | --- |
| key | int |  |

**Returns:**
java.lang.Object
### getDirectCellAttr(int key) {#getDirectCellAttr-int}
```
public Object getDirectCellAttr(int key)
```




**Parameters:**
| Parameter | Type | Description |
| --- | --- | --- |
| key | int |  |

**Returns:**
java.lang.Object
### getDirectParaAttr(int key) {#getDirectParaAttr-int}
```
public Object getDirectParaAttr(int key)
```




**Parameters:**
| Parameter | Type | Description |
| --- | --- | --- |
| key | int |  |

**Returns:**
java.lang.Object
### getDirectParaAttr(int key, int revisionsView) {#getDirectParaAttr-int-int}
```
public Object getDirectParaAttr(int key, int revisionsView)
```




**Parameters:**
| Parameter | Type | Description |
| --- | --- | --- |
| key | int |  |
| revisionsView | int |  |

**Returns:**
java.lang.Object
### getDirectRowAttr(int key) {#getDirectRowAttr-int}
```
public Object getDirectRowAttr(int key)
```




**Parameters:**
| Parameter | Type | Description |
| --- | --- | --- |
| key | int |  |

**Returns:**
java.lang.Object
### getDirectRunAttr(int key) {#getDirectRunAttr-int}
```
public Object getDirectRunAttr(int key)
```




**Parameters:**
| Parameter | Type | Description |
| --- | --- | --- |
| key | int |  |

**Returns:**
java.lang.Object
### getDirectRunAttr(int key, int revisionsView) {#getDirectRunAttr-int-int}
```
public Object getDirectRunAttr(int key, int revisionsView)
```




**Parameters:**
| Parameter | Type | Description |
| --- | --- | --- |
| key | int |  |
| revisionsView | int |  |

**Returns:**
java.lang.Object
### getDocument() {#getDocument}
```
public DocumentBase getDocument()
```


Gets the owner document.

**Returns:**
[DocumentBase](../../com.aspose.words/documentbase/) - The owner document.
### getFont() {#getFont}
```
public Font getFont()
```


Gets the character formatting of the style.

For list styles this property returns  null .

**Returns:**
[Font](../../com.aspose.words/font/) - The character formatting of the style.
### getLeftIndent() {#getLeftIndent}
```
public double getLeftIndent()
```


Gets the value that represents the left indent of a table.

**Returns:**
double - The value that represents the left indent of a table.
### getLeftPadding() {#getLeftPadding}
```
public double getLeftPadding()
```


Gets the amount of space (in points) to add to the left of the contents of table cells.

**Returns:**
double - The amount of space (in points) to add to the left of the contents of table cells.
### getLinkedStyleName() {#getLinkedStyleName}
```
public String getLinkedStyleName()
```


Gets the name of the [Style](../../com.aspose.words/style/) linked to this one. Returns empty string if no styles are linked.

**Returns:**
java.lang.String - The name of the [Style](../../com.aspose.words/style/) linked to this one.
### getList() {#getList}
```
public List getList()
```


Gets the list that defines formatting of this list style.

This property is only valid for list styles. For other style types this property returns  null .

**Returns:**
[List](../../com.aspose.words/list/) - The list that defines formatting of this list style.
### getListFormat() {#getListFormat}
```
public ListFormat getListFormat()
```


Provides access to the list formatting properties of a paragraph style.

This property is only valid for paragraph styles. For other style types this property returns  null .

**Returns:**
[ListFormat](../../com.aspose.words/listformat/) - The corresponding [ListFormat](../../com.aspose.words/listformat/) value.
### getName() {#getName}
```
public String getName()
```


Gets the name of the style.

Can not be empty string.

If there already is a style with such name in the collection, then this style will override it. All affected nodes will reference new style.

**Returns:**
java.lang.String - The name of the style.
### getNextParagraphStyleName() {#getNextParagraphStyleName}
```
public String getNextParagraphStyleName()
```


Gets/sets the name of the style to be applied automatically to a new paragraph inserted after a paragraph formatted with the specified style. This property is not used by Aspose.Words. The next paragraph style will only be applied automatically when you edit the document in MS Word.

**Returns:**
java.lang.String - The corresponding java.lang.String value.
### getParagraphFormat() {#getParagraphFormat}
```
public ParagraphFormat getParagraphFormat()
```


Gets the paragraph formatting of the style.

For character and list styles this property returns  null .

**Returns:**
[ParagraphFormat](../../com.aspose.words/paragraphformat/) - The paragraph formatting of the style.
### getRightPadding() {#getRightPadding}
```
public double getRightPadding()
```


Gets the amount of space (in points) to add to the right of the contents of table cells.

**Returns:**
double - The amount of space (in points) to add to the right of the contents of table cells.
### getRowStripe() {#getRowStripe}
```
public int getRowStripe()
```


Gets a number of rows to include in the banding when the style specifies odd/even row banding.

**Returns:**
int - A number of rows to include in the banding when the style specifies odd/even row banding.
### getShading() {#getShading}
```
public Shading getShading()
```


Gets a [Shading](../../com.aspose.words/shading/) object that refers to the shading formatting for table cells.

**Returns:**
[Shading](../../com.aspose.words/shading/) - A [Shading](../../com.aspose.words/shading/) object that refers to the shading formatting for table cells.
### getStyleIdentifier() {#getStyleIdentifier}
```
public int getStyleIdentifier()
```


Gets the locale independent style identifier for a built-in style.

For user defined (custom) styles, this property returns [StyleIdentifier.USER](../../com.aspose.words/styleidentifier/\#USER).

**Returns:**
int - The locale independent style identifier for a built-in style. The returned value is one of [StyleIdentifier](../../com.aspose.words/styleidentifier/) constants.
### getStyles() {#getStyles}
```
public StyleCollection getStyles()
```


Gets the collection of styles this style belongs to.

**Returns:**
[StyleCollection](../../com.aspose.words/stylecollection/) - The collection of styles this style belongs to.
### getTopPadding() {#getTopPadding}
```
public double getTopPadding()
```


Gets the amount of space (in points) to add above the contents of table cells.

**Returns:**
double - The amount of space (in points) to add above the contents of table cells.
### getType() {#getType}
```
public int getType()
```


Gets the style type (paragraph or character).

**Returns:**
int - The style type (paragraph or character). The returned value is one of [StyleType](../../com.aspose.words/styletype/) constants.
### getVerticalAlignment() {#getVerticalAlignment}
```
public int getVerticalAlignment()
```


Specifies the vertical alignment for the cells. The default value is [CellVerticalAlignment.TOP](../../com.aspose.words/cellverticalalignment/\#TOP).

**Returns:**
int - The corresponding  int  value. The returned value is one of [CellVerticalAlignment](../../com.aspose.words/cellverticalalignment/) constants.
### hashCode() {#hashCode}
```
public native int hashCode()
```




**Returns:**
int
### isHeading() {#isHeading}
```
public boolean isHeading()
```


True when the style is one of the built-in Heading styles.

**Returns:**
boolean - The corresponding  boolean  value.
### isQuickStyle() {#isQuickStyle}
```
public boolean isQuickStyle()
```


Specifies whether this style is shown in the Quick Style gallery inside MS Word UI.

**Returns:**
boolean - The corresponding  boolean  value.
### isQuickStyle(boolean value) {#isQuickStyle-boolean}
```
public void isQuickStyle(boolean value)
```


Specifies whether this style is shown in the Quick Style gallery inside MS Word UI.

**Parameters:**
| Parameter | Type | Description |
| --- | --- | --- |
| value | boolean | The corresponding  boolean  value. |

### notify() {#notify}
```
public final native void notify()
```




### notifyAll() {#notifyAll}
```
public final native void notifyAll()
```




### remove() {#remove}
```
public void remove()
```


Removes the specified style from the document. Style removal has following effects on the document model:

 *  All references to the style are removed from corresponding paragraphs, runs and tables.
 *  If base style is removed its formatting is moved to child styles.
 *  If style to be deleted has a linked style, then both of these are deleted.

### removeParaAttr(int key) {#removeParaAttr-int}
```
public void removeParaAttr(int key)
```




**Parameters:**
| Parameter | Type | Description |
| --- | --- | --- |
| key | int |  |

### removeRunAttr(int key) {#removeRunAttr-int}
```
public void removeRunAttr(int key)
```




**Parameters:**
| Parameter | Type | Description |
| --- | --- | --- |
| key | int |  |

### resetToDefaultAttrs() {#resetToDefaultAttrs}
```
public void resetToDefaultAttrs()
```




### setAlignment(int value) {#setAlignment-int}
```
public void setAlignment(int value)
```


Specifies the alignment for the table style. The default value is [TableAlignment.LEFT](../../com.aspose.words/tablealignment/\#LEFT).

**Parameters:**
| Parameter | Type | Description |
| --- | --- | --- |
| value | int | The corresponding  int  value. The value must be one of [TableAlignment](../../com.aspose.words/tablealignment/) constants. |

### setAllowBreakAcrossPages(boolean value) {#setAllowBreakAcrossPages-boolean}
```
public void setAllowBreakAcrossPages(boolean value)
```


Sets a flag indicating whether text in a table row is allowed to split across a page break. The default value is  true .

**Parameters:**
| Parameter | Type | Description |
| --- | --- | --- |
| value | boolean | A flag indicating whether text in a table row is allowed to split across a page break. |

### setAutomaticallyUpdate(boolean value) {#setAutomaticallyUpdate-boolean}
```
public void setAutomaticallyUpdate(boolean value)
```


Specifies whether this style is automatically redefined based on the appropriate value.

If the property value is set to true, MS Word automatically redefines the current style when the appropriate paragraph formatting has been changed.

AutomaticallyUpdate property is applicable to paragraph styles only.

The default value is  false .

**Parameters:**
| Parameter | Type | Description |
| --- | --- | --- |
| value | boolean | The corresponding  boolean  value. |

### setBaseStyleName(String value) {#setBaseStyleName-java.lang.String}
```
public void setBaseStyleName(String value)
```


Gets/sets the name of the style this style is based on. This will be an empty string if the style is not based on any other style and it can be set to an empty string.

**Parameters:**
| Parameter | Type | Description |
| --- | --- | --- |
| value | java.lang.String | The corresponding java.lang.String value. |

### setBidi(boolean value) {#setBidi-boolean}
```
public void setBidi(boolean value)
```


Sets whether this is a style for a right-to-left table.

When  true , the cells in rows are laid out right to left.

The default value is  false .

**Parameters:**
| Parameter | Type | Description |
| --- | --- | --- |
| value | boolean | Whether this is a style for a right-to-left table. |

### setBorderAttr(int key, Object value) {#setBorderAttr-int-java.lang.Object}
```
public void setBorderAttr(int key, Object value)
```




**Parameters:**
| Parameter | Type | Description |
| --- | --- | --- |
| key | int |  |
| value | java.lang.Object |  |

### setBottomPadding(double value) {#setBottomPadding-double}
```
public void setBottomPadding(double value)
```


Sets the amount of space (in points) to add below the contents of table cells.

**Parameters:**
| Parameter | Type | Description |
| --- | --- | --- |
| value | double | The amount of space (in points) to add below the contents of table cells. |

### setCellAttr(int key, Object value) {#setCellAttr-int-java.lang.Object}
```
public void setCellAttr(int key, Object value)
```




**Parameters:**
| Parameter | Type | Description |
| --- | --- | --- |
| key | int |  |
| value | java.lang.Object |  |

### setCellSpacing(double value) {#setCellSpacing-double}
```
public void setCellSpacing(double value)
```


Sets the amount of space (in points) between the cells.

**Parameters:**
| Parameter | Type | Description |
| --- | --- | --- |
| value | double | The amount of space (in points) between the cells. |

### setColumnStripe(int value) {#setColumnStripe-int}
```
public void setColumnStripe(int value)
```


Sets a number of columns to include in the banding when the style specifies odd/even columns banding.

**Parameters:**
| Parameter | Type | Description |
| --- | --- | --- |
| value | int | A number of columns to include in the banding when the style specifies odd/even columns banding. |

### setLeftIndent(double value) {#setLeftIndent-double}
```
public void setLeftIndent(double value)
```


Sets the value that represents the left indent of a table.

**Parameters:**
| Parameter | Type | Description |
| --- | --- | --- |
| value | double | The value that represents the left indent of a table. |

### setLeftPadding(double value) {#setLeftPadding-double}
```
public void setLeftPadding(double value)
```


Sets the amount of space (in points) to add to the left of the contents of table cells.

**Parameters:**
| Parameter | Type | Description |
| --- | --- | --- |
| value | double | The amount of space (in points) to add to the left of the contents of table cells. |

### setName(String value) {#setName-java.lang.String}
```
public void setName(String value)
```


Sets the name of the style.

Can not be empty string.

If there already is a style with such name in the collection, then this style will override it. All affected nodes will reference new style.

**Parameters:**
| Parameter | Type | Description |
| --- | --- | --- |
| value | java.lang.String | The name of the style. |

### setNextParagraphStyleName(String value) {#setNextParagraphStyleName-java.lang.String}
```
public void setNextParagraphStyleName(String value)
```


Gets/sets the name of the style to be applied automatically to a new paragraph inserted after a paragraph formatted with the specified style. This property is not used by Aspose.Words. The next paragraph style will only be applied automatically when you edit the document in MS Word.

**Parameters:**
| Parameter | Type | Description |
| --- | --- | --- |
| value | java.lang.String | The corresponding java.lang.String value. |

### setParaAttr(int key, Object value) {#setParaAttr-int-java.lang.Object}
```
public void setParaAttr(int key, Object value)
```




**Parameters:**
| Parameter | Type | Description |
| --- | --- | --- |
| key | int |  |
| value | java.lang.Object |  |

### setRightPadding(double value) {#setRightPadding-double}
```
public void setRightPadding(double value)
```


Sets the amount of space (in points) to add to the right of the contents of table cells.

**Parameters:**
| Parameter | Type | Description |
| --- | --- | --- |
| value | double | The amount of space (in points) to add to the right of the contents of table cells. |

### setRowAttr(int key, Object value) {#setRowAttr-int-java.lang.Object}
```
public void setRowAttr(int key, Object value)
```




**Parameters:**
| Parameter | Type | Description |
| --- | --- | --- |
| key | int |  |
| value | java.lang.Object |  |

### setRowStripe(int value) {#setRowStripe-int}
```
public void setRowStripe(int value)
```


Sets a number of rows to include in the banding when the style specifies odd/even row banding.

**Parameters:**
| Parameter | Type | Description |
| --- | --- | --- |
| value | int | A number of rows to include in the banding when the style specifies odd/even row banding. |

### setRunAttr(int key, Object value) {#setRunAttr-int-java.lang.Object}
```
public void setRunAttr(int key, Object value)
```




**Parameters:**
| Parameter | Type | Description |
| --- | --- | --- |
| key | int |  |
| value | java.lang.Object |  |

### setTopPadding(double value) {#setTopPadding-double}
```
public void setTopPadding(double value)
```


Sets the amount of space (in points) to add above the contents of table cells.

**Parameters:**
| Parameter | Type | Description |
| --- | --- | --- |
| value | double | The amount of space (in points) to add above the contents of table cells. |

### setVerticalAlignment(int value) {#setVerticalAlignment-int}
```
public void setVerticalAlignment(int value)
```


Specifies the vertical alignment for the cells. The default value is [CellVerticalAlignment.TOP](../../com.aspose.words/cellverticalalignment/\#TOP).

**Parameters:**
| Parameter | Type | Description |
| --- | --- | --- |
| value | int | The corresponding  int  value. The value must be one of [CellVerticalAlignment](../../com.aspose.words/cellverticalalignment/) constants. |

### toString() {#toString}
```
public String toString()
```




**Returns:**
java.lang.String
### wait() {#wait}
```
public final void wait()
```




### wait(long arg0) {#wait-long}
```
public final native void wait(long arg0)
```




**Parameters:**
| Parameter | Type | Description |
| --- | --- | --- |
| arg0 | long |  |

### wait(long arg0, int arg1) {#wait-long-int}
```
public final void wait(long arg0, int arg1)
```




**Parameters:**
| Parameter | Type | Description |
| --- | --- | --- |
| arg0 | long |  |
| arg1 | int |  |

