---
title: "RelativeHorizontalPosition"
linktitle: "RelativeHorizontalPosition"
second_title: "Aspose.Words Java için"
description: "Java'da bir şekil veya metin çerçevesinin yatay konumunun neye göre olduğunu belirtir."
type: docs
weight: 561
url: /tr/java/com.aspose.words/relativehorizontalposition/
---

**Inheritance:**
java.lang.Object
```
public class RelativeHorizontalPosition
```

Bir şeklin veya metin çerçevesinin yatay konumunun neye göre olduğunu belirtir.

 **Examples:** 

Bir görüntünün nasıl ekleneceğini ve filigran olarak nasıl kullanılacağını gösterir.

```

 Document doc = new Document();
 DocumentBuilder builder = new DocumentBuilder(doc);

 // Insert the image into the header so that it will be visible on every page.
 builder.moveToHeaderFooter(HeaderFooterType.HEADER_PRIMARY);
 Shape shape = builder.insertImage(getImageDir() + "Transparent background logo.png");
 shape.setWrapType(WrapType.NONE);
 shape.setBehindText(true);

 // Place the image at the center of the page.
 shape.setRelativeHorizontalPosition(RelativeHorizontalPosition.PAGE);
 shape.setRelativeVerticalPosition(RelativeVerticalPosition.PAGE);
 shape.setLeft((builder.getPageSetup().getPageWidth() - shape.getWidth()) / 2.0);
 shape.setTop((builder.getPageSetup().getPageHeight() - shape.getHeight()) / 2.0);

 doc.save(getArtifactsDir() + "DocumentBuilder.InsertWatermark.docx");
 
```

Yüzen bir görüntünün sayfanın ortasına nasıl ekleneceğini gösterir.

```

 Document doc = new Document();
 DocumentBuilder builder = new DocumentBuilder(doc);

 // Insert a floating image that will appear behind the overlapping text and align it to the page's center.
 Shape shape = builder.insertImage(getImageDir() + "Logo.jpg");
 shape.setWrapType(WrapType.NONE);
 shape.setBehindText(true);
 shape.setRelativeHorizontalPosition(RelativeHorizontalPosition.PAGE);
 shape.setRelativeVerticalPosition(RelativeVerticalPosition.PAGE);
 shape.setHorizontalAlignment(HorizontalAlignment.CENTER);
 shape.setVerticalAlignment(VerticalAlignment.CENTER);

 doc.save(getArtifactsDir() + "Image.CreateFloatingPageCenter.docx");
 
```
## Alanlar

| Alan | Açıklama |
| --- | --- |
| [CHARACTER](#CHARACTER) | Nesne, paragrafın sol tarafına göre konumlandırılır. |
| [COLUMN](#COLUMN) | Nesne, sütunun sol tarafına göre konumlandırılır. |
| [DEFAULT](#DEFAULT) | Varsayılan değer [COLUMN](../../com.aspose.words/relativehorizontalposition/\#COLUMN). |
| [INSIDE_MARGIN](#INSIDE-MARGIN) | Yatay konumlamanın geçerli sayfanın iç kenarına göre olacağını belirtir (tek sayfalarda sol kenar, çift sayfalarda sağ kenar). |
| [LEFT_MARGIN](#LEFT-MARGIN) | Yatay konumlamanın sayfanın sol kenarına göre olacağını belirtir. |
| [MARGIN](#MARGIN) | Yatay konumlamanın sayfa kenar boşluklarına göre olacağını belirtir. |
| [OUTSIDE_MARGIN](#OUTSIDE-MARGIN) | Yatay konumlamanın geçerli sayfanın dış kenarına göre olacağını belirtir (tek sayfalarda sağ kenar, çift sayfalarda sol kenar). |
| [PAGE](#PAGE) | Nesne, sayfanın sol kenarına göre konumlandırılır. |
| [RIGHT_MARGIN](#RIGHT-MARGIN) | Yatay konumlamanın sayfanın sağ kenarına göre olacağını belirtir. |
| [length](#length) |  |
## Yöntemler

| Yöntem | Açıklama |
| --- | --- |
| [fromName(String relativeHorizontalPositionName)](#fromName-java.lang.String) |  |
| [getName(int relativeHorizontalPosition)](#getName-int) |  |
| [getValues()](#getValues) |  |
| [toString(int relativeHorizontalPosition)](#toString-int) |  |
### CHARACTER {#CHARACTER}
```
public static int CHARACTER
```


Nesne, paragrafın sol tarafına göre konumlandırılır.

### COLUMN {#COLUMN}
```
public static int COLUMN
```


Nesne, sütunun sol tarafına göre konumlandırılır.

### DEFAULT {#DEFAULT}
```
public static int DEFAULT
```


Varsayılan değer [COLUMN](../../com.aspose.words/relativehorizontalposition/\#COLUMN).

### INSIDE_MARGIN {#INSIDE-MARGIN}
```
public static int INSIDE_MARGIN
```


Yatay konumlamanın geçerli sayfanın iç kenarına göre olacağını belirtir (tek sayfalarda sol kenar, çift sayfalarda sağ kenar).

### LEFT_MARGIN {#LEFT-MARGIN}
```
public static int LEFT_MARGIN
```


Yatay konumlamanın sayfanın sol kenarına göre olacağını belirtir.

### MARGIN {#MARGIN}
```
public static int MARGIN
```


Yatay konumlamanın sayfa kenar boşluklarına göre olacağını belirtir.

### OUTSIDE_MARGIN {#OUTSIDE-MARGIN}
```
public static int OUTSIDE_MARGIN
```


Yatay konumlamanın geçerli sayfanın dış kenarına göre olacağını belirtir (tek sayfalarda sağ kenar, çift sayfalarda sol kenar).

### PAGE {#PAGE}
```
public static int PAGE
```


Nesne, sayfanın sol kenarına göre konumlandırılır.

### RIGHT_MARGIN {#RIGHT-MARGIN}
```
public static int RIGHT_MARGIN
```


Yatay konumlamanın sayfanın sağ kenarına göre olacağını belirtir.

### length {#length}
```
public static int length
```


### fromName(String relativeHorizontalPositionName) {#fromName-java.lang.String}
```
public static int fromName(String relativeHorizontalPositionName)
```




**Parameters:**
| Parametre | Tür | Açıklama |
| --- | --- | --- |
| relativeHorizontalPositionName | java.lang.String |  |

**Returns:**
int
### getName(int relativeHorizontalPosition) {#getName-int}
```
public static String getName(int relativeHorizontalPosition)
```




**Parameters:**
| Parametre | Tür | Açıklama |
| --- | --- | --- |
| relativeHorizontalPosition | int |  |

**Returns:**
java.lang.String
### getValues() {#getValues}
```
public static int[] getValues()
```




**Returns:**
int[]
### toString(int relativeHorizontalPosition) {#toString-int}
```
public static String toString(int relativeHorizontalPosition)
```




**Parameters:**
| Parametre | Tür | Açıklama |
| --- | --- | --- |
| relativeHorizontalPosition | int |  |

**Returns:**
java.lang.String
