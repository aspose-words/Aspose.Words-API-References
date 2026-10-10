---
title: "SvgTextOutputMode"
linktitle: "SvgTextOutputMode"
second_title: "Aspose.Words Java için"
description: "Java'da SVG formatında kaydederken bir belgedeki metnin nasıl render edileceğini belirtmeye olanak tanır."
type: docs
weight: 650
url: /tr/java/com.aspose.words/svgtextoutputmode/
---

**Inheritance:**
java.lang.Object
```
public class SvgTextOutputMode
```

Belge içindeki metnin SVG formatında kaydedilirken nasıl render edileceğini belirtmeye izin verir.

 **Examples:** 

.docx belgesini .svg'ye dönüştürürken görüntü özelliklerini nasıl taklit edileceğini gösterir.

```

 Document doc = new Document(getMyDir() + "Document.docx");

 // Configure the SvgSaveOptions object to save with no page borders or selectable text.
 SvgSaveOptions options = new SvgSaveOptions();
 {
     options.setFitToViewPort(true);
     options.setShowPageBorder(false);
     options.setTextOutputMode(SvgTextOutputMode.USE_PLACED_GLYPHS);
 }

 doc.save(getArtifactsDir() + "SvgSaveOptions.SaveLikeImage.svg", options);
 
```
## Alanlar

| Alan | Açıklama |
| --- | --- |
| [USE_PLACED_GLYPHS](#USE-PLACED-GLYPHS) | Metin eğriler kullanılarak render edilir. |
| [USE_SVG_FONTS](#USE-SVG-FONTS) | Metni render etmek için SVG yazı tipleri kullanılır. |
| [USE_TARGET_MACHINE_FONTS](#USE-TARGET-MACHINE-FONTS) | Metni render etmek için hedef makinede yüklü yazı tipleri kullanılır. |
| [length](#length) |  |
## Yöntemler

| Yöntem | Açıklama |
| --- | --- |
| [fromName(String svgTextOutputModeName)](#fromName-java.lang.String) |  |
| [getName(int svgTextOutputMode)](#getName-int) |  |
| [getValues()](#getValues) |  |
| [toString(int svgTextOutputMode)](#toString-int) |  |
### USE_PLACED_GLYPHS {#USE-PLACED-GLYPHS}
```
public static int USE_PLACED_GLYPHS
```


Metin eğriler kullanılarak render edilir. Not: Bu seçeneği kullanırsanız metin seçimi çalışmayacaktır.

### USE_SVG_FONTS {#USE-SVG-FONTS}
```
public static int USE_SVG_FONTS
```


Metni render etmek için SVG yazı tipleri kullanılır. Not: Tüm tarayıcılar SVG yazı tiplerini desteklemez.

### USE_TARGET_MACHINE_FONTS {#USE-TARGET-MACHINE-FONTS}
```
public static int USE_TARGET_MACHINE_FONTS
```


Metni render etmek için hedef makinede yüklü yazı tipleri kullanılır. Not: Belgede kullanılan bazı yazı tipleri hedef makinede mevcut değilse, belge farklı görünebilir.

### length {#length}
```
public static int length
```


### fromName(String svgTextOutputModeName) {#fromName-java.lang.String}
```
public static int fromName(String svgTextOutputModeName)
```




**Parameters:**
| Parametre | Tür | Açıklama |
| --- | --- | --- |
| svgTextOutputModeName | java.lang.String |  |

**Returns:**
int
### getName(int svgTextOutputMode) {#getName-int}
```
public static String getName(int svgTextOutputMode)
```




**Parameters:**
| Parametre | Tür | Açıklama |
| --- | --- | --- |
| svgTextOutputMode | int |  |

**Returns:**
java.lang.String
### getValues() {#getValues}
```
public static int[] getValues()
```




**Returns:**
int[]
### toString(int svgTextOutputMode) {#toString-int}
```
public static String toString(int svgTextOutputMode)
```




**Parameters:**
| Parametre | Tür | Açıklama |
| --- | --- | --- |
| svgTextOutputMode | int |  |

**Returns:**
java.lang.String
