---
title: NumeralFormat
linktitle: NumeralFormat
second_title: Aspose.Words for Java
description: Indicates the symbol set that is used to represent numbers while rendering to fixed page formats in Java.
type: docs
weight: 431
url: /java/com.aspose.words/numeralformat/
---

**Inheritance:**
java.lang.Object
```
public class NumeralFormat
```

Indicates the symbol set that is used to represent numbers while rendering to fixed page formats.
## Fields

| Field | Description |
| --- | --- |
| [ARABIC_INDIC](#ARABIC-INDIC) | Numerals used in Arabic: \\u0660\\u0661\\u0662\\u0663\\u0664\\u0665\\u0666\\u0667\\u0668\\u0669. |
| [CONTEXT](#CONTEXT) | Symbol set is decided from context(locale and RTL property). |
| [EASTERN_ARABIC_INDIC](#EASTERN-ARABIC-INDIC) | Numerals used in Persian and Urdu: \\u06f0\\u06f1\\u06f2\\u06f3\\u06f4\\u06f5\\u06f6\\u06f7\\u06f8\\u06f9. |
| [EUROPEAN](#EUROPEAN) | European numerals: 0123456789. |
| [SYSTEM](#SYSTEM) | THIS OPTION IS NOT SUPPORTED. |
| [length](#length) |  |
## Methods

| Method | Description |
| --- | --- |
| [fromName(String numeralFormatName)](#fromName-java.lang.String) |  |
| [getName(int numeralFormat)](#getName-int) |  |
| [getValues()](#getValues) |  |
| [toString(int numeralFormat)](#toString-int) |  |
### ARABIC_INDIC {#ARABIC-INDIC}
```
public static int ARABIC_INDIC
```


Numerals used in Arabic: \\u0660\\u0661\\u0662\\u0663\\u0664\\u0665\\u0666\\u0667\\u0668\\u0669. Unicode range U+0660 - u+0669.

### CONTEXT {#CONTEXT}
```
public static int CONTEXT
```


Symbol set is decided from context(locale and RTL property).

### EASTERN_ARABIC_INDIC {#EASTERN-ARABIC-INDIC}
```
public static int EASTERN_ARABIC_INDIC
```


Numerals used in Persian and Urdu: \\u06f0\\u06f1\\u06f2\\u06f3\\u06f4\\u06f5\\u06f6\\u06f7\\u06f8\\u06f9. Unicode range U+06F0 - u+06F9.

### EUROPEAN {#EUROPEAN}
```
public static int EUROPEAN
```


European numerals: 0123456789.

### SYSTEM {#SYSTEM}
```
public static int SYSTEM
```


THIS OPTION IS NOT SUPPORTED. Symbol set is decided from regional settings.

### length {#length}
```
public static int length
```


### fromName(String numeralFormatName) {#fromName-java.lang.String}
```
public static int fromName(String numeralFormatName)
```




**Parameters:**
| Parameter | Type | Description |
| --- | --- | --- |
| numeralFormatName | java.lang.String |  |

**Returns:**
int
### getName(int numeralFormat) {#getName-int}
```
public static String getName(int numeralFormat)
```




**Parameters:**
| Parameter | Type | Description |
| --- | --- | --- |
| numeralFormat | int |  |

**Returns:**
java.lang.String
### getValues() {#getValues}
```
public static int[] getValues()
```




**Returns:**
int[]
### toString(int numeralFormat) {#toString-int}
```
public static String toString(int numeralFormat)
```




**Parameters:**
| Parameter | Type | Description |
| --- | --- | --- |
| numeralFormat | int |  |

**Returns:**
java.lang.String
