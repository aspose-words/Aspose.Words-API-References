---
title: "HtmlOfficeMathOutputMode"
linktitle: "HtmlOfficeMathOutputMode"
second_title: "Aspose.Words لـ Java"
description: "يحدد كيفية تصدير Aspose.Words لـ OfficeMath إلى HTML وMHTML وEPUB في Java."
type: docs
weight: 384
url: /ar/java/com.aspose.words/htmlofficemathoutputmode/
---

**Inheritance:**
java.lang.Object
```
public class HtmlOfficeMathOutputMode
```

يحدد كيفية تصدير Aspose.Words لـ OfficeMath إلى HTML وMHTML وEPUB.

 **Examples:** 

يوضح كيفية تحديد طريقة تصدير كائنات Microsoft OfficeMath إلى HTML.

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
## الحقول

| حقل | الوصف |
| --- | --- |
|  | [IMAGE](#IMAGE) | يتم تحويل OfficeMath إلى HTML كصورة محددة بواسطة الوسم ![Image 1][]. |


[Image 1]:  |
| [MATH_ML](#MATH-ML) | يتم تحويل OfficeMath إلى HTML باستخدام MathML. |
| [TEXT](#TEXT) | يتم تحويل OfficeMath إلى HTML كسلسلة من القطاعات المحددة بواسطة وسوم . |
| [length](#length) |  |
## الطرق

| طريقة | الوصف |
| --- | --- |
| [fromName(String htmlOfficeMathOutputModeName)](#fromName-java.lang.String) |  |
| [getName(int htmlOfficeMathOutputMode)](#getName-int) |  |
| [getValues()](#getValues) |  |
| [toString(int htmlOfficeMathOutputMode)](#toString-int) |  |
### IMAGE {#IMAGE}
```
public static int IMAGE
```


يتم تحويل OfficeMath إلى HTML كصورة محددة بواسطة الوسم ![Image 1][].


[Image 1]: 

### MATH_ML {#MATH-ML}
```
public static int MATH_ML
```


يتم تحويل OfficeMath إلى HTML باستخدام MathML.

### TEXT {#TEXT}
```
public static int TEXT
```


يتم تحويل OfficeMath إلى HTML كسلسلة من القطاعات المحددة بواسطة وسوم .

### length {#length}
```
public static int length
```


### fromName(String htmlOfficeMathOutputModeName) {#fromName-java.lang.String}
```
public static int fromName(String htmlOfficeMathOutputModeName)
```




**Parameters:**
| معامل | نوع | الوصف |
| --- | --- | --- |
| htmlOfficeMathOutputModeName | java.lang.String |  |

**Returns:**
int
### getName(int htmlOfficeMathOutputMode) {#getName-int}
```
public static String getName(int htmlOfficeMathOutputMode)
```




**Parameters:**
| معامل | نوع | الوصف |
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
| معامل | نوع | الوصف |
| --- | --- | --- |
| htmlOfficeMathOutputMode | int |  |

**Returns:**
java.lang.String
