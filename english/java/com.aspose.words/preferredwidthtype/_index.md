---
title: PreferredWidthType
second_title: Aspose.Words for Java API Reference
description: A utility class providing constants.
type: docs
weight: 467
url: /java/com.aspose.words/preferredwidthtype/
---

**Inheritance:**
java.lang.Object
```
public class PreferredWidthType
```

A utility class providing constants. Specifies the unit of measurement for the preferred width of a table or cell.
## Fields

| Field | Description |
| --- | --- |
| [AUTO](#AUTO) | The preferred width is not specified. |
| [PERCENT](#PERCENT) | Measure the current item width using a specified percentage. |
| [POINTS](#POINTS) | Measure the current item width using a specified number of points (1/72 inch). |
| [length](#length) |  |
## Methods

| Method | Description |
| --- | --- |
| [getName(int preferredWidthType)](#getName-int-) |  |
| [toString(int preferredWidthType)](#toString-int-) |  |
| [fromName(String preferredWidthTypeName)](#fromName-java.lang.String-) |  |
| [getValues()](#getValues--) |  |
### AUTO {#AUTO}
```
public static int AUTO
```


The preferred width is not specified. The actual width of the table or cell is either specified using the explicit width or will be determined automatically by the table layout algorithm when the table is displayed, depending on the table auto fit setting.

### PERCENT {#PERCENT}
```
public static int PERCENT
```


Measure the current item width using a specified percentage.

### POINTS {#POINTS}
```
public static int POINTS
```


Measure the current item width using a specified number of points (1/72 inch).

### length {#length}
```
public static int length
```


### getName(int preferredWidthType) {#getName-int-}
```
public static String getName(int preferredWidthType)
```




**Parameters:**
| Parameter | Type | Description |
| --- | --- | --- |
| preferredWidthType | int |  |

**Returns:**
java.lang.String
### toString(int preferredWidthType) {#toString-int-}
```
public static String toString(int preferredWidthType)
```




**Parameters:**
| Parameter | Type | Description |
| --- | --- | --- |
| preferredWidthType | int |  |

**Returns:**
java.lang.String
### fromName(String preferredWidthTypeName) {#fromName-java.lang.String-}
```
public static int fromName(String preferredWidthTypeName)
```




**Parameters:**
| Parameter | Type | Description |
| --- | --- | --- |
| preferredWidthTypeName | java.lang.String |  |

**Returns:**
int
### getValues() {#getValues--}
```
public static int[] getValues()
```




**Returns:**
int[]
