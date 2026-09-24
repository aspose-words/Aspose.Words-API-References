---
title: "Márgenes"
linktitle: "Márgenes"
second_title: "Aspose.Words para Java"
description: "Especifica márgenes predefinidos en Java."
type: docs
weight: 449
url: /es/java/com.aspose.words/margins/
---

**Inheritance:**
java.lang.Object
```
public class Margins
```

Especifica los márgenes predefinidos.

 **Examples:** 

Muestra cuándo recalcular el diseño de página del documento.

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
## Campos

| Campo | Descripción |
| --- | --- |
| [CUSTOM](#CUSTOM) | Márgenes personalizados. |
| [MIRRORED](#MIRRORED) | Márgenes reflejados. |
| [MODERATE](#MODERATE) | Márgenes moderados. |
| [NARROW](#NARROW) | Márgenes estrechos. |
| [NORMAL](#NORMAL) | Márgenes normales. |
| [WIDE](#WIDE) | Márgenes anchos. |
| [length](#length) |  |
## Métodos

| Método | Descripción |
| --- | --- |
| [fromName(String marginsName)](#fromName-java.lang.String) |  |
| [getName(int margins)](#getName-int) |  |
| [getValues()](#getValues) |  |
| [toString(int margins)](#toString-int) |  |
### CUSTOM {#CUSTOM}
```
public static int CUSTOM
```


Márgenes personalizados.

### MIRRORED {#MIRRORED}
```
public static int MIRRORED
```


Márgenes reflejados.

 **Remarks:** 

Configurar los márgenes a Reflejados establecerá el valor apropiado para la propiedad [PageSetup.getMultiplePages()](../../com.aspose.words/pagesetup/\#getMultiplePages) / [PageSetup.setMultiplePages(int)](../../com.aspose.words/pagesetup/\#setMultiplePages-int). Esto afectará a todo el documento, no solo a la sección actual.

### MODERATE {#MODERATE}
```
public static int MODERATE
```


Márgenes moderados.

### NARROW {#NARROW}
```
public static int NARROW
```


Márgenes estrechos.

### NORMAL {#NORMAL}
```
public static int NORMAL
```


Márgenes normales.

### WIDE {#WIDE}
```
public static int WIDE
```


Márgenes anchos.

### length {#length}
```
public static int length
```


### fromName(String marginsName) {#fromName-java.lang.String}
```
public static int fromName(String marginsName)
```




**Parameters:**
| Parámetro | Tipo | Descripción |
| --- | --- | --- |
| marginsName | java.lang.String |  |

**Returns:**
int
### getName(int margins) {#getName-int}
```
public static String getName(int margins)
```




**Parameters:**
| Parámetro | Tipo | Descripción |
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
| Parámetro | Tipo | Descripción |
| --- | --- | --- |
| margins | int |  |

**Returns:**
java.lang.String
