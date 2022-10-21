---
title: ChartLegendEntry
second_title: Aspose.Words for Java API Reference
description: Represents a chart legend entry.
type: docs
weight: 64
url: /java/com.aspose.words/chartlegendentry/
---

**Inheritance:**
java.lang.Object

**All Implemented Interfaces:**
java.lang.Cloneable
```
public class ChartLegendEntry implements Cloneable
```

Represents a chart legend entry.

To learn more, visit the **Working with Charts** documentation article.

A legend entry corresponds to a specific chart series or trendline.

The text of the entry is the name of the series or trendline. The text cannot be changed.
## Methods

| Method | Description |
| --- | --- |
| [getDirectRunAttr(int key)](#getDirectRunAttr-int-) |  |
| [fetchInheritedRunAttr(int key)](#fetchInheritedRunAttr-int-) |  |
| [setRunAttr(int key, Object value)](#setRunAttr-int-java.lang.Object-) |  |
| [removeRunAttr(int key)](#removeRunAttr-int-) |  |
| [clearRunAttrs()](#clearRunAttrs--) |  |
| [isHidden()](#isHidden--) | Gets a value indicating whether this entry is hidden in the chart legend. |
| [isHidden(boolean value)](#isHidden-boolean-) | Sets a value indicating whether this entry is hidden in the chart legend. |
| [getFont()](#getFont--) | Provides access to the font formatting of this legend entry. |
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




### isHidden() {#isHidden--}
```
public boolean isHidden()
```


Gets a value indicating whether this entry is hidden in the chart legend. The default value is **false**. When a chart legend entry is hidden, it does not affect the corresponding chart series or trendline that is still displayed on the chart.

**Returns:**
boolean - A value indicating whether this entry is hidden in the chart legend.
### isHidden(boolean value) {#isHidden-boolean-}
```
public void isHidden(boolean value)
```


Sets a value indicating whether this entry is hidden in the chart legend. The default value is **false**. When a chart legend entry is hidden, it does not affect the corresponding chart series or trendline that is still displayed on the chart.

**Parameters:**
| Parameter | Type | Description |
| --- | --- | --- |
| value | boolean | A value indicating whether this entry is hidden in the chart legend. |

### getFont() {#getFont--}
```
public Font getFont()
```


Provides access to the font formatting of this legend entry.

**Returns:**
[Font](../../com.aspose.words/font) - The corresponding [Font](../../com.aspose.words/font) value.
