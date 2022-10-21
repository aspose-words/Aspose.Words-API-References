---
title: MergeFieldImageDimension
second_title: Aspose.Words for Java API Reference
description: Represents an image dimension i.e.
type: docs
weight: 394
url: /java/com.aspose.words/mergefieldimagedimension/
---

**Inheritance:**
java.lang.Object

**All Implemented Interfaces:**
java.lang.Cloneable
```
public class MergeFieldImageDimension implements Cloneable
```

Represents an image dimension (i.e. the width or the height) used across a mail merge process.

To learn more, visit the **Working with Fields** documentation article.

To indicate that the image should be inserted with its original dimension during a mail merge, you should assign a negative value to the [getValue()](../../com.aspose.words/mergefieldimagedimension\#getValue--) / [setValue(double)](../../com.aspose.words/mergefieldimagedimension\#setValue-double-) property.
## Constructors

| Constructor | Description |
| --- | --- |
| [MergeFieldImageDimension(double value)](#MergeFieldImageDimension-double-) | Creates an image dimension instance with the given value in points. |
| [MergeFieldImageDimension(double value, int unit)](#MergeFieldImageDimension-double-int-) | Initializes a new instance of this class. |
## Methods

| Method | Description |
| --- | --- |
| [getValue()](#getValue--) | The value. |
| [setValue(double value)](#setValue-double-) | The value. |
| [getUnit()](#getUnit--) | The unit. |
| [setUnit(int value)](#setUnit-int-) | The unit. |
### MergeFieldImageDimension(double value) {#MergeFieldImageDimension-double-}
```
public MergeFieldImageDimension(double value)
```


Creates an image dimension instance with the given value in points. You should use a negative value to indicate that the original value of the corresponding image dimension should be applied.

**Parameters:**
| Parameter | Type | Description |
| --- | --- | --- |
| value | double | The value. |

### MergeFieldImageDimension(double value, int unit) {#MergeFieldImageDimension-double-int-}
```
public MergeFieldImageDimension(double value, int unit)
```


Initializes a new instance of this class.

**Parameters:**
| Parameter | Type | Description |
| --- | --- | --- |
| value | double |  |
| unit | int |  |

### getValue() {#getValue--}
```
public double getValue()
```


The value. You should use a negative value to indicate that the original value of the corresponding image dimension should be applied.

**Returns:**
double - The corresponding  double  value.
### setValue(double value) {#setValue-double-}
```
public void setValue(double value)
```


The value. You should use a negative value to indicate that the original value of the corresponding image dimension should be applied.

**Parameters:**
| Parameter | Type | Description |
| --- | --- | --- |
| value | double | The corresponding  double  value. |

### getUnit() {#getUnit--}
```
public int getUnit()
```


The unit.

**Returns:**
int - The corresponding  int  value. The returned value is one of [MergeFieldImageDimensionUnit](../../com.aspose.words/mergefieldimagedimensionunit) constants.
### setUnit(int value) {#setUnit-int-}
```
public void setUnit(int value)
```


The unit.

**Parameters:**
| Parameter | Type | Description |
| --- | --- | --- |
| value | int | The corresponding  int  value. The value must be one of [MergeFieldImageDimensionUnit](../../com.aspose.words/mergefieldimagedimensionunit) constants. |

