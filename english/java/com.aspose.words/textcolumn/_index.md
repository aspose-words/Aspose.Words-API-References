---
title: TextColumn
second_title: Aspose.Words for Java API Reference
description: Represents a single text column.
type: docs
weight: 561
url: /java/com.aspose.words/textcolumn/
---

**Inheritance:**
java.lang.Object

**All Implemented Interfaces:**
java.lang.Cloneable
```
public class TextColumn implements Cloneable
```

Represents a single text column. **TextColumn** is a member of the [TextColumnCollection](../../com.aspose.words/textcolumncollection) collection. The **TextColumns** collection includes all the columns in a section of a document.

To learn more, visit the **Working with Sections** documentation article.

**TextColumn** objects are only used to specify columns with custom width and spacing. If you want the columns in the document to be of equal width, set TextColumns. [TextColumnCollection.getEvenlySpaced()](../../com.aspose.words/textcolumncollection\#getEvenlySpaced--) / [TextColumnCollection.setEvenlySpaced(boolean)](../../com.aspose.words/textcolumncollection\#setEvenlySpaced-boolean-) to **true**.

When a new **TextColumn** is created it has its width and spacing set to zero.
## Methods

| Method | Description |
| --- | --- |
| [getWidth()](#getWidth--) | Gets the width of the text column in points. |
| [setWidth(double value)](#setWidth-double-) | Sets the width of the text column in points. |
| [getSpaceAfter()](#getSpaceAfter--) | Gets the space between this column and the next column in points. |
| [setSpaceAfter(double value)](#setSpaceAfter-double-) | Sets the space between this column and the next column in points. |
### getWidth() {#getWidth--}
```
public double getWidth()
```


Gets the width of the text column in points.

**Returns:**
double - The width of the text column in points.
### setWidth(double value) {#setWidth-double-}
```
public void setWidth(double value)
```


Sets the width of the text column in points.

**Parameters:**
| Parameter | Type | Description |
| --- | --- | --- |
| value | double | The width of the text column in points. |

### getSpaceAfter() {#getSpaceAfter--}
```
public double getSpaceAfter()
```


Gets the space between this column and the next column in points. Not required for the last column.

**Returns:**
double - The space between this column and the next column in points.
### setSpaceAfter(double value) {#setSpaceAfter-double-}
```
public void setSpaceAfter(double value)
```


Sets the space between this column and the next column in points. Not required for the last column.

**Parameters:**
| Parameter | Type | Description |
| --- | --- | --- |
| value | double | The space between this column and the next column in points. |

