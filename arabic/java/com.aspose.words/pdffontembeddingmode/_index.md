---
title: "PdfFontEmbeddingMode"
linktitle: "PdfFontEmbeddingMode"
second_title: "Aspose.Words لـ Java"
description: "يحدد كيفية تضمين الخطوط في Java بواسطة Aspose.Words."
type: docs
weight: 535
url: /ar/java/com.aspose.words/pdffontembeddingmode/
---

**Inheritance:**
java.lang.Object
```
public class PdfFontEmbeddingMode
```

يحدد كيفية تضمين الخطوط بواسطة Aspose.Words.

 **Examples:** 

يعرض كيفية ضبط Aspose.Words لتخطي تضمين خطوط Arial و Times New Roman في مستند PDF.

```

 Document doc = new Document();
 DocumentBuilder builder = new DocumentBuilder(doc);

 // "Arial" is a standard font, and "Courier New" is a nonstandard font.
 builder.getFont().setName("Arial");
 builder.writeln("Hello world!");
 builder.getFont().setName("Courier New");
 builder.writeln("The quick brown fox jumps over the lazy dog.");

 // Create a "PdfSaveOptions" object that we can pass to the document's "Save" method
 // to modify how that method converts the document to .PDF.
 PdfSaveOptions options = new PdfSaveOptions();

 // Set the "EmbedFullFonts" property to "true" to embed every glyph of every embedded font in the output PDF.
 options.setEmbedFullFonts(true);

 // Set the "FontEmbeddingMode" property to "EmbedAll" to embed all fonts in the output PDF.
 // Set the "FontEmbeddingMode" property to "EmbedNonstandard" to only allow nonstandard fonts' embedding in the output PDF.
 // Set the "FontEmbeddingMode" property to "EmbedNone" to not embed any fonts in the output PDF.
 options.setFontEmbeddingMode(pdfFontEmbeddingMode);

 doc.save(getArtifactsDir() + "PdfSaveOptions.EmbedWindowsFonts.pdf", options);

 switch (pdfFontEmbeddingMode) {
     case PdfFontEmbeddingMode.EMBED_ALL:
         Assert.assertTrue(new File(getArtifactsDir() + "PdfSaveOptions.EmbedWindowsFonts.pdf").length() < 1047200);
         break;
     case PdfFontEmbeddingMode.EMBED_NONSTANDARD:
         Assert.assertTrue(new File(getArtifactsDir() + "PdfSaveOptions.EmbedWindowsFonts.pdf").length() < 491800);
         break;
     case PdfFontEmbeddingMode.EMBED_NONE:
         Assert.assertTrue(new File(getArtifactsDir() + "PdfSaveOptions.EmbedWindowsFonts.pdf").length() <= 4258);
         break;
 }
 
```
## الحقول

| حقل | الوصف |
| --- | --- |
| [EMBED_ALL](#EMBED-ALL) | يقوم Aspose.Words بتضمين جميع الخطوط. |
| [EMBED_NONE](#EMBED-NONE) | لا يقوم Aspose.Words بتضمين أي خطوط. |
| [EMBED_NONSTANDARD](#EMBED-NONSTANDARD) | يقوم Aspose.Words بتضمين جميع الخطوط باستثناء خطوط Windows القياسية Arial و Times New Roman. |
| [length](#length) |  |
## الطرق

| طريقة | الوصف |
| --- | --- |
| [fromName(String pdfFontEmbeddingModeName)](#fromName-java.lang.String) |  |
| [getName(int pdfFontEmbeddingMode)](#getName-int) |  |
| [getValues()](#getValues) |  |
| [toString(int pdfFontEmbeddingMode)](#toString-int) |  |
### EMBED_ALL {#EMBED-ALL}
```
public static int EMBED_ALL
```


يقوم Aspose.Words بتضمين جميع الخطوط.

### EMBED_NONE {#EMBED-NONE}
```
public static int EMBED_NONE
```


لا يقوم Aspose.Words بتضمين أي خطوط.

### EMBED_NONSTANDARD {#EMBED-NONSTANDARD}
```
public static int EMBED_NONSTANDARD
```


يقوم Aspose.Words بتضمين جميع الخطوط باستثناء خطوط Windows القياسية Arial و Times New Roman. في هذا الوضع، تتأثر فقط خطوط Arial و Times New Roman لأن MS Word لا يقوم بتضمين هذه الخطوط فقط عند حفظ المستند كملف PDF.

### length {#length}
```
public static int length
```


### fromName(String pdfFontEmbeddingModeName) {#fromName-java.lang.String}
```
public static int fromName(String pdfFontEmbeddingModeName)
```




**Parameters:**
| معامل | نوع | الوصف |
| --- | --- | --- |
| pdfFontEmbeddingModeName | java.lang.String |  |

**Returns:**
int
### getName(int pdfFontEmbeddingMode) {#getName-int}
```
public static String getName(int pdfFontEmbeddingMode)
```




**Parameters:**
| معامل | نوع | الوصف |
| --- | --- | --- |
| pdfFontEmbeddingMode | int |  |

**Returns:**
java.lang.String
### getValues() {#getValues}
```
public static int[] getValues()
```




**Returns:**
int[]
### toString(int pdfFontEmbeddingMode) {#toString-int}
```
public static String toString(int pdfFontEmbeddingMode)
```




**Parameters:**
| معامل | نوع | الوصف |
| --- | --- | --- |
| pdfFontEmbeddingMode | int |  |

**Returns:**
java.lang.String
