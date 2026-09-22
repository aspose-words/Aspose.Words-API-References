---
title: "PdfTextCompression"
linktitle: "PdfTextCompression"
second_title: "Aspose.Words لـ Java"
description: "يحدد نوع الضغط المطبق على جميع محتويات ملف PDF باستثناء الصور في Java."
type: docs
weight: 543
url: /ar/java/com.aspose.words/pdftextcompression/
---

**Inheritance:**
java.lang.Object
```
public class PdfTextCompression
```

يحدد نوع الضغط المطبق على جميع المحتويات في ملف PDF باستثناء الصور.

 **Examples:** 

يوضح كيفية تطبيق ضغط النص عند حفظ المستند إلى PDF.

```

 Document doc = new Document();
 DocumentBuilder builder = new DocumentBuilder(doc);

 for (int i = 0; i < 100; i++)
     builder.writeln("Lorem ipsum dolor sit amet, consectetur adipiscing elit, " +
             "sed do eiusmod tempor incididunt ut labore et dolore magna aliqua.");

 // Create a "PdfSaveOptions" object that we can pass to the document's "Save" method
 // to modify how that method converts the document to .PDF.
 PdfSaveOptions options = new PdfSaveOptions();

 // Set the "TextCompression" property to "PdfTextCompression.None" to not apply any
 // compression to text when we save the document to PDF.
 // Set the "TextCompression" property to "PdfTextCompression.Flate" to apply ZIP compression
 // to text when we save the document to PDF. The larger the document, the bigger the impact that this will have.
 options.setTextCompression(pdfTextCompression);

 doc.save(getArtifactsDir() + "PdfSaveOptions.TextCompression.pdf", options);
 
```
## الحقول

| حقل | الوصف |
| --- | --- |
| [FLATE](#FLATE) | ضغط Flate (ZIP). |
| [NONE](#NONE) | بدون ضغط. |
| [length](#length) |  |
## الطرق

| طريقة | الوصف |
| --- | --- |
| [fromName(String pdfTextCompressionName)](#fromName-java.lang.String) |  |
| [getName(int pdfTextCompression)](#getName-int) |  |
| [getValues()](#getValues) |  |
| [toString(int pdfTextCompression)](#toString-int) |  |
### FLATE {#FLATE}
```
public static int FLATE
```


ضغط Flate (ZIP).

### NONE {#NONE}
```
public static int NONE
```


بدون ضغط.

### length {#length}
```
public static int length
```


### fromName(String pdfTextCompressionName) {#fromName-java.lang.String}
```
public static int fromName(String pdfTextCompressionName)
```




**Parameters:**
| معامل | نوع | الوصف |
| --- | --- | --- |
| pdfTextCompressionName | java.lang.String |  |

**Returns:**
int
### getName(int pdfTextCompression) {#getName-int}
```
public static String getName(int pdfTextCompression)
```




**Parameters:**
| معامل | نوع | الوصف |
| --- | --- | --- |
| pdfTextCompression | int |  |

**Returns:**
java.lang.String
### getValues() {#getValues}
```
public static int[] getValues()
```




**Returns:**
int[]
### toString(int pdfTextCompression) {#toString-int}
```
public static String toString(int pdfTextCompression)
```




**Parameters:**
| معامل | نوع | الوصف |
| --- | --- | --- |
| pdfTextCompression | int |  |

**Returns:**
java.lang.String
