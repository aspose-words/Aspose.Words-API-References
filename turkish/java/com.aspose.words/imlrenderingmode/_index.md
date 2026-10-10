---
title: "ImlRenderingMode"
linktitle: "ImlRenderingMode"
second_title: "Aspose.Words Java için"
description: "Java'da ink InkML nesnelerinin sabit sayfa formatlarına nasıl render edildiğini belirtir."
type: docs
weight: 399
url: /tr/java/com.aspose.words/imlrenderingmode/
---

**Inheritance:**
java.lang.Object
```
public class ImlRenderingMode
```

Mürekkep (InkML) nesnelerinin sabit sayfa biçimlerine nasıl render edildiğini belirtir.

 **Examples:** 

Ink nesnesinin nasıl render edileceğini gösterir.

```

 Document doc = new Document(getMyDir() + "Ink object.docx");

 // Set 'ImlRenderingMode.InkML' ignores fall-back shape of ink (InkML) object and renders InkML itself.
 // If the rendering result is unsatisfactory,
 // please use 'ImlRenderingMode.Fallback' to get a result similar to previous versions.
 ImageSaveOptions saveOptions = new ImageSaveOptions(SaveFormat.JPEG);
 {
     saveOptions.setImlRenderingMode(ImlRenderingMode.INK_ML);
 }

 doc.save(getArtifactsDir() + "ImageSaveOptions.RenderInkObject.jpeg", saveOptions);
 
```
## Alanlar

| Alan | Açıklama |
| --- | --- |
| [FALLBACK](#FALLBACK) | Eğer ink (InkML) nesnesi için geri dönüş şekli mevcutsa, Aspose.Words InkML yerine geri dönüş şeklini render eder. |
| [INK_ML](#INK-ML) | Aspose.Words, ink (InkML) nesnesinin geri dönüş şeklini yok sayar ve InkML'yi kendisi render eder. |
| [length](#length) |  |
## Yöntemler

| Yöntem | Açıklama |
| --- | --- |
| [fromName(String imlRenderingModeName)](#fromName-java.lang.String) |  |
| [getName(int imlRenderingMode)](#getName-int) |  |
| [getValues()](#getValues) |  |
| [toString(int imlRenderingMode)](#toString-int) |  |
### FALLBACK {#FALLBACK}
```
public static int FALLBACK
```


Eğer ink (InkML) nesnesi için geri dönüş şekli mevcutsa, Aspose.Words InkML yerine geri dönüş şeklini render eder.

 **Remarks:** 

Lütfen unutmayın ki, bir belgeyi geri dönüş render moduyla sabit sayfa formatına kaydettikten sonra, AW belge modelindeki InkML nesneleri kalıcı olarak geri dönüş karşılıklarıyla değiştirilir. Sonuç olarak, aynı belgeyi tekrar kaydetmek her zaman geri dönüş şekillerini kullanacaktır, hatta [ImlRenderingMode](../../com.aspose.words/imlrenderingmode/) [INK\_ML](../../com.aspose.words/imlrenderingmode/\#INK-ML) olarak ayarlı olsa bile.

### INK_ML {#INK-ML}
```
public static int INK_ML
```


Aspose.Words, ink (InkML) nesnesinin geri dönüş şeklini yok sayar ve InkML'yi kendisi render eder. Bu varsayılan moddur.

### length {#length}
```
public static int length
```


### fromName(String imlRenderingModeName) {#fromName-java.lang.String}
```
public static int fromName(String imlRenderingModeName)
```




**Parameters:**
| Parametre | Tür | Açıklama |
| --- | --- | --- |
| imlRenderingModeName | java.lang.String |  |

**Returns:**
int
### getName(int imlRenderingMode) {#getName-int}
```
public static String getName(int imlRenderingMode)
```




**Parameters:**
| Parametre | Tür | Açıklama |
| --- | --- | --- |
| imlRenderingMode | int |  |

**Returns:**
java.lang.String
### getValues() {#getValues}
```
public static int[] getValues()
```




**Returns:**
int[]
### toString(int imlRenderingMode) {#toString-int}
```
public static String toString(int imlRenderingMode)
```




**Parameters:**
| Parametre | Tür | Açıklama |
| --- | --- | --- |
| imlRenderingMode | int |  |

**Returns:**
java.lang.String
