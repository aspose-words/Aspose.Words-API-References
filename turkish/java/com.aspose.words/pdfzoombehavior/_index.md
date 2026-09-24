---
title: "PdfZoomBehavior"
linktitle: "PdfZoomBehavior"
second_title: "Aspose.Words Java için"
description: "Java'da bir PDF görüntüleyicide açıldığında bir PDF belgesine uygulanan yakınlaştırma türünü belirtir."
type: docs
weight: 544
url: /tr/java/com.aspose.words/pdfzoombehavior/
---

**Inheritance:**
java.lang.Object
```
public class PdfZoomBehavior
```

PDF görüntüleyicide açıldığında bir PDF belgesine uygulanan yakınlaştırma türünü belirtir.

 **Examples:** 

Oluşturulmuş bir PDF belgesini açarken okuyucunun uyguladığı varsayılan yakınlaştırmayı ayarlamayı gösterir.

```

 Document doc = new Document();
 DocumentBuilder builder = new DocumentBuilder(doc);
 builder.writeln("Hello world!");

 // Create a "PdfSaveOptions" object that we can pass to the document's "Save" method
 // to modify how that method converts the document to .PDF.
 // Set the "ZoomBehavior" property to "PdfZoomBehavior.ZoomFactor" to get a PDF reader to
 // apply a percentage-based zoom factor when we open the document with it.
 // Set the "ZoomFactor" property to "25" to give the zoom factor a value of 25%.
 PdfSaveOptions options = new PdfSaveOptions();
 {
     options.setZoomBehavior(PdfZoomBehavior.ZOOM_FACTOR);
     options.setZoomFactor(25);
 }

 // When we open this document using a reader such as Adobe Acrobat, we will see the document scaled at 1/4 of its actual size.
 doc.save(getArtifactsDir() + "PdfSaveOptions.ZoomBehaviour.pdf", options);
 
```
## Alanlar

| Alan | Açıklama |
| --- | --- |
| [FIT_BOX](#FIT-BOX) | Sınırlayıcı kutuya (sayfadaki tüm görünür öğeleri içeren dikdörtgen) uyar. |
| [FIT_HEIGHT](#FIT-HEIGHT) | Sayfanın yüksekliğine uyar. |
| [FIT_PAGE](#FIT-PAGE) | Sayfayı tamamen görünür olacak şekilde gösterir. |
| [FIT_WIDTH](#FIT-WIDTH) | Sayfanın genişliğine uyar. |
| [NONE](#NONE) | Belgenin nasıl görüntüleneceği PDF görüntüleyiciye bırakılır. |
| [ZOOM_FACTOR](#ZOOM-FACTOR) | Sayfayı belirtilen yakınlaştırma faktörüyle gösterir. |
| [length](#length) |  |
## Yöntemler

| Yöntem | Açıklama |
| --- | --- |
| [fromName(String pdfZoomBehaviorName)](#fromName-java.lang.String) |  |
| [getName(int pdfZoomBehavior)](#getName-int) |  |
| [getValues()](#getValues) |  |
| [toString(int pdfZoomBehavior)](#toString-int) |  |
### FIT_BOX {#FIT-BOX}
```
public static int FIT_BOX
```


Sınırlayıcı kutuya (sayfadaki tüm görünür öğeleri içeren dikdörtgen) uyar.

### FIT_HEIGHT {#FIT-HEIGHT}
```
public static int FIT_HEIGHT
```


Sayfanın yüksekliğine uyar.

### FIT_PAGE {#FIT-PAGE}
```
public static int FIT_PAGE
```


Sayfayı tamamen görünür olacak şekilde gösterir.

### FIT_WIDTH {#FIT-WIDTH}
```
public static int FIT_WIDTH
```


Sayfanın genişliğine uyar.

### NONE {#NONE}
```
public static int NONE
```


Belgenin nasıl görüntüleneceği PDF görüntüleyiciye bırakılır. Genellikle görüntüleyici belgeyi sayfa genişliğine sığdıracak şekilde gösterir.

### ZOOM_FACTOR {#ZOOM-FACTOR}
```
public static int ZOOM_FACTOR
```


Sayfayı belirtilen yakınlaştırma faktörüyle gösterir.

### length {#length}
```
public static int length
```


### fromName(String pdfZoomBehaviorName) {#fromName-java.lang.String}
```
public static int fromName(String pdfZoomBehaviorName)
```




**Parameters:**
| Parametre | Tür | Açıklama |
| --- | --- | --- |
| pdfZoomBehaviorName | java.lang.String |  |

**Returns:**
int
### getName(int pdfZoomBehavior) {#getName-int}
```
public static String getName(int pdfZoomBehavior)
```




**Parameters:**
| Parametre | Tür | Açıklama |
| --- | --- | --- |
| pdfZoomBehavior | int |  |

**Returns:**
java.lang.String
### getValues() {#getValues}
```
public static int[] getValues()
```




**Returns:**
int[]
### toString(int pdfZoomBehavior) {#toString-int}
```
public static String toString(int pdfZoomBehavior)
```




**Parameters:**
| Parametre | Tür | Açıklama |
| --- | --- | --- |
| pdfZoomBehavior | int |  |

**Returns:**
java.lang.String
