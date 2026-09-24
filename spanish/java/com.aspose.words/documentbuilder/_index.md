---
title: "DocumentBuilder"
linktitle: "DocumentBuilder"
second_title: "Aspose.Words para Java"
description: "Proporciona métodos para insertar texto, imágenes y otro contenido, y especificar el formato de fuente, párrafo y sección en Java."
type: docs
weight: 163
url: /es/java/com.aspose.words/documentbuilder/
---

**Inheritance:**
java.lang.Object
```
public class DocumentBuilder
```

Proporciona métodos para insertar texto, imágenes y otro contenido, especificar la fuente, el formato de párrafo y de sección.

Para obtener más información, visite el artículo de documentación [ Document Builder Overview ][Document Builder Overview].

 **Remarks:** 

[DocumentBuilder](../../com.aspose.words/documentbuilder/) makes the process of building a [Document](../../com.aspose.words/document/) easier. [Document](../../com.aspose.words/document/) is a composite object consisting of a tree of nodes and while inserting content nodes directly into the tree is possible, it requires good understanding of the tree structure. [DocumentBuilder](../../com.aspose.words/documentbuilder/) is a "facade" for the complex structure of [Document](../../com.aspose.words/document/) and allows to insert content and formatting quickly and easily.

Cree un [DocumentBuilder](../../com.aspose.words/documentbuilder/) y asócielo con un [Document](../../com.aspose.words/document/).

El [DocumentBuilder](../../com.aspose.words/documentbuilder/) tiene un cursor interno donde se insertará el texto cuando llame a [write(java.lang.String)](../../com.aspose.words/documentbuilder/\#write-java.lang.String), [writeln(java.lang.String)](../../com.aspose.words/documentbuilder/\#writeln-java.lang.String), **M:Aspose.Words.DocumentBuilder.InsertBreak(Aspose.Words.BreakType)** y otros métodos. Puede navegar el cursor del [DocumentBuilder](../../com.aspose.words/documentbuilder/) a una ubicación diferente en un documento usando varios métodos MoveToXXX.

Utilice la propiedad [getFont()](../../com.aspose.words/documentbuilder/\#getFont) para especificar el formato de caracteres que se aplicará a todo el texto insertado desde la posición actual en el documento en adelante.

Utilice la propiedad [getParagraphFormat()](../../com.aspose.words/documentbuilder/\#getParagraphFormat) para especificar el formato de párrafo para el actual y todos los párrafos que se insertarán.

Utilice la propiedad [getPageSetup()](../../com.aspose.words/documentbuilder/\#getPageSetup) para especificar las propiedades de página y sección para la sección actual y todas las secciones que se insertarán.

Utilice las propiedades [getCellFormat()](../../com.aspose.words/documentbuilder/\#getCellFormat) y [getRowFormat()](../../com.aspose.words/documentbuilder/\#getRowFormat) para especificar las propiedades de formato para celdas y filas de tabla. Utilice los métodos [insertCell()](../../com.aspose.words/documentbuilder/\#insertCell) y [endRow()](../../com.aspose.words/documentbuilder/\#endRow) para crear una tabla.

Tenga en cuenta que las propiedades [getFont()](../../com.aspose.words/documentbuilder/\#getFont), [getParagraphFormat()](../../com.aspose.words/documentbuilder/\#getParagraphFormat) y [getPageSetup()](../../com.aspose.words/documentbuilder/\#getPageSetup) se actualizan siempre que navegue a un lugar diferente en el documento para reflejar las propiedades de formato disponibles en la nueva ubicación.

 **Examples:** 

Muestra cómo crear encabezados y pies de página en un documento usando DocumentBuilder.

```

 Document doc = new Document();
 DocumentBuilder builder = new DocumentBuilder(doc);

 // Specify that we want different headers and footers for first, even and odd pages.
 builder.getPageSetup().setDifferentFirstPageHeaderFooter(true);
 builder.getPageSetup().setOddAndEvenPagesHeaderFooter(true);

 // Create the headers, then add three pages to the document to display each header type.
 builder.moveToHeaderFooter(HeaderFooterType.HEADER_FIRST);
 builder.write("Header for the first page");
 builder.moveToHeaderFooter(HeaderFooterType.HEADER_EVEN);
 builder.write("Header for even pages");
 builder.moveToHeaderFooter(HeaderFooterType.HEADER_PRIMARY);
 builder.write("Header for all other pages");

 builder.moveToSection(0);
 builder.writeln("Page1");
 builder.insertBreak(BreakType.PAGE_BREAK);
 builder.writeln("Page2");
 builder.insertBreak(BreakType.PAGE_BREAK);
 builder.writeln("Page3");

 doc.save(getArtifactsDir() + "DocumentBuilder.HeadersAndFooters.docx");
 
```

Muestra cómo crear una tabla con bordes personalizados.

```

 Document doc = new Document();
 DocumentBuilder builder = new DocumentBuilder(doc);

 builder.startTable();

 // Setting table formatting options for a document builder
 // will apply them to every row and cell that we add with it.
 builder.getParagraphFormat().setAlignment(ParagraphAlignment.CENTER);

 builder.getCellFormat().clearFormatting();
 builder.getCellFormat().setWidth(150.0);
 builder.getCellFormat().setVerticalAlignment(CellVerticalAlignment.CENTER);
 builder.getCellFormat().getShading().setBackgroundPatternColor(Color.GREEN);
 builder.getCellFormat().setWrapText(false);
 builder.getCellFormat().setFitText(true);

 builder.getRowFormat().clearFormatting();
 builder.getRowFormat().setHeightRule(HeightRule.EXACTLY);
 builder.getRowFormat().setHeight(50.0);
 builder.getRowFormat().getBorders().setLineStyle(LineStyle.ENGRAVE_3_D);
 builder.getRowFormat().getBorders().setColor(Color.ORANGE);

 builder.insertCell();
 builder.write("Row 1, Col 1");

 builder.insertCell();
 builder.write("Row 1, Col 2");
 builder.endRow();

 // Changing the formatting will apply it to the current cell,
 // and any new cells that we create with the builder afterward.
 // This will not affect the cells that we have added previously.
 builder.getCellFormat().getShading().clearFormatting();

 builder.insertCell();
 builder.write("Row 2, Col 1");

 builder.insertCell();
 builder.write("Row 2, Col 2");

 builder.endRow();

 // Increase row height to fit the vertical text.
 builder.insertCell();
 builder.getRowFormat().setHeight(150.0);
 builder.getCellFormat().setOrientation(TextOrientation.UPWARD);
 builder.write("Row 3, Col 1");

 builder.insertCell();
 builder.getCellFormat().setOrientation(TextOrientation.DOWNWARD);
 builder.write("Row 3, Col 2");

 builder.endRow();
 builder.endTable();

 doc.save(getArtifactsDir() + "DocumentBuilder.InsertTable.docx");
 
```

Muestra cómo usar un DocumentBuilder para crear una tabla.

```

 Document doc = new Document();
 DocumentBuilder builder = new DocumentBuilder(doc);

 // Start the table, then populate the first row with two cells.
 builder.startTable();
 builder.insertCell();
 builder.write("Row 1, Cell 1.");
 builder.insertCell();
 builder.write("Row 1, Cell 2.");

 // Call the builder's "EndRow" method to start a new row.
 builder.endRow();
 builder.insertCell();
 builder.write("Row 2, Cell 1.");
 builder.insertCell();
 builder.write("Row 2, Cell 2.");
 builder.endTable();

 doc.save(getArtifactsDir() + "DocumentBuilder.CreateTable.docx");
 
```


[Document Builder Overview]: https://docs.aspose.com/words/java/document-builder-overview/
## Constructores

| Constructor | Descripción |
| --- | --- |
| [DocumentBuilder()](#DocumentBuilder) | Inicializa una nueva instancia de esta clase. |
| [DocumentBuilder(DocumentBuilderOptions options)](#DocumentBuilder-com.aspose.words.DocumentBuilderOptions) | Inicializa una nueva instancia de esta clase. |
| [DocumentBuilder(Document doc)](#DocumentBuilder-com.aspose.words.Document) | Inicializa una nueva instancia de esta clase. |
| [DocumentBuilder(Document doc, DocumentBuilderOptions options)](#DocumentBuilder-com.aspose.words.Document-com.aspose.words.DocumentBuilderOptions) | Inicializa una nueva instancia de esta clase. |
## Métodos

| Método | Descripción |
| --- | --- |
| [clearCellAttrs()](#clearCellAttrs) |  |
| [clearParaAttrs()](#clearParaAttrs) |  |
| [clearRowAttrs()](#clearRowAttrs) |  |
| [clearRunAttrs()](#clearRunAttrs) |  |
| [deleteRow(int tableIndex, int rowIndex)](#deleteRow-int-int) | Elimina una fila de una tabla. |
| [endBookmark(String bookmarkName)](#endBookmark-java.lang.String) | Marca la posición actual en el documento como el final de un marcador. |
| [endColumnBookmark(String bookmarkName)](#endColumnBookmark-java.lang.String) | Marca la posición actual en el documento como el final de un marcador de columna. |
| [endEditableRange()](#endEditableRange) | Marca la posición actual en el documento como el final de un rango editable. |
| [endEditableRange(EditableRangeStart start)](#endEditableRange-com.aspose.words.EditableRangeStart) | Marca la posición actual en el documento como el final de un rango editable. |
| [endRow()](#endRow) | Finaliza una fila de tabla en el documento. |
| [endTable()](#endTable) | Finaliza una tabla en el documento. |
| [fetchCellAttr(int key)](#fetchCellAttr-int) |  |
| [fetchInheritedCellAttr(int key)](#fetchInheritedCellAttr-int) |  |
| [fetchInheritedParaAttr(int key)](#fetchInheritedParaAttr-int) |  |
| [fetchInheritedRowAttr(int key)](#fetchInheritedRowAttr-int) |  |
| [fetchInheritedRunAttr(int fontAttr)](#fetchInheritedRunAttr-int) |  |
| [fetchParaAttr(int key)](#fetchParaAttr-int) |  |
| [fetchRowAttr(int key)](#fetchRowAttr-int) |  |
| [getBold()](#getBold) | True si la fuente está formateada en negrita. |
| [getCellFormat()](#getCellFormat) | Devuelve un objeto que representa las propiedades de formato de la celda de tabla actual. |
| [getCurrentNode()](#getCurrentNode) | Obtiene el nodo que está actualmente seleccionado en este DocumentBuilder. |
| [getCurrentParagraph()](#getCurrentParagraph) | Obtiene el párrafo que está actualmente seleccionado en este [DocumentBuilder](../../com.aspose.words/documentbuilder/). |
| [getCurrentSection()](#getCurrentSection) | Obtiene la sección que está actualmente seleccionada en este [DocumentBuilder](../../com.aspose.words/documentbuilder/). |
| [getCurrentStory()](#getCurrentStory) | Obtiene la historia que está actualmente seleccionada en este [DocumentBuilder](../../com.aspose.words/documentbuilder/). |
| [getCurrentStructuredDocumentTag()](#getCurrentStructuredDocumentTag) | Obtiene la etiqueta de documento estructurado que está actualmente seleccionada en este [DocumentBuilder](../../com.aspose.words/documentbuilder/). |
| [getDirectCellAttr(int key)](#getDirectCellAttr-int) |  |
| [getDirectParaAttr(int key)](#getDirectParaAttr-int) |  |
| [getDirectParaAttr(int key, int revisionsView)](#getDirectParaAttr-int-int) |  |
| [getDirectRowAttr(int key)](#getDirectRowAttr-int) |  |
| [getDirectRunAttr(int fontAttr)](#getDirectRunAttr-int) |  |
| [getDirectRunAttr(int key, int revisionsView)](#getDirectRunAttr-int-int) |  |
| [getDocument()](#getDocument) | Obtiene el objeto [getDocument()](../../com.aspose.words/documentbuilder/\#getDocument) / [setDocument(com.aspose.words.Document)](../../com.aspose.words/documentbuilder/\#setDocument-com.aspose.words.Document) al que está adjunto este objeto. |
| [getFont()](#getFont) | Devuelve un objeto que representa las propiedades de formato de fuente actuales. |
| [getItalic()](#getItalic) | Verdadero si la fuente está formateada en cursiva. |
| [getListFormat()](#getListFormat) | Devuelve un objeto que representa las propiedades de formato de lista actuales. |
| [getPageSetup()](#getPageSetup) | Devuelve un objeto que representa la configuración de página y las propiedades de sección actuales. |
| [getParagraphFormat()](#getParagraphFormat) | Devuelve un objeto que representa las propiedades de formato de párrafo actuales. |
| [getRowFormat()](#getRowFormat) | Devuelve un objeto que representa las propiedades de formato de fila de tabla actuales. |
| [getUnderline()](#getUnderline) | Obtiene/establece el tipo de subrayado para la fuente actual. |
| [insertBreak(int breakType)](#insertBreak-int) |  |
| [insertCell()](#insertCell) | Inserta una celda de tabla en el documento. |
| [insertChart(int chartType, double width, double height)](#insertChart-int-double-double) |  |
| [insertChart(int chartType, double width, double height, int chartStyle)](#insertChart-int-double-double-int) |  |
| [insertChart(int chartType, int horzPos, double left, int vertPos, double top, double width, double height, int wrapType)](#insertChart-int-int-double-int-double-double-double-int) |  |
| [insertChart(int chartType, int horzPos, double left, int vertPos, double top, double width, double height, int wrapType, int chartStyle)](#insertChart-int-int-double-int-double-double-double-int-int) |  |
| [insertCheckBox(String name, boolean defaultValue, boolean checkedValue, int size)](#insertCheckBox-java.lang.String-boolean-boolean-int) | Inserta un campo de formulario de casilla de verificación en la posición actual. |
| [insertCheckBox(String name, boolean checkedValue, int size)](#insertCheckBox-java.lang.String-boolean-int) | Inserta un campo de formulario de casilla de verificación en la posición actual. |
| [insertComboBox(String name, String[] items, int selectedIndex)](#insertComboBox-java.lang.String-java.lang.String---int) | Inserta un campo de formulario de cuadro combinado en la posición actual. |
| [insertDocument(Document srcDoc, int importFormatMode)](#insertDocument-com.aspose.words.Document-int) |  |
| [insertDocument(Document srcDoc, int importFormatMode, ImportFormatOptions importFormatOptions)](#insertDocument-com.aspose.words.Document-int-com.aspose.words.ImportFormatOptions) |  |
| [insertDocumentInline(Document srcDoc, int importFormatMode, ImportFormatOptions importFormatOptions)](#insertDocumentInline-com.aspose.words.Document-int-com.aspose.words.ImportFormatOptions) |  |
| [insertField(int fieldType, boolean updateField)](#insertField-int-boolean) |  |
| [insertField(String fieldCode)](#insertField-java.lang.String) | Inserta un campo de Word en un documento y actualiza el resultado del campo. |
| [insertField(String fieldCode, String fieldValue)](#insertField-java.lang.String-java.lang.String) | Inserta un campo de Word en un documento sin actualizar el resultado del campo. |
| [insertFootnote(int footnoteType, String footnoteText)](#insertFootnote-int-java.lang.String) |  |
| [insertFootnote(int footnoteType, String footnoteText, String referenceMark)](#insertFootnote-int-java.lang.String-java.lang.String) |  |
| [insertForms2OleControl(Forms2OleControl forms2OleControl)](#insertForms2OleControl-com.aspose.words.Forms2OleControl) | Inserta el objeto [Forms2OleControl](../../com.aspose.words/forms2olecontrol/) en la posición actual. |
| [insertGroupShape(ShapeBase[] shapes)](#insertGroupShape-com.aspose.words.ShapeBase...) | Agrupa las formas pasadas como parámetro en un nuevo nodo GroupShape que se inserta en la posición actual. |
| [insertGroupShape(double left, double top, double width, double height, ShapeBase[] shapes)](#insertGroupShape-double-double-double-double-com.aspose.words.ShapeBase...) | Agrupa las formas pasadas como parámetro en un nuevo nodo GroupShape del tamaño especificado que se inserta en la posición especificada. |
| [insertHorizontalRule()](#insertHorizontalRule) | Inserta una forma de regla horizontal en el documento. |
| [insertHtml(String html)](#insertHtml-java.lang.String) | Inserta una cadena HTML en el documento. |
| [insertHtml(String html, boolean useBuilderFormatting)](#insertHtml-java.lang.String-boolean) | Inserta una cadena HTML en el documento. |
| [insertHtml(String html, int options)](#insertHtml-java.lang.String-int) |  |
| [insertHyperlink(String displayText, String urlOrBookmark, boolean isBookmark)](#insertHyperlink-java.lang.String-java.lang.String-boolean) | Inserta un hipervínculo en el documento. |
| [insertImage(byte[] imageBytes)](#insertImage-byte) | Inserta una imagen desde una matriz de bytes en el documento. |
| [insertImage(byte[] imageBytes, double width, double height)](#insertImage-byte---double-double) | Inserta una imagen en línea desde una matriz de bytes en el documento y la escala al tamaño especificado. |
| [insertImage(byte[] imageBytes, int horzPos, double left, int vertPos, double top, double width, double height, int wrapType)](#insertImage-byte---int-double-int-double-double-double-int) |  |
| [insertImage(BufferedImage image)](#insertImage-java.awt.image.BufferedImage) | Inserta una imagen en el documento. |
| [insertImage(BufferedImage image, double width, double height)](#insertImage-java.awt.image.BufferedImage-double-double) | Inserta una imagen en línea desde un objeto java.awt.image.BufferedImage en el documento y la escala al tamaño especificado. |
| [insertImage(BufferedImage image, int horzPos, double left, int vertPos, double top, double width, double height, int wrapType)](#insertImage-java.awt.image.BufferedImage-int-double-int-double-double-double-int) |  |
| [insertImage(InputStream stream)](#insertImage-java.io.InputStream) |  |
| [insertImage(InputStream stream, double width, double height)](#insertImage-java.io.InputStream-double-double) |  |
| [insertImage(InputStream stream, int horzPos, double left, int vertPos, double top, double width, double height, int wrapType)](#insertImage-java.io.InputStream-int-double-int-double-double-double-int) |  |
| [insertImage(String fileName)](#insertImage-java.lang.String) | Inserta una imagen desde un archivo o URL en el documento. |
| [insertImage(String fileName, double width, double height)](#insertImage-java.lang.String-double-double) | Inserta una imagen en línea desde un archivo o URL en el documento y la escala al tamaño especificado. |
| [insertImage(String fileName, int horzPos, double left, int vertPos, double top, double width, double height, int wrapType)](#insertImage-java.lang.String-int-double-int-double-double-double-int) |  |
| [insertNode(Node node)](#insertNode-com.aspose.words.Node) | Inserta un nodo antes del cursor. |
| [insertOleObject(InputStream stream, String progId, boolean asIcon, InputStream presentation)](#insertOleObject-java.io.InputStream-java.lang.String-boolean-java.io.InputStream) |  |
| [insertOleObject(String fileName, boolean isLinked, boolean asIcon, InputStream presentation)](#insertOleObject-java.lang.String-boolean-boolean-java.io.InputStream) |  |
| [insertOleObject(String fileName, String progId, boolean isLinked, boolean asIcon, InputStream presentation)](#insertOleObject-java.lang.String-java.lang.String-boolean-boolean-java.io.InputStream) |  |
| [insertOleObjectAsIcon(InputStream stream, String progId, String iconFile, String iconCaption)](#insertOleObjectAsIcon-java.io.InputStream-java.lang.String-java.lang.String-java.lang.String) |  |
| [insertOleObjectAsIcon(String fileName, boolean isLinked, String iconFile, String iconCaption)](#insertOleObjectAsIcon-java.lang.String-boolean-java.lang.String-java.lang.String) | Inserta un objeto OLE incrustado o vinculado como ícono en el documento. |
| [insertOleObjectAsIcon(String fileName, String progId, boolean isLinked, String iconFile, String iconCaption)](#insertOleObjectAsIcon-java.lang.String-java.lang.String-boolean-java.lang.String-java.lang.String) | Inserta un objeto OLE incrustado o vinculado como ícono en el documento. |
| [insertOnlineVideo(String videoUrl, double width, double height)](#insertOnlineVideo-java.lang.String-double-double) | Inserta un objeto de video en línea en el documento y lo escala al tamaño especificado. |
| [insertOnlineVideo(String videoUrl, int horzPos, double left, int vertPos, double top, double width, double height, int wrapType)](#insertOnlineVideo-java.lang.String-int-double-int-double-double-double-int) |  |
| [insertOnlineVideo(String videoUrl, String videoEmbedCode, byte[] thumbnailImageBytes, double width, double height)](#insertOnlineVideo-java.lang.String-java.lang.String-byte---double-double) | Inserta un objeto de video en línea en el documento y lo escala al tamaño especificado. |
| [insertOnlineVideo(String videoUrl, String videoEmbedCode, byte[] thumbnailImageBytes, int horzPos, double left, int vertPos, double top, double width, double height, int wrapType)](#insertOnlineVideo-java.lang.String-java.lang.String-byte---int-double-int-double-double-double-int) |  |
| [insertParagraph()](#insertParagraph) | Inserta un salto de párrafo en el documento. |
| [insertShape(int shapeType, double width, double height)](#insertShape-int-double-double) |  |
| [insertShape(int shapeType, int horzPos, double left, int vertPos, double top, double width, double height, int wrapType)](#insertShape-int-int-double-int-double-double-double-int) |  |
| [insertSignatureLine(SignatureLineOptions signatureLineOptions)](#insertSignatureLine-com.aspose.words.SignatureLineOptions) | Inserta una línea de firma en la posición actual. |
| [insertSignatureLine(SignatureLineOptions signatureLineOptions, int horzPos, double left, int vertPos, double top, int wrapType)](#insertSignatureLine-com.aspose.words.SignatureLineOptions-int-double-int-double-int) |  |
| [insertStructuredDocumentTag(int type)](#insertStructuredDocumentTag-int) |  |
| [insertStyleSeparator()](#insertStyleSeparator) | Inserta un separador de estilo en el documento. |
| [insertTableOfContents(String switches)](#insertTableOfContents-java.lang.String) | Inserta un campo TOC (tabla de contenido) en el documento. |
| [insertTextInput(String name, int type, String format, String fieldValue, int maxLength)](#insertTextInput-java.lang.String-int-java.lang.String-java.lang.String-int) |  |
| [isAtEndOfParagraph()](#isAtEndOfParagraph) | Devuelve  true  si el cursor está al final del párrafo actual. |
| [isAtEndOfStructuredDocumentTag()](#isAtEndOfStructuredDocumentTag) | Devuelve **true** si el cursor está al final de una etiqueta de documento estructurado. |
| [isAtStartOfParagraph()](#isAtStartOfParagraph) | Devuelve  true  si el cursor está al comienzo del párrafo actual (no hay texto antes del cursor). |
| [moveTo(Node node)](#moveTo-com.aspose.words.Node) | Mueve el cursor a un nodo en línea o al final de un párrafo. |
| [moveToBookmark(String bookmarkName)](#moveToBookmark-java.lang.String) | Mueve el cursor a un marcador. |
| [moveToBookmark(String bookmarkName, boolean isStart, boolean isAfter)](#moveToBookmark-java.lang.String-boolean-boolean) | Mueve el cursor a un marcador con mayor precisión. |
| [moveToCell(int tableIndex, int rowIndex, int columnIndex, int characterIndex)](#moveToCell-int-int-int-int) | Mueve el cursor a una celda de tabla en la sección actual. |
| [moveToDocumentEnd()](#moveToDocumentEnd) | Mueve el cursor al final del documento. |
| [moveToDocumentStart()](#moveToDocumentStart) | Mueve el cursor al comienzo del documento. |
| [moveToField(Field field, boolean isAfter)](#moveToField-com.aspose.words.Field-boolean) | Mueve el cursor a un campo en el documento. |
| [moveToHeaderFooter(int headerFooterType)](#moveToHeaderFooter-int) |  |
| [moveToMergeField(String fieldName)](#moveToMergeField-java.lang.String) | Mueve el cursor al campo de combinación especificado. |
| [moveToMergeField(String fieldName, boolean isAfter, boolean isDeleteField)](#moveToMergeField-java.lang.String-boolean-boolean) | Mueve el campo de combinación al campo de combinación especificado. |
| [moveToParagraph(int paragraphIndex, int characterIndex)](#moveToParagraph-int-int) | Mueve el cursor a un párrafo en la sección actual. |
| [moveToSection(int sectionIndex)](#moveToSection-int) | Mueve el cursor al comienzo del cuerpo en una sección especificada. |
| [moveToStructuredDocumentTag(StructuredDocumentTag structuredDocumentTag, int characterIndex)](#moveToStructuredDocumentTag-com.aspose.words.StructuredDocumentTag-int) | Mueve el cursor a la etiqueta de documento estructurado. |
| [moveToStructuredDocumentTag(int structuredDocumentTagIndex, int characterIndex)](#moveToStructuredDocumentTag-int-int) | Mueve el cursor a una etiqueta de documento estructurado en la sección actual. |
| [popFont()](#popFont) | Recupera el formato de carácter previamente guardado en la pila. |
| [pushFont()](#pushFont) | Guarda el formato de carácter actual en la pila. |
| [removeParaAttr(int key)](#removeParaAttr-int) |  |
| [removeRunAttr(int key)](#removeRunAttr-int) |  |
| [resetToDefaultAttrs()](#resetToDefaultAttrs) |  |
| [setBold(boolean value)](#setBold-boolean) | True si la fuente está formateada en negrita. |
| [setCellAttr(int key, Object value)](#setCellAttr-int-java.lang.Object) |  |
| [setDocument(Document value)](#setDocument-com.aspose.words.Document) | Establece el objeto [getDocument()](../../com.aspose.words/documentbuilder/\#getDocument) / [setDocument(com.aspose.words.Document)](../../com.aspose.words/documentbuilder/\#setDocument-com.aspose.words.Document) al que este objeto está adjunto. |
| [setItalic(boolean value)](#setItalic-boolean) | Verdadero si la fuente está formateada en cursiva. |
| [setParaAttr(int key, Object value)](#setParaAttr-int-java.lang.Object) |  |
| [setRowAttr(int key, Object value)](#setRowAttr-int-java.lang.Object) |  |
| [setRunAttr(int fontAttr, Object value)](#setRunAttr-int-java.lang.Object) |  |
| [setUnderline(int value)](#setUnderline-int) | Obtiene/establece el tipo de subrayado para la fuente actual. |
| [startBookmark(String bookmarkName)](#startBookmark-java.lang.String) | Marca la posición actual en el documento como inicio de marcador. |
| [startColumnBookmark(String bookmarkName)](#startColumnBookmark-java.lang.String) | Marca la posición actual en el documento como inicio de marcador de columna. |
| [startEditableRange()](#startEditableRange) | Marca la posición actual en el documento como inicio de un rango editable. |
| [startTable()](#startTable) | Inicia una tabla en el documento. |
| [write(String text)](#write-java.lang.String) | Inserta una cadena en el documento en la posición de inserción actual. |
| [writeln()](#writeln) | Inserta un salto de párrafo en el documento. |
| [writeln(String text)](#writeln-java.lang.String) | Inserta una cadena y un salto de párrafo en el documento. |
### DocumentBuilder() {#DocumentBuilder}
```
public DocumentBuilder()
```


Inicializa una nueva instancia de esta clase.

 **Remarks:** 

Crea un nuevo objeto [DocumentBuilder](../../com.aspose.words/documentbuilder/) y lo adjunta a un nuevo objeto [Document](../../com.aspose.words/document/).

 **Examples:** 

Muestra cómo insertar texto con formato usando DocumentBuilder.

```

 Document doc = new Document();
 DocumentBuilder builder = new DocumentBuilder(doc);

 // Specify font formatting, then add text.
 Font font = builder.getFont();
 font.setSize(16.0);
 font.setBold(true);
 font.setColor(Color.BLUE);
 font.setName("Courier New");
 font.setUnderline(Underline.DASH);

 builder.write("Hello world!");
 
```

### DocumentBuilder(DocumentBuilderOptions options) {#DocumentBuilder-com.aspose.words.DocumentBuilderOptions}
```
public DocumentBuilder(DocumentBuilderOptions options)
```


Inicializa una nueva instancia de esta clase.

 **Remarks:** 

Crea un nuevo objeto [DocumentBuilder](../../com.aspose.words/documentbuilder/) y lo adjunta a un nuevo objeto [Document](../../com.aspose.words/document/). Se pueden especificar opciones adicionales de construcción del documento.

 **Examples:** 

Muestra cómo ignorar el formato de tabla para el contenido posterior.

```

 Document doc = new Document();
 DocumentBuilderOptions builderOptions = new DocumentBuilderOptions();
 builderOptions.setContextTableFormatting(true);
 DocumentBuilder builder = new DocumentBuilder(doc, builderOptions);

 // Adds content before the table.
 // Default font size is 12.
 builder.writeln("Font size 12 here.");
 builder.startTable();
 builder.insertCell();
 // Changes the font size inside the table.
 builder.getFont().setSize(5.0);
 builder.write("Font size 5 here");
 builder.insertCell();
 builder.write("Font size 5 here");
 builder.endRow();
 builder.endTable();

 // If ContextTableFormatting is true, then table formatting isn't applied to the content after.
 // If ContextTableFormatting is false, then table formatting is applied to the content after.
 builder.writeln("Font size 12 here.");

 doc.save(getArtifactsDir() + "Table.ContextTableFormatting.docx");
 
```

**Parameters:**
| Parámetro | Tipo | Descripción |
| --- | --- | --- |
| options | [DocumentBuilderOptions](../../com.aspose.words/documentbuilderoptions/) |  |

### DocumentBuilder(Document doc) {#DocumentBuilder-com.aspose.words.Document}
```
public DocumentBuilder(Document doc)
```


Inicializa una nueva instancia de esta clase.

 **Remarks:** 

Crea un nuevo objeto [DocumentBuilder](../../com.aspose.words/documentbuilder/), lo adjunta al objeto [Document](../../com.aspose.words/document/) especificado. El cursor se posiciona al comienzo del documento.

 **Examples:** 

Muestra cómo crear encabezados y pies de página en un documento usando DocumentBuilder.

```

 Document doc = new Document();
 DocumentBuilder builder = new DocumentBuilder(doc);

 // Specify that we want different headers and footers for first, even and odd pages.
 builder.getPageSetup().setDifferentFirstPageHeaderFooter(true);
 builder.getPageSetup().setOddAndEvenPagesHeaderFooter(true);

 // Create the headers, then add three pages to the document to display each header type.
 builder.moveToHeaderFooter(HeaderFooterType.HEADER_FIRST);
 builder.write("Header for the first page");
 builder.moveToHeaderFooter(HeaderFooterType.HEADER_EVEN);
 builder.write("Header for even pages");
 builder.moveToHeaderFooter(HeaderFooterType.HEADER_PRIMARY);
 builder.write("Header for all other pages");

 builder.moveToSection(0);
 builder.writeln("Page1");
 builder.insertBreak(BreakType.PAGE_BREAK);
 builder.writeln("Page2");
 builder.insertBreak(BreakType.PAGE_BREAK);
 builder.writeln("Page3");

 doc.save(getArtifactsDir() + "DocumentBuilder.HeadersAndFooters.docx");
 
```

Muestra cómo insertar una tabla de contenido (TOC) en un documento usando estilos de encabezado como entradas.

```

 Document doc = new Document();
 DocumentBuilder builder = new DocumentBuilder(doc);

 // Insert a table of contents for the first page of the document.
 // Configure the table to pick up paragraphs with headings of levels 1 to 3.
 // Also, set its entries to be hyperlinks that will take us
 // to the location of the heading when left-clicked in Microsoft Word.
 builder.insertTableOfContents("\\o \"1-3\" \\h \\z \\u");
 builder.insertBreak(BreakType.PAGE_BREAK);

 // Populate the table of contents by adding paragraphs with heading styles.
 // Each such heading with a level between 1 and 3 will create an entry in the table.
 builder.getParagraphFormat().setStyleIdentifier(StyleIdentifier.HEADING_1);
 builder.writeln("Heading 1");

 builder.getParagraphFormat().setStyleIdentifier(StyleIdentifier.HEADING_2);
 builder.writeln("Heading 1.1");
 builder.writeln("Heading 1.2");

 builder.getParagraphFormat().setStyleIdentifier(StyleIdentifier.HEADING_1);
 builder.writeln("Heading 2");
 builder.writeln("Heading 3");

 builder.getParagraphFormat().setStyleIdentifier(StyleIdentifier.HEADING_2);
 builder.writeln("Heading 3.1");

 builder.getParagraphFormat().setStyleIdentifier(StyleIdentifier.HEADING_3);
 builder.writeln("Heading 3.1.1");
 builder.writeln("Heading 3.1.2");
 builder.writeln("Heading 3.1.3");

 builder.getParagraphFormat().setStyleIdentifier(StyleIdentifier.HEADING_4);
 builder.writeln("Heading 3.1.3.1");
 builder.writeln("Heading 3.1.3.2");

 builder.getParagraphFormat().setStyleIdentifier(StyleIdentifier.HEADING_2);
 builder.writeln("Heading 3.2");
 builder.writeln("Heading 3.3");

 // A table of contents is a field of a type that needs to be updated to show an up-to-date result.
 doc.updateFields();
 doc.save(getArtifactsDir() + "DocumentBuilder.InsertToc.docx");
 
```

**Parameters:**
| Parámetro | Tipo | Descripción |
| --- | --- | --- |
| doc | [Document](../../com.aspose.words/document/) | El objeto [Document](../../com.aspose.words/document/) al que se adjuntará. |

### DocumentBuilder(Document doc, DocumentBuilderOptions options) {#DocumentBuilder-com.aspose.words.Document-com.aspose.words.DocumentBuilderOptions}
```
public DocumentBuilder(Document doc, DocumentBuilderOptions options)
```


Inicializa una nueva instancia de esta clase.

 **Remarks:** 

Crea un nuevo objeto [DocumentBuilder](../../com.aspose.words/documentbuilder/), lo adjunta al objeto [Document](../../com.aspose.words/document/) especificado. El cursor se posiciona al comienzo del documento.

 **Examples:** 

Muestra cómo ignorar el formato de tabla para el contenido posterior.

```

 Document doc = new Document();
 DocumentBuilderOptions builderOptions = new DocumentBuilderOptions();
 builderOptions.setContextTableFormatting(true);
 DocumentBuilder builder = new DocumentBuilder(doc, builderOptions);

 // Adds content before the table.
 // Default font size is 12.
 builder.writeln("Font size 12 here.");
 builder.startTable();
 builder.insertCell();
 // Changes the font size inside the table.
 builder.getFont().setSize(5.0);
 builder.write("Font size 5 here");
 builder.insertCell();
 builder.write("Font size 5 here");
 builder.endRow();
 builder.endTable();

 // If ContextTableFormatting is true, then table formatting isn't applied to the content after.
 // If ContextTableFormatting is false, then table formatting is applied to the content after.
 builder.writeln("Font size 12 here.");

 doc.save(getArtifactsDir() + "Table.ContextTableFormatting.docx");
 
```

**Parameters:**
| Parámetro | Tipo | Descripción |
| --- | --- | --- |
| doc | [Document](../../com.aspose.words/document/) | El objeto [Document](../../com.aspose.words/document/) al que se adjuntará. |
| options | [DocumentBuilderOptions](../../com.aspose.words/documentbuilderoptions/) | Opciones adicionales para el proceso de construcción del documento. |

### clearCellAttrs() {#clearCellAttrs}
```
public void clearCellAttrs()
```




### clearParaAttrs() {#clearParaAttrs}
```
public void clearParaAttrs()
```




### clearRowAttrs() {#clearRowAttrs}
```
public void clearRowAttrs()
```




### clearRunAttrs() {#clearRunAttrs}
```
public void clearRunAttrs()
```




### deleteRow(int tableIndex, int rowIndex) {#deleteRow-int-int}
```
public Row deleteRow(int tableIndex, int rowIndex)
```


Elimina una fila de una tabla.

 **Remarks:** 

Si el cursor está dentro de la fila que se está eliminando, el cursor se mueve a la siguiente fila o al siguiente párrafo después de la tabla.

Si eliminas una fila de una tabla que contiene solo una fila, se elimina toda la tabla.

Para los parámetros de índice, cuando el índice es mayor o igual a 0, especifica un índice desde el principio, siendo 0 el primer elemento. Cuando el índice es menor que 0, especifica un índice desde el final, siendo -1 el último elemento.

 **Examples:** 

Muestra cómo eliminar una fila de una tabla.

```

 Document doc = new Document();
 DocumentBuilder builder = new DocumentBuilder(doc);

 Table table = builder.startTable();
 builder.insertCell();
 builder.write("Row 1, cell 1.");
 builder.insertCell();
 builder.write("Row 1, cell 2.");
 builder.endRow();
 builder.insertCell();
 builder.write("Row 2, cell 1.");
 builder.insertCell();
 builder.write("Row 2, cell 2.");
 builder.endTable();

 Assert.assertEquals(2, table.getRows().getCount());

 // Delete the first row of the first table in the document.
 builder.deleteRow(0, 0);

 Assert.assertEquals(1, table.getRows().getCount());
 Assert.assertEquals("Row 2, cell 1.Row 2, cell 2.", table.getText().trim());
 
```

**Parameters:**
| Parámetro | Tipo | Descripción |
| --- | --- | --- |
| tableIndex | int | El índice de la tabla. |
| rowIndex | int | El índice de la fila en la tabla. |

**Returns:**
[Row](../../com.aspose.words/row/) - The row node that was just removed.
### endBookmark(String bookmarkName) {#endBookmark-java.lang.String}
```
public BookmarkEnd endBookmark(String bookmarkName)
```


Marca la posición actual en el documento como el final de un marcador.

 **Remarks:** 

Los marcadores en un documento pueden superponerse y abarcar cualquier rango. Para crear un marcador válido, debes llamar tanto a [startBookmark(java.lang.String)](../../com.aspose.words/documentbuilder/\#startBookmark-java.lang.String) como a [endBookmark(java.lang.String)](../../com.aspose.words/documentbuilder/\#endBookmark-java.lang.String) con el mismo  bookmarkName  parámetro.

Los marcadores mal formados o los marcadores con nombres duplicados serán ignorados al guardar el documento.

 **Examples:** 

Muestra cómo crear un marcador.

```

 Document doc = new Document();
 DocumentBuilder builder = new DocumentBuilder(doc);

 // A valid bookmark needs to have document body text enclosed by
 // BookmarkStart and BookmarkEnd nodes created with a matching bookmark name.
 builder.startBookmark("MyBookmark");
 builder.writeln("Hello world!");
 builder.endBookmark("MyBookmark");

 Assert.assertEquals(1, doc.getRange().getBookmarks().getCount());
 Assert.assertEquals("MyBookmark", doc.getRange().getBookmarks().get(0).getName());
 Assert.assertEquals("Hello world!", doc.getRange().getBookmarks().get(0).getText().trim());
 
```

Muestra cómo insertar un hipervínculo que hace referencia a un marcador local.

```

 Document doc = new Document();
 DocumentBuilder builder = new DocumentBuilder(doc);

 builder.startBookmark("Bookmark1");
 builder.write("Bookmarked text. ");
 builder.endBookmark("Bookmark1");
 builder.writeln("Text outside of the bookmark.");

 // Insert a HYPERLINK field that links to the bookmark. We can pass field switches
 // to the "InsertHyperlink" method as part of the argument containing the referenced bookmark's name.
 builder.getFont().setColor(Color.BLUE);
 builder.getFont().setUnderline(Underline.SINGLE);
 FieldHyperlink hyperlink = (FieldHyperlink)builder.insertHyperlink("Link to Bookmark1", "Bookmark1", true);
 hyperlink.setScreenTip("Hyperlink Tip");

 doc.save(getArtifactsDir() + "DocumentBuilder.InsertHyperlinkToLocalBookmark.docx");
 
```

**Parameters:**
| Parámetro | Tipo | Descripción |
| --- | --- | --- |
| bookmarkName | java.lang.String | Nombre del marcador. |

**Returns:**
[BookmarkEnd](../../com.aspose.words/bookmarkend/) - The bookmark end node that was just created.
### endColumnBookmark(String bookmarkName) {#endColumnBookmark-java.lang.String}
```
public BookmarkEnd endColumnBookmark(String bookmarkName)
```


Marca la posición actual en el documento como fin de un marcador de columna. La posición debe estar en una celda de tabla.

 **Remarks:** 

Un marcador de columna cubre una o más columnas en un rango de filas. Para crear un marcador válido, debes llamar tanto a [startColumnBookmark(java.lang.String)](../../com.aspose.words/documentbuilder/\#startColumnBookmark-java.lang.String) como a [endColumnBookmark(java.lang.String)](../../com.aspose.words/documentbuilder/\#endColumnBookmark-java.lang.String) con el mismo  bookmarkName  parámetro.

Los marcadores mal formados o los marcadores con nombres duplicados serán ignorados al guardar el documento.

La posición real del nodo [BookmarkEnd](../../com.aspose.words/bookmarkend/) insertado puede diferir de la posición actual del document builder.

 **Examples:** 

Muestra cómo crear un marcador de columna.

```

 Document doc = new Document();
 DocumentBuilder builder = new DocumentBuilder(doc);

 builder.startTable();

 builder.insertCell();
 // Cells 1,2,4,5 will be bookmarked.
 builder.startColumnBookmark("MyBookmark_1");
 // Badly formed bookmarks or bookmarks with duplicate names will be ignored when the document is saved.
 builder.startColumnBookmark("MyBookmark_1");
 builder.startColumnBookmark("BadStartBookmark");
 builder.write("Cell 1");

 builder.insertCell();
 builder.write("Cell 2");

 builder.insertCell();
 builder.write("Cell 3");

 builder.endRow();

 builder.insertCell();
 builder.write("Cell 4");

 builder.insertCell();
 builder.write("Cell 5");
 builder.endColumnBookmark("MyBookmark_1");
 builder.endColumnBookmark("MyBookmark_1");

 builder.insertCell();
 builder.write("Cell 6");

 builder.endRow();
 builder.endTable();

 doc.save(getArtifactsDir() + "Bookmarks.CreateColumnBookmark.docx");
 
```

**Parameters:**
| Parámetro | Tipo | Descripción |
| --- | --- | --- |
| bookmarkName | java.lang.String | Nombre del marcador. |

**Returns:**
[BookmarkEnd](../../com.aspose.words/bookmarkend/) - The bookmark end node that was just created.
### endEditableRange() {#endEditableRange}
```
public EditableRangeEnd endEditableRange()
```


Marca la posición actual en el documento como el final de un rango editable.

 **Remarks:** 

El rango editable en un documento puede superponerse y abarcar cualquier rango. Para crear un rango editable válido, debe llamar a los métodos [startEditableRange()](../../com.aspose.words/documentbuilder/\#startEditableRange) y [endEditableRange()](../../com.aspose.words/documentbuilder/\#endEditableRange) o [endEditableRange(com.aspose.words.EditableRangeStart)](../../com.aspose.words/documentbuilder/\#endEditableRange-com.aspose.words.EditableRangeStart).

Un rango editable mal formado será ignorado cuando se guarde el documento.

 **Examples:** 

Muestra cómo trabajar con un rango editable.

```

 Document doc = new Document();
 doc.protect(ProtectionType.READ_ONLY, "MyPassword");

 DocumentBuilder builder = new DocumentBuilder(doc);
 builder.writeln("Hello world! Since we have set the document's protection level to read-only," +
         " we cannot edit this paragraph without the password.");

 // Editable ranges allow us to leave parts of protected documents open for editing.
 EditableRangeStart editableRangeStart = builder.startEditableRange();
 builder.writeln("This paragraph is inside an editable range, and can be edited.");
 EditableRangeEnd editableRangeEnd = builder.endEditableRange();

 // A well-formed editable range has a start node, and end node.
 // These nodes have matching IDs and encompass editable nodes.
 EditableRange editableRange = editableRangeStart.getEditableRange();

 Assert.assertEquals(editableRangeStart.getId(), editableRange.getId());
 Assert.assertEquals(editableRangeEnd.getId(), editableRange.getId());

 // Different parts of the editable range link to each other.
 Assert.assertEquals(editableRangeStart.getId(), editableRange.getEditableRangeStart().getId());
 Assert.assertEquals(editableRangeStart.getId(), editableRangeEnd.getEditableRangeStart().getId());
 Assert.assertEquals(editableRange.getId(), editableRangeStart.getEditableRange().getId());
 Assert.assertEquals(editableRangeEnd.getId(), editableRange.getEditableRangeEnd().getId());

 // We can access the node types of each part like this. The editable range itself is not a node,
 // but an entity which consists of a start, an end, and their enclosed contents.
 Assert.assertEquals(NodeType.EDITABLE_RANGE_START, editableRangeStart.getNodeType());
 Assert.assertEquals(NodeType.EDITABLE_RANGE_END, editableRangeEnd.getNodeType());

 builder.writeln("This paragraph is outside the editable range, and cannot be edited.");

 doc.save(getArtifactsDir() + "EditableRange.CreateAndRemove.docx");

 // Remove an editable range. All the nodes that were inside the range will remain intact.
 editableRange.remove();
 
```

**Returns:**
[EditableRangeEnd](../../com.aspose.words/editablerangeend/) - The editable range end node that was just created.
### endEditableRange(EditableRangeStart start) {#endEditableRange-com.aspose.words.EditableRangeStart}
```
public EditableRangeEnd endEditableRange(EditableRangeStart start)
```


Marca la posición actual en el documento como el final de un rango editable.

 **Remarks:** 

Utilice esta sobrecarga al crear rangos editables anidados.

El rango editable en un documento puede superponerse y abarcar cualquier rango. Para crear un rango editable válido, debe llamar a los métodos [startEditableRange()](../../com.aspose.words/documentbuilder/\#startEditableRange) y [endEditableRange()](../../com.aspose.words/documentbuilder/\#endEditableRange) o [endEditableRange(com.aspose.words.EditableRangeStart)](../../com.aspose.words/documentbuilder/\#endEditableRange-com.aspose.words.EditableRangeStart).

Un rango editable mal formado será ignorado cuando se guarde el documento.

 **Examples:** 

Muestra cómo crear rangos editables anidados.

```

 Document doc = new Document();
 doc.protect(ProtectionType.READ_ONLY, "MyPassword");

 DocumentBuilder builder = new DocumentBuilder(doc);
 builder.writeln("Hello world! Since we have set the document's protection level to read-only, " +
         "we cannot edit this paragraph without the password.");

 // Create two nested editable ranges.
 EditableRangeStart outerEditableRangeStart = builder.startEditableRange();
 builder.writeln("This paragraph inside the outer editable range and can be edited.");

 EditableRangeStart innerEditableRangeStart = builder.startEditableRange();
 builder.writeln("This paragraph inside both the outer and inner editable ranges and can be edited.");

 // Currently, the document builder's node insertion cursor is in more than one ongoing editable range.
 // When we want to end an editable range in this situation,
 // we need to specify which of the ranges we wish to end by passing its EditableRangeStart node.
 builder.endEditableRange(innerEditableRangeStart);

 builder.writeln("This paragraph inside the outer editable range and can be edited.");

 builder.endEditableRange(outerEditableRangeStart);

 builder.writeln("This paragraph is outside any editable ranges, and cannot be edited.");

 // If a region of text has two overlapping editable ranges with specified groups,
 // the combined group of users excluded by both groups are prevented from editing it.
 outerEditableRangeStart.getEditableRange().setEditorGroup(EditorType.EVERYONE);
 innerEditableRangeStart.getEditableRange().setEditorGroup(EditorType.CONTRIBUTORS);

 doc.save(getArtifactsDir() + "EditableRange.Nested.docx");
 
```

**Parameters:**
| Parámetro | Tipo | Descripción |
| --- | --- | --- |
| start | [EditableRangeStart](../../com.aspose.words/editablerangestart/) | Este inicio de rango editable. |

**Returns:**
[EditableRangeEnd](../../com.aspose.words/editablerangeend/) - The editable range end node that was just created.
### endRow() {#endRow}
```
public Row endRow()
```


Finaliza una fila de tabla en el documento.

 **Remarks:** 

Llame a [endRow()](../../com.aspose.words/documentbuilder/\#endRow) para terminar una fila de tabla. Si llama a [insertCell()](../../com.aspose.words/documentbuilder/\#insertCell) inmediatamente después, la tabla continuará en una nueva fila.

Utilice la propiedad [getRowFormat()](../../com.aspose.words/documentbuilder/\#getRowFormat) para especificar el formato de la fila.

 **Examples:** 

Muestra cómo combinar celdas de tabla verticalmente.

```

 Document doc = new Document();
 DocumentBuilder builder = new DocumentBuilder(doc);

 // Insert a cell into the first column of the first row.
 // This cell will be the first in a range of vertically merged cells.
 builder.insertCell();
 builder.getCellFormat().setVerticalMerge(CellMerge.FIRST);
 builder.write("Text in merged cells.");

 // Insert a cell into the second column of the first row, then end the row.
 // Also, configure the builder to disable vertical merging in created cells.
 builder.insertCell();
 builder.getCellFormat().setVerticalMerge(CellMerge.NONE);
 builder.write("Text in unmerged cell.");
 builder.endRow();

 // Insert a cell into the first column of the second row.
 // Instead of adding text contents, we will merge this cell with the first cell that we added directly above.
 builder.insertCell();
 builder.getCellFormat().setVerticalMerge(CellMerge.PREVIOUS);

 // Insert another independent cell in the second column of the second row.
 builder.insertCell();
 builder.getCellFormat().setVerticalMerge(CellMerge.NONE);
 builder.write("Text in unmerged cell.");
 builder.endRow();
 builder.endTable();

 doc.save(getArtifactsDir() + "CellFormat.VerticalMerge.docx");
 
```

Muestra cómo crear una tabla con bordes personalizados.

```

 Document doc = new Document();
 DocumentBuilder builder = new DocumentBuilder(doc);

 builder.startTable();

 // Setting table formatting options for a document builder
 // will apply them to every row and cell that we add with it.
 builder.getParagraphFormat().setAlignment(ParagraphAlignment.CENTER);

 builder.getCellFormat().clearFormatting();
 builder.getCellFormat().setWidth(150.0);
 builder.getCellFormat().setVerticalAlignment(CellVerticalAlignment.CENTER);
 builder.getCellFormat().getShading().setBackgroundPatternColor(Color.GREEN);
 builder.getCellFormat().setWrapText(false);
 builder.getCellFormat().setFitText(true);

 builder.getRowFormat().clearFormatting();
 builder.getRowFormat().setHeightRule(HeightRule.EXACTLY);
 builder.getRowFormat().setHeight(50.0);
 builder.getRowFormat().getBorders().setLineStyle(LineStyle.ENGRAVE_3_D);
 builder.getRowFormat().getBorders().setColor(Color.ORANGE);

 builder.insertCell();
 builder.write("Row 1, Col 1");

 builder.insertCell();
 builder.write("Row 1, Col 2");
 builder.endRow();

 // Changing the formatting will apply it to the current cell,
 // and any new cells that we create with the builder afterward.
 // This will not affect the cells that we have added previously.
 builder.getCellFormat().getShading().clearFormatting();

 builder.insertCell();
 builder.write("Row 2, Col 1");

 builder.insertCell();
 builder.write("Row 2, Col 2");

 builder.endRow();

 // Increase row height to fit the vertical text.
 builder.insertCell();
 builder.getRowFormat().setHeight(150.0);
 builder.getCellFormat().setOrientation(TextOrientation.UPWARD);
 builder.write("Row 3, Col 1");

 builder.insertCell();
 builder.getCellFormat().setOrientation(TextOrientation.DOWNWARD);
 builder.write("Row 3, Col 2");

 builder.endRow();
 builder.endTable();

 doc.save(getArtifactsDir() + "DocumentBuilder.InsertTable.docx");
 
```

Muestra cómo crear una tabla formateada de 2x2.

```

 Document doc = new Document();
 DocumentBuilder builder = new DocumentBuilder(doc);

 Table table = builder.startTable();
 builder.insertCell();
 builder.getCellFormat().setVerticalAlignment(CellVerticalAlignment.CENTER);
 builder.write("Row 1, cell 1.");
 builder.insertCell();
 builder.write("Row 1, cell 2.");
 builder.endRow();

 // While building the table, the document builder will apply its current RowFormat/CellFormat property values
 // to the current row/cell that its cursor is in and any new rows/cells as it creates them.
 Assert.assertEquals(CellVerticalAlignment.CENTER, table.getRows().get(0).getCells().get(0).getCellFormat().getVerticalAlignment());
 Assert.assertEquals(CellVerticalAlignment.CENTER, table.getRows().get(0).getCells().get(1).getCellFormat().getVerticalAlignment());

 builder.insertCell();
 builder.getRowFormat().setHeight(100.0);
 builder.getRowFormat().setHeightRule(HeightRule.EXACTLY);
 builder.getCellFormat().setOrientation(TextOrientation.UPWARD);
 builder.write("Row 2, cell 1.");
 builder.insertCell();
 builder.getCellFormat().setOrientation(TextOrientation.DOWNWARD);
 builder.write("Row 2, cell 2.");
 builder.endRow();
 builder.endTable();

 // Previously added rows and cells are not retroactively affected by changes to the builder's formatting.
 Assert.assertEquals(0.0, table.getRows().get(0).getRowFormat().getHeight());
 Assert.assertEquals(HeightRule.AUTO, table.getRows().get(0).getRowFormat().getHeightRule());
 Assert.assertEquals(100.0, table.getRows().get(1).getRowFormat().getHeight());
 Assert.assertEquals(HeightRule.EXACTLY, table.getRows().get(1).getRowFormat().getHeightRule());
 Assert.assertEquals(TextOrientation.UPWARD, table.getRows().get(1).getCells().get(0).getCellFormat().getOrientation());
 Assert.assertEquals(TextOrientation.DOWNWARD, table.getRows().get(1).getCells().get(1).getCellFormat().getOrientation());

 doc.save(getArtifactsDir() + "DocumentBuilder.BuildTable.docx");
 
```

**Returns:**
[Row](../../com.aspose.words/row/) - The row node that was just finished.
### endTable() {#endTable}
```
public Table endTable()
```


Finaliza una tabla en el documento.

 **Remarks:** 

Este método debe llamarse solo una vez después de que se haya llamado a [endRow()](../../com.aspose.words/documentbuilder/\#endRow). Cuando se llama, [endTable()](../../com.aspose.words/documentbuilder/\#endTable) mueve el cursor fuera de la celda actual para situarse justo después de la tabla.

 **Examples:** 

Muestra cómo crear una tabla con bordes personalizados.

```

 Document doc = new Document();
 DocumentBuilder builder = new DocumentBuilder(doc);

 builder.startTable();

 // Setting table formatting options for a document builder
 // will apply them to every row and cell that we add with it.
 builder.getParagraphFormat().setAlignment(ParagraphAlignment.CENTER);

 builder.getCellFormat().clearFormatting();
 builder.getCellFormat().setWidth(150.0);
 builder.getCellFormat().setVerticalAlignment(CellVerticalAlignment.CENTER);
 builder.getCellFormat().getShading().setBackgroundPatternColor(Color.GREEN);
 builder.getCellFormat().setWrapText(false);
 builder.getCellFormat().setFitText(true);

 builder.getRowFormat().clearFormatting();
 builder.getRowFormat().setHeightRule(HeightRule.EXACTLY);
 builder.getRowFormat().setHeight(50.0);
 builder.getRowFormat().getBorders().setLineStyle(LineStyle.ENGRAVE_3_D);
 builder.getRowFormat().getBorders().setColor(Color.ORANGE);

 builder.insertCell();
 builder.write("Row 1, Col 1");

 builder.insertCell();
 builder.write("Row 1, Col 2");
 builder.endRow();

 // Changing the formatting will apply it to the current cell,
 // and any new cells that we create with the builder afterward.
 // This will not affect the cells that we have added previously.
 builder.getCellFormat().getShading().clearFormatting();

 builder.insertCell();
 builder.write("Row 2, Col 1");

 builder.insertCell();
 builder.write("Row 2, Col 2");

 builder.endRow();

 // Increase row height to fit the vertical text.
 builder.insertCell();
 builder.getRowFormat().setHeight(150.0);
 builder.getCellFormat().setOrientation(TextOrientation.UPWARD);
 builder.write("Row 3, Col 1");

 builder.insertCell();
 builder.getCellFormat().setOrientation(TextOrientation.DOWNWARD);
 builder.write("Row 3, Col 2");

 builder.endRow();
 builder.endTable();

 doc.save(getArtifactsDir() + "DocumentBuilder.InsertTable.docx");
 
```

Muestra cómo crear una tabla formateada de 2x2.

```

 Document doc = new Document();
 DocumentBuilder builder = new DocumentBuilder(doc);

 Table table = builder.startTable();
 builder.insertCell();
 builder.getCellFormat().setVerticalAlignment(CellVerticalAlignment.CENTER);
 builder.write("Row 1, cell 1.");
 builder.insertCell();
 builder.write("Row 1, cell 2.");
 builder.endRow();

 // While building the table, the document builder will apply its current RowFormat/CellFormat property values
 // to the current row/cell that its cursor is in and any new rows/cells as it creates them.
 Assert.assertEquals(CellVerticalAlignment.CENTER, table.getRows().get(0).getCells().get(0).getCellFormat().getVerticalAlignment());
 Assert.assertEquals(CellVerticalAlignment.CENTER, table.getRows().get(0).getCells().get(1).getCellFormat().getVerticalAlignment());

 builder.insertCell();
 builder.getRowFormat().setHeight(100.0);
 builder.getRowFormat().setHeightRule(HeightRule.EXACTLY);
 builder.getCellFormat().setOrientation(TextOrientation.UPWARD);
 builder.write("Row 2, cell 1.");
 builder.insertCell();
 builder.getCellFormat().setOrientation(TextOrientation.DOWNWARD);
 builder.write("Row 2, cell 2.");
 builder.endRow();
 builder.endTable();

 // Previously added rows and cells are not retroactively affected by changes to the builder's formatting.
 Assert.assertEquals(0.0, table.getRows().get(0).getRowFormat().getHeight());
 Assert.assertEquals(HeightRule.AUTO, table.getRows().get(0).getRowFormat().getHeightRule());
 Assert.assertEquals(100.0, table.getRows().get(1).getRowFormat().getHeight());
 Assert.assertEquals(HeightRule.EXACTLY, table.getRows().get(1).getRowFormat().getHeightRule());
 Assert.assertEquals(TextOrientation.UPWARD, table.getRows().get(1).getCells().get(0).getCellFormat().getOrientation());
 Assert.assertEquals(TextOrientation.DOWNWARD, table.getRows().get(1).getCells().get(1).getCellFormat().getOrientation());

 doc.save(getArtifactsDir() + "DocumentBuilder.BuildTable.docx");
 
```

Muestra cómo dar formato a las celdas con un document builder.

```

 Document doc = new Document();
 DocumentBuilder builder = new DocumentBuilder(doc);

 Table table = builder.startTable();
 builder.insertCell();
 builder.write("Row 1, cell 1.");

 // Insert a second cell, and then configure cell text padding options.
 // The builder will apply these settings at its current cell, and any new cells creates afterwards.
 builder.insertCell();

 CellFormat cellFormat = builder.getCellFormat();
 cellFormat.setWidth(250.0);
 cellFormat.setLeftPadding(30.0);
 cellFormat.setRightPadding(30.0);
 cellFormat.setTopPadding(30.0);
 cellFormat.setBottomPadding(30.0);

 builder.write("Row 1, cell 2.");
 builder.endRow();
 builder.endTable();

 // The first cell was unaffected by the padding reconfiguration, and still holds the default values.
 Assert.assertEquals(0.0d, table.getFirstRow().getCells().get(0).getCellFormat().getWidth());
 Assert.assertEquals(5.4d, table.getFirstRow().getCells().get(0).getCellFormat().getLeftPadding());
 Assert.assertEquals(5.4d, table.getFirstRow().getCells().get(0).getCellFormat().getRightPadding());
 Assert.assertEquals(0.0d, table.getFirstRow().getCells().get(0).getCellFormat().getTopPadding());
 Assert.assertEquals(0.0d, table.getFirstRow().getCells().get(0).getCellFormat().getBottomPadding());

 Assert.assertEquals(250.0d, table.getFirstRow().getCells().get(1).getCellFormat().getWidth());
 Assert.assertEquals(30.0d, table.getFirstRow().getCells().get(1).getCellFormat().getLeftPadding());
 Assert.assertEquals(30.0d, table.getFirstRow().getCells().get(1).getCellFormat().getRightPadding());
 Assert.assertEquals(30.0d, table.getFirstRow().getCells().get(1).getCellFormat().getTopPadding());
 Assert.assertEquals(30.0d, table.getFirstRow().getCells().get(1).getCellFormat().getBottomPadding());

 // The first cell will still grow in the output document to match the size of its neighboring cell.
 doc.save(getArtifactsDir() + "DocumentBuilder.SetCellFormatting.docx");
 
```

**Returns:**
[Table](../../com.aspose.words/table/) - The table node that was just finished.
### fetchCellAttr(int key) {#fetchCellAttr-int}
```
public Object fetchCellAttr(int key)
```




**Parameters:**
| Parámetro | Tipo | Descripción |
| --- | --- | --- |
| key | int |  |

**Returns:**
java.lang.Object
### fetchInheritedCellAttr(int key) {#fetchInheritedCellAttr-int}
```
public Object fetchInheritedCellAttr(int key)
```




**Parameters:**
| Parámetro | Tipo | Descripción |
| --- | --- | --- |
| key | int |  |

**Returns:**
java.lang.Object
### fetchInheritedParaAttr(int key) {#fetchInheritedParaAttr-int}
```
public Object fetchInheritedParaAttr(int key)
```




**Parameters:**
| Parámetro | Tipo | Descripción |
| --- | --- | --- |
| key | int |  |

**Returns:**
java.lang.Object
### fetchInheritedRowAttr(int key) {#fetchInheritedRowAttr-int}
```
public Object fetchInheritedRowAttr(int key)
```




**Parameters:**
| Parámetro | Tipo | Descripción |
| --- | --- | --- |
| key | int |  |

**Returns:**
java.lang.Object
### fetchInheritedRunAttr(int fontAttr) {#fetchInheritedRunAttr-int}
```
public Object fetchInheritedRunAttr(int fontAttr)
```




**Parameters:**
| Parámetro | Tipo | Descripción |
| --- | --- | --- |
| fontAttr | int |  |

**Returns:**
java.lang.Object
### fetchParaAttr(int key) {#fetchParaAttr-int}
```
public Object fetchParaAttr(int key)
```




**Parameters:**
| Parámetro | Tipo | Descripción |
| --- | --- | --- |
| key | int |  |

**Returns:**
java.lang.Object
### fetchRowAttr(int key) {#fetchRowAttr-int}
```
public Object fetchRowAttr(int key)
```




**Parameters:**
| Parámetro | Tipo | Descripción |
| --- | --- | --- |
| key | int |  |

**Returns:**
java.lang.Object
### getBold() {#getBold}
```
public boolean getBold()
```


True si la fuente está formateada en negrita.

 **Examples:** 

Muestra cómo rellenar MERGEFIELDs con datos usando un document builder en lugar de una combinación de correspondencia.

```

 Document doc = new Document();
 DocumentBuilder builder = new DocumentBuilder(doc);

 // Insert some MERGEFIELDS, which accept data from columns of the same name in a data source during a mail merge,
 // and then fill them manually.
 builder.insertField(" MERGEFIELD Chairman ");
 builder.insertField(" MERGEFIELD ChiefFinancialOfficer ");
 builder.insertField(" MERGEFIELD ChiefTechnologyOfficer ");

 builder.moveToMergeField("Chairman");
 builder.setBold(true);
 builder.writeln("John Doe");

 builder.moveToMergeField("ChiefFinancialOfficer");
 builder.setItalic(true);
 builder.writeln("Jane Doe");

 builder.moveToMergeField("ChiefTechnologyOfficer");
 builder.setItalic(true);
 builder.writeln("John Bloggs");

 doc.save(getArtifactsDir() + "DocumentBuilder.FillMergeFields.docx");
 
```

**Returns:**
boolean - El valor  boolean  correspondiente.
### getCellFormat() {#getCellFormat}
```
public CellFormat getCellFormat()
```


Devuelve un objeto que representa las propiedades de formato de la celda de tabla actual.

 **Examples:** 

Muestra cómo crear una tabla con bordes personalizados.

```

 Document doc = new Document();
 DocumentBuilder builder = new DocumentBuilder(doc);

 builder.startTable();

 // Setting table formatting options for a document builder
 // will apply them to every row and cell that we add with it.
 builder.getParagraphFormat().setAlignment(ParagraphAlignment.CENTER);

 builder.getCellFormat().clearFormatting();
 builder.getCellFormat().setWidth(150.0);
 builder.getCellFormat().setVerticalAlignment(CellVerticalAlignment.CENTER);
 builder.getCellFormat().getShading().setBackgroundPatternColor(Color.GREEN);
 builder.getCellFormat().setWrapText(false);
 builder.getCellFormat().setFitText(true);

 builder.getRowFormat().clearFormatting();
 builder.getRowFormat().setHeightRule(HeightRule.EXACTLY);
 builder.getRowFormat().setHeight(50.0);
 builder.getRowFormat().getBorders().setLineStyle(LineStyle.ENGRAVE_3_D);
 builder.getRowFormat().getBorders().setColor(Color.ORANGE);

 builder.insertCell();
 builder.write("Row 1, Col 1");

 builder.insertCell();
 builder.write("Row 1, Col 2");
 builder.endRow();

 // Changing the formatting will apply it to the current cell,
 // and any new cells that we create with the builder afterward.
 // This will not affect the cells that we have added previously.
 builder.getCellFormat().getShading().clearFormatting();

 builder.insertCell();
 builder.write("Row 2, Col 1");

 builder.insertCell();
 builder.write("Row 2, Col 2");

 builder.endRow();

 // Increase row height to fit the vertical text.
 builder.insertCell();
 builder.getRowFormat().setHeight(150.0);
 builder.getCellFormat().setOrientation(TextOrientation.UPWARD);
 builder.write("Row 3, Col 1");

 builder.insertCell();
 builder.getCellFormat().setOrientation(TextOrientation.DOWNWARD);
 builder.write("Row 3, Col 2");

 builder.endRow();
 builder.endTable();

 doc.save(getArtifactsDir() + "DocumentBuilder.InsertTable.docx");
 
```

Muestra cómo crear una tabla formateada de 2x2.

```

 Document doc = new Document();
 DocumentBuilder builder = new DocumentBuilder(doc);

 Table table = builder.startTable();
 builder.insertCell();
 builder.getCellFormat().setVerticalAlignment(CellVerticalAlignment.CENTER);
 builder.write("Row 1, cell 1.");
 builder.insertCell();
 builder.write("Row 1, cell 2.");
 builder.endRow();

 // While building the table, the document builder will apply its current RowFormat/CellFormat property values
 // to the current row/cell that its cursor is in and any new rows/cells as it creates them.
 Assert.assertEquals(CellVerticalAlignment.CENTER, table.getRows().get(0).getCells().get(0).getCellFormat().getVerticalAlignment());
 Assert.assertEquals(CellVerticalAlignment.CENTER, table.getRows().get(0).getCells().get(1).getCellFormat().getVerticalAlignment());

 builder.insertCell();
 builder.getRowFormat().setHeight(100.0);
 builder.getRowFormat().setHeightRule(HeightRule.EXACTLY);
 builder.getCellFormat().setOrientation(TextOrientation.UPWARD);
 builder.write("Row 2, cell 1.");
 builder.insertCell();
 builder.getCellFormat().setOrientation(TextOrientation.DOWNWARD);
 builder.write("Row 2, cell 2.");
 builder.endRow();
 builder.endTable();

 // Previously added rows and cells are not retroactively affected by changes to the builder's formatting.
 Assert.assertEquals(0.0, table.getRows().get(0).getRowFormat().getHeight());
 Assert.assertEquals(HeightRule.AUTO, table.getRows().get(0).getRowFormat().getHeightRule());
 Assert.assertEquals(100.0, table.getRows().get(1).getRowFormat().getHeight());
 Assert.assertEquals(HeightRule.EXACTLY, table.getRows().get(1).getRowFormat().getHeightRule());
 Assert.assertEquals(TextOrientation.UPWARD, table.getRows().get(1).getCells().get(0).getCellFormat().getOrientation());
 Assert.assertEquals(TextOrientation.DOWNWARD, table.getRows().get(1).getCells().get(1).getCellFormat().getOrientation());

 doc.save(getArtifactsDir() + "DocumentBuilder.BuildTable.docx");
 
```

Muestra cómo dar formato a las celdas con un document builder.

```

 Document doc = new Document();
 DocumentBuilder builder = new DocumentBuilder(doc);

 Table table = builder.startTable();
 builder.insertCell();
 builder.write("Row 1, cell 1.");

 // Insert a second cell, and then configure cell text padding options.
 // The builder will apply these settings at its current cell, and any new cells creates afterwards.
 builder.insertCell();

 CellFormat cellFormat = builder.getCellFormat();
 cellFormat.setWidth(250.0);
 cellFormat.setLeftPadding(30.0);
 cellFormat.setRightPadding(30.0);
 cellFormat.setTopPadding(30.0);
 cellFormat.setBottomPadding(30.0);

 builder.write("Row 1, cell 2.");
 builder.endRow();
 builder.endTable();

 // The first cell was unaffected by the padding reconfiguration, and still holds the default values.
 Assert.assertEquals(0.0d, table.getFirstRow().getCells().get(0).getCellFormat().getWidth());
 Assert.assertEquals(5.4d, table.getFirstRow().getCells().get(0).getCellFormat().getLeftPadding());
 Assert.assertEquals(5.4d, table.getFirstRow().getCells().get(0).getCellFormat().getRightPadding());
 Assert.assertEquals(0.0d, table.getFirstRow().getCells().get(0).getCellFormat().getTopPadding());
 Assert.assertEquals(0.0d, table.getFirstRow().getCells().get(0).getCellFormat().getBottomPadding());

 Assert.assertEquals(250.0d, table.getFirstRow().getCells().get(1).getCellFormat().getWidth());
 Assert.assertEquals(30.0d, table.getFirstRow().getCells().get(1).getCellFormat().getLeftPadding());
 Assert.assertEquals(30.0d, table.getFirstRow().getCells().get(1).getCellFormat().getRightPadding());
 Assert.assertEquals(30.0d, table.getFirstRow().getCells().get(1).getCellFormat().getTopPadding());
 Assert.assertEquals(30.0d, table.getFirstRow().getCells().get(1).getCellFormat().getBottomPadding());

 // The first cell will still grow in the output document to match the size of its neighboring cell.
 doc.save(getArtifactsDir() + "DocumentBuilder.SetCellFormatting.docx");
 
```

**Returns:**
[CellFormat](../../com.aspose.words/cellformat/) - An object that represents current table cell formatting properties.
### getCurrentNode() {#getCurrentNode}
```
public Node getCurrentNode()
```


Obtiene el nodo que está actualmente seleccionado en este DocumentBuilder.

 **Remarks:** 

[getCurrentNode()](../../com.aspose.words/documentbuilder/\#getCurrentNode) is a cursor of [DocumentBuilder](../../com.aspose.words/documentbuilder/) and points to a [Node](../../com.aspose.words/node/) that is a direct child of a [Paragraph](../../com.aspose.words/paragraph/). Any insert operations you perform using [DocumentBuilder](../../com.aspose.words/documentbuilder/) will insert before the [getCurrentNode()](../../com.aspose.words/documentbuilder/\#getCurrentNode).

Cuando el párrafo actual está vacío o el cursor está posicionado justo antes del final de un párrafo o etiqueta de documento estructurado, [getCurrentNode()](../../com.aspose.words/documentbuilder/\#getCurrentNode) devuelve null.

 **Examples:** 

Muestra cómo mover el cursor de un document builder a diferentes nodos en un documento.

```

 Document doc = new Document();
 DocumentBuilder builder = new DocumentBuilder(doc);

 // Create a valid bookmark, an entity that consists of nodes enclosed by a bookmark start node,
 // and a bookmark end node.
 builder.startBookmark("MyBookmark");
 builder.write("Bookmark contents.");
 builder.endBookmark("MyBookmark");

 NodeCollection firstParagraphNodes = doc.getFirstSection().getBody().getFirstParagraph().getChildNodes(NodeType.ANY, false);

 Assert.assertEquals(NodeType.BOOKMARK_START, firstParagraphNodes.get(0).getNodeType());
 Assert.assertEquals(NodeType.RUN, firstParagraphNodes.get(1).getNodeType());
 Assert.assertEquals("Bookmark contents.", firstParagraphNodes.get(1).getText().trim());
 Assert.assertEquals(NodeType.BOOKMARK_END, firstParagraphNodes.get(2).getNodeType());

 // The document builder's cursor is always ahead of the node that we last added with it.
 // If the builder's cursor is at the end of the document, its current node will be null.
 // The previous node is the bookmark end node that we last added.
 // Adding new nodes with the builder will append them to the last node.
 Assert.assertNull(builder.getCurrentNode());

 // If we wish to edit a different part of the document with the builder,
 // we will need to bring its cursor to the node we wish to edit.
 builder.moveToBookmark("MyBookmark");

 // Moving it to a bookmark will move it to the first node within the bookmark start and end nodes, the enclosed run.
 Assert.assertEquals(firstParagraphNodes.get(1), builder.getCurrentNode());

 // We can also move the cursor to an individual node like this.
 builder.moveTo(doc.getFirstSection().getBody().getFirstParagraph().getChildNodes(NodeType.ANY, false).get(0));

 Assert.assertEquals(NodeType.BOOKMARK_START, builder.getCurrentNode().getNodeType());
 Assert.assertEquals(doc.getFirstSection().getBody().getFirstParagraph(), builder.getCurrentParagraph());
 Assert.assertTrue(builder.isAtStartOfParagraph());

 // We can use specific methods to move to the start/end of a document.
 builder.moveToDocumentEnd();

 Assert.assertTrue(builder.isAtEndOfParagraph());

 builder.moveToDocumentStart();

 Assert.assertTrue(builder.isAtStartOfParagraph());
 
```

**Returns:**
[Node](../../com.aspose.words/node/) - The node that is currently selected in this DocumentBuilder.
### getCurrentParagraph() {#getCurrentParagraph}
```
public Paragraph getCurrentParagraph()
```


Obtiene el párrafo que está actualmente seleccionado en este [DocumentBuilder](../../com.aspose.words/documentbuilder/).

 **Remarks:** 

[getCurrentNode()](../../com.aspose.words/documentbuilder/\#getCurrentNode)

 **Examples:** 

Muestra cómo mover el cursor de un document builder a diferentes nodos en un documento.

```

 Document doc = new Document();
 DocumentBuilder builder = new DocumentBuilder(doc);

 // Create a valid bookmark, an entity that consists of nodes enclosed by a bookmark start node,
 // and a bookmark end node.
 builder.startBookmark("MyBookmark");
 builder.write("Bookmark contents.");
 builder.endBookmark("MyBookmark");

 NodeCollection firstParagraphNodes = doc.getFirstSection().getBody().getFirstParagraph().getChildNodes(NodeType.ANY, false);

 Assert.assertEquals(NodeType.BOOKMARK_START, firstParagraphNodes.get(0).getNodeType());
 Assert.assertEquals(NodeType.RUN, firstParagraphNodes.get(1).getNodeType());
 Assert.assertEquals("Bookmark contents.", firstParagraphNodes.get(1).getText().trim());
 Assert.assertEquals(NodeType.BOOKMARK_END, firstParagraphNodes.get(2).getNodeType());

 // The document builder's cursor is always ahead of the node that we last added with it.
 // If the builder's cursor is at the end of the document, its current node will be null.
 // The previous node is the bookmark end node that we last added.
 // Adding new nodes with the builder will append them to the last node.
 Assert.assertNull(builder.getCurrentNode());

 // If we wish to edit a different part of the document with the builder,
 // we will need to bring its cursor to the node we wish to edit.
 builder.moveToBookmark("MyBookmark");

 // Moving it to a bookmark will move it to the first node within the bookmark start and end nodes, the enclosed run.
 Assert.assertEquals(firstParagraphNodes.get(1), builder.getCurrentNode());

 // We can also move the cursor to an individual node like this.
 builder.moveTo(doc.getFirstSection().getBody().getFirstParagraph().getChildNodes(NodeType.ANY, false).get(0));

 Assert.assertEquals(NodeType.BOOKMARK_START, builder.getCurrentNode().getNodeType());
 Assert.assertEquals(doc.getFirstSection().getBody().getFirstParagraph(), builder.getCurrentParagraph());
 Assert.assertTrue(builder.isAtStartOfParagraph());

 // We can use specific methods to move to the start/end of a document.
 builder.moveToDocumentEnd();

 Assert.assertTrue(builder.isAtEndOfParagraph());

 builder.moveToDocumentStart();

 Assert.assertTrue(builder.isAtStartOfParagraph());
 
```

**Returns:**
[Paragraph](../../com.aspose.words/paragraph/) - The paragraph that is currently selected in this [DocumentBuilder](../../com.aspose.words/documentbuilder/).
### getCurrentSection() {#getCurrentSection}
```
public Section getCurrentSection()
```


Obtiene la sección que está actualmente seleccionada en este [DocumentBuilder](../../com.aspose.words/documentbuilder/).

 **Examples:** 

Muestra cómo insertar una imagen flotante y especificar su posición y tamaño.

```

 Document doc = new Document();
 DocumentBuilder builder = new DocumentBuilder(doc);

 Shape shape = builder.insertImage(getImageDir() + "Logo.jpg");
 shape.setWrapType(WrapType.NONE);

 // Configure the shape's "RelativeHorizontalPosition" property to treat the value of the "Left" property
 // as the shape's horizontal distance, in points, from the left side of the page.
 shape.setRelativeHorizontalPosition(RelativeHorizontalPosition.PAGE);

 // Set the shape's horizontal distance from the left side of the page to 100.
 shape.setLeft(100.0);

 // Use the "RelativeVerticalPosition" property in a similar way to position the shape 80pt below the top of the page.
 shape.setRelativeVerticalPosition(RelativeVerticalPosition.PAGE);
 shape.setTop(80.0);

 // Set the shape's height, which will automatically scale the width to preserve dimensions.
 shape.setHeight(125.0);

 Assert.assertEquals(125.0d, shape.getWidth());

 // The "Bottom" and "Right" properties contain the bottom and right edges of the image.
 Assert.assertEquals(shape.getTop() + shape.getHeight(), shape.getBottom());
 Assert.assertEquals(shape.getLeft() + shape.getWidth(), shape.getRight());

 doc.save(getArtifactsDir() + "Image.CreateFloatingPositionSize.docx");
 
```

**Returns:**
[Section](../../com.aspose.words/section/) - The section that is currently selected in this [DocumentBuilder](../../com.aspose.words/documentbuilder/).
### getCurrentStory() {#getCurrentStory}
```
public Story getCurrentStory()
```


Obtiene la historia que está actualmente seleccionada en este [DocumentBuilder](../../com.aspose.words/documentbuilder/).

 **Examples:** 

Muestra cómo trabajar con la historia actual de un document builder.

```

 Document doc = new Document();
 DocumentBuilder builder = new DocumentBuilder(doc);

 // A Story is a type of node that has child Paragraph nodes, such as a Body.
 Assert.assertEquals(builder.getCurrentStory(), doc.getFirstSection().getBody());
 Assert.assertEquals(builder.getCurrentStory(), builder.getCurrentParagraph().getParentNode());
 Assert.assertEquals(StoryType.MAIN_TEXT, builder.getCurrentStory().getStoryType());

 builder.getCurrentStory().appendParagraph("Text added to current Story.");

 // A Story can also contain tables.
 Table table = builder.startTable();
 builder.insertCell();
 builder.write("Row 1, cell 1");
 builder.insertCell();
 builder.write("Row 1, cell 2");
 builder.endTable();

 Assert.assertTrue(builder.getCurrentStory().getTables().contains(table));
 
```

**Returns:**
[Story](../../com.aspose.words/story/) - The story that is currently selected in this [DocumentBuilder](../../com.aspose.words/documentbuilder/).
### getCurrentStructuredDocumentTag() {#getCurrentStructuredDocumentTag}
```
public StructuredDocumentTag getCurrentStructuredDocumentTag()
```


Obtiene la etiqueta de documento estructurado que está actualmente seleccionada en este [DocumentBuilder](../../com.aspose.words/documentbuilder/).

 **Examples:** 

Muestra cómo mover el cursor de DocumentBuilder dentro de una etiqueta de documento estructurado.

```

 Document doc = new Document(getMyDir() + "Structured document tags.docx");
 DocumentBuilder builder = new DocumentBuilder(doc);

 // There is a several ways to move the cursor:
 // 1 -  Move to the first character of structured document tag by index.
 builder.moveToStructuredDocumentTag(1, 1);

 // 2 -  Move to the first character of structured document tag by object.
 StructuredDocumentTag tag = (StructuredDocumentTag)doc.getChild(NodeType.STRUCTURED_DOCUMENT_TAG, 2, true);
 builder.moveToStructuredDocumentTag(tag, 1);
 builder.write(" New text.");

 Assert.assertEquals("R New text.ichText", tag.getText().trim());

 // 3 -  Move to the end of the second structured document tag.
 builder.moveToStructuredDocumentTag(1, -1);
 Assert.assertTrue(builder.isAtEndOfStructuredDocumentTag());

 // Get currently selected structured document tag.
 builder.getCurrentStructuredDocumentTag().setColor(Color.GREEN);

 doc.save(getArtifactsDir() + "Document.MoveToStructuredDocumentTag.docx");
 
```

**Returns:**
[StructuredDocumentTag](../../com.aspose.words/structureddocumenttag/) - The structured document tag that is currently selected in this [DocumentBuilder](../../com.aspose.words/documentbuilder/).
### getDirectCellAttr(int key) {#getDirectCellAttr-int}
```
public Object getDirectCellAttr(int key)
```




**Parameters:**
| Parámetro | Tipo | Descripción |
| --- | --- | --- |
| key | int |  |

**Returns:**
java.lang.Object
### getDirectParaAttr(int key) {#getDirectParaAttr-int}
```
public Object getDirectParaAttr(int key)
```




**Parameters:**
| Parámetro | Tipo | Descripción |
| --- | --- | --- |
| key | int |  |

**Returns:**
java.lang.Object
### getDirectParaAttr(int key, int revisionsView) {#getDirectParaAttr-int-int}
```
public Object getDirectParaAttr(int key, int revisionsView)
```




**Parameters:**
| Parámetro | Tipo | Descripción |
| --- | --- | --- |
| key | int |  |
| revisionsView | int |  |

**Returns:**
java.lang.Object
### getDirectRowAttr(int key) {#getDirectRowAttr-int}
```
public Object getDirectRowAttr(int key)
```




**Parameters:**
| Parámetro | Tipo | Descripción |
| --- | --- | --- |
| key | int |  |

**Returns:**
java.lang.Object
### getDirectRunAttr(int fontAttr) {#getDirectRunAttr-int}
```
public Object getDirectRunAttr(int fontAttr)
```




**Parameters:**
| Parámetro | Tipo | Descripción |
| --- | --- | --- |
| fontAttr | int |  |

**Returns:**
java.lang.Object
### getDirectRunAttr(int key, int revisionsView) {#getDirectRunAttr-int-int}
```
public Object getDirectRunAttr(int key, int revisionsView)
```




**Parameters:**
| Parámetro | Tipo | Descripción |
| --- | --- | --- |
| key | int |  |
| revisionsView | int |  |

**Returns:**
java.lang.Object
### getDocument() {#getDocument}
```
public Document getDocument()
```


Obtiene el objeto [getDocument()](../../com.aspose.words/documentbuilder/\#getDocument) / [setDocument(com.aspose.words.Document)](../../com.aspose.words/documentbuilder/\#setDocument-com.aspose.words.Document) al que está adjunto este objeto.

 **Examples:** 

Muestra cómo aplicar y revertir la configuración de página a secciones en un documento.

```

 Document doc = new Document();
 DocumentBuilder builder = new DocumentBuilder(doc);

 // Modify the page setup properties for the builder's current section and add text.
 builder.getPageSetup().setOrientation(Orientation.LANDSCAPE);
 builder.getPageSetup().setVerticalAlignment(PageVerticalAlignment.CENTER);
 builder.writeln("This is the first section, which landscape oriented with vertically centered text.");

 // If we start a new section using a document builder,
 // it will inherit the builder's current page setup properties.
 builder.insertBreak(BreakType.SECTION_BREAK_NEW_PAGE);

 Assert.assertEquals(Orientation.LANDSCAPE, doc.getSections().get(1).getPageSetup().getOrientation());
 Assert.assertEquals(PageVerticalAlignment.CENTER, doc.getSections().get(1).getPageSetup().getVerticalAlignment());

 // We can revert its page setup properties to their default values using the "ClearFormatting" method.
 builder.getPageSetup().clearFormatting();

 Assert.assertEquals(Orientation.PORTRAIT, doc.getSections().get(1).getPageSetup().getOrientation());
 Assert.assertEquals(PageVerticalAlignment.TOP, doc.getSections().get(1).getPageSetup().getVerticalAlignment());

 builder.writeln("This is the second section, which is in default Letter paper size, portrait orientation and top alignment.");

 doc.save(getArtifactsDir() + "PageSetup.ClearFormatting.docx");
 
```

**Returns:**
[Document](../../com.aspose.words/document/) - The [getDocument()](../../com.aspose.words/documentbuilder/\#getDocument) / [setDocument(com.aspose.words.Document)](../../com.aspose.words/documentbuilder/\#setDocument-com.aspose.words.Document) object that this object is attached to.
### getFont() {#getFont}
```
public Font getFont()
```


Devuelve un objeto que representa las propiedades de formato de fuente actuales.

 **Remarks:** 

Utilice [getFont()](../../com.aspose.words/documentbuilder/\#getFont) para acceder y modificar las propiedades de formato de fuente.

Especifique el formato de fuente antes de insertar texto.

 **Examples:** 

Muestra cómo insertar una cadena rodeada por un borde en un documento.

```

 Document doc = new Document();
 DocumentBuilder builder = new DocumentBuilder(doc);

 builder.getFont().getBorder().setColor(Color.GREEN);
 builder.getFont().getBorder().setLineWidth(2.5);
 builder.getFont().getBorder().setLineStyle(LineStyle.DASH_DOT_STROKER);

 builder.write("Text surrounded by green border.");

 doc.save(getArtifactsDir() + "Border.FontBorder.docx");
 
```

Muestra cómo crear una tabla formateada usando DocumentBuilder.

```

 Document doc = new Document();
 DocumentBuilder builder = new DocumentBuilder(doc);

 Table table = builder.startTable();
 builder.insertCell();
 table.setLeftIndent(20.0);

 // Set some formatting options for text and table appearance.
 builder.getRowFormat().setHeight(40.0);
 builder.getRowFormat().setHeightRule(HeightRule.AT_LEAST);
 builder.getCellFormat().getShading().setBackgroundPatternColor(new Color((198), (217), (241)));

 builder.getParagraphFormat().setAlignment(ParagraphAlignment.CENTER);
 builder.getFont().setSize(16.0);
 builder.getFont().setName("Arial");
 builder.getFont().setBold(true);

 // Configuring the formatting options in a document builder will apply them
 // to the current cell/row its cursor is in,
 // as well as any new cells and rows created using that builder.
 builder.write("Header Row,\n Cell 1");
 builder.insertCell();
 builder.write("Header Row,\n Cell 2");
 builder.insertCell();
 builder.write("Header Row,\n Cell 3");
 builder.endRow();

 // Reconfigure the builder's formatting objects for new rows and cells that we are about to make.
 // The builder will not apply these to the first row already created so that it will stand out as a header row.
 builder.getCellFormat().getShading().setBackgroundPatternColor(Color.WHITE);
 builder.getCellFormat().setVerticalAlignment(CellVerticalAlignment.CENTER);
 builder.getRowFormat().setHeight(30.0);
 builder.getRowFormat().setHeightRule(HeightRule.AUTO);
 builder.insertCell();
 builder.getFont().setSize(12.0);
 builder.getFont().setBold(false);

 builder.write("Row 1, Cell 1.");
 builder.insertCell();
 builder.write("Row 1, Cell 2.");
 builder.insertCell();
 builder.write("Row 1, Cell 3.");
 builder.endRow();
 builder.insertCell();
 builder.write("Row 2, Cell 1.");
 builder.insertCell();
 builder.write("Row 2, Cell 2.");
 builder.insertCell();
 builder.write("Row 2, Cell 3.");
 builder.endRow();
 builder.endTable();

 doc.save(getArtifactsDir() + "DocumentBuilder.CreateFormattedTable.docx");
 
```

**Returns:**
[Font](../../com.aspose.words/font/) - An object that represents current font formatting properties.
### getItalic() {#getItalic}
```
public boolean getItalic()
```


Verdadero si la fuente está formateada en cursiva.

 **Examples:** 

Muestra cómo rellenar MERGEFIELDs con datos usando un document builder en lugar de una combinación de correspondencia.

```

 Document doc = new Document();
 DocumentBuilder builder = new DocumentBuilder(doc);

 // Insert some MERGEFIELDS, which accept data from columns of the same name in a data source during a mail merge,
 // and then fill them manually.
 builder.insertField(" MERGEFIELD Chairman ");
 builder.insertField(" MERGEFIELD ChiefFinancialOfficer ");
 builder.insertField(" MERGEFIELD ChiefTechnologyOfficer ");

 builder.moveToMergeField("Chairman");
 builder.setBold(true);
 builder.writeln("John Doe");

 builder.moveToMergeField("ChiefFinancialOfficer");
 builder.setItalic(true);
 builder.writeln("Jane Doe");

 builder.moveToMergeField("ChiefTechnologyOfficer");
 builder.setItalic(true);
 builder.writeln("John Bloggs");

 doc.save(getArtifactsDir() + "DocumentBuilder.FillMergeFields.docx");
 
```

**Returns:**
boolean - El valor  boolean  correspondiente.
### getListFormat() {#getListFormat}
```
public ListFormat getListFormat()
```


Devuelve un objeto que representa las propiedades de formato de lista actuales.

 **Examples:** 

Muestra cómo crear listas con viñetas y numeradas.

```

 Document doc = new Document();
 DocumentBuilder builder = new DocumentBuilder(doc);

 builder.writeln("Aspose.Words main advantages are:");

 // A list allows us to organize and decorate sets of paragraphs with prefix symbols and indents.
 // We can create nested lists by increasing the indent level.
 // We can begin and end a list by using a document builder's "ListFormat" property.
 // Each paragraph that we add between a list's start and the end will become an item in the list.
 // Below are two types of lists that we can create with a document builder.
 // 1 -  A bulleted list:
 // This list will apply an indent and a bullet symbol ("\u2022") before each paragraph.
 builder.getListFormat().applyBulletDefault();
 builder.writeln("Great performance");
 builder.writeln("High reliability");
 builder.writeln("Quality code and working");
 builder.writeln("Wide variety of features");
 builder.writeln("Easy to understand API");

 // End the bulleted list.
 builder.getListFormat().removeNumbers();

 builder.insertBreak(BreakType.PARAGRAPH_BREAK);
 builder.writeln("Aspose.Words allows:");

 // 2 -  A numbered list:
 // Numbered lists create a logical order for their paragraphs by numbering each item.
 builder.getListFormat().applyNumberDefault();

 // This paragraph is the first item. The first item of a numbered list will have a "1." as its list item symbol.
 builder.writeln("Opening documents from different formats:");

 Assert.assertEquals(0, builder.getListFormat().getListLevelNumber());

 // Call the "ListIndent" method to increase the current list level,
 // which will start a new self-contained list, with a deeper indent, at the current item of the first list level.
 builder.getListFormat().listIndent();

 Assert.assertEquals(1, builder.getListFormat().getListLevelNumber());

 // These are the first three list items of the second list level, which will maintain a count
 // independent of the count of the first list level. According to the current list format,
 // they will have symbols of "a.", "b.", and "c.".
 builder.writeln("DOC");
 builder.writeln("PDF");
 builder.writeln("HTML");

 // Call the "ListOutdent" method to return to the previous list level.
 builder.getListFormat().listOutdent();

 Assert.assertEquals(0, builder.getListFormat().getListLevelNumber());

 // These two paragraphs will continue the count of the first list level.
 // These items will have symbols of "2.", and "3."
 builder.writeln("Processing documents");
 builder.writeln("Saving documents in different formats:");

 // If we increase the list level to a level that we have added items to previously,
 // the nested list will be separate from the previous, and its numbering will start from the beginning.
 // These list items will have symbols of "a.", "b.", "c.", "d.", and "e".
 builder.getListFormat().listIndent();
 builder.writeln("DOC");
 builder.writeln("PDF");
 builder.writeln("HTML");
 builder.writeln("MHTML");
 builder.writeln("Plain text");

 // Outdent the list level again.
 builder.getListFormat().listOutdent();
 builder.writeln("Doing many other things!");

 // End the numbered list.
 builder.getListFormat().removeNumbers();

 doc.save(getArtifactsDir() + "Lists.ApplyDefaultBulletsAndNumbers.docx");
 
```

**Returns:**
[ListFormat](../../com.aspose.words/listformat/) - An object that represents current list formatting properties.
### getPageSetup() {#getPageSetup}
```
public PageSetup getPageSetup()
```


Devuelve un objeto que representa la configuración de página y las propiedades de sección actuales.

 **Examples:** 

Muestra cómo aplicar y revertir la configuración de página a secciones en un documento.

```

 Document doc = new Document();
 DocumentBuilder builder = new DocumentBuilder(doc);

 // Modify the page setup properties for the builder's current section and add text.
 builder.getPageSetup().setOrientation(Orientation.LANDSCAPE);
 builder.getPageSetup().setVerticalAlignment(PageVerticalAlignment.CENTER);
 builder.writeln("This is the first section, which landscape oriented with vertically centered text.");

 // If we start a new section using a document builder,
 // it will inherit the builder's current page setup properties.
 builder.insertBreak(BreakType.SECTION_BREAK_NEW_PAGE);

 Assert.assertEquals(Orientation.LANDSCAPE, doc.getSections().get(1).getPageSetup().getOrientation());
 Assert.assertEquals(PageVerticalAlignment.CENTER, doc.getSections().get(1).getPageSetup().getVerticalAlignment());

 // We can revert its page setup properties to their default values using the "ClearFormatting" method.
 builder.getPageSetup().clearFormatting();

 Assert.assertEquals(Orientation.PORTRAIT, doc.getSections().get(1).getPageSetup().getOrientation());
 Assert.assertEquals(PageVerticalAlignment.TOP, doc.getSections().get(1).getPageSetup().getVerticalAlignment());

 builder.writeln("This is the second section, which is in default Letter paper size, portrait orientation and top alignment.");

 doc.save(getArtifactsDir() + "PageSetup.ClearFormatting.docx");
 
```

**Returns:**
[PageSetup](../../com.aspose.words/pagesetup/) - An object that represents current page setup and section properties.
### getParagraphFormat() {#getParagraphFormat}
```
public ParagraphFormat getParagraphFormat()
```


Devuelve un objeto que representa las propiedades de formato de párrafo actuales.

 **Examples:** 

Muestra cómo crear una tabla formateada usando DocumentBuilder.

```

 Document doc = new Document();
 DocumentBuilder builder = new DocumentBuilder(doc);

 Table table = builder.startTable();
 builder.insertCell();
 table.setLeftIndent(20.0);

 // Set some formatting options for text and table appearance.
 builder.getRowFormat().setHeight(40.0);
 builder.getRowFormat().setHeightRule(HeightRule.AT_LEAST);
 builder.getCellFormat().getShading().setBackgroundPatternColor(new Color((198), (217), (241)));

 builder.getParagraphFormat().setAlignment(ParagraphAlignment.CENTER);
 builder.getFont().setSize(16.0);
 builder.getFont().setName("Arial");
 builder.getFont().setBold(true);

 // Configuring the formatting options in a document builder will apply them
 // to the current cell/row its cursor is in,
 // as well as any new cells and rows created using that builder.
 builder.write("Header Row,\n Cell 1");
 builder.insertCell();
 builder.write("Header Row,\n Cell 2");
 builder.insertCell();
 builder.write("Header Row,\n Cell 3");
 builder.endRow();

 // Reconfigure the builder's formatting objects for new rows and cells that we are about to make.
 // The builder will not apply these to the first row already created so that it will stand out as a header row.
 builder.getCellFormat().getShading().setBackgroundPatternColor(Color.WHITE);
 builder.getCellFormat().setVerticalAlignment(CellVerticalAlignment.CENTER);
 builder.getRowFormat().setHeight(30.0);
 builder.getRowFormat().setHeightRule(HeightRule.AUTO);
 builder.insertCell();
 builder.getFont().setSize(12.0);
 builder.getFont().setBold(false);

 builder.write("Row 1, Cell 1.");
 builder.insertCell();
 builder.write("Row 1, Cell 2.");
 builder.insertCell();
 builder.write("Row 1, Cell 3.");
 builder.endRow();
 builder.insertCell();
 builder.write("Row 2, Cell 1.");
 builder.insertCell();
 builder.write("Row 2, Cell 2.");
 builder.insertCell();
 builder.write("Row 2, Cell 3.");
 builder.endRow();
 builder.endTable();

 doc.save(getArtifactsDir() + "DocumentBuilder.CreateFormattedTable.docx");
 
```

**Returns:**
[ParagraphFormat](../../com.aspose.words/paragraphformat/) - An object that represents current paragraph formatting properties.
### getRowFormat() {#getRowFormat}
```
public RowFormat getRowFormat()
```


Devuelve un objeto que representa las propiedades de formato de fila de tabla actuales.

 **Examples:** 

Muestra cómo crear una tabla con bordes personalizados.

```

 Document doc = new Document();
 DocumentBuilder builder = new DocumentBuilder(doc);

 builder.startTable();

 // Setting table formatting options for a document builder
 // will apply them to every row and cell that we add with it.
 builder.getParagraphFormat().setAlignment(ParagraphAlignment.CENTER);

 builder.getCellFormat().clearFormatting();
 builder.getCellFormat().setWidth(150.0);
 builder.getCellFormat().setVerticalAlignment(CellVerticalAlignment.CENTER);
 builder.getCellFormat().getShading().setBackgroundPatternColor(Color.GREEN);
 builder.getCellFormat().setWrapText(false);
 builder.getCellFormat().setFitText(true);

 builder.getRowFormat().clearFormatting();
 builder.getRowFormat().setHeightRule(HeightRule.EXACTLY);
 builder.getRowFormat().setHeight(50.0);
 builder.getRowFormat().getBorders().setLineStyle(LineStyle.ENGRAVE_3_D);
 builder.getRowFormat().getBorders().setColor(Color.ORANGE);

 builder.insertCell();
 builder.write("Row 1, Col 1");

 builder.insertCell();
 builder.write("Row 1, Col 2");
 builder.endRow();

 // Changing the formatting will apply it to the current cell,
 // and any new cells that we create with the builder afterward.
 // This will not affect the cells that we have added previously.
 builder.getCellFormat().getShading().clearFormatting();

 builder.insertCell();
 builder.write("Row 2, Col 1");

 builder.insertCell();
 builder.write("Row 2, Col 2");

 builder.endRow();

 // Increase row height to fit the vertical text.
 builder.insertCell();
 builder.getRowFormat().setHeight(150.0);
 builder.getCellFormat().setOrientation(TextOrientation.UPWARD);
 builder.write("Row 3, Col 1");

 builder.insertCell();
 builder.getCellFormat().setOrientation(TextOrientation.DOWNWARD);
 builder.write("Row 3, Col 2");

 builder.endRow();
 builder.endTable();

 doc.save(getArtifactsDir() + "DocumentBuilder.InsertTable.docx");
 
```

Muestra cómo crear una tabla formateada de 2x2.

```

 Document doc = new Document();
 DocumentBuilder builder = new DocumentBuilder(doc);

 Table table = builder.startTable();
 builder.insertCell();
 builder.getCellFormat().setVerticalAlignment(CellVerticalAlignment.CENTER);
 builder.write("Row 1, cell 1.");
 builder.insertCell();
 builder.write("Row 1, cell 2.");
 builder.endRow();

 // While building the table, the document builder will apply its current RowFormat/CellFormat property values
 // to the current row/cell that its cursor is in and any new rows/cells as it creates them.
 Assert.assertEquals(CellVerticalAlignment.CENTER, table.getRows().get(0).getCells().get(0).getCellFormat().getVerticalAlignment());
 Assert.assertEquals(CellVerticalAlignment.CENTER, table.getRows().get(0).getCells().get(1).getCellFormat().getVerticalAlignment());

 builder.insertCell();
 builder.getRowFormat().setHeight(100.0);
 builder.getRowFormat().setHeightRule(HeightRule.EXACTLY);
 builder.getCellFormat().setOrientation(TextOrientation.UPWARD);
 builder.write("Row 2, cell 1.");
 builder.insertCell();
 builder.getCellFormat().setOrientation(TextOrientation.DOWNWARD);
 builder.write("Row 2, cell 2.");
 builder.endRow();
 builder.endTable();

 // Previously added rows and cells are not retroactively affected by changes to the builder's formatting.
 Assert.assertEquals(0.0, table.getRows().get(0).getRowFormat().getHeight());
 Assert.assertEquals(HeightRule.AUTO, table.getRows().get(0).getRowFormat().getHeightRule());
 Assert.assertEquals(100.0, table.getRows().get(1).getRowFormat().getHeight());
 Assert.assertEquals(HeightRule.EXACTLY, table.getRows().get(1).getRowFormat().getHeightRule());
 Assert.assertEquals(TextOrientation.UPWARD, table.getRows().get(1).getCells().get(0).getCellFormat().getOrientation());
 Assert.assertEquals(TextOrientation.DOWNWARD, table.getRows().get(1).getCells().get(1).getCellFormat().getOrientation());

 doc.save(getArtifactsDir() + "DocumentBuilder.BuildTable.docx");
 
```

Muestra cómo formatear filas con un document builder.

```

 Document doc = new Document();
 DocumentBuilder builder = new DocumentBuilder(doc);

 Table table = builder.startTable();
 builder.insertCell();
 builder.write("Row 1, cell 1.");

 // Start a second row, and then configure its height. The builder will apply these settings to
 // its current row, as well as any new rows it creates afterwards.
 builder.endRow();

 RowFormat rowFormat = builder.getRowFormat();
 rowFormat.setHeight(100.0);
 rowFormat.setHeightRule(HeightRule.EXACTLY);

 builder.insertCell();
 builder.write("Row 2, cell 1.");
 builder.endTable();

 // The first row was unaffected by the padding reconfiguration and still holds the default values.
 Assert.assertEquals(0.0d, table.getRows().get(0).getRowFormat().getHeight());
 Assert.assertEquals(HeightRule.AUTO, table.getRows().get(0).getRowFormat().getHeightRule());

 Assert.assertEquals(100.0d, table.getRows().get(1).getRowFormat().getHeight());
 Assert.assertEquals(HeightRule.EXACTLY, table.getRows().get(1).getRowFormat().getHeightRule());

 doc.save(getArtifactsDir() + "DocumentBuilder.SetRowFormatting.docx");
 
```

**Returns:**
[RowFormat](../../com.aspose.words/rowformat/) - An object that represents current table row formatting properties.
### getUnderline() {#getUnderline}
```
public int getUnderline()
```


Obtiene/establece el tipo de subrayado para la fuente actual.

 **Examples:** 

Muestra cómo dar formato al texto insertado por un document builder.

```

 Document doc = new Document();
 DocumentBuilder builder = new DocumentBuilder(doc);

 builder.setUnderline(Underline.DASH);
 builder.getFont().setColor(Color.BLUE);
 builder.getFont().setSize(32.0);

 // The builder applies formatting to its current paragraph and any new text added by it afterward.
 builder.writeln("Large, blue, and underlined text.");

 doc.save(getArtifactsDir() + "DocumentBuilder.InsertUnderline.docx");
 
```

**Returns:**
int - El valor int correspondiente. El valor devuelto es una de las constantes [Underline](../../com.aspose.words/underline/) .
### insertBreak(int breakType) {#insertBreak-int}
```
public void insertBreak(int breakType)
```




**Parameters:**
| Parámetro | Tipo | Descripción |
| --- | --- | --- |
| breakType | int |  |

### insertCell() {#insertCell}
```
public Cell insertCell()
```


Inserta una celda de tabla en el documento.

 **Remarks:** 

Para iniciar una tabla, simplemente llame a [insertCell()](../../com.aspose.words/documentbuilder/\#insertCell). Después de esto, cualquier contenido que añada usando otros métodos de la clase [DocumentBuilder](../../com.aspose.words/documentbuilder/) se añadirá a la celda actual.

Para iniciar una nueva celda en la misma fila, llame a [insertCell()](../../com.aspose.words/documentbuilder/\#insertCell) nuevamente.

Para terminar una fila de tabla, llame a [endRow()](../../com.aspose.words/documentbuilder/\#endRow).

Utilice la propiedad [getCellFormat()](../../com.aspose.words/documentbuilder/\#getCellFormat) para especificar el formato de la celda.

 **Examples:** 

Muestra cómo crear una tabla con bordes personalizados.

```

 Document doc = new Document();
 DocumentBuilder builder = new DocumentBuilder(doc);

 builder.startTable();

 // Setting table formatting options for a document builder
 // will apply them to every row and cell that we add with it.
 builder.getParagraphFormat().setAlignment(ParagraphAlignment.CENTER);

 builder.getCellFormat().clearFormatting();
 builder.getCellFormat().setWidth(150.0);
 builder.getCellFormat().setVerticalAlignment(CellVerticalAlignment.CENTER);
 builder.getCellFormat().getShading().setBackgroundPatternColor(Color.GREEN);
 builder.getCellFormat().setWrapText(false);
 builder.getCellFormat().setFitText(true);

 builder.getRowFormat().clearFormatting();
 builder.getRowFormat().setHeightRule(HeightRule.EXACTLY);
 builder.getRowFormat().setHeight(50.0);
 builder.getRowFormat().getBorders().setLineStyle(LineStyle.ENGRAVE_3_D);
 builder.getRowFormat().getBorders().setColor(Color.ORANGE);

 builder.insertCell();
 builder.write("Row 1, Col 1");

 builder.insertCell();
 builder.write("Row 1, Col 2");
 builder.endRow();

 // Changing the formatting will apply it to the current cell,
 // and any new cells that we create with the builder afterward.
 // This will not affect the cells that we have added previously.
 builder.getCellFormat().getShading().clearFormatting();

 builder.insertCell();
 builder.write("Row 2, Col 1");

 builder.insertCell();
 builder.write("Row 2, Col 2");

 builder.endRow();

 // Increase row height to fit the vertical text.
 builder.insertCell();
 builder.getRowFormat().setHeight(150.0);
 builder.getCellFormat().setOrientation(TextOrientation.UPWARD);
 builder.write("Row 3, Col 1");

 builder.insertCell();
 builder.getCellFormat().setOrientation(TextOrientation.DOWNWARD);
 builder.write("Row 3, Col 2");

 builder.endRow();
 builder.endTable();

 doc.save(getArtifactsDir() + "DocumentBuilder.InsertTable.docx");
 
```

Muestra cómo usar un DocumentBuilder para crear una tabla.

```

 Document doc = new Document();
 DocumentBuilder builder = new DocumentBuilder(doc);

 // Start the table, then populate the first row with two cells.
 builder.startTable();
 builder.insertCell();
 builder.write("Row 1, Cell 1.");
 builder.insertCell();
 builder.write("Row 1, Cell 2.");

 // Call the builder's "EndRow" method to start a new row.
 builder.endRow();
 builder.insertCell();
 builder.write("Row 2, Cell 1.");
 builder.insertCell();
 builder.write("Row 2, Cell 2.");
 builder.endTable();

 doc.save(getArtifactsDir() + "DocumentBuilder.CreateTable.docx");
 
```

**Returns:**
[Cell](../../com.aspose.words/cell/) - The cell node that was just inserted.
### insertChart(int chartType, double width, double height) {#insertChart-int-double-double}
```
public Shape insertChart(int chartType, double width, double height)
```




**Parameters:**
| Parámetro | Tipo | Descripción |
| --- | --- | --- |
| chartType | int |  |
| ancho | double |  |
| alto | double |  |

**Returns:**
[Shape](../../com.aspose.words/shape/)
### insertChart(int chartType, double width, double height, int chartStyle) {#insertChart-int-double-double-int}
```
public Shape insertChart(int chartType, double width, double height, int chartStyle)
```




**Parameters:**
| Parámetro | Tipo | Descripción |
| --- | --- | --- |
| chartType | int |  |
| ancho | double |  |
| alto | double |  |
| chartStyle | int |  |

**Returns:**
[Shape](../../com.aspose.words/shape/)
### insertChart(int chartType, int horzPos, double left, int vertPos, double top, double width, double height, int wrapType) {#insertChart-int-int-double-int-double-double-double-int}
```
public Shape insertChart(int chartType, int horzPos, double left, int vertPos, double top, double width, double height, int wrapType)
```




**Parameters:**
| Parámetro | Tipo | Descripción |
| --- | --- | --- |
| chartType | int |  |
| horzPos | int |  |
| izquierda | double |  |
| vertPos | int |  |
| superior | double |  |
| ancho | double |  |
| alto | double |  |
| wrapType | int |  |

**Returns:**
[Shape](../../com.aspose.words/shape/)
### insertChart(int chartType, int horzPos, double left, int vertPos, double top, double width, double height, int wrapType, int chartStyle) {#insertChart-int-int-double-int-double-double-double-int-int}
```
public Shape insertChart(int chartType, int horzPos, double left, int vertPos, double top, double width, double height, int wrapType, int chartStyle)
```




**Parameters:**
| Parámetro | Tipo | Descripción |
| --- | --- | --- |
| chartType | int |  |
| horzPos | int |  |
| izquierda | double |  |
| vertPos | int |  |
| superior | double |  |
| ancho | double |  |
| alto | double |  |
| wrapType | int |  |
| chartStyle | int |  |

**Returns:**
[Shape](../../com.aspose.words/shape/)
### insertCheckBox(String name, boolean defaultValue, boolean checkedValue, int size) {#insertCheckBox-java.lang.String-boolean-boolean-int}
```
public FormField insertCheckBox(String name, boolean defaultValue, boolean checkedValue, int size)
```


Inserta un campo de formulario de casilla de verificación en la posición actual.

 **Remarks:** 

Si especifica un nombre para el campo del formulario, entonces se crea automáticamente un marcador con el mismo nombre.

 **Examples:** 

Muestra cómo insertar casillas de verificación en el documento.

```

 Document doc = new Document();
 DocumentBuilder builder = new DocumentBuilder(doc);

 // Insert checkboxes of varying sizes and default checked statuses.
 builder.write("Unchecked check box of a default size: ");
 builder.insertCheckBox("", false, false, 0);
 builder.insertParagraph();

 builder.write("Large checked check box: ");
 builder.insertCheckBox("CheckBox_Default", true, true, 50);
 builder.insertParagraph();

 // Form fields have a name length limit of 20 characters.
 builder.write("Very large checked check box: ");
 builder.insertCheckBox("CheckBox_OnlyCheckedValue", true, 100);

 Assert.assertEquals("CheckBox_OnlyChecked", doc.getRange().getFormFields().get(2).getName());

 // We can interact with these check boxes in Microsoft Word by double clicking them.
 doc.save(getArtifactsDir() + "DocumentBuilder.InsertCheckBox.docx");
 
```

**Parameters:**
| Parámetro | Tipo | Descripción |
| --- | --- | --- |
| nombre | java.lang.String | El nombre del campo del formulario. Puede ser una cadena vacía. El valor con más de 20 caracteres será truncado. |
| defaultValue | boolean | Valor predeterminado del campo de casilla de verificación. |
| checkedValue | boolean | Estado actual marcado del campo de casilla de verificación. |
| tamaño | int | Especifica el tamaño de la casilla de verificación en puntos. Especifique 0 para que MS Word calcule automáticamente el tamaño de la casilla de verificación. |

**Returns:**
[FormField](../../com.aspose.words/formfield/) - The form field node that was just inserted.
### insertCheckBox(String name, boolean checkedValue, int size) {#insertCheckBox-java.lang.String-boolean-int}
```
public FormField insertCheckBox(String name, boolean checkedValue, int size)
```


Inserta un campo de formulario de casilla de verificación en la posición actual.

 **Remarks:** 

Si especifica un nombre para el campo del formulario, entonces se crea automáticamente un marcador con el mismo nombre.

 **Examples:** 

Muestra cómo insertar casillas de verificación en el documento.

```

 Document doc = new Document();
 DocumentBuilder builder = new DocumentBuilder(doc);

 // Insert checkboxes of varying sizes and default checked statuses.
 builder.write("Unchecked check box of a default size: ");
 builder.insertCheckBox("", false, false, 0);
 builder.insertParagraph();

 builder.write("Large checked check box: ");
 builder.insertCheckBox("CheckBox_Default", true, true, 50);
 builder.insertParagraph();

 // Form fields have a name length limit of 20 characters.
 builder.write("Very large checked check box: ");
 builder.insertCheckBox("CheckBox_OnlyCheckedValue", true, 100);

 Assert.assertEquals("CheckBox_OnlyChecked", doc.getRange().getFormFields().get(2).getName());

 // We can interact with these check boxes in Microsoft Word by double clicking them.
 doc.save(getArtifactsDir() + "DocumentBuilder.InsertCheckBox.docx");
 
```

**Parameters:**
| Parámetro | Tipo | Descripción |
| --- | --- | --- |
| nombre | java.lang.String | El nombre del campo del formulario. Puede ser una cadena vacía. El valor con más de 20 caracteres será truncado. |
| checkedValue | boolean | Estado marcado del campo de casilla de verificación. |
| tamaño | int | Especifica el tamaño de la casilla de verificación en puntos. Especifique 0 para que MS Word calcule automáticamente el tamaño de la casilla de verificación. |

**Returns:**
[FormField](../../com.aspose.words/formfield/) - The form field node that was just inserted.
### insertComboBox(String name, String[] items, int selectedIndex) {#insertComboBox-java.lang.String-java.lang.String---int}
```
public FormField insertComboBox(String name, String[] items, int selectedIndex)
```


Inserta un campo de formulario de cuadro combinado en la posición actual.

 **Remarks:** 

Si especifica un nombre para el campo del formulario, entonces se crea automáticamente un marcador con el mismo nombre.

 **Examples:** 

Muestra cómo crear campos de formulario.

```

 DocumentBuilder builder = new DocumentBuilder();

 // Form fields are objects in the document that the user can interact with by being prompted to enter values.
 // We can create them using a document builder, and below are two ways of doing so.
 // 1 -  Basic text input:
 builder.insertTextInput("My text input", TextFormFieldType.REGULAR,
         "", "Enter your name here", 30);

 // 2 -  Combo box with prompt text, and a range of possible values:
 String[] items =
         {
                 "-- Select your favorite footwear --", "Sneakers", "Oxfords", "Flip-flops", "Other"
         };

 builder.insertParagraph();
 builder.insertComboBox("My combo box", items, 0);

 builder.getDocument().save(getArtifactsDir() + "DocumentBuilder.CreateForm.docx");
 
```

Muestra cómo insertar un campo de formulario de cuadro combinado en un documento.

```

 Document doc = new Document();
 DocumentBuilder builder = new DocumentBuilder(doc);

 // Insert a form that prompts the user to pick one of the items from the menu.
 builder.write("Pick a fruit: ");
 String[] items = {"Apple", "Banana", "Cherry"};
 builder.insertComboBox("DropDown", items, 0);

 doc.save(getArtifactsDir() + "DocumentBuilder.InsertComboBox.docx");
 
```

**Parameters:**
| Parámetro | Tipo | Descripción |
| --- | --- | --- |
| nombre | java.lang.String | El nombre del campo del formulario. Puede ser una cadena vacía. El valor con más de 20 caracteres será truncado. |
| items | java.lang.String[] | Los elementos del ComboBox. El máximo es 25 elementos. |
| selectedIndex | int | El índice del elemento seleccionado en el ComboBox. |

**Returns:**
[FormField](../../com.aspose.words/formfield/) - The form field node that was just inserted.
### insertDocument(Document srcDoc, int importFormatMode) {#insertDocument-com.aspose.words.Document-int}
```
public Node insertDocument(Document srcDoc, int importFormatMode)
```




**Parameters:**
| Parámetro | Tipo | Descripción |
| --- | --- | --- |
| srcDoc | [Document](../../com.aspose.words/document/) |  |
| importFormatMode | int |  |

**Returns:**
[Node](../../com.aspose.words/node/)
### insertDocument(Document srcDoc, int importFormatMode, ImportFormatOptions importFormatOptions) {#insertDocument-com.aspose.words.Document-int-com.aspose.words.ImportFormatOptions}
```
public Node insertDocument(Document srcDoc, int importFormatMode, ImportFormatOptions importFormatOptions)
```




**Parameters:**
| Parámetro | Tipo | Descripción |
| --- | --- | --- |
| srcDoc | [Document](../../com.aspose.words/document/) |  |
| importFormatMode | int |  |
| importFormatOptions | [ImportFormatOptions](../../com.aspose.words/importformatoptions/) |  |

**Returns:**
[Node](../../com.aspose.words/node/)
### insertDocumentInline(Document srcDoc, int importFormatMode, ImportFormatOptions importFormatOptions) {#insertDocumentInline-com.aspose.words.Document-int-com.aspose.words.ImportFormatOptions}
```
public Node insertDocumentInline(Document srcDoc, int importFormatMode, ImportFormatOptions importFormatOptions)
```




**Parameters:**
| Parámetro | Tipo | Descripción |
| --- | --- | --- |
| srcDoc | [Document](../../com.aspose.words/document/) |  |
| importFormatMode | int |  |
| importFormatOptions | [ImportFormatOptions](../../com.aspose.words/importformatoptions/) |  |

**Returns:**
[Node](../../com.aspose.words/node/)
### insertField(int fieldType, boolean updateField) {#insertField-int-boolean}
```
public Field insertField(int fieldType, boolean updateField)
```




**Parameters:**
| Parámetro | Tipo | Descripción |
| --- | --- | --- |
| fieldType | int |  |
| updateField | boolean |  |

**Returns:**
[Field](../../com.aspose.words/field/)
### insertField(String fieldCode) {#insertField-java.lang.String}
```
public Field insertField(String fieldCode)
```


Inserta un campo de Word en un documento y actualiza el resultado del campo.

 **Remarks:** 

Este método inserta un campo en un documento y actualiza el resultado del campo inmediatamente. Aspose.Words puede actualizar campos de la mayoría de los tipos, pero no de todos. Para más detalles, consulte la sobrecarga [insertField(java.lang.String, java.lang.String)](../../com.aspose.words/documentbuilder/\#insertField-java.lang.String--java.lang.String).

 **Examples:** 

Muestra cómo insertar campos y mover el cursor del DocumentBuilder a ellos.

```

 Document doc = new Document();
 DocumentBuilder builder = new DocumentBuilder(doc);
 builder.insertField("MERGEFIELD MyMergeField1 \\* MERGEFORMAT");
 builder.insertField("MERGEFIELD MyMergeField2 \\* MERGEFORMAT");

 // Move the cursor to the first MERGEFIELD.
 builder.moveToMergeField("MyMergeField1", true, false);

 // Note that the cursor is placed immediately after the first MERGEFIELD, and before the second.
 Assert.assertEquals(doc.getRange().getFields().get(1).getStart(), builder.getCurrentNode());
 Assert.assertEquals(doc.getRange().getFields().get(0).getEnd(), builder.getCurrentNode().getPreviousSibling());

 // If we wish to edit the field's field code or contents using the builder,
 // its cursor would need to be inside a field.
 // To place it inside a field, we would need to call the document builder's MoveTo method
 // and pass the field's start or separator node as an argument.
 builder.write(" Text between our merge fields. ");

 doc.save(getArtifactsDir() + "DocumentBuilder.MergeFields.docx");
 
```

Muestra cómo insertar un campo en un documento usando un código de campo.

```

 Document doc = new Document();
 DocumentBuilder builder = new DocumentBuilder(doc);

 Field dateField = builder.insertField("DATE \\* MERGEFORMAT");

 Assert.assertEquals(FieldType.FIELD_DATE, dateField.getType());
 Assert.assertEquals("DATE \\* MERGEFORMAT", dateField.getFieldCode());
 
```

**Parameters:**
| Parámetro | Tipo | Descripción |
| --- | --- | --- |
| fieldCode | java.lang.String | El código de campo a insertar (sin llaves). |

**Returns:**
[Field](../../com.aspose.words/field/) - A [Field](../../com.aspose.words/field/) object that represents the inserted field.
### insertField(String fieldCode, String fieldValue) {#insertField-java.lang.String-java.lang.String}
```
public Field insertField(String fieldCode, String fieldValue)
```


Inserta un campo de Word en un documento sin actualizar el resultado del campo.

 **Remarks:** 

Los campos en documentos de Microsoft Word constan de un código de campo y un resultado de campo. El código de campo es como una fórmula y el resultado de campo es como el valor que produce la fórmula. El código de campo también puede contener interruptores de campo que son como instrucciones adicionales para realizar una acción específica.

Puede alternar entre mostrar códigos de campo y resultados en su documento de Microsoft Word usando el atajo de teclado Alt+F9. Los códigos de campo aparecen entre llaves ( \{ \} ).

Para crear un campo, debe especificar un tipo de campo, un código de campo y un valor de campo "placeholder". Si no está seguro sobre la sintaxis de un código de campo en particular, cree el campo primero en Microsoft Word y cambie a la vista de código de campo para verlo.

Aspose.Words puede calcular los resultados de campo para la mayoría de los tipos de campo, pero este método no actualiza el resultado del campo automáticamente. Debido a que el resultado del campo no se calcula automáticamente, se espera que proporcione algún valor de cadena (o incluso una cadena vacía) que se insertará en el resultado del campo. Este valor permanecerá en el resultado del campo como un marcador de posición hasta que el campo se actualice. Para actualizar el resultado del campo puede llamar a [Field.update()](../../com.aspose.words/field/\#update) en el objeto de campo devuelto o a [Document.updateFields()](../../com.aspose.words/document/\#updateFields) para actualizar los campos en todo el documento.

 **Examples:** 

Muestra cómo configurar la numeración de páginas en una sección.

```

 Document doc = new Document();
 DocumentBuilder builder = new DocumentBuilder(doc);

 builder.writeln("Section 1, page 1.");
 builder.insertBreak(BreakType.PAGE_BREAK);
 builder.writeln("Section 1, page 2.");
 builder.insertBreak(BreakType.PAGE_BREAK);
 builder.writeln("Section 1, page 3.");
 builder.insertBreak(BreakType.SECTION_BREAK_NEW_PAGE);
 builder.writeln("Section 2, page 1.");
 builder.insertBreak(BreakType.PAGE_BREAK);
 builder.writeln("Section 2, page 2.");
 builder.insertBreak(BreakType.PAGE_BREAK);
 builder.writeln("Section 2, page 3.");

 // Move the document builder to the first section's primary header,
 // which every page in that section will display.
 builder.moveToSection(0);
 builder.moveToHeaderFooter(HeaderFooterType.HEADER_PRIMARY);

 // Insert a PAGE field, which will display the number of the current page.
 builder.write("Page ");
 builder.insertField("PAGE", "");

 // Configure the section to have the page count that PAGE fields display start from 5.
 // Also, configure all PAGE fields to display their page numbers using uppercase Roman numerals.
 PageSetup pageSetup = doc.getSections().get(0).getPageSetup();
 pageSetup.setRestartPageNumbering(true);
 pageSetup.setPageStartingNumber(5);
 pageSetup.setPageNumberStyle(NumberStyle.UPPERCASE_ROMAN);

 // Create another primary header for the second section, with another PAGE field.
 builder.moveToSection(1);
 builder.moveToHeaderFooter(HeaderFooterType.HEADER_PRIMARY);
 builder.getParagraphFormat().setAlignment(ParagraphAlignment.CENTER);
 builder.write(" - ");
 builder.insertField("PAGE", "");
 builder.write(" - ");

 // Configure the section to have the page count that PAGE fields display start from 10.
 // Also, configure all PAGE fields to display their page numbers using Arabic numbers.
 pageSetup = doc.getSections().get(1).getPageSetup();
 pageSetup.setPageStartingNumber(10);
 pageSetup.setRestartPageNumbering(true);
 pageSetup.setPageNumberStyle(NumberStyle.ARABIC);

 doc.save(getArtifactsDir() + "PageSetup.PageNumbering.docx");
 
```

**Parameters:**
| Parámetro | Tipo | Descripción |
| --- | --- | --- |
| fieldCode | java.lang.String | El código de campo a insertar (sin llaves). |
| fieldValue | java.lang.String | El valor del campo a insertar. Pase  null  para los campos que no tienen un valor. |

**Returns:**
[Field](../../com.aspose.words/field/) - A [Field](../../com.aspose.words/field/) object that represents the inserted field.
### insertFootnote(int footnoteType, String footnoteText) {#insertFootnote-int-java.lang.String}
```
public Footnote insertFootnote(int footnoteType, String footnoteText)
```




**Parameters:**
| Parámetro | Tipo | Descripción |
| --- | --- | --- |
| footnoteType | int |  |
| footnoteText | java.lang.String |  |

**Returns:**
[Footnote](../../com.aspose.words/footnote/)
### insertFootnote(int footnoteType, String footnoteText, String referenceMark) {#insertFootnote-int-java.lang.String-java.lang.String}
```
public Footnote insertFootnote(int footnoteType, String footnoteText, String referenceMark)
```




**Parameters:**
| Parámetro | Tipo | Descripción |
| --- | --- | --- |
| footnoteType | int |  |
| footnoteText | java.lang.String |  |
| referenceMark | java.lang.String |  |

**Returns:**
[Footnote](../../com.aspose.words/footnote/)
### insertForms2OleControl(Forms2OleControl forms2OleControl) {#insertForms2OleControl-com.aspose.words.Forms2OleControl}
```
public Shape insertForms2OleControl(Forms2OleControl forms2OleControl)
```


Inserta el objeto [Forms2OleControl](../../com.aspose.words/forms2olecontrol/) en la posición actual.

 **Examples:** 

Muestra cómo insertar un control ActiveX.

```

 DocumentBuilder builder = new DocumentBuilder();

 CommandButtonControl button1 = new CommandButtonControl();
 Shape shape = builder.insertForms2OleControl(button1);
 Assert.assertEquals(Forms2OleControlType.COMMAND_BUTTON, button1.getType());
 
```

**Parameters:**
| Parámetro | Tipo | Descripción |
| --- | --- | --- |
| forms2OleControl | [Forms2OleControl](../../com.aspose.words/forms2olecontrol/) |  |

**Returns:**
[Shape](../../com.aspose.words/shape/) - [Shape](../../com.aspose.words/shape/) object that contains passed [Forms2OleControl](../../com.aspose.words/forms2olecontrol/)
### insertGroupShape(ShapeBase[] shapes) {#insertGroupShape-com.aspose.words.ShapeBase...}
```
public GroupShape insertGroupShape(ShapeBase[] shapes)
```


Agrupa las formas pasadas como parámetro en un nuevo nodo GroupShape que se inserta en la posición actual.

 **Remarks:** 

La posición y dimensión del nuevo GroupShape se calcularán automáticamente.

Las formas VML y DML no pueden agruparse juntas.

 **Examples:** 

Muestra cómo insertar una forma de grupo DML.

```

 Document doc = new Document();
 DocumentBuilder builder = new DocumentBuilder(doc);

 Shape shape1 = builder.insertShape(ShapeType.RECTANGLE, 200.0, 250.0);
 shape1.setLeft(20.0);
 shape1.setTop(20.0);
 shape1.getStroke().setColor(Color.RED);

 Shape shape2 = builder.insertShape(ShapeType.ELLIPSE, 150.0, 200.0);
 shape2.setLeft(40.0);
 shape2.setTop(50.0);
 shape2.getStroke().setColor(Color.GREEN);

 // Dimensions for the new GroupShape node.
 double left = 10.0;
 double top = 10.0;
 double width = 200.0;
 double height = 300.0;
 // Insert GroupShape node for the specified size which is inserted into the specified position.
 GroupShape groupShape1 = builder.insertGroupShape(left, top, width, height, new Shape[] { shape1, shape2 });

 // Insert GroupShape node which position and dimension will be calculated automatically.
 Shape shape3 = (Shape)shape1.deepClone(true);
 GroupShape groupShape2 = builder.insertGroupShape(shape3);

 doc.save(getArtifactsDir() + "Shape.InsertGroupShape.docx");
 
```

Muestra cómo combinar una forma de grupo con la forma.

```

 Document doc = new Document();
 DocumentBuilder builder = new DocumentBuilder(doc);

 Shape shape1 = builder.insertShape(ShapeType.RECTANGLE, 200.0, 250.0);
 shape1.setLeft(20.0);
 shape1.setTop(20.0);
 shape1.getStroke().setColor(Color.RED);

 Shape shape2 = builder.insertShape(ShapeType.ELLIPSE, 150.0, 200.0);
 shape2.setLeft(40.0);
 shape2.setTop(50.0);
 shape2.getStroke().setColor(Color.GREEN);

 // Combine shapes into a GroupShape node which is inserted into the specified position.
 GroupShape groupShape1 = builder.insertGroupShape(shape1, shape2);

 // Combine Shape and GroupShape nodes.
 Shape shape3 = (Shape)shape1.deepClone(true);
 GroupShape groupShape2 = builder.insertGroupShape(groupShape1, shape3);

 doc.save(getArtifactsDir() + "Shape.CombineGroupShape.docx");
 
```

**Parameters:**
| Parámetro | Tipo | Descripción |
| --- | --- | --- |
| shapes | [ShapeBase\[\]](../../com.aspose.words/shapebase/) | La lista de formas a agrupar. |

**Returns:**
[GroupShape](../../com.aspose.words/groupshape/)
### insertGroupShape(double left, double top, double width, double height, ShapeBase[] shapes) {#insertGroupShape-double-double-double-double-com.aspose.words.ShapeBase...}
```
public GroupShape insertGroupShape(double left, double top, double width, double height, ShapeBase[] shapes)
```


Agrupa las formas pasadas como parámetro en un nuevo nodo GroupShape del tamaño especificado que se inserta en la posición especificada.

 **Remarks:** 

Las formas VML y DML no pueden agruparse juntas.

 **Examples:** 

Muestra cómo insertar una forma de grupo DML.

```

 Document doc = new Document();
 DocumentBuilder builder = new DocumentBuilder(doc);

 Shape shape1 = builder.insertShape(ShapeType.RECTANGLE, 200.0, 250.0);
 shape1.setLeft(20.0);
 shape1.setTop(20.0);
 shape1.getStroke().setColor(Color.RED);

 Shape shape2 = builder.insertShape(ShapeType.ELLIPSE, 150.0, 200.0);
 shape2.setLeft(40.0);
 shape2.setTop(50.0);
 shape2.getStroke().setColor(Color.GREEN);

 // Dimensions for the new GroupShape node.
 double left = 10.0;
 double top = 10.0;
 double width = 200.0;
 double height = 300.0;
 // Insert GroupShape node for the specified size which is inserted into the specified position.
 GroupShape groupShape1 = builder.insertGroupShape(left, top, width, height, new Shape[] { shape1, shape2 });

 // Insert GroupShape node which position and dimension will be calculated automatically.
 Shape shape3 = (Shape)shape1.deepClone(true);
 GroupShape groupShape2 = builder.insertGroupShape(shape3);

 doc.save(getArtifactsDir() + "Shape.InsertGroupShape.docx");
 
```

**Parameters:**
| Parámetro | Tipo | Descripción |
| --- | --- | --- |
| izquierda | double | Distancia en puntos desde el origen hasta el lado izquierdo de la forma de grupo. |
| superior | double | Distancia en puntos desde el origen hasta el lado superior de la forma de grupo. |
| ancho | double | El ancho de la forma de grupo en puntos. No se permite un valor negativo. |
| alto | double | La altura de la forma de grupo en puntos. No se permite un valor negativo. |
| shapes | [ShapeBase\[\]](../../com.aspose.words/shapebase/) | La lista de formas a agrupar. |

**Returns:**
[GroupShape](../../com.aspose.words/groupshape/)
### insertHorizontalRule() {#insertHorizontalRule}
```
public Shape insertHorizontalRule()
```


Inserta una forma de regla horizontal en el documento.

 **Examples:** 

Muestra cómo insertar una forma de regla horizontal y personalizar su formato.

```

 Document doc = new Document();
 DocumentBuilder builder = new DocumentBuilder(doc);
 Shape shape = builder.insertHorizontalRule();

 HorizontalRuleFormat horizontalRuleFormat = shape.getHorizontalRuleFormat();
 horizontalRuleFormat.setAlignment(HorizontalRuleAlignment.CENTER);
 horizontalRuleFormat.setWidthPercent(70.0);
 horizontalRuleFormat.setHeight(3.0);
 horizontalRuleFormat.setColor(Color.BLUE);
 horizontalRuleFormat.setNoShade(true);

 Assert.assertTrue(shape.isHorizontalRule());
 Assert.assertTrue(shape.getHorizontalRuleFormat().getNoShade());
 
```

**Returns:**
[Shape](../../com.aspose.words/shape/) - The shape that is a horizontal rule.
### insertHtml(String html) {#insertHtml-java.lang.String}
```
public void insertHtml(String html)
```


Inserta una cadena HTML en el documento.

 **Remarks:** 

Puede usar este método para insertar un fragmento HTML o un documento HTML completo.

 **Examples:** 

Muestra cómo usar un document builder para insertar contenido html en un documento.

```

 Document doc = new Document();
 DocumentBuilder builder = new DocumentBuilder(doc);

 final String HTML = " Paragraph right" +
         "Implicit paragraph left" +
         " Div center" +
         " Heading 1 left.";

 builder.insertHtml(HTML);

 // Inserting HTML code parses the formatting of each element into equivalent document text formatting.
 ParagraphCollection paragraphs = doc.getFirstSection().getBody().getParagraphs();

 Assert.assertEquals("Paragraph right", paragraphs.get(0).getText().trim());
 Assert.assertEquals(ParagraphAlignment.RIGHT, paragraphs.get(0).getParagraphFormat().getAlignment());

 Assert.assertEquals("Implicit paragraph left", paragraphs.get(1).getText().trim());
 Assert.assertEquals(ParagraphAlignment.LEFT, paragraphs.get(1).getParagraphFormat().getAlignment());
 Assert.assertTrue(paragraphs.get(1).getRuns().get(0).getFont().getBold());

 Assert.assertEquals("Div center", paragraphs.get(2).getText().trim());
 Assert.assertEquals(ParagraphAlignment.CENTER, paragraphs.get(2).getParagraphFormat().getAlignment());

 Assert.assertEquals("Heading 1 left.", paragraphs.get(3).getText().trim());
 Assert.assertEquals("Heading 1", paragraphs.get(3).getParagraphFormat().getStyle().getName());

 doc.save(getArtifactsDir() + "DocumentBuilder.InsertHtml.docx");
 
```

Muestra cómo ejecutar una combinación de correspondencia con una devolución de llamada personalizada que maneja los datos de combinación en forma de documentos HTML.

```

 public void insertHtml() throws Exception {
     Document doc = new Document(getMyDir() + "Field sample - MERGEFIELD.docx");

     // Add a handler for the MergeField event
     doc.getMailMerge().setFieldMergingCallback(new HandleMergeFieldInsertHtml());

     final String htmlText = "\r\n Hello world!\r\n";

     // Execute mail merge
     doc.getMailMerge().execute(new String[]{"htmlField1"}, new String[]{htmlText});

     // Save resulting document with a new name
     doc.save(getArtifactsDir() + "MailMergeEvent.InsertHtml.docx");
 }

 private class HandleMergeFieldInsertHtml implements IFieldMergingCallback {
     // This is called when merge field is actually merged with data in the document.
     public void fieldMerging(final FieldMergingArgs args) throws Exception {
         // All merge fields that expect HTML data should be marked with some prefix, e.g. 'html'
         if (args.getDocumentFieldName().startsWith("html") && args.getField().getFieldCode().contains("\\b")) {
             FieldMergeField field = args.getField();

             // Insert the text for this merge field as HTML data, using DocumentBuilder
             DocumentBuilder builder = new DocumentBuilder(args.getDocument());
             builder.moveToMergeField(args.getDocumentFieldName());
             builder.write(field.getTextBefore());
             builder.insertHtml((String) args.getFieldValue());

             // The HTML text itself should not be inserted
             // We have already inserted it as an HTML
             args.setText("");
         }
     }

     public void imageFieldMerging(ImageFieldMergingArgs args) {
         // Do nothing
     }
 }
 
```

**Parameters:**
| Parámetro | Tipo | Descripción |
| --- | --- | --- |
| html | java.lang.String | Una cadena HTML para insertar en el documento. |

### insertHtml(String html, boolean useBuilderFormatting) {#insertHtml-java.lang.String-boolean}
```
public void insertHtml(String html, boolean useBuilderFormatting)
```


Inserta una cadena HTML en el documento.

 **Remarks:** 

Puede usar este método para insertar un fragmento HTML o un documento HTML completo.

Cuando  useBuilderFormatting  es  false , el formato de [DocumentBuilder](../../com.aspose.words/documentbuilder/) se ignora y el formato del texto insertado se basa en el formato HTML predeterminado. Como resultado, el texto se muestra tal como se renderiza en los navegadores.

Cuando useBuilderFormatting es verdadero, el formato del texto insertado se basa en el formato de [DocumentBuilder](../../com.aspose.words/documentbuilder/) y el texto parece como si se hubiera insertado con [write(java.lang.String)](../../com.aspose.words/documentbuilder/\#write-java.lang.String).

 **Examples:** 

Muestra cómo aplicar el formato de un document builder al insertar contenido HTML.

```

 Document doc = new Document();
 DocumentBuilder builder = new DocumentBuilder(doc);

 // Set a text alignment for the builder, insert an HTML paragraph with a specified alignment, and one without.
 builder.getParagraphFormat().setAlignment(ParagraphAlignment.DISTRIBUTED);
 builder.insertHtml(
         " Paragraph 1." +
                 " Paragraph 2.", useBuilderFormatting);

 ParagraphCollection paragraphs = doc.getFirstSection().getBody().getParagraphs();

 // The first paragraph has an alignment specified. When InsertHtml parses the HTML code,
 // the paragraph alignment value found in the HTML code always supersedes the document builder's value.
 Assert.assertEquals("Paragraph 1.", paragraphs.get(0).getText().trim());
 Assert.assertEquals(ParagraphAlignment.RIGHT, paragraphs.get(0).getParagraphFormat().getAlignment());

 // The second paragraph has no alignment specified. It can have its alignment value filled in
 // by the builder's value depending on the flag we passed to the InsertHtml method.
 Assert.assertEquals("Paragraph 2.", paragraphs.get(1).getText().trim());
 Assert.assertEquals(useBuilderFormatting ? ParagraphAlignment.DISTRIBUTED : ParagraphAlignment.LEFT,
         paragraphs.get(1).getParagraphFormat().getAlignment());

 doc.save(getArtifactsDir() + "DocumentBuilder.InsertHtmlWithFormatting.docx");
 
```

**Parameters:**
| Parámetro | Tipo | Descripción |
| --- | --- | --- |
| html | java.lang.String | Una cadena HTML para insertar en el documento. |
| useBuilderFormatting | boolean | Un valor que indica si el formato especificado en [DocumentBuilder](../../com.aspose.words/documentbuilder/) se utiliza como formato base para el texto importado desde HTML. |

### insertHtml(String html, int options) {#insertHtml-java.lang.String-int}
```
public void insertHtml(String html, int options)
```




**Parameters:**
| Parámetro | Tipo | Descripción |
| --- | --- | --- |
| html | java.lang.String |  |
| opciones | int |  |

### insertHyperlink(String displayText, String urlOrBookmark, boolean isBookmark) {#insertHyperlink-java.lang.String-java.lang.String-boolean}
```
public Field insertHyperlink(String displayText, String urlOrBookmark, boolean isBookmark)
```


Inserta un hipervínculo en el documento.

 **Remarks:** 

Tenga en cuenta que debe especificar el formato de fuente para el texto visible del hipervínculo explícitamente mediante la propiedad [getFont()](../../com.aspose.words/documentbuilder/\#getFont).

Este método llama internamente a [insertField(java.lang.String)](../../com.aspose.words/documentbuilder/\#insertField-java.lang.String) para insertar un campo HYPERLINK de MS Word en el documento.

 **Examples:** 

Muestra cómo insertar un campo de hipervínculo.

```

 Document doc = new Document();
 DocumentBuilder builder = new DocumentBuilder(doc);

 builder.write("For more information, please visit the ");

 // Insert a hyperlink and emphasize it with custom formatting.
 // The hyperlink will be a clickable piece of text which will take us to the location specified in the URL.
 builder.getFont().setColor(Color.BLUE);
 builder.getFont().setUnderline(Underline.SINGLE);
 builder.insertHyperlink("Google website", "https://www.google.com", false);
 builder.getFont().clearFormatting();
 builder.writeln(".");

 // Ctrl + left clicking the link in the text in Microsoft Word will take us to the URL via a new web browser window.
 doc.save(getArtifactsDir() + "DocumentBuilder.InsertHyperlink.docx");
 
```

Muestra cómo usar la pila de formato de un document builder.

```

 Document doc = new Document();
 DocumentBuilder builder = new DocumentBuilder(doc);

 // Set up font formatting, then write the text that goes before the hyperlink.
 builder.getFont().setName("Arial");
 builder.getFont().setSize(24.0);
 builder.write("To visit Google, hold Ctrl and click ");

 // Preserve our current formatting configuration on the stack.
 builder.pushFont();

 // Alter the builder's current formatting by applying a new style.
 builder.getFont().setStyleIdentifier(StyleIdentifier.HYPERLINK);
 builder.insertHyperlink("here", "http://www.google.com", false);

 Assert.assertEquals(Color.BLUE.getRGB(), builder.getFont().getColor().getRGB());
 Assert.assertEquals(Underline.SINGLE, builder.getFont().getUnderline());

 // Restore the font formatting that we saved earlier and remove the element from the stack.
 builder.popFont();

 Assert.assertEquals(0, builder.getFont().getColor().getRGB());
 Assert.assertEquals(Underline.NONE, builder.getFont().getUnderline());

 builder.write(". We hope you enjoyed the example.");

 doc.save(getArtifactsDir() + "DocumentBuilder.PushPopFont.docx");
 
```

Muestra cómo insertar un hipervínculo que hace referencia a un marcador local.

```

 Document doc = new Document();
 DocumentBuilder builder = new DocumentBuilder(doc);

 builder.startBookmark("Bookmark1");
 builder.write("Bookmarked text. ");
 builder.endBookmark("Bookmark1");
 builder.writeln("Text outside of the bookmark.");

 // Insert a HYPERLINK field that links to the bookmark. We can pass field switches
 // to the "InsertHyperlink" method as part of the argument containing the referenced bookmark's name.
 builder.getFont().setColor(Color.BLUE);
 builder.getFont().setUnderline(Underline.SINGLE);
 FieldHyperlink hyperlink = (FieldHyperlink)builder.insertHyperlink("Link to Bookmark1", "Bookmark1", true);
 hyperlink.setScreenTip("Hyperlink Tip");

 doc.save(getArtifactsDir() + "DocumentBuilder.InsertHyperlinkToLocalBookmark.docx");
 
```

**Parameters:**
| Parámetro | Tipo | Descripción |
| --- | --- | --- |
| displayText | java.lang.String | Texto del enlace que se mostrará en el documento. |
| urlOrBookmark | java.lang.String | Destino del enlace. Puede ser una URL o el nombre de un marcador dentro del documento. Este método siempre agrega comillas al principio y al final de la URL. |
| isBookmark | boolean | true si el parámetro anterior es el nombre de un marcador dentro del documento; false si el parámetro anterior es una URL. |

**Returns:**
[Field](../../com.aspose.words/field/) - A [Field](../../com.aspose.words/field/) object that represents the inserted field.
### insertImage(byte[] imageBytes) {#insertImage-byte}
```
public Shape insertImage(byte[] imageBytes)
```


Inserta una imagen desde un arreglo de bytes en el documento. La imagen se inserta en línea y al 100 % de escala.

 **Remarks:** 

Puede cambiar el tamaño, la ubicación, el método de posicionamiento y otras configuraciones de la imagen usando el objeto [Shape](../../com.aspose.words/shape/) devuelto por este método.

 **Examples:** 

Muestra cómo insertar una imagen desde un arreglo de bytes en un documento.

```

 Document doc = new Document();
 DocumentBuilder builder = new DocumentBuilder(doc);

 byte[] imageByteArray = DocumentHelper.getBytesFromStream(new FileInputStream(getImageDir() + "Logo.jpg"));

 // Below are three ways of inserting an image from a byte array.
 // 1 -  Inline shape with a default size based on the image's original dimensions:
 builder.insertImage(imageByteArray);

 builder.insertBreak(BreakType.PAGE_BREAK);

 // 2 -  Inline shape with custom dimensions:
 builder.insertImage(imageByteArray, ConvertUtil.pixelToPoint(250.0), ConvertUtil.pixelToPoint(144.0));

 builder.insertBreak(BreakType.PAGE_BREAK);

 // 3 -  Floating shape with custom dimensions:
 builder.insertImage(imageByteArray, RelativeHorizontalPosition.MARGIN, 100.0, RelativeVerticalPosition.MARGIN,
         100.0, 200.0, 100.0, WrapType.SQUARE);

 doc.save(getArtifactsDir() + "DocumentBuilderImages.InsertImageFromByteArray.docx");
 
```

**Parameters:**
| Parámetro | Tipo | Descripción |
| --- | --- | --- |
| imageBytes | byte[] | El arreglo de bytes que contiene la imagen. |

**Returns:**
[Shape](../../com.aspose.words/shape/) - The image node that was just inserted.
### insertImage(byte[] imageBytes, double width, double height) {#insertImage-byte---double-double}
```
public Shape insertImage(byte[] imageBytes, double width, double height)
```


Inserta una imagen en línea desde una matriz de bytes en el documento y la escala al tamaño especificado.

 **Remarks:** 

Puede cambiar el tamaño, la ubicación, el método de posicionamiento y otras configuraciones de la imagen usando el objeto [Shape](../../com.aspose.words/shape/) devuelto por este método.

 **Examples:** 

Muestra cómo insertar una imagen desde un arreglo de bytes en un documento.

```

 Document doc = new Document();
 DocumentBuilder builder = new DocumentBuilder(doc);

 byte[] imageByteArray = DocumentHelper.getBytesFromStream(new FileInputStream(getImageDir() + "Logo.jpg"));

 // Below are three ways of inserting an image from a byte array.
 // 1 -  Inline shape with a default size based on the image's original dimensions:
 builder.insertImage(imageByteArray);

 builder.insertBreak(BreakType.PAGE_BREAK);

 // 2 -  Inline shape with custom dimensions:
 builder.insertImage(imageByteArray, ConvertUtil.pixelToPoint(250.0), ConvertUtil.pixelToPoint(144.0));

 builder.insertBreak(BreakType.PAGE_BREAK);

 // 3 -  Floating shape with custom dimensions:
 builder.insertImage(imageByteArray, RelativeHorizontalPosition.MARGIN, 100.0, RelativeVerticalPosition.MARGIN,
         100.0, 200.0, 100.0, WrapType.SQUARE);

 doc.save(getArtifactsDir() + "DocumentBuilderImages.InsertImageFromByteArray.docx");
 
```

**Parameters:**
| Parámetro | Tipo | Descripción |
| --- | --- | --- |
| imageBytes | byte[] | El arreglo de bytes que contiene la imagen. |
| ancho | double | El ancho de la imagen en puntos. Puede ser un valor negativo o cero para solicitar el 100 % de escala. |
| alto | double | La altura de la imagen en puntos. Puede ser un valor negativo o cero para solicitar el 100 % de escala. |

**Returns:**
[Shape](../../com.aspose.words/shape/) - The image node that was just inserted.
### insertImage(byte[] imageBytes, int horzPos, double left, int vertPos, double top, double width, double height, int wrapType) {#insertImage-byte---int-double-int-double-double-double-int}
```
public Shape insertImage(byte[] imageBytes, int horzPos, double left, int vertPos, double top, double width, double height, int wrapType)
```




**Parameters:**
| Parámetro | Tipo | Descripción |
| --- | --- | --- |
| imageBytes | byte[] |  |
| horzPos | int |  |
| izquierda | double |  |
| vertPos | int |  |
| superior | double |  |
| ancho | double |  |
| alto | double |  |
| wrapType | int |  |

**Returns:**
[Shape](../../com.aspose.words/shape/)
### insertImage(BufferedImage image) {#insertImage-java.awt.image.BufferedImage}
```
public Shape insertImage(BufferedImage image)
```


Inserta una imagen en el documento. Inserta una imagen desde un objeto java.awt.image.BufferedImage en el documento. La imagen se inserta en línea y al 100 % de escala.

 **Remarks:** 

Puede cambiar el tamaño, la ubicación, el método de posicionamiento y otras configuraciones de la imagen usando el objeto [Shape](../../com.aspose.words/shape/) devuelto por este método.

Aspose.Words insertará la imagen en formato PNG y con la configuración predeterminada. Si desea insertar un  BufferedImage  en otro formato o con otras configuraciones, necesita guardar la imagen en un arreglo de bytes y usar [insertImage(byte[])](../../com.aspose.words/documentbuilder/\#insertImage-byte).

 **Examples:** 

Muestra cómo insertar una imagen desde un objeto en un documento.

```

 Document doc = new Document();
 DocumentBuilder builder = new DocumentBuilder(doc);

 String imageFile = getImageDir() + "Logo.jpg";

 // Below are three ways of inserting an image from an Image object instance.
 // 1 -  Inline shape with a default size based on the image's original dimensions:
 builder.insertImage(imageFile);

 builder.insertBreak(BreakType.PAGE_BREAK);

 // 2 -  Inline shape with custom dimensions:
 builder.insertImage(imageFile, ConvertUtil.pixelToPoint(250.0), ConvertUtil.pixelToPoint(144.0));

 builder.insertBreak(BreakType.PAGE_BREAK);

 // 3 -  Floating shape with custom dimensions:
 builder.insertImage(imageFile, RelativeHorizontalPosition.MARGIN, 100.0, RelativeVerticalPosition.MARGIN,
         100.0, 200.0, 100.0, WrapType.SQUARE);

 doc.save(getArtifactsDir() + "DocumentBuilderImages.InsertImageFromImageObject.docx");
 
```

**Parameters:**
| Parámetro | Tipo | Descripción |
| --- | --- | --- |
| imagen | java.awt.image.BufferedImage | La imagen a insertar en el documento. |

**Returns:**
[Shape](../../com.aspose.words/shape/) - The image node that was just inserted.
### insertImage(BufferedImage image, double width, double height) {#insertImage-java.awt.image.BufferedImage-double-double}
```
public Shape insertImage(BufferedImage image, double width, double height)
```


Inserta una imagen en línea desde un objeto java.awt.image.BufferedImage en el documento y la escala al tamaño especificado.

 **Remarks:** 

Puede cambiar el tamaño, la ubicación, el método de posicionamiento y otras configuraciones de la imagen usando el objeto [Shape](../../com.aspose.words/shape/) devuelto por este método.

Aspose.Words insertará la imagen en formato PNG y con la configuración predeterminada. Si desea insertar un  BufferedImage  en otro formato o con otras configuraciones, necesita guardar la imagen en un arreglo de bytes y usar [insertImage(byte[])](../../com.aspose.words/documentbuilder/\#insertImage-byte).

 **Examples:** 

Muestra cómo insertar una imagen desde un objeto en un documento.

```

 Document doc = new Document();
 DocumentBuilder builder = new DocumentBuilder(doc);

 String imageFile = getImageDir() + "Logo.jpg";

 // Below are three ways of inserting an image from an Image object instance.
 // 1 -  Inline shape with a default size based on the image's original dimensions:
 builder.insertImage(imageFile);

 builder.insertBreak(BreakType.PAGE_BREAK);

 // 2 -  Inline shape with custom dimensions:
 builder.insertImage(imageFile, ConvertUtil.pixelToPoint(250.0), ConvertUtil.pixelToPoint(144.0));

 builder.insertBreak(BreakType.PAGE_BREAK);

 // 3 -  Floating shape with custom dimensions:
 builder.insertImage(imageFile, RelativeHorizontalPosition.MARGIN, 100.0, RelativeVerticalPosition.MARGIN,
         100.0, 200.0, 100.0, WrapType.SQUARE);

 doc.save(getArtifactsDir() + "DocumentBuilderImages.InsertImageFromImageObject.docx");
 
```

**Parameters:**
| Parámetro | Tipo | Descripción |
| --- | --- | --- |
| imagen | java.awt.image.BufferedImage | La imagen a insertar en el documento. |
| ancho | double | El ancho de la imagen en puntos. Puede ser un valor negativo o cero para solicitar el 100 % de escala. |
| alto | double | La altura de la imagen en puntos. Puede ser un valor negativo o cero para solicitar el 100 % de escala. |

**Returns:**
[Shape](../../com.aspose.words/shape/) - The image node that was just inserted.
### insertImage(BufferedImage image, int horzPos, double left, int vertPos, double top, double width, double height, int wrapType) {#insertImage-java.awt.image.BufferedImage-int-double-int-double-double-double-int}
```
public Shape insertImage(BufferedImage image, int horzPos, double left, int vertPos, double top, double width, double height, int wrapType)
```




**Parameters:**
| Parámetro | Tipo | Descripción |
| --- | --- | --- |
| imagen | java.awt.image.BufferedImage |  |
| horzPos | int |  |
| izquierda | double |  |
| vertPos | int |  |
| superior | double |  |
| ancho | double |  |
| alto | double |  |
| wrapType | int |  |

**Returns:**
[Shape](../../com.aspose.words/shape/)
### insertImage(InputStream stream) {#insertImage-java.io.InputStream}
```
public Shape insertImage(InputStream stream)
```




**Parameters:**
| Parámetro | Tipo | Descripción |
| --- | --- | --- |
| stream | java.io.InputStream |  |

**Returns:**
[Shape](../../com.aspose.words/shape/)
### insertImage(InputStream stream, double width, double height) {#insertImage-java.io.InputStream-double-double}
```
public Shape insertImage(InputStream stream, double width, double height)
```




**Parameters:**
| Parámetro | Tipo | Descripción |
| --- | --- | --- |
| stream | java.io.InputStream |  |
| ancho | double |  |
| alto | double |  |

**Returns:**
[Shape](../../com.aspose.words/shape/)
### insertImage(InputStream stream, int horzPos, double left, int vertPos, double top, double width, double height, int wrapType) {#insertImage-java.io.InputStream-int-double-int-double-double-double-int}
```
public Shape insertImage(InputStream stream, int horzPos, double left, int vertPos, double top, double width, double height, int wrapType)
```




**Parameters:**
| Parámetro | Tipo | Descripción |
| --- | --- | --- |
| stream | java.io.InputStream |  |
| horzPos | int |  |
| izquierda | double |  |
| vertPos | int |  |
| superior | double |  |
| ancho | double |  |
| alto | double |  |
| wrapType | int |  |

**Returns:**
[Shape](../../com.aspose.words/shape/)
### insertImage(String fileName) {#insertImage-java.lang.String}
```
public Shape insertImage(String fileName)
```


Inserta una imagen desde un archivo o URL en el documento. La imagen se inserta en línea y al 100 % de escala.

 **Remarks:** 

Esta sobrecarga descargará automáticamente la imagen antes de insertarla en el documento si especifica una URI remota.

Puede cambiar el tamaño, la ubicación, el método de posicionamiento y otras configuraciones de la imagen usando el objeto [Shape](../../com.aspose.words/shape/) devuelto por este método.

 **Examples:** 

Muestra cómo insertar una imagen desde el sistema de archivos local en un documento.

```

 Document doc = new Document();
 DocumentBuilder builder = new DocumentBuilder(doc);

 // Below are three ways of inserting an image from a local system filename.
 // 1 -  Inline shape with a default size based on the image's original dimensions:
 builder.insertImage(getImageDir() + "Logo.jpg");

 builder.insertBreak(BreakType.PAGE_BREAK);

 // 2 -  Inline shape with custom dimensions:
 builder.insertImage(getImageDir() + "Transparent background logo.png", ConvertUtil.pixelToPoint(250.0),
         ConvertUtil.pixelToPoint(144.0));

 builder.insertBreak(BreakType.PAGE_BREAK);

 // 3 -  Floating shape with custom dimensions:
 builder.insertImage(getImageDir() + "Windows MetaFile.wmf", RelativeHorizontalPosition.MARGIN, 100.0,
         RelativeVerticalPosition.MARGIN, 100.0, 200.0, 100.0, WrapType.SQUARE);

 doc.save(getArtifactsDir() + "DocumentBuilderImages.InsertImageFromFilename.docx");
 
```

Muestra cómo determinar qué imagen se insertará.

```

 Document doc = new Document();
 DocumentBuilder builder = new DocumentBuilder(doc);

 builder.insertImage(getImageDir() + "Scalable Vector Graphics.svg");

 // Aspose.Words insert SVG image to the document as PNG with svgBlip extension
 // that contains the original vector SVG image representation.
 doc.save(getArtifactsDir() + "DocumentBuilderImages.InsertSvgImage.SvgWithSvgBlip.docx");

 // Aspose.Words insert SVG image to the document as PNG, just like Microsoft Word does for old format.
 doc.save(getArtifactsDir() + "DocumentBuilderImages.InsertSvgImage.Svg.doc");

 doc.getCompatibilityOptions().optimizeFor(MsWordVersion.WORD_2003);

 // Aspose.Words insert SVG image to the document as EMF metafile to keep the image in vector representation.
 doc.save(getArtifactsDir() + "DocumentBuilderImages.InsertSvgImage.Emf.docx");
 
```

Muestra cómo insertar una imagen GIF en el documento.

```

 DocumentBuilder builder = new DocumentBuilder();

 // We can insert gif image using path or bytes array.
 // It works only if DocumentBuilder optimized to Word version 2010 or higher.
 // Note, that access to the image bytes causes conversion Gif to Png.
 Shape gifImage = builder.insertImage(getImageDir() + "Graphics Interchange Format.gif");

 gifImage = builder.insertImage(DocumentHelper.getBytesFromStream(new FileInputStream(getImageDir() + "Graphics Interchange Format.gif")));

 builder.getDocument().save(getArtifactsDir() + "InsertGif.docx");
 
```

Muestra cómo insertar una forma con una imagen en un documento.

```

 Document doc = new Document();
 DocumentBuilder builder = new DocumentBuilder(doc);

 // Below are two locations where the document builder's "InsertShape" method
 // can source the image that the shape will display.
 // 1 -  Pass a local file system filename of an image file:
 builder.write("Image from local file: ");
 builder.insertImage(getImageDir() + "Logo.jpg");
 builder.writeln();

 // 2 -  Pass a URL which points to an image.
 builder.write("Image from a URL: ");
 builder.insertImage(getImageUri().toURL().openStream());
 builder.writeln();

 doc.save(getArtifactsDir() + "Image.FromUrl.docx");
 
```

Muestra cómo insertar una imagen flotante en el centro de una página.

```

 Document doc = new Document();
 DocumentBuilder builder = new DocumentBuilder(doc);

 // Insert a floating image that will appear behind the overlapping text and align it to the page's center.
 Shape shape = builder.insertImage(getImageDir() + "Logo.jpg");
 shape.setWrapType(WrapType.NONE);
 shape.setBehindText(true);
 shape.setRelativeHorizontalPosition(RelativeHorizontalPosition.PAGE);
 shape.setRelativeVerticalPosition(RelativeVerticalPosition.PAGE);
 shape.setHorizontalAlignment(HorizontalAlignment.CENTER);
 shape.setVerticalAlignment(VerticalAlignment.CENTER);

 doc.save(getArtifactsDir() + "Image.CreateFloatingPageCenter.docx");
 
```

Muestra cómo insertar una imagen WebP.

```

 Document doc = new Document();
 DocumentBuilder builder = new DocumentBuilder(doc);

 builder.insertImage(getImageDir() + "WebP image.webp");

 doc.save(getArtifactsDir() + "Image.InsertWebpImage.docx");
 
```

**Parameters:**
| Parámetro | Tipo | Descripción |
| --- | --- | --- |
| fileName | java.lang.String | El archivo con la imagen. Puede ser cualquier URI local o remoto válido. |

**Returns:**
[Shape](../../com.aspose.words/shape/) - The image node that was just inserted.
### insertImage(String fileName, double width, double height) {#insertImage-java.lang.String-double-double}
```
public Shape insertImage(String fileName, double width, double height)
```


Inserta una imagen en línea desde un archivo o URL en el documento y la escala al tamaño especificado.

 **Remarks:** 

Puede cambiar el tamaño, la ubicación, el método de posicionamiento y otras configuraciones de la imagen usando el objeto [Shape](../../com.aspose.words/shape/) devuelto por este método.

 **Examples:** 

Muestra cómo insertar una imagen desde el sistema de archivos local en un documento.

```

 Document doc = new Document();
 DocumentBuilder builder = new DocumentBuilder(doc);

 // Below are three ways of inserting an image from a local system filename.
 // 1 -  Inline shape with a default size based on the image's original dimensions:
 builder.insertImage(getImageDir() + "Logo.jpg");

 builder.insertBreak(BreakType.PAGE_BREAK);

 // 2 -  Inline shape with custom dimensions:
 builder.insertImage(getImageDir() + "Transparent background logo.png", ConvertUtil.pixelToPoint(250.0),
         ConvertUtil.pixelToPoint(144.0));

 builder.insertBreak(BreakType.PAGE_BREAK);

 // 3 -  Floating shape with custom dimensions:
 builder.insertImage(getImageDir() + "Windows MetaFile.wmf", RelativeHorizontalPosition.MARGIN, 100.0,
         RelativeVerticalPosition.MARGIN, 100.0, 200.0, 100.0, WrapType.SQUARE);

 doc.save(getArtifactsDir() + "DocumentBuilderImages.InsertImageFromFilename.docx");
 
```

**Parameters:**
| Parámetro | Tipo | Descripción |
| --- | --- | --- |
| fileName | java.lang.String | El archivo que contiene la imagen. |
| ancho | double | El ancho de la imagen en puntos. Puede ser un valor negativo o cero para solicitar el 100 % de escala. |
| alto | double | La altura de la imagen en puntos. Puede ser un valor negativo o cero para solicitar el 100 % de escala. |

**Returns:**
[Shape](../../com.aspose.words/shape/) - The image node that was just inserted.
### insertImage(String fileName, int horzPos, double left, int vertPos, double top, double width, double height, int wrapType) {#insertImage-java.lang.String-int-double-int-double-double-double-int}
```
public Shape insertImage(String fileName, int horzPos, double left, int vertPos, double top, double width, double height, int wrapType)
```




**Parameters:**
| Parámetro | Tipo | Descripción |
| --- | --- | --- |
| fileName | java.lang.String |  |
| horzPos | int |  |
| izquierda | double |  |
| vertPos | int |  |
| superior | double |  |
| ancho | double |  |
| alto | double |  |
| wrapType | int |  |

**Returns:**
[Shape](../../com.aspose.words/shape/)
### insertNode(Node node) {#insertNode-com.aspose.words.Node}
```
public void insertNode(Node node)
```


Inserta un nodo antes del cursor.

 **Examples:** 

Muestra cómo insertar una imagen enlazada en un documento.

```

 Document doc = new Document();
 DocumentBuilder builder = new DocumentBuilder(doc);

 String imageFileName = getImageDir() + "Windows MetaFile.wmf";

 // Below are two ways of applying an image to a shape so that it can display it.
 // 1 -  Set the shape to contain the image.
 Shape shape = new Shape(builder.getDocument(), ShapeType.IMAGE);
 shape.setWrapType(WrapType.INLINE);
 shape.getImageData().setImage(imageFileName);

 builder.insertNode(shape);

 doc.save(getArtifactsDir() + "Image.CreateLinkedImage.Embedded.docx");

 // Every image that we store in shape will increase the size of our document.
 Assert.assertTrue(new File(getArtifactsDir() + "Image.CreateLinkedImage.Embedded.docx").length() > 70000);

 doc.getFirstSection().getBody().getFirstParagraph().removeAllChildren();

 // 2 -  Set the shape to link to an image file in the local file system.
 shape = new Shape(builder.getDocument(), ShapeType.IMAGE);
 shape.setWrapType(WrapType.INLINE);
 shape.getImageData().setSourceFullName(imageFileName);

 builder.insertNode(shape);
 doc.save(getArtifactsDir() + "Image.CreateLinkedImage.Linked.docx");

 // Linking to images will save space and result in a smaller document.
 // However, the document can only display the image correctly while
 // the image file is present at the location that the shape's "SourceFullName" property points to.
 Assert.assertTrue(new File(getArtifactsDir() + "Image.CreateLinkedImage.Linked.docx").length() < 10000);
 
```

**Parameters:**
| Parámetro | Tipo | Descripción |
| --- | --- | --- |
| node | [Node](../../com.aspose.words/node/) |  |

### insertOleObject(InputStream stream, String progId, boolean asIcon, InputStream presentation) {#insertOleObject-java.io.InputStream-java.lang.String-boolean-java.io.InputStream}
```
public Shape insertOleObject(InputStream stream, String progId, boolean asIcon, InputStream presentation)
```




**Parameters:**
| Parámetro | Tipo | Descripción |
| --- | --- | --- |
| stream | java.io.InputStream |  |
| progId | java.lang.String |  |
| asIcon | boolean |  |
| presentation | java.io.InputStream |  |

**Returns:**
[Shape](../../com.aspose.words/shape/)
### insertOleObject(String fileName, boolean isLinked, boolean asIcon, InputStream presentation) {#insertOleObject-java.lang.String-boolean-boolean-java.io.InputStream}
```
public Shape insertOleObject(String fileName, boolean isLinked, boolean asIcon, InputStream presentation)
```




**Parameters:**
| Parámetro | Tipo | Descripción |
| --- | --- | --- |
| fileName | java.lang.String |  |
| isLinked | boolean |  |
| asIcon | boolean |  |
| presentation | java.io.InputStream |  |

**Returns:**
[Shape](../../com.aspose.words/shape/)
### insertOleObject(String fileName, String progId, boolean isLinked, boolean asIcon, InputStream presentation) {#insertOleObject-java.lang.String-java.lang.String-boolean-boolean-java.io.InputStream}
```
public Shape insertOleObject(String fileName, String progId, boolean isLinked, boolean asIcon, InputStream presentation)
```




**Parameters:**
| Parámetro | Tipo | Descripción |
| --- | --- | --- |
| fileName | java.lang.String |  |
| progId | java.lang.String |  |
| isLinked | boolean |  |
| asIcon | boolean |  |
| presentation | java.io.InputStream |  |

**Returns:**
[Shape](../../com.aspose.words/shape/)
### insertOleObjectAsIcon(InputStream stream, String progId, String iconFile, String iconCaption) {#insertOleObjectAsIcon-java.io.InputStream-java.lang.String-java.lang.String-java.lang.String}
```
public Shape insertOleObjectAsIcon(InputStream stream, String progId, String iconFile, String iconCaption)
```




**Parameters:**
| Parámetro | Tipo | Descripción |
| --- | --- | --- |
| stream | java.io.InputStream |  |
| progId | java.lang.String |  |
| iconFile | java.lang.String |  |
| iconCaption | java.lang.String |  |

**Returns:**
[Shape](../../com.aspose.words/shape/)
### insertOleObjectAsIcon(String fileName, boolean isLinked, String iconFile, String iconCaption) {#insertOleObjectAsIcon-java.lang.String-boolean-java.lang.String-java.lang.String}
```
public Shape insertOleObjectAsIcon(String fileName, boolean isLinked, String iconFile, String iconCaption)
```


Inserta un objeto OLE incrustado o vinculado como ícono en el documento. Permite especificar el archivo de ícono y la leyenda. Detecta el tipo de objeto OLE usando la extensión del archivo.

 **Examples:** 

Muestra cómo insertar un objeto OLE en un documento.

```

 Document doc = new Document();
 DocumentBuilder builder = new DocumentBuilder(doc);

 // OLE objects are links to files in our local file system that can be opened by other installed applications.
 // Double clicking these shapes will launch the application, and then use it to open the linked object.
 // There are three ways of using the InsertOleObject method to insert these shapes and configure their appearance.
 // If 'presentation' is omitted and 'asIcon' is set, this overloaded method selects
 // the icon according to the file extension and uses the filename for the icon caption.
 // 1 -  Image taken from the local file system:
 builder.insertOleObject(getMyDir() + "Spreadsheet.xlsx", false, false, new FileInputStream(getImageDir() + "Logo.jpg"));

 // If 'presentation' is omitted and 'asIcon' is set, this overloaded method selects
 // the icon according to 'progId' and uses the filename for the icon caption.
 // 2 -  Icon based on the application that will open the object:
 builder.insertOleObject(getMyDir() + "Spreadsheet.xlsx", "Excel.Sheet", false, true, new FileInputStream(getImageDir() + "Logo.jpg"));

 // If 'iconFile' and 'iconCaption' are omitted, this overloaded method selects
 // the icon according to 'progId' and uses the predefined icon caption.
 // 3 -  Image icon that's 32 x 32 pixels or smaller from the local file system, with a custom caption:
 builder.insertOleObjectAsIcon(getMyDir() + "Presentation.pptx", false, getImageDir() + "Logo icon.ico",
         "Double click to view presentation!");

 doc.save(getArtifactsDir() + "DocumentBuilder.InsertOleObject.docx");
 
```

**Parameters:**
| Parámetro | Tipo | Descripción |
| --- | --- | --- |
| fileName | java.lang.String | Ruta completa al archivo. |
| isLinked | boolean | Si  true  entonces se inserta un objeto OLE vinculado; de lo contrario se inserta un objeto OLE incrustado. |
| iconFile | java.lang.String | Ruta completa al archivo ICO. Si el valor es  null , Aspose.Words usará una imagen predefinida. |
| iconCaption | java.lang.String | Leyenda del ícono. Si el valor es  null , Aspose.Words usará el nombre del archivo. |

**Returns:**
[Shape](../../com.aspose.words/shape/) - Shape node containing Ole object and inserted at the current Builder position.
### insertOleObjectAsIcon(String fileName, String progId, boolean isLinked, String iconFile, String iconCaption) {#insertOleObjectAsIcon-java.lang.String-java.lang.String-boolean-java.lang.String-java.lang.String}
```
public Shape insertOleObjectAsIcon(String fileName, String progId, boolean isLinked, String iconFile, String iconCaption)
```


Inserta un objeto OLE incrustado o vinculado como ícono en el documento. Permite especificar el archivo de ícono y la leyenda. Detecta el tipo de objeto OLE usando el parámetro progID proporcionado.

 **Examples:** 

Muestra cómo insertar un objeto OLE incrustado o vinculado como ícono en el documento.

```

 Document doc = new Document();
 DocumentBuilder builder = new DocumentBuilder(doc);

 // If 'iconFile' and 'iconCaption' are omitted, this overloaded method selects
 // the icon according to 'progId' and uses the filename for the icon caption.
 builder.insertOleObjectAsIcon(getMyDir() + "Presentation.pptx", "Package", false, getImageDir() + "Logo icon.ico", "My embedded file");

 builder.insertBreak(BreakType.LINE_BREAK);

 try (FileInputStream stream = new FileInputStream(getMyDir() + "Presentation.pptx")) {
     // If 'iconFile' and 'iconCaption' are omitted, this overloaded method selects
     // the icon according to the file extension and uses the filename for the icon caption.
     Shape shape = builder.insertOleObjectAsIcon(stream, "PowerPoint.Application", getImageDir() + "Logo icon.ico",
             "My embedded file stream");

     OlePackage setOlePackage = shape.getOleFormat().getOlePackage();
     setOlePackage.setFileName("Presentation.pptx");
     setOlePackage.setDisplayName("Presentation.pptx");
 }

 doc.save(getArtifactsDir() + "DocumentBuilder.InsertOleObjectAsIcon.docx");
 
```

**Parameters:**
| Parámetro | Tipo | Descripción |
| --- | --- | --- |
| fileName | java.lang.String | Ruta completa al archivo. |
| progId | java.lang.String | ProgId del objeto OLE. |
| isLinked | boolean | Si  true  entonces se inserta un objeto OLE vinculado; de lo contrario se inserta un objeto OLE incrustado. |
| iconFile | java.lang.String | Ruta completa al archivo ICO. Si el valor es  null , Aspose.Words usará una imagen predefinida. |
| iconCaption | java.lang.String | Leyenda del ícono. Si el valor es  null , Aspose.Words usará el nombre del archivo. |

**Returns:**
[Shape](../../com.aspose.words/shape/) - Shape node containing Ole object and inserted at the current Builder position.
### insertOnlineVideo(String videoUrl, double width, double height) {#insertOnlineVideo-java.lang.String-double-double}
```
public Shape insertOnlineVideo(String videoUrl, double width, double height)
```


Inserta un objeto de video en línea en el documento y lo escala al tamaño especificado.

 **Remarks:** 

Puede cambiar el tamaño, la ubicación, el método de posicionamiento y otras configuraciones de la imagen usando el objeto [Shape](../../com.aspose.words/shape/) devuelto por este método.

Se admite la inserción de video en línea de los siguientes recursos:

 *  https://www.youtube.com/
 *  https://vimeo.com/

Si su video en línea no se muestra correctamente, use [insertOnlineVideo(java.lang.String, java.lang.String, byte[], double, double)](../../com.aspose.words/documentbuilder/\#insertOnlineVideo-java.lang.String--java.lang.String--byte----double--double), que acepta código HTML incrustado personalizado.

El código para incrustar video puede variar entre proveedores; consulte al proveedor correspondiente de su elección para obtener detalles.

 **Examples:** 

Muestra cómo insertar un video en línea en un documento usando una URL.

```

 Document doc = new Document();
 DocumentBuilder builder = new DocumentBuilder(doc);

 builder.insertOnlineVideo("https://youtu.be/g1N9ke8Prmk", 360.0, 270.0);

 // We can watch the video from Microsoft Word by clicking on the shape.
 doc.save(getArtifactsDir() + "DocumentBuilder.InsertVideoWithUrl.docx");
 
```

**Parameters:**
| Parámetro | Tipo | Descripción |
| --- | --- | --- |
| videoUrl | java.lang.String | La URL del video. |
| ancho | double | El ancho de la imagen en puntos. Puede ser un valor negativo o cero para solicitar el 100 % de escala. |
| alto | double | La altura de la imagen en puntos. Puede ser un valor negativo o cero para solicitar el 100 % de escala. |

**Returns:**
[Shape](../../com.aspose.words/shape/) - The image node that was just inserted.
### insertOnlineVideo(String videoUrl, int horzPos, double left, int vertPos, double top, double width, double height, int wrapType) {#insertOnlineVideo-java.lang.String-int-double-int-double-double-double-int}
```
public Shape insertOnlineVideo(String videoUrl, int horzPos, double left, int vertPos, double top, double width, double height, int wrapType)
```




**Parameters:**
| Parámetro | Tipo | Descripción |
| --- | --- | --- |
| videoUrl | java.lang.String |  |
| horzPos | int |  |
| izquierda | double |  |
| vertPos | int |  |
| superior | double |  |
| ancho | double |  |
| alto | double |  |
| wrapType | int |  |

**Returns:**
[Shape](../../com.aspose.words/shape/)
### insertOnlineVideo(String videoUrl, String videoEmbedCode, byte[] thumbnailImageBytes, double width, double height) {#insertOnlineVideo-java.lang.String-java.lang.String-byte---double-double}
```
public Shape insertOnlineVideo(String videoUrl, String videoEmbedCode, byte[] thumbnailImageBytes, double width, double height)
```


Inserta un objeto de video en línea en el documento y lo escala al tamaño especificado.

 **Remarks:** 

Puede cambiar el tamaño, la ubicación, el método de posicionamiento y otras configuraciones de la imagen usando el objeto [Shape](../../com.aspose.words/shape/) devuelto por este método.

 **Examples:** 

Muestra cómo insertar un video en línea en un documento con una miniatura personalizada.

```

 Document doc = new Document();
 DocumentBuilder builder = new DocumentBuilder(doc);

 String videoUrl = "https://vimeo.com/52477838";
 String videoEmbedCode = "";

 byte[] thumbnailImageBytes = IOUtils.toByteArray(getImageUri().toURL().openStream());

 BufferedImage image = ImageIO.read(new ByteArrayInputStream(thumbnailImageBytes));

 // Below are two ways of creating a shape with a custom thumbnail, which links to an online video
 // that will play when we click on the shape in Microsoft Word.
 // 1 -  Insert an inline shape at the builder's node insertion cursor:
 builder.insertOnlineVideo(videoUrl, videoEmbedCode, thumbnailImageBytes, image.getWidth(), image.getHeight());

 builder.insertBreak(BreakType.PAGE_BREAK);

 // 2 -  Insert a floating shape:
 double left = builder.getPageSetup().getRightMargin() - image.getWidth();
 double top = builder.getPageSetup().getBottomMargin() - image.getHeight();

 builder.insertOnlineVideo(videoUrl, videoEmbedCode, thumbnailImageBytes,
         RelativeHorizontalPosition.RIGHT_MARGIN, left, RelativeVerticalPosition.BOTTOM_MARGIN, top,
         image.getWidth(), image.getHeight(), WrapType.SQUARE);

 doc.save(getArtifactsDir() + "DocumentBuilder.InsertOnlineVideoCustomThumbnail.docx");
 
```

**Parameters:**
| Parámetro | Tipo | Descripción |
| --- | --- | --- |
| videoUrl | java.lang.String | La URL del video. |
| videoEmbedCode | java.lang.String | El código incrustado del video. |
| thumbnailImageBytes | byte[] | Los bytes de la imagen de miniatura. |
| ancho | double | El ancho de la imagen en puntos. Puede ser un valor negativo o cero para solicitar el 100 % de escala. |
| alto | double | La altura de la imagen en puntos. Puede ser un valor negativo o cero para solicitar el 100 % de escala. |

**Returns:**
[Shape](../../com.aspose.words/shape/) - The image node that was just inserted.
### insertOnlineVideo(String videoUrl, String videoEmbedCode, byte[] thumbnailImageBytes, int horzPos, double left, int vertPos, double top, double width, double height, int wrapType) {#insertOnlineVideo-java.lang.String-java.lang.String-byte---int-double-int-double-double-double-int}
```
public Shape insertOnlineVideo(String videoUrl, String videoEmbedCode, byte[] thumbnailImageBytes, int horzPos, double left, int vertPos, double top, double width, double height, int wrapType)
```




**Parameters:**
| Parámetro | Tipo | Descripción |
| --- | --- | --- |
| videoUrl | java.lang.String |  |
| videoEmbedCode | java.lang.String |  |
| thumbnailImageBytes | byte[] |  |
| horzPos | int |  |
| izquierda | double |  |
| vertPos | int |  |
| superior | double |  |
| ancho | double |  |
| alto | double |  |
| wrapType | int |  |

**Returns:**
[Shape](../../com.aspose.words/shape/)
### insertParagraph() {#insertParagraph}
```
public Paragraph insertParagraph()
```


Inserta un salto de párrafo en el documento.

 **Remarks:** 

Se utiliza el formato de párrafo actual especificado por la propiedad [getParagraphFormat()](../../com.aspose.words/documentbuilder/\#getParagraphFormat).

Divide el párrafo actual en dos. Después de insertar el párrafo, el cursor se coloca al comienzo del nuevo párrafo.

Se lanza una excepción si no es posible insertar un salto de párrafo en la posición actual del cursor.

 **Examples:** 

Muestra cómo insertar un párrafo en el documento.

```

 Document doc = new Document();
 DocumentBuilder builder = new DocumentBuilder(doc);

 Font font = builder.getFont();
 font.setSize(16.0);
 font.setBold(true);
 font.setColor(Color.BLUE);
 font.setName("Arial");
 font.setUnderline(Underline.DASH);

 ParagraphFormat paragraphFormat = builder.getParagraphFormat();
 paragraphFormat.setFirstLineIndent(8.0);
 paragraphFormat.setAlignment(ParagraphAlignment.JUSTIFY);
 paragraphFormat.setAddSpaceBetweenFarEastAndAlpha(true);
 paragraphFormat.setAddSpaceBetweenFarEastAndDigit(true);
 paragraphFormat.setKeepTogether(true);

 // The "Writeln" method ends the paragraph after appending text
 // and then starts a new line, adding a new paragraph.
 builder.writeln("Hello world!");

 Assert.assertTrue(builder.getCurrentParagraph().isEndOfDocument());
 
```

**Returns:**
[Paragraph](../../com.aspose.words/paragraph/) - The paragraph node that was just inserted. It is the same node as [getCurrentParagraph()](../../com.aspose.words/documentbuilder/\#getCurrentParagraph).
### insertShape(int shapeType, double width, double height) {#insertShape-int-double-double}
```
public Shape insertShape(int shapeType, double width, double height)
```




**Parameters:**
| Parámetro | Tipo | Descripción |
| --- | --- | --- |
| shapeType | int |  |
| ancho | double |  |
| alto | double |  |

**Returns:**
[Shape](../../com.aspose.words/shape/)
### insertShape(int shapeType, int horzPos, double left, int vertPos, double top, double width, double height, int wrapType) {#insertShape-int-int-double-int-double-double-double-int}
```
public Shape insertShape(int shapeType, int horzPos, double left, int vertPos, double top, double width, double height, int wrapType)
```




**Parameters:**
| Parámetro | Tipo | Descripción |
| --- | --- | --- |
| shapeType | int |  |
| horzPos | int |  |
| izquierda | double |  |
| vertPos | int |  |
| superior | double |  |
| ancho | double |  |
| alto | double |  |
| wrapType | int |  |

**Returns:**
[Shape](../../com.aspose.words/shape/)
### insertSignatureLine(SignatureLineOptions signatureLineOptions) {#insertSignatureLine-com.aspose.words.SignatureLineOptions}
```
public Shape insertSignatureLine(SignatureLineOptions signatureLineOptions)
```


Inserta una línea de firma en la posición actual.

 **Examples:** 

Muestra cómo firmar un documento con un certificado personal y una línea de firma.

```

 Document doc = new Document();
 DocumentBuilder builder = new DocumentBuilder(doc);

 SignatureLineOptions signatureLineOptions = new SignatureLineOptions();
 signatureLineOptions.setSigner("vderyushev");
 signatureLineOptions.setSignerTitle("QA");
 signatureLineOptions.setEmail("vderyushev@aspose.com");
 signatureLineOptions.setShowDate(true);
 signatureLineOptions.setDefaultInstructions(false);
 signatureLineOptions.setInstructions("Please sign here.");
 signatureLineOptions.setAllowComments(true);

 SignatureLine signatureLine = builder.insertSignatureLine(signatureLineOptions).getSignatureLine();
 signatureLine.setProviderId(UUID.fromString("CF5A7BB4-8F3C-4756-9DF6-BEF7F13259A2"));

 Assert.assertFalse(signatureLine.isSigned());
 Assert.assertFalse(signatureLine.isValid());

 doc.save(getArtifactsDir() + "DocumentBuilder.SignatureLineProviderId.docx");

 Date currentDate = new Date();

 SignOptions signOptions = new SignOptions();
 signOptions.setSignatureLineId(signatureLine.getId());
 signOptions.setProviderId(signatureLine.getProviderId());
 signOptions.setComments("Document was signed by vderyushev");
 signOptions.setSignTime(currentDate);

 CertificateHolder certHolder = CertificateHolder.create(getMyDir() + "morzal.pfx", "aw");

 DigitalSignatureUtil.sign(getArtifactsDir() + "DocumentBuilder.SignatureLineProviderId.docx",
         getArtifactsDir() + "DocumentBuilder.SignatureLineProviderId.Signed.docx", certHolder, signOptions);

 // Re-open our saved document, and verify that the "IsSigned" and "IsValid" properties both equal "true",
 // indicating that the signature line contains a signature.
 doc = new Document(getArtifactsDir() + "DocumentBuilder.SignatureLineProviderId.Signed.docx");
 Shape shape = (Shape) doc.getChild(NodeType.SHAPE, 0, true);
 signatureLine = shape.getSignatureLine();

 Assert.assertTrue(signatureLine.isSigned());
 Assert.assertTrue(signatureLine.isValid());
 
```

**Parameters:**
| Parámetro | Tipo | Descripción |
| --- | --- | --- |
| signatureLineOptions | [SignatureLineOptions](../../com.aspose.words/signaturelineoptions/) | El objeto que almacena los parámetros para crear una línea de firma. |

**Returns:**
[Shape](../../com.aspose.words/shape/) - The signature line node that was just inserted.
### insertSignatureLine(SignatureLineOptions signatureLineOptions, int horzPos, double left, int vertPos, double top, int wrapType) {#insertSignatureLine-com.aspose.words.SignatureLineOptions-int-double-int-double-int}
```
public Shape insertSignatureLine(SignatureLineOptions signatureLineOptions, int horzPos, double left, int vertPos, double top, int wrapType)
```




**Parameters:**
| Parámetro | Tipo | Descripción |
| --- | --- | --- |
| signatureLineOptions | [SignatureLineOptions](../../com.aspose.words/signaturelineoptions/) |  |
| horzPos | int |  |
| izquierda | double |  |
| vertPos | int |  |
| superior | double |  |
| wrapType | int |  |

**Returns:**
[Shape](../../com.aspose.words/shape/)
### insertStructuredDocumentTag(int type) {#insertStructuredDocumentTag-int}
```
public StructuredDocumentTag insertStructuredDocumentTag(int type)
```




**Parameters:**
| Parámetro | Tipo | Descripción |
| --- | --- | --- |
| tipo | int |  |

**Returns:**
[StructuredDocumentTag](../../com.aspose.words/structureddocumenttag/)
### insertStyleSeparator() {#insertStyleSeparator}
```
public void insertStyleSeparator()
```


Inserta un separador de estilo en el documento.

 **Remarks:** 

Este método permite aplicar diferentes estilos de párrafo a dos partes distintas de una línea de texto.

 **Examples:** 

Muestra cómo trabajar con separadores de estilo.

```

 Document doc = new Document();
 DocumentBuilder builder = new DocumentBuilder(doc);

 // Each paragraph can only have one style.
 // The InsertStyleSeparator method allows us to work around this limitation.
 builder.getParagraphFormat().setStyleIdentifier(StyleIdentifier.HEADING_1);
 builder.write("This text is in a Heading style. ");
 builder.insertStyleSeparator();

 Style paraStyle = builder.getDocument().getStyles().add(StyleType.PARAGRAPH, "MyParaStyle");
 paraStyle.getFont().setBold(false);
 paraStyle.getFont().setSize(8.0);
 paraStyle.getFont().setName("Arial");

 builder.getParagraphFormat().setStyleName(paraStyle.getName());
 builder.write("This text is in a custom style. ");

 // Calling the InsertStyleSeparator method creates another paragraph,
 // which can have a different style to the previous. There will be no break between paragraphs.
 // The text in the output document will look like one paragraph with two styles.
 Assert.assertEquals(2, doc.getFirstSection().getBody().getParagraphs().getCount());
 Assert.assertEquals("Heading 1", doc.getFirstSection().getBody().getParagraphs().get(0).getParagraphFormat().getStyle().getName());
 Assert.assertEquals("MyParaStyle", doc.getFirstSection().getBody().getParagraphs().get(1).getParagraphFormat().getStyle().getName());

 doc.save(getArtifactsDir() + "DocumentBuilder.InsertStyleSeparator.docx");
 
```

### insertTableOfContents(String switches) {#insertTableOfContents-java.lang.String}
```
public Field insertTableOfContents(String switches)
```


Inserta un campo TOC (tabla de contenido) en el documento.

 **Remarks:** 

Este método inserta un campo TOC (tabla de contenido) en el documento en la posición actual.

Una tabla de contenido en un documento de Word puede construirse de varias maneras y formatearse usando una variedad de opciones. La forma en que la tabla se construye y muestra en Microsoft Word está controlada por los interruptores de campo.

La forma más fácil de especificar los interruptores es insertar y configurar una tabla de contenido en un documento de Word usando el menú Insertar->Referencia->Índice y tablas, luego activar la visualización de códigos de campo para ver los interruptores. Puedes presionar Alt+F9 en Microsoft Word para alternar la visualización de los códigos de campo.

Por ejemplo, después de crear una tabla de contenido, el siguiente campo se inserta en el documento: **\{ TOC \\o \"1-3\" \\h \\z \}**. Puedes copiar **\\o \"1-3\" \\h \\z** y usarlo como parámetro de los interruptores.

Ten en cuenta que [insertTableOfContents(java.lang.String)](../../com.aspose.words/documentbuilder/\#insertTableOfContents-java.lang.String) solo insertará un campo TOC, pero no construirá realmente la tabla de contenido. La tabla de contenido es construida por Microsoft Word cuando se actualiza el campo.

Si insertas una tabla de contenido usando este método y luego abres el archivo en Microsoft Word, no verás la tabla de contenido porque el campo TOC aún no se ha actualizado.

En Microsoft Word, los campos no se actualizan automáticamente al abrir un documento, pero puedes actualizar los campos en cualquier momento presionando F9.

 **Examples:** 

Muestra cómo insertar una tabla de contenido (TOC) en un documento usando estilos de encabezado como entradas.

```

 Document doc = new Document();
 DocumentBuilder builder = new DocumentBuilder(doc);

 // Insert a table of contents for the first page of the document.
 // Configure the table to pick up paragraphs with headings of levels 1 to 3.
 // Also, set its entries to be hyperlinks that will take us
 // to the location of the heading when left-clicked in Microsoft Word.
 builder.insertTableOfContents("\\o \"1-3\" \\h \\z \\u");
 builder.insertBreak(BreakType.PAGE_BREAK);

 // Populate the table of contents by adding paragraphs with heading styles.
 // Each such heading with a level between 1 and 3 will create an entry in the table.
 builder.getParagraphFormat().setStyleIdentifier(StyleIdentifier.HEADING_1);
 builder.writeln("Heading 1");

 builder.getParagraphFormat().setStyleIdentifier(StyleIdentifier.HEADING_2);
 builder.writeln("Heading 1.1");
 builder.writeln("Heading 1.2");

 builder.getParagraphFormat().setStyleIdentifier(StyleIdentifier.HEADING_1);
 builder.writeln("Heading 2");
 builder.writeln("Heading 3");

 builder.getParagraphFormat().setStyleIdentifier(StyleIdentifier.HEADING_2);
 builder.writeln("Heading 3.1");

 builder.getParagraphFormat().setStyleIdentifier(StyleIdentifier.HEADING_3);
 builder.writeln("Heading 3.1.1");
 builder.writeln("Heading 3.1.2");
 builder.writeln("Heading 3.1.3");

 builder.getParagraphFormat().setStyleIdentifier(StyleIdentifier.HEADING_4);
 builder.writeln("Heading 3.1.3.1");
 builder.writeln("Heading 3.1.3.2");

 builder.getParagraphFormat().setStyleIdentifier(StyleIdentifier.HEADING_2);
 builder.writeln("Heading 3.2");
 builder.writeln("Heading 3.3");

 // A table of contents is a field of a type that needs to be updated to show an up-to-date result.
 doc.updateFields();
 doc.save(getArtifactsDir() + "DocumentBuilder.InsertToc.docx");
 
```

**Parameters:**
| Parámetro | Tipo | Descripción |
| --- | --- | --- |
| interruptores | java.lang.String | Los interruptores del campo TOC. |

**Returns:**
[Field](../../com.aspose.words/field/)
### insertTextInput(String name, int type, String format, String fieldValue, int maxLength) {#insertTextInput-java.lang.String-int-java.lang.String-java.lang.String-int}
```
public FormField insertTextInput(String name, int type, String format, String fieldValue, int maxLength)
```




**Parameters:**
| Parámetro | Tipo | Descripción |
| --- | --- | --- |
| nombre | java.lang.String |  |
| tipo | int |  |
| formato | java.lang.String |  |
| fieldValue | java.lang.String |  |
| maxLength | int |  |

**Returns:**
[FormField](../../com.aspose.words/formfield/)
### isAtEndOfParagraph() {#isAtEndOfParagraph}
```
public boolean isAtEndOfParagraph()
```


Devuelve  true  si el cursor está al final del párrafo actual.

 **Examples:** 

Muestra cómo mover el cursor de un document builder a diferentes nodos en un documento.

```

 Document doc = new Document();
 DocumentBuilder builder = new DocumentBuilder(doc);

 // Create a valid bookmark, an entity that consists of nodes enclosed by a bookmark start node,
 // and a bookmark end node.
 builder.startBookmark("MyBookmark");
 builder.write("Bookmark contents.");
 builder.endBookmark("MyBookmark");

 NodeCollection firstParagraphNodes = doc.getFirstSection().getBody().getFirstParagraph().getChildNodes(NodeType.ANY, false);

 Assert.assertEquals(NodeType.BOOKMARK_START, firstParagraphNodes.get(0).getNodeType());
 Assert.assertEquals(NodeType.RUN, firstParagraphNodes.get(1).getNodeType());
 Assert.assertEquals("Bookmark contents.", firstParagraphNodes.get(1).getText().trim());
 Assert.assertEquals(NodeType.BOOKMARK_END, firstParagraphNodes.get(2).getNodeType());

 // The document builder's cursor is always ahead of the node that we last added with it.
 // If the builder's cursor is at the end of the document, its current node will be null.
 // The previous node is the bookmark end node that we last added.
 // Adding new nodes with the builder will append them to the last node.
 Assert.assertNull(builder.getCurrentNode());

 // If we wish to edit a different part of the document with the builder,
 // we will need to bring its cursor to the node we wish to edit.
 builder.moveToBookmark("MyBookmark");

 // Moving it to a bookmark will move it to the first node within the bookmark start and end nodes, the enclosed run.
 Assert.assertEquals(firstParagraphNodes.get(1), builder.getCurrentNode());

 // We can also move the cursor to an individual node like this.
 builder.moveTo(doc.getFirstSection().getBody().getFirstParagraph().getChildNodes(NodeType.ANY, false).get(0));

 Assert.assertEquals(NodeType.BOOKMARK_START, builder.getCurrentNode().getNodeType());
 Assert.assertEquals(doc.getFirstSection().getBody().getFirstParagraph(), builder.getCurrentParagraph());
 Assert.assertTrue(builder.isAtStartOfParagraph());

 // We can use specific methods to move to the start/end of a document.
 builder.moveToDocumentEnd();

 Assert.assertTrue(builder.isAtEndOfParagraph());

 builder.moveToDocumentStart();

 Assert.assertTrue(builder.isAtStartOfParagraph());
 
```

**Returns:**
boolean -  true  si el cursor está al final del párrafo actual.
### isAtEndOfStructuredDocumentTag() {#isAtEndOfStructuredDocumentTag}
```
public boolean isAtEndOfStructuredDocumentTag()
```


Devuelve **true** si el cursor está al final de una etiqueta de documento estructurado.

 **Examples:** 

Muestra cómo mover el cursor de DocumentBuilder dentro de una etiqueta de documento estructurado.

```

 Document doc = new Document(getMyDir() + "Structured document tags.docx");
 DocumentBuilder builder = new DocumentBuilder(doc);

 // There is a several ways to move the cursor:
 // 1 -  Move to the first character of structured document tag by index.
 builder.moveToStructuredDocumentTag(1, 1);

 // 2 -  Move to the first character of structured document tag by object.
 StructuredDocumentTag tag = (StructuredDocumentTag)doc.getChild(NodeType.STRUCTURED_DOCUMENT_TAG, 2, true);
 builder.moveToStructuredDocumentTag(tag, 1);
 builder.write(" New text.");

 Assert.assertEquals("R New text.ichText", tag.getText().trim());

 // 3 -  Move to the end of the second structured document tag.
 builder.moveToStructuredDocumentTag(1, -1);
 Assert.assertTrue(builder.isAtEndOfStructuredDocumentTag());

 // Get currently selected structured document tag.
 builder.getCurrentStructuredDocumentTag().setColor(Color.GREEN);

 doc.save(getArtifactsDir() + "Document.MoveToStructuredDocumentTag.docx");
 
```

**Returns:**
boolean - **true** si el cursor está al final de una etiqueta de documento estructurado.
### isAtStartOfParagraph() {#isAtStartOfParagraph}
```
public boolean isAtStartOfParagraph()
```


Devuelve  true  si el cursor está al comienzo del párrafo actual (no hay texto antes del cursor).

 **Examples:** 

Muestra cómo mover el cursor de un document builder a diferentes nodos en un documento.

```

 Document doc = new Document();
 DocumentBuilder builder = new DocumentBuilder(doc);

 // Create a valid bookmark, an entity that consists of nodes enclosed by a bookmark start node,
 // and a bookmark end node.
 builder.startBookmark("MyBookmark");
 builder.write("Bookmark contents.");
 builder.endBookmark("MyBookmark");

 NodeCollection firstParagraphNodes = doc.getFirstSection().getBody().getFirstParagraph().getChildNodes(NodeType.ANY, false);

 Assert.assertEquals(NodeType.BOOKMARK_START, firstParagraphNodes.get(0).getNodeType());
 Assert.assertEquals(NodeType.RUN, firstParagraphNodes.get(1).getNodeType());
 Assert.assertEquals("Bookmark contents.", firstParagraphNodes.get(1).getText().trim());
 Assert.assertEquals(NodeType.BOOKMARK_END, firstParagraphNodes.get(2).getNodeType());

 // The document builder's cursor is always ahead of the node that we last added with it.
 // If the builder's cursor is at the end of the document, its current node will be null.
 // The previous node is the bookmark end node that we last added.
 // Adding new nodes with the builder will append them to the last node.
 Assert.assertNull(builder.getCurrentNode());

 // If we wish to edit a different part of the document with the builder,
 // we will need to bring its cursor to the node we wish to edit.
 builder.moveToBookmark("MyBookmark");

 // Moving it to a bookmark will move it to the first node within the bookmark start and end nodes, the enclosed run.
 Assert.assertEquals(firstParagraphNodes.get(1), builder.getCurrentNode());

 // We can also move the cursor to an individual node like this.
 builder.moveTo(doc.getFirstSection().getBody().getFirstParagraph().getChildNodes(NodeType.ANY, false).get(0));

 Assert.assertEquals(NodeType.BOOKMARK_START, builder.getCurrentNode().getNodeType());
 Assert.assertEquals(doc.getFirstSection().getBody().getFirstParagraph(), builder.getCurrentParagraph());
 Assert.assertTrue(builder.isAtStartOfParagraph());

 // We can use specific methods to move to the start/end of a document.
 builder.moveToDocumentEnd();

 Assert.assertTrue(builder.isAtEndOfParagraph());

 builder.moveToDocumentStart();

 Assert.assertTrue(builder.isAtStartOfParagraph());
 
```

**Returns:**
boolean -  true  si el cursor está al comienzo del párrafo actual (no hay texto antes del cursor).
### moveTo(Node node) {#moveTo-com.aspose.words.Node}
```
public void moveTo(Node node)
```


Mueve el cursor a un nodo en línea o al final de un párrafo.

 **Remarks:** 

Cuando *node* es un nodo de nivel en línea, el cursor se mueve a este nodo y el contenido adicional se insertará antes de ese nodo.

Cuando *node* es un [Paragraph](../../com.aspose.words/paragraph/), el cursor se mueve al final del párrafo y el contenido adicional se insertará justo antes del salto de párrafo.

Cuando *node* es un nodo de nivel de bloque pero no un [Paragraph](../../com.aspose.words/paragraph/), el cursor se mueve al final del primer párrafo dentro del nodo de nivel de bloque y el contenido adicional se insertará justo antes del salto de párrafo.

 **Examples:** 

Muestra cómo mover el cursor de un document builder a diferentes nodos en un documento.

```

 Document doc = new Document();
 DocumentBuilder builder = new DocumentBuilder(doc);

 // Create a valid bookmark, an entity that consists of nodes enclosed by a bookmark start node,
 // and a bookmark end node.
 builder.startBookmark("MyBookmark");
 builder.write("Bookmark contents.");
 builder.endBookmark("MyBookmark");

 NodeCollection firstParagraphNodes = doc.getFirstSection().getBody().getFirstParagraph().getChildNodes(NodeType.ANY, false);

 Assert.assertEquals(NodeType.BOOKMARK_START, firstParagraphNodes.get(0).getNodeType());
 Assert.assertEquals(NodeType.RUN, firstParagraphNodes.get(1).getNodeType());
 Assert.assertEquals("Bookmark contents.", firstParagraphNodes.get(1).getText().trim());
 Assert.assertEquals(NodeType.BOOKMARK_END, firstParagraphNodes.get(2).getNodeType());

 // The document builder's cursor is always ahead of the node that we last added with it.
 // If the builder's cursor is at the end of the document, its current node will be null.
 // The previous node is the bookmark end node that we last added.
 // Adding new nodes with the builder will append them to the last node.
 Assert.assertNull(builder.getCurrentNode());

 // If we wish to edit a different part of the document with the builder,
 // we will need to bring its cursor to the node we wish to edit.
 builder.moveToBookmark("MyBookmark");

 // Moving it to a bookmark will move it to the first node within the bookmark start and end nodes, the enclosed run.
 Assert.assertEquals(firstParagraphNodes.get(1), builder.getCurrentNode());

 // We can also move the cursor to an individual node like this.
 builder.moveTo(doc.getFirstSection().getBody().getFirstParagraph().getChildNodes(NodeType.ANY, false).get(0));

 Assert.assertEquals(NodeType.BOOKMARK_START, builder.getCurrentNode().getNodeType());
 Assert.assertEquals(doc.getFirstSection().getBody().getFirstParagraph(), builder.getCurrentParagraph());
 Assert.assertTrue(builder.isAtStartOfParagraph());

 // We can use specific methods to move to the start/end of a document.
 builder.moveToDocumentEnd();

 Assert.assertTrue(builder.isAtEndOfParagraph());

 builder.moveToDocumentStart();

 Assert.assertTrue(builder.isAtStartOfParagraph());
 
```

Muestra cómo mover la posición del cursor de un DocumentBuilder a un nodo especificado.

```

 Document doc = new Document();
 DocumentBuilder builder = new DocumentBuilder(doc);
 builder.writeln("Run 1. ");

 // The document builder has a cursor, which acts as the part of the document
 // where the builder appends new nodes when we use its document construction methods.
 // This cursor functions in the same way as Microsoft Word's blinking cursor,
 // and it also always ends up immediately after any node that the builder just inserted.
 // To append content to a different part of the document,
 // we can move the cursor to a different node with the "MoveTo" method.
 builder.moveTo(doc.getFirstSection().getBody().getFirstParagraph().getRuns().get(0));
 // The cursor is now in front of the node that we moved it to.
 // Adding a second run will insert it in front of the first run.
 builder.writeln("Run 2. ");

 Assert.assertEquals("Run 2. \rRun 1.", doc.getText().trim());

 // Move the cursor to the end of the document to continue appending text to the end as before.
 builder.moveTo(doc.getLastSection().getBody().getLastParagraph());
 builder.writeln("Run 3. ");

 Assert.assertEquals("Run 2. \rRun 1. \rRun 3.", doc.getText().trim());
 
```

**Parameters:**
| Parámetro | Tipo | Descripción |
| --- | --- | --- |
| node | [Node](../../com.aspose.words/node/) | El nodo debe ser un párrafo o un hijo directo de un párrafo. |

### moveToBookmark(String bookmarkName) {#moveToBookmark-java.lang.String}
```
public boolean moveToBookmark(String bookmarkName)
```


Mueve el cursor a un marcador.

 **Remarks:** 

Mueve el cursor a una posición justo después del inicio del marcador con el nombre especificado.

La comparación no distingue entre mayúsculas y minúsculas. Si no se encuentra el marcador,  false  se devuelve y el cursor no se mueve.

Insertar texto nuevo no reemplaza el texto existente del marcador.

Tenga en cuenta que algunos marcadores en el documento están asignados a campos de formulario. Moverse a dicho marcador e insertar texto allí inserta el texto en el código del campo de formulario. Aunque esto no invalidará el campo de formulario, el texto insertado no será visible porque pasa a formar parte del código del campo.

 **Examples:** 

Muestra cómo mover el cursor de un document builder a diferentes nodos en un documento.

```

 Document doc = new Document();
 DocumentBuilder builder = new DocumentBuilder(doc);

 // Create a valid bookmark, an entity that consists of nodes enclosed by a bookmark start node,
 // and a bookmark end node.
 builder.startBookmark("MyBookmark");
 builder.write("Bookmark contents.");
 builder.endBookmark("MyBookmark");

 NodeCollection firstParagraphNodes = doc.getFirstSection().getBody().getFirstParagraph().getChildNodes(NodeType.ANY, false);

 Assert.assertEquals(NodeType.BOOKMARK_START, firstParagraphNodes.get(0).getNodeType());
 Assert.assertEquals(NodeType.RUN, firstParagraphNodes.get(1).getNodeType());
 Assert.assertEquals("Bookmark contents.", firstParagraphNodes.get(1).getText().trim());
 Assert.assertEquals(NodeType.BOOKMARK_END, firstParagraphNodes.get(2).getNodeType());

 // The document builder's cursor is always ahead of the node that we last added with it.
 // If the builder's cursor is at the end of the document, its current node will be null.
 // The previous node is the bookmark end node that we last added.
 // Adding new nodes with the builder will append them to the last node.
 Assert.assertNull(builder.getCurrentNode());

 // If we wish to edit a different part of the document with the builder,
 // we will need to bring its cursor to the node we wish to edit.
 builder.moveToBookmark("MyBookmark");

 // Moving it to a bookmark will move it to the first node within the bookmark start and end nodes, the enclosed run.
 Assert.assertEquals(firstParagraphNodes.get(1), builder.getCurrentNode());

 // We can also move the cursor to an individual node like this.
 builder.moveTo(doc.getFirstSection().getBody().getFirstParagraph().getChildNodes(NodeType.ANY, false).get(0));

 Assert.assertEquals(NodeType.BOOKMARK_START, builder.getCurrentNode().getNodeType());
 Assert.assertEquals(doc.getFirstSection().getBody().getFirstParagraph(), builder.getCurrentParagraph());
 Assert.assertTrue(builder.isAtStartOfParagraph());

 // We can use specific methods to move to the start/end of a document.
 builder.moveToDocumentEnd();

 Assert.assertTrue(builder.isAtEndOfParagraph());

 builder.moveToDocumentStart();

 Assert.assertTrue(builder.isAtStartOfParagraph());
 
```

**Parameters:**
| Parámetro | Tipo | Descripción |
| --- | --- | --- |
| bookmarkName | java.lang.String | El nombre del marcador al que mover el cursor. |

**Returns:**
boolean -  true  si se encontró el marcador;  false  de lo contrario.
### moveToBookmark(String bookmarkName, boolean isStart, boolean isAfter) {#moveToBookmark-java.lang.String-boolean-boolean}
```
public boolean moveToBookmark(String bookmarkName, boolean isStart, boolean isAfter)
```


Mueve el cursor a un marcador con mayor precisión.

 **Remarks:** 

Mueve el cursor a una posición antes o después del inicio o fin del marcador.

Si la posición deseada no está a nivel en línea, se mueve al siguiente párrafo.

La comparación no distingue entre mayúsculas y minúsculas. Si no se encuentra el marcador,  false  se devuelve y el cursor no se mueve.

 **Examples:** 

Muestra cómo mover el cursor del punto de inserción de nodos de un document builder a un marcador.

```

 Document doc = new Document();
 DocumentBuilder builder = new DocumentBuilder(doc);

 // A valid bookmark consists of a BookmarkStart node, a BookmarkEnd node with a
 // matching bookmark name somewhere afterward, and contents enclosed by those nodes.
 builder.startBookmark("MyBookmark");
 builder.write("Hello world! ");
 builder.endBookmark("MyBookmark");

 // There are 4 ways of moving a document builder's cursor to a bookmark.
 // If we are between the BookmarkStart and BookmarkEnd nodes, the cursor will be inside the bookmark.
 // This means that any text added by the builder will become a part of the bookmark.
 // 1 -  Outside of the bookmark, in front of the BookmarkStart node:
 Assert.assertTrue(builder.moveToBookmark("MyBookmark", true, false));
 builder.write("1. ");

 Assert.assertEquals("Hello world! ", doc.getRange().getBookmarks().get("MyBookmark").getText());
 Assert.assertEquals("1. Hello world!", doc.getText().trim());

 // 2 -  Inside the bookmark, right after the BookmarkStart node:
 Assert.assertTrue(builder.moveToBookmark("MyBookmark", true, true));
 builder.write("2. ");

 Assert.assertEquals("2. Hello world! ", doc.getRange().getBookmarks().get("MyBookmark").getText());
 Assert.assertEquals("1. 2. Hello world!", doc.getText().trim());

 // 2 -  Inside the bookmark, right in front of the BookmarkEnd node:
 Assert.assertTrue(builder.moveToBookmark("MyBookmark", false, false));
 builder.write("3. ");

 Assert.assertEquals("2. Hello world! 3. ", doc.getRange().getBookmarks().get("MyBookmark").getText());
 Assert.assertEquals("1. 2. Hello world! 3.", doc.getText().trim());

 // 4 -  Outside of the bookmark, after the BookmarkEnd node:
 Assert.assertTrue(builder.moveToBookmark("MyBookmark", false, true));
 builder.write("4.");

 Assert.assertEquals("2. Hello world! 3. ", doc.getRange().getBookmarks().get("MyBookmark").getText());
 Assert.assertEquals("1. 2. Hello world! 3. 4.", doc.getText().trim());
 
```

**Parameters:**
| Parámetro | Tipo | Descripción |
| --- | --- | --- |
| bookmarkName | java.lang.String | El nombre del marcador al que mover el cursor. |
| isStart | boolean | Cuando  true , mueve el cursor al comienzo del marcador. Cuando  false , mueve el cursor al final del marcador. |
| isAfter | boolean | Cuando  true , mueve el cursor para que esté después de la posición de inicio o fin del marcador. Cuando  false , mueve el cursor para que esté antes de la posición de inicio o fin del marcador. |

**Returns:**
boolean -  true  si se encontró el marcador;  false  de lo contrario.
### moveToCell(int tableIndex, int rowIndex, int columnIndex, int characterIndex) {#moveToCell-int-int-int-int}
```
public void moveToCell(int tableIndex, int rowIndex, int columnIndex, int characterIndex)
```


Mueve el cursor a una celda de tabla en la sección actual.

 **Remarks:** 

La navegación se realiza dentro de la historia actual de la sección actual.

Para los parámetros de índice, cuando el índice es mayor o igual a 0, especifica un índice desde el principio, siendo 0 el primer elemento. Cuando el índice es menor que 0, especifica un índice desde el final, siendo -1 el último elemento.

 **Examples:** 

Muestra cómo mover el cursor de un document builder a una celda en una tabla.

```

 Document doc = new Document();
 DocumentBuilder builder = new DocumentBuilder(doc);

 // Create an empty 2x2 table.
 builder.startTable();
 builder.insertCell();
 builder.insertCell();
 builder.endRow();
 builder.insertCell();
 builder.insertCell();
 builder.endTable();

 // Because we have ended the table with the EndTable method,
 // the document builder's cursor is currently outside the table.
 // This cursor has the same function as Microsoft Word's blinking text cursor.
 // It can also be moved to a different location in the document using the builder's MoveTo methods.
 // We can move the cursor back inside the table to a specific cell.
 builder.moveToCell(0, 1, 1, 0);
 builder.write("Column 2, cell 2.");

 doc.save(getArtifactsDir() + "DocumentBuilder.MoveToCell.docx");
 
```

**Parameters:**
| Parámetro | Tipo | Descripción |
| --- | --- | --- |
| tableIndex | int | El índice de la tabla a la que moverse. |
| rowIndex | int | El índice de la fila en la tabla. |
| columnIndex | int | El índice de la columna en la tabla. |
| characterIndex | int | El índice del carácter dentro de la celda. Un valor negativo le permite especificar una posición desde el final de la celda. Use -1 para moverse al final de la celda. |

### moveToDocumentEnd() {#moveToDocumentEnd}
```
public void moveToDocumentEnd()
```


Mueve el cursor al final del documento.

 **Examples:** 

Muestra cómo mover el cursor de un document builder a diferentes nodos en un documento.

```

 Document doc = new Document();
 DocumentBuilder builder = new DocumentBuilder(doc);

 // Create a valid bookmark, an entity that consists of nodes enclosed by a bookmark start node,
 // and a bookmark end node.
 builder.startBookmark("MyBookmark");
 builder.write("Bookmark contents.");
 builder.endBookmark("MyBookmark");

 NodeCollection firstParagraphNodes = doc.getFirstSection().getBody().getFirstParagraph().getChildNodes(NodeType.ANY, false);

 Assert.assertEquals(NodeType.BOOKMARK_START, firstParagraphNodes.get(0).getNodeType());
 Assert.assertEquals(NodeType.RUN, firstParagraphNodes.get(1).getNodeType());
 Assert.assertEquals("Bookmark contents.", firstParagraphNodes.get(1).getText().trim());
 Assert.assertEquals(NodeType.BOOKMARK_END, firstParagraphNodes.get(2).getNodeType());

 // The document builder's cursor is always ahead of the node that we last added with it.
 // If the builder's cursor is at the end of the document, its current node will be null.
 // The previous node is the bookmark end node that we last added.
 // Adding new nodes with the builder will append them to the last node.
 Assert.assertNull(builder.getCurrentNode());

 // If we wish to edit a different part of the document with the builder,
 // we will need to bring its cursor to the node we wish to edit.
 builder.moveToBookmark("MyBookmark");

 // Moving it to a bookmark will move it to the first node within the bookmark start and end nodes, the enclosed run.
 Assert.assertEquals(firstParagraphNodes.get(1), builder.getCurrentNode());

 // We can also move the cursor to an individual node like this.
 builder.moveTo(doc.getFirstSection().getBody().getFirstParagraph().getChildNodes(NodeType.ANY, false).get(0));

 Assert.assertEquals(NodeType.BOOKMARK_START, builder.getCurrentNode().getNodeType());
 Assert.assertEquals(doc.getFirstSection().getBody().getFirstParagraph(), builder.getCurrentParagraph());
 Assert.assertTrue(builder.isAtStartOfParagraph());

 // We can use specific methods to move to the start/end of a document.
 builder.moveToDocumentEnd();

 Assert.assertTrue(builder.isAtEndOfParagraph());

 builder.moveToDocumentStart();

 Assert.assertTrue(builder.isAtStartOfParagraph());
 
```

### moveToDocumentStart() {#moveToDocumentStart}
```
public void moveToDocumentStart()
```


Mueve el cursor al comienzo del documento.

 **Examples:** 

Muestra cómo mover el cursor de un document builder a diferentes nodos en un documento.

```

 Document doc = new Document();
 DocumentBuilder builder = new DocumentBuilder(doc);

 // Create a valid bookmark, an entity that consists of nodes enclosed by a bookmark start node,
 // and a bookmark end node.
 builder.startBookmark("MyBookmark");
 builder.write("Bookmark contents.");
 builder.endBookmark("MyBookmark");

 NodeCollection firstParagraphNodes = doc.getFirstSection().getBody().getFirstParagraph().getChildNodes(NodeType.ANY, false);

 Assert.assertEquals(NodeType.BOOKMARK_START, firstParagraphNodes.get(0).getNodeType());
 Assert.assertEquals(NodeType.RUN, firstParagraphNodes.get(1).getNodeType());
 Assert.assertEquals("Bookmark contents.", firstParagraphNodes.get(1).getText().trim());
 Assert.assertEquals(NodeType.BOOKMARK_END, firstParagraphNodes.get(2).getNodeType());

 // The document builder's cursor is always ahead of the node that we last added with it.
 // If the builder's cursor is at the end of the document, its current node will be null.
 // The previous node is the bookmark end node that we last added.
 // Adding new nodes with the builder will append them to the last node.
 Assert.assertNull(builder.getCurrentNode());

 // If we wish to edit a different part of the document with the builder,
 // we will need to bring its cursor to the node we wish to edit.
 builder.moveToBookmark("MyBookmark");

 // Moving it to a bookmark will move it to the first node within the bookmark start and end nodes, the enclosed run.
 Assert.assertEquals(firstParagraphNodes.get(1), builder.getCurrentNode());

 // We can also move the cursor to an individual node like this.
 builder.moveTo(doc.getFirstSection().getBody().getFirstParagraph().getChildNodes(NodeType.ANY, false).get(0));

 Assert.assertEquals(NodeType.BOOKMARK_START, builder.getCurrentNode().getNodeType());
 Assert.assertEquals(doc.getFirstSection().getBody().getFirstParagraph(), builder.getCurrentParagraph());
 Assert.assertTrue(builder.isAtStartOfParagraph());

 // We can use specific methods to move to the start/end of a document.
 builder.moveToDocumentEnd();

 Assert.assertTrue(builder.isAtEndOfParagraph());

 builder.moveToDocumentStart();

 Assert.assertTrue(builder.isAtStartOfParagraph());
 
```

### moveToField(Field field, boolean isAfter) {#moveToField-com.aspose.words.Field-boolean}
```
public void moveToField(Field field, boolean isAfter)
```


Mueve el cursor a un campo en el documento.

 **Examples:** 

Muestra cómo mover el cursor del punto de inserción de nodos del document builder a un campo específico.

```

 Document doc = new Document();
 DocumentBuilder builder = new DocumentBuilder(doc);

 // Insert a field using the DocumentBuilder and add a run of text after it.
 Field field = builder.insertField(" AUTHOR \"John Doe\" ");

 // The builder's cursor is currently at end of the document.
 Assert.assertNull(builder.getCurrentNode());

 // Move the cursor to the field while specifying whether to place that cursor before or after the field.
 builder.moveToField(field, moveCursorToAfterTheField);

 // Note that the cursor is outside of the field in both cases.
 // This means that we cannot edit the field using the builder like this.
 // To edit a field, we can use the builder's MoveTo method on a field's FieldStart
 // or FieldSeparator node to place the cursor inside.
 if (moveCursorToAfterTheField) {
     Assert.assertNull(builder.getCurrentNode());
     builder.write(" Text immediately after the field.");

     Assert.assertEquals("AUTHOR \"John Doe\" John Doe Text immediately after the field.",
             doc.getText().trim());
 } else {
     Assert.assertEquals(field.getStart(), builder.getCurrentNode());
     builder.write("Text immediately before the field. ");

     Assert.assertEquals("Text immediately before the field.  AUTHOR \"John Doe\" John Doe",
             doc.getText().trim());
 }
 
```

**Parameters:**
| Parámetro | Tipo | Descripción |
| --- | --- | --- |
| field | [Field](../../com.aspose.words/field/) | El campo al que mover el cursor. |
| isAfter | boolean | Cuando  true , mueve el cursor para que quede después del final del campo. Cuando  false , lo mueve para que quede antes del inicio del campo. |

### moveToHeaderFooter(int headerFooterType) {#moveToHeaderFooter-int}
```
public void moveToHeaderFooter(int headerFooterType)
```




**Parameters:**
| Parámetro | Tipo | Descripción |
| --- | --- | --- |
| headerFooterType | int |  |

### moveToMergeField(String fieldName) {#moveToMergeField-java.lang.String}
```
public boolean moveToMergeField(String fieldName)
```


Mueve el cursor al campo de combinación especificado.  Mueve el cursor a una posición justo más allá del campo de combinación especificado y elimina el campo de combinación.

 **Remarks:** 

Tenga en cuenta que este método elimina el campo de combinación del documento después de mover el cursor.

 **Examples:** 

Muestra cómo rellenar MERGEFIELDs con datos usando un document builder en lugar de una combinación de correspondencia.

```

 Document doc = new Document();
 DocumentBuilder builder = new DocumentBuilder(doc);

 // Insert some MERGEFIELDS, which accept data from columns of the same name in a data source during a mail merge,
 // and then fill them manually.
 builder.insertField(" MERGEFIELD Chairman ");
 builder.insertField(" MERGEFIELD ChiefFinancialOfficer ");
 builder.insertField(" MERGEFIELD ChiefTechnologyOfficer ");

 builder.moveToMergeField("Chairman");
 builder.setBold(true);
 builder.writeln("John Doe");

 builder.moveToMergeField("ChiefFinancialOfficer");
 builder.setItalic(true);
 builder.writeln("Jane Doe");

 builder.moveToMergeField("ChiefTechnologyOfficer");
 builder.setItalic(true);
 builder.writeln("John Bloggs");

 doc.save(getArtifactsDir() + "DocumentBuilder.FillMergeFields.docx");
 
```

Muestra cómo insertar campos de formulario de casilla de verificación en un documento durante la combinación de correspondencia.

```

 public void insertCheckBox() throws Exception {
     Document doc = new Document();
     DocumentBuilder builder = new DocumentBuilder(doc);

     builder.startTable();
     builder.insertCell();
     builder.insertField(" MERGEFIELD  TableStart:StudentCourse ");
     builder.insertCell();
     builder.insertField(" MERGEFIELD  CourseName ");
     builder.insertCell();
     builder.insertField(" MERGEFIELD  TableEnd:StudentCourse ");
     builder.endTable();

     // Add a handler for the MergeField event
     doc.getMailMerge().setFieldMergingCallback(new HandleMergeFieldInsertCheckBox());

     // Execute mail merge with regions
     DataTable dataTable = getStudentCourseDataTable();
     doc.getMailMerge().executeWithRegions(dataTable);

     // Save resulting document with a new name
     doc.save(getArtifactsDir() + "MailMergeEvent.InsertCheckBox.docx");
 }

 private class HandleMergeFieldInsertCheckBox implements IFieldMergingCallback {
     // This is called for each merge field in the document
     // when Document.MailMerge.ExecuteWithRegions is called.
     public void fieldMerging(final FieldMergingArgs args) throws Exception {
         if (args.getDocumentFieldName().equals("CourseName")) {
             // The name of the table that we are merging can be found here
             Assert.assertEquals(args.getTableName(), "StudentCourse");

             // Insert the checkbox for this merge field, using DocumentBuilder
             DocumentBuilder builder = new DocumentBuilder(args.getDocument());
             builder.moveToMergeField(args.getFieldName());
             builder.insertCheckBox(args.getDocumentFieldName() + mCheckBoxCount, false, 0);
             // Get the actual value of the field
             String fieldValue = args.getFieldValue().toString();

             // In this case, for every record index 'n', the corresponding field value is "Course n"
             Assert.assertEquals(args.getRecordIndex(), Character.getNumericValue(fieldValue.charAt(7)));

             builder.write(fieldValue);
             mCheckBoxCount++;
         }
     }

     public void imageFieldMerging(final ImageFieldMergingArgs args) {
         // Do nothing
     }

     // Counter for CheckBox name generation.
     private int mCheckBoxCount;
 }

 // Create DataTable and fill it with data.
 // In real life this DataTable should be filled from a database.
 private static DataTable getStudentCourseDataTable() throws Exception {
     DataTable dataTable = new DataTable("StudentCourse");
     dataTable.getColumns().add("CourseName");
     for (int i = 0; i < 10; i++) {
         DataRow datarow = dataTable.newRow();
         dataTable.getRows().add(datarow);
         datarow.set(0, "Course " + i);
     }
     return dataTable;
 }
 
```

**Parameters:**
| Parámetro | Tipo | Descripción |
| --- | --- | --- |
| fieldName | java.lang.String | El nombre sin distinción de mayúsculas y minúsculas del campo de combinación de correo. |

**Returns:**
boolean -  true  si se encontró el campo de combinación y se movió el cursor;  false  en caso contrario.
### moveToMergeField(String fieldName, boolean isAfter, boolean isDeleteField) {#moveToMergeField-java.lang.String-boolean-boolean}
```
public boolean moveToMergeField(String fieldName, boolean isAfter, boolean isDeleteField)
```


Mueve el campo de combinación al campo de combinación especificado.

 **Examples:** 

Muestra cómo insertar campos y mover el cursor del DocumentBuilder a ellos.

```

 Document doc = new Document();
 DocumentBuilder builder = new DocumentBuilder(doc);
 builder.insertField("MERGEFIELD MyMergeField1 \\* MERGEFORMAT");
 builder.insertField("MERGEFIELD MyMergeField2 \\* MERGEFORMAT");

 // Move the cursor to the first MERGEFIELD.
 builder.moveToMergeField("MyMergeField1", true, false);

 // Note that the cursor is placed immediately after the first MERGEFIELD, and before the second.
 Assert.assertEquals(doc.getRange().getFields().get(1).getStart(), builder.getCurrentNode());
 Assert.assertEquals(doc.getRange().getFields().get(0).getEnd(), builder.getCurrentNode().getPreviousSibling());

 // If we wish to edit the field's field code or contents using the builder,
 // its cursor would need to be inside a field.
 // To place it inside a field, we would need to call the document builder's MoveTo method
 // and pass the field's start or separator node as an argument.
 builder.write(" Text between our merge fields. ");

 doc.save(getArtifactsDir() + "DocumentBuilder.MergeFields.docx");
 
```

**Parameters:**
| Parámetro | Tipo | Descripción |
| --- | --- | --- |
| fieldName | java.lang.String | El nombre sin distinción de mayúsculas y minúsculas del campo de combinación de correo. |
| isAfter | boolean | Cuando  true , mueve el cursor para que quede después del final del campo. Cuando  false , lo mueve para que quede antes del inicio del campo. |
| isDeleteField | boolean | Cuando  true , elimina el campo de combinación. |

**Returns:**
boolean -  true  si se encontró el campo de combinación y se movió el cursor;  false  en caso contrario.
### moveToParagraph(int paragraphIndex, int characterIndex) {#moveToParagraph-int-int}
```
public void moveToParagraph(int paragraphIndex, int characterIndex)
```


Mueve el cursor a un párrafo en la sección actual.

 **Remarks:** 

La navegación se realiza dentro de la historia actual de la sección actual. Es decir, si movió el cursor al encabezado principal de la primera sección, entonces  paragraphIndex  especifica el índice del párrafo dentro de ese encabezado de esa sección.

Cuando  paragraphIndex  es mayor o igual a 0, especifica un índice desde el comienzo de la sección, siendo 0 el primer párrafo. Cuando  paragraphIndex  es menor que 0, especifica un índice desde el final de la sección, siendo -1 el último párrafo.

 **Examples:** 

Muestra cómo mover la posición del cursor de un builder a un párrafo especificado.

```

 Document doc = new Document(getMyDir() + "Paragraphs.docx");
 ParagraphCollection paragraphs = doc.getFirstSection().getBody().getParagraphs();

 Assert.assertEquals(22, paragraphs.getCount());

 // Create document builder to edit the document. The builder's cursor,
 // which is the point where it will insert new nodes when we call its document construction methods,
 // is currently at the beginning of the document.
 DocumentBuilder builder = new DocumentBuilder(doc);

 Assert.assertEquals(0, paragraphs.indexOf(builder.getCurrentParagraph()));

 // Move that cursor to a different paragraph will place that cursor in front of that paragraph.
 builder.moveToParagraph(2, 0);
 // Any new content that we add will be inserted at that point.
 builder.writeln("This is a new third paragraph. ");
 
```

**Parameters:**
| Parámetro | Tipo | Descripción |
| --- | --- | --- |
| paragraphIndex | int | El índice del párrafo al que mover. |
| characterIndex | int | El índice del carácter dentro del párrafo. Un valor negativo le permite especificar una posición desde el final del párrafo. Use -1 para moverse al final del párrafo. |

### moveToSection(int sectionIndex) {#moveToSection-int}
```
public void moveToSection(int sectionIndex)
```


Mueve el cursor al comienzo del cuerpo en una sección especificada.

 **Remarks:** 

Cuando  sectionIndex  es mayor o igual a 0, especifica un índice desde el comienzo del documento, siendo 0 la primera sección. Cuando  sectionIndex  es menor que 0, especifica un índice desde el final del documento, siendo -1 la última sección.

El cursor se mueve al primer párrafo en el [Body](../../com.aspose.words/body/) de la sección especificada.

 **Examples:** 

Muestra cómo crear encabezados y pies de página en un documento usando DocumentBuilder.

```

 Document doc = new Document();
 DocumentBuilder builder = new DocumentBuilder(doc);

 // Specify that we want different headers and footers for first, even and odd pages.
 builder.getPageSetup().setDifferentFirstPageHeaderFooter(true);
 builder.getPageSetup().setOddAndEvenPagesHeaderFooter(true);

 // Create the headers, then add three pages to the document to display each header type.
 builder.moveToHeaderFooter(HeaderFooterType.HEADER_FIRST);
 builder.write("Header for the first page");
 builder.moveToHeaderFooter(HeaderFooterType.HEADER_EVEN);
 builder.write("Header for even pages");
 builder.moveToHeaderFooter(HeaderFooterType.HEADER_PRIMARY);
 builder.write("Header for all other pages");

 builder.moveToSection(0);
 builder.writeln("Page1");
 builder.insertBreak(BreakType.PAGE_BREAK);
 builder.writeln("Page2");
 builder.insertBreak(BreakType.PAGE_BREAK);
 builder.writeln("Page3");

 doc.save(getArtifactsDir() + "DocumentBuilder.HeadersAndFooters.docx");
 
```

**Parameters:**
| Parámetro | Tipo | Descripción |
| --- | --- | --- |
| sectionIndex | int | El índice de la sección a la que mover. |

### moveToStructuredDocumentTag(StructuredDocumentTag structuredDocumentTag, int characterIndex) {#moveToStructuredDocumentTag-com.aspose.words.StructuredDocumentTag-int}
```
public void moveToStructuredDocumentTag(StructuredDocumentTag structuredDocumentTag, int characterIndex)
```


Mueve el cursor a la etiqueta de documento estructurado.

 **Examples:** 

Muestra cómo mover el cursor de DocumentBuilder dentro de una etiqueta de documento estructurado.

```

 Document doc = new Document(getMyDir() + "Structured document tags.docx");
 DocumentBuilder builder = new DocumentBuilder(doc);

 // There is a several ways to move the cursor:
 // 1 -  Move to the first character of structured document tag by index.
 builder.moveToStructuredDocumentTag(1, 1);

 // 2 -  Move to the first character of structured document tag by object.
 StructuredDocumentTag tag = (StructuredDocumentTag)doc.getChild(NodeType.STRUCTURED_DOCUMENT_TAG, 2, true);
 builder.moveToStructuredDocumentTag(tag, 1);
 builder.write(" New text.");

 Assert.assertEquals("R New text.ichText", tag.getText().trim());

 // 3 -  Move to the end of the second structured document tag.
 builder.moveToStructuredDocumentTag(1, -1);
 Assert.assertTrue(builder.isAtEndOfStructuredDocumentTag());

 // Get currently selected structured document tag.
 builder.getCurrentStructuredDocumentTag().setColor(Color.GREEN);

 doc.save(getArtifactsDir() + "Document.MoveToStructuredDocumentTag.docx");
 
```

**Parameters:**
| Parámetro | Tipo | Descripción |
| --- | --- | --- |
| structuredDocumentTag | [StructuredDocumentTag](../../com.aspose.words/structureddocumenttag/) | La etiqueta de documento estructurado a la que mover. |
| characterIndex | int | El índice del carácter dentro de la etiqueta de documento estructurado. Un valor negativo le permite especificar una posición desde el final de la etiqueta de documento estructurado. Use -1 para moverse al final de la etiqueta de documento estructurado. Si la etiqueta de documento estructurado está a nivel de bloque y desea mover el cursor al final de su último párrafo, especifique -2. |

### moveToStructuredDocumentTag(int structuredDocumentTagIndex, int characterIndex) {#moveToStructuredDocumentTag-int-int}
```
public void moveToStructuredDocumentTag(int structuredDocumentTagIndex, int characterIndex)
```


Mueve el cursor a una etiqueta de documento estructurado en la sección actual.

 **Remarks:** 

La navegación se realiza dentro de la historia actual de la sección actual. Es decir, si movió el cursor al encabezado principal de la primera sección, entonces  structuredDocumentTagIndex  especifica el índice de la etiqueta de documento estructurado dentro de ese encabezado de esa sección.

Cuando  structuredDocumentTagIndex  es mayor o igual a 0, especifica un índice desde el comienzo de la sección, siendo 0 la primera etiqueta de documento estructurado. Cuando  structuredDocumentTagIndex  es menor que 0, especifica un índice desde el final de la sección, siendo -1 la última etiqueta de documento estructurado.

 **Examples:** 

Muestra cómo mover el cursor de DocumentBuilder dentro de una etiqueta de documento estructurado.

```

 Document doc = new Document(getMyDir() + "Structured document tags.docx");
 DocumentBuilder builder = new DocumentBuilder(doc);

 // There is a several ways to move the cursor:
 // 1 -  Move to the first character of structured document tag by index.
 builder.moveToStructuredDocumentTag(1, 1);

 // 2 -  Move to the first character of structured document tag by object.
 StructuredDocumentTag tag = (StructuredDocumentTag)doc.getChild(NodeType.STRUCTURED_DOCUMENT_TAG, 2, true);
 builder.moveToStructuredDocumentTag(tag, 1);
 builder.write(" New text.");

 Assert.assertEquals("R New text.ichText", tag.getText().trim());

 // 3 -  Move to the end of the second structured document tag.
 builder.moveToStructuredDocumentTag(1, -1);
 Assert.assertTrue(builder.isAtEndOfStructuredDocumentTag());

 // Get currently selected structured document tag.
 builder.getCurrentStructuredDocumentTag().setColor(Color.GREEN);

 doc.save(getArtifactsDir() + "Document.MoveToStructuredDocumentTag.docx");
 
```

**Parameters:**
| Parámetro | Tipo | Descripción |
| --- | --- | --- |
| structuredDocumentTagIndex | int | El índice de la etiqueta de documento estructurado a la que mover. |
| characterIndex | int | El índice del carácter dentro de la etiqueta de documento estructurado. Un valor negativo le permite especificar una posición desde el final de la etiqueta de documento estructurado. Use -1 para moverse al final de la etiqueta de documento estructurado. Si la etiqueta de documento estructurado está a nivel de bloque y desea mover el cursor al final de su último párrafo, especifique -2. |

### popFont() {#popFont}
```
public void popFont()
```


Recupera el formato de carácter previamente guardado en la pila.

 **Examples:** 

Muestra cómo usar la pila de formato de un document builder.

```

 Document doc = new Document();
 DocumentBuilder builder = new DocumentBuilder(doc);

 // Set up font formatting, then write the text that goes before the hyperlink.
 builder.getFont().setName("Arial");
 builder.getFont().setSize(24.0);
 builder.write("To visit Google, hold Ctrl and click ");

 // Preserve our current formatting configuration on the stack.
 builder.pushFont();

 // Alter the builder's current formatting by applying a new style.
 builder.getFont().setStyleIdentifier(StyleIdentifier.HYPERLINK);
 builder.insertHyperlink("here", "http://www.google.com", false);

 Assert.assertEquals(Color.BLUE.getRGB(), builder.getFont().getColor().getRGB());
 Assert.assertEquals(Underline.SINGLE, builder.getFont().getUnderline());

 // Restore the font formatting that we saved earlier and remove the element from the stack.
 builder.popFont();

 Assert.assertEquals(0, builder.getFont().getColor().getRGB());
 Assert.assertEquals(Underline.NONE, builder.getFont().getUnderline());

 builder.write(". We hope you enjoyed the example.");

 doc.save(getArtifactsDir() + "DocumentBuilder.PushPopFont.docx");
 
```

### pushFont() {#pushFont}
```
public void pushFont()
```


Guarda el formato de carácter actual en la pila.

 **Examples:** 

Muestra cómo usar la pila de formato de un document builder.

```

 Document doc = new Document();
 DocumentBuilder builder = new DocumentBuilder(doc);

 // Set up font formatting, then write the text that goes before the hyperlink.
 builder.getFont().setName("Arial");
 builder.getFont().setSize(24.0);
 builder.write("To visit Google, hold Ctrl and click ");

 // Preserve our current formatting configuration on the stack.
 builder.pushFont();

 // Alter the builder's current formatting by applying a new style.
 builder.getFont().setStyleIdentifier(StyleIdentifier.HYPERLINK);
 builder.insertHyperlink("here", "http://www.google.com", false);

 Assert.assertEquals(Color.BLUE.getRGB(), builder.getFont().getColor().getRGB());
 Assert.assertEquals(Underline.SINGLE, builder.getFont().getUnderline());

 // Restore the font formatting that we saved earlier and remove the element from the stack.
 builder.popFont();

 Assert.assertEquals(0, builder.getFont().getColor().getRGB());
 Assert.assertEquals(Underline.NONE, builder.getFont().getUnderline());

 builder.write(". We hope you enjoyed the example.");

 doc.save(getArtifactsDir() + "DocumentBuilder.PushPopFont.docx");
 
```

### removeParaAttr(int key) {#removeParaAttr-int}
```
public void removeParaAttr(int key)
```




**Parameters:**
| Parámetro | Tipo | Descripción |
| --- | --- | --- |
| key | int |  |

### removeRunAttr(int key) {#removeRunAttr-int}
```
public void removeRunAttr(int key)
```




**Parameters:**
| Parámetro | Tipo | Descripción |
| --- | --- | --- |
| key | int |  |

### resetToDefaultAttrs() {#resetToDefaultAttrs}
```
public void resetToDefaultAttrs()
```




### setBold(boolean value) {#setBold-boolean}
```
public void setBold(boolean value)
```


True si la fuente está formateada en negrita.

 **Examples:** 

Muestra cómo rellenar MERGEFIELDs con datos usando un document builder en lugar de una combinación de correspondencia.

```

 Document doc = new Document();
 DocumentBuilder builder = new DocumentBuilder(doc);

 // Insert some MERGEFIELDS, which accept data from columns of the same name in a data source during a mail merge,
 // and then fill them manually.
 builder.insertField(" MERGEFIELD Chairman ");
 builder.insertField(" MERGEFIELD ChiefFinancialOfficer ");
 builder.insertField(" MERGEFIELD ChiefTechnologyOfficer ");

 builder.moveToMergeField("Chairman");
 builder.setBold(true);
 builder.writeln("John Doe");

 builder.moveToMergeField("ChiefFinancialOfficer");
 builder.setItalic(true);
 builder.writeln("Jane Doe");

 builder.moveToMergeField("ChiefTechnologyOfficer");
 builder.setItalic(true);
 builder.writeln("John Bloggs");

 doc.save(getArtifactsDir() + "DocumentBuilder.FillMergeFields.docx");
 
```

**Parameters:**
| Parámetro | Tipo | Descripción |
| --- | --- | --- |
| valor | boolean | El valor  boolean  correspondiente. |

### setCellAttr(int key, Object value) {#setCellAttr-int-java.lang.Object}
```
public void setCellAttr(int key, Object value)
```




**Parameters:**
| Parámetro | Tipo | Descripción |
| --- | --- | --- |
| key | int |  |
| valor | java.lang.Object |  |

### setDocument(Document value) {#setDocument-com.aspose.words.Document}
```
public void setDocument(Document value)
```


Establece el objeto [getDocument()](../../com.aspose.words/documentbuilder/\#getDocument) / [setDocument(com.aspose.words.Document)](../../com.aspose.words/documentbuilder/\#setDocument-com.aspose.words.Document) al que este objeto está adjunto.

 **Examples:** 

Muestra cómo aplicar y revertir la configuración de página a secciones en un documento.

```

 Document doc = new Document();
 DocumentBuilder builder = new DocumentBuilder(doc);

 // Modify the page setup properties for the builder's current section and add text.
 builder.getPageSetup().setOrientation(Orientation.LANDSCAPE);
 builder.getPageSetup().setVerticalAlignment(PageVerticalAlignment.CENTER);
 builder.writeln("This is the first section, which landscape oriented with vertically centered text.");

 // If we start a new section using a document builder,
 // it will inherit the builder's current page setup properties.
 builder.insertBreak(BreakType.SECTION_BREAK_NEW_PAGE);

 Assert.assertEquals(Orientation.LANDSCAPE, doc.getSections().get(1).getPageSetup().getOrientation());
 Assert.assertEquals(PageVerticalAlignment.CENTER, doc.getSections().get(1).getPageSetup().getVerticalAlignment());

 // We can revert its page setup properties to their default values using the "ClearFormatting" method.
 builder.getPageSetup().clearFormatting();

 Assert.assertEquals(Orientation.PORTRAIT, doc.getSections().get(1).getPageSetup().getOrientation());
 Assert.assertEquals(PageVerticalAlignment.TOP, doc.getSections().get(1).getPageSetup().getVerticalAlignment());

 builder.writeln("This is the second section, which is in default Letter paper size, portrait orientation and top alignment.");

 doc.save(getArtifactsDir() + "PageSetup.ClearFormatting.docx");
 
```

**Parameters:**
| Parámetro | Tipo | Descripción |
| --- | --- | --- |
| value | [Document](../../com.aspose.words/document/) | El objeto [getDocument()](../../com.aspose.words/documentbuilder/\#getDocument) / [setDocument(com.aspose.words.Document)](../../com.aspose.words/documentbuilder/\#setDocument-com.aspose.words.Document) al que está adjunto este objeto. |

### setItalic(boolean value) {#setItalic-boolean}
```
public void setItalic(boolean value)
```


Verdadero si la fuente está formateada en cursiva.

 **Examples:** 

Muestra cómo rellenar MERGEFIELDs con datos usando un document builder en lugar de una combinación de correspondencia.

```

 Document doc = new Document();
 DocumentBuilder builder = new DocumentBuilder(doc);

 // Insert some MERGEFIELDS, which accept data from columns of the same name in a data source during a mail merge,
 // and then fill them manually.
 builder.insertField(" MERGEFIELD Chairman ");
 builder.insertField(" MERGEFIELD ChiefFinancialOfficer ");
 builder.insertField(" MERGEFIELD ChiefTechnologyOfficer ");

 builder.moveToMergeField("Chairman");
 builder.setBold(true);
 builder.writeln("John Doe");

 builder.moveToMergeField("ChiefFinancialOfficer");
 builder.setItalic(true);
 builder.writeln("Jane Doe");

 builder.moveToMergeField("ChiefTechnologyOfficer");
 builder.setItalic(true);
 builder.writeln("John Bloggs");

 doc.save(getArtifactsDir() + "DocumentBuilder.FillMergeFields.docx");
 
```

**Parameters:**
| Parámetro | Tipo | Descripción |
| --- | --- | --- |
| valor | boolean | El valor  boolean  correspondiente. |

### setParaAttr(int key, Object value) {#setParaAttr-int-java.lang.Object}
```
public void setParaAttr(int key, Object value)
```




**Parameters:**
| Parámetro | Tipo | Descripción |
| --- | --- | --- |
| key | int |  |
| valor | java.lang.Object |  |

### setRowAttr(int key, Object value) {#setRowAttr-int-java.lang.Object}
```
public void setRowAttr(int key, Object value)
```




**Parameters:**
| Parámetro | Tipo | Descripción |
| --- | --- | --- |
| key | int |  |
| valor | java.lang.Object |  |

### setRunAttr(int fontAttr, Object value) {#setRunAttr-int-java.lang.Object}
```
public void setRunAttr(int fontAttr, Object value)
```




**Parameters:**
| Parámetro | Tipo | Descripción |
| --- | --- | --- |
| fontAttr | int |  |
| valor | java.lang.Object |  |

### setUnderline(int value) {#setUnderline-int}
```
public void setUnderline(int value)
```


Obtiene/establece el tipo de subrayado para la fuente actual.

 **Examples:** 

Muestra cómo dar formato al texto insertado por un document builder.

```

 Document doc = new Document();
 DocumentBuilder builder = new DocumentBuilder(doc);

 builder.setUnderline(Underline.DASH);
 builder.getFont().setColor(Color.BLUE);
 builder.getFont().setSize(32.0);

 // The builder applies formatting to its current paragraph and any new text added by it afterward.
 builder.writeln("Large, blue, and underlined text.");

 doc.save(getArtifactsDir() + "DocumentBuilder.InsertUnderline.docx");
 
```

**Parameters:**
| Parámetro | Tipo | Descripción |
| --- | --- | --- |
| value | int | El valor entero correspondiente. El valor debe ser una de las constantes de [Underline](../../com.aspose.words/underline/) . |

### startBookmark(String bookmarkName) {#startBookmark-java.lang.String}
```
public BookmarkStart startBookmark(String bookmarkName)
```


Marca la posición actual en el documento como inicio de marcador.

 **Remarks:** 

Los marcadores en un documento pueden superponerse y abarcar cualquier rango. Para crear un marcador válido, debes llamar tanto a [startBookmark(java.lang.String)](../../com.aspose.words/documentbuilder/\#startBookmark-java.lang.String) como a [endBookmark(java.lang.String)](../../com.aspose.words/documentbuilder/\#endBookmark-java.lang.String) con el mismo  bookmarkName  parámetro.

Los marcadores mal formados o los marcadores con nombres duplicados serán ignorados al guardar el documento.

 **Examples:** 

Muestra cómo crear un marcador.

```

 Document doc = new Document();
 DocumentBuilder builder = new DocumentBuilder(doc);

 // A valid bookmark needs to have document body text enclosed by
 // BookmarkStart and BookmarkEnd nodes created with a matching bookmark name.
 builder.startBookmark("MyBookmark");
 builder.writeln("Hello world!");
 builder.endBookmark("MyBookmark");

 Assert.assertEquals(1, doc.getRange().getBookmarks().getCount());
 Assert.assertEquals("MyBookmark", doc.getRange().getBookmarks().get(0).getName());
 Assert.assertEquals("Hello world!", doc.getRange().getBookmarks().get(0).getText().trim());
 
```

Muestra cómo insertar un hipervínculo que hace referencia a un marcador local.

```

 Document doc = new Document();
 DocumentBuilder builder = new DocumentBuilder(doc);

 builder.startBookmark("Bookmark1");
 builder.write("Bookmarked text. ");
 builder.endBookmark("Bookmark1");
 builder.writeln("Text outside of the bookmark.");

 // Insert a HYPERLINK field that links to the bookmark. We can pass field switches
 // to the "InsertHyperlink" method as part of the argument containing the referenced bookmark's name.
 builder.getFont().setColor(Color.BLUE);
 builder.getFont().setUnderline(Underline.SINGLE);
 FieldHyperlink hyperlink = (FieldHyperlink)builder.insertHyperlink("Link to Bookmark1", "Bookmark1", true);
 hyperlink.setScreenTip("Hyperlink Tip");

 doc.save(getArtifactsDir() + "DocumentBuilder.InsertHyperlinkToLocalBookmark.docx");
 
```

**Parameters:**
| Parámetro | Tipo | Descripción |
| --- | --- | --- |
| bookmarkName | java.lang.String | Nombre del marcador. |

**Returns:**
[BookmarkStart](../../com.aspose.words/bookmarkstart/) - The bookmark start node that was just created.
### startColumnBookmark(String bookmarkName) {#startColumnBookmark-java.lang.String}
```
public BookmarkStart startColumnBookmark(String bookmarkName)
```


Marca la posición actual en el documento como el inicio de un marcador de columna. La posición debe estar en una celda de tabla.

 **Remarks:** 

Un marcador de columna cubre una o más columnas en un rango de filas. Para crear un marcador válido, debes llamar tanto a [startColumnBookmark(java.lang.String)](../../com.aspose.words/documentbuilder/\#startColumnBookmark-java.lang.String) como a [endColumnBookmark(java.lang.String)](../../com.aspose.words/documentbuilder/\#endColumnBookmark-java.lang.String) con el mismo  bookmarkName  parámetro.

Los marcadores mal formados o los marcadores con nombres duplicados serán ignorados al guardar el documento.

La posición real del nodo [BookmarkStart](../../com.aspose.words/bookmarkstart/) insertado puede diferir de la posición actual del document builder.

 **Examples:** 

Muestra cómo crear un marcador de columna.

```

 Document doc = new Document();
 DocumentBuilder builder = new DocumentBuilder(doc);

 builder.startTable();

 builder.insertCell();
 // Cells 1,2,4,5 will be bookmarked.
 builder.startColumnBookmark("MyBookmark_1");
 // Badly formed bookmarks or bookmarks with duplicate names will be ignored when the document is saved.
 builder.startColumnBookmark("MyBookmark_1");
 builder.startColumnBookmark("BadStartBookmark");
 builder.write("Cell 1");

 builder.insertCell();
 builder.write("Cell 2");

 builder.insertCell();
 builder.write("Cell 3");

 builder.endRow();

 builder.insertCell();
 builder.write("Cell 4");

 builder.insertCell();
 builder.write("Cell 5");
 builder.endColumnBookmark("MyBookmark_1");
 builder.endColumnBookmark("MyBookmark_1");

 builder.insertCell();
 builder.write("Cell 6");

 builder.endRow();
 builder.endTable();

 doc.save(getArtifactsDir() + "Bookmarks.CreateColumnBookmark.docx");
 
```

**Parameters:**
| Parámetro | Tipo | Descripción |
| --- | --- | --- |
| bookmarkName | java.lang.String | Nombre del marcador. |

**Returns:**
[BookmarkStart](../../com.aspose.words/bookmarkstart/) - The bookmark start node that was just created.
### startEditableRange() {#startEditableRange}
```
public EditableRangeStart startEditableRange()
```


Marca la posición actual en el documento como inicio de un rango editable.

 **Remarks:** 

El rango editable en un documento puede superponerse y abarcar cualquier rango. Para crear un rango editable válido, debe llamar a los métodos [startEditableRange()](../../com.aspose.words/documentbuilder/\#startEditableRange) y [endEditableRange()](../../com.aspose.words/documentbuilder/\#endEditableRange) o [endEditableRange(com.aspose.words.EditableRangeStart)](../../com.aspose.words/documentbuilder/\#endEditableRange-com.aspose.words.EditableRangeStart).

Un rango editable mal formado será ignorado cuando se guarde el documento.

 **Examples:** 

Muestra cómo trabajar con un rango editable.

```

 Document doc = new Document();
 doc.protect(ProtectionType.READ_ONLY, "MyPassword");

 DocumentBuilder builder = new DocumentBuilder(doc);
 builder.writeln("Hello world! Since we have set the document's protection level to read-only," +
         " we cannot edit this paragraph without the password.");

 // Editable ranges allow us to leave parts of protected documents open for editing.
 EditableRangeStart editableRangeStart = builder.startEditableRange();
 builder.writeln("This paragraph is inside an editable range, and can be edited.");
 EditableRangeEnd editableRangeEnd = builder.endEditableRange();

 // A well-formed editable range has a start node, and end node.
 // These nodes have matching IDs and encompass editable nodes.
 EditableRange editableRange = editableRangeStart.getEditableRange();

 Assert.assertEquals(editableRangeStart.getId(), editableRange.getId());
 Assert.assertEquals(editableRangeEnd.getId(), editableRange.getId());

 // Different parts of the editable range link to each other.
 Assert.assertEquals(editableRangeStart.getId(), editableRange.getEditableRangeStart().getId());
 Assert.assertEquals(editableRangeStart.getId(), editableRangeEnd.getEditableRangeStart().getId());
 Assert.assertEquals(editableRange.getId(), editableRangeStart.getEditableRange().getId());
 Assert.assertEquals(editableRangeEnd.getId(), editableRange.getEditableRangeEnd().getId());

 // We can access the node types of each part like this. The editable range itself is not a node,
 // but an entity which consists of a start, an end, and their enclosed contents.
 Assert.assertEquals(NodeType.EDITABLE_RANGE_START, editableRangeStart.getNodeType());
 Assert.assertEquals(NodeType.EDITABLE_RANGE_END, editableRangeEnd.getNodeType());

 builder.writeln("This paragraph is outside the editable range, and cannot be edited.");

 doc.save(getArtifactsDir() + "EditableRange.CreateAndRemove.docx");

 // Remove an editable range. All the nodes that were inside the range will remain intact.
 editableRange.remove();
 
```

Muestra cómo crear rangos editables anidados.

```

 Document doc = new Document();
 doc.protect(ProtectionType.READ_ONLY, "MyPassword");

 DocumentBuilder builder = new DocumentBuilder(doc);
 builder.writeln("Hello world! Since we have set the document's protection level to read-only, " +
         "we cannot edit this paragraph without the password.");

 // Create two nested editable ranges.
 EditableRangeStart outerEditableRangeStart = builder.startEditableRange();
 builder.writeln("This paragraph inside the outer editable range and can be edited.");

 EditableRangeStart innerEditableRangeStart = builder.startEditableRange();
 builder.writeln("This paragraph inside both the outer and inner editable ranges and can be edited.");

 // Currently, the document builder's node insertion cursor is in more than one ongoing editable range.
 // When we want to end an editable range in this situation,
 // we need to specify which of the ranges we wish to end by passing its EditableRangeStart node.
 builder.endEditableRange(innerEditableRangeStart);

 builder.writeln("This paragraph inside the outer editable range and can be edited.");

 builder.endEditableRange(outerEditableRangeStart);

 builder.writeln("This paragraph is outside any editable ranges, and cannot be edited.");

 // If a region of text has two overlapping editable ranges with specified groups,
 // the combined group of users excluded by both groups are prevented from editing it.
 outerEditableRangeStart.getEditableRange().setEditorGroup(EditorType.EVERYONE);
 innerEditableRangeStart.getEditableRange().setEditorGroup(EditorType.CONTRIBUTORS);

 doc.save(getArtifactsDir() + "EditableRange.Nested.docx");
 
```

**Returns:**
[EditableRangeStart](../../com.aspose.words/editablerangestart/) - The editable range start node that was just created.
### startTable() {#startTable}
```
public Table startTable()
```


Inicia una tabla en el documento.

 **Remarks:** 

El siguiente método a llamar es [insertCell()](../../com.aspose.words/documentbuilder/\#insertCell).

Este método inicia una tabla anidada cuando se llama dentro de una celda.

 **Examples:** 

Muestra cómo crear una tabla con bordes personalizados.

```

 Document doc = new Document();
 DocumentBuilder builder = new DocumentBuilder(doc);

 builder.startTable();

 // Setting table formatting options for a document builder
 // will apply them to every row and cell that we add with it.
 builder.getParagraphFormat().setAlignment(ParagraphAlignment.CENTER);

 builder.getCellFormat().clearFormatting();
 builder.getCellFormat().setWidth(150.0);
 builder.getCellFormat().setVerticalAlignment(CellVerticalAlignment.CENTER);
 builder.getCellFormat().getShading().setBackgroundPatternColor(Color.GREEN);
 builder.getCellFormat().setWrapText(false);
 builder.getCellFormat().setFitText(true);

 builder.getRowFormat().clearFormatting();
 builder.getRowFormat().setHeightRule(HeightRule.EXACTLY);
 builder.getRowFormat().setHeight(50.0);
 builder.getRowFormat().getBorders().setLineStyle(LineStyle.ENGRAVE_3_D);
 builder.getRowFormat().getBorders().setColor(Color.ORANGE);

 builder.insertCell();
 builder.write("Row 1, Col 1");

 builder.insertCell();
 builder.write("Row 1, Col 2");
 builder.endRow();

 // Changing the formatting will apply it to the current cell,
 // and any new cells that we create with the builder afterward.
 // This will not affect the cells that we have added previously.
 builder.getCellFormat().getShading().clearFormatting();

 builder.insertCell();
 builder.write("Row 2, Col 1");

 builder.insertCell();
 builder.write("Row 2, Col 2");

 builder.endRow();

 // Increase row height to fit the vertical text.
 builder.insertCell();
 builder.getRowFormat().setHeight(150.0);
 builder.getCellFormat().setOrientation(TextOrientation.UPWARD);
 builder.write("Row 3, Col 1");

 builder.insertCell();
 builder.getCellFormat().setOrientation(TextOrientation.DOWNWARD);
 builder.write("Row 3, Col 2");

 builder.endRow();
 builder.endTable();

 doc.save(getArtifactsDir() + "DocumentBuilder.InsertTable.docx");
 
```

Muestra cómo crear una tabla formateada de 2x2.

```

 Document doc = new Document();
 DocumentBuilder builder = new DocumentBuilder(doc);

 Table table = builder.startTable();
 builder.insertCell();
 builder.getCellFormat().setVerticalAlignment(CellVerticalAlignment.CENTER);
 builder.write("Row 1, cell 1.");
 builder.insertCell();
 builder.write("Row 1, cell 2.");
 builder.endRow();

 // While building the table, the document builder will apply its current RowFormat/CellFormat property values
 // to the current row/cell that its cursor is in and any new rows/cells as it creates them.
 Assert.assertEquals(CellVerticalAlignment.CENTER, table.getRows().get(0).getCells().get(0).getCellFormat().getVerticalAlignment());
 Assert.assertEquals(CellVerticalAlignment.CENTER, table.getRows().get(0).getCells().get(1).getCellFormat().getVerticalAlignment());

 builder.insertCell();
 builder.getRowFormat().setHeight(100.0);
 builder.getRowFormat().setHeightRule(HeightRule.EXACTLY);
 builder.getCellFormat().setOrientation(TextOrientation.UPWARD);
 builder.write("Row 2, cell 1.");
 builder.insertCell();
 builder.getCellFormat().setOrientation(TextOrientation.DOWNWARD);
 builder.write("Row 2, cell 2.");
 builder.endRow();
 builder.endTable();

 // Previously added rows and cells are not retroactively affected by changes to the builder's formatting.
 Assert.assertEquals(0.0, table.getRows().get(0).getRowFormat().getHeight());
 Assert.assertEquals(HeightRule.AUTO, table.getRows().get(0).getRowFormat().getHeightRule());
 Assert.assertEquals(100.0, table.getRows().get(1).getRowFormat().getHeight());
 Assert.assertEquals(HeightRule.EXACTLY, table.getRows().get(1).getRowFormat().getHeightRule());
 Assert.assertEquals(TextOrientation.UPWARD, table.getRows().get(1).getCells().get(0).getCellFormat().getOrientation());
 Assert.assertEquals(TextOrientation.DOWNWARD, table.getRows().get(1).getCells().get(1).getCellFormat().getOrientation());

 doc.save(getArtifactsDir() + "DocumentBuilder.BuildTable.docx");
 
```

Muestra cómo dar formato a las celdas con un document builder.

```

 Document doc = new Document();
 DocumentBuilder builder = new DocumentBuilder(doc);

 Table table = builder.startTable();
 builder.insertCell();
 builder.write("Row 1, cell 1.");

 // Insert a second cell, and then configure cell text padding options.
 // The builder will apply these settings at its current cell, and any new cells creates afterwards.
 builder.insertCell();

 CellFormat cellFormat = builder.getCellFormat();
 cellFormat.setWidth(250.0);
 cellFormat.setLeftPadding(30.0);
 cellFormat.setRightPadding(30.0);
 cellFormat.setTopPadding(30.0);
 cellFormat.setBottomPadding(30.0);

 builder.write("Row 1, cell 2.");
 builder.endRow();
 builder.endTable();

 // The first cell was unaffected by the padding reconfiguration, and still holds the default values.
 Assert.assertEquals(0.0d, table.getFirstRow().getCells().get(0).getCellFormat().getWidth());
 Assert.assertEquals(5.4d, table.getFirstRow().getCells().get(0).getCellFormat().getLeftPadding());
 Assert.assertEquals(5.4d, table.getFirstRow().getCells().get(0).getCellFormat().getRightPadding());
 Assert.assertEquals(0.0d, table.getFirstRow().getCells().get(0).getCellFormat().getTopPadding());
 Assert.assertEquals(0.0d, table.getFirstRow().getCells().get(0).getCellFormat().getBottomPadding());

 Assert.assertEquals(250.0d, table.getFirstRow().getCells().get(1).getCellFormat().getWidth());
 Assert.assertEquals(30.0d, table.getFirstRow().getCells().get(1).getCellFormat().getLeftPadding());
 Assert.assertEquals(30.0d, table.getFirstRow().getCells().get(1).getCellFormat().getRightPadding());
 Assert.assertEquals(30.0d, table.getFirstRow().getCells().get(1).getCellFormat().getTopPadding());
 Assert.assertEquals(30.0d, table.getFirstRow().getCells().get(1).getCellFormat().getBottomPadding());

 // The first cell will still grow in the output document to match the size of its neighboring cell.
 doc.save(getArtifactsDir() + "DocumentBuilder.SetCellFormatting.docx");
 
```

**Returns:**
[Table](../../com.aspose.words/table/) - The table node that was just created.
### write(String text) {#write-java.lang.String}
```
public void write(String text)
```


Inserta una cadena en el documento en la posición de inserción actual.

 **Remarks:** 

Se utiliza el formato de fuente actual especificado por la propiedad [getFont()](../../com.aspose.words/documentbuilder/\#getFont).

 **Examples:** 

Muestra cómo insertar una cadena rodeada por un borde en un documento.

```

 Document doc = new Document();
 DocumentBuilder builder = new DocumentBuilder(doc);

 builder.getFont().getBorder().setColor(Color.GREEN);
 builder.getFont().getBorder().setLineWidth(2.5);
 builder.getFont().getBorder().setLineStyle(LineStyle.DASH_DOT_STROKER);

 builder.write("Text surrounded by green border.");

 doc.save(getArtifactsDir() + "Border.FontBorder.docx");
 
```

Muestra cómo crear una tabla con bordes personalizados.

```

 Document doc = new Document();
 DocumentBuilder builder = new DocumentBuilder(doc);

 builder.startTable();

 // Setting table formatting options for a document builder
 // will apply them to every row and cell that we add with it.
 builder.getParagraphFormat().setAlignment(ParagraphAlignment.CENTER);

 builder.getCellFormat().clearFormatting();
 builder.getCellFormat().setWidth(150.0);
 builder.getCellFormat().setVerticalAlignment(CellVerticalAlignment.CENTER);
 builder.getCellFormat().getShading().setBackgroundPatternColor(Color.GREEN);
 builder.getCellFormat().setWrapText(false);
 builder.getCellFormat().setFitText(true);

 builder.getRowFormat().clearFormatting();
 builder.getRowFormat().setHeightRule(HeightRule.EXACTLY);
 builder.getRowFormat().setHeight(50.0);
 builder.getRowFormat().getBorders().setLineStyle(LineStyle.ENGRAVE_3_D);
 builder.getRowFormat().getBorders().setColor(Color.ORANGE);

 builder.insertCell();
 builder.write("Row 1, Col 1");

 builder.insertCell();
 builder.write("Row 1, Col 2");
 builder.endRow();

 // Changing the formatting will apply it to the current cell,
 // and any new cells that we create with the builder afterward.
 // This will not affect the cells that we have added previously.
 builder.getCellFormat().getShading().clearFormatting();

 builder.insertCell();
 builder.write("Row 2, Col 1");

 builder.insertCell();
 builder.write("Row 2, Col 2");

 builder.endRow();

 // Increase row height to fit the vertical text.
 builder.insertCell();
 builder.getRowFormat().setHeight(150.0);
 builder.getCellFormat().setOrientation(TextOrientation.UPWARD);
 builder.write("Row 3, Col 1");

 builder.insertCell();
 builder.getCellFormat().setOrientation(TextOrientation.DOWNWARD);
 builder.write("Row 3, Col 2");

 builder.endRow();
 builder.endTable();

 doc.save(getArtifactsDir() + "DocumentBuilder.InsertTable.docx");
 
```

Muestra cómo usar un DocumentBuilder para crear una tabla.

```

 Document doc = new Document();
 DocumentBuilder builder = new DocumentBuilder(doc);

 // Start the table, then populate the first row with two cells.
 builder.startTable();
 builder.insertCell();
 builder.write("Row 1, Cell 1.");
 builder.insertCell();
 builder.write("Row 1, Cell 2.");

 // Call the builder's "EndRow" method to start a new row.
 builder.endRow();
 builder.insertCell();
 builder.write("Row 2, Cell 1.");
 builder.insertCell();
 builder.write("Row 2, Cell 2.");
 builder.endTable();

 doc.save(getArtifactsDir() + "DocumentBuilder.CreateTable.docx");
 
```

Muestra cómo crear una tabla formateada de 2x2.

```

 Document doc = new Document();
 DocumentBuilder builder = new DocumentBuilder(doc);

 Table table = builder.startTable();
 builder.insertCell();
 builder.getCellFormat().setVerticalAlignment(CellVerticalAlignment.CENTER);
 builder.write("Row 1, cell 1.");
 builder.insertCell();
 builder.write("Row 1, cell 2.");
 builder.endRow();

 // While building the table, the document builder will apply its current RowFormat/CellFormat property values
 // to the current row/cell that its cursor is in and any new rows/cells as it creates them.
 Assert.assertEquals(CellVerticalAlignment.CENTER, table.getRows().get(0).getCells().get(0).getCellFormat().getVerticalAlignment());
 Assert.assertEquals(CellVerticalAlignment.CENTER, table.getRows().get(0).getCells().get(1).getCellFormat().getVerticalAlignment());

 builder.insertCell();
 builder.getRowFormat().setHeight(100.0);
 builder.getRowFormat().setHeightRule(HeightRule.EXACTLY);
 builder.getCellFormat().setOrientation(TextOrientation.UPWARD);
 builder.write("Row 2, cell 1.");
 builder.insertCell();
 builder.getCellFormat().setOrientation(TextOrientation.DOWNWARD);
 builder.write("Row 2, cell 2.");
 builder.endRow();
 builder.endTable();

 // Previously added rows and cells are not retroactively affected by changes to the builder's formatting.
 Assert.assertEquals(0.0, table.getRows().get(0).getRowFormat().getHeight());
 Assert.assertEquals(HeightRule.AUTO, table.getRows().get(0).getRowFormat().getHeightRule());
 Assert.assertEquals(100.0, table.getRows().get(1).getRowFormat().getHeight());
 Assert.assertEquals(HeightRule.EXACTLY, table.getRows().get(1).getRowFormat().getHeightRule());
 Assert.assertEquals(TextOrientation.UPWARD, table.getRows().get(1).getCells().get(0).getCellFormat().getOrientation());
 Assert.assertEquals(TextOrientation.DOWNWARD, table.getRows().get(1).getCells().get(1).getCellFormat().getOrientation());

 doc.save(getArtifactsDir() + "DocumentBuilder.BuildTable.docx");
 
```

**Parameters:**
| Parámetro | Tipo | Descripción |
| --- | --- | --- |
| text | java.lang.String | La cadena a insertar en el documento. |

### writeln() {#writeln}
```
public void writeln()
```


Inserta un salto de párrafo en el documento.

 **Remarks:** 

Llama a [insertParagraph()](../../com.aspose.words/documentbuilder/\#insertParagraph).

 **Examples:** 

Muestra cómo crear encabezados y pies de página en un documento usando DocumentBuilder.

```

 Document doc = new Document();
 DocumentBuilder builder = new DocumentBuilder(doc);

 // Specify that we want different headers and footers for first, even and odd pages.
 builder.getPageSetup().setDifferentFirstPageHeaderFooter(true);
 builder.getPageSetup().setOddAndEvenPagesHeaderFooter(true);

 // Create the headers, then add three pages to the document to display each header type.
 builder.moveToHeaderFooter(HeaderFooterType.HEADER_FIRST);
 builder.write("Header for the first page");
 builder.moveToHeaderFooter(HeaderFooterType.HEADER_EVEN);
 builder.write("Header for even pages");
 builder.moveToHeaderFooter(HeaderFooterType.HEADER_PRIMARY);
 builder.write("Header for all other pages");

 builder.moveToSection(0);
 builder.writeln("Page1");
 builder.insertBreak(BreakType.PAGE_BREAK);
 builder.writeln("Page2");
 builder.insertBreak(BreakType.PAGE_BREAK);
 builder.writeln("Page3");

 doc.save(getArtifactsDir() + "DocumentBuilder.HeadersAndFooters.docx");
 
```

### writeln(String text) {#writeln-java.lang.String}
```
public void writeln(String text)
```


Inserta una cadena y un salto de párrafo en el documento.

 **Remarks:** 

Se utilizan el formato de fuente y de párrafo actuales especificados por las propiedades [getFont()](../../com.aspose.words/documentbuilder/\#getFont) y [getParagraphFormat()](../../com.aspose.words/documentbuilder/\#getParagraphFormat).

 **Examples:** 

Muestra cómo crear una tabla formateada de 2x2.

```

 Document doc = new Document();
 DocumentBuilder builder = new DocumentBuilder(doc);

 Table table = builder.startTable();
 builder.insertCell();
 builder.getCellFormat().setVerticalAlignment(CellVerticalAlignment.CENTER);
 builder.write("Row 1, cell 1.");
 builder.insertCell();
 builder.write("Row 1, cell 2.");
 builder.endRow();

 // While building the table, the document builder will apply its current RowFormat/CellFormat property values
 // to the current row/cell that its cursor is in and any new rows/cells as it creates them.
 Assert.assertEquals(CellVerticalAlignment.CENTER, table.getRows().get(0).getCells().get(0).getCellFormat().getVerticalAlignment());
 Assert.assertEquals(CellVerticalAlignment.CENTER, table.getRows().get(0).getCells().get(1).getCellFormat().getVerticalAlignment());

 builder.insertCell();
 builder.getRowFormat().setHeight(100.0);
 builder.getRowFormat().setHeightRule(HeightRule.EXACTLY);
 builder.getCellFormat().setOrientation(TextOrientation.UPWARD);
 builder.write("Row 2, cell 1.");
 builder.insertCell();
 builder.getCellFormat().setOrientation(TextOrientation.DOWNWARD);
 builder.write("Row 2, cell 2.");
 builder.endRow();
 builder.endTable();

 // Previously added rows and cells are not retroactively affected by changes to the builder's formatting.
 Assert.assertEquals(0.0, table.getRows().get(0).getRowFormat().getHeight());
 Assert.assertEquals(HeightRule.AUTO, table.getRows().get(0).getRowFormat().getHeightRule());
 Assert.assertEquals(100.0, table.getRows().get(1).getRowFormat().getHeight());
 Assert.assertEquals(HeightRule.EXACTLY, table.getRows().get(1).getRowFormat().getHeightRule());
 Assert.assertEquals(TextOrientation.UPWARD, table.getRows().get(1).getCells().get(0).getCellFormat().getOrientation());
 Assert.assertEquals(TextOrientation.DOWNWARD, table.getRows().get(1).getCells().get(1).getCellFormat().getOrientation());

 doc.save(getArtifactsDir() + "DocumentBuilder.BuildTable.docx");
 
```

**Parameters:**
| Parámetro | Tipo | Descripción |
| --- | --- | --- |
| text | java.lang.String | La cadena a insertar en el documento. |

