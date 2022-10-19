---
title: AxisCrosses
second_title: Aspose.Words for Java API Reference
description: A utility class providing constants.
type: docs
weight: 19
url: /java/com.aspose.words/axiscrosses/
---

**Inheritance:**
java.lang.Object
```
public class AxisCrosses
```

A utility class providing constants. Specifies the possible crossing points for an axis.
## Fields

| Field | Description |
| --- | --- |
| [AUTOMATIC](#AUTOMATIC) | The category axis crosses at the zero point of the value axis (if possible), or at the minimum value if the minimum is greater than zero, or at the maximum if the maximum is less than zero. |
| [MAXIMUM](#MAXIMUM) | A perpendicular axis crosses at the maximum value of the axis. |
| [MINIMUM](#MINIMUM) | A perpendicular axis crosses at the minimum value of the axis. |
| [CUSTOM](#CUSTOM) | A perpendicular axis crosses at the specified value of the axis. |
| [length](#length) |  |
## Methods

| Method | Description |
| --- | --- |
| [getName(int axisCrosses)](#getName-int-) |  |
| [toString(int axisCrosses)](#toString-int-) |  |
| [fromName(String axisCrossesName)](#fromName-java.lang.String-) |  |
| [getValues()](#getValues--) |  |
### AUTOMATIC {#AUTOMATIC}
```
public static int AUTOMATIC
```


The category axis crosses at the zero point of the value axis (if possible), or at the minimum value if the minimum is greater than zero, or at the maximum if the maximum is less than zero.

### MAXIMUM {#MAXIMUM}
```
public static int MAXIMUM
```


A perpendicular axis crosses at the maximum value of the axis.

### MINIMUM {#MINIMUM}
```
public static int MINIMUM
```


A perpendicular axis crosses at the minimum value of the axis.

### CUSTOM {#CUSTOM}
```
public static int CUSTOM
```


A perpendicular axis crosses at the specified value of the axis.

### length {#length}
```
public static int length
```


### getName(int axisCrosses) {#getName-int-}
```
public static String getName(int axisCrosses)
```




**Parameters:**
| Parameter | Type | Description |
| --- | --- | --- |
| axisCrosses | int |  |

**Returns:**
java.lang.String
### toString(int axisCrosses) {#toString-int-}
```
public static String toString(int axisCrosses)
```




**Parameters:**
| Parameter | Type | Description |
| --- | --- | --- |
| axisCrosses | int |  |

**Returns:**
java.lang.String
### fromName(String axisCrossesName) {#fromName-java.lang.String-}
```
public static int fromName(String axisCrossesName)
```




**Parameters:**
| Parameter | Type | Description |
| --- | --- | --- |
| axisCrossesName | java.lang.String |  |

**Returns:**
int
### getValues() {#getValues--}
```
public static int[] getValues()
```




**Returns:**
int[]
