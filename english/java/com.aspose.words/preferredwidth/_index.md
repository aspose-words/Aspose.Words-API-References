---
title: PreferredWidth
second_title: Aspose.Words for Java API Reference
description: Represents a value and its unit of measure that is used to specify the preferred width of a table or a cell.
type: docs
weight: 466
url: /java/com.aspose.words/preferredwidth/
---

**Inheritance:**
java.lang.Object
```
public class PreferredWidth
```

Represents a value and its unit of measure that is used to specify the preferred width of a table or a cell.

To learn more, visit the **Working with Tables** documentation article.

Preferred width can be specified as a percentage, number of points or a special "none/auto" value.

The instances of this class are immutable.
## Fields

| Field | Description |
| --- | --- |
| [AUTO](#AUTO) | Returns an instance that represents the "preferred width is not specified" value. |
## Methods

| Method | Description |
| --- | --- |
| [fromPercent(double percent)](#fromPercent-double-) | A creation method that returns a new instance that represents a preferred width specified as a percentage. |
| [fromPoints(double points)](#fromPoints-double-) | A creation method that returns a new instance that represents a preferred width specified using a number of points. |
| [getType()](#getType--) | Gets the unit of measure used for this preferred width value. |
| [getValue()](#getValue--) | Gets the preferred width value. |
| [equals(PreferredWidth other)](#equals-com.aspose.words.PreferredWidth-) | Determines whether the specified PreferredWidth is equal in value to the current PreferredWidth. |
| [equals(Object obj)](#equals-java.lang.Object-) | Determines whether the specified object is equal in value to the current object. |
| [hashCode()](#hashCode--) |  |
| [toString()](#toString--) | Returns a user-friendly string that displays the value of this object. |
### AUTO {#AUTO}
```
public static PreferredWidth AUTO
```


Returns an instance that represents the "preferred width is not specified" value.

### fromPercent(double percent) {#fromPercent-double-}
```
public static PreferredWidth fromPercent(double percent)
```


A creation method that returns a new instance that represents a preferred width specified as a percentage.

**Parameters:**
| Parameter | Type | Description |
| --- | --- | --- |
| percent | double | The value must be from 0 to 100. |

**Returns:**
[PreferredWidth](../../com.aspose.words/preferredwidth)
### fromPoints(double points) {#fromPoints-double-}
```
public static PreferredWidth fromPoints(double points)
```


A creation method that returns a new instance that represents a preferred width specified using a number of points.

**Parameters:**
| Parameter | Type | Description |
| --- | --- | --- |
| points | double | The value must be from 0 to 22 inches (22 \* 72 points). |

**Returns:**
[PreferredWidth](../../com.aspose.words/preferredwidth)
### getType() {#getType--}
```
public int getType()
```


Gets the unit of measure used for this preferred width value.

**Returns:**
int - The unit of measure used for this preferred width value. The returned value is one of [PreferredWidthType](../../com.aspose.words/preferredwidthtype) constants.
### getValue() {#getValue--}
```
public double getValue()
```


Gets the preferred width value. The unit of measure is specified in the [getType()](../../com.aspose.words/preferredwidth\#getType--) property.

**Returns:**
double - The preferred width value.
### equals(PreferredWidth other) {#equals-com.aspose.words.PreferredWidth-}
```
public boolean equals(PreferredWidth other)
```


Determines whether the specified PreferredWidth is equal in value to the current PreferredWidth.

**Parameters:**
| Parameter | Type | Description |
| --- | --- | --- |
| other | [PreferredWidth](../../com.aspose.words/preferredwidth) |  |

**Returns:**
boolean
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
