---
title: "ImageType"
linktitle: "ImageType"
second_title: "Aspose.Words لـ Java"
description: "يحدد تنسيق نوع الصورة في مستند Microsoft Word باستخدام Java."
type: docs
weight: 397
url: /ar/java/com.aspose.words/imagetype/
---

**Inheritance:**
java.lang.Object
```
public class ImageType
```

يحدد نوع (تنسيق) الصورة في مستند Microsoft Word.

 **Examples:** 

يوضح كيفية إضافة صورة إلى شكل والتحقق من نوعها.

```

 Document doc = new Document();
 DocumentBuilder builder = new DocumentBuilder(doc);

 BufferedImage image = ImageIO.read(getImageUri().toURL().openStream());

 // The image in the URL is a .gif. Inserting it into a document converts it into a .png.
 Shape imgShape = builder.insertImage(image);
 Assert.assertEquals(imgShape.getImageData().getImageType(), ImageType.PNG);
 
```

يوضح كيفية قراءة صورة WebP.

```

 Document doc = new Document(getMyDir() + "Document with WebP image.docx");

 Shape shape = (Shape)doc.getChild(NodeType.SHAPE, 0, true);
 Assert.assertEquals(ImageType.WEB_P, shape.getImageData().getImageType());
 
```
## الحقول

| حقل | الوصف |
| --- | --- |
| [BMP](#BMP) | Windows Bitmap. |
| [EMF](#EMF) | Windows Enhanced Metafile. |
| [EPS](#EPS) | Encapsulated PostScript. |
| [GIF](#GIF) | GIF |
| [JPEG](#JPEG) | JPEG JFIF. |
| [NO_IMAGE](#NO-IMAGE) | لا توجد بيانات صورة. |
| [PICT](#PICT) | Macintosh PICT. |
| [PNG](#PNG) | Portable Network Graphics. |
| [UNKNOWN](#UNKNOWN) | نوع صورة غير معروف أو نوع صورة لا يمكن تخزينه مباشرة داخل مستند Microsoft Word. |
| [WEB_P](#WEB-P) | WebP. |
| [WMF](#WMF) | Windows Metafile. |
| [length](#length) |  |
## الطرق

| طريقة | الوصف |
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


لا توجد بيانات صورة.

### PICT {#PICT}
```
public static int PICT
```


Macintosh PICT. سيتم الحفاظ على الصورة الموجودة في المستند، لكن إدراج صور PICT جديدة في المستند غير مدعوم.

### PNG {#PNG}
```
public static int PNG
```


Portable Network Graphics.

### UNKNOWN {#UNKNOWN}
```
public static int UNKNOWN
```


نوع صورة غير معروف أو نوع صورة لا يمكن تخزينه مباشرة داخل مستند Microsoft Word.

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
| معامل | نوع | الوصف |
| --- | --- | --- |
| imageTypeName | java.lang.String |  |

**Returns:**
int
### getName(int imageType) {#getName-int}
```
public static String getName(int imageType)
```




**Parameters:**
| معامل | نوع | الوصف |
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
| معامل | نوع | الوصف |
| --- | --- | --- |
| imageType | int |  |

**Returns:**
java.lang.String
