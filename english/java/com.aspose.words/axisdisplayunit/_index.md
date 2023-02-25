---
title: AxisDisplayUnit
linktitle: AxisDisplayUnit
second_title: Aspose.Words for Java API Reference
description: Provides access to the scaling options of the display units for the value axis in Java.
type: docs
weight: 20
url: /java/com.aspose.words/axisdisplayunit/
---

**Inheritance:**
java.lang.Object

**All Implemented Interfaces:**
java.lang.Cloneable
```
public class AxisDisplayUnit implements Cloneable
```

Provides access to the scaling options of the display units for the value axis.

To learn more, visit the [ Working with Charts ][Working with Charts] documentation article.


[Working with Charts]: https://docs.aspose.com/words/java/working-with-charts/
## Methods

| Method | Description |
| --- | --- |
| [equals(Object arg0)](#equals-java.lang.Object) |  |
| [getClass()](#getClass) |  |
| [getCustomUnit()](#getCustomUnit) | Gets a user-defined divisor to scale display units on the value axis. |
| [getDocument()](#getDocument) | Returns the Document the title holder belongs. |
| [getTitle()](#getTitle) |  |
| [getTitleDeleted()](#getTitleDeleted) |  |
| [getTitlePosition()](#getTitlePosition) |  |
| [getUnit()](#getUnit) | Gets the scaling value of the display units as one of the predefined values. |
| [hashCode()](#hashCode) |  |
| [isVisible()](#isVisible) |  |
| [notify()](#notify) |  |
| [notifyAll()](#notifyAll) |  |
| [setCustomUnit(double value)](#setCustomUnit-double) | Sets a user-defined divisor to scale display units on the value axis. |
| [setTitle(ChartTitle value)](#setTitle-com.aspose.words.ChartTitle) |  |
| [setTitleDeleted(boolean value)](#setTitleDeleted-boolean) |  |
| [setUnit(int value)](#setUnit-int) | Sets the scaling value of the display units as one of the predefined values. |
| [toString()](#toString) |  |
| [wait()](#wait) |  |
| [wait(long arg0)](#wait-long) |  |
| [wait(long arg0, int arg1)](#wait-long-int) |  |
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
### getClass() {#getClass}
```
public final native Class<?> getClass()
```




**Returns:**
java.lang.Class<?>
### getCustomUnit() {#getCustomUnit}
```
public double getCustomUnit()
```


Gets a user-defined divisor to scale display units on the value axis.

The property is not supported by MS Office 2016 new charts. Default value is 1.

Setting this property sets the [getUnit()](../../com.aspose.words/axisdisplayunit/\#getUnit) / [setUnit(int)](../../com.aspose.words/axisdisplayunit/\#setUnit-int) property to [AxisBuiltInUnit.CUSTOM](../../com.aspose.words/axisbuiltinunit/\#CUSTOM).

**Returns:**
double - A user-defined divisor to scale display units on the value axis.
### getDocument() {#getDocument}
```
public DocumentBase getDocument()
```


Returns the Document the title holder belongs.

**Returns:**
[DocumentBase](../../com.aspose.words/documentbase/) - The Document the title holder belongs.
### getTitle() {#getTitle}
```
public ChartTitle getTitle()
```




**Returns:**
[ChartTitle](../../com.aspose.words/charttitle/)
### getTitleDeleted() {#getTitleDeleted}
```
public boolean getTitleDeleted()
```




**Returns:**
boolean
### getTitlePosition() {#getTitlePosition}
```
public int getTitlePosition()
```




**Returns:**
int
### getUnit() {#getUnit}
```
public int getUnit()
```


Gets the scaling value of the display units as one of the predefined values. Default value is [AxisBuiltInUnit.NONE](../../com.aspose.words/axisbuiltinunit/\#NONE). The [AxisBuiltInUnit.CUSTOM](../../com.aspose.words/axisbuiltinunit/\#CUSTOM) and [AxisBuiltInUnit.PERCENTAGE](../../com.aspose.words/axisbuiltinunit/\#PERCENTAGE) values are not available in some chart types; see [AxisBuiltInUnit](../../com.aspose.words/axisbuiltinunit/) for more information.

**Returns:**
int - The scaling value of the display units as one of the predefined values. The returned value is one of [AxisBuiltInUnit](../../com.aspose.words/axisbuiltinunit/) constants.
### hashCode() {#hashCode}
```
public native int hashCode()
```




**Returns:**
int
### isVisible() {#isVisible}
```
public boolean isVisible()
```




**Returns:**
boolean
### notify() {#notify}
```
public final native void notify()
```




### notifyAll() {#notifyAll}
```
public final native void notifyAll()
```




### setCustomUnit(double value) {#setCustomUnit-double}
```
public void setCustomUnit(double value)
```


Sets a user-defined divisor to scale display units on the value axis.

The property is not supported by MS Office 2016 new charts. Default value is 1.

Setting this property sets the [getUnit()](../../com.aspose.words/axisdisplayunit/\#getUnit) / [setUnit(int)](../../com.aspose.words/axisdisplayunit/\#setUnit-int) property to [AxisBuiltInUnit.CUSTOM](../../com.aspose.words/axisbuiltinunit/\#CUSTOM).

**Parameters:**
| Parameter | Type | Description |
| --- | --- | --- |
| value | double | A user-defined divisor to scale display units on the value axis. |

### setTitle(ChartTitle value) {#setTitle-com.aspose.words.ChartTitle}
```
public void setTitle(ChartTitle value)
```




**Parameters:**
| Parameter | Type | Description |
| --- | --- | --- |
| value | [ChartTitle](../../com.aspose.words/charttitle/) |  |

### setTitleDeleted(boolean value) {#setTitleDeleted-boolean}
```
public void setTitleDeleted(boolean value)
```




**Parameters:**
| Parameter | Type | Description |
| --- | --- | --- |
| value | boolean |  |

### setUnit(int value) {#setUnit-int}
```
public void setUnit(int value)
```


Sets the scaling value of the display units as one of the predefined values. Default value is [AxisBuiltInUnit.NONE](../../com.aspose.words/axisbuiltinunit/\#NONE). The [AxisBuiltInUnit.CUSTOM](../../com.aspose.words/axisbuiltinunit/\#CUSTOM) and [AxisBuiltInUnit.PERCENTAGE](../../com.aspose.words/axisbuiltinunit/\#PERCENTAGE) values are not available in some chart types; see [AxisBuiltInUnit](../../com.aspose.words/axisbuiltinunit/) for more information.

**Parameters:**
| Parameter | Type | Description |
| --- | --- | --- |
| value | int | The scaling value of the display units as one of the predefined values. The value must be one of [AxisBuiltInUnit](../../com.aspose.words/axisbuiltinunit/) constants. |

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

