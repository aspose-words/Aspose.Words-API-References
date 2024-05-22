---
title: PdfPageMode
linktitle: PdfPageMode
second_title: Aspose.Words for Java
description: Specifies how the PDF document should be displayed when opened in the PDF reader in Java.
type: docs
weight: 498
url: /java/com.aspose.words/pdfpagemode/
---

**Inheritance:**
java.lang.Object
```
public class PdfPageMode
```

Specifies how the PDF document should be displayed when opened in the PDF reader.

 **Examples:** 

Shows how to set instructions for some PDF readers to follow when opening an output document.

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

Shows to process bookmarks in headers/footers in a document that we are rendering to PDF.

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
## Fields

| Field | Description |
| --- | --- |
| [FULL_SCREEN](#FULL-SCREEN) | Full-screen mode, with no menu bar, window controls, or any other window visible. |
| [USE_ATTACHMENTS](#USE-ATTACHMENTS) | Attachments panel is visible. |
| [USE_NONE](#USE-NONE) | Neither document outline nor thumbnail images are visible. |
| [USE_OC](#USE-OC) | Optional content group panel is visible. |
| [USE_OUTLINES](#USE-OUTLINES) | Document outline is visible. |
| [USE_THUMBS](#USE-THUMBS) | Thumbnail images are visible. |
| [length](#length) |  |
## Methods

| Method | Description |
| --- | --- |
| [fromName(String pdfPageModeName)](#fromName-java.lang.String) |  |
| [getName(int pdfPageMode)](#getName-int) |  |
| [getValues()](#getValues) |  |
| [toString(int pdfPageMode)](#toString-int) |  |
### FULL_SCREEN {#FULL-SCREEN}
```
public static int FULL_SCREEN
```


Full-screen mode, with no menu bar, window controls, or any other window visible.

### USE_ATTACHMENTS {#USE-ATTACHMENTS}
```
public static int USE_ATTACHMENTS
```


Attachments panel is visible.

 **Remarks:** 

Not supported in the following PDF versions: [PdfCompliance.PDF\_A\_1\_A](../../com.aspose.words/pdfcompliance/\#PDF-A-1-A), [PdfCompliance.PDF\_A\_1\_B](../../com.aspose.words/pdfcompliance/\#PDF-A-1-B).

### USE_NONE {#USE-NONE}
```
public static int USE_NONE
```


Neither document outline nor thumbnail images are visible.

### USE_OC {#USE-OC}
```
public static int USE_OC
```


Optional content group panel is visible.

 **Remarks:** 

Not supported in the following PDF versions: [PdfCompliance.PDF\_A\_1\_A](../../com.aspose.words/pdfcompliance/\#PDF-A-1-A), [PdfCompliance.PDF\_A\_1\_B](../../com.aspose.words/pdfcompliance/\#PDF-A-1-B).

### USE_OUTLINES {#USE-OUTLINES}
```
public static int USE_OUTLINES
```


Document outline is visible. Note that if there're no outlines in the PDF document then outline navigation pane will not be visible anyway.

### USE_THUMBS {#USE-THUMBS}
```
public static int USE_THUMBS
```


Thumbnail images are visible.

### length {#length}
```
public static int length
```


### fromName(String pdfPageModeName) {#fromName-java.lang.String}
```
public static int fromName(String pdfPageModeName)
```




**Parameters:**
| Parameter | Type | Description |
| --- | --- | --- |
| pdfPageModeName | java.lang.String |  |

**Returns:**
int
### getName(int pdfPageMode) {#getName-int}
```
public static String getName(int pdfPageMode)
```




**Parameters:**
| Parameter | Type | Description |
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
| Parameter | Type | Description |
| --- | --- | --- |
| pdfPageMode | int |  |

**Returns:**
java.lang.String
