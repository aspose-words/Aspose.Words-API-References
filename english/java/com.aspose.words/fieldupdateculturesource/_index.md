---
title: FieldUpdateCultureSource
linktitle: FieldUpdateCultureSource
second_title: Aspose.Words for Java
description: Indicates what culture to use during field update in Java.
type: docs
weight: 278
url: /java/com.aspose.words/fieldupdateculturesource/
---

**Inheritance:**
java.lang.Object
```
public class FieldUpdateCultureSource
```

Indicates what culture to use during field update.
## Fields

| Field | Description |
| --- | --- |
| [CURRENT_THREAD](#CURRENT-THREAD) | The culture of the current execution thread is used to update fields. |
| [FIELD_CODE](#FIELD-CODE) | The culture specified in the field formatting properties via language setting is used. |
| [length](#length) |  |
## Methods

| Method | Description |
| --- | --- |
| [fromName(String fieldUpdateCultureSourceName)](#fromName-java.lang.String) |  |
| [getName(int fieldUpdateCultureSource)](#getName-int) |  |
| [getValues()](#getValues) |  |
| [toString(int fieldUpdateCultureSource)](#toString-int) |  |
### CURRENT_THREAD {#CURRENT-THREAD}
```
public static int CURRENT_THREAD
```


The culture of the current execution thread is used to update fields.

### FIELD_CODE {#FIELD-CODE}
```
public static int FIELD_CODE
```


The culture specified in the field formatting properties via language setting is used.

 **Remarks:** 

To be exact, Aspose.Words mimics MS Word by using the language set for the first character of the field code.

### length {#length}
```
public static int length
```


### fromName(String fieldUpdateCultureSourceName) {#fromName-java.lang.String}
```
public static int fromName(String fieldUpdateCultureSourceName)
```




**Parameters:**
| Parameter | Type | Description |
| --- | --- | --- |
| fieldUpdateCultureSourceName | java.lang.String |  |

**Returns:**
int
### getName(int fieldUpdateCultureSource) {#getName-int}
```
public static String getName(int fieldUpdateCultureSource)
```




**Parameters:**
| Parameter | Type | Description |
| --- | --- | --- |
| fieldUpdateCultureSource | int |  |

**Returns:**
java.lang.String
### getValues() {#getValues}
```
public static int[] getValues()
```




**Returns:**
int[]
### toString(int fieldUpdateCultureSource) {#toString-int}
```
public static String toString(int fieldUpdateCultureSource)
```




**Parameters:**
| Parameter | Type | Description |
| --- | --- | --- |
| fieldUpdateCultureSource | int |  |

**Returns:**
java.lang.String
