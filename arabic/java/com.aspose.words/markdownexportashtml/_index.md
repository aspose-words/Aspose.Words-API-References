---
title: "MarkdownExportAsHtml"
linktitle: "MarkdownExportAsHtml"
second_title: "Aspose.Words لـ Java"
description: "يسمح بتحديد العناصر التي سيتم تصديرها إلى Markdown كـ HTML خام في Java."
type: docs
weight: 451
url: /ar/java/com.aspose.words/markdownexportashtml/
---

**Inheritance:**
java.lang.Object
```
public class MarkdownExportAsHtml
```

يسمح بتحديد العناصر التي سيتم تصديرها إلى Markdown كـ HTML خام.

 **Examples:** 

يعرض كيفية تصدير جدول إلى Markdown كـ HTML خام.

```

 Document doc = new Document();
 DocumentBuilder builder = new DocumentBuilder(doc);

 builder.writeln("Sample table:");

 // Create table.
 builder.insertCell();
 builder.getParagraphFormat().setAlignment(ParagraphAlignment.RIGHT);
 builder.write("Cell1");
 builder.insertCell();
 builder.getParagraphFormat().setAlignment(ParagraphAlignment.CENTER);
 builder.write("Cell2");

 MarkdownSaveOptions saveOptions = new MarkdownSaveOptions();
 saveOptions.setExportAsHtml(MarkdownExportAsHtml.TABLES);

 doc.save(getArtifactsDir() + "MarkdownSaveOptions.ExportTableAsHtml.md", saveOptions);
 
```

يعرض كيفية تصدير الجداول التي لا يمكن تمثيلها بشكل صحيح في Markdown النقي كـ HTML خام.

```

 String outputPath = getArtifactsDir() + "MarkdownSaveOptions.NonCompatibleTables.md";

 Document doc = new Document(getMyDir() + "Non compatible table.docx");

 // With the "NonCompatibleTables" option, you can export tables that have a complex structure with merged cells
 // or nested tables to raw HTML and leave simple tables in Markdown format.
 MarkdownSaveOptions saveOptions = new MarkdownSaveOptions();
 saveOptions.setExportAsHtml(MarkdownExportAsHtml.NON_COMPATIBLE_TABLES);

 doc.save(outputPath, saveOptions);
 
```
## الحقول

| حقل | الوصف |
| --- | --- |
| [NONE](#NONE) | تصدير جميع العناصر باستخدام صيغة Markdown دون أي HTML خام. |
| [NON_COMPATIBLE_TABLES](#NON-COMPATIBLE-TABLES) | يعرض كيفية تصدير الجداول التي لا يمكن تمثيلها بشكل صحيح في Markdown النقي كـ HTML خام. |
| [TABLES](#TABLES) | تصدير الجداول كـ HTML خام. |
| [length](#length) |  |
## الطرق

| طريقة | الوصف |
| --- | --- |
| [fromName(String markdownExportAsHtmlName)](#fromName-java.lang.String) |  |
| [fromNames(Set markdownExportAsHtmlNames)](#fromNames-java.util.Set) |  |
| [getName(int markdownExportAsHtml)](#getName-int) |  |
| [getNames(int markdownExportAsHtml)](#getNames-int) |  |
| [getValues()](#getValues) |  |
| [toString(int markdownExportAsHtml)](#toString-int) |  |
| [toStringSet(int attr)](#toStringSet-int) |  |
### NONE {#NONE}
```
public static int NONE
```


تصدير جميع العناصر باستخدام صيغة Markdown دون أي HTML خام.

### NON_COMPATIBLE_TABLES {#NON-COMPATIBLE-TABLES}
```
public static int NON_COMPATIBLE_TABLES
```


يعرض كيفية تصدير الجداول التي لا يمكن تمثيلها بشكل صحيح في Markdown النقي كـ HTML خام.

 **Remarks:** 

عند تفعيل هذا الخيار، سيقوم Aspose.Words بتصدير الجداول التي تحتوي على خلايا مدمجة أو جداول متداخلة فقط كـ HTML خام. وستُصدَّر جميع الجداول الأخرى بصيغة Markdown. كما يجب ملاحظة أن هذا الخيار لن يحافظ على جميع تنسيقات الجدول، بل سيحافظ فقط على الفواصل المقابلة للخلايا.

إذا تم تعيين علم [TABLES](../../com.aspose.words/markdownexportashtml/\#TABLES) المتعلق، فسيتم تجاهل هذا العلم.

### TABLES {#TABLES}
```
public static int TABLES
```


تصدير الجداول كـ HTML خام.

 **Remarks:** 

عند تفعيل هذا الخيار، سيتم تصدير كل جدول كـ HTML خام. سيحاول Aspose.Words الحفاظ على جميع تنسيقات الجداول في هذه الحالة.

إذا تم تعيين هذا العلم، فسيتم تجاهل علم [NON\_COMPATIBLE\_TABLES](../../com.aspose.words/markdownexportashtml/\#NON-COMPATIBLE-TABLES) المتعلق.

### length {#length}
```
public static int length
```


### fromName(String markdownExportAsHtmlName) {#fromName-java.lang.String}
```
public static int fromName(String markdownExportAsHtmlName)
```




**Parameters:**
| معامل | نوع | الوصف |
| --- | --- | --- |
| markdownExportAsHtmlName | java.lang.String |  |

**Returns:**
int
### fromNames(Set markdownExportAsHtmlNames) {#fromNames-java.util.Set}
```
public static int fromNames(Set markdownExportAsHtmlNames)
```




**Parameters:**
| معامل | نوع | الوصف |
| --- | --- | --- |
| markdownExportAsHtmlNames | java.util.Set |  |

**Returns:**
int
### getName(int markdownExportAsHtml) {#getName-int}
```
public static String getName(int markdownExportAsHtml)
```




**Parameters:**
| معامل | نوع | الوصف |
| --- | --- | --- |
| markdownExportAsHtml | int |  |

**Returns:**
java.lang.String
### getNames(int markdownExportAsHtml) {#getNames-int}
```
public static Set getNames(int markdownExportAsHtml)
```




**Parameters:**
| معامل | نوع | الوصف |
| --- | --- | --- |
| markdownExportAsHtml | int |  |

**Returns:**
java.util.Set
### getValues() {#getValues}
```
public static int[] getValues()
```




**Returns:**
int[]
### toString(int markdownExportAsHtml) {#toString-int}
```
public static String toString(int markdownExportAsHtml)
```




**Parameters:**
| معامل | نوع | الوصف |
| --- | --- | --- |
| markdownExportAsHtml | int |  |

**Returns:**
java.lang.String
### toStringSet(int attr) {#toStringSet-int}
```
public static String toStringSet(int attr)
```




**Parameters:**
| معامل | نوع | الوصف |
| --- | --- | --- |
| attr | int |  |

**Returns:**
java.lang.String
