---
title: "PdfPageLayout"
linktitle: "PdfPageLayout"
second_title: "Aspose.Words für Java"
description: "Gibt das Seitenlayout an, das verwendet werden soll, wenn das Dokument in einem PDF‑Reader in Java geöffnet wird."
type: docs
weight: 539
url: /de/java/com.aspose.words/pdfpagelayout/
---

**Inheritance:**
java.lang.Object
```
public class PdfPageLayout
```

Gibt das Seitenlayout an, das verwendet werden soll, wenn das Dokument in einem PDF‑Reader geöffnet wird.

 **Examples:** 

Zeigt, wie Seiten angezeigt werden, wenn sie in einem PDF‑Reader geöffnet werden.

```

 Document doc = new Document(getMyDir() + "Big document.docx");

 // Display the pages two at a time, with odd-numbered pages on the left.
 PdfSaveOptions saveOptions = new PdfSaveOptions();
 saveOptions.setPageLayout(PdfPageLayout.TWO_PAGE_LEFT);

 doc.save(getArtifactsDir() + "PdfSaveOptions.PageLayout.pdf", saveOptions);
 
```
## Felder

| Feld | Beschreibung |
| --- | --- |
| [ONE_COLUMN](#ONE-COLUMN) | Zeigt die Seiten in einer Spalte an. |
| [SINGLE_PAGE](#SINGLE-PAGE) | Zeigt jeweils eine Seite an. |
| [TWO_COLUMN_LEFT](#TWO-COLUMN-LEFT) | Zeigt die Seiten in zwei Spalten an, wobei ungerade Seiten links angezeigt werden. |
| [TWO_COLUMN_RIGHT](#TWO-COLUMN-RIGHT) | Zeigt die Seiten in zwei Spalten an, wobei ungerade Seiten rechts angezeigt werden. |
| [TWO_PAGE_LEFT](#TWO-PAGE-LEFT) | Zeigt jeweils zwei Seiten an, wobei ungerade Seiten links angezeigt werden. |
| [TWO_PAGE_RIGHT](#TWO-PAGE-RIGHT) | Zeigt jeweils zwei Seiten an, wobei ungerade Seiten rechts angezeigt werden. |
| [length](#length) |  |
## Methoden

| Methode | Beschreibung |
| --- | --- |
| [fromName(String pdfPageLayoutName)](#fromName-java.lang.String) |  |
| [getName(int pdfPageLayout)](#getName-int) |  |
| [getValues()](#getValues) |  |
| [toString(int pdfPageLayout)](#toString-int) |  |
### ONE_COLUMN {#ONE-COLUMN}
```
public static int ONE_COLUMN
```


Zeigt die Seiten in einer Spalte an.

### SINGLE_PAGE {#SINGLE-PAGE}
```
public static int SINGLE_PAGE
```


Zeigt jeweils eine Seite an.

### TWO_COLUMN_LEFT {#TWO-COLUMN-LEFT}
```
public static int TWO_COLUMN_LEFT
```


Zeigt die Seiten in zwei Spalten an, wobei ungerade Seiten links angezeigt werden.

### TWO_COLUMN_RIGHT {#TWO-COLUMN-RIGHT}
```
public static int TWO_COLUMN_RIGHT
```


Zeigt die Seiten in zwei Spalten an, wobei ungerade Seiten rechts angezeigt werden.

### TWO_PAGE_LEFT {#TWO-PAGE-LEFT}
```
public static int TWO_PAGE_LEFT
```


Zeigt jeweils zwei Seiten an, wobei ungerade Seiten links angezeigt werden.

### TWO_PAGE_RIGHT {#TWO-PAGE-RIGHT}
```
public static int TWO_PAGE_RIGHT
```


Zeigt jeweils zwei Seiten an, wobei ungerade Seiten rechts angezeigt werden.

### length {#length}
```
public static int length
```


### fromName(String pdfPageLayoutName) {#fromName-java.lang.String}
```
public static int fromName(String pdfPageLayoutName)
```




**Parameters:**
| Parameter | Typ | Beschreibung |
| --- | --- | --- |
| pdfPageLayoutName | java.lang.String |  |

**Returns:**
int
### getName(int pdfPageLayout) {#getName-int}
```
public static String getName(int pdfPageLayout)
```




**Parameters:**
| Parameter | Typ | Beschreibung |
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
| Parameter | Typ | Beschreibung |
| --- | --- | --- |
| pdfPageLayout | int |  |

**Returns:**
java.lang.String
