---
title: "PdfPageLayout"
linktitle: "PdfPageLayout"
second_title: "Aspose.Words para Java"
description: "Especifica el diseño de página que se usará cuando el documento se abra en un lector PDF en Java."
type: docs
weight: 539
url: /es/java/com.aspose.words/pdfpagelayout/
---

**Inheritance:**
java.lang.Object
```
public class PdfPageLayout
```

Especifica el diseño de página que se usará cuando el documento se abra en un lector PDF.

 **Examples:** 

Muestra cómo visualizar las páginas cuando se abre en un lector PDF.

```

 Document doc = new Document(getMyDir() + "Big document.docx");

 // Display the pages two at a time, with odd-numbered pages on the left.
 PdfSaveOptions saveOptions = new PdfSaveOptions();
 saveOptions.setPageLayout(PdfPageLayout.TWO_PAGE_LEFT);

 doc.save(getArtifactsDir() + "PdfSaveOptions.PageLayout.pdf", saveOptions);
 
```
## Campos

| Campo | Descripción |
| --- | --- |
| [ONE_COLUMN](#ONE-COLUMN) | Muestra las páginas en una columna. |
| [SINGLE_PAGE](#SINGLE-PAGE) | Muestra una página a la vez. |
| [TWO_COLUMN_LEFT](#TWO-COLUMN-LEFT) | Muestra las páginas en dos columnas, con las páginas impares a la izquierda. |
| [TWO_COLUMN_RIGHT](#TWO-COLUMN-RIGHT) | Muestra las páginas en dos columnas, con las páginas impares a la derecha. |
| [TWO_PAGE_LEFT](#TWO-PAGE-LEFT) | Muestra dos páginas a la vez, con las páginas impares a la izquierda. |
| [TWO_PAGE_RIGHT](#TWO-PAGE-RIGHT) | Muestra dos páginas a la vez, con las páginas impares a la derecha. |
| [length](#length) |  |
## Métodos

| Método | Descripción |
| --- | --- |
| [fromName(String pdfPageLayoutName)](#fromName-java.lang.String) |  |
| [getName(int pdfPageLayout)](#getName-int) |  |
| [getValues()](#getValues) |  |
| [toString(int pdfPageLayout)](#toString-int) |  |
### ONE_COLUMN {#ONE-COLUMN}
```
public static int ONE_COLUMN
```


Muestra las páginas en una columna.

### SINGLE_PAGE {#SINGLE-PAGE}
```
public static int SINGLE_PAGE
```


Muestra una página a la vez.

### TWO_COLUMN_LEFT {#TWO-COLUMN-LEFT}
```
public static int TWO_COLUMN_LEFT
```


Muestra las páginas en dos columnas, con las páginas impares a la izquierda.

### TWO_COLUMN_RIGHT {#TWO-COLUMN-RIGHT}
```
public static int TWO_COLUMN_RIGHT
```


Muestra las páginas en dos columnas, con las páginas impares a la derecha.

### TWO_PAGE_LEFT {#TWO-PAGE-LEFT}
```
public static int TWO_PAGE_LEFT
```


Muestra dos páginas a la vez, con las páginas impares a la izquierda.

### TWO_PAGE_RIGHT {#TWO-PAGE-RIGHT}
```
public static int TWO_PAGE_RIGHT
```


Muestra dos páginas a la vez, con las páginas impares a la derecha.

### length {#length}
```
public static int length
```


### fromName(String pdfPageLayoutName) {#fromName-java.lang.String}
```
public static int fromName(String pdfPageLayoutName)
```




**Parameters:**
| Parámetro | Tipo | Descripción |
| --- | --- | --- |
| pdfPageLayoutName | java.lang.String |  |

**Returns:**
int
### getName(int pdfPageLayout) {#getName-int}
```
public static String getName(int pdfPageLayout)
```




**Parameters:**
| Parámetro | Tipo | Descripción |
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
| Parámetro | Tipo | Descripción |
| --- | --- | --- |
| pdfPageLayout | int |  |

**Returns:**
java.lang.String
