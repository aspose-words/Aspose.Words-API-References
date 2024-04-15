---
title: JsonSimpleValueParseMode
linktitle: JsonSimpleValueParseMode
second_title: Aspose.Words for Java
description: Specifies a mode for parsing JSON simple values null boolean number integer and string while loading JSON in Java.
type: docs
weight: 378
url: /java/com.aspose.words/jsonsimplevalueparsemode/
---

**Inheritance:**
java.lang.Object
```
public class JsonSimpleValueParseMode
```

Specifies a mode for parsing JSON simple values (null, boolean, number, integer, and string) while loading JSON. Such a mode does not affect parsing of date-time values.
## Fields

| Field | Description |
| --- | --- |
| [LOOSE](#LOOSE) | Specifies the mode where types of JSON simple values are determined upon parsing of their string representations. |
| [STRICT](#STRICT) | Specifies the mode where types of JSON simple values are determined from JSON notation itself. |
| [length](#length) |  |
## Methods

| Method | Description |
| --- | --- |
| [fromName(String jsonSimpleValueParseModeName)](#fromName-java.lang.String) |  |
| [getName(int jsonSimpleValueParseMode)](#getName-int) |  |
| [getValues()](#getValues) |  |
| [toString(int jsonSimpleValueParseMode)](#toString-int) |  |
### LOOSE {#LOOSE}
```
public static int LOOSE
```


Specifies the mode where types of JSON simple values are determined upon parsing of their string representations. For example, the type of 'prop' from the JSON snippet '\{ prop: "123" \}' is determined as integer in this mode.

### STRICT {#STRICT}
```
public static int STRICT
```


Specifies the mode where types of JSON simple values are determined from JSON notation itself. For example, the type of 'prop' from the JSON snippet '\{ prop: "123" \}' is determined as string in this mode.

### length {#length}
```
public static int length
```


### fromName(String jsonSimpleValueParseModeName) {#fromName-java.lang.String}
```
public static int fromName(String jsonSimpleValueParseModeName)
```




**Parameters:**
| Parameter | Type | Description |
| --- | --- | --- |
| jsonSimpleValueParseModeName | java.lang.String |  |

**Returns:**
int
### getName(int jsonSimpleValueParseMode) {#getName-int}
```
public static String getName(int jsonSimpleValueParseMode)
```




**Parameters:**
| Parameter | Type | Description |
| --- | --- | --- |
| jsonSimpleValueParseMode | int |  |

**Returns:**
java.lang.String
### getValues() {#getValues}
```
public static int[] getValues()
```




**Returns:**
int[]
### toString(int jsonSimpleValueParseMode) {#toString-int}
```
public static String toString(int jsonSimpleValueParseMode)
```




**Parameters:**
| Parameter | Type | Description |
| --- | --- | --- |
| jsonSimpleValueParseMode | int |  |

**Returns:**
java.lang.String
