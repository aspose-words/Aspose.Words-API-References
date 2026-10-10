---
title: "BaselineAlignment"
linktitle: "BaselineAlignment"
second_title: "Aspose.Words لـ Java"
description: "يحدد الموضع العمودي للخطوط على سطر في Java."
type: docs
weight: 36
url: /ar/java/com.aspose.words/baselinealignment/
---

**Inheritance:**
java.lang.Object
```
public class BaselineAlignment
```

يحدد الموضع الرأسي للخطوط على السطر.

 **Examples:** 

يظهر كيفية ضبط الموضع العمودي للخطوط على سطر.

```

 Document doc = new Document(getMyDir() + "Office math.docx");

 ParagraphFormat format = doc.getFirstSection().getBody().getParagraphs().get(0).getParagraphFormat();
 if (format.getBaselineAlignment() == BaselineAlignment.AUTO)
 {
     format.setBaselineAlignment(BaselineAlignment.TOP);
 }

 doc.save(getArtifactsDir() + "ParagraphFormat.ParagraphBaselineAlignment.docx");
 
```
## الحقول

| حقل | الوصف |
| --- | --- |
| [AUTO](#AUTO) | يتم تعديل الخط الأساسي تلقائيًا. |
| [BASELINE](#BASELINE) | محاذاة إلى الخط الأساسي للفقرة. |
| [BOTTOM](#BOTTOM) | محاذاة إلى أسفل كل خط. |
| [CENTER](#CENTER) | محاذاة نقاط المركز لكل خط. |
| [TOP](#TOP) | محاذاة على أعلى كل خط. |
| [length](#length) |  |
## الطرق

| طريقة | الوصف |
| --- | --- |
| [fromName(String baselineAlignmentName)](#fromName-java.lang.String) |  |
| [getName(int baselineAlignment)](#getName-int) |  |
| [getValues()](#getValues) |  |
| [toString(int baselineAlignment)](#toString-int) |  |
### AUTO {#AUTO}
```
public static int AUTO
```


يتم تعديل الخط الأساسي تلقائيًا.

### BASELINE {#BASELINE}
```
public static int BASELINE
```


محاذاة إلى الخط الأساسي للفقرة.

### BOTTOM {#BOTTOM}
```
public static int BOTTOM
```


محاذاة إلى أسفل كل خط.

### CENTER {#CENTER}
```
public static int CENTER
```


محاذاة نقاط المركز لكل خط.

### TOP {#TOP}
```
public static int TOP
```


محاذاة على أعلى كل خط.

### length {#length}
```
public static int length
```


### fromName(String baselineAlignmentName) {#fromName-java.lang.String}
```
public static int fromName(String baselineAlignmentName)
```




**Parameters:**
| معامل | نوع | الوصف |
| --- | --- | --- |
| baselineAlignmentName | java.lang.String |  |

**Returns:**
int
### getName(int baselineAlignment) {#getName-int}
```
public static String getName(int baselineAlignment)
```




**Parameters:**
| معامل | نوع | الوصف |
| --- | --- | --- |
| baselineAlignment | int |  |

**Returns:**
java.lang.String
### getValues() {#getValues}
```
public static int[] getValues()
```




**Returns:**
int[]
### toString(int baselineAlignment) {#toString-int}
```
public static String toString(int baselineAlignment)
```




**Parameters:**
| معامل | نوع | الوصف |
| --- | --- | --- |
| baselineAlignment | int |  |

**Returns:**
java.lang.String
