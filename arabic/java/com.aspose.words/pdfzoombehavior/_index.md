---
title: "PdfZoomBehavior"
linktitle: "PdfZoomBehavior"
second_title: "Aspose.Words لـ Java"
description: "يحدد نوع التكبير المطبق على مستند PDF عند فتحه في عارض PDF في Java."
type: docs
weight: 544
url: /ar/java/com.aspose.words/pdfzoombehavior/
---

**Inheritance:**
java.lang.Object
```
public class PdfZoomBehavior
```

يحدد نوع التكبير المطبق على مستند PDF عندما يتم فتحه في عارض PDF.

 **Examples:** 

يعرض كيفية تعيين التكبير الافتراضي الذي يطبقه القارئ عند فتح مستند PDF مُصوَّر.

```

 Document doc = new Document();
 DocumentBuilder builder = new DocumentBuilder(doc);
 builder.writeln("Hello world!");

 // Create a "PdfSaveOptions" object that we can pass to the document's "Save" method
 // to modify how that method converts the document to .PDF.
 // Set the "ZoomBehavior" property to "PdfZoomBehavior.ZoomFactor" to get a PDF reader to
 // apply a percentage-based zoom factor when we open the document with it.
 // Set the "ZoomFactor" property to "25" to give the zoom factor a value of 25%.
 PdfSaveOptions options = new PdfSaveOptions();
 {
     options.setZoomBehavior(PdfZoomBehavior.ZOOM_FACTOR);
     options.setZoomFactor(25);
 }

 // When we open this document using a reader such as Adobe Acrobat, we will see the document scaled at 1/4 of its actual size.
 doc.save(getArtifactsDir() + "PdfSaveOptions.ZoomBehaviour.pdf", options);
 
```
## الحقول

| حقل | الوصف |
| --- | --- |
| [FIT_BOX](#FIT-BOX) | يتناسب مع الصندوق المحيط (المستطيل الذي يحتوي على جميع العناصر المرئية في الصفحة). |
| [FIT_HEIGHT](#FIT-HEIGHT) | يتناسب مع ارتفاع الصفحة. |
| [FIT_PAGE](#FIT-PAGE) | يعرض الصفحة بحيث تكون مرئية بالكامل. |
| [FIT_WIDTH](#FIT-WIDTH) | يتناسب مع عرض الصفحة. |
| [NONE](#NONE) | كيفية عرض المستند تُترك لعارض PDF. |
| [ZOOM_FACTOR](#ZOOM-FACTOR) | يعرض الصفحة باستخدام عامل التكبير المحدد. |
| [length](#length) |  |
## الطرق

| طريقة | الوصف |
| --- | --- |
| [fromName(String pdfZoomBehaviorName)](#fromName-java.lang.String) |  |
| [getName(int pdfZoomBehavior)](#getName-int) |  |
| [getValues()](#getValues) |  |
| [toString(int pdfZoomBehavior)](#toString-int) |  |
### FIT_BOX {#FIT-BOX}
```
public static int FIT_BOX
```


يتناسب مع الصندوق المحيط (المستطيل الذي يحتوي على جميع العناصر المرئية في الصفحة).

### FIT_HEIGHT {#FIT-HEIGHT}
```
public static int FIT_HEIGHT
```


يتناسب مع ارتفاع الصفحة.

### FIT_PAGE {#FIT-PAGE}
```
public static int FIT_PAGE
```


يعرض الصفحة بحيث تكون مرئية بالكامل.

### FIT_WIDTH {#FIT-WIDTH}
```
public static int FIT_WIDTH
```


يتناسب مع عرض الصفحة.

### NONE {#NONE}
```
public static int NONE
```


كيفية عرض المستند تُترك لعارض PDF. عادةً ما يعرض العارض المستند ليتناسب مع عرض الصفحة.

### ZOOM_FACTOR {#ZOOM-FACTOR}
```
public static int ZOOM_FACTOR
```


يعرض الصفحة باستخدام عامل التكبير المحدد.

### length {#length}
```
public static int length
```


### fromName(String pdfZoomBehaviorName) {#fromName-java.lang.String}
```
public static int fromName(String pdfZoomBehaviorName)
```




**Parameters:**
| معامل | نوع | الوصف |
| --- | --- | --- |
| pdfZoomBehaviorName | java.lang.String |  |

**Returns:**
int
### getName(int pdfZoomBehavior) {#getName-int}
```
public static String getName(int pdfZoomBehavior)
```




**Parameters:**
| معامل | نوع | الوصف |
| --- | --- | --- |
| pdfZoomBehavior | int |  |

**Returns:**
java.lang.String
### getValues() {#getValues}
```
public static int[] getValues()
```




**Returns:**
int[]
### toString(int pdfZoomBehavior) {#toString-int}
```
public static String toString(int pdfZoomBehavior)
```




**Parameters:**
| معامل | نوع | الوصف |
| --- | --- | --- |
| pdfZoomBehavior | int |  |

**Returns:**
java.lang.String
