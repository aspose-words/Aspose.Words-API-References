---
title: "DocumentBuilder"
linktitle: "DocumentBuilder"
second_title: "Aspose.Words pour Java"
description: "Fournit des méthodes pour insérer du texte, des images et d'autres contenus, spécifier la police, le paragraphe et le formatage des sections en Java."
type: docs
weight: 163
url: /fr/java/com.aspose.words/documentbuilder/
---

**Inheritance:**
java.lang.Object
```
public class DocumentBuilder
```

Fournit des méthodes pour insérer du texte, des images et d'autres contenus, spécifier la police, le formatage des paragraphes et des sections.

Pour en savoir plus, consultez l'article de documentation [ Document Builder Overview ][Document Builder Overview].

 **Remarks:** 

[DocumentBuilder](../../com.aspose.words/documentbuilder/) makes the process of building a [Document](../../com.aspose.words/document/) easier. [Document](../../com.aspose.words/document/) is a composite object consisting of a tree of nodes and while inserting content nodes directly into the tree is possible, it requires good understanding of the tree structure. [DocumentBuilder](../../com.aspose.words/documentbuilder/) is a "facade" for the complex structure of [Document](../../com.aspose.words/document/) and allows to insert content and formatting quickly and easily.

Créez un [DocumentBuilder](../../com.aspose.words/documentbuilder/) et associez-le à un [Document](../../com.aspose.words/document/).

Le [DocumentBuilder](../../com.aspose.words/documentbuilder/) possède un curseur interne où le texte sera inséré lorsque vous appelez [write(java.lang.String)](../../com.aspose.words/documentbuilder/\#write-java.lang.String), [writeln(java.lang.String)](../../com.aspose.words/documentbuilder/\#writeln-java.lang.String), **M:Aspose.Words.DocumentBuilder.InsertBreak(Aspose.Words.BreakType)** et d'autres méthodes. Vous pouvez déplacer le curseur du [DocumentBuilder](../../com.aspose.words/documentbuilder/) vers un autre emplacement dans un document en utilisant diverses méthodes MoveToXXX.

Utilisez la propriété [getFont()](../../com.aspose.words/documentbuilder/\#getFont) pour spécifier le formatage des caractères qui s'appliquera à tout le texte inséré à partir de la position actuelle dans le document.

Utilisez la propriété [getParagraphFormat()](../../com.aspose.words/documentbuilder/\#getParagraphFormat) pour spécifier le formatage des paragraphes pour le paragraphe actuel et tous les paragraphes qui seront insérés.

Utilisez la propriété [getPageSetup()](../../com.aspose.words/documentbuilder/\#getPageSetup) pour spécifier les propriétés de page et de section pour la section actuelle et toutes les sections qui seront insérées.

Utilisez les propriétés [getCellFormat()](../../com.aspose.words/documentbuilder/\#getCellFormat) et [getRowFormat()](../../com.aspose.words/documentbuilder/\#getRowFormat) pour spécifier les propriétés de formatage des cellules et des lignes de tableau. Utilisez les méthodes [insertCell()](../../com.aspose.words/documentbuilder/\#insertCell) et [endRow()](../../com.aspose.words/documentbuilder/\#endRow) pour créer un tableau.

Notez que les propriétés [getFont()](../../com.aspose.words/documentbuilder/\#getFont), [getParagraphFormat()](../../com.aspose.words/documentbuilder/\#getParagraphFormat) et [getPageSetup()](../../com.aspose.words/documentbuilder/\#getPageSetup) sont mises à jour chaque fois que vous naviguez vers un autre emplacement dans le document afin de refléter les propriétés de formatage disponibles à ce nouvel emplacement.

 **Examples:** 

Montre comment créer des en-têtes et pieds de page dans un document en utilisant DocumentBuilder.

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

Montre comment créer un tableau avec des bordures personnalisées.

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

Montre comment utiliser un document builder pour créer un tableau.

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
## Constructors

| Constructor | Description |
| --- | --- |
| [DocumentBuilder()](#DocumentBuilder) | Initialise une nouvelle instance de cette classe. |
| [DocumentBuilder(DocumentBuilderOptions options)](#DocumentBuilder-com.aspose.words.DocumentBuilderOptions) | Initialise une nouvelle instance de cette classe. |
| [DocumentBuilder(Document doc)](#DocumentBuilder-com.aspose.words.Document) | Initialise une nouvelle instance de cette classe. |
| [DocumentBuilder(Document doc, DocumentBuilderOptions options)](#DocumentBuilder-com.aspose.words.Document-com.aspose.words.DocumentBuilderOptions) | Initialise une nouvelle instance de cette classe. |
## Méthodes

| Méthode | Description |
| --- | --- |
| [clearCellAttrs()](#clearCellAttrs) |  |
| [clearParaAttrs()](#clearParaAttrs) |  |
| [clearRowAttrs()](#clearRowAttrs) |  |
| [clearRunAttrs()](#clearRunAttrs) |  |
| [deleteRow(int tableIndex, int rowIndex)](#deleteRow-int-int) | Supprime une ligne d'un tableau. |
| [endBookmark(String bookmarkName)](#endBookmark-java.lang.String) | Marque la position actuelle dans le document comme la fin d'un signet. |
| [endColumnBookmark(String bookmarkName)](#endColumnBookmark-java.lang.String) | Marque la position actuelle dans le document comme la fin d'un signet de colonne. |
| [endEditableRange()](#endEditableRange) | Marque la position actuelle dans le document comme la fin d'une plage modifiable. |
| [endEditableRange(EditableRangeStart start)](#endEditableRange-com.aspose.words.EditableRangeStart) | Marque la position actuelle dans le document comme la fin d'une plage modifiable. |
| [endRow()](#endRow) | Termine une ligne de tableau dans le document. |
| [endTable()](#endTable) | Termine un tableau dans le document. |
| [fetchCellAttr(int key)](#fetchCellAttr-int) |  |
| [fetchInheritedCellAttr(int key)](#fetchInheritedCellAttr-int) |  |
| [fetchInheritedParaAttr(int key)](#fetchInheritedParaAttr-int) |  |
| [fetchInheritedRowAttr(int key)](#fetchInheritedRowAttr-int) |  |
| [fetchInheritedRunAttr(int fontAttr)](#fetchInheritedRunAttr-int) |  |
| [fetchParaAttr(int key)](#fetchParaAttr-int) |  |
| [fetchRowAttr(int key)](#fetchRowAttr-int) |  |
| [getBold()](#getBold) | Vrai si la police est formatée en gras. |
| [getCellFormat()](#getCellFormat) | Renvoie un objet qui représente les propriétés de formatage de la cellule de tableau actuelle. |
| [getCurrentNode()](#getCurrentNode) | Obtient le nœud actuellement sélectionné dans ce DocumentBuilder. |
| [getCurrentParagraph()](#getCurrentParagraph) | Obtient le paragraphe actuellement sélectionné dans ce [DocumentBuilder](../../com.aspose.words/documentbuilder/). |
| [getCurrentSection()](#getCurrentSection) | Obtient la section actuellement sélectionnée dans ce [DocumentBuilder](../../com.aspose.words/documentbuilder/). |
| [getCurrentStory()](#getCurrentStory) | Obtient le story actuellement sélectionné dans ce [DocumentBuilder](../../com.aspose.words/documentbuilder/). |
| [getCurrentStructuredDocumentTag()](#getCurrentStructuredDocumentTag) | Obtient la balise de document structuré actuellement sélectionnée dans ce [DocumentBuilder](../../com.aspose.words/documentbuilder/). |
| [getDirectCellAttr(int key)](#getDirectCellAttr-int) |  |
| [getDirectParaAttr(int key)](#getDirectParaAttr-int) |  |
| [getDirectParaAttr(int key, int revisionsView)](#getDirectParaAttr-int-int) |  |
| [getDirectRowAttr(int key)](#getDirectRowAttr-int) |  |
| [getDirectRunAttr(int fontAttr)](#getDirectRunAttr-int) |  |
| [getDirectRunAttr(int key, int revisionsView)](#getDirectRunAttr-int-int) |  |
| [getDocument()](#getDocument) | Obtient l'objet [getDocument()](../../com.aspose.words/documentbuilder/\#getDocument) / [setDocument(com.aspose.words.Document)](../../com.aspose.words/documentbuilder/\#setDocument-com.aspose.words.Document) auquel cet objet est attaché. |
| [getFont()](#getFont) | Renvoie un objet qui représente les propriétés de formatage de la police actuelle. |
| [getItalic()](#getItalic) | Vrai si la police est formatée en italique. |
| [getListFormat()](#getListFormat) | Renvoie un objet qui représente les propriétés de formatage de la liste actuelle. |
| [getPageSetup()](#getPageSetup) | Renvoie un objet qui représente les propriétés de configuration de page et de section actuelles. |
| [getParagraphFormat()](#getParagraphFormat) | Renvoie un objet qui représente les propriétés de formatage du paragraphe actuel. |
| [getRowFormat()](#getRowFormat) | Renvoie un objet qui représente les propriétés de formatage de la ligne de tableau actuelle. |
| [getUnderline()](#getUnderline) | Obtient/définit le type de soulignement pour la police actuelle. |
| [insertBreak(int breakType)](#insertBreak-int) |  |
| [insertCell()](#insertCell) | Insère une cellule de tableau dans le document. |
| [insertChart(int chartType, double width, double height)](#insertChart-int-double-double) |  |
| [insertChart(int chartType, double width, double height, int chartStyle)](#insertChart-int-double-double-int) |  |
| [insertChart(int chartType, int horzPos, double left, int vertPos, double top, double width, double height, int wrapType)](#insertChart-int-int-double-int-double-double-double-int) |  |
| [insertChart(int chartType, int horzPos, double left, int vertPos, double top, double width, double height, int wrapType, int chartStyle)](#insertChart-int-int-double-int-double-double-double-int-int) |  |
| [insertCheckBox(String name, boolean defaultValue, boolean checkedValue, int size)](#insertCheckBox-java.lang.String-boolean-boolean-int) | Insère un champ de formulaire case à cocher à la position actuelle. |
| [insertCheckBox(String name, boolean checkedValue, int size)](#insertCheckBox-java.lang.String-boolean-int) | Insère un champ de formulaire case à cocher à la position actuelle. |
| [insertComboBox(String name, String[] items, int selectedIndex)](#insertComboBox-java.lang.String-java.lang.String---int) | Insère un champ de formulaire zone de liste déroulante à la position actuelle. |
| [insertDocument(Document srcDoc, int importFormatMode)](#insertDocument-com.aspose.words.Document-int) |  |
| [insertDocument(Document srcDoc, int importFormatMode, ImportFormatOptions importFormatOptions)](#insertDocument-com.aspose.words.Document-int-com.aspose.words.ImportFormatOptions) |  |
| [insertDocumentInline(Document srcDoc, int importFormatMode, ImportFormatOptions importFormatOptions)](#insertDocumentInline-com.aspose.words.Document-int-com.aspose.words.ImportFormatOptions) |  |
| [insertField(int fieldType, boolean updateField)](#insertField-int-boolean) |  |
| [insertField(String fieldCode)](#insertField-java.lang.String) | Insère un champ Word dans un document et met à jour le résultat du champ. |
| [insertField(String fieldCode, String fieldValue)](#insertField-java.lang.String-java.lang.String) | Insère un champ Word dans un document sans mettre à jour le résultat du champ. |
| [insertFootnote(int footnoteType, String footnoteText)](#insertFootnote-int-java.lang.String) |  |
| [insertFootnote(int footnoteType, String footnoteText, String referenceMark)](#insertFootnote-int-java.lang.String-java.lang.String) |  |
| [insertForms2OleControl(Forms2OleControl forms2OleControl)](#insertForms2OleControl-com.aspose.words.Forms2OleControl) | Insère l'objet [Forms2OleControl](../../com.aspose.words/forms2olecontrol/) dans la position actuelle.. |
| [insertGroupShape(ShapeBase[] shapes)](#insertGroupShape-com.aspose.words.ShapeBase...) | Regroupe les formes passées en paramètre dans un nouveau nœud GroupShape qui est inséré à la position actuelle. |
| [insertGroupShape(double left, double top, double width, double height, ShapeBase[] shapes)](#insertGroupShape-double-double-double-double-com.aspose.words.ShapeBase...) | Regroupe les formes passées en paramètre dans un nouveau nœud GroupShape de la taille spécifiée qui est inséré à la position spécifiée. |
| [insertHorizontalRule()](#insertHorizontalRule) | Insère une forme de règle horizontale dans le document. |
| [insertHtml(String html)](#insertHtml-java.lang.String) | Insère une chaîne HTML dans le document. |
| [insertHtml(String html, boolean useBuilderFormatting)](#insertHtml-java.lang.String-boolean) | Insère une chaîne HTML dans le document. |
| [insertHtml(String html, int options)](#insertHtml-java.lang.String-int) |  |
| [insertHyperlink(String displayText, String urlOrBookmark, boolean isBookmark)](#insertHyperlink-java.lang.String-java.lang.String-boolean) | Insère un hyperlien dans le document. |
| [insertImage(byte[] imageBytes)](#insertImage-byte) | Insère une image à partir d'un tableau d'octets dans le document. |
| [insertImage(byte[] imageBytes, double width, double height)](#insertImage-byte---double-double) | Insère une image en ligne à partir d'un tableau d'octets dans le document et la redimensionne à la taille spécifiée. |
| [insertImage(byte[] imageBytes, int horzPos, double left, int vertPos, double top, double width, double height, int wrapType)](#insertImage-byte---int-double-int-double-double-double-int) |  |
| [insertImage(BufferedImage image)](#insertImage-java.awt.image.BufferedImage) | Insère une image dans le document. |
| [insertImage(BufferedImage image, double width, double height)](#insertImage-java.awt.image.BufferedImage-double-double) | Insère une image en ligne à partir d'un objet java.awt.image.BufferedImage dans le document et la redimensionne à la taille spécifiée. |
| [insertImage(BufferedImage image, int horzPos, double left, int vertPos, double top, double width, double height, int wrapType)](#insertImage-java.awt.image.BufferedImage-int-double-int-double-double-double-int) |  |
| [insertImage(InputStream stream)](#insertImage-java.io.InputStream) |  |
| [insertImage(InputStream stream, double width, double height)](#insertImage-java.io.InputStream-double-double) |  |
| [insertImage(InputStream stream, int horzPos, double left, int vertPos, double top, double width, double height, int wrapType)](#insertImage-java.io.InputStream-int-double-int-double-double-double-int) |  |
| [insertImage(String fileName)](#insertImage-java.lang.String) | Insère une image à partir d'un fichier ou d'une URL dans le document. |
| [insertImage(String fileName, double width, double height)](#insertImage-java.lang.String-double-double) | Insère une image en ligne à partir d'un fichier ou d'une URL dans le document et la redimensionne à la taille spécifiée. |
| [insertImage(String fileName, int horzPos, double left, int vertPos, double top, double width, double height, int wrapType)](#insertImage-java.lang.String-int-double-int-double-double-double-int) |  |
| [insertNode(Node node)](#insertNode-com.aspose.words.Node) | Insère un nœud avant le curseur. |
| [insertOleObject(InputStream stream, String progId, boolean asIcon, InputStream presentation)](#insertOleObject-java.io.InputStream-java.lang.String-boolean-java.io.InputStream) |  |
| [insertOleObject(String fileName, boolean isLinked, boolean asIcon, InputStream presentation)](#insertOleObject-java.lang.String-boolean-boolean-java.io.InputStream) |  |
| [insertOleObject(String fileName, String progId, boolean isLinked, boolean asIcon, InputStream presentation)](#insertOleObject-java.lang.String-java.lang.String-boolean-boolean-java.io.InputStream) |  |
| [insertOleObjectAsIcon(InputStream stream, String progId, String iconFile, String iconCaption)](#insertOleObjectAsIcon-java.io.InputStream-java.lang.String-java.lang.String-java.lang.String) |  |
| [insertOleObjectAsIcon(String fileName, boolean isLinked, String iconFile, String iconCaption)](#insertOleObjectAsIcon-java.lang.String-boolean-java.lang.String-java.lang.String) | Insère un objet OLE incorporé ou lié sous forme d'icône dans le document. |
| [insertOleObjectAsIcon(String fileName, String progId, boolean isLinked, String iconFile, String iconCaption)](#insertOleObjectAsIcon-java.lang.String-java.lang.String-boolean-java.lang.String-java.lang.String) | Insère un objet OLE incorporé ou lié sous forme d'icône dans le document. |
| [insertOnlineVideo(String videoUrl, double width, double height)](#insertOnlineVideo-java.lang.String-double-double) | Insère un objet vidéo en ligne dans le document et le redimensionne à la taille spécifiée. |
| [insertOnlineVideo(String videoUrl, int horzPos, double left, int vertPos, double top, double width, double height, int wrapType)](#insertOnlineVideo-java.lang.String-int-double-int-double-double-double-int) |  |
| [insertOnlineVideo(String videoUrl, String videoEmbedCode, byte[] thumbnailImageBytes, double width, double height)](#insertOnlineVideo-java.lang.String-java.lang.String-byte---double-double) | Insère un objet vidéo en ligne dans le document et le redimensionne à la taille spécifiée. |
| [insertOnlineVideo(String videoUrl, String videoEmbedCode, byte[] thumbnailImageBytes, int horzPos, double left, int vertPos, double top, double width, double height, int wrapType)](#insertOnlineVideo-java.lang.String-java.lang.String-byte---int-double-int-double-double-double-int) |  |
| [insertParagraph()](#insertParagraph) | Insère un saut de paragraphe dans le document. |
| [insertShape(int shapeType, double width, double height)](#insertShape-int-double-double) |  |
| [insertShape(int shapeType, int horzPos, double left, int vertPos, double top, double width, double height, int wrapType)](#insertShape-int-int-double-int-double-double-double-int) |  |
| [insertSignatureLine(SignatureLineOptions signatureLineOptions)](#insertSignatureLine-com.aspose.words.SignatureLineOptions) | Insère une ligne de signature à la position actuelle. |
| [insertSignatureLine(SignatureLineOptions signatureLineOptions, int horzPos, double left, int vertPos, double top, int wrapType)](#insertSignatureLine-com.aspose.words.SignatureLineOptions-int-double-int-double-int) |  |
| [insertStructuredDocumentTag(int type)](#insertStructuredDocumentTag-int) |  |
| [insertStyleSeparator()](#insertStyleSeparator) | Insère un séparateur de style dans le document. |
| [insertTableOfContents(String switches)](#insertTableOfContents-java.lang.String) | Insère un champ TOC (table des matières) dans le document. |
| [insertTextInput(String name, int type, String format, String fieldValue, int maxLength)](#insertTextInput-java.lang.String-int-java.lang.String-java.lang.String-int) |  |
| [isAtEndOfParagraph()](#isAtEndOfParagraph) | Renvoie  true  si le curseur est à la fin du paragraphe actuel. |
| [isAtEndOfStructuredDocumentTag()](#isAtEndOfStructuredDocumentTag) | Renvoie **true** si le curseur est à la fin d’une balise de document structuré. |
| [isAtStartOfParagraph()](#isAtStartOfParagraph) | Renvoie  true  si le curseur est au début du paragraphe actuel (aucun texte avant le curseur). |
| [moveTo(Node node)](#moveTo-com.aspose.words.Node) | Déplace le curseur vers un nœud en ligne ou vers la fin d’un paragraphe. |
| [moveToBookmark(String bookmarkName)](#moveToBookmark-java.lang.String) | Déplace le curseur vers un signet. |
| [moveToBookmark(String bookmarkName, boolean isStart, boolean isAfter)](#moveToBookmark-java.lang.String-boolean-boolean) | Déplace le curseur vers un signet avec une plus grande précision. |
| [moveToCell(int tableIndex, int rowIndex, int columnIndex, int characterIndex)](#moveToCell-int-int-int-int) | Déplace le curseur vers une cellule de tableau dans la section actuelle. |
| [moveToDocumentEnd()](#moveToDocumentEnd) | Déplace le curseur vers la fin du document. |
| [moveToDocumentStart()](#moveToDocumentStart) | Déplace le curseur vers le début du document. |
| [moveToField(Field field, boolean isAfter)](#moveToField-com.aspose.words.Field-boolean) | Déplace le curseur vers un champ dans le document. |
| [moveToHeaderFooter(int headerFooterType)](#moveToHeaderFooter-int) |  |
| [moveToMergeField(String fieldName)](#moveToMergeField-java.lang.String) | Déplace le curseur vers le champ de fusion spécifié. |
| [moveToMergeField(String fieldName, boolean isAfter, boolean isDeleteField)](#moveToMergeField-java.lang.String-boolean-boolean) | Déplace le champ de fusion vers le champ de fusion spécifié. |
| [moveToParagraph(int paragraphIndex, int characterIndex)](#moveToParagraph-int-int) | Déplace le curseur vers un paragraphe dans la section actuelle. |
| [moveToSection(int sectionIndex)](#moveToSection-int) | Déplace le curseur vers le début du corps dans une section spécifiée. |
| [moveToStructuredDocumentTag(StructuredDocumentTag structuredDocumentTag, int characterIndex)](#moveToStructuredDocumentTag-com.aspose.words.StructuredDocumentTag-int) | Déplace le curseur vers la balise de document structuré. |
| [moveToStructuredDocumentTag(int structuredDocumentTagIndex, int characterIndex)](#moveToStructuredDocumentTag-int-int) | Déplace le curseur vers une balise de document structuré dans la section actuelle. |
| [popFont()](#popFont) | Récupère le formatage de caractères précédemment enregistré sur la pile. |
| [pushFont()](#pushFont) | Enregistre le formatage de caractères actuel sur la pile. |
| [removeParaAttr(int key)](#removeParaAttr-int) |  |
| [removeRunAttr(int key)](#removeRunAttr-int) |  |
| [resetToDefaultAttrs()](#resetToDefaultAttrs) |  |
| [setBold(boolean value)](#setBold-boolean) | Vrai si la police est formatée en gras. |
| [setCellAttr(int key, Object value)](#setCellAttr-int-java.lang.Object) |  |
| [setDocument(Document value)](#setDocument-com.aspose.words.Document) | Définit l’objet [getDocument()](../../com.aspose.words/documentbuilder/\#getDocument) / [setDocument(com.aspose.words.Document)](../../com.aspose.words/documentbuilder/\#setDocument-com.aspose.words.Document) auquel cet objet est attaché. |
| [setItalic(boolean value)](#setItalic-boolean) | Vrai si la police est formatée en italique. |
| [setParaAttr(int key, Object value)](#setParaAttr-int-java.lang.Object) |  |
| [setRowAttr(int key, Object value)](#setRowAttr-int-java.lang.Object) |  |
| [setRunAttr(int fontAttr, Object value)](#setRunAttr-int-java.lang.Object) |  |
| [setUnderline(int value)](#setUnderline-int) | Obtient/définit le type de soulignement pour la police actuelle. |
| [startBookmark(String bookmarkName)](#startBookmark-java.lang.String) | Marque la position actuelle dans le document comme le début d’un signet. |
| [startColumnBookmark(String bookmarkName)](#startColumnBookmark-java.lang.String) | Marque la position actuelle dans le document comme le début d’un signet de colonne. |
| [startEditableRange()](#startEditableRange) | Marque la position actuelle dans le document comme le début d'une plage modifiable. |
| [startTable()](#startTable) | Démarre un tableau dans le document. |
| [write(String text)](#write-java.lang.String) | Insère une chaîne dans le document à la position d'insertion actuelle. |
| [writeln()](#writeln) | Insère un saut de paragraphe dans le document. |
| [writeln(String text)](#writeln-java.lang.String) | Insère une chaîne et un saut de paragraphe dans le document. |
### DocumentBuilder() {#DocumentBuilder}
```
public DocumentBuilder()
```


Initialise une nouvelle instance de cette classe.

 **Remarks:** 

Crée un nouvel objet [DocumentBuilder](../../com.aspose.words/documentbuilder/) et le lie à un nouvel objet [Document](../../com.aspose.words/document/).

 **Examples:** 

Montre comment insérer du texte formaté en utilisant DocumentBuilder.

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


Initialise une nouvelle instance de cette classe.

 **Remarks:** 

Crée un nouvel objet [DocumentBuilder](../../com.aspose.words/documentbuilder/) et le lie à un nouvel objet [Document](../../com.aspose.words/document/). Des options supplémentaires de création de document peuvent être spécifiées.

 **Examples:** 

Montre comment ignorer le formatage du tableau pour le contenu suivant.

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
| Paramètre | Type | Description |
| --- | --- | --- |
| options | [DocumentBuilderOptions](../../com.aspose.words/documentbuilderoptions/) |  |

### DocumentBuilder(Document doc) {#DocumentBuilder-com.aspose.words.Document}
```
public DocumentBuilder(Document doc)
```


Initialise une nouvelle instance de cette classe.

 **Remarks:** 

Crée un nouvel objet [DocumentBuilder](../../com.aspose.words/documentbuilder/), le lie à l'objet [Document](../../com.aspose.words/document/) spécifié. Le curseur est positionné au début du document.

 **Examples:** 

Montre comment créer des en-têtes et pieds de page dans un document en utilisant DocumentBuilder.

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

Montre comment insérer une table des matières (TOC) dans un document en utilisant les styles de titres comme entrées.

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
| Paramètre | Type | Description |
| --- | --- | --- |
| doc | [Document](../../com.aspose.words/document/) | L'objet [Document](../../com.aspose.words/document/) auquel se lier. |

### DocumentBuilder(Document doc, DocumentBuilderOptions options) {#DocumentBuilder-com.aspose.words.Document-com.aspose.words.DocumentBuilderOptions}
```
public DocumentBuilder(Document doc, DocumentBuilderOptions options)
```


Initialise une nouvelle instance de cette classe.

 **Remarks:** 

Crée un nouvel objet [DocumentBuilder](../../com.aspose.words/documentbuilder/), le lie à l'objet [Document](../../com.aspose.words/document/) spécifié. Le curseur est positionné au début du document.

 **Examples:** 

Montre comment ignorer le formatage du tableau pour le contenu suivant.

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
| Paramètre | Type | Description |
| --- | --- | --- |
| doc | [Document](../../com.aspose.words/document/) | L'objet [Document](../../com.aspose.words/document/) auquel se lier. |
| options | [DocumentBuilderOptions](../../com.aspose.words/documentbuilderoptions/) | Options supplémentaires pour le processus de création de document. |

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


Supprime une ligne d'un tableau.

 **Remarks:** 

Si le curseur se trouve à l'intérieur de la ligne qui est supprimée, le curseur est déplacé vers la ligne suivante ou vers le paragraphe suivant après le tableau.

Si vous supprimez une ligne d'un tableau qui ne contient qu'une seule ligne, le tableau entier est supprimé.

Pour les paramètres d'index, lorsque l'index est supérieur ou égal à 0, il indique un index depuis le début avec 0 étant le premier élément. Lorsque l'index est inférieur à 0, il indique un index depuis la fin avec -1 étant le dernier élément.

 **Examples:** 

Montre comment supprimer une ligne d'un tableau.

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
| Paramètre | Type | Description |
| --- | --- | --- |
| tableIndex | int | L'index du tableau. |
| rowIndex | int | L'index de la ligne dans le tableau. |

**Returns:**
[Row](../../com.aspose.words/row/) - The row node that was just removed.
### endBookmark(String bookmarkName) {#endBookmark-java.lang.String}
```
public BookmarkEnd endBookmark(String bookmarkName)
```


Marque la position actuelle dans le document comme la fin d'un signet.

 **Remarks:** 

Les signets dans un document peuvent se chevaucher et couvrir n'importe quelle plage. Pour créer un signet valide, vous devez appeler à la fois [startBookmark(java.lang.String)](../../com.aspose.words/documentbuilder/\#startBookmark-java.lang.String) et [endBookmark(java.lang.String)](../../com.aspose.words/documentbuilder/\#endBookmark-java.lang.String) avec le même  bookmarkName  parameter.

Les signets mal formés ou les signets avec des noms en double seront ignorés lors de l'enregistrement du document.

 **Examples:** 

Montre comment créer un signet.

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

Montre comment insérer un hyperlien qui référence un signet local.

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
| Paramètre | Type | Description |
| --- | --- | --- |
| bookmarkName | java.lang.String | Nom du signet. |

**Returns:**
[BookmarkEnd](../../com.aspose.words/bookmarkend/) - The bookmark end node that was just created.
### endColumnBookmark(String bookmarkName) {#endColumnBookmark-java.lang.String}
```
public BookmarkEnd endColumnBookmark(String bookmarkName)
```


Marque la position actuelle dans le document comme la fin d'un signet de colonne. La position doit être dans une cellule de tableau.

 **Remarks:** 

Un signet de colonne couvre une ou plusieurs colonnes dans une plage de lignes. Pour créer un signet valide, vous devez appeler à la fois [startColumnBookmark(java.lang.String)](../../com.aspose.words/documentbuilder/\#startColumnBookmark-java.lang.String) et [endColumnBookmark(java.lang.String)](../../com.aspose.words/documentbuilder/\#endColumnBookmark-java.lang.String) avec le même  bookmarkName  paramètre.

Les signets mal formés ou les signets avec des noms en double seront ignorés lors de l'enregistrement du document.

La position réelle du nœud [BookmarkEnd](../../com.aspose.words/bookmarkend/) inséré peut différer de la position actuelle du DocumentBuilder.

 **Examples:** 

Montre comment créer un signet de colonne.

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
| Paramètre | Type | Description |
| --- | --- | --- |
| bookmarkName | java.lang.String | Nom du signet. |

**Returns:**
[BookmarkEnd](../../com.aspose.words/bookmarkend/) - The bookmark end node that was just created.
### endEditableRange() {#endEditableRange}
```
public EditableRangeEnd endEditableRange()
```


Marque la position actuelle dans le document comme la fin d'une plage modifiable.

 **Remarks:** 

Une plage modifiable dans un document peut se chevaucher et couvrir n'importe quelle plage. Pour créer une plage modifiable valide, vous devez appeler les méthodes [startEditableRange()](../../com.aspose.words/documentbuilder/\#startEditableRange) et [endEditableRange()](../../com.aspose.words/documentbuilder/\#endEditableRange) ou [endEditableRange(com.aspose.words.EditableRangeStart)](../../com.aspose.words/documentbuilder/\#endEditableRange-com.aspose.words.EditableRangeStart).

Une plage modifiable mal formée sera ignorée lors de l'enregistrement du document.

 **Examples:** 

Montre comment travailler avec une plage éditable.

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


Marque la position actuelle dans le document comme la fin d'une plage modifiable.

 **Remarks:** 

Utilisez cette surcharge lors de la création de plages modifiables imbriquées.

Une plage modifiable dans un document peut se chevaucher et couvrir n'importe quelle plage. Pour créer une plage modifiable valide, vous devez appeler les méthodes [startEditableRange()](../../com.aspose.words/documentbuilder/\#startEditableRange) et [endEditableRange()](../../com.aspose.words/documentbuilder/\#endEditableRange) ou [endEditableRange(com.aspose.words.EditableRangeStart)](../../com.aspose.words/documentbuilder/\#endEditableRange-com.aspose.words.EditableRangeStart).

Une plage modifiable mal formée sera ignorée lors de l'enregistrement du document.

 **Examples:** 

Montre comment créer des plages éditables imbriquées.

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
| Paramètre | Type | Description |
| --- | --- | --- |
| start | [EditableRangeStart](../../com.aspose.words/editablerangestart/) | Début de cette plage modifiable. |

**Returns:**
[EditableRangeEnd](../../com.aspose.words/editablerangeend/) - The editable range end node that was just created.
### endRow() {#endRow}
```
public Row endRow()
```


Termine une ligne de tableau dans le document.

 **Remarks:** 

Appelez [endRow()](../../com.aspose.words/documentbuilder/\#endRow) pour terminer une ligne de tableau. Si vous appelez immédiatement [insertCell()](../../com.aspose.words/documentbuilder/\#insertCell) après cela, le tableau continue sur une nouvelle ligne.

Utilisez la propriété [getRowFormat()](../../com.aspose.words/documentbuilder/\#getRowFormat) pour spécifier le formatage des lignes.

 **Examples:** 

Montre comment fusionner les cellules de tableau verticalement.

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

Montre comment créer un tableau avec des bordures personnalisées.

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

Montre comment créer un tableau 2x2 formaté.

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


Termine un tableau dans le document.

 **Remarks:** 

Cette méthode doit être appelée une seule fois après que [endRow()](../../com.aspose.words/documentbuilder/\#endRow) a été appelé. Lorsqu'elle est appelée, [endTable()](../../com.aspose.words/documentbuilder/\#endTable) déplace le curseur hors de la cellule actuelle pour le placer juste après le tableau.

 **Examples:** 

Montre comment créer un tableau avec des bordures personnalisées.

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

Montre comment créer un tableau 2x2 formaté.

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

Montre comment formater les cellules avec un DocumentBuilder.

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
| Paramètre | Type | Description |
| --- | --- | --- |
| key | int |  |

**Returns:**
java.lang.Object
### fetchInheritedCellAttr(int key) {#fetchInheritedCellAttr-int}
```
public Object fetchInheritedCellAttr(int key)
```




**Parameters:**
| Paramètre | Type | Description |
| --- | --- | --- |
| key | int |  |

**Returns:**
java.lang.Object
### fetchInheritedParaAttr(int key) {#fetchInheritedParaAttr-int}
```
public Object fetchInheritedParaAttr(int key)
```




**Parameters:**
| Paramètre | Type | Description |
| --- | --- | --- |
| key | int |  |

**Returns:**
java.lang.Object
### fetchInheritedRowAttr(int key) {#fetchInheritedRowAttr-int}
```
public Object fetchInheritedRowAttr(int key)
```




**Parameters:**
| Paramètre | Type | Description |
| --- | --- | --- |
| key | int |  |

**Returns:**
java.lang.Object
### fetchInheritedRunAttr(int fontAttr) {#fetchInheritedRunAttr-int}
```
public Object fetchInheritedRunAttr(int fontAttr)
```




**Parameters:**
| Paramètre | Type | Description |
| --- | --- | --- |
| fontAttr | int |  |

**Returns:**
java.lang.Object
### fetchParaAttr(int key) {#fetchParaAttr-int}
```
public Object fetchParaAttr(int key)
```




**Parameters:**
| Paramètre | Type | Description |
| --- | --- | --- |
| key | int |  |

**Returns:**
java.lang.Object
### fetchRowAttr(int key) {#fetchRowAttr-int}
```
public Object fetchRowAttr(int key)
```




**Parameters:**
| Paramètre | Type | Description |
| --- | --- | --- |
| key | int |  |

**Returns:**
java.lang.Object
### getBold() {#getBold}
```
public boolean getBold()
```


Vrai si la police est formatée en gras.

 **Examples:** 

Montre comment remplir les MERGEFIELDs avec des données à l'aide d'un DocumentBuilder au lieu d'une fusion de courrier.

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
boolean - La valeur  boolean  correspondante.
### getCellFormat() {#getCellFormat}
```
public CellFormat getCellFormat()
```


Renvoie un objet qui représente les propriétés de formatage de la cellule de tableau actuelle.

 **Examples:** 

Montre comment créer un tableau avec des bordures personnalisées.

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

Montre comment créer un tableau 2x2 formaté.

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

Montre comment formater les cellules avec un DocumentBuilder.

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


Obtient le nœud actuellement sélectionné dans ce DocumentBuilder.

 **Remarks:** 

[getCurrentNode()](../../com.aspose.words/documentbuilder/\#getCurrentNode) is a cursor of [DocumentBuilder](../../com.aspose.words/documentbuilder/) and points to a [Node](../../com.aspose.words/node/) that is a direct child of a [Paragraph](../../com.aspose.words/paragraph/). Any insert operations you perform using [DocumentBuilder](../../com.aspose.words/documentbuilder/) will insert before the [getCurrentNode()](../../com.aspose.words/documentbuilder/\#getCurrentNode).

Lorsque le paragraphe actuel est vide ou que le curseur est positionné juste avant la fin d'un paragraphe ou d'une balise de document structuré, [getCurrentNode()](../../com.aspose.words/documentbuilder/\#getCurrentNode) renvoie null.

 **Examples:** 

Montre comment déplacer le curseur d'un DocumentBuilder vers différents nœuds dans un document.

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


Obtient le paragraphe actuellement sélectionné dans ce [DocumentBuilder](../../com.aspose.words/documentbuilder/).

 **Remarks:** 

[getCurrentNode()](../../com.aspose.words/documentbuilder/\#getCurrentNode)

 **Examples:** 

Montre comment déplacer le curseur d'un DocumentBuilder vers différents nœuds dans un document.

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


Obtient la section actuellement sélectionnée dans ce [DocumentBuilder](../../com.aspose.words/documentbuilder/).

 **Examples:** 

Montre comment insérer une image flottante et spécifier sa position et sa taille.

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


Obtient le story actuellement sélectionné dans ce [DocumentBuilder](../../com.aspose.words/documentbuilder/).

 **Examples:** 

Montre comment travailler avec l'histoire actuelle d'un DocumentBuilder.

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


Obtient la balise de document structuré actuellement sélectionnée dans ce [DocumentBuilder](../../com.aspose.words/documentbuilder/).

 **Examples:** 

Montre comment déplacer le curseur du DocumentBuilder à l'intérieur d'une balise de document structuré.

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
| Paramètre | Type | Description |
| --- | --- | --- |
| key | int |  |

**Returns:**
java.lang.Object
### getDirectParaAttr(int key) {#getDirectParaAttr-int}
```
public Object getDirectParaAttr(int key)
```




**Parameters:**
| Paramètre | Type | Description |
| --- | --- | --- |
| key | int |  |

**Returns:**
java.lang.Object
### getDirectParaAttr(int key, int revisionsView) {#getDirectParaAttr-int-int}
```
public Object getDirectParaAttr(int key, int revisionsView)
```




**Parameters:**
| Paramètre | Type | Description |
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
| Paramètre | Type | Description |
| --- | --- | --- |
| key | int |  |

**Returns:**
java.lang.Object
### getDirectRunAttr(int fontAttr) {#getDirectRunAttr-int}
```
public Object getDirectRunAttr(int fontAttr)
```




**Parameters:**
| Paramètre | Type | Description |
| --- | --- | --- |
| fontAttr | int |  |

**Returns:**
java.lang.Object
### getDirectRunAttr(int key, int revisionsView) {#getDirectRunAttr-int-int}
```
public Object getDirectRunAttr(int key, int revisionsView)
```




**Parameters:**
| Paramètre | Type | Description |
| --- | --- | --- |
| key | int |  |
| revisionsView | int |  |

**Returns:**
java.lang.Object
### getDocument() {#getDocument}
```
public Document getDocument()
```


Obtient l'objet [getDocument()](../../com.aspose.words/documentbuilder/\#getDocument) / [setDocument(com.aspose.words.Document)](../../com.aspose.words/documentbuilder/\#setDocument-com.aspose.words.Document) auquel cet objet est attaché.

 **Examples:** 

Montre comment appliquer et rétablir les paramètres de mise en page aux sections d'un document.

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


Renvoie un objet qui représente les propriétés de formatage de la police actuelle.

 **Remarks:** 

Utilisez [getFont()](../../com.aspose.words/documentbuilder/\#getFont) pour accéder et modifier les propriétés de formatage de la police.

Spécifiez le formatage de la police avant d'insérer du texte.

 **Examples:** 

Montre comment insérer une chaîne entourée d'une bordure dans un document.

```

 Document doc = new Document();
 DocumentBuilder builder = new DocumentBuilder(doc);

 builder.getFont().getBorder().setColor(Color.GREEN);
 builder.getFont().getBorder().setLineWidth(2.5);
 builder.getFont().getBorder().setLineStyle(LineStyle.DASH_DOT_STROKER);

 builder.write("Text surrounded by green border.");

 doc.save(getArtifactsDir() + "Border.FontBorder.docx");
 
```

Montre comment créer un tableau formaté en utilisant DocumentBuilder.

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


Vrai si la police est formatée en italique.

 **Examples:** 

Montre comment remplir les MERGEFIELDs avec des données à l'aide d'un DocumentBuilder au lieu d'une fusion de courrier.

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
boolean - La valeur  boolean  correspondante.
### getListFormat() {#getListFormat}
```
public ListFormat getListFormat()
```


Renvoie un objet qui représente les propriétés de formatage de la liste actuelle.

 **Examples:** 

Montre comment créer des listes à puces et numérotées.

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


Renvoie un objet qui représente les propriétés de configuration de page et de section actuelles.

 **Examples:** 

Montre comment appliquer et rétablir les paramètres de mise en page aux sections d'un document.

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


Renvoie un objet qui représente les propriétés de formatage du paragraphe actuel.

 **Examples:** 

Montre comment créer un tableau formaté en utilisant DocumentBuilder.

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


Renvoie un objet qui représente les propriétés de formatage de la ligne de tableau actuelle.

 **Examples:** 

Montre comment créer un tableau avec des bordures personnalisées.

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

Montre comment créer un tableau 2x2 formaté.

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

Montre comment formater les lignes avec un document builder.

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


Obtient/définit le type de soulignement pour la police actuelle.

 **Examples:** 

Montre comment formater le texte inséré par un DocumentBuilder.

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
int - La valeur int correspondante. La valeur renvoyée est l'une des constantes [Underline](../../com.aspose.words/underline/).
### insertBreak(int breakType) {#insertBreak-int}
```
public void insertBreak(int breakType)
```




**Parameters:**
| Paramètre | Type | Description |
| --- | --- | --- |
| breakType | int |  |

### insertCell() {#insertCell}
```
public Cell insertCell()
```


Insère une cellule de tableau dans le document.

 **Remarks:** 

Pour démarrer un tableau, appelez simplement [insertCell()](../../com.aspose.words/documentbuilder/\#insertCell). Après cela, tout contenu que vous ajoutez en utilisant d'autres méthodes de la classe [DocumentBuilder](../../com.aspose.words/documentbuilder/) sera ajouté à la cellule actuelle.

Pour démarrer une nouvelle cellule dans la même ligne, appelez à nouveau [insertCell()](../../com.aspose.words/documentbuilder/\#insertCell).

Pour terminer une ligne de tableau, appelez [endRow()](../../com.aspose.words/documentbuilder/\#endRow).

Utilisez la propriété [getCellFormat()](../../com.aspose.words/documentbuilder/\#getCellFormat) pour spécifier le formatage des cellules.

 **Examples:** 

Montre comment créer un tableau avec des bordures personnalisées.

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

Montre comment utiliser un document builder pour créer un tableau.

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
| Paramètre | Type | Description |
| --- | --- | --- |
| chartType | int |  |
| largeur | double |  |
| hauteur | double |  |

**Returns:**
[Shape](../../com.aspose.words/shape/)
### insertChart(int chartType, double width, double height, int chartStyle) {#insertChart-int-double-double-int}
```
public Shape insertChart(int chartType, double width, double height, int chartStyle)
```




**Parameters:**
| Paramètre | Type | Description |
| --- | --- | --- |
| chartType | int |  |
| largeur | double |  |
| hauteur | double |  |
| chartStyle | int |  |

**Returns:**
[Shape](../../com.aspose.words/shape/)
### insertChart(int chartType, int horzPos, double left, int vertPos, double top, double width, double height, int wrapType) {#insertChart-int-int-double-int-double-double-double-int}
```
public Shape insertChart(int chartType, int horzPos, double left, int vertPos, double top, double width, double height, int wrapType)
```




**Parameters:**
| Paramètre | Type | Description |
| --- | --- | --- |
| chartType | int |  |
| horzPos | int |  |
| left | double |  |
| vertPos | int |  |
| top | double |  |
| largeur | double |  |
| hauteur | double |  |
| wrapType | int |  |

**Returns:**
[Shape](../../com.aspose.words/shape/)
### insertChart(int chartType, int horzPos, double left, int vertPos, double top, double width, double height, int wrapType, int chartStyle) {#insertChart-int-int-double-int-double-double-double-int-int}
```
public Shape insertChart(int chartType, int horzPos, double left, int vertPos, double top, double width, double height, int wrapType, int chartStyle)
```




**Parameters:**
| Paramètre | Type | Description |
| --- | --- | --- |
| chartType | int |  |
| horzPos | int |  |
| left | double |  |
| vertPos | int |  |
| top | double |  |
| largeur | double |  |
| hauteur | double |  |
| wrapType | int |  |
| chartStyle | int |  |

**Returns:**
[Shape](../../com.aspose.words/shape/)
### insertCheckBox(String name, boolean defaultValue, boolean checkedValue, int size) {#insertCheckBox-java.lang.String-boolean-boolean-int}
```
public FormField insertCheckBox(String name, boolean defaultValue, boolean checkedValue, int size)
```


Insère un champ de formulaire case à cocher à la position actuelle.

 **Remarks:** 

Si vous spécifiez un nom pour le champ de formulaire, un signet est alors créé automatiquement avec le même nom.

 **Examples:** 

Montre comment insérer des cases à cocher dans le document.

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
| Paramètre | Type | Description |
| --- | --- | --- |
| nom | java.lang.String | Le nom du champ de formulaire. Peut être une chaîne vide. La valeur de plus de 20 caractères sera tronquée. |
| defaultValue | boolean | Valeur par défaut du champ de case à cocher. |
| checkedValue | boolean | État coché actuel du champ de case à cocher. |
| size | int | Spécifie la taille de la case à cocher en points. Indiquez 0 pour que MS Word calcule automatiquement la taille de la case à cocher. |

**Returns:**
[FormField](../../com.aspose.words/formfield/) - The form field node that was just inserted.
### insertCheckBox(String name, boolean checkedValue, int size) {#insertCheckBox-java.lang.String-boolean-int}
```
public FormField insertCheckBox(String name, boolean checkedValue, int size)
```


Insère un champ de formulaire case à cocher à la position actuelle.

 **Remarks:** 

Si vous spécifiez un nom pour le champ de formulaire, un signet est alors créé automatiquement avec le même nom.

 **Examples:** 

Montre comment insérer des cases à cocher dans le document.

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
| Paramètre | Type | Description |
| --- | --- | --- |
| nom | java.lang.String | Le nom du champ de formulaire. Peut être une chaîne vide. La valeur de plus de 20 caractères sera tronquée. |
| checkedValue | boolean | État coché du champ de case à cocher. |
| size | int | Spécifie la taille de la case à cocher en points. Indiquez 0 pour que MS Word calcule automatiquement la taille de la case à cocher. |

**Returns:**
[FormField](../../com.aspose.words/formfield/) - The form field node that was just inserted.
### insertComboBox(String name, String[] items, int selectedIndex) {#insertComboBox-java.lang.String-java.lang.String---int}
```
public FormField insertComboBox(String name, String[] items, int selectedIndex)
```


Insère un champ de formulaire zone de liste déroulante à la position actuelle.

 **Remarks:** 

Si vous spécifiez un nom pour le champ de formulaire, un signet est alors créé automatiquement avec le même nom.

 **Examples:** 

Montre comment créer des champs de formulaire.

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

Montre comment insérer un champ de formulaire de zone combinée dans un document.

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
| Paramètre | Type | Description |
| --- | --- | --- |
| nom | java.lang.String | Le nom du champ de formulaire. Peut être une chaîne vide. La valeur de plus de 20 caractères sera tronquée. |
| items | java.lang.String[] | Les éléments de la zone combinée. Le maximum est de 25 éléments. |
| selectedIndex | int | L'index de l'élément sélectionné dans la zone combinée. |

**Returns:**
[FormField](../../com.aspose.words/formfield/) - The form field node that was just inserted.
### insertDocument(Document srcDoc, int importFormatMode) {#insertDocument-com.aspose.words.Document-int}
```
public Node insertDocument(Document srcDoc, int importFormatMode)
```




**Parameters:**
| Paramètre | Type | Description |
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
| Paramètre | Type | Description |
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
| Paramètre | Type | Description |
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
| Paramètre | Type | Description |
| --- | --- | --- |
| fieldType | int |  |
| updateField | boolean |  |

**Returns:**
[Field](../../com.aspose.words/field/)
### insertField(String fieldCode) {#insertField-java.lang.String}
```
public Field insertField(String fieldCode)
```


Insère un champ Word dans un document et met à jour le résultat du champ.

 **Remarks:** 

Cette méthode insère un champ dans un document et met à jour le résultat du champ immédiatement. Aspose.Words peut mettre à jour les champs de la plupart des types, mais pas tous. Pour plus de détails, voir la surcharge [insertField(java.lang.String, java.lang.String)](../../com.aspose.words/documentbuilder/\#insertField-java.lang.String--java.lang.String).

 **Examples:** 

Montre comment insérer des champs et déplacer le curseur du DocumentBuilder vers eux.

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

Montre comment insérer un champ dans un document en utilisant un code de champ.

```

 Document doc = new Document();
 DocumentBuilder builder = new DocumentBuilder(doc);

 Field dateField = builder.insertField("DATE \\* MERGEFORMAT");

 Assert.assertEquals(FieldType.FIELD_DATE, dateField.getType());
 Assert.assertEquals("DATE \\* MERGEFORMAT", dateField.getFieldCode());
 
```

**Parameters:**
| Paramètre | Type | Description |
| --- | --- | --- |
| fieldCode | java.lang.String | Le code de champ à insérer (sans accolades). |

**Returns:**
[Field](../../com.aspose.words/field/) - A [Field](../../com.aspose.words/field/) object that represents the inserted field.
### insertField(String fieldCode, String fieldValue) {#insertField-java.lang.String-java.lang.String}
```
public Field insertField(String fieldCode, String fieldValue)
```


Insère un champ Word dans un document sans mettre à jour le résultat du champ.

 **Remarks:** 

Les champs dans les documents Microsoft Word se composent d'un code de champ et d'un résultat de champ. Le code de champ est comme une formule et le résultat de champ est comme la valeur que la formule produit. Le code de champ peut également contenir des commutateurs de champ qui sont comme des instructions supplémentaires pour effectuer une action spécifique.

Vous pouvez basculer entre l'affichage des codes de champ et des résultats dans votre document Microsoft Word en utilisant le raccourci clavier Alt+F9. Les codes de champ apparaissent entre accolades ( \\{ \\} ).

Pour créer un champ, vous devez spécifier un type de champ, un code de champ et une valeur de champ \"placeholder\". Si vous n'êtes pas sûr de la syntaxe d'un code de champ particulier, créez d'abord le champ dans Microsoft Word puis basculez pour voir son code de champ.

Aspose.Words peut calculer les résultats de champ pour la plupart des types de champ, mais cette méthode ne met pas à jour le résultat du champ automatiquement. Comme le résultat du champ n'est pas calculé automatiquement, vous devez fournir une valeur de chaîne (ou même une chaîne vide) qui sera insérée dans le résultat du champ. Cette valeur restera dans le résultat du champ comme un espace réservé jusqu'à ce que le champ soit mis à jour. Pour mettre à jour le résultat du champ, vous pouvez appeler [Field.update()](../../com.aspose.words/field/\\#update) sur l'objet champ qui vous est retourné ou [Document.updateFields()](../../com.aspose.words/document/\\#updateFields) pour mettre à jour les champs dans tout le document.

 **Examples:** 

Montre comment configurer la numérotation des pages dans une section.

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
| Paramètre | Type | Description |
| --- | --- | --- |
| fieldCode | java.lang.String | Le code de champ à insérer (sans accolades). |
| fieldValue | java.lang.String | La valeur du champ à insérer. Passez  null  pour les champs qui n'ont pas de valeur. |

**Returns:**
[Field](../../com.aspose.words/field/) - A [Field](../../com.aspose.words/field/) object that represents the inserted field.
### insertFootnote(int footnoteType, String footnoteText) {#insertFootnote-int-java.lang.String}
```
public Footnote insertFootnote(int footnoteType, String footnoteText)
```




**Parameters:**
| Paramètre | Type | Description |
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
| Paramètre | Type | Description |
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


Insère l'objet [Forms2OleControl](../../com.aspose.words/forms2olecontrol/) dans la position actuelle..

 **Examples:** 

Montre comment insérer un contrôle ActiveX.

```

 DocumentBuilder builder = new DocumentBuilder();

 CommandButtonControl button1 = new CommandButtonControl();
 Shape shape = builder.insertForms2OleControl(button1);
 Assert.assertEquals(Forms2OleControlType.COMMAND_BUTTON, button1.getType());
 
```

**Parameters:**
| Paramètre | Type | Description |
| --- | --- | --- |
| forms2OleControl | [Forms2OleControl](../../com.aspose.words/forms2olecontrol/) |  |

**Returns:**
[Shape](../../com.aspose.words/shape/) - [Shape](../../com.aspose.words/shape/) object that contains passed [Forms2OleControl](../../com.aspose.words/forms2olecontrol/)
### insertGroupShape(ShapeBase[] shapes) {#insertGroupShape-com.aspose.words.ShapeBase...}
```
public GroupShape insertGroupShape(ShapeBase[] shapes)
```


Regroupe les formes passées en paramètre dans un nouveau nœud GroupShape qui est inséré à la position actuelle.

 **Remarks:** 

La position et les dimensions du nouveau GroupShape seront calculées automatiquement.

Les formes VML et DML ne peuvent pas être groupées ensemble.

 **Examples:** 

Montre comment insérer une forme groupée DML.

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

Montre comment combiner une forme groupée avec la forme.

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
| Paramètre | Type | Description |
| --- | --- | --- |
| shapes | [ShapeBase\[\]](../../com.aspose.words/shapebase/) | La liste des formes à regrouper. |

**Returns:**
[GroupShape](../../com.aspose.words/groupshape/)
### insertGroupShape(double left, double top, double width, double height, ShapeBase[] shapes) {#insertGroupShape-double-double-double-double-com.aspose.words.ShapeBase...}
```
public GroupShape insertGroupShape(double left, double top, double width, double height, ShapeBase[] shapes)
```


Regroupe les formes passées en paramètre dans un nouveau nœud GroupShape de la taille spécifiée qui est inséré à la position spécifiée.

 **Remarks:** 

Les formes VML et DML ne peuvent pas être groupées ensemble.

 **Examples:** 

Montre comment insérer une forme groupée DML.

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
| Paramètre | Type | Description |
| --- | --- | --- |
| left | double | Distance en points depuis l'origine jusqu'au côté gauche de la forme groupée. |
| top | double | Distance en points depuis l'origine jusqu'au côté supérieur de la forme groupée. |
| largeur | double | La largeur de la forme groupée en points. Une valeur négative n'est pas autorisée. |
| hauteur | double | La hauteur de la forme groupée en points. Une valeur négative n'est pas autorisée. |
| shapes | [ShapeBase\[\]](../../com.aspose.words/shapebase/) | La liste des formes à regrouper. |

**Returns:**
[GroupShape](../../com.aspose.words/groupshape/)
### insertHorizontalRule() {#insertHorizontalRule}
```
public Shape insertHorizontalRule()
```


Insère une forme de règle horizontale dans le document.

 **Examples:** 

Montre comment insérer une forme de règle horizontale et personnaliser son formatage.

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


Insère une chaîne HTML dans le document.

 **Remarks:** 

Vous pouvez utiliser cette méthode pour insérer un fragment HTML ou un document HTML complet.

 **Examples:** 

Montre comment utiliser un constructeur de document pour insérer du contenu HTML dans un document.

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

Montre comment exécuter un publipostage avec un rappel personnalisé qui gère les données de fusion sous forme de documents HTML.

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
| Paramètre | Type | Description |
| --- | --- | --- |
| html | java.lang.String | Une chaîne HTML à insérer dans le document. |

### insertHtml(String html, boolean useBuilderFormatting) {#insertHtml-java.lang.String-boolean}
```
public void insertHtml(String html, boolean useBuilderFormatting)
```


Insère une chaîne HTML dans le document.

 **Remarks:** 

Vous pouvez utiliser cette méthode pour insérer un fragment HTML ou un document HTML complet.

Lorsque  useBuilderFormatting  est  false , le formatage de [DocumentBuilder](../../com.aspose.words/documentbuilder/) est ignoré et le formatage du texte inséré est basé sur le formatage HTML par défaut. En conséquence, le texte apparaît tel qu'il est rendu dans les navigateurs.

Lorsque useBuilderFormatting est vrai, le formatage du texte inséré est basé sur le formatage de [DocumentBuilder](../../com.aspose.words/documentbuilder/), et le texte apparaît comme s'il avait été inséré avec [write(java.lang.String)](../../com.aspose.words/documentbuilder/\#write-java.lang.String).

 **Examples:** 

Montre comment appliquer le formatage d'un DocumentBuilder lors de l'insertion de contenu HTML.

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
| Paramètre | Type | Description |
| --- | --- | --- |
| html | java.lang.String | Une chaîne HTML à insérer dans le document. |
| useBuilderFormatting | boolean | Valeur indiquant si le formatage spécifié dans [DocumentBuilder](../../com.aspose.words/documentbuilder/) est utilisé comme formatage de base pour le texte importé depuis HTML. |

### insertHtml(String html, int options) {#insertHtml-java.lang.String-int}
```
public void insertHtml(String html, int options)
```




**Parameters:**
| Paramètre | Type | Description |
| --- | --- | --- |
| html | java.lang.String |  |
| options | int |  |

### insertHyperlink(String displayText, String urlOrBookmark, boolean isBookmark) {#insertHyperlink-java.lang.String-java.lang.String-boolean}
```
public Field insertHyperlink(String displayText, String urlOrBookmark, boolean isBookmark)
```


Insère un hyperlien dans le document.

 **Remarks:** 

Notez que vous devez spécifier explicitement le formatage de police pour le texte d'affichage du lien hypertexte en utilisant la propriété [getFont()](../../com.aspose.words/documentbuilder/\#getFont).

Cette méthode appelle en interne [insertField(java.lang.String)](../../com.aspose.words/documentbuilder/\#insertField-java.lang.String) pour insérer un champ HYPERLINK de MS Word dans le document.

 **Examples:** 

Montre comment insérer un champ hyperlien.

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

Montre comment utiliser la pile de formatage d'un DocumentBuilder.

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

Montre comment insérer un hyperlien qui référence un signet local.

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
| Paramètre | Type | Description |
| --- | --- | --- |
| displayText | java.lang.String | Texte du lien à afficher dans le document. |
| urlOrBookmark | java.lang.String | Destination du lien. Peut être une URL ou le nom d'un signet dans le document. Cette méthode ajoute toujours des apostrophes au début et à la fin de l'URL. |
| isBookmark | boolean | true si le paramètre précédent est le nom d'un signet dans le document ; false si le paramètre précédent est une URL. |

**Returns:**
[Field](../../com.aspose.words/field/) - A [Field](../../com.aspose.words/field/) object that represents the inserted field.
### insertImage(byte[] imageBytes) {#insertImage-byte}
```
public Shape insertImage(byte[] imageBytes)
```


Insère une image à partir d'un tableau d'octets dans le document. L'image est insérée en ligne et à 100 % d'échelle.

 **Remarks:** 

Vous pouvez modifier la taille, l'emplacement, la méthode de positionnement et d'autres paramètres de l'image en utilisant l'objet [Shape](../../com.aspose.words/shape/) retourné par cette méthode.

 **Examples:** 

Montre comment insérer une image à partir d'un tableau d'octets dans un document.

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
| Paramètre | Type | Description |
| --- | --- | --- |
| imageBytes | byte[] | Le tableau d'octets contenant l'image. |

**Returns:**
[Shape](../../com.aspose.words/shape/) - The image node that was just inserted.
### insertImage(byte[] imageBytes, double width, double height) {#insertImage-byte---double-double}
```
public Shape insertImage(byte[] imageBytes, double width, double height)
```


Insère une image en ligne à partir d'un tableau d'octets dans le document et la redimensionne à la taille spécifiée.

 **Remarks:** 

Vous pouvez modifier la taille, l'emplacement, la méthode de positionnement et d'autres paramètres de l'image en utilisant l'objet [Shape](../../com.aspose.words/shape/) retourné par cette méthode.

 **Examples:** 

Montre comment insérer une image à partir d'un tableau d'octets dans un document.

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
| Paramètre | Type | Description |
| --- | --- | --- |
| imageBytes | byte[] | Le tableau d'octets contenant l'image. |
| largeur | double | La largeur de l'image en points. Peut être une valeur négative ou zéro pour demander une échelle de 100 %. |
| hauteur | double | La hauteur de l'image en points. Peut être une valeur négative ou zéro pour demander une échelle de 100 %. |

**Returns:**
[Shape](../../com.aspose.words/shape/) - The image node that was just inserted.
### insertImage(byte[] imageBytes, int horzPos, double left, int vertPos, double top, double width, double height, int wrapType) {#insertImage-byte---int-double-int-double-double-double-int}
```
public Shape insertImage(byte[] imageBytes, int horzPos, double left, int vertPos, double top, double width, double height, int wrapType)
```




**Parameters:**
| Paramètre | Type | Description |
| --- | --- | --- |
| imageBytes | byte[] |  |
| horzPos | int |  |
| left | double |  |
| vertPos | int |  |
| top | double |  |
| largeur | double |  |
| hauteur | double |  |
| wrapType | int |  |

**Returns:**
[Shape](../../com.aspose.words/shape/)
### insertImage(BufferedImage image) {#insertImage-java.awt.image.BufferedImage}
```
public Shape insertImage(BufferedImage image)
```


Insère une image dans le document. Insère une image à partir d'un objet java.awt.image.BufferedImage dans le document. L'image est insérée en ligne et à 100 % d'échelle.

 **Remarks:** 

Vous pouvez modifier la taille, l'emplacement, la méthode de positionnement et d'autres paramètres de l'image en utilisant l'objet [Shape](../../com.aspose.words/shape/) retourné par cette méthode.

Aspose.Words insérera l'image au format PNG avec les paramètres par défaut. Si vous souhaitez insérer un  BufferedImage  dans un autre format ou avec d'autres paramètres, vous devez enregistrer l'image dans un tableau d'octets et utiliser [insertImage(byte[])](../../com.aspose.words/documentbuilder/\#insertImage-byte).

 **Examples:** 

Montre comment insérer une image à partir d'un objet dans un document.

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
| Paramètre | Type | Description |
| --- | --- | --- |
| image | java.awt.image.BufferedImage | L'image à insérer dans le document. |

**Returns:**
[Shape](../../com.aspose.words/shape/) - The image node that was just inserted.
### insertImage(BufferedImage image, double width, double height) {#insertImage-java.awt.image.BufferedImage-double-double}
```
public Shape insertImage(BufferedImage image, double width, double height)
```


Insère une image en ligne à partir d'un objet java.awt.image.BufferedImage dans le document et la redimensionne à la taille spécifiée.

 **Remarks:** 

Vous pouvez modifier la taille, l'emplacement, la méthode de positionnement et d'autres paramètres de l'image en utilisant l'objet [Shape](../../com.aspose.words/shape/) retourné par cette méthode.

Aspose.Words insérera l'image au format PNG avec les paramètres par défaut. Si vous souhaitez insérer un  BufferedImage  dans un autre format ou avec d'autres paramètres, vous devez enregistrer l'image dans un tableau d'octets et utiliser [insertImage(byte[])](../../com.aspose.words/documentbuilder/\#insertImage-byte).

 **Examples:** 

Montre comment insérer une image à partir d'un objet dans un document.

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
| Paramètre | Type | Description |
| --- | --- | --- |
| image | java.awt.image.BufferedImage | L'image à insérer dans le document. |
| largeur | double | La largeur de l'image en points. Peut être une valeur négative ou zéro pour demander une échelle de 100 %. |
| hauteur | double | La hauteur de l'image en points. Peut être une valeur négative ou zéro pour demander une échelle de 100 %. |

**Returns:**
[Shape](../../com.aspose.words/shape/) - The image node that was just inserted.
### insertImage(BufferedImage image, int horzPos, double left, int vertPos, double top, double width, double height, int wrapType) {#insertImage-java.awt.image.BufferedImage-int-double-int-double-double-double-int}
```
public Shape insertImage(BufferedImage image, int horzPos, double left, int vertPos, double top, double width, double height, int wrapType)
```




**Parameters:**
| Paramètre | Type | Description |
| --- | --- | --- |
| image | java.awt.image.BufferedImage |  |
| horzPos | int |  |
| left | double |  |
| vertPos | int |  |
| top | double |  |
| largeur | double |  |
| hauteur | double |  |
| wrapType | int |  |

**Returns:**
[Shape](../../com.aspose.words/shape/)
### insertImage(InputStream stream) {#insertImage-java.io.InputStream}
```
public Shape insertImage(InputStream stream)
```




**Parameters:**
| Paramètre | Type | Description |
| --- | --- | --- |
| stream | java.io.InputStream |  |

**Returns:**
[Shape](../../com.aspose.words/shape/)
### insertImage(InputStream stream, double width, double height) {#insertImage-java.io.InputStream-double-double}
```
public Shape insertImage(InputStream stream, double width, double height)
```




**Parameters:**
| Paramètre | Type | Description |
| --- | --- | --- |
| stream | java.io.InputStream |  |
| largeur | double |  |
| hauteur | double |  |

**Returns:**
[Shape](../../com.aspose.words/shape/)
### insertImage(InputStream stream, int horzPos, double left, int vertPos, double top, double width, double height, int wrapType) {#insertImage-java.io.InputStream-int-double-int-double-double-double-int}
```
public Shape insertImage(InputStream stream, int horzPos, double left, int vertPos, double top, double width, double height, int wrapType)
```




**Parameters:**
| Paramètre | Type | Description |
| --- | --- | --- |
| stream | java.io.InputStream |  |
| horzPos | int |  |
| left | double |  |
| vertPos | int |  |
| top | double |  |
| largeur | double |  |
| hauteur | double |  |
| wrapType | int |  |

**Returns:**
[Shape](../../com.aspose.words/shape/)
### insertImage(String fileName) {#insertImage-java.lang.String}
```
public Shape insertImage(String fileName)
```


Insère une image à partir d'un fichier ou d'une URL dans le document. L'image est insérée en ligne et à 100 % d'échelle.

 **Remarks:** 

Cette surcharge téléchargera automatiquement l'image avant de l'insérer dans le document si vous spécifiez une URI distante.

Vous pouvez modifier la taille, l'emplacement, la méthode de positionnement et d'autres paramètres de l'image en utilisant l'objet [Shape](../../com.aspose.words/shape/) retourné par cette méthode.

 **Examples:** 

Montre comment insérer une image depuis le système de fichiers local dans un document.

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

Montre comment déterminer quelle image sera insérée.

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

Montre comment insérer une image gif dans le document.

```

 DocumentBuilder builder = new DocumentBuilder();

 // We can insert gif image using path or bytes array.
 // It works only if DocumentBuilder optimized to Word version 2010 or higher.
 // Note, that access to the image bytes causes conversion Gif to Png.
 Shape gifImage = builder.insertImage(getImageDir() + "Graphics Interchange Format.gif");

 gifImage = builder.insertImage(DocumentHelper.getBytesFromStream(new FileInputStream(getImageDir() + "Graphics Interchange Format.gif")));

 builder.getDocument().save(getArtifactsDir() + "InsertGif.docx");
 
```

Montre comment insérer une forme avec une image dans un document.

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

Montre comment insérer une image flottante au centre d’une page.

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

Montre comment insérer une image WebP.

```

 Document doc = new Document();
 DocumentBuilder builder = new DocumentBuilder(doc);

 builder.insertImage(getImageDir() + "WebP image.webp");

 doc.save(getArtifactsDir() + "Image.InsertWebpImage.docx");
 
```

**Parameters:**
| Paramètre | Type | Description |
| --- | --- | --- |
| fileName | java.lang.String | Le fichier contenant l'image. Peut être n'importe quel URI local ou distant valide. |

**Returns:**
[Shape](../../com.aspose.words/shape/) - The image node that was just inserted.
### insertImage(String fileName, double width, double height) {#insertImage-java.lang.String-double-double}
```
public Shape insertImage(String fileName, double width, double height)
```


Insère une image en ligne à partir d'un fichier ou d'une URL dans le document et la redimensionne à la taille spécifiée.

 **Remarks:** 

Vous pouvez modifier la taille, l'emplacement, la méthode de positionnement et d'autres paramètres de l'image en utilisant l'objet [Shape](../../com.aspose.words/shape/) retourné par cette méthode.

 **Examples:** 

Montre comment insérer une image depuis le système de fichiers local dans un document.

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
| Paramètre | Type | Description |
| --- | --- | --- |
| fileName | java.lang.String | Le fichier qui contient l'image. |
| largeur | double | La largeur de l'image en points. Peut être une valeur négative ou zéro pour demander une échelle de 100 %. |
| hauteur | double | La hauteur de l'image en points. Peut être une valeur négative ou zéro pour demander une échelle de 100 %. |

**Returns:**
[Shape](../../com.aspose.words/shape/) - The image node that was just inserted.
### insertImage(String fileName, int horzPos, double left, int vertPos, double top, double width, double height, int wrapType) {#insertImage-java.lang.String-int-double-int-double-double-double-int}
```
public Shape insertImage(String fileName, int horzPos, double left, int vertPos, double top, double width, double height, int wrapType)
```




**Parameters:**
| Paramètre | Type | Description |
| --- | --- | --- |
| fileName | java.lang.String |  |
| horzPos | int |  |
| left | double |  |
| vertPos | int |  |
| top | double |  |
| largeur | double |  |
| hauteur | double |  |
| wrapType | int |  |

**Returns:**
[Shape](../../com.aspose.words/shape/)
### insertNode(Node node) {#insertNode-com.aspose.words.Node}
```
public void insertNode(Node node)
```


Insère un nœud avant le curseur.

 **Examples:** 

Montre comment insérer une image liée dans un document.

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
| Paramètre | Type | Description |
| --- | --- | --- |
| node | [Node](../../com.aspose.words/node/) |  |

### insertOleObject(InputStream stream, String progId, boolean asIcon, InputStream presentation) {#insertOleObject-java.io.InputStream-java.lang.String-boolean-java.io.InputStream}
```
public Shape insertOleObject(InputStream stream, String progId, boolean asIcon, InputStream presentation)
```




**Parameters:**
| Paramètre | Type | Description |
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
| Paramètre | Type | Description |
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
| Paramètre | Type | Description |
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
| Paramètre | Type | Description |
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


Insère un objet OLE intégré ou lié sous forme d'icône dans le document. Permet de spécifier le fichier d'icône et la légende. Détecte le type d'objet OLE à l'aide de l'extension du fichier.

 **Examples:** 

Montre comment insérer un objet OLE dans un document.

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
| Paramètre | Type | Description |
| --- | --- | --- |
| fileName | java.lang.String | Chemin complet vers le fichier. |
| isLinked | boolean | Si  true  alors l'objet OLE lié est inséré sinon l'objet OLE intégré est inséré. |
| iconFile | java.lang.String | Chemin complet vers le fichier ICO. Si la valeur est  null , Aspose.Words utilisera une image prédéfinie. |
| iconCaption | java.lang.String | Légende de l'icône. Si la valeur est  null , Aspose.Words utilisera le nom du fichier. |

**Returns:**
[Shape](../../com.aspose.words/shape/) - Shape node containing Ole object and inserted at the current Builder position.
### insertOleObjectAsIcon(String fileName, String progId, boolean isLinked, String iconFile, String iconCaption) {#insertOleObjectAsIcon-java.lang.String-java.lang.String-boolean-java.lang.String-java.lang.String}
```
public Shape insertOleObjectAsIcon(String fileName, String progId, boolean isLinked, String iconFile, String iconCaption)
```


Insère un objet OLE intégré ou lié sous forme d'icône dans le document. Permet de spécifier le fichier d'icône et la légende. Détecte le type d'objet OLE à l'aide du paramètre progID fourni.

 **Examples:** 

Montre comment insérer un objet OLE intégré ou lié sous forme d'icône dans le document.

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
| Paramètre | Type | Description |
| --- | --- | --- |
| fileName | java.lang.String | Chemin complet vers le fichier. |
| progId | java.lang.String | ProgId de l'objet OLE. |
| isLinked | boolean | Si  true  alors l'objet OLE lié est inséré sinon l'objet OLE intégré est inséré. |
| iconFile | java.lang.String | Chemin complet vers le fichier ICO. Si la valeur est  null , Aspose.Words utilisera une image prédéfinie. |
| iconCaption | java.lang.String | Légende de l'icône. Si la valeur est  null , Aspose.Words utilisera le nom du fichier. |

**Returns:**
[Shape](../../com.aspose.words/shape/) - Shape node containing Ole object and inserted at the current Builder position.
### insertOnlineVideo(String videoUrl, double width, double height) {#insertOnlineVideo-java.lang.String-double-double}
```
public Shape insertOnlineVideo(String videoUrl, double width, double height)
```


Insère un objet vidéo en ligne dans le document et le redimensionne à la taille spécifiée.

 **Remarks:** 

Vous pouvez modifier la taille, l'emplacement, la méthode de positionnement et d'autres paramètres de l'image en utilisant l'objet [Shape](../../com.aspose.words/shape/) retourné par cette méthode.

L'insertion de vidéo en ligne à partir des ressources suivantes est prise en charge :

 *  https://www.youtube.com/
 *  https://vimeo.com/

Si votre vidéo en ligne ne s'affiche pas correctement, utilisez [insertOnlineVideo(java.lang.String, java.lang.String, byte[], double, double)](../../com.aspose.words/documentbuilder/\#insertOnlineVideo-java.lang.String--java.lang.String--byte----double--double), qui accepte du code HTML intégré personnalisé.

Le code d'intégration de la vidéo peut varier selon les fournisseurs, consultez le fournisseur correspondant de votre choix pour plus de détails.

 **Examples:** 

Montre comment insérer une vidéo en ligne dans un document en utilisant une URL.

```

 Document doc = new Document();
 DocumentBuilder builder = new DocumentBuilder(doc);

 builder.insertOnlineVideo("https://youtu.be/g1N9ke8Prmk", 360.0, 270.0);

 // We can watch the video from Microsoft Word by clicking on the shape.
 doc.save(getArtifactsDir() + "DocumentBuilder.InsertVideoWithUrl.docx");
 
```

**Parameters:**
| Paramètre | Type | Description |
| --- | --- | --- |
| videoUrl | java.lang.String | L'URL de la vidéo. |
| largeur | double | La largeur de l'image en points. Peut être une valeur négative ou zéro pour demander une échelle de 100 %. |
| hauteur | double | La hauteur de l'image en points. Peut être une valeur négative ou zéro pour demander une échelle de 100 %. |

**Returns:**
[Shape](../../com.aspose.words/shape/) - The image node that was just inserted.
### insertOnlineVideo(String videoUrl, int horzPos, double left, int vertPos, double top, double width, double height, int wrapType) {#insertOnlineVideo-java.lang.String-int-double-int-double-double-double-int}
```
public Shape insertOnlineVideo(String videoUrl, int horzPos, double left, int vertPos, double top, double width, double height, int wrapType)
```




**Parameters:**
| Paramètre | Type | Description |
| --- | --- | --- |
| videoUrl | java.lang.String |  |
| horzPos | int |  |
| left | double |  |
| vertPos | int |  |
| top | double |  |
| largeur | double |  |
| hauteur | double |  |
| wrapType | int |  |

**Returns:**
[Shape](../../com.aspose.words/shape/)
### insertOnlineVideo(String videoUrl, String videoEmbedCode, byte[] thumbnailImageBytes, double width, double height) {#insertOnlineVideo-java.lang.String-java.lang.String-byte---double-double}
```
public Shape insertOnlineVideo(String videoUrl, String videoEmbedCode, byte[] thumbnailImageBytes, double width, double height)
```


Insère un objet vidéo en ligne dans le document et le redimensionne à la taille spécifiée.

 **Remarks:** 

Vous pouvez modifier la taille, l'emplacement, la méthode de positionnement et d'autres paramètres de l'image en utilisant l'objet [Shape](../../com.aspose.words/shape/) retourné par cette méthode.

 **Examples:** 

Montre comment insérer une vidéo en ligne dans un document avec une miniature personnalisée.

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
| Paramètre | Type | Description |
| --- | --- | --- |
| videoUrl | java.lang.String | L'URL de la vidéo. |
| videoEmbedCode | java.lang.String | Le code d'intégration de la vidéo. |
| thumbnailImageBytes | byte[] | Les octets de l'image miniature. |
| largeur | double | La largeur de l'image en points. Peut être une valeur négative ou zéro pour demander une échelle de 100 %. |
| hauteur | double | La hauteur de l'image en points. Peut être une valeur négative ou zéro pour demander une échelle de 100 %. |

**Returns:**
[Shape](../../com.aspose.words/shape/) - The image node that was just inserted.
### insertOnlineVideo(String videoUrl, String videoEmbedCode, byte[] thumbnailImageBytes, int horzPos, double left, int vertPos, double top, double width, double height, int wrapType) {#insertOnlineVideo-java.lang.String-java.lang.String-byte---int-double-int-double-double-double-int}
```
public Shape insertOnlineVideo(String videoUrl, String videoEmbedCode, byte[] thumbnailImageBytes, int horzPos, double left, int vertPos, double top, double width, double height, int wrapType)
```




**Parameters:**
| Paramètre | Type | Description |
| --- | --- | --- |
| videoUrl | java.lang.String |  |
| videoEmbedCode | java.lang.String |  |
| thumbnailImageBytes | byte[] |  |
| horzPos | int |  |
| left | double |  |
| vertPos | int |  |
| top | double |  |
| largeur | double |  |
| hauteur | double |  |
| wrapType | int |  |

**Returns:**
[Shape](../../com.aspose.words/shape/)
### insertParagraph() {#insertParagraph}
```
public Paragraph insertParagraph()
```


Insère un saut de paragraphe dans le document.

 **Remarks:** 

Le formatage du paragraphe actuel spécifié par la propriété [getParagraphFormat()](../../com.aspose.words/documentbuilder/\#getParagraphFormat) est utilisé.

Divise le paragraphe actuel en deux. Après l'insertion du paragraphe, le curseur est placé au début du nouveau paragraphe.

Une exception est levée s'il n'est pas possible d'insérer un saut de paragraphe à la position actuelle du curseur.

 **Examples:** 

Montre comment insérer un paragraphe dans le document.

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
| Paramètre | Type | Description |
| --- | --- | --- |
| shapeType | int |  |
| largeur | double |  |
| hauteur | double |  |

**Returns:**
[Shape](../../com.aspose.words/shape/)
### insertShape(int shapeType, int horzPos, double left, int vertPos, double top, double width, double height, int wrapType) {#insertShape-int-int-double-int-double-double-double-int}
```
public Shape insertShape(int shapeType, int horzPos, double left, int vertPos, double top, double width, double height, int wrapType)
```




**Parameters:**
| Paramètre | Type | Description |
| --- | --- | --- |
| shapeType | int |  |
| horzPos | int |  |
| left | double |  |
| vertPos | int |  |
| top | double |  |
| largeur | double |  |
| hauteur | double |  |
| wrapType | int |  |

**Returns:**
[Shape](../../com.aspose.words/shape/)
### insertSignatureLine(SignatureLineOptions signatureLineOptions) {#insertSignatureLine-com.aspose.words.SignatureLineOptions}
```
public Shape insertSignatureLine(SignatureLineOptions signatureLineOptions)
```


Insère une ligne de signature à la position actuelle.

 **Examples:** 

Montre comment signer un document avec un certificat personnel et une ligne de signature.

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
| Paramètre | Type | Description |
| --- | --- | --- |
| signatureLineOptions | [SignatureLineOptions](../../com.aspose.words/signaturelineoptions/) | L'objet qui stocke les paramètres de création de la ligne de signature. |

**Returns:**
[Shape](../../com.aspose.words/shape/) - The signature line node that was just inserted.
### insertSignatureLine(SignatureLineOptions signatureLineOptions, int horzPos, double left, int vertPos, double top, int wrapType) {#insertSignatureLine-com.aspose.words.SignatureLineOptions-int-double-int-double-int}
```
public Shape insertSignatureLine(SignatureLineOptions signatureLineOptions, int horzPos, double left, int vertPos, double top, int wrapType)
```




**Parameters:**
| Paramètre | Type | Description |
| --- | --- | --- |
| signatureLineOptions | [SignatureLineOptions](../../com.aspose.words/signaturelineoptions/) |  |
| horzPos | int |  |
| left | double |  |
| vertPos | int |  |
| top | double |  |
| wrapType | int |  |

**Returns:**
[Shape](../../com.aspose.words/shape/)
### insertStructuredDocumentTag(int type) {#insertStructuredDocumentTag-int}
```
public StructuredDocumentTag insertStructuredDocumentTag(int type)
```




**Parameters:**
| Paramètre | Type | Description |
| --- | --- | --- |
| type | int |  |

**Returns:**
[StructuredDocumentTag](../../com.aspose.words/structureddocumenttag/)
### insertStyleSeparator() {#insertStyleSeparator}
```
public void insertStyleSeparator()
```


Insère un séparateur de style dans le document.

 **Remarks:** 

Cette méthode permet d'appliquer différents styles de paragraphe à deux parties différentes d'une ligne de texte.

 **Examples:** 

Montre comment travailler avec les séparateurs de style.

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


Insère un champ TOC (table des matières) dans le document.

 **Remarks:** 

Cette méthode insère un champ TOC (table des matières) dans le document à la position actuelle.

Une table des matières dans un document Word peut être construite de plusieurs manières et formatée à l'aide de diverses options. La façon dont la table est construite et affichée par Microsoft Word est contrôlée par les commutateurs de champ.

Le moyen le plus simple de spécifier les commutateurs consiste à insérer et configurer une table des matières dans un document Word en utilisant le menu Insertion->Référence->Index et tables, puis activer l'affichage des codes de champ pour voir les commutateurs. Vous pouvez appuyer sur Alt+F9 dans Microsoft Word pour activer ou désactiver l'affichage des codes de champ.

Par exemple, après avoir créé une table des matières, le champ suivant est inséré dans le document : **\{ TOC \\o \"1-3\" \\h \\z \}**. Vous pouvez copier **\\o \"1-3\" \\h \\z** et l'utiliser comme paramètre des commutateurs.

Notez que [insertTableOfContents(java.lang.String)](../../com.aspose.words/documentbuilder/\#insertTableOfContents-java.lang.String) n'insérera qu'un champ TOC, mais ne construira pas réellement la table des matières. La table des matières est construite par Microsoft Word lorsque le champ est mis à jour.

Si vous insérez une table des matières en utilisant cette méthode puis ouvrez le fichier dans Microsoft Word, vous ne verrez pas la table des matières car le champ TOC n'a pas encore été mis à jour.

Dans Microsoft Word, les champs ne sont pas automatiquement mis à jour lorsqu'un document est ouvert, mais vous pouvez mettre à jour les champs d'un document à tout moment en appuyant sur F9.

 **Examples:** 

Montre comment insérer une table des matières (TOC) dans un document en utilisant les styles de titres comme entrées.

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
| Paramètre | Type | Description |
| --- | --- | --- |
| commutateurs | java.lang.String | Les commutateurs du champ TOC. |

**Returns:**
[Field](../../com.aspose.words/field/)
### insertTextInput(String name, int type, String format, String fieldValue, int maxLength) {#insertTextInput-java.lang.String-int-java.lang.String-java.lang.String-int}
```
public FormField insertTextInput(String name, int type, String format, String fieldValue, int maxLength)
```




**Parameters:**
| Paramètre | Type | Description |
| --- | --- | --- |
| nom | java.lang.String |  |
| type | int |  |
| format | java.lang.String |  |
| fieldValue | java.lang.String |  |
| maxLength | int |  |

**Returns:**
[FormField](../../com.aspose.words/formfield/)
### isAtEndOfParagraph() {#isAtEndOfParagraph}
```
public boolean isAtEndOfParagraph()
```


Renvoie  true  si le curseur est à la fin du paragraphe actuel.

 **Examples:** 

Montre comment déplacer le curseur d'un DocumentBuilder vers différents nœuds dans un document.

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
booléen -  true  si le curseur est à la fin du paragraphe actuel.
### isAtEndOfStructuredDocumentTag() {#isAtEndOfStructuredDocumentTag}
```
public boolean isAtEndOfStructuredDocumentTag()
```


Renvoie **true** si le curseur est à la fin d’une balise de document structuré.

 **Examples:** 

Montre comment déplacer le curseur du DocumentBuilder à l'intérieur d'une balise de document structuré.

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
booléen - **true** si le curseur se trouve à la fin d'une balise de document structuré.
### isAtStartOfParagraph() {#isAtStartOfParagraph}
```
public boolean isAtStartOfParagraph()
```


Renvoie  true  si le curseur est au début du paragraphe actuel (aucun texte avant le curseur).

 **Examples:** 

Montre comment déplacer le curseur d'un DocumentBuilder vers différents nœuds dans un document.

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
booléen -  true  si le curseur est au début du paragraphe actuel (aucun texte avant le curseur).
### moveTo(Node node) {#moveTo-com.aspose.words.Node}
```
public void moveTo(Node node)
```


Déplace le curseur vers un nœud en ligne ou vers la fin d’un paragraphe.

 **Remarks:** 

Lorsque *node* est un nœud de niveau en ligne, le curseur est déplacé vers ce nœud et le contenu supplémentaire sera inséré avant ce nœud.

Lorsque *node* est un [Paragraph](../../com.aspose.words/paragraph/), le curseur est déplacé à la fin du paragraphe et le contenu supplémentaire sera inséré juste avant le saut de paragraphe.

Lorsque *node* est un nœud de niveau bloc mais pas un [Paragraph](../../com.aspose.words/paragraph/), le curseur est déplacé à la fin du premier paragraphe du nœud de niveau bloc et le contenu supplémentaire sera inséré juste avant le saut de paragraphe.

 **Examples:** 

Montre comment déplacer le curseur d'un DocumentBuilder vers différents nœuds dans un document.

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

Montre comment déplacer la position du curseur d'un DocumentBuilder vers un nœud spécifié.

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
| Paramètre | Type | Description |
| --- | --- | --- |
| node | [Node](../../com.aspose.words/node/) | Le nœud doit être un paragraphe ou un enfant direct d'un paragraphe. |

### moveToBookmark(String bookmarkName) {#moveToBookmark-java.lang.String}
```
public boolean moveToBookmark(String bookmarkName)
```


Déplace le curseur vers un signet.

 **Remarks:** 

Déplace le curseur à une position juste après le début du signet portant le nom spécifié.

La comparaison n'est pas sensible à la casse. Si le signet n'est pas trouvé,  false  est renvoyé et le curseur n'est pas déplacé.

L'insertion de nouveau texte ne remplace pas le texte existant du signet.

Notez que certains signets du document sont assignés à des champs de formulaire. Se déplacer vers un tel signet et y insérer du texte insère le texte dans le code du champ de formulaire. Bien que cela n'invalide pas le champ de formulaire, le texte inséré ne sera pas visible car il devient partie du code du champ.

 **Examples:** 

Montre comment déplacer le curseur d'un DocumentBuilder vers différents nœuds dans un document.

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
| Paramètre | Type | Description |
| --- | --- | --- |
| bookmarkName | java.lang.String | Le nom du signet vers lequel déplacer le curseur. |

**Returns:**
booléen -  true  si le signet a été trouvé ;  false  sinon.
### moveToBookmark(String bookmarkName, boolean isStart, boolean isAfter) {#moveToBookmark-java.lang.String-boolean-boolean}
```
public boolean moveToBookmark(String bookmarkName, boolean isStart, boolean isAfter)
```


Déplace le curseur vers un signet avec une plus grande précision.

 **Remarks:** 

Déplace le curseur à une position avant ou après le début ou la fin du signet.

Si la position souhaitée n'est pas au niveau en ligne, déplace au paragraphe suivant.

La comparaison n'est pas sensible à la casse. Si le signet n'est pas trouvé,  false  est renvoyé et le curseur n'est pas déplacé.

 **Examples:** 

Montre comment déplacer le curseur du point d'insertion de nœud d'un document builder vers un signet.

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
| Paramètre | Type | Description |
| --- | --- | --- |
| bookmarkName | java.lang.String | Le nom du signet vers lequel déplacer le curseur. |
| isStart | boolean | Lorsque  true , le curseur est déplacé au début du signet. Lorsque  false , le curseur est déplacé à la fin du signet. |
| isAfter | boolean | Lorsque  true , le curseur est placé après la position de début ou de fin du signet. Lorsque  false , le curseur est placé avant la position de début ou de fin du signet. |

**Returns:**
booléen -  true  si le signet a été trouvé ;  false  sinon.
### moveToCell(int tableIndex, int rowIndex, int columnIndex, int characterIndex) {#moveToCell-int-int-int-int}
```
public void moveToCell(int tableIndex, int rowIndex, int columnIndex, int characterIndex)
```


Déplace le curseur vers une cellule de tableau dans la section actuelle.

 **Remarks:** 

La navigation est effectuée à l'intérieur de l'histoire actuelle de la section actuelle.

Pour les paramètres d'index, lorsque l'index est supérieur ou égal à 0, il indique un index depuis le début avec 0 étant le premier élément. Lorsque l'index est inférieur à 0, il indique un index depuis la fin avec -1 étant le dernier élément.

 **Examples:** 

Montre comment déplacer le curseur d'un document builder vers une cellule d'un tableau.

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
| Paramètre | Type | Description |
| --- | --- | --- |
| tableIndex | int | L'index du tableau vers lequel se déplacer. |
| rowIndex | int | L'index de la ligne dans le tableau. |
| columnIndex | int | L'index de la colonne dans le tableau. |
| characterIndex | int | L'index du caractère à l'intérieur de la cellule. Une valeur négative vous permet de spécifier une position depuis la fin de la cellule. Utilisez -1 pour vous déplacer à la fin de la cellule. |

### moveToDocumentEnd() {#moveToDocumentEnd}
```
public void moveToDocumentEnd()
```


Déplace le curseur vers la fin du document.

 **Examples:** 

Montre comment déplacer le curseur d'un DocumentBuilder vers différents nœuds dans un document.

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


Déplace le curseur vers le début du document.

 **Examples:** 

Montre comment déplacer le curseur d'un DocumentBuilder vers différents nœuds dans un document.

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


Déplace le curseur vers un champ dans le document.

 **Examples:** 

Montre comment déplacer le curseur du point d'insertion du nœud d'un document builder vers un champ spécifique.

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
| Paramètre | Type | Description |
| --- | --- | --- |
| field | [Field](../../com.aspose.words/field/) | Le champ vers lequel déplacer le curseur. |
| isAfter | boolean | Lorsque  true , le curseur est déplacé pour être après la fin du champ. Lorsque  false , le curseur est déplacé pour être avant le début du champ. |

### moveToHeaderFooter(int headerFooterType) {#moveToHeaderFooter-int}
```
public void moveToHeaderFooter(int headerFooterType)
```




**Parameters:**
| Paramètre | Type | Description |
| --- | --- | --- |
| headerFooterType | int |  |

### moveToMergeField(String fieldName) {#moveToMergeField-java.lang.String}
```
public boolean moveToMergeField(String fieldName)
```


Déplace le curseur vers le champ de fusion spécifié.  Déplace le curseur à une position juste après le champ de fusion spécifié et supprime le champ de fusion.

 **Remarks:** 

Notez que cette méthode supprime le champ de fusion du document après avoir déplacé le curseur.

 **Examples:** 

Montre comment remplir les MERGEFIELDs avec des données à l'aide d'un DocumentBuilder au lieu d'une fusion de courrier.

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

Montre comment insérer des champs de formulaire à case à cocher dans un document lors de la fusion de courrier.

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
| Paramètre | Type | Description |
| --- | --- | --- |
| fieldName | java.lang.String | Le nom du champ de fusion de courrier, insensible à la casse. |

**Returns:**
booléen -  true  si le champ de fusion a été trouvé et que le curseur a été déplacé ;  false  sinon.
### moveToMergeField(String fieldName, boolean isAfter, boolean isDeleteField) {#moveToMergeField-java.lang.String-boolean-boolean}
```
public boolean moveToMergeField(String fieldName, boolean isAfter, boolean isDeleteField)
```


Déplace le champ de fusion vers le champ de fusion spécifié.

 **Examples:** 

Montre comment insérer des champs et déplacer le curseur du DocumentBuilder vers eux.

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
| Paramètre | Type | Description |
| --- | --- | --- |
| fieldName | java.lang.String | Le nom du champ de fusion de courrier, insensible à la casse. |
| isAfter | boolean | Lorsque  true , le curseur est déplacé pour être après la fin du champ. Lorsque  false , le curseur est déplacé pour être avant le début du champ. |
| isDeleteField | boolean | Lorsque  true , supprime le champ de fusion. |

**Returns:**
booléen -  true  si le champ de fusion a été trouvé et que le curseur a été déplacé ;  false  sinon.
### moveToParagraph(int paragraphIndex, int characterIndex) {#moveToParagraph-int-int}
```
public void moveToParagraph(int paragraphIndex, int characterIndex)
```


Déplace le curseur vers un paragraphe dans la section actuelle.

 **Remarks:** 

La navigation est effectuée à l'intérieur de l'histoire courante de la section actuelle. C'est-à-dire, si vous avez déplacé le curseur vers l'en-tête principal de la première section, alors  paragraphIndex  spécifie l'index du paragraphe à l'intérieur de cet en-tête de cette section.

Lorsque  paragraphIndex  est supérieur ou égal à 0, il spécifie un index depuis le début de la section avec 0 étant le premier paragraphe. Lorsque  paragraphIndex  est inférieur à 0, il spécifie un index depuis la fin de la section avec -1 étant le dernier paragraphe.

 **Examples:** 

Montre comment déplacer la position du curseur d'un builder vers un paragraphe spécifié.

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
| Paramètre | Type | Description |
| --- | --- | --- |
| paragraphIndex | int | L'index du paragraphe vers lequel se déplacer. |
| characterIndex | int | L'index du caractère à l'intérieur du paragraphe. Une valeur négative vous permet de spécifier une position depuis la fin du paragraphe. Utilisez -1 pour vous déplacer à la fin du paragraphe. |

### moveToSection(int sectionIndex) {#moveToSection-int}
```
public void moveToSection(int sectionIndex)
```


Déplace le curseur vers le début du corps dans une section spécifiée.

 **Remarks:** 

Lorsque  sectionIndex  est supérieur ou égal à 0, il spécifie un index depuis le début du document avec 0 étant la première section. Lorsque  sectionIndex  est inférieur à 0, il spécifie un index depuis la fin du document avec -1 étant la dernière section.

Le curseur est déplacé vers le premier paragraphe du [Body](../../com.aspose.words/body/) de la section spécifiée.

 **Examples:** 

Montre comment créer des en-têtes et pieds de page dans un document en utilisant DocumentBuilder.

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
| Paramètre | Type | Description |
| --- | --- | --- |
| sectionIndex | int | L'index de la section vers laquelle se déplacer. |

### moveToStructuredDocumentTag(StructuredDocumentTag structuredDocumentTag, int characterIndex) {#moveToStructuredDocumentTag-com.aspose.words.StructuredDocumentTag-int}
```
public void moveToStructuredDocumentTag(StructuredDocumentTag structuredDocumentTag, int characterIndex)
```


Déplace le curseur vers la balise de document structuré.

 **Examples:** 

Montre comment déplacer le curseur du DocumentBuilder à l'intérieur d'une balise de document structuré.

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
| Paramètre | Type | Description |
| --- | --- | --- |
| structuredDocumentTag | [StructuredDocumentTag](../../com.aspose.words/structureddocumenttag/) | Le tag de document structuré vers lequel se déplacer. |
| characterIndex | int | L'index du caractère à l'intérieur du tag de document structuré. Une valeur négative vous permet de spécifier une position depuis la fin du tag de document structuré. Utilisez -1 pour vous déplacer à la fin du tag de document structuré. Si le tag de document structuré est au niveau du bloc, et que vous souhaitez déplacer le curseur à la fin de son dernier paragraphe, spécifiez -2. |

### moveToStructuredDocumentTag(int structuredDocumentTagIndex, int characterIndex) {#moveToStructuredDocumentTag-int-int}
```
public void moveToStructuredDocumentTag(int structuredDocumentTagIndex, int characterIndex)
```


Déplace le curseur vers une balise de document structuré dans la section actuelle.

 **Remarks:** 

La navigation est effectuée à l'intérieur de l'histoire courante de la section actuelle. C'est-à-dire, si vous avez déplacé le curseur vers l'en-tête principal de la première section, alors  structuredDocumentTagIndex  spécifie l'index du tag de document structuré à l'intérieur de cet en-tête de cette section.

Lorsque  structuredDocumentTagIndex  est supérieur ou égal à 0, il spécifie un index depuis le début de la section avec 0 étant le premier tag de document structuré. Lorsque  structuredDocumentTagIndex  est inférieur à 0, il spécifie un index depuis la fin de la section avec -1 étant le dernier tag de document structuré.

 **Examples:** 

Montre comment déplacer le curseur du DocumentBuilder à l'intérieur d'une balise de document structuré.

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
| Paramètre | Type | Description |
| --- | --- | --- |
| structuredDocumentTagIndex | int | L'index du tag de document structuré vers lequel se déplacer. |
| characterIndex | int | L'index du caractère à l'intérieur du tag de document structuré. Une valeur négative vous permet de spécifier une position depuis la fin du tag de document structuré. Utilisez -1 pour vous déplacer à la fin du tag de document structuré. Si le tag de document structuré est au niveau du bloc, et que vous souhaitez déplacer le curseur à la fin de son dernier paragraphe, spécifiez -2. |

### popFont() {#popFont}
```
public void popFont()
```


Récupère le formatage de caractères précédemment enregistré sur la pile.

 **Examples:** 

Montre comment utiliser la pile de formatage d'un DocumentBuilder.

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


Enregistre le formatage de caractères actuel sur la pile.

 **Examples:** 

Montre comment utiliser la pile de formatage d'un DocumentBuilder.

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
| Paramètre | Type | Description |
| --- | --- | --- |
| key | int |  |

### removeRunAttr(int key) {#removeRunAttr-int}
```
public void removeRunAttr(int key)
```




**Parameters:**
| Paramètre | Type | Description |
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


Vrai si la police est formatée en gras.

 **Examples:** 

Montre comment remplir les MERGEFIELDs avec des données à l'aide d'un DocumentBuilder au lieu d'une fusion de courrier.

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
| Paramètre | Type | Description |
| --- | --- | --- |
| valeur | boolean | La valeur  boolean  correspondante. |

### setCellAttr(int key, Object value) {#setCellAttr-int-java.lang.Object}
```
public void setCellAttr(int key, Object value)
```




**Parameters:**
| Paramètre | Type | Description |
| --- | --- | --- |
| key | int |  |
| valeur | java.lang.Object |  |

### setDocument(Document value) {#setDocument-com.aspose.words.Document}
```
public void setDocument(Document value)
```


Définit l’objet [getDocument()](../../com.aspose.words/documentbuilder/\#getDocument) / [setDocument(com.aspose.words.Document)](../../com.aspose.words/documentbuilder/\#setDocument-com.aspose.words.Document) auquel cet objet est attaché.

 **Examples:** 

Montre comment appliquer et rétablir les paramètres de mise en page aux sections d'un document.

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
| Paramètre | Type | Description |
| --- | --- | --- |
| value | [Document](../../com.aspose.words/document/) | L'objet [getDocument()](../../com.aspose.words/documentbuilder/\#getDocument) / [setDocument(com.aspose.words.Document)](../../com.aspose.words/documentbuilder/\#setDocument-com.aspose.words.Document) auquel cet objet est attaché. |

### setItalic(boolean value) {#setItalic-boolean}
```
public void setItalic(boolean value)
```


Vrai si la police est formatée en italique.

 **Examples:** 

Montre comment remplir les MERGEFIELDs avec des données à l'aide d'un DocumentBuilder au lieu d'une fusion de courrier.

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
| Paramètre | Type | Description |
| --- | --- | --- |
| valeur | boolean | La valeur  boolean  correspondante. |

### setParaAttr(int key, Object value) {#setParaAttr-int-java.lang.Object}
```
public void setParaAttr(int key, Object value)
```




**Parameters:**
| Paramètre | Type | Description |
| --- | --- | --- |
| key | int |  |
| valeur | java.lang.Object |  |

### setRowAttr(int key, Object value) {#setRowAttr-int-java.lang.Object}
```
public void setRowAttr(int key, Object value)
```




**Parameters:**
| Paramètre | Type | Description |
| --- | --- | --- |
| key | int |  |
| valeur | java.lang.Object |  |

### setRunAttr(int fontAttr, Object value) {#setRunAttr-int-java.lang.Object}
```
public void setRunAttr(int fontAttr, Object value)
```




**Parameters:**
| Paramètre | Type | Description |
| --- | --- | --- |
| fontAttr | int |  |
| valeur | java.lang.Object |  |

### setUnderline(int value) {#setUnderline-int}
```
public void setUnderline(int value)
```


Obtient/définit le type de soulignement pour la police actuelle.

 **Examples:** 

Montre comment formater le texte inséré par un DocumentBuilder.

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
| Paramètre | Type | Description |
| --- | --- | --- |
| value | int | La valeur int correspondante. La valeur doit être l'une des constantes [Underline](../../com.aspose.words/underline/). |

### startBookmark(String bookmarkName) {#startBookmark-java.lang.String}
```
public BookmarkStart startBookmark(String bookmarkName)
```


Marque la position actuelle dans le document comme le début d’un signet.

 **Remarks:** 

Les signets dans un document peuvent se chevaucher et couvrir n'importe quelle plage. Pour créer un signet valide, vous devez appeler à la fois [startBookmark(java.lang.String)](../../com.aspose.words/documentbuilder/\#startBookmark-java.lang.String) et [endBookmark(java.lang.String)](../../com.aspose.words/documentbuilder/\#endBookmark-java.lang.String) avec le même  bookmarkName  parameter.

Les signets mal formés ou les signets avec des noms en double seront ignorés lors de l'enregistrement du document.

 **Examples:** 

Montre comment créer un signet.

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

Montre comment insérer un hyperlien qui référence un signet local.

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
| Paramètre | Type | Description |
| --- | --- | --- |
| bookmarkName | java.lang.String | Nom du signet. |

**Returns:**
[BookmarkStart](../../com.aspose.words/bookmarkstart/) - The bookmark start node that was just created.
### startColumnBookmark(String bookmarkName) {#startColumnBookmark-java.lang.String}
```
public BookmarkStart startColumnBookmark(String bookmarkName)
```


Marque la position actuelle dans le document comme le début d'un signet de colonne. La position doit être dans une cellule de tableau.

 **Remarks:** 

Un signet de colonne couvre une ou plusieurs colonnes dans une plage de lignes. Pour créer un signet valide, vous devez appeler à la fois [startColumnBookmark(java.lang.String)](../../com.aspose.words/documentbuilder/\#startColumnBookmark-java.lang.String) et [endColumnBookmark(java.lang.String)](../../com.aspose.words/documentbuilder/\#endColumnBookmark-java.lang.String) avec le même  bookmarkName  paramètre.

Les signets mal formés ou les signets avec des noms en double seront ignorés lors de l'enregistrement du document.

La position réelle du nœud [BookmarkStart](../../com.aspose.words/bookmarkstart/) inséré peut différer de la position actuelle du constructeur de document.

 **Examples:** 

Montre comment créer un signet de colonne.

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
| Paramètre | Type | Description |
| --- | --- | --- |
| bookmarkName | java.lang.String | Nom du signet. |

**Returns:**
[BookmarkStart](../../com.aspose.words/bookmarkstart/) - The bookmark start node that was just created.
### startEditableRange() {#startEditableRange}
```
public EditableRangeStart startEditableRange()
```


Marque la position actuelle dans le document comme le début d'une plage modifiable.

 **Remarks:** 

Une plage modifiable dans un document peut se chevaucher et couvrir n'importe quelle plage. Pour créer une plage modifiable valide, vous devez appeler les méthodes [startEditableRange()](../../com.aspose.words/documentbuilder/\#startEditableRange) et [endEditableRange()](../../com.aspose.words/documentbuilder/\#endEditableRange) ou [endEditableRange(com.aspose.words.EditableRangeStart)](../../com.aspose.words/documentbuilder/\#endEditableRange-com.aspose.words.EditableRangeStart).

Une plage modifiable mal formée sera ignorée lors de l'enregistrement du document.

 **Examples:** 

Montre comment travailler avec une plage éditable.

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

Montre comment créer des plages éditables imbriquées.

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


Démarre un tableau dans le document.

 **Remarks:** 

La prochaine méthode à appeler est [insertCell()](../../com.aspose.words/documentbuilder/\#insertCell).

Cette méthode démarre un tableau imbriqué lorsqu'elle est appelée à l'intérieur d'une cellule.

 **Examples:** 

Montre comment créer un tableau avec des bordures personnalisées.

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

Montre comment créer un tableau 2x2 formaté.

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

Montre comment formater les cellules avec un DocumentBuilder.

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


Insère une chaîne dans le document à la position d'insertion actuelle.

 **Remarks:** 

Le formatage de police actuel spécifié par la propriété [getFont()](../../com.aspose.words/documentbuilder/\#getFont) est utilisé.

 **Examples:** 

Montre comment insérer une chaîne entourée d'une bordure dans un document.

```

 Document doc = new Document();
 DocumentBuilder builder = new DocumentBuilder(doc);

 builder.getFont().getBorder().setColor(Color.GREEN);
 builder.getFont().getBorder().setLineWidth(2.5);
 builder.getFont().getBorder().setLineStyle(LineStyle.DASH_DOT_STROKER);

 builder.write("Text surrounded by green border.");

 doc.save(getArtifactsDir() + "Border.FontBorder.docx");
 
```

Montre comment créer un tableau avec des bordures personnalisées.

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

Montre comment utiliser un document builder pour créer un tableau.

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

Montre comment créer un tableau 2x2 formaté.

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
| Paramètre | Type | Description |
| --- | --- | --- |
| text | java.lang.String | La chaîne à insérer dans le document. |

### writeln() {#writeln}
```
public void writeln()
```


Insère un saut de paragraphe dans le document.

 **Remarks:** 

Appelle [insertParagraph()](../../com.aspose.words/documentbuilder/\#insertParagraph).

 **Examples:** 

Montre comment créer des en-têtes et pieds de page dans un document en utilisant DocumentBuilder.

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


Insère une chaîne et un saut de paragraphe dans le document.

 **Remarks:** 

Le formatage actuel de la police et du paragraphe spécifié par les propriétés [getFont()](../../com.aspose.words/documentbuilder/\#getFont) et [getParagraphFormat()](../../com.aspose.words/documentbuilder/\#getParagraphFormat) est utilisé.

 **Examples:** 

Montre comment créer un tableau 2x2 formaté.

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
| Paramètre | Type | Description |
| --- | --- | --- |
| text | java.lang.String | La chaîne à insérer dans le document. |

