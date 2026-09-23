---
title: "HeaderFooterBookmarksExportMode"
linktitle: "HeaderFooterBookmarksExportMode"
second_title: "Aspose.Words für Java"
description: "Gibt an, wie Lesezeichen in Kopf‑/Fußzeilen in Java exportiert werden."
type: docs
weight: 370
url: /de/java/com.aspose.words/headerfooterbookmarksexportmode/
---

**Inheritance:**
java.lang.Object
```
public class HeaderFooterBookmarksExportMode
```

Gibt an, wie Lesezeichen in Headern/Footern exportiert werden.

 **Examples:** 

Zeigt, wie Lesezeichen in Kopf‑/Fußzeilen in einem Dokument verarbeitet werden, das wir zu PDF rendern.

```

 Document doc = new Document(getMyDir() + "Bookmarks in headers and footers.docx");

 // Create a "PdfSaveOptions" object that we can pass to the document's "Save" method
 // to modify how that method converts the document to .PDF.
 PdfSaveOptions saveOptions = new PdfSaveOptions();

 // Set the "PageMode" property to "PdfPageMode.UseOutlines" to display the outline navigation pane in the output PDF.
 saveOptions.setPageMode(PdfPageMode.USE_OUTLINES);

 // Set the "DefaultBookmarksOutlineLevel" property to "1" to display all
 // bookmarks at the first level of the outline in the output PDF.
 saveOptions.getOutlineOptions().setDefaultBookmarksOutlineLevel(1);

 // Set the "HeaderFooterBookmarksExportMode" property to "HeaderFooterBookmarksExportMode.None" to
 // not export any bookmarks that are inside headers/footers.
 // Set the "HeaderFooterBookmarksExportMode" property to "HeaderFooterBookmarksExportMode.First" to
 // only export bookmarks in the first section's header/footers.
 // Set the "HeaderFooterBookmarksExportMode" property to "HeaderFooterBookmarksExportMode.All" to
 // export bookmarks that are in all headers/footers.
 saveOptions.setHeaderFooterBookmarksExportMode(headerFooterBookmarksExportMode);

 doc.save(getArtifactsDir() + "PdfSaveOptions.HeaderFooterBookmarksExportMode.pdf", saveOptions);
 
```
## Felder

| Feld | Beschreibung |
| --- | --- |
| [ALL](#ALL) | Lesezeichen in allen Kopf‑/Fußzeilen werden exportiert. |
| [FIRST](#FIRST) | Nur das Lesezeichen in der ersten Kopf‑/Fußzeile des Abschnitts wird exportiert. |
| [NONE](#NONE) | Lesezeichen in Kopf‑/Fußzeilen werden nicht exportiert. |
| [length](#length) |  |
## Methoden

| Methode | Beschreibung |
| --- | --- |
| [fromName(String headerFooterBookmarksExportModeName)](#fromName-java.lang.String) |  |
| [getName(int headerFooterBookmarksExportMode)](#getName-int) |  |
| [getValues()](#getValues) |  |
| [toString(int headerFooterBookmarksExportMode)](#toString-int) |  |
### ALL {#ALL}
```
public static int ALL
```


Lesezeichen in allen Kopf‑/Fußzeilen werden exportiert.

### FIRST {#FIRST}
```
public static int FIRST
```


Nur das Lesezeichen in der ersten Kopf‑/Fußzeile des Abschnitts wird exportiert.

### NONE {#NONE}
```
public static int NONE
```


Lesezeichen in Kopf‑/Fußzeilen werden nicht exportiert.

### length {#length}
```
public static int length
```


### fromName(String headerFooterBookmarksExportModeName) {#fromName-java.lang.String}
```
public static int fromName(String headerFooterBookmarksExportModeName)
```




**Parameters:**
| Parameter | Typ | Beschreibung |
| --- | --- | --- |
| headerFooterBookmarksExportModeName | java.lang.String |  |

**Returns:**
int
### getName(int headerFooterBookmarksExportMode) {#getName-int}
```
public static String getName(int headerFooterBookmarksExportMode)
```




**Parameters:**
| Parameter | Typ | Beschreibung |
| --- | --- | --- |
| headerFooterBookmarksExportMode | int |  |

**Returns:**
java.lang.String
### getValues() {#getValues}
```
public static int[] getValues()
```




**Returns:**
int[]
### toString(int headerFooterBookmarksExportMode) {#toString-int}
```
public static String toString(int headerFooterBookmarksExportMode)
```




**Parameters:**
| Parameter | Typ | Beschreibung |
| --- | --- | --- |
| headerFooterBookmarksExportMode | int |  |

**Returns:**
java.lang.String
