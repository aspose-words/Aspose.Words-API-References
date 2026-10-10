---
title: "ImageType"
linktitle: "ImageType"
second_title: "Aspose.Words für Java"
description: "Gibt das Typformat eines Bildes in einem Microsoft Word-Dokument in Java an."
type: docs
weight: 397
url: /de/java/com.aspose.words/imagetype/
---

**Inheritance:**
java.lang.Object
```
public class ImageType
```

Gibt den Typ (Format) eines Bildes in einem Microsoft Word-Dokument an.

 **Examples:** 

Zeigt, wie man ein Bild zu einer Form hinzufügt und dessen Typ überprüft.

```

 Document doc = new Document();
 DocumentBuilder builder = new DocumentBuilder(doc);

 BufferedImage image = ImageIO.read(getImageUri().toURL().openStream());

 // The image in the URL is a .gif. Inserting it into a document converts it into a .png.
 Shape imgShape = builder.insertImage(image);
 Assert.assertEquals(imgShape.getImageData().getImageType(), ImageType.PNG);
 
```

Zeigt, wie man ein WebP-Bild liest.

```

 Document doc = new Document(getMyDir() + "Document with WebP image.docx");

 Shape shape = (Shape)doc.getChild(NodeType.SHAPE, 0, true);
 Assert.assertEquals(ImageType.WEB_P, shape.getImageData().getImageType());
 
```
## Felder

| Feld | Beschreibung |
| --- | --- |
| [BMP](#BMP) | Windows-Bitmap. |
| [EMF](#EMF) | Windows Enhanced Metafile. |
| [EPS](#EPS) | Encapsulated PostScript. |
| [GIF](#GIF) | GIF |
| [JPEG](#JPEG) | JPEG JFIF. |
| [NO_IMAGE](#NO-IMAGE) | Es gibt keine Bilddaten. |
| [PICT](#PICT) | Macintosh PICT. |
| [PNG](#PNG) | Portable Network Graphics. |
| [UNKNOWN](#UNKNOWN) | Ein unbekannter Bildtyp oder ein Bildtyp, der nicht direkt in einem Microsoft Word-Dokument gespeichert werden kann. |
| [WEB_P](#WEB-P) | WebP. |
| [WMF](#WMF) | Windows Metafile. |
| [length](#length) |  |
## Methoden

| Methode | Beschreibung |
| --- | --- |
| [fromName(String imageTypeName)](#fromName-java.lang.String) |  |
| [getName(int imageType)](#getName-int) |  |
| [getValues()](#getValues) |  |
| [toString(int imageType)](#toString-int) |  |
### BMP {#BMP}
```
public static int BMP
```


Windows-Bitmap.

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


Es gibt keine Bilddaten.

### PICT {#PICT}
```
public static int PICT
```


Macintosh PICT. Ein vorhandenes Bild wird in einem Dokument erhalten bleiben, aber das Einfügen neuer PICT-Bilder in ein Dokument wird nicht unterstützt.

### PNG {#PNG}
```
public static int PNG
```


Portable Network Graphics.

### UNKNOWN {#UNKNOWN}
```
public static int UNKNOWN
```


Ein unbekannter Bildtyp oder ein Bildtyp, der nicht direkt in einem Microsoft Word-Dokument gespeichert werden kann.

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
| Parameter | Typ | Beschreibung |
| --- | --- | --- |
| imageTypeName | java.lang.String |  |

**Returns:**
int
### getName(int imageType) {#getName-int}
```
public static String getName(int imageType)
```




**Parameters:**
| Parameter | Typ | Beschreibung |
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
| Parameter | Typ | Beschreibung |
| --- | --- | --- |
| imageType | int |  |

**Returns:**
java.lang.String
