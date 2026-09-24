---
title: "OutlineOptions"
linktitle: "OutlineOptions"
second_title: "Aspose.Words para Java"
description: "Permite especificar opciones de esquema en Java."
type: docs
weight: 509
url: /es/java/com.aspose.words/outlineoptions/
---

**Inheritance:**
java.lang.Object
```
public class OutlineOptions
```

Permite especificar opciones de esquema.

Para obtener más información, visite el artículo de documentación [ Save a Document ][Save a Document].

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


[Save a Document]: https://docs.aspose.com/words/java/save-a-document/
## Métodos

| Método | Descripción |
| --- | --- |
| [getBookmarksOutlineLevels()](#getBookmarksOutlineLevels) | Permite especificar el nivel de esquema de marcadores individuales. |
| [getCreateMissingOutlineLevels()](#getCreateMissingOutlineLevels) | Obtiene o establece un valor que determina si se deben crear niveles de esquema faltantes cuando el documento se exporta. |
| [getCreateOutlinesForHeadingsInTables()](#getCreateOutlinesForHeadingsInTables) | Especifica si se deben crear esquemas para los encabezados (párrafos con los estilos de Encabezado) dentro de tablas. |
| [getDefaultBookmarksOutlineLevel()](#getDefaultBookmarksOutlineLevel) | Especifica el nivel predeterminado en el esquema del documento en el que se mostrarán los marcadores de Word. |
| [getExpandedOutlineLevels()](#getExpandedOutlineLevels) | Especifica cuántos niveles del esquema del documento se mostrarán expandidos al visualizar el archivo. |
| [getHeadingsOutlineLevels()](#getHeadingsOutlineLevels) | Especifica cuántos niveles de encabezados (párrafos con los estilos de Encabezado) se incluirán en el esquema del documento. |
| [setCreateMissingOutlineLevels(boolean value)](#setCreateMissingOutlineLevels-boolean) | Obtiene o establece un valor que determina si se deben crear niveles de esquema faltantes cuando el documento se exporta. |
| [setCreateOutlinesForHeadingsInTables(boolean value)](#setCreateOutlinesForHeadingsInTables-boolean) | Especifica si se deben crear esquemas para los encabezados (párrafos con los estilos de Encabezado) dentro de tablas. |
| [setDefaultBookmarksOutlineLevel(int value)](#setDefaultBookmarksOutlineLevel-int) | Especifica el nivel predeterminado en el esquema del documento en el que se mostrarán los marcadores de Word. |
| [setExpandedOutlineLevels(int value)](#setExpandedOutlineLevels-int) | Especifica cuántos niveles del esquema del documento se mostrarán expandidos al visualizar el archivo. |
| [setHeadingsOutlineLevels(int value)](#setHeadingsOutlineLevels-int) | Especifica cuántos niveles de encabezados (párrafos con los estilos de Encabezado) se incluirán en el esquema del documento. |
### getBookmarksOutlineLevels() {#getBookmarksOutlineLevels}
```
public BookmarksOutlineLevelCollection getBookmarksOutlineLevels()
```


Permite especificar el nivel de esquema de marcadores individuales.

 **Remarks:** 

Si el nivel de marcador no se especifica en esta colección, se utilizará el valor de [getDefaultBookmarksOutlineLevel()](../../com.aspose.words/outlineoptions/\#getDefaultBookmarksOutlineLevel) / [setDefaultBookmarksOutlineLevel(int)](../../com.aspose.words/outlineoptions/\#setDefaultBookmarksOutlineLevel-int).

 **Examples:** 

Muestra cómo establecer niveles de esquema para los marcadores.

```

 Document doc = new Document();
 DocumentBuilder builder = new DocumentBuilder(doc);

 // Insert a bookmark with another bookmark nested inside it.
 builder.startBookmark("Bookmark 1");
 builder.writeln("Text inside Bookmark 1.");

 builder.startBookmark("Bookmark 2");
 builder.writeln("Text inside Bookmark 1 and 2.");
 builder.endBookmark("Bookmark 2");

 builder.writeln("Text inside Bookmark 1.");
 builder.endBookmark("Bookmark 1");

 // Insert another bookmark.
 builder.startBookmark("Bookmark 3");
 builder.writeln("Text inside Bookmark 3.");
 builder.endBookmark("Bookmark 3");

 // When saving to .pdf, bookmarks can be accessed via a drop-down menu and used as anchors by most readers.
 // Bookmarks can also have numeric values for outline levels,
 // enabling lower level outline entries to hide higher-level child entries when collapsed in the reader.
 PdfSaveOptions pdfSaveOptions = new PdfSaveOptions();
 BookmarksOutlineLevelCollection outlineLevels = pdfSaveOptions.getOutlineOptions().getBookmarksOutlineLevels();

 outlineLevels.add("Bookmark 1", 1);
 outlineLevels.add("Bookmark 2", 2);
 outlineLevels.add("Bookmark 3", 3);

 Assert.assertEquals(outlineLevels.getCount(), 3);
 Assert.assertTrue(outlineLevels.contains("Bookmark 1"));
 Assert.assertEquals(outlineLevels.get(0), 1);
 Assert.assertEquals(outlineLevels.get("Bookmark 2"), 2);
 Assert.assertEquals(outlineLevels.indexOfKey("Bookmark 3"), 2);

 // We can remove two elements so that only the outline level designation for "Bookmark 1" is left.
 outlineLevels.removeAt(2);
 outlineLevels.remove("Bookmark 2");

 // There are nine outline levels. Their numbering will be optimized during the save operation.
 // In this case, levels "5" and "9" will become "2" and "3".
 outlineLevels.add("Bookmark 2", 5);
 outlineLevels.add("Bookmark 3", 9);

 doc.save(getArtifactsDir() + "BookmarksOutlineLevelCollection.BookmarkLevels.pdf", pdfSaveOptions);

 // Emptying this collection will preserve the bookmarks and put them all on the same outline level.
 outlineLevels.clear();
 
```

**Returns:**
[BookmarksOutlineLevelCollection](../../com.aspose.words/bookmarksoutlinelevelcollection/) - The corresponding [BookmarksOutlineLevelCollection](../../com.aspose.words/bookmarksoutlinelevelcollection/) value.
### getCreateMissingOutlineLevels() {#getCreateMissingOutlineLevels}
```
public boolean getCreateMissingOutlineLevels()
```


Obtiene o establece un valor que determina si se deben crear niveles de esquema faltantes cuando el documento se exporta.

El valor predeterminado para esta propiedad es false.

 **Examples:** 

Muestra cómo trabajar con niveles de esquema que no contienen encabezados correspondientes al guardar un documento PDF.

```

 Document doc = new Document();
 DocumentBuilder builder = new DocumentBuilder(doc);

 // Insert headings that can serve as TOC entries of levels 1 and 5.
 builder.getParagraphFormat().setStyleIdentifier(StyleIdentifier.HEADING_1);

 Assert.assertTrue(builder.getParagraphFormat().isHeading());

 builder.writeln("Heading 1");

 builder.getParagraphFormat().setStyleIdentifier(StyleIdentifier.HEADING_5);

 builder.writeln("Heading 1.1.1.1.1");
 builder.writeln("Heading 1.1.1.1.2");

 // Create a "PdfSaveOptions" object that we can pass to the document's "Save" method
 // to modify how that method converts the document to .PDF.
 PdfSaveOptions saveOptions = new PdfSaveOptions();

 // The output PDF document will contain an outline, which is a table of contents that lists headings in the document body.
 // Clicking on an entry in this outline will take us to the location of its respective heading.
 // Set the "HeadingsOutlineLevels" property to "5" to include all headings of levels 5 and below in the outline.
 saveOptions.getOutlineOptions().setHeadingsOutlineLevels(5);

 // This document contains headings of levels 1 and 5, and no headings with levels of 2, 3, and 4.
 // The output PDF document will treat outline levels 2, 3, and 4 as "missing".
 // Set the "CreateMissingOutlineLevels" property to "true" to include all missing levels in the outline,
 // leaving blank outline entries since there are no usable headings.
 // Set the "CreateMissingOutlineLevels" property to "false" to ignore missing outline levels,
 // and treat the outline level 5 headings as level 2.
 saveOptions.getOutlineOptions().setCreateMissingOutlineLevels(createMissingOutlineLevels);

 doc.save(getArtifactsDir() + "PdfSaveOptions.CreateMissingOutlineLevels.pdf", saveOptions);
 
```

**Returns:**
boolean - El valor  boolean  correspondiente.
### getCreateOutlinesForHeadingsInTables() {#getCreateOutlinesForHeadingsInTables}
```
public boolean getCreateOutlinesForHeadingsInTables()
```


Especifica si se deben crear esquemas para los encabezados (párrafos con los estilos de Encabezado) dentro de tablas.

 **Remarks:** 

El valor predeterminado es false.

 **Examples:** 

Muestra cómo crear entradas de esquema de documento PDF para encabezados dentro de tablas.

```

 Document doc = new Document();
 DocumentBuilder builder = new DocumentBuilder(doc);

 // Create a table with three rows. The first row,
 // whose text we will format in a heading-type style, will serve as the column header.
 builder.startTable();
 builder.insertCell();
 builder.getParagraphFormat().setStyleIdentifier(StyleIdentifier.HEADING_1);
 builder.write("Customers");
 builder.endRow();
 builder.insertCell();
 builder.getParagraphFormat().setStyleIdentifier(StyleIdentifier.NORMAL);
 builder.write("John Doe");
 builder.endRow();
 builder.insertCell();
 builder.write("Jane Doe");
 builder.endTable();

 // Create a "PdfSaveOptions" object that we can pass to the document's "Save" method
 // to modify how that method converts the document to .PDF.
 PdfSaveOptions pdfSaveOptions = new PdfSaveOptions();

 // The output PDF document will contain an outline, which is a table of contents that lists headings in the document body.
 // Clicking on an entry in this outline will take us to the location of its respective heading.
 // Set the "HeadingsOutlineLevels" property to "1" to get the outline
 // to only register headings with heading levels that are no larger than 1.
 pdfSaveOptions.getOutlineOptions().setHeadingsOutlineLevels(1);

 // Set the "CreateOutlinesForHeadingsInTables" property to "false" to exclude all headings within tables,
 // such as the one we have created above from the outline.
 // Set the "CreateOutlinesForHeadingsInTables" property to "true" to include all headings within tables
 // in the outline, provided that they have a heading level that is no larger than the value of the "HeadingsOutlineLevels" property.
 pdfSaveOptions.getOutlineOptions().setCreateOutlinesForHeadingsInTables(createOutlinesForHeadingsInTables);

 doc.save(getArtifactsDir() + "PdfSaveOptions.TableHeadingOutlines.pdf", pdfSaveOptions);
 
```

**Returns:**
boolean - El valor  boolean  correspondiente.
### getDefaultBookmarksOutlineLevel() {#getDefaultBookmarksOutlineLevel}
```
public int getDefaultBookmarksOutlineLevel()
```


Especifica el nivel predeterminado en el esquema del documento en el que se mostrarán los marcadores de Word.

 **Remarks:** 

El nivel de marcadores individuales se puede especificar mediante la propiedad [getBookmarksOutlineLevels()](../../com.aspose.words/outlineoptions/\#getBookmarksOutlineLevels).

Especifique 0 y los marcadores de Word no se mostrarán en el esquema del documento. Especifique 1 y los marcadores de Word se mostrarán en el esquema del documento en el nivel 1; 2 para el nivel 2 y así sucesivamente.

El valor predeterminado es 0. El rango válido es de 0 a 9.

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

**Returns:**
int - El valor  int  correspondiente.
### getExpandedOutlineLevels() {#getExpandedOutlineLevels}
```
public int getExpandedOutlineLevels()
```


Especifica cuántos niveles del esquema del documento se mostrarán expandidos al visualizar el archivo.

 **Remarks:** 

Tenga en cuenta que estas opciones no funcionarán al guardar en XPS.

Especifique 0 y el esquema del documento se colapsará; especifique 1 y los elementos del primer nivel en el esquema se expandirán, y así sucesivamente.

El valor predeterminado es 0. El rango válido es de 0 a 9.

 **Examples:** 

Muestra cómo convertir un documento completo a PDF con tres niveles en el esquema del documento.

```

 Document doc = new Document();
 DocumentBuilder builder = new DocumentBuilder(doc);

 // Insert headings of levels 1 to 5.
 builder.getParagraphFormat().setStyleIdentifier(StyleIdentifier.HEADING_1);

 Assert.assertTrue(builder.getParagraphFormat().isHeading());

 builder.writeln("Heading 1");

 builder.getParagraphFormat().setStyleIdentifier(StyleIdentifier.HEADING_2);

 builder.writeln("Heading 1.1");
 builder.writeln("Heading 1.2");

 builder.getParagraphFormat().setStyleIdentifier(StyleIdentifier.HEADING_3);

 builder.writeln("Heading 1.2.1");
 builder.writeln("Heading 1.2.2");

 builder.getParagraphFormat().setStyleIdentifier(StyleIdentifier.HEADING_4);

 builder.writeln("Heading 1.2.2.1");
 builder.writeln("Heading 1.2.2.2");

 builder.getParagraphFormat().setStyleIdentifier(StyleIdentifier.HEADING_5);

 builder.writeln("Heading 1.2.2.2.1");
 builder.writeln("Heading 1.2.2.2.2");

 // Create a "PdfSaveOptions" object that we can pass to the document's "Save" method
 // to modify how that method converts the document to .PDF.
 PdfSaveOptions options = new PdfSaveOptions();

 // The output PDF document will contain an outline, which is a table of contents that lists headings in the document body.
 // Clicking on an entry in this outline will take us to the location of its respective heading.
 // Set the "HeadingsOutlineLevels" property to "4" to exclude all headings whose levels are above 4 from the outline.
 options.getOutlineOptions().setHeadingsOutlineLevels(4);

 // If an outline entry has subsequent entries of a higher level inbetween itself and the next entry of the same or lower level,
 // an arrow will appear to the left of the entry. This entry is the "owner" of several such "sub-entries".
 // In our document, the outline entries from the 5th heading level are sub-entries of the second 4th level outline entry,
 // the 4th and 5th heading level entries are sub-entries of the second 3rd level entry, and so on.
 // In the outline, we can click on the arrow of the "owner" entry to collapse/expand all its sub-entries.
 // Set the "ExpandedOutlineLevels" property to "2" to automatically expand all heading level 2 and lower outline entries
 // and collapse all level and 3 and higher entries when we open the document.
 options.getOutlineOptions().setExpandedOutlineLevels(2);

 doc.save(getArtifactsDir() + "PdfSaveOptions.ExpandedOutlineLevels.pdf", options);
 
```

**Returns:**
int - El valor  int  correspondiente.
### getHeadingsOutlineLevels() {#getHeadingsOutlineLevels}
```
public int getHeadingsOutlineLevels()
```


Especifica cuántos niveles de encabezados (párrafos con los estilos de Encabezado) se incluirán en el esquema del documento.

 **Remarks:** 

Especifique 0 para no tener encabezados en el esquema; especifique 1 para un nivel de encabezados en el esquema, y así sucesivamente.

El valor predeterminado es 0. El rango válido es de 0 a 9.

 **Examples:** 

Muestra cómo convertir un documento completo a PDF con tres niveles en el esquema del documento.

```

 Document doc = new Document();
 DocumentBuilder builder = new DocumentBuilder(doc);

 // Insert headings of levels 1 to 5.
 builder.getParagraphFormat().setStyleIdentifier(StyleIdentifier.HEADING_1);

 Assert.assertTrue(builder.getParagraphFormat().isHeading());

 builder.writeln("Heading 1");

 builder.getParagraphFormat().setStyleIdentifier(StyleIdentifier.HEADING_2);

 builder.writeln("Heading 1.1");
 builder.writeln("Heading 1.2");

 builder.getParagraphFormat().setStyleIdentifier(StyleIdentifier.HEADING_3);

 builder.writeln("Heading 1.2.1");
 builder.writeln("Heading 1.2.2");

 builder.getParagraphFormat().setStyleIdentifier(StyleIdentifier.HEADING_4);

 builder.writeln("Heading 1.2.2.1");
 builder.writeln("Heading 1.2.2.2");

 builder.getParagraphFormat().setStyleIdentifier(StyleIdentifier.HEADING_5);

 builder.writeln("Heading 1.2.2.2.1");
 builder.writeln("Heading 1.2.2.2.2");

 // Create a "PdfSaveOptions" object that we can pass to the document's "Save" method
 // to modify how that method converts the document to .PDF.
 PdfSaveOptions options = new PdfSaveOptions();

 // The output PDF document will contain an outline, which is a table of contents that lists headings in the document body.
 // Clicking on an entry in this outline will take us to the location of its respective heading.
 // Set the "HeadingsOutlineLevels" property to "4" to exclude all headings whose levels are above 4 from the outline.
 options.getOutlineOptions().setHeadingsOutlineLevels(4);

 // If an outline entry has subsequent entries of a higher level inbetween itself and the next entry of the same or lower level,
 // an arrow will appear to the left of the entry. This entry is the "owner" of several such "sub-entries".
 // In our document, the outline entries from the 5th heading level are sub-entries of the second 4th level outline entry,
 // the 4th and 5th heading level entries are sub-entries of the second 3rd level entry, and so on.
 // In the outline, we can click on the arrow of the "owner" entry to collapse/expand all its sub-entries.
 // Set the "ExpandedOutlineLevels" property to "2" to automatically expand all heading level 2 and lower outline entries
 // and collapse all level and 3 and higher entries when we open the document.
 options.getOutlineOptions().setExpandedOutlineLevels(2);

 doc.save(getArtifactsDir() + "PdfSaveOptions.ExpandedOutlineLevels.pdf", options);
 
```

**Returns:**
int - El valor  int  correspondiente.
### setCreateMissingOutlineLevels(boolean value) {#setCreateMissingOutlineLevels-boolean}
```
public void setCreateMissingOutlineLevels(boolean value)
```


Obtiene o establece un valor que determina si se deben crear niveles de esquema faltantes cuando el documento se exporta.

El valor predeterminado para esta propiedad es false.

 **Examples:** 

Muestra cómo trabajar con niveles de esquema que no contienen encabezados correspondientes al guardar un documento PDF.

```

 Document doc = new Document();
 DocumentBuilder builder = new DocumentBuilder(doc);

 // Insert headings that can serve as TOC entries of levels 1 and 5.
 builder.getParagraphFormat().setStyleIdentifier(StyleIdentifier.HEADING_1);

 Assert.assertTrue(builder.getParagraphFormat().isHeading());

 builder.writeln("Heading 1");

 builder.getParagraphFormat().setStyleIdentifier(StyleIdentifier.HEADING_5);

 builder.writeln("Heading 1.1.1.1.1");
 builder.writeln("Heading 1.1.1.1.2");

 // Create a "PdfSaveOptions" object that we can pass to the document's "Save" method
 // to modify how that method converts the document to .PDF.
 PdfSaveOptions saveOptions = new PdfSaveOptions();

 // The output PDF document will contain an outline, which is a table of contents that lists headings in the document body.
 // Clicking on an entry in this outline will take us to the location of its respective heading.
 // Set the "HeadingsOutlineLevels" property to "5" to include all headings of levels 5 and below in the outline.
 saveOptions.getOutlineOptions().setHeadingsOutlineLevels(5);

 // This document contains headings of levels 1 and 5, and no headings with levels of 2, 3, and 4.
 // The output PDF document will treat outline levels 2, 3, and 4 as "missing".
 // Set the "CreateMissingOutlineLevels" property to "true" to include all missing levels in the outline,
 // leaving blank outline entries since there are no usable headings.
 // Set the "CreateMissingOutlineLevels" property to "false" to ignore missing outline levels,
 // and treat the outline level 5 headings as level 2.
 saveOptions.getOutlineOptions().setCreateMissingOutlineLevels(createMissingOutlineLevels);

 doc.save(getArtifactsDir() + "PdfSaveOptions.CreateMissingOutlineLevels.pdf", saveOptions);
 
```

**Parameters:**
| Parámetro | Tipo | Descripción |
| --- | --- | --- |
| valor | boolean | El valor  boolean  correspondiente. |

### setCreateOutlinesForHeadingsInTables(boolean value) {#setCreateOutlinesForHeadingsInTables-boolean}
```
public void setCreateOutlinesForHeadingsInTables(boolean value)
```


Especifica si se deben crear esquemas para los encabezados (párrafos con los estilos de Encabezado) dentro de tablas.

 **Remarks:** 

El valor predeterminado es false.

 **Examples:** 

Muestra cómo crear entradas de esquema de documento PDF para encabezados dentro de tablas.

```

 Document doc = new Document();
 DocumentBuilder builder = new DocumentBuilder(doc);

 // Create a table with three rows. The first row,
 // whose text we will format in a heading-type style, will serve as the column header.
 builder.startTable();
 builder.insertCell();
 builder.getParagraphFormat().setStyleIdentifier(StyleIdentifier.HEADING_1);
 builder.write("Customers");
 builder.endRow();
 builder.insertCell();
 builder.getParagraphFormat().setStyleIdentifier(StyleIdentifier.NORMAL);
 builder.write("John Doe");
 builder.endRow();
 builder.insertCell();
 builder.write("Jane Doe");
 builder.endTable();

 // Create a "PdfSaveOptions" object that we can pass to the document's "Save" method
 // to modify how that method converts the document to .PDF.
 PdfSaveOptions pdfSaveOptions = new PdfSaveOptions();

 // The output PDF document will contain an outline, which is a table of contents that lists headings in the document body.
 // Clicking on an entry in this outline will take us to the location of its respective heading.
 // Set the "HeadingsOutlineLevels" property to "1" to get the outline
 // to only register headings with heading levels that are no larger than 1.
 pdfSaveOptions.getOutlineOptions().setHeadingsOutlineLevels(1);

 // Set the "CreateOutlinesForHeadingsInTables" property to "false" to exclude all headings within tables,
 // such as the one we have created above from the outline.
 // Set the "CreateOutlinesForHeadingsInTables" property to "true" to include all headings within tables
 // in the outline, provided that they have a heading level that is no larger than the value of the "HeadingsOutlineLevels" property.
 pdfSaveOptions.getOutlineOptions().setCreateOutlinesForHeadingsInTables(createOutlinesForHeadingsInTables);

 doc.save(getArtifactsDir() + "PdfSaveOptions.TableHeadingOutlines.pdf", pdfSaveOptions);
 
```

**Parameters:**
| Parámetro | Tipo | Descripción |
| --- | --- | --- |
| valor | boolean | El valor  boolean  correspondiente. |

### setDefaultBookmarksOutlineLevel(int value) {#setDefaultBookmarksOutlineLevel-int}
```
public void setDefaultBookmarksOutlineLevel(int value)
```


Especifica el nivel predeterminado en el esquema del documento en el que se mostrarán los marcadores de Word.

 **Remarks:** 

El nivel de marcadores individuales se puede especificar mediante la propiedad [getBookmarksOutlineLevels()](../../com.aspose.words/outlineoptions/\#getBookmarksOutlineLevels).

Especifique 0 y los marcadores de Word no se mostrarán en el esquema del documento. Especifique 1 y los marcadores de Word se mostrarán en el esquema del documento en el nivel 1; 2 para el nivel 2 y así sucesivamente.

El valor predeterminado es 0. El rango válido es de 0 a 9.

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

**Parameters:**
| Parámetro | Tipo | Descripción |
| --- | --- | --- |
| valor | int | El valor  int  correspondiente. |

### setExpandedOutlineLevels(int value) {#setExpandedOutlineLevels-int}
```
public void setExpandedOutlineLevels(int value)
```


Especifica cuántos niveles del esquema del documento se mostrarán expandidos al visualizar el archivo.

 **Remarks:** 

Tenga en cuenta que estas opciones no funcionarán al guardar en XPS.

Especifique 0 y el esquema del documento se colapsará; especifique 1 y los elementos del primer nivel en el esquema se expandirán, y así sucesivamente.

El valor predeterminado es 0. El rango válido es de 0 a 9.

 **Examples:** 

Muestra cómo convertir un documento completo a PDF con tres niveles en el esquema del documento.

```

 Document doc = new Document();
 DocumentBuilder builder = new DocumentBuilder(doc);

 // Insert headings of levels 1 to 5.
 builder.getParagraphFormat().setStyleIdentifier(StyleIdentifier.HEADING_1);

 Assert.assertTrue(builder.getParagraphFormat().isHeading());

 builder.writeln("Heading 1");

 builder.getParagraphFormat().setStyleIdentifier(StyleIdentifier.HEADING_2);

 builder.writeln("Heading 1.1");
 builder.writeln("Heading 1.2");

 builder.getParagraphFormat().setStyleIdentifier(StyleIdentifier.HEADING_3);

 builder.writeln("Heading 1.2.1");
 builder.writeln("Heading 1.2.2");

 builder.getParagraphFormat().setStyleIdentifier(StyleIdentifier.HEADING_4);

 builder.writeln("Heading 1.2.2.1");
 builder.writeln("Heading 1.2.2.2");

 builder.getParagraphFormat().setStyleIdentifier(StyleIdentifier.HEADING_5);

 builder.writeln("Heading 1.2.2.2.1");
 builder.writeln("Heading 1.2.2.2.2");

 // Create a "PdfSaveOptions" object that we can pass to the document's "Save" method
 // to modify how that method converts the document to .PDF.
 PdfSaveOptions options = new PdfSaveOptions();

 // The output PDF document will contain an outline, which is a table of contents that lists headings in the document body.
 // Clicking on an entry in this outline will take us to the location of its respective heading.
 // Set the "HeadingsOutlineLevels" property to "4" to exclude all headings whose levels are above 4 from the outline.
 options.getOutlineOptions().setHeadingsOutlineLevels(4);

 // If an outline entry has subsequent entries of a higher level inbetween itself and the next entry of the same or lower level,
 // an arrow will appear to the left of the entry. This entry is the "owner" of several such "sub-entries".
 // In our document, the outline entries from the 5th heading level are sub-entries of the second 4th level outline entry,
 // the 4th and 5th heading level entries are sub-entries of the second 3rd level entry, and so on.
 // In the outline, we can click on the arrow of the "owner" entry to collapse/expand all its sub-entries.
 // Set the "ExpandedOutlineLevels" property to "2" to automatically expand all heading level 2 and lower outline entries
 // and collapse all level and 3 and higher entries when we open the document.
 options.getOutlineOptions().setExpandedOutlineLevels(2);

 doc.save(getArtifactsDir() + "PdfSaveOptions.ExpandedOutlineLevels.pdf", options);
 
```

**Parameters:**
| Parámetro | Tipo | Descripción |
| --- | --- | --- |
| valor | int | El valor  int  correspondiente. |

### setHeadingsOutlineLevels(int value) {#setHeadingsOutlineLevels-int}
```
public void setHeadingsOutlineLevels(int value)
```


Especifica cuántos niveles de encabezados (párrafos con los estilos de Encabezado) se incluirán en el esquema del documento.

 **Remarks:** 

Especifique 0 para no tener encabezados en el esquema; especifique 1 para un nivel de encabezados en el esquema, y así sucesivamente.

El valor predeterminado es 0. El rango válido es de 0 a 9.

 **Examples:** 

Muestra cómo convertir un documento completo a PDF con tres niveles en el esquema del documento.

```

 Document doc = new Document();
 DocumentBuilder builder = new DocumentBuilder(doc);

 // Insert headings of levels 1 to 5.
 builder.getParagraphFormat().setStyleIdentifier(StyleIdentifier.HEADING_1);

 Assert.assertTrue(builder.getParagraphFormat().isHeading());

 builder.writeln("Heading 1");

 builder.getParagraphFormat().setStyleIdentifier(StyleIdentifier.HEADING_2);

 builder.writeln("Heading 1.1");
 builder.writeln("Heading 1.2");

 builder.getParagraphFormat().setStyleIdentifier(StyleIdentifier.HEADING_3);

 builder.writeln("Heading 1.2.1");
 builder.writeln("Heading 1.2.2");

 builder.getParagraphFormat().setStyleIdentifier(StyleIdentifier.HEADING_4);

 builder.writeln("Heading 1.2.2.1");
 builder.writeln("Heading 1.2.2.2");

 builder.getParagraphFormat().setStyleIdentifier(StyleIdentifier.HEADING_5);

 builder.writeln("Heading 1.2.2.2.1");
 builder.writeln("Heading 1.2.2.2.2");

 // Create a "PdfSaveOptions" object that we can pass to the document's "Save" method
 // to modify how that method converts the document to .PDF.
 PdfSaveOptions options = new PdfSaveOptions();

 // The output PDF document will contain an outline, which is a table of contents that lists headings in the document body.
 // Clicking on an entry in this outline will take us to the location of its respective heading.
 // Set the "HeadingsOutlineLevels" property to "4" to exclude all headings whose levels are above 4 from the outline.
 options.getOutlineOptions().setHeadingsOutlineLevels(4);

 // If an outline entry has subsequent entries of a higher level inbetween itself and the next entry of the same or lower level,
 // an arrow will appear to the left of the entry. This entry is the "owner" of several such "sub-entries".
 // In our document, the outline entries from the 5th heading level are sub-entries of the second 4th level outline entry,
 // the 4th and 5th heading level entries are sub-entries of the second 3rd level entry, and so on.
 // In the outline, we can click on the arrow of the "owner" entry to collapse/expand all its sub-entries.
 // Set the "ExpandedOutlineLevels" property to "2" to automatically expand all heading level 2 and lower outline entries
 // and collapse all level and 3 and higher entries when we open the document.
 options.getOutlineOptions().setExpandedOutlineLevels(2);

 doc.save(getArtifactsDir() + "PdfSaveOptions.ExpandedOutlineLevels.pdf", options);
 
```

**Parameters:**
| Parámetro | Tipo | Descripción |
| --- | --- | --- |
| valor | int | El valor  int  correspondiente. |

