---
title: "PdfPageLayout"
linktitle: "PdfPageLayout"
second_title: "Aspose.Words для Java"
description: "Указывает макет страницы, который будет использоваться при открытии документа в PDF‑просмотрщике на Java."
type: docs
weight: 539
url: /ru/java/com.aspose.words/pdfpagelayout/
---

**Inheritance:**
java.lang.Object
```
public class PdfPageLayout
```

Указывает макет страницы, используемый при открытии документа в PDF‑просмотрщике.

 **Examples:** 

Показывает, как отображать страницы при открытии в PDF‑просмотрщике.

```

 Document doc = new Document(getMyDir() + "Big document.docx");

 // Display the pages two at a time, with odd-numbered pages on the left.
 PdfSaveOptions saveOptions = new PdfSaveOptions();
 saveOptions.setPageLayout(PdfPageLayout.TWO_PAGE_LEFT);

 doc.save(getArtifactsDir() + "PdfSaveOptions.PageLayout.pdf", saveOptions);
 
```
## Поля

| Поле | Описание |
| --- | --- |
| [ONE_COLUMN](#ONE-COLUMN) | Отображать страницы в одной колонке. |
| [SINGLE_PAGE](#SINGLE-PAGE) | Отображать одну страницу за раз. |
| [TWO_COLUMN_LEFT](#TWO-COLUMN-LEFT) | Отображать страницы в двух колонках, при этом нечётные страницы слева. |
| [TWO_COLUMN_RIGHT](#TWO-COLUMN-RIGHT) | Отображать страницы в двух колонках, при этом нечётные страницы справа. |
| [TWO_PAGE_LEFT](#TWO-PAGE-LEFT) | Отображать две страницы одновременно, при этом нечётные страницы слева. |
| [TWO_PAGE_RIGHT](#TWO-PAGE-RIGHT) | Отображать две страницы одновременно, при этом нечётные страницы справа. |
| [length](#length) |  |
## Методы

| Метод | Описание |
| --- | --- |
| [fromName(String pdfPageLayoutName)](#fromName-java.lang.String) |  |
| [getName(int pdfPageLayout)](#getName-int) |  |
| [getValues()](#getValues) |  |
| [toString(int pdfPageLayout)](#toString-int) |  |
### ONE_COLUMN {#ONE-COLUMN}
```
public static int ONE_COLUMN
```


Отображать страницы в одной колонке.

### SINGLE_PAGE {#SINGLE-PAGE}
```
public static int SINGLE_PAGE
```


Отображать одну страницу за раз.

### TWO_COLUMN_LEFT {#TWO-COLUMN-LEFT}
```
public static int TWO_COLUMN_LEFT
```


Отображать страницы в двух колонках, при этом нечётные страницы слева.

### TWO_COLUMN_RIGHT {#TWO-COLUMN-RIGHT}
```
public static int TWO_COLUMN_RIGHT
```


Отображать страницы в двух колонках, при этом нечётные страницы справа.

### TWO_PAGE_LEFT {#TWO-PAGE-LEFT}
```
public static int TWO_PAGE_LEFT
```


Отображать две страницы одновременно, при этом нечётные страницы слева.

### TWO_PAGE_RIGHT {#TWO-PAGE-RIGHT}
```
public static int TWO_PAGE_RIGHT
```


Отображать две страницы одновременно, при этом нечётные страницы справа.

### length {#length}
```
public static int length
```


### fromName(String pdfPageLayoutName) {#fromName-java.lang.String}
```
public static int fromName(String pdfPageLayoutName)
```




**Parameters:**
| Параметр | Тип | Описание |
| --- | --- | --- |
| pdfPageLayoutName | java.lang.String |  |

**Returns:**
int
### getName(int pdfPageLayout) {#getName-int}
```
public static String getName(int pdfPageLayout)
```




**Parameters:**
| Параметр | Тип | Описание |
| --- | --- | --- |
| pdfPageLayout | int |  |

**Returns:**
java.lang.String
### getValues() {#getValues}
```
public static int[] getValues()
```




**Returns:**
int[]
### toString(int pdfPageLayout) {#toString-int}
```
public static String toString(int pdfPageLayout)
```




**Parameters:**
| Параметр | Тип | Описание |
| --- | --- | --- |
| pdfPageLayout | int |  |

**Returns:**
java.lang.String
