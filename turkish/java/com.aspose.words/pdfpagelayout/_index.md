---
title: "PdfPageLayout"
linktitle: "PdfPageLayout"
second_title: "Aspose.Words Java için"
description: "Java'da bir PDF okuyucusunda belge açıldığında kullanılacak sayfa düzenini belirtir."
type: docs
weight: 539
url: /tr/java/com.aspose.words/pdfpagelayout/
---

**Inheritance:**
java.lang.Object
```
public class PdfPageLayout
```

Belge bir PDF okuyucusunda açıldığında kullanılacak sayfa düzenini belirtir.

 **Examples:** 

PDF okuyucusunda açıldığında sayfaların nasıl görüntüleneceğini gösterir.

```

 Document doc = new Document(getMyDir() + "Big document.docx");

 // Display the pages two at a time, with odd-numbered pages on the left.
 PdfSaveOptions saveOptions = new PdfSaveOptions();
 saveOptions.setPageLayout(PdfPageLayout.TWO_PAGE_LEFT);

 doc.save(getArtifactsDir() + "PdfSaveOptions.PageLayout.pdf", saveOptions);
 
```
## Alanlar

| Alan | Açıklama |
| --- | --- |
| [ONE_COLUMN](#ONE-COLUMN) | Sayfaları tek sütunda görüntüle. |
| [SINGLE_PAGE](#SINGLE-PAGE) | Bir seferde bir sayfa görüntüle. |
| [TWO_COLUMN_LEFT](#TWO-COLUMN-LEFT) | Sayfaları iki sütunda görüntüle, tek sayılı sayfalar solda. |
| [TWO_COLUMN_RIGHT](#TWO-COLUMN-RIGHT) | Sayfaları iki sütunda görüntüle, tek sayılı sayfalar sağda. |
| [TWO_PAGE_LEFT](#TWO-PAGE-LEFT) | Sayfaları iki seferde bir görüntüle, tek sayılı sayfalar solda. |
| [TWO_PAGE_RIGHT](#TWO-PAGE-RIGHT) | Sayfaları iki seferde bir görüntüle, tek sayılı sayfalar sağda. |
| [length](#length) |  |
## Yöntemler

| Yöntem | Açıklama |
| --- | --- |
| [fromName(String pdfPageLayoutName)](#fromName-java.lang.String) |  |
| [getName(int pdfPageLayout)](#getName-int) |  |
| [getValues()](#getValues) |  |
| [toString(int pdfPageLayout)](#toString-int) |  |
### ONE_COLUMN {#ONE-COLUMN}
```
public static int ONE_COLUMN
```


Sayfaları tek sütunda görüntüle.

### SINGLE_PAGE {#SINGLE-PAGE}
```
public static int SINGLE_PAGE
```


Bir seferde bir sayfa görüntüle.

### TWO_COLUMN_LEFT {#TWO-COLUMN-LEFT}
```
public static int TWO_COLUMN_LEFT
```


Sayfaları iki sütunda görüntüle, tek sayılı sayfalar solda.

### TWO_COLUMN_RIGHT {#TWO-COLUMN-RIGHT}
```
public static int TWO_COLUMN_RIGHT
```


Sayfaları iki sütunda görüntüle, tek sayılı sayfalar sağda.

### TWO_PAGE_LEFT {#TWO-PAGE-LEFT}
```
public static int TWO_PAGE_LEFT
```


Sayfaları iki seferde bir görüntüle, tek sayılı sayfalar solda.

### TWO_PAGE_RIGHT {#TWO-PAGE-RIGHT}
```
public static int TWO_PAGE_RIGHT
```


Sayfaları iki seferde bir görüntüle, tek sayılı sayfalar sağda.

### length {#length}
```
public static int length
```


### fromName(String pdfPageLayoutName) {#fromName-java.lang.String}
```
public static int fromName(String pdfPageLayoutName)
```




**Parameters:**
| Parametre | Tür | Açıklama |
| --- | --- | --- |
| pdfPageLayoutName | java.lang.String |  |

**Returns:**
int
### getName(int pdfPageLayout) {#getName-int}
```
public static String getName(int pdfPageLayout)
```




**Parameters:**
| Parametre | Tür | Açıklama |
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
| Parametre | Tür | Açıklama |
| --- | --- | --- |
| pdfPageLayout | int |  |

**Returns:**
java.lang.String
