---
title: "ImageType"
linktitle: "ImageType"
second_title: "Aspose.Words pour Java"
description: "Spécifie le format de type d'une image dans un document Microsoft Word en Java."
type: docs
weight: 397
url: /fr/java/com.aspose.words/imagetype/
---

**Inheritance:**
java.lang.Object
```
public class ImageType
```

Spécifie le type (format) d'une image dans un document Microsoft Word.

 **Examples:** 

Montre comment ajouter une image à une forme et vérifier son type.

```

 Document doc = new Document();
 DocumentBuilder builder = new DocumentBuilder(doc);

 BufferedImage image = ImageIO.read(getImageUri().toURL().openStream());

 // The image in the URL is a .gif. Inserting it into a document converts it into a .png.
 Shape imgShape = builder.insertImage(image);
 Assert.assertEquals(imgShape.getImageData().getImageType(), ImageType.PNG);
 
```

Montre comment lire une image WebP.

```

 Document doc = new Document(getMyDir() + "Document with WebP image.docx");

 Shape shape = (Shape)doc.getChild(NodeType.SHAPE, 0, true);
 Assert.assertEquals(ImageType.WEB_P, shape.getImageData().getImageType());
 
```
## Champs

| Champ | Description |
| --- | --- |
| [BMP](#BMP) | Bitmap Windows. |
| [EMF](#EMF) | Métafile amélioré Windows. |
| [EPS](#EPS) | PostScript encapsulé. |
| [GIF](#GIF) | GIF |
| [JPEG](#JPEG) | JPEG JFIF. |
| [NO_IMAGE](#NO-IMAGE) | Il n'y a aucune donnée d'image. |
| [PICT](#PICT) | PICT Macintosh. |
| [PNG](#PNG) | Graphiques réseau portables. |
| [UNKNOWN](#UNKNOWN) | Un type d'image inconnu ou un type d'image qui ne peut pas être stocké directement dans un document Microsoft Word. |
| [WEB_P](#WEB-P) | WebP. |
| [WMF](#WMF) | Métafile Windows. |
| [length](#length) |  |
## Méthodes

| Méthode | Description |
| --- | --- |
| [fromName(String imageTypeName)](#fromName-java.lang.String) |  |
| [getName(int imageType)](#getName-int) |  |
| [getValues()](#getValues) |  |
| [toString(int imageType)](#toString-int) |  |
### BMP {#BMP}
```
public static int BMP
```


Bitmap Windows.

### EMF {#EMF}
```
public static int EMF
```


Métafile amélioré Windows.

### EPS {#EPS}
```
public static int EPS
```


PostScript encapsulé.

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


Il n'y a aucune donnée d'image.

### PICT {#PICT}
```
public static int PICT
```


PICT Macintosh. Une image existante sera conservée dans un document, mais l'insertion de nouvelles images PICT dans un document n'est pas prise en charge.

### PNG {#PNG}
```
public static int PNG
```


Graphiques réseau portables.

### UNKNOWN {#UNKNOWN}
```
public static int UNKNOWN
```


Un type d'image inconnu ou un type d'image qui ne peut pas être stocké directement dans un document Microsoft Word.

### WEB_P {#WEB-P}
```
public static int WEB_P
```


WebP.

### WMF {#WMF}
```
public static int WMF
```


Métafile Windows.

### length {#length}
```
public static int length
```


### fromName(String imageTypeName) {#fromName-java.lang.String}
```
public static int fromName(String imageTypeName)
```




**Parameters:**
| Paramètre | Type | Description |
| --- | --- | --- |
| imageTypeName | java.lang.String |  |

**Returns:**
int
### getName(int imageType) {#getName-int}
```
public static String getName(int imageType)
```




**Parameters:**
| Paramètre | Type | Description |
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
| Paramètre | Type | Description |
| --- | --- | --- |
| imageType | int |  |

**Returns:**
java.lang.String
