---
title: "MergeFormatMode"
linktitle: "MergeFormatMode"
second_title: "Aspose.Words لـ Java"
description: "يحدد كيفية دمج التنسيق عند دمج مستندات متعددة في Java."
type: docs
weight: 464
url: /ar/java/com.aspose.words/mergeformatmode/
---

**Inheritance:**
java.lang.Object
```
public class MergeFormatMode
```

يحدد كيفية دمج التنسيق عند دمج مستندات متعددة.

 **Examples:** 

يوضح كيفية دمج المستندات في مستند إخراج واحد.

```

 //There is a several ways to merge documents:
 String inputDoc1 = getMyDir() + "Big document.docx";
 String inputDoc2 = getMyDir() + "Tables.docx";

 Merger.merge(getArtifactsDir() + "LowCode.MergeDocument.1.docx", new String[]{inputDoc1, inputDoc2});

 OoxmlSaveOptions saveOptions = new OoxmlSaveOptions();
 {
     saveOptions.setPassword("Aspose.Words");
 }
 Merger.merge(getArtifactsDir() + "LowCode.MergeDocument.2.docx", new String[]{inputDoc1, inputDoc2}, saveOptions, MergeFormatMode.KEEP_SOURCE_FORMATTING);

 Merger.merge(getArtifactsDir() + "LowCode.MergeDocument.3.pdf", new String[]{inputDoc1, inputDoc2}, SaveFormat.PDF, MergeFormatMode.KEEP_SOURCE_LAYOUT);

 LoadOptions firstLoadOptions = new LoadOptions();
 {
     firstLoadOptions.setIgnoreOleData(true);
 }
 LoadOptions secondLoadOptions = new LoadOptions();
 {
     secondLoadOptions.setIgnoreOleData(false);
 }
 Merger.merge(getArtifactsDir() + "LowCode.MergeDocument.4.docx", new String[]{inputDoc1, inputDoc2}, new LoadOptions[]{firstLoadOptions, secondLoadOptions},
         saveOptions, MergeFormatMode.KEEP_SOURCE_FORMATTING);

 Document doc = Merger.merge(new String[]{inputDoc1, inputDoc2}, MergeFormatMode.MERGE_FORMATTING);
 doc.save(getArtifactsDir() + "LowCode.MergeDocument.5.docx");

 doc = Merger.merge(new String[]{inputDoc1, inputDoc2}, new LoadOptions[]{firstLoadOptions, secondLoadOptions}, MergeFormatMode.MERGE_FORMATTING);
 doc.save(getArtifactsDir() + "LowCode.MergeDocument.6.docx");
 
```
## الحقول

| حقل | الوصف |
| --- | --- |
| [KEEP_SOURCE_FORMATTING](#KEEP-SOURCE-FORMATTING) | يعني أن المستند المصدر سيحتفظ بالتنسيق الأصلي له، مثل أنماط الخطوط، الأحجام، الألوان، المسافات البادئة، وأي عناصر تنسيق أخرى تم تطبيقها على محتواه. |
| [KEEP_SOURCE_LAYOUT](#KEEP-SOURCE-LAYOUT) | حافظ على تخطيط المستندات الأصلية في المستند النهائي. |
| [MERGE_FORMATTING](#MERGE-FORMATTING) | اجمع تنسيق المستندات المدمجة. |
| [length](#length) |  |
## الطرق

| طريقة | الوصف |
| --- | --- |
| [fromName(String mergeFormatModeName)](#fromName-java.lang.String) |  |
| [getName(int mergeFormatMode)](#getName-int) |  |
| [getValues()](#getValues) |  |
| [toString(int mergeFormatMode)](#toString-int) |  |
### KEEP_SOURCE_FORMATTING {#KEEP-SOURCE-FORMATTING}
```
public static int KEEP_SOURCE_FORMATTING
```


يعني أن المستند المصدر سيحتفظ بالتنسيق الأصلي له، مثل أنماط الخطوط، الأحجام، الألوان، المسافات البادئة، وأي عناصر تنسيق أخرى تم تطبيقها على محتواه.

 **Remarks:** 

باستخدام هذا الخيار، تضمن أن المحتوى المنسوخ يظهر كما كان في المصدر الأصلي، بغض النظر عن إعدادات التنسيق للمستند الأول في طابور الدمج.

هذا الخيار لا يؤثر عندما تكون صيغ الإدخال والإخراج هي PDF.

### KEEP_SOURCE_LAYOUT {#KEEP-SOURCE-LAYOUT}
```
public static int KEEP_SOURCE_LAYOUT
```


حافظ على تخطيط المستندات الأصلية في المستند النهائي.

 **Remarks:** 

عمومًا، يبدو الأمر كما لو أنك تطبع المستندات الأصلية وتلصقها يدويًا معًا باستخدام الغراء.

### MERGE_FORMATTING {#MERGE-FORMATTING}
```
public static int MERGE_FORMATTING
```


اجمع تنسيق المستندات المدمجة.

 **Remarks:** 

باستخدام هذا الخيار، تقوم Aspose.Words بتكييف تنسيق المستند الأول ليتطابق مع بنية ومظهر المستند الثاني، مع الحفاظ على بعض التنسيقات الأصلية دون تغيير. هذا الخيار مفيد عندما تريد الحفاظ على المظهر العام للمستند الهدف مع الاحتفاظ ببعض جوانب التنسيق من المستند الأصلي.

هذا الخيار لا يؤثر عندما تكون صيغ الإدخال والإخراج هي PDF.

### length {#length}
```
public static int length
```


### fromName(String mergeFormatModeName) {#fromName-java.lang.String}
```
public static int fromName(String mergeFormatModeName)
```




**Parameters:**
| معامل | نوع | الوصف |
| --- | --- | --- |
| mergeFormatModeName | java.lang.String |  |

**Returns:**
int
### getName(int mergeFormatMode) {#getName-int}
```
public static String getName(int mergeFormatMode)
```




**Parameters:**
| معامل | نوع | الوصف |
| --- | --- | --- |
| mergeFormatMode | int |  |

**Returns:**
java.lang.String
### getValues() {#getValues}
```
public static int[] getValues()
```




**Returns:**
int[]
### toString(int mergeFormatMode) {#toString-int}
```
public static String toString(int mergeFormatMode)
```




**Parameters:**
| معامل | نوع | الوصف |
| --- | --- | --- |
| mergeFormatMode | int |  |

**Returns:**
java.lang.String
