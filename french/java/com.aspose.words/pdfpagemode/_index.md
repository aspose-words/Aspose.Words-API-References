---
title: "PdfPageMode"
linktitle: "PdfPageMode"
second_title: "Aspose.Words pour Java"
description: "Spécifie comment le document PDF doit être affiché lorsqu'il est ouvert dans le lecteur PDF en Java."
type: docs
weight: 540
url: /fr/java/com.aspose.words/pdfpagemode/
---

**Inheritance:**
java.lang.Object
```
public class PdfPageMode
```

Spécifie comment le document PDF doit être affiché lorsqu'il est ouvert dans le lecteur PDF.

 **Examples:** 

Montre comment traiter les signets dans les en-têtes/pieds de page d'un document que nous rendons en PDF.

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

Montre comment définir des instructions que certains lecteurs PDF doivent suivre lors de l'ouverture d'un document de sortie.

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
## Champs

| Champ | Description |
| --- | --- |
| [FULL_SCREEN](#FULL-SCREEN) | Mode plein écran, sans barre de menus, contrôles de fenêtre, ni aucune autre fenêtre visible. |
| [USE_ATTACHMENTS](#USE-ATTACHMENTS) | Le panneau des pièces jointes est visible. |
| [USE_NONE](#USE-NONE) | Ni le plan du document ni les images miniatures ne sont visibles. |
| [USE_OC](#USE-OC) | Le panneau du groupe de contenu optionnel est visible. |
| [USE_OUTLINES](#USE-OUTLINES) | Le plan du document est visible. |
| [USE_THUMBS](#USE-THUMBS) | Les images miniatures sont visibles. |
| [length](#length) |  |
## Méthodes

| Méthode | Description |
| --- | --- |
| [fromName(String pdfPageModeName)](#fromName-java.lang.String) |  |
| [getName(int pdfPageMode)](#getName-int) |  |
| [getValues()](#getValues) |  |
| [toString(int pdfPageMode)](#toString-int) |  |
### FULL_SCREEN {#FULL-SCREEN}
```
public static int FULL_SCREEN
```


Mode plein écran, sans barre de menus, contrôles de fenêtre, ni aucune autre fenêtre visible.

### USE_ATTACHMENTS {#USE-ATTACHMENTS}
```
public static int USE_ATTACHMENTS
```


Le panneau des pièces jointes est visible.

 **Remarks:** 

Non pris en charge dans les versions PDF suivantes : [PdfCompliance.PDF\_A\_1\_A](../../com.aspose.words/pdfcompliance/\#PDF-A-1-A), [PdfCompliance.PDF\_A\_1\_B](../../com.aspose.words/pdfcompliance/\#PDF-A-1-B).

### USE_NONE {#USE-NONE}
```
public static int USE_NONE
```


Ni le plan du document ni les images miniatures ne sont visibles.

### USE_OC {#USE-OC}
```
public static int USE_OC
```


Le panneau du groupe de contenu optionnel est visible.

 **Remarks:** 

Non pris en charge dans les versions PDF suivantes : [PdfCompliance.PDF\_A\_1\_A](../../com.aspose.words/pdfcompliance/\#PDF-A-1-A), [PdfCompliance.PDF\_A\_1\_B](../../com.aspose.words/pdfcompliance/\#PDF-A-1-B).

### USE_OUTLINES {#USE-OUTLINES}
```
public static int USE_OUTLINES
```


Le plan du document est visible. Notez que s'il n'y a aucun plan dans le document PDF, le volet de navigation du plan ne sera de toute façon pas visible.

### USE_THUMBS {#USE-THUMBS}
```
public static int USE_THUMBS
```


Les images miniatures sont visibles.

### length {#length}
```
public static int length
```


### fromName(String pdfPageModeName) {#fromName-java.lang.String}
```
public static int fromName(String pdfPageModeName)
```




**Parameters:**
| Paramètre | Type | Description |
| --- | --- | --- |
| pdfPageModeName | java.lang.String |  |

**Returns:**
int
### getName(int pdfPageMode) {#getName-int}
```
public static String getName(int pdfPageMode)
```




**Parameters:**
| Paramètre | Type | Description |
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
| Paramètre | Type | Description |
| --- | --- | --- |
| pdfPageMode | int |  |

**Returns:**
java.lang.String
