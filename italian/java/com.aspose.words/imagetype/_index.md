---
title: "ImageType"
linktitle: "ImageType"
second_title: "Aspose.Words per Java"
description: "Specifica il formato di tipo di un'immagine in un documento Microsoft Word in Java."
type: docs
weight: 397
url: /it/java/com.aspose.words/imagetype/
---

**Inheritance:**
java.lang.Object
```
public class ImageType
```

Specifica il tipo (formato) di un'immagine in un documento Microsoft Word.

 **Examples:** 

Mostra come aggiungere un'immagine a una forma e controllarne il tipo.

```

 Document doc = new Document();
 DocumentBuilder builder = new DocumentBuilder(doc);

 BufferedImage image = ImageIO.read(getImageUri().toURL().openStream());

 // The image in the URL is a .gif. Inserting it into a document converts it into a .png.
 Shape imgShape = builder.insertImage(image);
 Assert.assertEquals(imgShape.getImageData().getImageType(), ImageType.PNG);
 
```

Mostra come leggere un'immagine WebP.

```

 Document doc = new Document(getMyDir() + "Document with WebP image.docx");

 Shape shape = (Shape)doc.getChild(NodeType.SHAPE, 0, true);
 Assert.assertEquals(ImageType.WEB_P, shape.getImageData().getImageType());
 
```
## Campi

| Campo | Descrizione |
| --- | --- |
| [BMP](#BMP) | Bitmap Windows. |
| [EMF](#EMF) | Metafile Windows Enhanced. |
| [EPS](#EPS) | PostScript Incapsulato. |
| [GIF](#GIF) | GIF |
| [JPEG](#JPEG) | JPEG JFIF. |
| [NO_IMAGE](#NO-IMAGE) | Non ci sono dati dell'immagine. |
| [PICT](#PICT) | Macintosh PICT. |
| [PNG](#PNG) | Portable Network Graphics. |
| [UNKNOWN](#UNKNOWN) | Un tipo di immagine sconosciuto o un tipo di immagine che non può essere memorizzato direttamente all'interno di un documento Microsoft Word. |
| [WEB_P](#WEB-P) | WebP. |
| [WMF](#WMF) | Metafile Windows. |
| [length](#length) |  |
## Metodi

| Metodo | Descrizione |
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


Metafile Windows Enhanced.

### EPS {#EPS}
```
public static int EPS
```


PostScript Incapsulato.

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


Non ci sono dati dell'immagine.

### PICT {#PICT}
```
public static int PICT
```


Macintosh PICT. Un'immagine esistente verrà conservata in un documento, ma l'inserimento di nuove immagini PICT in un documento non è supportato.

### PNG {#PNG}
```
public static int PNG
```


Portable Network Graphics.

### UNKNOWN {#UNKNOWN}
```
public static int UNKNOWN
```


Un tipo di immagine sconosciuto o un tipo di immagine che non può essere memorizzato direttamente all'interno di un documento Microsoft Word.

### WEB_P {#WEB-P}
```
public static int WEB_P
```


WebP.

### WMF {#WMF}
```
public static int WMF
```


Metafile Windows.

### length {#length}
```
public static int length
```


### fromName(String imageTypeName) {#fromName-java.lang.String}
```
public static int fromName(String imageTypeName)
```




**Parameters:**
| Parametro | Tipo | Descrizione |
| --- | --- | --- |
| imageTypeName | java.lang.String |  |

**Returns:**
int
### getName(int imageType) {#getName-int}
```
public static String getName(int imageType)
```




**Parameters:**
| Parametro | Tipo | Descrizione |
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
| Parametro | Tipo | Descrizione |
| --- | --- | --- |
| imageType | int |  |

**Returns:**
java.lang.String
