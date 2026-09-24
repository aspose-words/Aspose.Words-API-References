---
title: "ScriptShapingLevel"
linktitle: "ScriptShapingLevel"
second_title: "Aspose.Words Java için"
description: "Java'da bir betik tarafından gereken şekillendirme seviyelerini açıklar."
type: docs
weight: 598
url: /tr/java/com.aspose.words/scriptshapinglevel/
---

**Inheritance:**
java.lang.Object
```
public class ScriptShapingLevel
```

Bir betik tarafından gereken şekillendirme seviyelerini açıklar.
## Alanlar

| Alan | Açıklama |
| --- | --- |
| [FULL](#FULL) | Betik tam şekillendirme desteği gerektirir. |
| [MINIMUM](#MINIMUM) | Betik minimum şekillendirme desteği gerektirir. |
| [NONE](#NONE) | Betik şekillendirme gerektirmez. |
| [UNKNOWN](#UNKNOWN) | Bu, betik için seviye belirtilmediğinde kullanılır. |
| [length](#length) |  |
## Yöntemler

| Yöntem | Açıklama |
| --- | --- |
| [fromName(String scriptShapingLevelName)](#fromName-java.lang.String) |  |
| [getName(int scriptShapingLevel)](#getName-int) |  |
| [getValues()](#getValues) |  |
| [toString(int scriptShapingLevel)](#toString-int) |  |
### FULL {#FULL}
```
public static int FULL
```


Betik tam şekillendirme desteği gerektirir.

### MINIMUM {#MINIMUM}
```
public static int MINIMUM
```


Betik minimum şekillendirme desteği gerektirir.

 **Remarks:** 

Minimum'ın ne anlama geldiği net değil. Minimum, bazı çok popüler betikler (Latin, Kiril...) için ayarlanmıştır.

### NONE {#NONE}
```
public static int NONE
```


Betik şekillendirme gerektirmez.

### UNKNOWN {#UNKNOWN}
```
public static int UNKNOWN
```


Bu, betik için seviye belirtilmediğinde kullanılır.

 **Remarks:** 

Böyle bir şey olmamalı.

### length {#length}
```
public static int length
```


### fromName(String scriptShapingLevelName) {#fromName-java.lang.String}
```
public static int fromName(String scriptShapingLevelName)
```




**Parameters:**
| Parametre | Tür | Açıklama |
| --- | --- | --- |
| scriptShapingLevelName | java.lang.String |  |

**Returns:**
int
### getName(int scriptShapingLevel) {#getName-int}
```
public static String getName(int scriptShapingLevel)
```




**Parameters:**
| Parametre | Tür | Açıklama |
| --- | --- | --- |
| scriptShapingLevel | int |  |

**Returns:**
java.lang.String
### getValues() {#getValues}
```
public static int[] getValues()
```




**Returns:**
int[]
### toString(int scriptShapingLevel) {#toString-int}
```
public static String toString(int scriptShapingLevel)
```




**Parameters:**
| Parametre | Tür | Açıklama |
| --- | --- | --- |
| scriptShapingLevel | int |  |

**Returns:**
java.lang.String
