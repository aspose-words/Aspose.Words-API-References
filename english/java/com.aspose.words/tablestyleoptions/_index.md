---
title: TableStyleOptions
second_title: Aspose.Words for Java API Reference
description: A utility class providing constants.
type: docs
weight: 553
url: /java/com.aspose.words/tablestyleoptions/
---

**Inheritance:**
java.lang.Object
```
public class TableStyleOptions
```

A utility class providing constants. Specifies how table style is applied to a table.
## Fields

| Field | Description |
| --- | --- |
| [NONE](#NONE) | No table style formatting is applied. |
| [FIRST_ROW](#FIRST-ROW) | Apply first row conditional formatting. |
| [LAST_ROW](#LAST-ROW) | Apply last row conditional formatting. |
| [FIRST_COLUMN](#FIRST-COLUMN) | Apply 1 first column conditional formatting. |
| [LAST_COLUMN](#LAST-COLUMN) | Apply last column conditional formatting. |
| [ROW_BANDS](#ROW-BANDS) | Apply row banding conditional formatting. |
| [COLUMN_BANDS](#COLUMN-BANDS) | Apply column banding conditional formatting. |
| [DEFAULT_2003](#DEFAULT-2003) | Row and column banding is applied. |
| [DEFAULT](#DEFAULT) | This is Microsoft Word defaults. |
| [length](#length) |  |
## Methods

| Method | Description |
| --- | --- |
| [getName(int tableStyleOptions)](#getName-int-) |  |
| [getNames(int tableStyleOptions)](#getNames-int-) |  |
| [toString(int tableStyleOptions)](#toString-int-) |  |
| [toStringSet(int attr)](#toStringSet-int-) |  |
| [fromName(String tableStyleOptionsName)](#fromName-java.lang.String-) |  |
| [fromNames(Set tableStyleOptionsNames)](#fromNames-java.util.Set-) |  |
| [getValues()](#getValues--) |  |
### NONE {#NONE}
```
public static int NONE
```


No table style formatting is applied.

### FIRST_ROW {#FIRST-ROW}
```
public static int FIRST_ROW
```


Apply first row conditional formatting.

### LAST_ROW {#LAST-ROW}
```
public static int LAST_ROW
```


Apply last row conditional formatting.

### FIRST_COLUMN {#FIRST-COLUMN}
```
public static int FIRST_COLUMN
```


Apply 1 first column conditional formatting.

### LAST_COLUMN {#LAST-COLUMN}
```
public static int LAST_COLUMN
```


Apply last column conditional formatting.

### ROW_BANDS {#ROW-BANDS}
```
public static int ROW_BANDS
```


Apply row banding conditional formatting.

### COLUMN_BANDS {#COLUMN-BANDS}
```
public static int COLUMN_BANDS
```


Apply column banding conditional formatting.

### DEFAULT_2003 {#DEFAULT-2003}
```
public static int DEFAULT_2003
```


Row and column banding is applied. This is Microsoft Word default for old formats such as DOC, WML and RTF.

### DEFAULT {#DEFAULT}
```
public static int DEFAULT
```


This is Microsoft Word defaults.

### length {#length}
```
public static int length
```


### getName(int tableStyleOptions) {#getName-int-}
```
public static String getName(int tableStyleOptions)
```




**Parameters:**
| Parameter | Type | Description |
| --- | --- | --- |
| tableStyleOptions | int |  |

**Returns:**
java.lang.String
### getNames(int tableStyleOptions) {#getNames-int-}
```
public static Set getNames(int tableStyleOptions)
```




**Parameters:**
| Parameter | Type | Description |
| --- | --- | --- |
| tableStyleOptions | int |  |

**Returns:**
java.util.Set
### toString(int tableStyleOptions) {#toString-int-}
```
public static String toString(int tableStyleOptions)
```




**Parameters:**
| Parameter | Type | Description |
| --- | --- | --- |
| tableStyleOptions | int |  |

**Returns:**
java.lang.String
### toStringSet(int attr) {#toStringSet-int-}
```
public static String toStringSet(int attr)
```




**Parameters:**
| Parameter | Type | Description |
| --- | --- | --- |
| attr | int |  |

**Returns:**
java.lang.String
### fromName(String tableStyleOptionsName) {#fromName-java.lang.String-}
```
public static int fromName(String tableStyleOptionsName)
```




**Parameters:**
| Parameter | Type | Description |
| --- | --- | --- |
| tableStyleOptionsName | java.lang.String |  |

**Returns:**
int
### fromNames(Set tableStyleOptionsNames) {#fromNames-java.util.Set-}
```
public static int fromNames(Set tableStyleOptionsNames)
```




**Parameters:**
| Parameter | Type | Description |
| --- | --- | --- |
| tableStyleOptionsNames | java.util.Set |  |

**Returns:**
int
### getValues() {#getValues--}
```
public static int[] getValues()
```




**Returns:**
int[]
