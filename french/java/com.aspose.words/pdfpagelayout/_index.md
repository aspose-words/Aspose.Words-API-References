---
title: "PdfPageLayout"
linktitle: "PdfPageLayout"
second_title: "Aspose.Words pour Java"
description: "Spécifie la mise en page à utiliser lorsque le document est ouvert dans un lecteur PDF en Java."
type: docs
weight: 539
url: /fr/java/com.aspose.words/pdfpagelayout/
---

**Inheritance:**
java.lang.Object
```
public class PdfPageLayout
```

Spécifie la mise en page à utiliser lorsque le document est ouvert dans un lecteur PDF.

 **Examples:** 

Montre comment afficher les pages lorsqu'elles sont ouvertes dans un lecteur PDF.

```

 Document doc = new Document(getMyDir() + "Big document.docx");

 // Display the pages two at a time, with odd-numbered pages on the left.
 PdfSaveOptions saveOptions = new PdfSaveOptions();
 saveOptions.setPageLayout(PdfPageLayout.TWO_PAGE_LEFT);

 doc.save(getArtifactsDir() + "PdfSaveOptions.PageLayout.pdf", saveOptions);
 
```
## Champs

| Champ | Description |
| --- | --- |
| [ONE_COLUMN](#ONE-COLUMN) | Affiche les pages en une colonne. |
| [SINGLE_PAGE](#SINGLE-PAGE) | Affiche une page à la fois. |
| [TWO_COLUMN_LEFT](#TWO-COLUMN-LEFT) | Affiche les pages en deux colonnes, les pages impaires à gauche. |
| [TWO_COLUMN_RIGHT](#TWO-COLUMN-RIGHT) | Affiche les pages en deux colonnes, les pages impaires à droite. |
| [TWO_PAGE_LEFT](#TWO-PAGE-LEFT) | Affiche les pages deux à la fois, les pages impaires à gauche. |
| [TWO_PAGE_RIGHT](#TWO-PAGE-RIGHT) | Affiche les pages deux à la fois, les pages impaires à droite. |
| [length](#length) |  |
## Méthodes

| Méthode | Description |
| --- | --- |
| [fromName(String pdfPageLayoutName)](#fromName-java.lang.String) |  |
| [getName(int pdfPageLayout)](#getName-int) |  |
| [getValues()](#getValues) |  |
| [toString(int pdfPageLayout)](#toString-int) |  |
### ONE_COLUMN {#ONE-COLUMN}
```
public static int ONE_COLUMN
```


Affiche les pages en une colonne.

### SINGLE_PAGE {#SINGLE-PAGE}
```
public static int SINGLE_PAGE
```


Affiche une page à la fois.

### TWO_COLUMN_LEFT {#TWO-COLUMN-LEFT}
```
public static int TWO_COLUMN_LEFT
```


Affiche les pages en deux colonnes, les pages impaires à gauche.

### TWO_COLUMN_RIGHT {#TWO-COLUMN-RIGHT}
```
public static int TWO_COLUMN_RIGHT
```


Affiche les pages en deux colonnes, les pages impaires à droite.

### TWO_PAGE_LEFT {#TWO-PAGE-LEFT}
```
public static int TWO_PAGE_LEFT
```


Affiche les pages deux à la fois, les pages impaires à gauche.

### TWO_PAGE_RIGHT {#TWO-PAGE-RIGHT}
```
public static int TWO_PAGE_RIGHT
```


Affiche les pages deux à la fois, les pages impaires à droite.

### length {#length}
```
public static int length
```


### fromName(String pdfPageLayoutName) {#fromName-java.lang.String}
```
public static int fromName(String pdfPageLayoutName)
```




**Parameters:**
| Paramètre | Type | Description |
| --- | --- | --- |
| pdfPageLayoutName | java.lang.String |  |

**Returns:**
int
### getName(int pdfPageLayout) {#getName-int}
```
public static String getName(int pdfPageLayout)
```




**Parameters:**
| Paramètre | Type | Description |
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
| Paramètre | Type | Description |
| --- | --- | --- |
| pdfPageLayout | int |  |

**Returns:**
java.lang.String
