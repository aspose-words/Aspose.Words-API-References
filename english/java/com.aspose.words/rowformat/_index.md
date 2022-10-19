---
title: RowFormat
second_title: Aspose.Words for Java API Reference
description: Represents all formatting for a table row.
type: docs
weight: 494
url: /java/com.aspose.words/rowformat/
---

**Inheritance:**
java.lang.Object
```
public class RowFormat
```

Represents all formatting for a table row.

To learn more, visit the **Working with Tables** documentation article.
## Methods

| Method | Description |
| --- | --- |
| [clearFormatting()](#clearFormatting--) | Resets to default row formatting. |
| [getBorders()](#getBorders--) | Gets the collection of default cell borders for the row. |
| [getHeight()](#getHeight--) | Gets the height of the table row in points. |
| [setHeight(double value)](#setHeight-double-) | Sets the height of the table row in points. |
| [getHeightRule()](#getHeightRule--) | Gets the rule for determining the height of the table row. |
| [setHeightRule(int value)](#setHeightRule-int-) | Sets the rule for determining the height of the table row. |
| [getAllowBreakAcrossPages()](#getAllowBreakAcrossPages--) | True if the text in a table row is allowed to split across a page break. |
| [setAllowBreakAcrossPages(boolean value)](#setAllowBreakAcrossPages-boolean-) | True if the text in a table row is allowed to split across a page break. |
| [getHeadingFormat()](#getHeadingFormat--) | True if the row is repeated as a table heading on every page when the table spans more than one page. |
| [setHeadingFormat(boolean value)](#setHeadingFormat-boolean-) | True if the row is repeated as a table heading on every page when the table spans more than one page. |
| [getDirectBorderAttr(int key)](#getDirectBorderAttr-int-) |  |
| [fetchInheritedBorderAttr(int key)](#fetchInheritedBorderAttr-int-) |  |
| [setBorderAttr(int key, Object value)](#setBorderAttr-int-java.lang.Object-) |  |
### clearFormatting() {#clearFormatting--}
```
public void clearFormatting()
```


Resets to default row formatting.

### getBorders() {#getBorders--}
```
public BorderCollection getBorders()
```


Gets the collection of default cell borders for the row.

**Returns:**
[BorderCollection](../../com.aspose.words/bordercollection) - The collection of default cell borders for the row.
### getHeight() {#getHeight--}
```
public double getHeight()
```


Gets the height of the table row in points.

**Returns:**
double - The height of the table row in points.
### setHeight(double value) {#setHeight-double-}
```
public void setHeight(double value)
```


Sets the height of the table row in points.

**Parameters:**
| Parameter | Type | Description |
| --- | --- | --- |
| value | double | The height of the table row in points. |

### getHeightRule() {#getHeightRule--}
```
public int getHeightRule()
```


Gets the rule for determining the height of the table row.

**Returns:**
int - The rule for determining the height of the table row. The returned value is one of [HeightRule](../../com.aspose.words/heightrule) constants.
### setHeightRule(int value) {#setHeightRule-int-}
```
public void setHeightRule(int value)
```


Sets the rule for determining the height of the table row.

**Parameters:**
| Parameter | Type | Description |
| --- | --- | --- |
| value | int | The rule for determining the height of the table row. The value must be one of [HeightRule](../../com.aspose.words/heightrule) constants. |

### getAllowBreakAcrossPages() {#getAllowBreakAcrossPages--}
```
public boolean getAllowBreakAcrossPages()
```


True if the text in a table row is allowed to split across a page break.

**Returns:**
boolean - The corresponding  boolean  value.
### setAllowBreakAcrossPages(boolean value) {#setAllowBreakAcrossPages-boolean-}
```
public void setAllowBreakAcrossPages(boolean value)
```


True if the text in a table row is allowed to split across a page break.

**Parameters:**
| Parameter | Type | Description |
| --- | --- | --- |
| value | boolean | The corresponding  boolean  value. |

### getHeadingFormat() {#getHeadingFormat--}
```
public boolean getHeadingFormat()
```


True if the row is repeated as a table heading on every page when the table spans more than one page.

**Returns:**
boolean - The corresponding  boolean  value.
### setHeadingFormat(boolean value) {#setHeadingFormat-boolean-}
```
public void setHeadingFormat(boolean value)
```


True if the row is repeated as a table heading on every page when the table spans more than one page.

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

