---
title: ChartTitle
second_title: Aspose.Words for Java API Reference
description: Provides access to the chart title properties.
type: docs
weight: 70
url: /java/com.aspose.words/charttitle/
---

**Inheritance:**
java.lang.Object

**All Implemented Interfaces:**
java.lang.Cloneable
```
public class ChartTitle implements Cloneable
```

Provides access to the chart title properties.

To learn more, visit the **Working with Charts** documentation article.
## Methods

| Method | Description |
| --- | --- |
| [getDirectRunAttr(int key)](#getDirectRunAttr-int-) |  |
| [fetchInheritedRunAttr(int key)](#fetchInheritedRunAttr-int-) |  |
| [setRunAttr(int key, Object value)](#setRunAttr-int-java.lang.Object-) |  |
| [removeRunAttr(int key)](#removeRunAttr-int-) |  |
| [clearRunAttrs()](#clearRunAttrs--) |  |
| [getText()](#getText--) | Gets the text of the chart title. |
| [setText(String value)](#setText-java.lang.String-) | Sets the text of the chart title. |
| [getOverlay()](#getOverlay--) | Determines whether other chart elements shall be allowed to overlap title. |
| [setOverlay(boolean value)](#setOverlay-boolean-) | Determines whether other chart elements shall be allowed to overlap title. |
| [getShow()](#getShow--) | Determines whether the title shall be shown for this chart. |
| [setShow(boolean value)](#setShow-boolean-) | Determines whether the title shall be shown for this chart. |
### getDirectRunAttr(int key) {#getDirectRunAttr-int-}
```
public Object getDirectRunAttr(int key)
```




**Parameters:**
| Parameter | Type | Description |
| --- | --- | --- |
| key | int |  |

**Returns:**
java.lang.Object
### fetchInheritedRunAttr(int key) {#fetchInheritedRunAttr-int-}
```
public Object fetchInheritedRunAttr(int key)
```




**Parameters:**
| Parameter | Type | Description |
| --- | --- | --- |
| key | int |  |

**Returns:**
java.lang.Object
### setRunAttr(int key, Object value) {#setRunAttr-int-java.lang.Object-}
```
public void setRunAttr(int key, Object value)
```




**Parameters:**
| Parameter | Type | Description |
| --- | --- | --- |
| key | int |  |
| value | java.lang.Object |  |

### removeRunAttr(int key) {#removeRunAttr-int-}
```
public void removeRunAttr(int key)
```




**Parameters:**
| Parameter | Type | Description |
| --- | --- | --- |
| key | int |  |

### clearRunAttrs() {#clearRunAttrs--}
```
public void clearRunAttrs()
```




### getText() {#getText--}
```
public String getText()
```


Gets the text of the chart title. If null or empty value is specified, auto generated title will be shown. Use [getShow()](../../com.aspose.words/charttitle\#getShow--) / [setShow(boolean)](../../com.aspose.words/charttitle\#setShow-boolean-) option if you need to hide the Title.

**Returns:**
java.lang.String - The text of the chart title.
### setText(String value) {#setText-java.lang.String-}
```
public void setText(String value)
```


Sets the text of the chart title. If null or empty value is specified, auto generated title will be shown. Use [getShow()](../../com.aspose.words/charttitle\#getShow--) / [setShow(boolean)](../../com.aspose.words/charttitle\#setShow-boolean-) option if you need to hide the Title.

**Parameters:**
| Parameter | Type | Description |
| --- | --- | --- |
| value | java.lang.String | The text of the chart title. |

### getOverlay() {#getOverlay--}
```
public boolean getOverlay()
```


Determines whether other chart elements shall be allowed to overlap title. By default overlay is false.

**Returns:**
boolean - The corresponding  boolean  value.
### setOverlay(boolean value) {#setOverlay-boolean-}
```
public void setOverlay(boolean value)
```


Determines whether other chart elements shall be allowed to overlap title. By default overlay is false.

**Parameters:**
| Parameter | Type | Description |
| --- | --- | --- |
| value | boolean | The corresponding  boolean  value. |

### getShow() {#getShow--}
```
public boolean getShow()
```


Determines whether the title shall be shown for this chart. Default value is true.

**Returns:**
boolean - The corresponding  boolean  value.
### setShow(boolean value) {#setShow-boolean-}
```
public void setShow(boolean value)
```


Determines whether the title shall be shown for this chart. Default value is true.

**Parameters:**
| Parameter | Type | Description |
| --- | --- | --- |
| value | boolean | The corresponding  boolean  value. |

