---
title: "HorizontalAlignment"
linktitle: "HorizontalAlignment"
second_title: "Aspose.Words Java için"
description: "Java'da yüzen şekil metin çerçevesi veya yüzen tablo için yatay hizalamayı belirtir."
type: docs
weight: 374
url: /tr/java/com.aspose.words/horizontalalignment/
---

**Inheritance:**
java.lang.Object
```
public class HorizontalAlignment
```

Yüzen bir şeklin, metin çerçevesinin veya yüzen bir tablonun yatay hizalamasını belirtir.

 **Examples:** 

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
| [CENTER](#CENTER) | Nesnenin yatay hizalama tabanına göre ortalanacağını belirtir. |
| [DEFAULT](#DEFAULT) | Aynı gibi [NONE](../../com.aspose.words/horizontalalignment/\#NONE). |
| [INSIDE](#INSIDE) | Nesnenin yatay hizalama temelinin içinde olması gerektiğini belirtir. |
| [LEFT](#LEFT) | Nesnenin yatay hizalama tabanına sola hizalanacağını belirtir. |
| [NONE](#NONE) | Nesne açıkça konumlandırılır, genellikle **Left** özelliği kullanılarak. |
| [OUTSIDE](#OUTSIDE) | Nesnenin yatay hizalama tabanının dışında olacağını belirtir. |
| [RIGHT](#RIGHT) | Nesnenin yatay hizalama tabanına sağa hizalanacağını belirtir. |
| [length](#length) |  |
## Yöntemler

| Yöntem | Açıklama |
| --- | --- |
| [fromName(String horizontalAlignmentName)](#fromName-java.lang.String) |  |
| [getName(int horizontalAlignment)](#getName-int) |  |
| [getValues()](#getValues) |  |
| [toString(int horizontalAlignment)](#toString-int) |  |
### CENTER {#CENTER}
```
public static int CENTER
```


Nesnenin yatay hizalama tabanına göre ortalanacağını belirtir.

### DEFAULT {#DEFAULT}
```
public static int DEFAULT
```


Aynı gibi [NONE](../../com.aspose.words/horizontalalignment/\#NONE).

### INSIDE {#INSIDE}
```
public static int INSIDE
```


Nesnenin yatay hizalama temelinin içinde olması gerektiğini belirtir.

### LEFT {#LEFT}
```
public static int LEFT
```


Nesnenin yatay hizalama tabanına sola hizalanacağını belirtir.

### NONE {#NONE}
```
public static int NONE
```


Nesne açıkça konumlandırılır, genellikle **Left** özelliği kullanılarak.

### OUTSIDE {#OUTSIDE}
```
public static int OUTSIDE
```


Nesnenin yatay hizalama tabanının dışında olacağını belirtir.

### RIGHT {#RIGHT}
```
public static int RIGHT
```


Nesnenin yatay hizalama tabanına sağa hizalanacağını belirtir.

### length {#length}
```
public static int length
```


### fromName(String horizontalAlignmentName) {#fromName-java.lang.String}
```
public static int fromName(String horizontalAlignmentName)
```




**Parameters:**
| Parametre | Tür | Açıklama |
| --- | --- | --- |
| horizontalAlignmentName | java.lang.String |  |

**Returns:**
int
### getName(int horizontalAlignment) {#getName-int}
```
public static String getName(int horizontalAlignment)
```




**Parameters:**
| Parametre | Tür | Açıklama |
| --- | --- | --- |
| horizontalAlignment | int |  |

**Returns:**
java.lang.String
### getValues() {#getValues}
```
public static int[] getValues()
```




**Returns:**
int[]
### toString(int horizontalAlignment) {#toString-int}
```
public static String toString(int horizontalAlignment)
```




**Parameters:**
| Parametre | Tür | Açıklama |
| --- | --- | --- |
| horizontalAlignment | int |  |

**Returns:**
java.lang.String
