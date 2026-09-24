---
title: "HtmlOfficeMathOutputMode"
linktitle: "HtmlOfficeMathOutputMode"
second_title: "Aspose.Words Java için"
description: "Aspose.Words'un Java'da OfficeMath'ı HTML, MHTML ve EPUB formatlarına nasıl dışa aktardığını belirtir."
type: docs
weight: 384
url: /tr/java/com.aspose.words/htmlofficemathoutputmode/
---

**Inheritance:**
java.lang.Object
```
public class HtmlOfficeMathOutputMode
```

Aspose.Words'ün OfficeMath'ı HTML, MHTML ve EPUB'a nasıl dışa aktardığını belirtir.

 **Examples:** 

Microsoft OfficeMath nesnelerinin HTML'ye nasıl dışa aktarılacağını gösterir.

```

 Document doc = new Document(getMyDir() + "Office math.docx");

 // When we save the document to HTML, we can pass a SaveOptions object
 // to determine how the saving operation handles OfficeMath objects.
 // Setting the "OfficeMathOutputMode" property to "HtmlOfficeMathOutputMode.Image"
 // will render each OfficeMath object into an image.
 // Setting the "OfficeMathOutputMode" property to "HtmlOfficeMathOutputMode.MathML"
 // will convert each OfficeMath object into MathML.
 // Setting the "OfficeMathOutputMode" property to "HtmlOfficeMathOutputMode.Text"
 // will represent each OfficeMath formula using plain HTML text.
 HtmlSaveOptions options = new HtmlSaveOptions();
 {
     options.setOfficeMathOutputMode(htmlOfficeMathOutputMode);
 }

 doc.save(getArtifactsDir() + "HtmlSaveOptions.OfficeMathOutputMode.html", options);
 
```
## Alanlar

| Alan | Açıklama |
| --- | --- |
|  | [IMAGE](#IMAGE) | OfficeMath, ![Image 1][] etiketiyle belirtilen bir görüntü olarak HTML'ye dönüştürülür. |


[Image 1]:  |
| [MATH_ML](#MATH-ML) | OfficeMath, MathML kullanılarak HTML'ye dönüştürülür. |
| [TEXT](#TEXT) | OfficeMath,  etiketleriyle belirtilen bir koşul dizisi olarak HTML'ye dönüştürülür. |
| [length](#length) |  |
## Yöntemler

| Yöntem | Açıklama |
| --- | --- |
| [fromName(String htmlOfficeMathOutputModeName)](#fromName-java.lang.String) |  |
| [getName(int htmlOfficeMathOutputMode)](#getName-int) |  |
| [getValues()](#getValues) |  |
| [toString(int htmlOfficeMathOutputMode)](#toString-int) |  |
### IMAGE {#IMAGE}
```
public static int IMAGE
```


OfficeMath, ![Image 1][] etiketiyle belirtilen bir görüntü olarak HTML'ye dönüştürülür.


[Image 1]: 

### MATH_ML {#MATH-ML}
```
public static int MATH_ML
```


OfficeMath, MathML kullanılarak HTML'ye dönüştürülür.

### TEXT {#TEXT}
```
public static int TEXT
```


OfficeMath,  etiketleriyle belirtilen bir koşul dizisi olarak HTML'ye dönüştürülür.

### length {#length}
```
public static int length
```


### fromName(String htmlOfficeMathOutputModeName) {#fromName-java.lang.String}
```
public static int fromName(String htmlOfficeMathOutputModeName)
```




**Parameters:**
| Parametre | Tür | Açıklama |
| --- | --- | --- |
| htmlOfficeMathOutputModeName | java.lang.String |  |

**Returns:**
int
### getName(int htmlOfficeMathOutputMode) {#getName-int}
```
public static String getName(int htmlOfficeMathOutputMode)
```




**Parameters:**
| Parametre | Tür | Açıklama |
| --- | --- | --- |
| htmlOfficeMathOutputMode | int |  |

**Returns:**
java.lang.String
### getValues() {#getValues}
```
public static int[] getValues()
```




**Returns:**
int[]
### toString(int htmlOfficeMathOutputMode) {#toString-int}
```
public static String toString(int htmlOfficeMathOutputMode)
```




**Parameters:**
| Parametre | Tür | Açıklama |
| --- | --- | --- |
| htmlOfficeMathOutputMode | int |  |

**Returns:**
java.lang.String
