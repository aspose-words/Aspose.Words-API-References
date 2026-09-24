---
title: "ImageType"
linktitle: "ImageType"
second_title: "Aspose.Words para Java"
description: "Especifica el formato de tipo de una imagen en un documento de Microsoft Word en Java."
type: docs
weight: 397
url: /es/java/com.aspose.words/imagetype/
---

**Inheritance:**
java.lang.Object
```
public class ImageType
```

Especifica el tipo (formato) de una imagen en un documento de Microsoft Word.

 **Examples:** 

Muestra cómo agregar una imagen a una forma y verificar su tipo.

```

 Document doc = new Document();
 DocumentBuilder builder = new DocumentBuilder(doc);

 BufferedImage image = ImageIO.read(getImageUri().toURL().openStream());

 // The image in the URL is a .gif. Inserting it into a document converts it into a .png.
 Shape imgShape = builder.insertImage(image);
 Assert.assertEquals(imgShape.getImageData().getImageType(), ImageType.PNG);
 
```

Muestra cómo leer una imagen WebP.

```

 Document doc = new Document(getMyDir() + "Document with WebP image.docx");

 Shape shape = (Shape)doc.getChild(NodeType.SHAPE, 0, true);
 Assert.assertEquals(ImageType.WEB_P, shape.getImageData().getImageType());
 
```
## Campos

| Campo | Descripción |
| --- | --- |
| [BMP](#BMP) | Bitmap de Windows. |
| [EMF](#EMF) | Metarchivo mejorado de Windows. |
| [EPS](#EPS) | PostScript encapsulado. |
| [GIF](#GIF) | GIF |
| [JPEG](#JPEG) | JPEG JFIF. |
| [NO_IMAGE](#NO-IMAGE) | No hay datos de imagen. |
| [PICT](#PICT) | Macintosh PICT. |
| [PNG](#PNG) | Portable Network Graphics. |
| [UNKNOWN](#UNKNOWN) | Un tipo de imagen desconocido o un tipo de imagen que no puede almacenarse directamente dentro de un documento de Microsoft Word. |
| [WEB_P](#WEB-P) | WebP. |
| [WMF](#WMF) | Metarchivo de Windows. |
| [length](#length) |  |
## Métodos

| Método | Descripción |
| --- | --- |
| [fromName(String imageTypeName)](#fromName-java.lang.String) |  |
| [getName(int imageType)](#getName-int) |  |
| [getValues()](#getValues) |  |
| [toString(int imageType)](#toString-int) |  |
### BMP {#BMP}
```
public static int BMP
```


Bitmap de Windows.

### EMF {#EMF}
```
public static int EMF
```


Metarchivo mejorado de Windows.

### EPS {#EPS}
```
public static int EPS
```


PostScript encapsulado.

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


No hay datos de imagen.

### PICT {#PICT}
```
public static int PICT
```


Macintosh PICT. Una imagen existente se conservará en un documento, pero la inserción de nuevas imágenes PICT en un documento no es compatible.

### PNG {#PNG}
```
public static int PNG
```


Portable Network Graphics.

### UNKNOWN {#UNKNOWN}
```
public static int UNKNOWN
```


Un tipo de imagen desconocido o un tipo de imagen que no puede almacenarse directamente dentro de un documento de Microsoft Word.

### WEB_P {#WEB-P}
```
public static int WEB_P
```


WebP.

### WMF {#WMF}
```
public static int WMF
```


Metarchivo de Windows.

### length {#length}
```
public static int length
```


### fromName(String imageTypeName) {#fromName-java.lang.String}
```
public static int fromName(String imageTypeName)
```




**Parameters:**
| Parámetro | Tipo | Descripción |
| --- | --- | --- |
| imageTypeName | java.lang.String |  |

**Returns:**
int
### getName(int imageType) {#getName-int}
```
public static String getName(int imageType)
```




**Parameters:**
| Parámetro | Tipo | Descripción |
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
| Parámetro | Tipo | Descripción |
| --- | --- | --- |
| imageType | int |  |

**Returns:**
java.lang.String
