---
title: "ScriptShapingLevel"
linktitle: "ScriptShapingLevel"
second_title: "Aspose.Words لـ Java"
description: "يصف مستويات التشكيل المطلوبة بواسطة سكريبت في Java."
type: docs
weight: 598
url: /ar/java/com.aspose.words/scriptshapinglevel/
---

**Inheritance:**
java.lang.Object
```
public class ScriptShapingLevel
```

يصف مستويات التشكيل المطلوبة بواسطة البرنامج النصي.
## الحقول

| حقل | الوصف |
| --- | --- |
| [FULL](#FULL) | يتطلب السكريبت دعم تشكيل كامل. |
| [MINIMUM](#MINIMUM) | يتطلب السكريبت الحد الأدنى من دعم التشكيل. |
| [NONE](#NONE) | السكريبت لا يتطلب تشكيلًا. |
| [UNKNOWN](#UNKNOWN) | يُستخدم هذا عندما لا يتم تحديد مستوى النص البرمجي. |
| [length](#length) |  |
## الطرق

| طريقة | الوصف |
| --- | --- |
| [fromName(String scriptShapingLevelName)](#fromName-java.lang.String) |  |
| [getName(int scriptShapingLevel)](#getName-int) |  |
| [getValues()](#getValues) |  |
| [toString(int scriptShapingLevel)](#toString-int) |  |
### FULL {#FULL}
```
public static int FULL
```


يتطلب السكريبت دعم تشكيل كامل.

### MINIMUM {#MINIMUM}
```
public static int MINIMUM
```


يتطلب السكريبت الحد الأدنى من دعم التشكيل.

 **Remarks:** 

ليس واضحًا ما يعنيه الحد الأدنى. يتم تعيين الحد الأدنى لبعض النصوص البرمجية الشهيرة (لاتينية، سيريالية...).

### NONE {#NONE}
```
public static int NONE
```


السكريبت لا يتطلب تشكيلًا.

### UNKNOWN {#UNKNOWN}
```
public static int UNKNOWN
```


يُستخدم هذا عندما لا يتم تحديد مستوى النص البرمجي.

 **Remarks:** 

يجب ألا يحدث ذلك.

### length {#length}
```
public static int length
```


### fromName(String scriptShapingLevelName) {#fromName-java.lang.String}
```
public static int fromName(String scriptShapingLevelName)
```




**Parameters:**
| معامل | نوع | الوصف |
| --- | --- | --- |
| scriptShapingLevelName | java.lang.String |  |

**Returns:**
int
### getName(int scriptShapingLevel) {#getName-int}
```
public static String getName(int scriptShapingLevel)
```




**Parameters:**
| معامل | نوع | الوصف |
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
| معامل | نوع | الوصف |
| --- | --- | --- |
| scriptShapingLevel | int |  |

**Returns:**
java.lang.String
