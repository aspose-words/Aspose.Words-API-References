---
title: "PdfPageLayout"
linktitle: "PdfPageLayout"
second_title: "Aspose.Words per Java"
description: "Specifica il layout della pagina da utilizzare quando il documento viene aperto in un lettore PDF in Java."
type: docs
weight: 539
url: /it/java/com.aspose.words/pdfpagelayout/
---

**Inheritance:**
java.lang.Object
```
public class PdfPageLayout
```

Specifica il layout di pagina da utilizzare quando il documento è aperto in un lettore PDF.

 **Examples:** 

Mostra come visualizzare le pagine quando vengono aperte in un lettore PDF.

```

 Document doc = new Document(getMyDir() + "Big document.docx");

 // Display the pages two at a time, with odd-numbered pages on the left.
 PdfSaveOptions saveOptions = new PdfSaveOptions();
 saveOptions.setPageLayout(PdfPageLayout.TWO_PAGE_LEFT);

 doc.save(getArtifactsDir() + "PdfSaveOptions.PageLayout.pdf", saveOptions);
 
```
## Campi

| Campo | Descrizione |
| --- | --- |
| [ONE_COLUMN](#ONE-COLUMN) | Visualizza le pagine in una colonna. |
| [SINGLE_PAGE](#SINGLE-PAGE) | Visualizza una pagina alla volta. |
| [TWO_COLUMN_LEFT](#TWO-COLUMN-LEFT) | Visualizza le pagine in due colonne, con le pagine dispari a sinistra. |
| [TWO_COLUMN_RIGHT](#TWO-COLUMN-RIGHT) | Visualizza le pagine in due colonne, con le pagine dispari a destra. |
| [TWO_PAGE_LEFT](#TWO-PAGE-LEFT) | Visualizza le pagine due alla volta, con le pagine dispari a sinistra. |
| [TWO_PAGE_RIGHT](#TWO-PAGE-RIGHT) | Visualizza le pagine due alla volta, con le pagine dispari a destra. |
| [length](#length) |  |
## Metodi

| Metodo | Descrizione |
| --- | --- |
| [fromName(String pdfPageLayoutName)](#fromName-java.lang.String) |  |
| [getName(int pdfPageLayout)](#getName-int) |  |
| [getValues()](#getValues) |  |
| [toString(int pdfPageLayout)](#toString-int) |  |
### ONE_COLUMN {#ONE-COLUMN}
```
public static int ONE_COLUMN
```


Visualizza le pagine in una colonna.

### SINGLE_PAGE {#SINGLE-PAGE}
```
public static int SINGLE_PAGE
```


Visualizza una pagina alla volta.

### TWO_COLUMN_LEFT {#TWO-COLUMN-LEFT}
```
public static int TWO_COLUMN_LEFT
```


Visualizza le pagine in due colonne, con le pagine dispari a sinistra.

### TWO_COLUMN_RIGHT {#TWO-COLUMN-RIGHT}
```
public static int TWO_COLUMN_RIGHT
```


Visualizza le pagine in due colonne, con le pagine dispari a destra.

### TWO_PAGE_LEFT {#TWO-PAGE-LEFT}
```
public static int TWO_PAGE_LEFT
```


Visualizza le pagine due alla volta, con le pagine dispari a sinistra.

### TWO_PAGE_RIGHT {#TWO-PAGE-RIGHT}
```
public static int TWO_PAGE_RIGHT
```


Visualizza le pagine due alla volta, con le pagine dispari a destra.

### length {#length}
```
public static int length
```


### fromName(String pdfPageLayoutName) {#fromName-java.lang.String}
```
public static int fromName(String pdfPageLayoutName)
```




**Parameters:**
| Parametro | Tipo | Descrizione |
| --- | --- | --- |
| pdfPageLayoutName | java.lang.String |  |

**Returns:**
int
### getName(int pdfPageLayout) {#getName-int}
```
public static String getName(int pdfPageLayout)
```




**Parameters:**
| Parametro | Tipo | Descrizione |
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
| Parametro | Tipo | Descrizione |
| --- | --- | --- |
| pdfPageLayout | int |  |

**Returns:**
java.lang.String
