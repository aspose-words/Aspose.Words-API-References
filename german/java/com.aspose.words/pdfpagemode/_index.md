---
title: "PdfPageMode"
linktitle: "PdfPageMode"
second_title: "Aspose.Words für Java"
description: "Gibt an, wie das PDF-Dokument angezeigt werden soll, wenn es im PDF-Reader in Java geöffnet wird."
type: docs
weight: 540
url: /de/java/com.aspose.words/pdfpagemode/
---

**Inheritance:**
java.lang.Object
```
public class PdfPageMode
```

Gibt an, wie das PDF-Dokument angezeigt werden soll, wenn es im PDF‑Reader geöffnet wird.

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

Zeigt, wie Anweisungen für einige PDF-Reader festgelegt werden, die beim Öffnen eines Ausgabedokuments befolgt werden sollen.

```

 Document doc = new Document();
 DocumentBuilder builder = new DocumentBuilder(doc);
 builder.writeln("Hello world!");

 // Create a "PdfSaveOptions" object that we can pass to the document's "Save" method
 // to modify how that method converts the document to .PDF.
 PdfSaveOptions options = new PdfSaveOptions();

 // Set the "PageMode" property to "PdfPageMode.FullScreen" to get the PDF reader to open the saved
 // document in full-screen mode, which takes over the monitor's display and has no controls visible.
 // Set the "PageMode" property to "PdfPageMode.UseThumbs" to get the PDF reader to display a separate panel
 // with a thumbnail for each page in the document.
 // Set the "PageMode" property to "PdfPageMode.UseOC" to get the PDF reader to display a separate panel
 // that allows us to work with any layers present in the document.
 // Set the "PageMode" property to "PdfPageMode.UseOutlines" to get the PDF reader
 // also to display the outline, if possible.
 // Set the "PageMode" property to "PdfPageMode.UseNone" to get the PDF reader to display just the document itself.
 // Set the "PageMode" property to "PdfPageMode.UseAttachments" to make visible attachments panel.
 options.setPageMode(pageMode);

 doc.save(getArtifactsDir() + "PdfSaveOptions.PageMode.pdf", options);
 
```
## Felder

| Feld | Beschreibung |
| --- | --- |
| [FULL_SCREEN](#FULL-SCREEN) | Vollbildmodus, ohne Menüleiste, Fenstersteuerungen oder andere sichtbare Fenster. |
| [USE_ATTACHMENTS](#USE-ATTACHMENTS) | Das Anhangs‑Panel ist sichtbar. |
| [USE_NONE](#USE-NONE) | Weder die Dokumentenübersicht noch die Miniaturbilder sind sichtbar. |
| [USE_OC](#USE-OC) | Das Panel für optionale Inhaltsgruppen ist sichtbar. |
| [USE_OUTLINES](#USE-OUTLINES) | Die Dokumentenübersicht ist sichtbar. |
| [USE_THUMBS](#USE-THUMBS) | Miniaturbilder sind sichtbar. |
| [length](#length) |  |
## Methoden

| Methode | Beschreibung |
| --- | --- |
| [fromName(String pdfPageModeName)](#fromName-java.lang.String) |  |
| [getName(int pdfPageMode)](#getName-int) |  |
| [getValues()](#getValues) |  |
| [toString(int pdfPageMode)](#toString-int) |  |
### FULL_SCREEN {#FULL-SCREEN}
```
public static int FULL_SCREEN
```


Vollbildmodus, ohne Menüleiste, Fenstersteuerungen oder andere sichtbare Fenster.

### USE_ATTACHMENTS {#USE-ATTACHMENTS}
```
public static int USE_ATTACHMENTS
```


Das Anhangs‑Panel ist sichtbar.

 **Remarks:** 

Nicht unterstützt in den folgenden PDF-Versionen: [PdfCompliance.PDF\_A\_1\_A](../../com.aspose.words/pdfcompliance/\#PDF-A-1-A), [PdfCompliance.PDF\_A\_1\_B](../../com.aspose.words/pdfcompliance/\#PDF-A-1-B).

### USE_NONE {#USE-NONE}
```
public static int USE_NONE
```


Weder die Dokumentenübersicht noch die Miniaturbilder sind sichtbar.

### USE_OC {#USE-OC}
```
public static int USE_OC
```


Das Panel für optionale Inhaltsgruppen ist sichtbar.

 **Remarks:** 

Nicht unterstützt in den folgenden PDF-Versionen: [PdfCompliance.PDF\_A\_1\_A](../../com.aspose.words/pdfcompliance/\#PDF-A-1-A), [PdfCompliance.PDF\_A\_1\_B](../../com.aspose.words/pdfcompliance/\#PDF-A-1-B).

### USE_OUTLINES {#USE-OUTLINES}
```
public static int USE_OUTLINES
```


Die Dokumentenübersicht ist sichtbar. Hinweis: Wenn im PDF-Dokument keine Übersichten vorhanden sind, wird das Navigations‑Paneel für Übersichten ohnehin nicht sichtbar sein.

### USE_THUMBS {#USE-THUMBS}
```
public static int USE_THUMBS
```


Miniaturbilder sind sichtbar.

### length {#length}
```
public static int length
```


### fromName(String pdfPageModeName) {#fromName-java.lang.String}
```
public static int fromName(String pdfPageModeName)
```




**Parameters:**
| Parameter | Typ | Beschreibung |
| --- | --- | --- |
| pdfPageModeName | java.lang.String |  |

**Returns:**
int
### getName(int pdfPageMode) {#getName-int}
```
public static String getName(int pdfPageMode)
```




**Parameters:**
| Parameter | Typ | Beschreibung |
| --- | --- | --- |
| pdfPageMode | int |  |

**Returns:**
java.lang.String
### getValues() {#getValues}
```
public static int[] getValues()
```




**Returns:**
int[]
### toString(int pdfPageMode) {#toString-int}
```
public static String toString(int pdfPageMode)
```




**Parameters:**
| Parameter | Typ | Beschreibung |
| --- | --- | --- |
| pdfPageMode | int |  |

**Returns:**
java.lang.String
