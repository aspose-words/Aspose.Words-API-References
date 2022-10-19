---
title: TextColumnCollection
second_title: Aspose.Words for Java API Reference
description: A collection of  objects that represent all the columns of text in a section of a document.
type: docs
weight: 562
url: /java/com.aspose.words/textcolumncollection/
---

**Inheritance:**
java.lang.Object
```
public class TextColumnCollection
```

A collection of [TextColumn](../../com.aspose.words/textcolumn) objects that represent all the columns of text in a section of a document.

To learn more, visit the **Working with Sections** documentation article.

Use [setCount(int)](../../com.aspose.words/textcolumncollection\#setCount-int-) to set the number of text columns.

To make all columns equal width and spaced evenly, set [getEvenlySpaced()](../../com.aspose.words/textcolumncollection\#getEvenlySpaced--) / [setEvenlySpaced(boolean)](../../com.aspose.words/textcolumncollection\#setEvenlySpaced-boolean-) to **true** and specify the amount of space between the columns in [getSpacing()](../../com.aspose.words/textcolumncollection\#getSpacing--) / [setSpacing(double)](../../com.aspose.words/textcolumncollection\#setSpacing-double-). MS Word will automatically calculate column widths.

If you have **EvenlySpaced** set to **false**, you need to specify width and spacing for each column individually. Use the indexer to access individual [TextColumn](../../com.aspose.words/textcolumn) objects.

When using custom column widths, make sure the sum of all column widths and spacings between them equals page width minus left and right page margins.
## Methods

| Method | Description |
| --- | --- |
| [setCount(int newCount)](#setCount-int-) | Arranges text into the specified number of text columns. |
| [getEvenlySpaced()](#getEvenlySpaced--) | **True** if text columns are of equal width and evenly spaced. |
| [setEvenlySpaced(boolean value)](#setEvenlySpaced-boolean-) | **True** if text columns are of equal width and evenly spaced. |
| [getSpacing()](#getSpacing--) | When columns are evenly spaced, gets or sets the amount of space between each column in points. |
| [setSpacing(double value)](#setSpacing-double-) | When columns are evenly spaced, gets or sets the amount of space between each column in points. |
| [getWidth()](#getWidth--) | When columns are evenly spaced, gets the width of the columns. |
| [getLineBetween()](#getLineBetween--) | When **true**, adds a vertical line between columns. |
| [setLineBetween(boolean value)](#setLineBetween-boolean-) | When **true**, adds a vertical line between columns. |
| [getCount()](#getCount--) | Gets the number of columns in the section of a document. |
| [get(int index)](#get-int-) | Returns a text column at the specified index. |
### setCount(int newCount) {#setCount-int-}
```
public void setCount(int newCount)
```


Arranges text into the specified number of text columns.

When [getEvenlySpaced()](../../com.aspose.words/textcolumncollection\#getEvenlySpaced--) / [setEvenlySpaced(boolean)](../../com.aspose.words/textcolumncollection\#setEvenlySpaced-boolean-) is **false** and you increase the number of columns, new [TextColumn](../../com.aspose.words/textcolumn) objects are created with zero width and spacing. You need to set width and spacing for the new columns.

**Parameters:**
| Parameter | Type | Description |
| --- | --- | --- |
| newCount | int | The number of columns the text is to be arranged into. |

### getEvenlySpaced() {#getEvenlySpaced--}
```
public boolean getEvenlySpaced()
```


**True** if text columns are of equal width and evenly spaced.

**Returns:**
boolean - The corresponding  boolean  value.
### setEvenlySpaced(boolean value) {#setEvenlySpaced-boolean-}
```
public void setEvenlySpaced(boolean value)
```


**True** if text columns are of equal width and evenly spaced.

**Parameters:**
| Parameter | Type | Description |
| --- | --- | --- |
| value | boolean | The corresponding  boolean  value. |

### getSpacing() {#getSpacing--}
```
public double getSpacing()
```


When columns are evenly spaced, gets or sets the amount of space between each column in points. Has effect only when [getEvenlySpaced()](../../com.aspose.words/textcolumncollection\#getEvenlySpaced--) / [setEvenlySpaced(boolean)](../../com.aspose.words/textcolumncollection\#setEvenlySpaced-boolean-) is set to **true**.

**Returns:**
double - The corresponding  double  value.
### setSpacing(double value) {#setSpacing-double-}
```
public void setSpacing(double value)
```


When columns are evenly spaced, gets or sets the amount of space between each column in points. Has effect only when [getEvenlySpaced()](../../com.aspose.words/textcolumncollection\#getEvenlySpaced--) / [setEvenlySpaced(boolean)](../../com.aspose.words/textcolumncollection\#setEvenlySpaced-boolean-) is set to **true**.

**Parameters:**
| Parameter | Type | Description |
| --- | --- | --- |
| value | double | The corresponding  double  value. |

### getWidth() {#getWidth--}
```
public double getWidth()
```


When columns are evenly spaced, gets the width of the columns.

Has effect only when [getEvenlySpaced()](../../com.aspose.words/textcolumncollection\#getEvenlySpaced--) / [setEvenlySpaced(boolean)](../../com.aspose.words/textcolumncollection\#setEvenlySpaced-boolean-) is set to **true**.

**Returns:**
double - The corresponding  double  value.
### getLineBetween() {#getLineBetween--}
```
public boolean getLineBetween()
```


When **true**, adds a vertical line between columns.

**Returns:**
boolean - The corresponding  boolean  value.
### setLineBetween(boolean value) {#setLineBetween-boolean-}
```
public void setLineBetween(boolean value)
```


When **true**, adds a vertical line between columns.

**Parameters:**
| Parameter | Type | Description |
| --- | --- | --- |
| value | boolean | The corresponding  boolean  value. |

### getCount() {#getCount--}
```
public int getCount()
```


Gets the number of columns in the section of a document.

**Returns:**
int - The number of columns in the section of a document.
### get(int index) {#get-int-}
```
public TextColumn get(int index)
```


Returns a text column at the specified index.

**Parameters:**
| Parameter | Type | Description |
| --- | --- | --- |
| index | int |  |

**Returns:**
[TextColumn](../../com.aspose.words/textcolumn) - A text column at the specified index.