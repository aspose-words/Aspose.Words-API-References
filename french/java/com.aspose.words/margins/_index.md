---
title: "Marges"
linktitle: "Marges"
second_title: "Aspose.Words pour Java"
description: "Spécifie les marges prédéfinies en Java."
type: docs
weight: 449
url: /fr/java/com.aspose.words/margins/
---

**Inheritance:**
java.lang.Object
```
public class Margins
```

Spécifie les marges prédéfinies.

 **Examples:** 

Montre quand recalculer la mise en page du document.

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
## Champs

| Champ | Description |
| --- | --- |
| [CUSTOM](#CUSTOM) | Marges personnalisées. |
| [MIRRORED](#MIRRORED) | Marges miroir. |
| [MODERATE](#MODERATE) | Marges modérées. |
| [NARROW](#NARROW) | Marges étroites. |
| [NORMAL](#NORMAL) | Marges normales. |
| [WIDE](#WIDE) | Marges larges. |
| [length](#length) |  |
## Méthodes

| Méthode | Description |
| --- | --- |
| [fromName(String marginsName)](#fromName-java.lang.String) |  |
| [getName(int margins)](#getName-int) |  |
| [getValues()](#getValues) |  |
| [toString(int margins)](#toString-int) |  |
### CUSTOM {#CUSTOM}
```
public static int CUSTOM
```


Marges personnalisées.

### MIRRORED {#MIRRORED}
```
public static int MIRRORED
```


Marges miroir.

 **Remarks:** 

Définir les marges sur Mirrored définira la valeur appropriée pour la propriété [PageSetup.getMultiplePages()](../../com.aspose.words/pagesetup/\#getMultiplePages) / [PageSetup.setMultiplePages(int)](../../com.aspose.words/pagesetup/\#setMultiplePages-int). Cela affectera l'ensemble du document, pas seulement la section actuelle.

### MODERATE {#MODERATE}
```
public static int MODERATE
```


Marges modérées.

### NARROW {#NARROW}
```
public static int NARROW
```


Marges étroites.

### NORMAL {#NORMAL}
```
public static int NORMAL
```


Marges normales.

### WIDE {#WIDE}
```
public static int WIDE
```


Marges larges.

### length {#length}
```
public static int length
```


### fromName(String marginsName) {#fromName-java.lang.String}
```
public static int fromName(String marginsName)
```




**Parameters:**
| Paramètre | Type | Description |
| --- | --- | --- |
| marginsName | java.lang.String |  |

**Returns:**
int
### getName(int margins) {#getName-int}
```
public static String getName(int margins)
```




**Parameters:**
| Paramètre | Type | Description |
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
| Paramètre | Type | Description |
| --- | --- | --- |
| margins | int |  |

**Returns:**
java.lang.String
