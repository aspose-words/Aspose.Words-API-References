---
title: HeaderFooterBookmarksExportMode
linktitle: HeaderFooterBookmarksExportMode
second_title: Aspose.Words for Java
description: Specifies how bookmarks in headers/footers are exported in Java.
type: docs
weight: 349
url: /java/com.aspose.words/headerfooterbookmarksexportmode/
---

**Inheritance:**
java.lang.Object
```
public class HeaderFooterBookmarksExportMode
```

Specifies how bookmarks in headers/footers are exported.

 **Examples:** 

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
| [ALL](#ALL) | Bookmarks in all headers/footers are exported. |
| [FIRST](#FIRST) | Only bookmark in first header/footer of the section is exported. |
| [NONE](#NONE) | Bookmarks in headers/footers are not exported. |
| [length](#length) |  |
## Methods

| Method | Description |
| --- | --- |
| [fromName(String headerFooterBookmarksExportModeName)](#fromName-java.lang.String) |  |
| [getName(int headerFooterBookmarksExportMode)](#getName-int) |  |
| [getValues()](#getValues) |  |
| [toString(int headerFooterBookmarksExportMode)](#toString-int) |  |
### ALL {#ALL}
```
public static int ALL
```


Bookmarks in all headers/footers are exported.

### FIRST {#FIRST}
```
public static int FIRST
```


Only bookmark in first header/footer of the section is exported.

### NONE {#NONE}
```
public static int NONE
```


Bookmarks in headers/footers are not exported.

### length {#length}
```
public static int length
```


### fromName(String headerFooterBookmarksExportModeName) {#fromName-java.lang.String}
```
public static int fromName(String headerFooterBookmarksExportModeName)
```




**Parameters:**
| Parameter | Type | Description |
| --- | --- | --- |
| headerFooterBookmarksExportModeName | java.lang.String |  |

**Returns:**
int
### getName(int headerFooterBookmarksExportMode) {#getName-int}
```
public static String getName(int headerFooterBookmarksExportMode)
```




**Parameters:**
| Parameter | Type | Description |
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
| Parameter | Type | Description |
| --- | --- | --- |
| headerFooterBookmarksExportMode | int |  |

**Returns:**
java.lang.String
