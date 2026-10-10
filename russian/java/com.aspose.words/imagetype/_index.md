---
title: "ImageType"
linktitle: "ImageType"
second_title: "Aspose.Words для Java"
description: "Указывает формат типа изображения в документе Microsoft Word на Java."
type: docs
weight: 397
url: /ru/java/com.aspose.words/imagetype/
---

**Inheritance:**
java.lang.Object
```
public class ImageType
```

Указывает тип (формат) изображения в документе Microsoft Word.

 **Examples:** 

Показывает, как добавить изображение в форму и проверить его тип.

```

 Document doc = new Document();
 DocumentBuilder builder = new DocumentBuilder(doc);

 BufferedImage image = ImageIO.read(getImageUri().toURL().openStream());

 // The image in the URL is a .gif. Inserting it into a document converts it into a .png.
 Shape imgShape = builder.insertImage(image);
 Assert.assertEquals(imgShape.getImageData().getImageType(), ImageType.PNG);
 
```

Показывает, как прочитать изображение WebP.

```

 Document doc = new Document(getMyDir() + "Document with WebP image.docx");

 Shape shape = (Shape)doc.getChild(NodeType.SHAPE, 0, true);
 Assert.assertEquals(ImageType.WEB_P, shape.getImageData().getImageType());
 
```
## Поля

| Поле | Описание |
| --- | --- |
| [BMP](#BMP) | Windows Bitmap. |
| [EMF](#EMF) | Windows Enhanced Metafile. |
| [EPS](#EPS) | Encapsulated PostScript. |
| [GIF](#GIF) | GIF |
| [JPEG](#JPEG) | JPEG JFIF. |
| [NO_IMAGE](#NO-IMAGE) | Нет данных изображения. |
| [PICT](#PICT) | Macintosh PICT. |
| [PNG](#PNG) | Portable Network Graphics. |
| [UNKNOWN](#UNKNOWN) | Неизвестный тип изображения или тип изображения, который нельзя напрямую сохранить в документе Microsoft Word. |
| [WEB_P](#WEB-P) | WebP. |
| [WMF](#WMF) | Windows Metafile. |
| [length](#length) |  |
## Методы

| Метод | Описание |
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


Нет данных изображения.

### PICT {#PICT}
```
public static int PICT
```


Macintosh PICT. Существующее изображение будет сохранено в документе, но вставка новых изображений PICT в документ не поддерживается.

### PNG {#PNG}
```
public static int PNG
```


Portable Network Graphics.

### UNKNOWN {#UNKNOWN}
```
public static int UNKNOWN
```


Неизвестный тип изображения или тип изображения, который нельзя напрямую сохранить в документе Microsoft Word.

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
| Параметр | Тип | Описание |
| --- | --- | --- |
| imageTypeName | java.lang.String |  |

**Returns:**
int
### getName(int imageType) {#getName-int}
```
public static String getName(int imageType)
```




**Parameters:**
| Параметр | Тип | Описание |
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
| Параметр | Тип | Описание |
| --- | --- | --- |
| imageType | int |  |

**Returns:**
java.lang.String
