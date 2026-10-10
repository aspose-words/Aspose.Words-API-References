---
title: "ImageType"
linktitle: "ImageType"
second_title: "Aspose.Words Java için"
description: "Java'da bir Microsoft Word belgesindeki görüntünün tip formatını belirtir."
type: docs
weight: 397
url: /tr/java/com.aspose.words/imagetype/
---

**Inheritance:**
java.lang.Object
```
public class ImageType
```

Microsoft Word belgesindeki bir görüntünün türünü (biçimini) belirtir.

 **Examples:** 

Bir şekle görüntü eklemeyi ve tipini kontrol etmeyi gösterir.

```

 Document doc = new Document();
 DocumentBuilder builder = new DocumentBuilder(doc);

 BufferedImage image = ImageIO.read(getImageUri().toURL().openStream());

 // The image in the URL is a .gif. Inserting it into a document converts it into a .png.
 Shape imgShape = builder.insertImage(image);
 Assert.assertEquals(imgShape.getImageData().getImageType(), ImageType.PNG);
 
```

WebP görüntüsünü okumayı gösterir.

```

 Document doc = new Document(getMyDir() + "Document with WebP image.docx");

 Shape shape = (Shape)doc.getChild(NodeType.SHAPE, 0, true);
 Assert.assertEquals(ImageType.WEB_P, shape.getImageData().getImageType());
 
```
## Alanlar

| Alan | Açıklama |
| --- | --- |
| [BMP](#BMP) | Windows Bitmap. |
| [EMF](#EMF) | Windows Enhanced Metafile. |
| [EPS](#EPS) | Encapsulated PostScript. |
| [GIF](#GIF) | GIF |
| [JPEG](#JPEG) | JPEG JFIF. |
| [NO_IMAGE](#NO-IMAGE) | Görüntü verisi yok. |
| [PICT](#PICT) | Macintosh PICT. |
| [PNG](#PNG) | Portable Network Graphics. |
| [UNKNOWN](#UNKNOWN) | Bilinmeyen bir görüntü tipi veya doğrudan bir Microsoft Word belgesi içinde saklanamayan bir görüntü tipi. |
| [WEB_P](#WEB-P) | WebP. |
| [WMF](#WMF) | Windows Metafile. |
| [length](#length) |  |
## Yöntemler

| Yöntem | Açıklama |
| --- | --- |
| [fromName(String imageTypeName)](#fromName-java.lang.String) |  |
| [getName(int imageType)](#getName-int) |  |
| [getValues()](#getValues) |  |
| [toString(int imageType)](#toString-int) |  |
### BMP {#BMP}
```
public static int BMP
```


Windows Bitmap.

### EMF {#EMF}
```
public static int EMF
```


Windows Enhanced Metafile.

### EPS {#EPS}
```
public static int EPS
```


Encapsulated PostScript.

### GIF {#GIF}
```
public static int GIF
```


GIF

### JPEG {#JPEG}
```
public static int JPEG
```


JPEG JFIF.

### NO_IMAGE {#NO-IMAGE}
```
public static int NO_IMAGE
```


Görüntü verisi yok.

### PICT {#PICT}
```
public static int PICT
```


Macintosh PICT. Mevcut bir görüntü belgede korunur, ancak yeni PICT görüntülerinin belgeye eklenmesi desteklenmez.

### PNG {#PNG}
```
public static int PNG
```


Portable Network Graphics.

### UNKNOWN {#UNKNOWN}
```
public static int UNKNOWN
```


Bilinmeyen bir görüntü tipi veya doğrudan bir Microsoft Word belgesi içinde saklanamayan bir görüntü tipi.

### WEB_P {#WEB-P}
```
public static int WEB_P
```


WebP.

### WMF {#WMF}
```
public static int WMF
```


Windows Metafile.

### length {#length}
```
public static int length
```


### fromName(String imageTypeName) {#fromName-java.lang.String}
```
public static int fromName(String imageTypeName)
```




**Parameters:**
| Parametre | Tür | Açıklama |
| --- | --- | --- |
| imageTypeName | java.lang.String |  |

**Returns:**
int
### getName(int imageType) {#getName-int}
```
public static String getName(int imageType)
```




**Parameters:**
| Parametre | Tür | Açıklama |
| --- | --- | --- |
| imageType | int |  |

**Returns:**
java.lang.String
### getValues() {#getValues}
```
public static int[] getValues()
```




**Returns:**
int[]
### toString(int imageType) {#toString-int}
```
public static String toString(int imageType)
```




**Parameters:**
| Parametre | Tür | Açıklama |
| --- | --- | --- |
| imageType | int |  |

**Returns:**
java.lang.String
