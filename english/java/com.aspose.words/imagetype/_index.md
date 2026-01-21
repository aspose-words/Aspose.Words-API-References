---
title: ImageType
linktitle: ImageType
second_title: Aspose.Words for Java
description: Specifies the type format of an image in a Microsoft Word document in Java.
type: docs
weight: 397
url: /java/com.aspose.words/imagetype/
---

**Inheritance:**
java.lang.Object
```
public class ImageType
```

Specifies the type (format) of an image in a Microsoft Word document.

 **Examples:** 

Shows how to read WebP image.

```

 Document doc = new Document(getMyDir() + "Document with WebP image.docx");

 Shape shape = (Shape)doc.getChild(NodeType.SHAPE, 0, true);
 Assert.assertEquals(ImageType.WEB_P, shape.getImageData().getImageType());
 
```

Shows how to add an image to a shape and check its type.

```

 Document doc = new Document();
 DocumentBuilder builder = new DocumentBuilder(doc);

 BufferedImage image = ImageIO.read(getAsposelogoUri().toURL().openStream());

 // The image in the URL is a .gif. Inserting it into a document converts it into a .png.
 Shape imgShape = builder.insertImage(image);
 Assert.assertEquals(imgShape.getImageData().getImageType(), ImageType.PNG);
 
```
## Fields

| Field | Description |
| --- | --- |
| [BMP](#BMP) | Windows Bitmap. |
| [EMF](#EMF) | Windows Enhanced Metafile. |
| [EPS](#EPS) | Encapsulated PostScript. |
| [GIF](#GIF) | GIF |
| [JPEG](#JPEG) | JPEG JFIF. |
| [NO_IMAGE](#NO-IMAGE) | The is no image data. |
| [PICT](#PICT) | Macintosh PICT. |
| [PNG](#PNG) | Portable Network Graphics. |
| [UNKNOWN](#UNKNOWN) | An unknown image type or image type that cannot be directly stored inside a Microsoft Word document. |
| [WEB_P](#WEB-P) | WebP. |
| [WMF](#WMF) | Windows Metafile. |
| [length](#length) |  |
## Methods

| Method | Description |
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


The is no image data.

### PICT {#PICT}
```
public static int PICT
```


Macintosh PICT. An existing image will be preserved in a document, but inserting new PICT images into a document is not supported.

### PNG {#PNG}
```
public static int PNG
```


Portable Network Graphics.

### UNKNOWN {#UNKNOWN}
```
public static int UNKNOWN
```


An unknown image type or image type that cannot be directly stored inside a Microsoft Word document.

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
| Parameter | Type | Description |
| --- | --- | --- |
| imageTypeName | java.lang.String |  |

**Returns:**
int
### getName(int imageType) {#getName-int}
```
public static String getName(int imageType)
```




**Parameters:**
| Parameter | Type | Description |
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
| Parameter | Type | Description |
| --- | --- | --- |
| imageType | int |  |

**Returns:**
java.lang.String
