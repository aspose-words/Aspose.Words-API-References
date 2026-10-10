---
title: "PdfPageMode"
linktitle: "PdfPageMode"
second_title: "Aspose.Words para Java"
description: "Especifica cómo se debe mostrar el documento PDF al abrirse en el lector PDF en Java."
type: docs
weight: 540
url: /es/java/com.aspose.words/pdfpagemode/
---

**Inheritance:**
java.lang.Object
```
public class PdfPageMode
```

Especifica cómo se debe mostrar el documento PDF al abrirse en el lector PDF.

 **Examples:** 

Muestra cómo procesar los marcadores en encabezados/pies de página en un documento que estamos renderizando a PDF.

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

Muestra cómo establecer instrucciones para que algunos lectores PDF las sigan al abrir un documento de salida.

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
## Campos

| Campo | Descripción |
| --- | --- |
| [FULL_SCREEN](#FULL-SCREEN) | Modo de pantalla completa, sin barra de menús, controles de ventana o cualquier otra ventana visible. |
| [USE_ATTACHMENTS](#USE-ATTACHMENTS) | El panel de adjuntos es visible. |
| [USE_NONE](#USE-NONE) | Ni el esquema del documento ni las imágenes en miniatura son visibles. |
| [USE_OC](#USE-OC) | El panel de grupo de contenido opcional es visible. |
| [USE_OUTLINES](#USE-OUTLINES) | El esquema del documento es visible. |
| [USE_THUMBS](#USE-THUMBS) | Las imágenes en miniatura son visibles. |
| [length](#length) |  |
## Métodos

| Método | Descripción |
| --- | --- |
| [fromName(String pdfPageModeName)](#fromName-java.lang.String) |  |
| [getName(int pdfPageMode)](#getName-int) |  |
| [getValues()](#getValues) |  |
| [toString(int pdfPageMode)](#toString-int) |  |
### FULL_SCREEN {#FULL-SCREEN}
```
public static int FULL_SCREEN
```


Modo de pantalla completa, sin barra de menús, controles de ventana o cualquier otra ventana visible.

### USE_ATTACHMENTS {#USE-ATTACHMENTS}
```
public static int USE_ATTACHMENTS
```


El panel de adjuntos es visible.

 **Remarks:** 

No compatible con las siguientes versiones de PDF: [PdfCompliance.PDF\_A\_1\_A](../../com.aspose.words/pdfcompliance/\#PDF-A-1-A), [PdfCompliance.PDF\_A\_1\_B](../../com.aspose.words/pdfcompliance/\#PDF-A-1-B).

### USE_NONE {#USE-NONE}
```
public static int USE_NONE
```


Ni el esquema del documento ni las imágenes en miniatura son visibles.

### USE_OC {#USE-OC}
```
public static int USE_OC
```


El panel de grupo de contenido opcional es visible.

 **Remarks:** 

No compatible con las siguientes versiones de PDF: [PdfCompliance.PDF\_A\_1\_A](../../com.aspose.words/pdfcompliance/\#PDF-A-1-A), [PdfCompliance.PDF\_A\_1\_B](../../com.aspose.words/pdfcompliance/\#PDF-A-1-B).

### USE_OUTLINES {#USE-OUTLINES}
```
public static int USE_OUTLINES
```


El esquema del documento es visible. Tenga en cuenta que si no hay esquemas en el documento PDF, el panel de navegación del esquema no será visible de todos modos.

### USE_THUMBS {#USE-THUMBS}
```
public static int USE_THUMBS
```


Las imágenes en miniatura son visibles.

### length {#length}
```
public static int length
```


### fromName(String pdfPageModeName) {#fromName-java.lang.String}
```
public static int fromName(String pdfPageModeName)
```




**Parameters:**
| Parámetro | Tipo | Descripción |
| --- | --- | --- |
| pdfPageModeName | java.lang.String |  |

**Returns:**
int
### getName(int pdfPageMode) {#getName-int}
```
public static String getName(int pdfPageMode)
```




**Parameters:**
| Parámetro | Tipo | Descripción |
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
| Parámetro | Tipo | Descripción |
| --- | --- | --- |
| pdfPageMode | int |  |

**Returns:**
java.lang.String
