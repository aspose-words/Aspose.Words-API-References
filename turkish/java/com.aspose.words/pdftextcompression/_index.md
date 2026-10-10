---
title: "PdfTextCompression"
linktitle: "PdfTextCompression"
second_title: "Aspose.Words Java için"
description: "Java'da PDF dosyasındaki görüntüler dışındaki tüm içeriğe uygulanan bir sıkıştırma türünü belirtir."
type: docs
weight: 543
url: /tr/java/com.aspose.words/pdftextcompression/
---

**Inheritance:**
java.lang.Object
```
public class PdfTextCompression
```

PDF dosyasındaki görüntüler dışındaki tüm içeriğe uygulanan sıkıştırma türünü belirtir.

 **Examples:** 

Bir belgeyi PDF olarak kaydederken metin sıkıştırmasının nasıl uygulanacağını gösterir.

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
## Alanlar

| Alan | Açıklama |
| --- | --- |
| [FLATE](#FLATE) | Flate (ZIP) sıkıştırması. |
| [NONE](#NONE) | Sıkıştırma yok. |
| [length](#length) |  |
## Yöntemler

| Yöntem | Açıklama |
| --- | --- |
| [fromName(String pdfTextCompressionName)](#fromName-java.lang.String) |  |
| [getName(int pdfTextCompression)](#getName-int) |  |
| [getValues()](#getValues) |  |
| [toString(int pdfTextCompression)](#toString-int) |  |
### FLATE {#FLATE}
```
public static int FLATE
```


Flate (ZIP) sıkıştırması.

### NONE {#NONE}
```
public static int NONE
```


Sıkıştırma yok.

### length {#length}
```
public static int length
```


### fromName(String pdfTextCompressionName) {#fromName-java.lang.String}
```
public static int fromName(String pdfTextCompressionName)
```




**Parameters:**
| Parametre | Tür | Açıklama |
| --- | --- | --- |
| pdfTextCompressionName | java.lang.String |  |

**Returns:**
int
### getName(int pdfTextCompression) {#getName-int}
```
public static String getName(int pdfTextCompression)
```




**Parameters:**
| Parametre | Tür | Açıklama |
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
| Parametre | Tür | Açıklama |
| --- | --- | --- |
| pdfTextCompression | int |  |

**Returns:**
java.lang.String
