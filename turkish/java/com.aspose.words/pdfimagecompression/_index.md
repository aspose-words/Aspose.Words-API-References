---
title: "PdfImageCompression"
linktitle: "PdfImageCompression"
second_title: "Aspose.Words Java için"
description: "Java'da PDF dosyasındaki görüntülere uygulanan sıkıştırma türünü belirtir."
type: docs
weight: 537
url: /tr/java/com.aspose.words/pdfimagecompression/
---

**Inheritance:**
java.lang.Object
```
public class PdfImageCompression
```

PDF dosyasındaki görüntülere uygulanan sıkıştırma türünü belirtir.

 **Examples:** 

PDF'ye dönüştürdüğümüz bir belgede tüm görüntüler için sıkıştırma türünün nasıl belirtileceğini gösterir.

```

 Document doc = new Document();
 DocumentBuilder builder = new DocumentBuilder(doc);

 builder.writeln("Jpeg image:");
 builder.insertImage(getImageDir() + "Logo.jpg");
 builder.insertParagraph();
 builder.writeln("Png image:");
 builder.insertImage(getImageDir() + "Transparent background logo.png");

 // Create a "PdfSaveOptions" object that we can pass to the document's "Save" method
 // to modify how that method converts the document to .PDF.
 PdfSaveOptions pdfSaveOptions = new PdfSaveOptions();

 // Set the "ImageCompression" property to "PdfImageCompression.Auto" to use the
 // "ImageCompression" property to control the quality of the Jpeg images that end up in the output PDF.
 // Set the "ImageCompression" property to "PdfImageCompression.Jpeg" to use the
 // "ImageCompression" property to control the quality of all images that end up in the output PDF.
 pdfSaveOptions.setImageCompression(pdfImageCompression);

 // Set the "JpegQuality" property to "10" to strengthen compression at the cost of image quality.
 pdfSaveOptions.setJpegQuality(10);

 doc.save(getArtifactsDir() + "PdfSaveOptions.ImageCompression.pdf", pdfSaveOptions);
 
```
## Alanlar

| Alan | Açıklama |
| --- | --- |
| [AUTO](#AUTO) | Her görüntü için en uygun sıkıştırmayı otomatik olarak seçer. |
| [JPEG](#JPEG) | Jpeg sıkıştırması. |
| [length](#length) |  |
## Yöntemler

| Yöntem | Açıklama |
| --- | --- |
| [fromName(String pdfImageCompressionName)](#fromName-java.lang.String) |  |
| [getName(int pdfImageCompression)](#getName-int) |  |
| [getValues()](#getValues) |  |
| [toString(int pdfImageCompression)](#toString-int) |  |
### AUTO {#AUTO}
```
public static int AUTO
```


Her görüntü için en uygun sıkıştırmayı otomatik olarak seçer.

### JPEG {#JPEG}
```
public static int JPEG
```


Jpeg sıkıştırması. Şeffaflığı desteklemez.

### length {#length}
```
public static int length
```


### fromName(String pdfImageCompressionName) {#fromName-java.lang.String}
```
public static int fromName(String pdfImageCompressionName)
```




**Parameters:**
| Parametre | Tür | Açıklama |
| --- | --- | --- |
| pdfImageCompressionName | java.lang.String |  |

**Returns:**
int
### getName(int pdfImageCompression) {#getName-int}
```
public static String getName(int pdfImageCompression)
```




**Parameters:**
| Parametre | Tür | Açıklama |
| --- | --- | --- |
| pdfImageCompression | int |  |

**Returns:**
java.lang.String
### getValues() {#getValues}
```
public static int[] getValues()
```




**Returns:**
int[]
### toString(int pdfImageCompression) {#toString-int}
```
public static String toString(int pdfImageCompression)
```




**Parameters:**
| Parametre | Tür | Açıklama |
| --- | --- | --- |
| pdfImageCompression | int |  |

**Returns:**
java.lang.String
