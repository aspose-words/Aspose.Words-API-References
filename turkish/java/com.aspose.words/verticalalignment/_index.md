---
title: "VerticalAlignment"
linktitle: "VerticalAlignment"
second_title: "Aspose.Words Java için"
description: "Java'da yüzen şekil metin çerçevesi veya yüzen tablonun dikey hizalamasını belirtir."
type: docs
weight: 713
url: /tr/java/com.aspose.words/verticalalignment/
---

**Inheritance:**
java.lang.Object
```
public class VerticalAlignment
```

Yüzen bir şeklin, metin çerçevesinin veya yüzen bir tablonun dikey hizalamasını belirtir.

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
| [BOTTOM](#BOTTOM) | Nesnenin dikey hizalama tabanının altında olacağını belirtir. |
| [CENTER](#CENTER) | Nesnenin dikey hizalama tabanına göre ortalanacağını belirtir. |
| [DEFAULT](#DEFAULT) | Aynı [NONE](../../com.aspose.words/verticalalignment/\#NONE) gibi. |
| [INLINE](#INLINE) | Belirtilmemiş. |
| [INSIDE](#INSIDE) | Nesnenin yatay hizalama temelinin içinde olması gerektiğini belirtir. |
| [NONE](#NONE) | Nesne açıkça konumlandırılmıştır, genellikle **Top** özelliği kullanılarak. |
| [OUTSIDE](#OUTSIDE) | Nesnenin dikey hizalama temelinin dışında olması gerektiğini belirtir. |
| [TOP](#TOP) | Nesnenin dikey hizalama temelinin üstünde olması gerektiğini belirtir. |
| [length](#length) |  |
## Yöntemler

| Yöntem | Açıklama |
| --- | --- |
| [fromName(String verticalAlignmentName)](#fromName-java.lang.String) |  |
| [getName(int verticalAlignment)](#getName-int) |  |
| [getValues()](#getValues) |  |
| [toString(int verticalAlignment)](#toString-int) |  |
### BOTTOM {#BOTTOM}
```
public static int BOTTOM
```


Nesnenin dikey hizalama tabanının altında olacağını belirtir.

### CENTER {#CENTER}
```
public static int CENTER
```


Nesnenin dikey hizalama tabanına göre ortalanacağını belirtir.

### DEFAULT {#DEFAULT}
```
public static int DEFAULT
```


Aynı [NONE](../../com.aspose.words/verticalalignment/\#NONE) gibi.

### INLINE {#INLINE}
```
public static int INLINE
```


Belirtilmemiş. Yüzen paragraflar ve tablolar için olası bir değer gibi görünüyor.

### INSIDE {#INSIDE}
```
public static int INSIDE
```


Nesnenin yatay hizalama temelinin içinde olması gerektiğini belirtir.

### NONE {#NONE}
```
public static int NONE
```


Nesne açıkça konumlandırılmıştır, genellikle **Top** özelliği kullanılarak.

### OUTSIDE {#OUTSIDE}
```
public static int OUTSIDE
```


Nesnenin dikey hizalama temelinin dışında olması gerektiğini belirtir.

### TOP {#TOP}
```
public static int TOP
```


Nesnenin dikey hizalama temelinin üstünde olması gerektiğini belirtir.

### length {#length}
```
public static int length
```


### fromName(String verticalAlignmentName) {#fromName-java.lang.String}
```
public static int fromName(String verticalAlignmentName)
```




**Parameters:**
| Parametre | Tür | Açıklama |
| --- | --- | --- |
| verticalAlignmentName | java.lang.String |  |

**Returns:**
int
### getName(int verticalAlignment) {#getName-int}
```
public static String getName(int verticalAlignment)
```




**Parameters:**
| Parametre | Tür | Açıklama |
| --- | --- | --- |
| verticalAlignment | int |  |

**Returns:**
java.lang.String
### getValues() {#getValues}
```
public static int[] getValues()
```




**Returns:**
int[]
### toString(int verticalAlignment) {#toString-int}
```
public static String toString(int verticalAlignment)
```




**Parameters:**
| Parametre | Tür | Açıklama |
| --- | --- | --- |
| verticalAlignment | int |  |

**Returns:**
java.lang.String
