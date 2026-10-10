---
title: "RelativeVerticalPosition"
linktitle: "RelativeVerticalPosition"
second_title: "Aspose.Words Java için"
description: "Bir şeklin veya metin çerçevesinin dikey konumunun Java'da neye göre olduğunu belirtir."
type: docs
weight: 563
url: /tr/java/com.aspose.words/relativeverticalposition/
---

**Inheritance:**
java.lang.Object
```
public class RelativeVerticalPosition
```

Bir şeklin veya metin çerçevesinin dikey konumunun neye göre olduğunu belirtir.

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
| [BOTTOM_MARGIN](#BOTTOM-MARGIN) | Dikey konumlamanın geçerli sayfanın alt kenar boşluğuna göre olacağını belirtir. |
| [INSIDE_MARGIN](#INSIDE-MARGIN) | Dikey konumlamanın geçerli sayfanın iç kenar boşluğuna göre olacağını belirtir. |
| [LINE](#LINE) | Belgelendirilmemiş. |
| [MARGIN](#MARGIN) | Dikey konumlamanın sayfa kenar boşluklarına göre olacağını belirtir. |
| [OUTSIDE_MARGIN](#OUTSIDE-MARGIN) | Dikey konumlamanın geçerli sayfanın dış kenar boşluğuna göre olacağını belirtir. |
| [PAGE](#PAGE) | Nesne, sayfanın üst kenarına göre konumlandırılmıştır. |
| [PARAGRAPH](#PARAGRAPH) | Nesne, bağlantıyı içeren paragrafın üst kısmına göre konumlandırılmıştır. |
| [TABLE_DEFAULT](#TABLE-DEFAULT) | Varsayılan değer [MARGIN](../../com.aspose.words/relativeverticalposition/\#MARGIN). |
| [TEXT_FRAME_DEFAULT](#TEXT-FRAME-DEFAULT) | Varsayılan değer [PARAGRAPH](../../com.aspose.words/relativeverticalposition/\#PARAGRAPH). |
| [TOP_MARGIN](#TOP-MARGIN) | Dikey konumlamanın geçerli sayfanın üst kenar boşluğuna göre olacağını belirtir. |
| [length](#length) |  |
## Yöntemler

| Yöntem | Açıklama |
| --- | --- |
| [fromName(String relativeVerticalPositionName)](#fromName-java.lang.String) |  |
| [getName(int relativeVerticalPosition)](#getName-int) |  |
| [getValues()](#getValues) |  |
| [toString(int relativeVerticalPosition)](#toString-int) |  |
### BOTTOM_MARGIN {#BOTTOM-MARGIN}
```
public static int BOTTOM_MARGIN
```


Dikey konumlamanın geçerli sayfanın alt kenar boşluğuna göre olacağını belirtir.

### INSIDE_MARGIN {#INSIDE-MARGIN}
```
public static int INSIDE_MARGIN
```


Dikey konumlamanın geçerli sayfanın iç kenar boşluğuna göre olacağını belirtir.

### LINE {#LINE}
```
public static int LINE
```


Belgelendirilmemiş.

### MARGIN {#MARGIN}
```
public static int MARGIN
```


Dikey konumlamanın sayfa kenar boşluklarına göre olacağını belirtir.

### OUTSIDE_MARGIN {#OUTSIDE-MARGIN}
```
public static int OUTSIDE_MARGIN
```


Dikey konumlamanın geçerli sayfanın dış kenar boşluğuna göre olacağını belirtir.

### PAGE {#PAGE}
```
public static int PAGE
```


Nesne, sayfanın üst kenarına göre konumlandırılmıştır.

### PARAGRAPH {#PARAGRAPH}
```
public static int PARAGRAPH
```


Nesne, bağlantıyı içeren paragrafın üst kısmına göre konumlandırılmıştır.

### TABLE_DEFAULT {#TABLE-DEFAULT}
```
public static int TABLE_DEFAULT
```


Varsayılan değer [MARGIN](../../com.aspose.words/relativeverticalposition/\#MARGIN).

### TEXT_FRAME_DEFAULT {#TEXT-FRAME-DEFAULT}
```
public static int TEXT_FRAME_DEFAULT
```


Varsayılan değer [PARAGRAPH](../../com.aspose.words/relativeverticalposition/\#PARAGRAPH).

### TOP_MARGIN {#TOP-MARGIN}
```
public static int TOP_MARGIN
```


Dikey konumlamanın geçerli sayfanın üst kenar boşluğuna göre olacağını belirtir.

### length {#length}
```
public static int length
```


### fromName(String relativeVerticalPositionName) {#fromName-java.lang.String}
```
public static int fromName(String relativeVerticalPositionName)
```




**Parameters:**
| Parametre | Tür | Açıklama |
| --- | --- | --- |
| relativeVerticalPositionName | java.lang.String |  |

**Returns:**
int
### getName(int relativeVerticalPosition) {#getName-int}
```
public static String getName(int relativeVerticalPosition)
```




**Parameters:**
| Parametre | Tür | Açıklama |
| --- | --- | --- |
| relativeVerticalPosition | int |  |

**Returns:**
java.lang.String
### getValues() {#getValues}
```
public static int[] getValues()
```




**Returns:**
int[]
### toString(int relativeVerticalPosition) {#toString-int}
```
public static String toString(int relativeVerticalPosition)
```




**Parameters:**
| Parametre | Tür | Açıklama |
| --- | --- | --- |
| relativeVerticalPosition | int |  |

**Returns:**
java.lang.String
