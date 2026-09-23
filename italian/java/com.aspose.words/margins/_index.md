---
title: "Margini"
linktitle: "Margini"
second_title: "Aspose.Words per Java"
description: "Specifica i margini predefiniti in Java."
type: docs
weight: 449
url: /it/java/com.aspose.words/margins/
---

**Inheritance:**
java.lang.Object
```
public class Margins
```

Specifica i margini predefiniti.

 **Examples:** 

Mostra quando ricalcolare il layout della pagina del documento.

```

 Document doc = new Document(getMyDir() + "Rendering.docx");

 // Saving a document to PDF, to an image, or printing for the first time will automatically
 // cache the layout of the document within its pages.
 doc.save(getArtifactsDir() + "Document.UpdatePageLayout.1.pdf");

 // Modify the document in some way.
 doc.getStyles().get("Normal").getFont().setSize(6.0);
 doc.getSections().get(0).getPageSetup().setOrientation(Orientation.LANDSCAPE);
 doc.getSections().get(0).getPageSetup().setMargins(Margins.MIRRORED);

 // In the current version of Aspose.Words, modifying the document does not automatically rebuild
 // the cached page layout. If we wish for the cached layout
 // to stay up to date, we will need to update it manually.
 doc.updatePageLayout();

 doc.save(getArtifactsDir() + "Document.UpdatePageLayout.2.pdf");
 
```
## Campi

| Campo | Descrizione |
| --- | --- |
| [CUSTOM](#CUSTOM) | Margini personalizzati. |
| [MIRRORED](#MIRRORED) | Margini speculari. |
| [MODERATE](#MODERATE) | Margini moderati. |
| [NARROW](#NARROW) | Margini stretti. |
| [NORMAL](#NORMAL) | Margini normali. |
| [WIDE](#WIDE) | Margini ampi. |
| [length](#length) |  |
## Metodi

| Metodo | Descrizione |
| --- | --- |
| [fromName(String marginsName)](#fromName-java.lang.String) |  |
| [getName(int margins)](#getName-int) |  |
| [getValues()](#getValues) |  |
| [toString(int margins)](#toString-int) |  |
### CUSTOM {#CUSTOM}
```
public static int CUSTOM
```


Margini personalizzati.

### MIRRORED {#MIRRORED}
```
public static int MIRRORED
```


Margini speculari.

 **Remarks:** 

Impostare i margini su Mirrored imposterà il valore appropriato per la proprietà [PageSetup.getMultiplePages()](../../com.aspose.words/pagesetup/\#getMultiplePages) / [PageSetup.setMultiplePages(int)](../../com.aspose.words/pagesetup/\#setMultiplePages-int). Questo influenzerà l'intero documento, non solo la sezione corrente.

### MODERATE {#MODERATE}
```
public static int MODERATE
```


Margini moderati.

### NARROW {#NARROW}
```
public static int NARROW
```


Margini stretti.

### NORMAL {#NORMAL}
```
public static int NORMAL
```


Margini normali.

### WIDE {#WIDE}
```
public static int WIDE
```


Margini ampi.

### length {#length}
```
public static int length
```


### fromName(String marginsName) {#fromName-java.lang.String}
```
public static int fromName(String marginsName)
```




**Parameters:**
| Parametro | Tipo | Descrizione |
| --- | --- | --- |
| marginsName | java.lang.String |  |

**Returns:**
int
### getName(int margins) {#getName-int}
```
public static String getName(int margins)
```




**Parameters:**
| Parametro | Tipo | Descrizione |
| --- | --- | --- |
| margins | int |  |

**Returns:**
java.lang.String
### getValues() {#getValues}
```
public static int[] getValues()
```




**Returns:**
int[]
### toString(int margins) {#toString-int}
```
public static String toString(int margins)
```




**Parameters:**
| Parametro | Tipo | Descrizione |
| --- | --- | --- |
| margins | int |  |

**Returns:**
java.lang.String
