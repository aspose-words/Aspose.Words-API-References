---
title: PdfPageLayout
linktitle: PdfPageLayout
second_title: Aspose.Words for Java
description: Specifies the page layout to be used when the document is opened in a PDF reader in Java.
type: docs
weight: 529
url: /java/com.aspose.words/pdfpagelayout/
---

**Inheritance:**
java.lang.Object
```
public class PdfPageLayout
```

Specifies the page layout to be used when the document is opened in a PDF reader.

 **Examples:** 

Shows how to display pages when opened in a PDF reader.

```

 Document doc = new Document(getMyDir() + "Big document.docx");

 // Display the pages two at a time, with odd-numbered pages on the left.
 PdfSaveOptions saveOptions = new PdfSaveOptions();
 saveOptions.setPageLayout(PdfPageLayout.TWO_PAGE_LEFT);

 doc.save(getArtifactsDir() + "PdfSaveOptions.PageLayout.pdf", saveOptions);
 
```
## Fields

| Field | Description |
| --- | --- |
| [ONE_COLUMN](#ONE-COLUMN) | Display the pages in one column. |
| [SINGLE_PAGE](#SINGLE-PAGE) | Display one page at a time. |
| [TWO_COLUMN_LEFT](#TWO-COLUMN-LEFT) | Display the pages in two columns, with odd-numbered pages on the left. |
| [TWO_COLUMN_RIGHT](#TWO-COLUMN-RIGHT) | Display the pages in two columns, with odd-numbered pages on the right. |
| [TWO_PAGE_LEFT](#TWO-PAGE-LEFT) | Display the pages two at a time, with odd-numbered pages on the left. |
| [TWO_PAGE_RIGHT](#TWO-PAGE-RIGHT) | Display the pages two at a time, with odd-numbered pages on the right. |
| [length](#length) |  |
## Methods

| Method | Description |
| --- | --- |
| [fromName(String pdfPageLayoutName)](#fromName-java.lang.String) |  |
| [getName(int pdfPageLayout)](#getName-int) |  |
| [getValues()](#getValues) |  |
| [toString(int pdfPageLayout)](#toString-int) |  |
### ONE_COLUMN {#ONE-COLUMN}
```
public static int ONE_COLUMN
```


Display the pages in one column.

### SINGLE_PAGE {#SINGLE-PAGE}
```
public static int SINGLE_PAGE
```


Display one page at a time.

### TWO_COLUMN_LEFT {#TWO-COLUMN-LEFT}
```
public static int TWO_COLUMN_LEFT
```


Display the pages in two columns, with odd-numbered pages on the left.

### TWO_COLUMN_RIGHT {#TWO-COLUMN-RIGHT}
```
public static int TWO_COLUMN_RIGHT
```


Display the pages in two columns, with odd-numbered pages on the right.

### TWO_PAGE_LEFT {#TWO-PAGE-LEFT}
```
public static int TWO_PAGE_LEFT
```


Display the pages two at a time, with odd-numbered pages on the left.

### TWO_PAGE_RIGHT {#TWO-PAGE-RIGHT}
```
public static int TWO_PAGE_RIGHT
```


Display the pages two at a time, with odd-numbered pages on the right.

### length {#length}
```
public static int length
```


### fromName(String pdfPageLayoutName) {#fromName-java.lang.String}
```
public static int fromName(String pdfPageLayoutName)
```




**Parameters:**
| Parameter | Type | Description |
| --- | --- | --- |
| pdfPageLayoutName | java.lang.String |  |

**Returns:**
int
### getName(int pdfPageLayout) {#getName-int}
```
public static String getName(int pdfPageLayout)
```




**Parameters:**
| Parameter | Type | Description |
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
| Parameter | Type | Description |
| --- | --- | --- |
| pdfPageLayout | int |  |

**Returns:**
java.lang.String
