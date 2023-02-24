---
title: NumeralFormat
linktitle: NumeralFormat
second_title: Aspose.Words for Java API Reference
description: Indicates the symbol set that is used to represent numbers while rendering to fixed page formats in Java.
type: docs
weight: 416
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
| [equals(Object arg0)](#equals-java.lang.Object) |  |
| [fromName(String numeralFormatName)](#fromName-java.lang.String) |  |
| [getClass()](#getClass) |  |
| [getName(int numeralFormat)](#getName-int) |  |
| [getValues()](#getValues) |  |
| [hashCode()](#hashCode) |  |
| [notify()](#notify) |  |
| [notifyAll()](#notifyAll) |  |
| [toString()](#toString) |  |
| [toString(int numeralFormat)](#toString-int) |  |
| [wait()](#wait) |  |
| [wait(long arg0)](#wait-long) |  |
| [wait(long arg0, int arg1)](#wait-long-int) |  |
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
### getClass() {#getClass}
```
public final native Class<?> getClass()
```




**Returns:**
java.lang.Class<?>
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
### hashCode() {#hashCode}
```
public native int hashCode()
```




**Returns:**
int
### notify() {#notify}
```
public final native void notify()
```




### notifyAll() {#notifyAll}
```
public final native void notifyAll()
```




### toString() {#toString}
```
public String toString()
```




**Returns:**
java.lang.String
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

