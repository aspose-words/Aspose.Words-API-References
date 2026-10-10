---
title: "ViewType"
linktitle: "ViewType"
second_title: "Aspose.Words Java için"
description: "Java'da Microsoft Word için görünüm modunun olası değerleri."
type: docs
weight: 715
url: /tr/java/com.aspose.words/viewtype/
---

**Inheritance:**
java.lang.Object
```
public class ViewType
```

Microsoft Word'deki görünüm modunun olası değerleri.

 **Examples:** 

Eski Microsoft Word sürümlerinin bir belgeyi yüklerken uygulayacağı özel bir yakınlaştırma faktörünün nasıl ayarlanacağını gösterir.

```

 Document doc = new Document();
 DocumentBuilder builder = new DocumentBuilder(doc);
 builder.writeln("Hello world!");

 doc.getViewOptions().setViewType(ViewType.PAGE_LAYOUT);
 doc.getViewOptions().setZoomPercent(50);

 Assert.assertEquals(ZoomType.CUSTOM, doc.getViewOptions().getZoomType());
 Assert.assertEquals(ZoomType.NONE, doc.getViewOptions().getZoomType());

 doc.save(getArtifactsDir() + "ViewOptions.SetZoomPercentage.doc");
 
```
## Alanlar

| Alan | Açıklama |
| --- | --- |
| [NONE](#NONE) | Belge, uygulamanın varsayılan görünümünde render edilecektir. |
| [NORMAL](#NORMAL) | Belge, taslak oluşturma veya uzun belgeler oluşturma için optimize edilmiş bir görünümde render edilecektir. |
| [OUTLINE](#OUTLINE) | Belge, taslak oluşturma veya uzun belgeler oluşturma için optimize edilmiş bir görünümde render edilecektir. |
| [PAGE_LAYOUT](#PAGE-LAYOUT) | Belge, belgenin yazdırılacağı şekilde gösteren bir görünümde açılacaktır. |
| [READING](#READING) | Belge, uygulamanın varsayılan görünümünde render edilecektir. |
| [WEB](#WEB) | Belge, bu belgenin bir web sayfasında gösterileceği şekli taklit eden bir görünümde render edilecektir. |
| [length](#length) |  |
## Yöntemler

| Yöntem | Açıklama |
| --- | --- |
| [fromName(String viewTypeName)](#fromName-java.lang.String) |  |
| [getName(int viewType)](#getName-int) |  |
| [getValues()](#getValues) |  |
| [toString(int viewType)](#toString-int) |  |
### NONE {#NONE}
```
public static int NONE
```


Belge, uygulamanın varsayılan görünümünde render edilecektir.

### NORMAL {#NORMAL}
```
public static int NORMAL
```


Belge, taslak oluşturma veya uzun belgeler oluşturma için optimize edilmiş bir görünümde render edilecektir.

### OUTLINE {#OUTLINE}
```
public static int OUTLINE
```


Belge, taslak oluşturma veya uzun belgeler oluşturma için optimize edilmiş bir görünümde render edilecektir.

### PAGE_LAYOUT {#PAGE-LAYOUT}
```
public static int PAGE_LAYOUT
```


Belge, belgenin yazdırılacağı şekilde gösteren bir görünümde açılacaktır.

### READING {#READING}
```
public static int READING
```


Belge, uygulamanın varsayılan görünümünde render edilecektir.

### WEB {#WEB}
```
public static int WEB
```


Belge, bu belgenin bir web sayfasında gösterileceği şekli taklit eden bir görünümde render edilecektir.

### length {#length}
```
public static int length
```


### fromName(String viewTypeName) {#fromName-java.lang.String}
```
public static int fromName(String viewTypeName)
```




**Parameters:**
| Parametre | Tür | Açıklama |
| --- | --- | --- |
| viewTypeName | java.lang.String |  |

**Returns:**
int
### getName(int viewType) {#getName-int}
```
public static String getName(int viewType)
```




**Parameters:**
| Parametre | Tür | Açıklama |
| --- | --- | --- |
| viewType | int |  |

**Returns:**
java.lang.String
### getValues() {#getValues}
```
public static int[] getValues()
```




**Returns:**
int[]
### toString(int viewType) {#toString-int}
```
public static String toString(int viewType)
```




**Parameters:**
| Parametre | Tür | Açıklama |
| --- | --- | --- |
| viewType | int |  |

**Returns:**
java.lang.String
