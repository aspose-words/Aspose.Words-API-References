---
title: "PdfCustomPropertiesExport"
linktitle: "PdfCustomPropertiesExport"
second_title: "Aspose.Words لـ Java"
description: "يحدد الطريقة التي يتم بها تصدير Document.getCustomDocumentProperties إلى ملف PDF في Java."
type: docs
weight: 530
url: /ar/java/com.aspose.words/pdfcustompropertiesexport/
---

**Inheritance:**
java.lang.Object
```
public class PdfCustomPropertiesExport
```

يحدد الطريقة التي يتم بها تصدير [Document.getCustomDocumentProperties()](../../com.aspose.words/document/\#getCustomDocumentProperties) إلى ملف PDF.

 **Examples:** 

يوضح كيفية تصدير الخصائص المخصصة أثناء تحويل مستند إلى PDF.

```

 Document doc = new Document();

 doc.getCustomDocumentProperties().add("Company", "My value");

 // Create a "PdfSaveOptions" object that we can pass to the document's "Save" method
 // to modify how that method converts the document to .PDF.
 PdfSaveOptions options = new PdfSaveOptions();

 // Set the "CustomPropertiesExport" property to "PdfCustomPropertiesExport.None" to discard
 // custom document properties as we save the document to .PDF.
 // Set the "CustomPropertiesExport" property to "PdfCustomPropertiesExport.Standard"
 // to preserve custom properties within the output PDF document.
 // Set the "CustomPropertiesExport" property to "PdfCustomPropertiesExport.Metadata"
 // to preserve custom properties in an XMP packet.
 options.setCustomPropertiesExport(pdfCustomPropertiesExportMode);

 doc.save(getArtifactsDir() + "PdfSaveOptions.CustomPropertiesExport.pdf", options);
 
```
## الحقول

| حقل | الوصف |
| --- | --- |
| [METADATA](#METADATA) | الخصائص المخصصة هي بيانات التعريف. |
| [NONE](#NONE) | لم يتم تصدير أي خصائص مخصصة. |
| [STANDARD](#STANDARD) | يتم تصدير الخصائص المخصصة كمدخلات في قاموس /Info. |
| [length](#length) |  |
## الطرق

| طريقة | الوصف |
| --- | --- |
| [fromName(String pdfCustomPropertiesExportName)](#fromName-java.lang.String) |  |
| [getName(int pdfCustomPropertiesExport)](#getName-int) |  |
| [getValues()](#getValues) |  |
| [toString(int pdfCustomPropertiesExport)](#toString-int) |  |
### METADATA {#METADATA}
```
public static int METADATA
```


الخصائص المخصصة هي بيانات التعريف.

 **Remarks:** 

مساحة الاسم للخصائص المصدرة في حزمة XMP هي "custprops". كل خاصية لها عنصر xml مرتبط "custprops:Property1"، "custprops:Property2" وهكذا. هناك عنصر "rdf:Description" داخل عنصر الخاصية. يحتوي عنصر الوصف على عنصرين "custprops:Name"، يحتوي على اسم الخاصية المخصصة كقيمة لهذا العنصر xml، و"custprops:Value"، يحتوي على قيمة الخاصية المخصصة كقيمة لهذا العنصر xml.

### NONE {#NONE}
```
public static int NONE
```


لم يتم تصدير أي خصائص مخصصة.

### STANDARD {#STANDARD}
```
public static int STANDARD
```


يتم تصدير الخصائص المخصصة كمدخلات في قاموس /Info.

الخصائص المخصصة بالأسماء التالية لا يتم تصديرها: "Title"، "Author"، "Subject"، "Keywords"، "Creator"، "Producer"، "CreationDate"، "ModDate"، "Trapped".

### length {#length}
```
public static int length
```


### fromName(String pdfCustomPropertiesExportName) {#fromName-java.lang.String}
```
public static int fromName(String pdfCustomPropertiesExportName)
```




**Parameters:**
| معامل | نوع | الوصف |
| --- | --- | --- |
| pdfCustomPropertiesExportName | java.lang.String |  |

**Returns:**
int
### getName(int pdfCustomPropertiesExport) {#getName-int}
```
public static String getName(int pdfCustomPropertiesExport)
```




**Parameters:**
| معامل | نوع | الوصف |
| --- | --- | --- |
| pdfCustomPropertiesExport | int |  |

**Returns:**
java.lang.String
### getValues() {#getValues}
```
public static int[] getValues()
```




**Returns:**
int[]
### toString(int pdfCustomPropertiesExport) {#toString-int}
```
public static String toString(int pdfCustomPropertiesExport)
```




**Parameters:**
| معامل | نوع | الوصف |
| --- | --- | --- |
| pdfCustomPropertiesExport | int |  |

**Returns:**
java.lang.String
