---
title: "WrapType"
linktitle: "WrapType"
second_title: "Aspose.Words Java için"
description: "Java'da metnin bir şekil veya resim etrafında nasıl sarılacağını belirtir."
type: docs
weight: 737
url: /tr/java/com.aspose.words/wraptype/
---

**Inheritance:**
java.lang.Object
```
public class WrapType
```

Metnin şekil veya resim etrafında nasıl dolandığını belirtir.

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
| [INLINE](#INLINE) | Şekil, metinle aynı katmanda kalır ve bir karakter olarak ele alınır. |
| [NONE](#NONE) | Şekil etrafında metin sarma yok. |
| [SQUARE](#SQUARE) | Metni şeklin kare sınırlayıcı kutusunun tüm kenarları etrafında sarar. |
| [THROUGH](#THROUGH) | Tight ile aynı, ancak şeklin açık olan herhangi bir kısmının içinde sarar. |
| [TIGHT](#TIGHT) | Şeklin kenarları etrafında sıkı bir şekilde sarar, sınırlayıcı kutu etrafında sarmak yerine. |
| [TOP_BOTTOM](#TOP-BOTTOM) | Metin, şeklin üstünde durur ve şeklin altındaki satırda yeniden başlar. |
| [length](#length) |  |
## Yöntemler

| Yöntem | Açıklama |
| --- | --- |
| [fromName(String wrapTypeName)](#fromName-java.lang.String) |  |
| [getName(int wrapType)](#getName-int) |  |
| [getValues()](#getValues) |  |
| [toString(int wrapType)](#toString-int) |  |
### INLINE {#INLINE}
```
public static int INLINE
```


Şekil, metinle aynı katmanda kalır ve bir karakter olarak ele alınır.

### NONE {#NONE}
```
public static int NONE
```


Şekil etrafında metin sarma yok. Şekil, metnin arkasına veya önüne yerleştirilir.

### SQUARE {#SQUARE}
```
public static int SQUARE
```


Metni şeklin kare sınırlayıcı kutusunun tüm kenarları etrafında sarar.

### THROUGH {#THROUGH}
```
public static int THROUGH
```


Tight ile aynı, ancak şeklin açık olan herhangi bir kısmının içinde sarar.

### TIGHT {#TIGHT}
```
public static int TIGHT
```


Şeklin kenarları etrafında sıkı bir şekilde sarar, sınırlayıcı kutu etrafında sarmak yerine.

### TOP_BOTTOM {#TOP-BOTTOM}
```
public static int TOP_BOTTOM
```


Metin, şeklin üstünde durur ve şeklin altındaki satırda yeniden başlar.

### length {#length}
```
public static int length
```


### fromName(String wrapTypeName) {#fromName-java.lang.String}
```
public static int fromName(String wrapTypeName)
```




**Parameters:**
| Parametre | Tür | Açıklama |
| --- | --- | --- |
| wrapTypeName | java.lang.String |  |

**Returns:**
int
### getName(int wrapType) {#getName-int}
```
public static String getName(int wrapType)
```




**Parameters:**
| Parametre | Tür | Açıklama |
| --- | --- | --- |
| wrapType | int |  |

**Returns:**
java.lang.String
### getValues() {#getValues}
```
public static int[] getValues()
```




**Returns:**
int[]
### toString(int wrapType) {#toString-int}
```
public static String toString(int wrapType)
```




**Parameters:**
| Parametre | Tür | Açıklama |
| --- | --- | --- |
| wrapType | int |  |

**Returns:**
java.lang.String
