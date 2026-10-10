---
title: "PdfImageColorSpaceExportMode"
linktitle: "PdfImageColorSpaceExportMode"
second_title: "Aspose.Words Java için"
description: "Java'da PDF belgesindeki görüntüler için renk uzayının nasıl seçileceğini belirtir."
type: docs
weight: 536
url: /tr/java/com.aspose.words/pdfimagecolorspaceexportmode/
---

**Inheritance:**
java.lang.Object
```
public class PdfImageColorSpaceExportMode
```

PDF belgesindeki görüntüler için renk uzayının nasıl seçileceğini belirtir.

 **Examples:** 

Bir belgeyi PDF olarak dışa aktarırken görüntüler için farklı bir renk uzayı ayarlamanın nasıl yapılacağını gösterir.

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

 // Set the "ImageColorSpaceExportMode" property to "PdfImageColorSpaceExportMode.Auto" to get Aspose.Words to
 // automatically select the color space for images in the document that it converts to PDF.
 // In most cases, the color space will be RGB.
 // Set the "ImageColorSpaceExportMode" property to "PdfImageColorSpaceExportMode.SimpleCmyk"
 // to use the CMYK color space for all images in the saved PDF.
 // Aspose.Words will also apply Flate compression to all images and ignore the "ImageCompression" property's value.
 pdfSaveOptions.setImageColorSpaceExportMode(pdfImageColorSpaceExportMode);

 doc.save(getArtifactsDir() + "PdfSaveOptions.ImageColorSpaceExportMode.pdf", pdfSaveOptions);
 
```
## Alanlar

| Alan | Açıklama |
| --- | --- |
| [AUTO](#AUTO) | Aspose.Words, her görüntü için en uygun renk uzayını otomatik olarak seçer. |
| [SIMPLE_CMYK](#SIMPLE-CMYK) | Aspose.Words, RGB görüntüleri basit bir formül kullanarak CMYK renk uzayına dönüştürür. |
| [length](#length) |  |
## Yöntemler

| Yöntem | Açıklama |
| --- | --- |
| [fromName(String pdfImageColorSpaceExportModeName)](#fromName-java.lang.String) |  |
| [getName(int pdfImageColorSpaceExportMode)](#getName-int) |  |
| [getValues()](#getValues) |  |
| [toString(int pdfImageColorSpaceExportMode)](#toString-int) |  |
### AUTO {#AUTO}
```
public static int AUTO
```


Aspose.Words, her görüntü için en uygun renk uzayını otomatik olarak seçer.

 **Remarks:** 

Görüntülerin çoğu RGB renk uzayında kaydedilir. Ayrıca Indexed ve Grayscale renk uzayları da kullanılabilir. CMYK renk uzayı hiç kullanılmaz.

Bazı görüntülerde renk uzayı farklı platformlarda değişiklik gösterebilir.

### SIMPLE_CMYK {#SIMPLE-CMYK}
```
public static int SIMPLE_CMYK
```


Aspose.Words, RGB görüntüleri basit bir formül kullanarak CMYK renk uzayına dönüştürür.

 **Remarks:** 

RGB renk uzayındaki görüntüler, aşağıdaki formül kullanılarak CMYK'ye dönüştürülür: Black = minimum(1-Red,1-Green,1-Blue). Cyan = (1-Red-Black)/(1-Black). Magenta = (1-Green-Black)/(1-Black). Yellow = (1-Blue-Black)/(1-Black). RGB değerleri normalleştirilir - değerler 0 ile 1.0 arasındadır.

### length {#length}
```
public static int length
```


### fromName(String pdfImageColorSpaceExportModeName) {#fromName-java.lang.String}
```
public static int fromName(String pdfImageColorSpaceExportModeName)
```




**Parameters:**
| Parametre | Tür | Açıklama |
| --- | --- | --- |
| pdfImageColorSpaceExportModeName | java.lang.String |  |

**Returns:**
int
### getName(int pdfImageColorSpaceExportMode) {#getName-int}
```
public static String getName(int pdfImageColorSpaceExportMode)
```




**Parameters:**
| Parametre | Tür | Açıklama |
| --- | --- | --- |
| pdfImageColorSpaceExportMode | int |  |

**Returns:**
java.lang.String
### getValues() {#getValues}
```
public static int[] getValues()
```




**Returns:**
int[]
### toString(int pdfImageColorSpaceExportMode) {#toString-int}
```
public static String toString(int pdfImageColorSpaceExportMode)
```




**Parameters:**
| Parametre | Tür | Açıklama |
| --- | --- | --- |
| pdfImageColorSpaceExportMode | int |  |

**Returns:**
java.lang.String
