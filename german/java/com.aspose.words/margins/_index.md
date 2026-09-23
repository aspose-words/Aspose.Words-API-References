---
title: "Margins"
linktitle: "Margins"
second_title: "Aspose.Words für Java"
description: "Gibt vordefinierte Ränder in Java an."
type: docs
weight: 449
url: /de/java/com.aspose.words/margins/
---

**Inheritance:**
java.lang.Object
```
public class Margins
```

Gibt voreingestellte Ränder an.

 **Examples:** 

Zeigt, wann das Seitenlayout des Dokuments neu berechnet werden soll.

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
## Felder

| Feld | Beschreibung |
| --- | --- |
| [CUSTOM](#CUSTOM) | Benutzerdefinierte Ränder. |
| [MIRRORED](#MIRRORED) | Spiegelnde Ränder. |
| [MODERATE](#MODERATE) | Mäßige Ränder. |
| [NARROW](#NARROW) | Schmale Ränder. |
| [NORMAL](#NORMAL) | Normale Ränder. |
| [WIDE](#WIDE) | Breite Ränder. |
| [length](#length) |  |
## Methoden

| Methode | Beschreibung |
| --- | --- |
| [fromName(String marginsName)](#fromName-java.lang.String) |  |
| [getName(int margins)](#getName-int) |  |
| [getValues()](#getValues) |  |
| [toString(int margins)](#toString-int) |  |
### CUSTOM {#CUSTOM}
```
public static int CUSTOM
```


Benutzerdefinierte Ränder.

### MIRRORED {#MIRRORED}
```
public static int MIRRORED
```


Spiegelnde Ränder.

 **Remarks:** 

Das Festlegen der Ränder auf Spiegelnd setzt den entsprechenden Wert für die Eigenschaft [PageSetup.getMultiplePages()](../../com.aspose.words/pagesetup/\#getMultiplePages) / [PageSetup.setMultiplePages(int)](../../com.aspose.words/pagesetup/\#setMultiplePages-int). Dies wirkt sich auf das gesamte Dokument aus, nicht nur auf den aktuellen Abschnitt.

### MODERATE {#MODERATE}
```
public static int MODERATE
```


Mäßige Ränder.

### NARROW {#NARROW}
```
public static int NARROW
```


Schmale Ränder.

### NORMAL {#NORMAL}
```
public static int NORMAL
```


Normale Ränder.

### WIDE {#WIDE}
```
public static int WIDE
```


Breite Ränder.

### length {#length}
```
public static int length
```


### fromName(String marginsName) {#fromName-java.lang.String}
```
public static int fromName(String marginsName)
```




**Parameters:**
| Parameter | Typ | Beschreibung |
| --- | --- | --- |
| marginsName | java.lang.String |  |

**Returns:**
int
### getName(int margins) {#getName-int}
```
public static String getName(int margins)
```




**Parameters:**
| Parameter | Typ | Beschreibung |
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
| Parameter | Typ | Beschreibung |
| --- | --- | --- |
| margins | int |  |

**Returns:**
java.lang.String
