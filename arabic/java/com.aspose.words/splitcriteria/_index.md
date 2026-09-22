---
title: "SplitCriteria"
linktitle: "SplitCriteria"
second_title: "Aspose.Words لـ Java"
description: "يحدد كيفية تقسيم المستند إلى أجزاء في Java."
type: docs
weight: 629
url: /ar/java/com.aspose.words/splitcriteria/
---

**Inheritance:**
java.lang.Object
```
public class SplitCriteria
```

يحدد كيفية تقسيم المستند إلى أجزاء.

 **Examples:** 

يوضح كيفية تقسيم المستند حسب الصفحات.

```

 String doc = getMyDir() + "Big document.docx";

 SplitOptions options = new SplitOptions();
 options.setSplitCriteria(SplitCriteria.PAGE);
 Splitter.split(doc, getArtifactsDir() + "LowCode.SplitDocument.1.docx", options);
 Splitter.split(doc, getArtifactsDir() + "LowCode.SplitDocument.2.docx", SaveFormat.DOCX, options);
 
```
## الحقول

| حقل | الوصف |
| --- | --- |
| [PAGE](#PAGE) | يحدد أن المستند يتم تقسيمه إلى صفحات. |
| [SECTION_BREAK](#SECTION-BREAK) | يحدد أن المستند يتم تقسيمه إلى أجزاء عند فاصل قسم من أي نوع. |
| [STYLE](#STYLE) | يحدد أن المستند يتم تقسيمه إلى أجزاء عند فقرة مُنسقة باستخدام النمط المحدد في [SplitOptions.getSplitStyle()](../../com.aspose.words/splitoptions/\#getSplitStyle) / [SplitOptions.setSplitStyle(java.lang.String)](../../com.aspose.words/splitoptions/\#setSplitStyle-java.lang.String). |
| [length](#length) |  |
## الطرق

| طريقة | الوصف |
| --- | --- |
| [fromName(String splitCriteriaName)](#fromName-java.lang.String) |  |
| [getName(int splitCriteria)](#getName-int) |  |
| [getValues()](#getValues) |  |
| [toString(int splitCriteria)](#toString-int) |  |
### PAGE {#PAGE}
```
public static int PAGE
```


يحدد أن المستند يتم تقسيمه إلى صفحات.

### SECTION_BREAK {#SECTION-BREAK}
```
public static int SECTION_BREAK
```


يحدد أن المستند يتم تقسيمه إلى أجزاء عند فاصل قسم من أي نوع.

### STYLE {#STYLE}
```
public static int STYLE
```


يحدد أن المستند يتم تقسيمه إلى أجزاء عند فقرة مُنسقة باستخدام النمط المحدد في [SplitOptions.getSplitStyle()](../../com.aspose.words/splitoptions/\#getSplitStyle) / [SplitOptions.setSplitStyle(java.lang.String)](../../com.aspose.words/splitoptions/\#setSplitStyle-java.lang.String).

### length {#length}
```
public static int length
```


### fromName(String splitCriteriaName) {#fromName-java.lang.String}
```
public static int fromName(String splitCriteriaName)
```




**Parameters:**
| معامل | نوع | الوصف |
| --- | --- | --- |
| splitCriteriaName | java.lang.String |  |

**Returns:**
int
### getName(int splitCriteria) {#getName-int}
```
public static String getName(int splitCriteria)
```




**Parameters:**
| معامل | نوع | الوصف |
| --- | --- | --- |
| splitCriteria | int |  |

**Returns:**
java.lang.String
### getValues() {#getValues}
```
public static int[] getValues()
```




**Returns:**
int[]
### toString(int splitCriteria) {#toString-int}
```
public static String toString(int splitCriteria)
```




**Parameters:**
| معامل | نوع | الوصف |
| --- | --- | --- |
| splitCriteria | int |  |

**Returns:**
java.lang.String
