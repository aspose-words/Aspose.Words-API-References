---
title: "ZoomType"
linktitle: "ZoomType"
second_title: "Aspose.Words Java için"
description: "Microsoft Word'te Java'da belgenin ekranda ne kadar büyük veya küçük göründüğüne ilişkin olası değerler."
type: docs
weight: 751
url: /tr/java/com.aspose.words/zoomtype/
---

**Inheritance:**
java.lang.Object
```
public class ZoomType
```

Microsoft Word'de belgenin ekranda ne kadar büyük veya küçük görüneceğine ilişkin olası değerler.

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
| [CUSTOM](#CUSTOM) | Yakınlaştırma yüzdesi açıkça ayarlanır. |
| [FULL_PAGE](#FULL-PAGE) | Yakınlaştırma yüzdesi bir tam sayfaya sığacak şekilde otomatik olarak yeniden hesaplanır. |
| [NONE](#NONE) | Açık yakınlaştırma yüzdesinin kullanılacağını gösterir. |
| [PAGE_WIDTH](#PAGE-WIDTH) | Yakınlaştırma yüzdesi sayfa genişliğine sığacak şekilde otomatik olarak yeniden hesaplanır. |
| [TEXT_FIT](#TEXT-FIT) | Yakınlaştırma yüzdesi metne sığacak şekilde otomatik olarak yeniden hesaplanır. |
| [length](#length) |  |
## Yöntemler

| Yöntem | Açıklama |
| --- | --- |
| [fromName(String zoomTypeName)](#fromName-java.lang.String) |  |
| [getName(int zoomType)](#getName-int) |  |
| [getValues()](#getValues) |  |
| [toString(int zoomType)](#toString-int) |  |
### CUSTOM {#CUSTOM}
```
public static int CUSTOM
```


Yakınlaştırma yüzdesi açıkça ayarlanır. Kontrol boyutu değiştiğinde otomatik olarak yeniden hesaplanmaz.

### FULL_PAGE {#FULL-PAGE}
```
public static int FULL_PAGE
```


Yakınlaştırma yüzdesi bir tam sayfaya sığacak şekilde otomatik olarak yeniden hesaplanır.

### NONE {#NONE}
```
public static int NONE
```


Açık yakınlaştırma yüzdesinin kullanılacağını gösterir. Aynı [CUSTOM](../../com.aspose.words/zoomtype/\#CUSTOM) ile.

### PAGE_WIDTH {#PAGE-WIDTH}
```
public static int PAGE_WIDTH
```


Yakınlaştırma yüzdesi sayfa genişliğine sığacak şekilde otomatik olarak yeniden hesaplanır.

### TEXT_FIT {#TEXT-FIT}
```
public static int TEXT_FIT
```


Yakınlaştırma yüzdesi metne sığacak şekilde otomatik olarak yeniden hesaplanır.

### length {#length}
```
public static int length
```


### fromName(String zoomTypeName) {#fromName-java.lang.String}
```
public static int fromName(String zoomTypeName)
```




**Parameters:**
| Parametre | Tür | Açıklama |
| --- | --- | --- |
| zoomTypeName | java.lang.String |  |

**Returns:**
int
### getName(int zoomType) {#getName-int}
```
public static String getName(int zoomType)
```




**Parameters:**
| Parametre | Tür | Açıklama |
| --- | --- | --- |
| zoomType | int |  |

**Returns:**
java.lang.String
### getValues() {#getValues}
```
public static int[] getValues()
```




**Returns:**
int[]
### toString(int zoomType) {#toString-int}
```
public static String toString(int zoomType)
```




**Parameters:**
| Parametre | Tür | Açıklama |
| --- | --- | --- |
| zoomType | int |  |

**Returns:**
java.lang.String
