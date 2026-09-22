---
title: "ImportFormatMode"
linktitle: "ImportFormatMode"
second_title: "Aspose.Words لـ Java"
description: "يحدد كيفية دمج التنسيق عند استيراد المحتوى من مستند آخر في جافا."
type: docs
weight: 400
url: /ar/java/com.aspose.words/importformatmode/
---

**Inheritance:**
java.lang.Object
```
public class ImportFormatMode
```

يحدد كيفية دمج التنسيق عند استيراد المحتوى من مستند آخر.

 **Remarks:** 

عند نسخ العقد من مستند إلى آخر، يحدد هذا الخيار كيفية حل التنسيق عندما يحتوي المستندان على نمط بنفس الاسم ولكن بتنسيق مختلف.

يتم حل التنسيق كما يلي:

1. يتم مطابقة الأنماط المدمجة باستخدام معرف النمط المستقل عن اللغة. يتم مطابقة الأنماط المعرفة من قبل المستخدم باستخدام اسم النمط حسّاس لحالة الأحرف.
2. إذا لم يتم العثور على نمط مطابق في المستند الوجهة، يتم نسخ النمط (وجميع الأنماط المشار إليها) إلى المستند الوجهة ويتم تحديث العقد المستوردة للإشارة إلى النمط الجديد.
3. إذا كان هناك نمط مطابق موجود بالفعل في المستند الوجهة، فإن ما يحدث يعتمد على معامل  importFormatMode  الممرَّر إلى **M:Aspose.Words.DocumentBase.ImportNode(Aspose.Words.Node,System.Boolean,Aspose.Words.ImportFormatMode)** كما هو موضح أدناه.

عند استخدام خيار [USE\\_DESTINATION\\_STYLES](../../com.aspose.words/importformatmode/\\#USE-DESTINATION-STYLES)، إذا كان هناك نمط مطابق موجود بالفعل في المستند الوجهة، فلن يتم نسخ النمط وتُحدَّث العقد المستوردة للإشارة إلى النمط الموجود.

العيب في استخدام [USE\\_DESTINATION\\_STYLES](../../com.aspose.words/importformatmode/\\#USE-DESTINATION-STYLES) هو أن النص المستورد قد يبدو مختلفًا في المستند الوجهة مقارنة بالمستند المصدر. على سبيل المثال، النمط \"Heading 1\" في المستند المصدر يستخدم خط Arial بحجم 16pt بينما النمط \"Heading 1\" في المستند الوجهة يستخدم خط Times New Roman بحجم 14pt. عند استيراد نص بنمط \"Heading 1\" دون أي تنسيق مباشر آخر، سيظهر كخط Times New Roman بحجم 14pt في المستند الوجهة.

[KEEP\_SOURCE\_FORMATTING](../../com.aspose.words/importformatmode/\#KEEP-SOURCE-FORMATTING) option allows to make sure the imported content looks the same in the destination document like it looks in the source document. If a matching style already exists in the destination document, the source style formatting is expanded into direct Node attributes and the style is changed to Normal. If the style does not exist in the destination document, then the source style is imported into the destination document and applied to the imported node. Note, that it is not always possible to preserve the source style even if it does not exist in the destination document. In this case formatting of such style will be expanded into direct Node attributes in favor of preserving original Node formatting.

العيب في استخدام [KEEP\\_SOURCE\\_FORMATTING](../../com.aspose.words/importformatmode/\\#KEEP-SOURCE-FORMATTING) هو أنه إذا قمت بإجراء عدة عمليات استيراد، قد ينتهي بك الأمر إلى وجود العديد من الأنماط في المستند الوجهة وهذا قد يجعل من الصعب استخدام تنسيق نمط متسق في Microsoft Word لهذا المستند.

استخدام خيار [KEEP\\_DIFFERENT\\_STYLES](../../com.aspose.words/importformatmode/\\#KEEP-DIFFERENT-STYLES) يسمح بإعادة استخدام أنماط الوجهة إذا كان التنسيق الذي تقدمه مطابقة للأنماط في المستند المصدر. إذا كان النمط في المستند الوجهة مختلفًا عن المصدر فسيتم استيراده.

 **Examples:** 

يعرض كيفية إدراج مستند داخل مستند آخر.

```

 Document doc = new Document(getMyDir() + "Document.docx");

 DocumentBuilder builder = new DocumentBuilder(doc);
 builder.moveToDocumentEnd();
 builder.insertBreak(BreakType.PAGE_BREAK);

 Document docToInsert = new Document(getMyDir() + "Formatted elements.docx");

 builder.insertDocument(docToInsert, ImportFormatMode.KEEP_SOURCE_FORMATTING);
 builder.getDocument().save(getArtifactsDir() + "DocumentBuilder.InsertDocument.docx");
 
```

**M:Aspose.Words.DocumentBase.ImportNode(Aspose.Words.Node,System.Boolean,Aspose.Words.ImportFormatMode)**
## الحقول

| حقل | الوصف |
| --- | --- |
| [KEEP_DIFFERENT_STYLES](#KEEP-DIFFERENT-STYLES) | انسخ فقط الأنماط التي تختلف عن تلك الموجودة في المستند المصدر. |
| [KEEP_SOURCE_FORMATTING](#KEEP-SOURCE-FORMATTING) | انسخ جميع الأنماط المطلوبة إلى المستند الوجهة، وأنشئ أسماء أنماط فريدة إذا لزم الأمر. |
| [USE_DESTINATION_STYLES](#USE-DESTINATION-STYLES) | استخدم أنماط المستند الوجهة وانسخ الأنماط الجديدة. |
| [length](#length) |  |
## الطرق

| طريقة | الوصف |
| --- | --- |
| [fromName(String importFormatModeName)](#fromName-java.lang.String) |  |
| [getName(int importFormatMode)](#getName-int) |  |
| [getValues()](#getValues) |  |
| [toString(int importFormatMode)](#toString-int) |  |
### KEEP_DIFFERENT_STYLES {#KEEP-DIFFERENT-STYLES}
```
public static int KEEP_DIFFERENT_STYLES
```


انسخ فقط الأنماط التي تختلف عن تلك الموجودة في المستند المصدر.

### KEEP_SOURCE_FORMATTING {#KEEP-SOURCE-FORMATTING}
```
public static int KEEP_SOURCE_FORMATTING
```


انسخ جميع الأنماط المطلوبة إلى المستند الوجهة، وأنشئ أسماء أنماط فريدة إذا لزم الأمر.

### USE_DESTINATION_STYLES {#USE-DESTINATION-STYLES}
```
public static int USE_DESTINATION_STYLES
```


استخدم أنماط المستند الوجهة وانسخ الأنماط الجديدة. هذا هو الخيار الافتراضي.

### length {#length}
```
public static int length
```


### fromName(String importFormatModeName) {#fromName-java.lang.String}
```
public static int fromName(String importFormatModeName)
```




**Parameters:**
| معامل | نوع | الوصف |
| --- | --- | --- |
| importFormatModeName | java.lang.String |  |

**Returns:**
int
### getName(int importFormatMode) {#getName-int}
```
public static String getName(int importFormatMode)
```




**Parameters:**
| معامل | نوع | الوصف |
| --- | --- | --- |
| importFormatMode | int |  |

**Returns:**
java.lang.String
### getValues() {#getValues}
```
public static int[] getValues()
```




**Returns:**
int[]
### toString(int importFormatMode) {#toString-int}
```
public static String toString(int importFormatMode)
```




**Parameters:**
| معامل | نوع | الوصف |
| --- | --- | --- |
| importFormatMode | int |  |

**Returns:**
java.lang.String
