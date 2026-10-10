---
title: "JustificationMode"
linktitle: "JustificationMode"
second_title: "Aspose.Words لـ Java"
description: "يحدد تعديل تباعد الأحرف لمستند في جافا."
type: docs
weight: 411
url: /ar/java/com.aspose.words/justificationmode/
---

**Inheritance:**
java.lang.Object
```
public class JustificationMode
```

يحدد تعديل تباعد الأحرف لمستند. القيمة الافتراضية هي Expand.

 **Examples:** 

يعرض كيفية إدارة التحكم في تباعد الأحرف.

```

 Document doc = new Document(getMyDir() + "Document.docx");

 int justificationMode = doc.getJustificationMode();
 if (justificationMode == JustificationMode.EXPAND)
     doc.setJustificationMode(JustificationMode.COMPRESS);

 doc.save(getArtifactsDir() + "Document.SetJustificationMode.docx");
 
```
## الحقول

| حقل | الوصف |
| --- | --- |
| [COMPRESS](#COMPRESS) | ضغط تباعد الأحرف. |
| [COMPRESS_KANA](#COMPRESS-KANA) | ضغط، باستخدام قواعد مقاطع الكانا، هيراغانا وكاتاكانا. |
| [EXPAND](#EXPAND) | لا تقم بضغط تباعد الأحرف. |
| [length](#length) |  |
## الطرق

| طريقة | الوصف |
| --- | --- |
| [fromName(String justificationModeName)](#fromName-java.lang.String) |  |
| [getName(int justificationMode)](#getName-int) |  |
| [getValues()](#getValues) |  |
| [toString(int justificationMode)](#toString-int) |  |
### COMPRESS {#COMPRESS}
```
public static int COMPRESS
```


ضغط تباعد الأحرف.

### COMPRESS_KANA {#COMPRESS-KANA}
```
public static int COMPRESS_KANA
```


ضغط، باستخدام قواعد مقاطع الكانا، هيراغانا وكاتاكانا.

### EXPAND {#EXPAND}
```
public static int EXPAND
```


لا تقم بضغط تباعد الأحرف.

### length {#length}
```
public static int length
```


### fromName(String justificationModeName) {#fromName-java.lang.String}
```
public static int fromName(String justificationModeName)
```




**Parameters:**
| معامل | نوع | الوصف |
| --- | --- | --- |
| justificationModeName | java.lang.String |  |

**Returns:**
int
### getName(int justificationMode) {#getName-int}
```
public static String getName(int justificationMode)
```




**Parameters:**
| معامل | نوع | الوصف |
| --- | --- | --- |
| justificationMode | int |  |

**Returns:**
java.lang.String
### getValues() {#getValues}
```
public static int[] getValues()
```




**Returns:**
int[]
### toString(int justificationMode) {#toString-int}
```
public static String toString(int justificationMode)
```




**Parameters:**
| معامل | نوع | الوصف |
| --- | --- | --- |
| justificationMode | int |  |

**Returns:**
java.lang.String
