---
title: "PdfZoomBehavior"
linktitle: "PdfZoomBehavior"
second_title: "Aspose.Words для Java"
description: "Указывает тип масштабирования, применяемый к PDF‑документу при его открытии в PDF‑просмотрщике на Java."
type: docs
weight: 544
url: /ru/java/com.aspose.words/pdfzoombehavior/
---

**Inheritance:**
java.lang.Object
```
public class PdfZoomBehavior
```

Указывает тип масштабирования, применяемого к PDF‑документу при его открытии в PDF‑просмотрщике.

 **Examples:** 

Показывает, как установить масштаб по умолчанию, который применяется читателем при открытии отрисованного PDF‑документа.

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
## Поля

| Поле | Описание |
| --- | --- |
| [FIT_BOX](#FIT-BOX) | Подгоняет ограничивающий прямоугольник (прямоугольник, содержащий все видимые элементы на странице). |
| [FIT_HEIGHT](#FIT-HEIGHT) | Подгоняет высоту страницы. |
| [FIT_PAGE](#FIT-PAGE) | Отображает страницу так, чтобы она была полностью видна. |
| [FIT_WIDTH](#FIT-WIDTH) | Подгоняет ширину страницы. |
| [NONE](#NONE) | Отображение документа оставлено на усмотрение PDF‑просмотрщика. |
| [ZOOM_FACTOR](#ZOOM-FACTOR) | Отображает страницу, используя указанный коэффициент масштабирования. |
| [length](#length) |  |
## Методы

| Метод | Описание |
| --- | --- |
| [fromName(String pdfZoomBehaviorName)](#fromName-java.lang.String) |  |
| [getName(int pdfZoomBehavior)](#getName-int) |  |
| [getValues()](#getValues) |  |
| [toString(int pdfZoomBehavior)](#toString-int) |  |
### FIT_BOX {#FIT-BOX}
```
public static int FIT_BOX
```


Подгоняет ограничивающий прямоугольник (прямоугольник, содержащий все видимые элементы на странице).

### FIT_HEIGHT {#FIT-HEIGHT}
```
public static int FIT_HEIGHT
```


Подгоняет высоту страницы.

### FIT_PAGE {#FIT-PAGE}
```
public static int FIT_PAGE
```


Отображает страницу так, чтобы она была полностью видна.

### FIT_WIDTH {#FIT-WIDTH}
```
public static int FIT_WIDTH
```


Подгоняет ширину страницы.

### NONE {#NONE}
```
public static int NONE
```


Отображение документа оставлено на усмотрение PDF‑просмотрщика. Обычно просмотрщик отображает документ, подгоняя его под ширину страницы.

### ZOOM_FACTOR {#ZOOM-FACTOR}
```
public static int ZOOM_FACTOR
```


Отображает страницу, используя указанный коэффициент масштабирования.

### length {#length}
```
public static int length
```


### fromName(String pdfZoomBehaviorName) {#fromName-java.lang.String}
```
public static int fromName(String pdfZoomBehaviorName)
```




**Parameters:**
| Параметр | Тип | Описание |
| --- | --- | --- |
| pdfZoomBehaviorName | java.lang.String |  |

**Returns:**
int
### getName(int pdfZoomBehavior) {#getName-int}
```
public static String getName(int pdfZoomBehavior)
```




**Parameters:**
| Параметр | Тип | Описание |
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
| Параметр | Тип | Описание |
| --- | --- | --- |
| pdfZoomBehavior | int |  |

**Returns:**
java.lang.String
