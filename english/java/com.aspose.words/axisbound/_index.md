---
title: AxisBound
second_title: Aspose.Words for Java API Reference
description: Represents minimum or maximum bound of axis values.
type: docs
weight: 16
url: /java/com.aspose.words/axisbound/
---

**Inheritance:**
java.lang.Object
```
public class AxisBound
```

Represents minimum or maximum bound of axis values.

To learn more, visit the **Working with Charts** documentation article.

Bound can be specified as a numeric, datetime or a special "auto" value.

The instances of this class are immutable.
## Constructors

| Constructor | Description |
| --- | --- |
| [AxisBound()](#AxisBound--) | Creates a new instance indicating that axis bound should be determined automatically by a word-processing application. |
| [AxisBound(double value)](#AxisBound-double-) | Creates an axis bound represented as a number. |
| [AxisBound(Date datetime)](#AxisBound-java.util.Date-) | Creates an axis bound represented as datetime value. |
## Methods

| Method | Description |
| --- | --- |
| [equals(Object obj)](#equals-java.lang.Object-) | Determines whether the specified object is equal in value to the current object. |
| [hashCode()](#hashCode--) |  |
| [toString()](#toString--) | Returns a user-friendly string that displays the value of this object. |
| [isAuto()](#isAuto--) | Returns a flag indicating that axis bound should be determined automatically. |
| [getValue()](#getValue--) | Returns numeric value of axis bound. |
| [getValueAsDate()](#getValueAsDate--) | Returns value of axis bound represented as datetime. |
### AxisBound() {#AxisBound--}
```
public AxisBound()
```


Creates a new instance indicating that axis bound should be determined automatically by a word-processing application.

### AxisBound(double value) {#AxisBound-double-}
```
public AxisBound(double value)
```


Creates an axis bound represented as a number.

**Parameters:**
| Parameter | Type | Description |
| --- | --- | --- |
| value | double |  |

### AxisBound(Date datetime) {#AxisBound-java.util.Date-}
```
public AxisBound(Date datetime)
```


Creates an axis bound represented as datetime value.

**Parameters:**
| Parameter | Type | Description |
| --- | --- | --- |
| datetime | java.util.Date |  |

### equals(Object obj) {#equals-java.lang.Object-}
```
public boolean equals(Object obj)
```


Determines whether the specified object is equal in value to the current object.

**Parameters:**
| Parameter | Type | Description |
| --- | --- | --- |
| obj | java.lang.Object |  |

**Returns:**
boolean
### hashCode() {#hashCode--}
```
public int hashCode()
```




**Returns:**
int
### toString() {#toString--}
```
public String toString()
```


Returns a user-friendly string that displays the value of this object.

**Returns:**
java.lang.String
### isAuto() {#isAuto--}
```
public boolean isAuto()
```


Returns a flag indicating that axis bound should be determined automatically.

**Returns:**
boolean - A flag indicating that axis bound should be determined automatically.
### getValue() {#getValue--}
```
public double getValue()
```


Returns numeric value of axis bound.

**Returns:**
double - Numeric value of axis bound.
### getValueAsDate() {#getValueAsDate--}
```
public Date getValueAsDate()
```


Returns value of axis bound represented as datetime.

**Returns:**
java.util.Date - Value of axis bound represented as datetime.
