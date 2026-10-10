---
title: "DocumentVisitor"
linktitle: "DocumentVisitor"
second_title: "Aspose.Words für Java"
description: "Basisklasse für benutzerdefinierte Dokumentbesucher in Java."
type: docs
weight: 175
url: /de/java/com.aspose.words/documentvisitor/
---

**Inheritance:**
java.lang.Object
```
public abstract class DocumentVisitor
```

Basisklasse für benutzerdefinierte Dokumentbesucher.

Um mehr zu erfahren, besuchen Sie den [ Aspose.Words Document Object Model (DOM) ][Aspose.Words Document Object Model _DOM_] Dokumentationsartikel.

 **Remarks:** 

Mit [DocumentVisitor](../../com.aspose.words/documentvisitor/) können Sie benutzerdefinierte Vorgänge definieren und ausführen, die eine Aufzählung des Dokumentbaums erfordern.

Zum Beispiel verwendet Aspose.Words intern [DocumentVisitor](../../com.aspose.words/documentvisitor/) zum Speichern von [Document](../../com.aspose.words/document/) in verschiedenen Formaten und für andere Vorgänge wie das Suchen von Feldern oder Lesezeichen in einem Dokumentfragment.

So verwenden Sie [DocumentVisitor](../../com.aspose.words/documentvisitor/):

1.  Erstellen Sie eine Klasse, die von [DocumentVisitor](../../com.aspose.words/documentvisitor/) abgeleitet ist.
2.  Überschreiben Sie und implementieren Sie einige oder alle VisitXXX‑Methoden, um benutzerdefinierte Vorgänge auszuführen.
3.  Rufen Sie [Node.accept(com.aspose.words.DocumentVisitor)](../../com.aspose.words/node/\\#accept-com.aspose.words.DocumentVisitor) auf dem [Node](../../com.aspose.words/node/) auf, von dem aus Sie die Aufzählung starten möchten.

[DocumentVisitor](../../com.aspose.words/documentvisitor/) provides default implementations for all of the VisitXXX methods to make it easier to create new document visitors as only the methods required for the particular visitor need to be overridden. It is not necessary to override all of the visitor methods.

Weitere Informationen finden Sie im Visitor‑Entwurfsmuster.

 **Examples:** 

Zeigt, wie ein DocumentVisitor verwendet wird, um die Knotenstruktur eines Dokuments auszugeben.

```

 public void docStructureToText() throws Exception {
     Document doc = new Document(getMyDir() + "DocumentVisitor-compatible features.docx");
     DocStructurePrinter visitor = new DocStructurePrinter();

     // When we get a composite node to accept a document visitor, the visitor visits the accepting node,
     // and then traverses all the node's children in a depth-first manner.
     // The visitor can read and modify each visited node.
     doc.accept(visitor);

     System.out.println(visitor.getText());
 }

 /// 
 /// Traverses a node's tree of child nodes.
 /// Creates a map of this tree in the form of a string.
 /// 
 public static class DocStructurePrinter extends DocumentVisitor {
     public DocStructurePrinter() {
         mAcceptingNodeChildTree = new StringBuilder();
     }

     public String getText() {
         return mAcceptingNodeChildTree.toString();
     }

     /// 
     /// Called when a Document node is encountered.
     /// 
     public int visitDocumentStart(Document doc) {
         int childNodeCount = doc.getChildNodes(NodeType.ANY, true).getCount();

         indentAndAppendLine("[Document start] Child nodes: " + childNodeCount);
         mDocTraversalDepth++;

         // Allow the visitor to continue visiting other nodes.
         return VisitorAction.CONTINUE;
     }

     /// 
     /// Called after all the child nodes of a Document node have been visited.
     /// 
     public int visitDocumentEnd(Document doc) {
         mDocTraversalDepth--;
         indentAndAppendLine("[Document end]");

         return VisitorAction.CONTINUE;
     }

     /// 
     /// Called when a Section node is encountered in the document.
     /// 
     public int visitSectionStart(final Section section) {
         // Get the index of our section within the document
         NodeCollection docSections = section.getDocument().getChildNodes(NodeType.SECTION, false);
         int sectionIndex = docSections.indexOf(section);

         indentAndAppendLine("[Section start] Section index: " + sectionIndex);
         mDocTraversalDepth++;

         return VisitorAction.CONTINUE;
     }

     /// 
     /// Called after all the child nodes of a Section node have been visited.
     /// 
     public int visitSectionEnd(final Section section) {
         mDocTraversalDepth--;
         indentAndAppendLine("[Section end]");

         return VisitorAction.CONTINUE;
     }

     /// 
     /// Called when a Body node is encountered in the document.
     /// 
     public int visitBodyStart(final Body body) {
         int paragraphCount = body.getParagraphs().getCount();
         indentAndAppendLine("[Body start] Paragraphs: " + paragraphCount);
         mDocTraversalDepth++;

         return VisitorAction.CONTINUE;
     }

     /// 
     /// Called after all the child nodes of a Body node have been visited.
     /// 
     public int visitBodyEnd(final Body body) {
         mDocTraversalDepth--;
         indentAndAppendLine("[Body end]");

         return VisitorAction.CONTINUE;
     }

     /// 
     /// Called when a Paragraph node is encountered in the document.
     /// 
     public int visitParagraphStart(final Paragraph paragraph) {
         indentAndAppendLine("[Paragraph start]");
         mDocTraversalDepth++;

         return VisitorAction.CONTINUE;
     }

     /// 
     /// Called after all the child nodes of a Paragraph node have been visited.
     /// 
     public int visitParagraphEnd(final Paragraph paragraph) {
         mDocTraversalDepth--;
         indentAndAppendLine("[Paragraph end]");

         return VisitorAction.CONTINUE;
     }

     /// 
     /// Called when a Run node is encountered in the document.
     /// 
     public int visitRun(final Run run) {
         indentAndAppendLine("[Run] \"" + run.getText() + "\"");

         return VisitorAction.CONTINUE;
     }

     /// 
     /// Called when a SubDocument node is encountered in the document.
     /// 
     public int visitSubDocument(final SubDocument subDocument) {
         indentAndAppendLine("[SubDocument]");

         return VisitorAction.CONTINUE;
     }

     /// 
     /// Called when a SubDocument node is encountered in the document.
     /// 
     public int visitStructuredDocumentTagRangeStart(StructuredDocumentTagRangeStart sdtRangeStart)
     {
         indentAndAppendLine("[SdtRangeStart]");

         return VisitorAction.CONTINUE;
     }

     /// 
     /// Called when a SubDocument node is encountered in the document.
     /// 
     public int visitStructuredDocumentTagRangeEnd(StructuredDocumentTagRangeEnd sdtRangeEnd)
     {
         indentAndAppendLine("[SdtRangeEnd]");

         return VisitorAction.CONTINUE;
     }

     /// 
     /// Append a line to the StringBuilder and indent it depending on how deep the visitor is into the document tree.
     /// 
     /// 
     private void indentAndAppendLine(final String text) {
         for (int i = 0; i < mDocTraversalDepth; i++) {
             mAcceptingNodeChildTree.append("|  ");
         }

         mAcceptingNodeChildTree.append(text + "\r\n");
     }

     private int mDocTraversalDepth;
     private final StringBuilder mAcceptingNodeChildTree;
 }
 
```


[Aspose.Words Document Object Model _DOM_]: https://docs.aspose.com/words/java/aspose-words-document-object-model/
## Methoden

| Methode | Beschreibung |
| --- | --- |
| [visitAbsolutePositionTab(AbsolutePositionTab tab)](#visitAbsolutePositionTab-com.aspose.words.AbsolutePositionTab) | Wird aufgerufen, wenn ein [AbsolutePositionTab](../../com.aspose.words/absolutepositiontab/)‑Knoten im Dokument gefunden wird. |
| [visitBodyEnd(Body body)](#visitBodyEnd-com.aspose.words.Body) | Wird aufgerufen, wenn die Aufzählung der Haupttext‑Story in einem Abschnitt beendet ist. |
| [visitBodyStart(Body body)](#visitBodyStart-com.aspose.words.Body) | Wird aufgerufen, wenn die Aufzählung der Haupttext‑Story in einem Abschnitt begonnen hat. |
| [visitBookmarkEnd(BookmarkEnd bookmarkEnd)](#visitBookmarkEnd-com.aspose.words.BookmarkEnd) | Wird aufgerufen, wenn das Ende eines Lesezeichens im Dokument gefunden wird. |
| [visitBookmarkStart(BookmarkStart bookmarkStart)](#visitBookmarkStart-com.aspose.words.BookmarkStart) | Wird aufgerufen, wenn der Beginn eines Lesezeichens im Dokument gefunden wird. |
| [visitBuildingBlockEnd(BuildingBlock block)](#visitBuildingBlockEnd-com.aspose.words.BuildingBlock) | Wird aufgerufen, wenn die Aufzählung eines Bausteins beendet ist. |
| [visitBuildingBlockStart(BuildingBlock block)](#visitBuildingBlockStart-com.aspose.words.BuildingBlock) | Wird aufgerufen, wenn die Aufzählung eines Bausteins begonnen hat. |
| [visitCellEnd(Cell cell)](#visitCellEnd-com.aspose.words.Cell) | Wird aufgerufen, wenn die Aufzählung einer Tabellenzelle beendet ist. |
| [visitCellStart(Cell cell)](#visitCellStart-com.aspose.words.Cell) | Wird aufgerufen, wenn die Aufzählung einer Tabellenzelle begonnen hat. |
| [visitCommentEnd(Comment comment)](#visitCommentEnd-com.aspose.words.Comment) | Wird aufgerufen, wenn die Aufzählung eines Kommentartexts beendet ist. |
| [visitCommentRangeEnd(CommentRangeEnd commentRangeEnd)](#visitCommentRangeEnd-com.aspose.words.CommentRangeEnd) | Wird aufgerufen, wenn das Ende eines kommentierten Textbereichs gefunden wird. |
| [visitCommentRangeStart(CommentRangeStart commentRangeStart)](#visitCommentRangeStart-com.aspose.words.CommentRangeStart) | Wird aufgerufen, wenn der Beginn eines kommentierten Textbereichs gefunden wird. |
| [visitCommentStart(Comment comment)](#visitCommentStart-com.aspose.words.Comment) | Wird aufgerufen, wenn die Aufzählung eines Kommentartexts begonnen hat. |
| [visitDocumentEnd(Document doc)](#visitDocumentEnd-com.aspose.words.Document) | Aufgerufen, wenn die Aufzählung des Dokuments abgeschlossen ist. |
| [visitDocumentStart(Document doc)](#visitDocumentStart-com.aspose.words.Document) | Aufgerufen, wenn die Aufzählung des Dokuments begonnen hat. |
| [visitEditableRangeEnd(EditableRangeEnd editableRangeEnd)](#visitEditableRangeEnd-com.aspose.words.EditableRangeEnd) | Aufgerufen, wenn das Ende eines bearbeitbaren Bereichs im Dokument gefunden wird. |
| [visitEditableRangeStart(EditableRangeStart editableRangeStart)](#visitEditableRangeStart-com.aspose.words.EditableRangeStart) | Aufgerufen, wenn der Beginn eines bearbeitbaren Bereichs im Dokument gefunden wird. |
| [visitFieldEnd(FieldEnd fieldEnd)](#visitFieldEnd-com.aspose.words.FieldEnd) | Aufgerufen, wenn ein Feld im Dokument endet. |
| [visitFieldSeparator(FieldSeparator fieldSeparator)](#visitFieldSeparator-com.aspose.words.FieldSeparator) | Aufgerufen, wenn ein Feldtrennzeichen im Dokument gefunden wird. |
| [visitFieldStart(FieldStart fieldStart)](#visitFieldStart-com.aspose.words.FieldStart) | Aufgerufen, wenn ein Feld im Dokument beginnt. |
| [visitFootnoteEnd(Footnote footnote)](#visitFootnoteEnd-com.aspose.words.Footnote) | Aufgerufen, wenn die Aufzählung eines Fuß- oder Endnoten-Textes abgeschlossen ist. |
| [visitFootnoteStart(Footnote footnote)](#visitFootnoteStart-com.aspose.words.Footnote) | Aufgerufen, wenn die Aufzählung eines Fuß- oder Endnoten-Textes begonnen hat. |
| [visitFormField(FormField formField)](#visitFormField-com.aspose.words.FormField) | Aufgerufen, wenn ein Formularfeld im Dokument gefunden wird. |
| [visitGlossaryDocumentEnd(GlossaryDocument glossary)](#visitGlossaryDocumentEnd-com.aspose.words.GlossaryDocument) | Aufgerufen, wenn die Aufzählung eines Glossar-Dokuments abgeschlossen ist. |
| [visitGlossaryDocumentStart(GlossaryDocument glossary)](#visitGlossaryDocumentStart-com.aspose.words.GlossaryDocument) | Aufgerufen, wenn die Aufzählung eines Glossar-Dokuments begonnen hat. |
| [visitGroupShapeEnd(GroupShape groupShape)](#visitGroupShapeEnd-com.aspose.words.GroupShape) | Aufgerufen, wenn die Aufzählung einer Gruppenform abgeschlossen ist. |
| [visitGroupShapeStart(GroupShape groupShape)](#visitGroupShapeStart-com.aspose.words.GroupShape) | Aufgerufen, wenn die Aufzählung einer Gruppenform begonnen hat. |
| [visitHeaderFooterEnd(HeaderFooter headerFooter)](#visitHeaderFooterEnd-com.aspose.words.HeaderFooter) | Aufgerufen, wenn die Aufzählung einer Kopf- oder Fußzeile in einem Abschnitt abgeschlossen ist. |
| [visitHeaderFooterStart(HeaderFooter headerFooter)](#visitHeaderFooterStart-com.aspose.words.HeaderFooter) | Aufgerufen, wenn die Aufzählung einer Kopf- oder Fußzeile in einem Abschnitt begonnen hat. |
| [visitOfficeMathEnd(OfficeMath officeMath)](#visitOfficeMathEnd-com.aspose.words.OfficeMath) | Aufgerufen, wenn die Aufzählung eines Office‑Math‑Objekts abgeschlossen ist. |
| [visitOfficeMathStart(OfficeMath officeMath)](#visitOfficeMathStart-com.aspose.words.OfficeMath) | Aufgerufen, wenn die Aufzählung eines Office‑Math‑Objekts begonnen hat. |
| [visitParagraphEnd(Paragraph paragraph)](#visitParagraphEnd-com.aspose.words.Paragraph) | Aufgerufen, wenn die Aufzählung eines Absatzes abgeschlossen ist. |
| [visitParagraphStart(Paragraph paragraph)](#visitParagraphStart-com.aspose.words.Paragraph) | Aufgerufen, wenn die Aufzählung eines Absatzes begonnen hat. |
| [visitRowEnd(Row row)](#visitRowEnd-com.aspose.words.Row) | Aufgerufen, wenn die Aufzählung einer Tabellenzeile abgeschlossen ist. |
| [visitRowStart(Row row)](#visitRowStart-com.aspose.words.Row) | Aufgerufen, wenn die Aufzählung einer Tabellenzeile begonnen hat. |
| [visitRun(Run run)](#visitRun-com.aspose.words.Run) | Aufgerufen, wenn ein Textlauf im Dokument gefunden wird. |
| [visitSectionEnd(Section section)](#visitSectionEnd-com.aspose.words.Section) | Aufgerufen, wenn die Aufzählung eines Abschnitts abgeschlossen ist. |
| [visitSectionStart(Section section)](#visitSectionStart-com.aspose.words.Section) | Aufgerufen, wenn die Aufzählung eines Abschnitts begonnen hat. |
| [visitShapeEnd(Shape shape)](#visitShapeEnd-com.aspose.words.Shape) | Aufgerufen, wenn die Aufzählung einer Form beendet ist. |
| [visitShapeStart(Shape shape)](#visitShapeStart-com.aspose.words.Shape) | Aufgerufen, wenn die Aufzählung einer Form begonnen hat. |
| [visitSmartTagEnd(SmartTag smartTag)](#visitSmartTagEnd-com.aspose.words.SmartTag) | Aufgerufen, wenn die Aufzählung eines Smart-Tags beendet ist. |
| [visitSmartTagStart(SmartTag smartTag)](#visitSmartTagStart-com.aspose.words.SmartTag) | Aufgerufen, wenn die Aufzählung eines Smart-Tags begonnen hat. |
| [visitSpecialChar(SpecialChar specialChar)](#visitSpecialChar-com.aspose.words.SpecialChar) | Aufgerufen, wenn ein [SpecialChar](../../com.aspose.words/specialchar/) Knoten im Dokument gefunden wird. |
| [visitStructuredDocumentTagEnd(StructuredDocumentTag sdt)](#visitStructuredDocumentTagEnd-com.aspose.words.StructuredDocumentTag) | Aufgerufen, wenn die Aufzählung eines strukturierten Dokument-Tags beendet ist. |
| [visitStructuredDocumentTagRangeEnd(StructuredDocumentTagRangeEnd sdtRangeEnd)](#visitStructuredDocumentTagRangeEnd-com.aspose.words.StructuredDocumentTagRangeEnd) | Aufgerufen, wenn ein StructuredDocumentTagRangeEnd gefunden wird. |
| [visitStructuredDocumentTagRangeStart(StructuredDocumentTagRangeStart sdtRangeStart)](#visitStructuredDocumentTagRangeStart-com.aspose.words.StructuredDocumentTagRangeStart) | Aufgerufen, wenn ein StructuredDocumentTagRangeStart gefunden wird. |
| [visitStructuredDocumentTagStart(StructuredDocumentTag sdt)](#visitStructuredDocumentTagStart-com.aspose.words.StructuredDocumentTag) | Aufgerufen, wenn die Aufzählung eines strukturierten Dokument-Tags begonnen hat. |
| [visitSubDocument(SubDocument subDocument)](#visitSubDocument-com.aspose.words.SubDocument) | Aufgerufen, wenn ein Unterdokument gefunden wird. |
| [visitTableEnd(Table table)](#visitTableEnd-com.aspose.words.Table) | Aufgerufen, wenn die Aufzählung einer Tabelle beendet ist. |
| [visitTableStart(Table table)](#visitTableStart-com.aspose.words.Table) | Aufgerufen, wenn die Aufzählung einer Tabelle begonnen hat. |
### visitAbsolutePositionTab(AbsolutePositionTab tab) {#visitAbsolutePositionTab-com.aspose.words.AbsolutePositionTab}
```
public int visitAbsolutePositionTab(AbsolutePositionTab tab)
```


Wird aufgerufen, wenn ein [AbsolutePositionTab](../../com.aspose.words/absolutepositiontab/)‑Knoten im Dokument gefunden wird.

 **Examples:** 

Zeigt, wie man Tabulatorzeichen mit absoluter Position mit einem DocumentVisitor verarbeitet.

```

 public void documentToTxt() throws Exception {
     Document doc = new Document(getMyDir() + "Absolute position tab.docx");

     // Extract the text contents of our document by accepting this custom document visitor.
     DocTextExtractor myDocTextExtractor = new DocTextExtractor();
     Section fisrtSection = doc.getFirstSection();
     fisrtSection.getBody().accept(myDocTextExtractor);
     // Visit only start of the document body.
     fisrtSection.getBody().acceptStart(myDocTextExtractor);
     // Visit only end of the document body.
     fisrtSection.getBody().acceptEnd(myDocTextExtractor);

     // The absolute position tab, which has no equivalent in string form, has been explicitly converted to a tab character.
     Assert.assertEquals("Before AbsolutePositionTab\tAfter AbsolutePositionTab", myDocTextExtractor.getText());

     // An AbsolutePositionTab can accept a DocumentVisitor by itself too.
     AbsolutePositionTab absPositionTab = (AbsolutePositionTab) doc.getFirstSection().getBody().getFirstParagraph().getChild(NodeType.SPECIAL_CHAR, 0, true);

     myDocTextExtractor = new DocTextExtractor();
     absPositionTab.accept(myDocTextExtractor);

     Assert.assertEquals("\t", myDocTextExtractor.getText());
 }

 /// 
 /// Collects the text contents of all runs in the visited document. Replaces all absolute tab characters with ordinary tabs.
 /// 
 public static class DocTextExtractor extends DocumentVisitor {
     public DocTextExtractor() {
         mBuilder = new StringBuilder();
     }

     /// 
     /// Called when a Run node is encountered in the document.
     /// 
     public int visitRun(final Run run) {
         appendText(run.getText());
         return VisitorAction.CONTINUE;
     }

     /// 
     /// Called when an AbsolutePositionTab node is encountered in the document.
     /// 
     public int visitAbsolutePositionTab(final AbsolutePositionTab tab) {
         mBuilder.append("\t");

         return VisitorAction.CONTINUE;
     }

     /// 
     /// Adds text to the current output. Honors the enabled/disabled output flag.
     /// 
     public void appendText(final String text) {
         mBuilder.append(text);
     }

     /// 
     /// Plain text of the document that was accumulated by the visitor.
     /// 
     public String getText() {
         return mBuilder.toString();
     }

     private final StringBuilder mBuilder;
 }
 
```

**Parameters:**
| Parameter | Typ | Beschreibung |
| --- | --- | --- |
| tab | [AbsolutePositionTab](../../com.aspose.words/absolutepositiontab/) | Das Objekt, das besucht wird. |

**Returns:**
int - Ein [VisitorAction](../../com.aspose.words/visitoraction/) Wert, der angibt, wie die Aufzählung fortgesetzt werden soll. Der zurückgegebene Wert ist einer der [VisitorAction](../../com.aspose.words/visitoraction/) Konstanten.
### visitBodyEnd(Body body) {#visitBodyEnd-com.aspose.words.Body}
```
public int visitBodyEnd(Body body)
```


Wird aufgerufen, wenn die Aufzählung der Haupttext‑Story in einem Abschnitt beendet ist.

 **Examples:** 

Zeigt, wie ein DocumentVisitor verwendet wird, um die Knotenstruktur eines Dokuments auszugeben.

```

 public void docStructureToText() throws Exception {
     Document doc = new Document(getMyDir() + "DocumentVisitor-compatible features.docx");
     DocStructurePrinter visitor = new DocStructurePrinter();

     // When we get a composite node to accept a document visitor, the visitor visits the accepting node,
     // and then traverses all the node's children in a depth-first manner.
     // The visitor can read and modify each visited node.
     doc.accept(visitor);

     System.out.println(visitor.getText());
 }

 /// 
 /// Traverses a node's tree of child nodes.
 /// Creates a map of this tree in the form of a string.
 /// 
 public static class DocStructurePrinter extends DocumentVisitor {
     public DocStructurePrinter() {
         mAcceptingNodeChildTree = new StringBuilder();
     }

     public String getText() {
         return mAcceptingNodeChildTree.toString();
     }

     /// 
     /// Called when a Document node is encountered.
     /// 
     public int visitDocumentStart(Document doc) {
         int childNodeCount = doc.getChildNodes(NodeType.ANY, true).getCount();

         indentAndAppendLine("[Document start] Child nodes: " + childNodeCount);
         mDocTraversalDepth++;

         // Allow the visitor to continue visiting other nodes.
         return VisitorAction.CONTINUE;
     }

     /// 
     /// Called after all the child nodes of a Document node have been visited.
     /// 
     public int visitDocumentEnd(Document doc) {
         mDocTraversalDepth--;
         indentAndAppendLine("[Document end]");

         return VisitorAction.CONTINUE;
     }

     /// 
     /// Called when a Section node is encountered in the document.
     /// 
     public int visitSectionStart(final Section section) {
         // Get the index of our section within the document
         NodeCollection docSections = section.getDocument().getChildNodes(NodeType.SECTION, false);
         int sectionIndex = docSections.indexOf(section);

         indentAndAppendLine("[Section start] Section index: " + sectionIndex);
         mDocTraversalDepth++;

         return VisitorAction.CONTINUE;
     }

     /// 
     /// Called after all the child nodes of a Section node have been visited.
     /// 
     public int visitSectionEnd(final Section section) {
         mDocTraversalDepth--;
         indentAndAppendLine("[Section end]");

         return VisitorAction.CONTINUE;
     }

     /// 
     /// Called when a Body node is encountered in the document.
     /// 
     public int visitBodyStart(final Body body) {
         int paragraphCount = body.getParagraphs().getCount();
         indentAndAppendLine("[Body start] Paragraphs: " + paragraphCount);
         mDocTraversalDepth++;

         return VisitorAction.CONTINUE;
     }

     /// 
     /// Called after all the child nodes of a Body node have been visited.
     /// 
     public int visitBodyEnd(final Body body) {
         mDocTraversalDepth--;
         indentAndAppendLine("[Body end]");

         return VisitorAction.CONTINUE;
     }

     /// 
     /// Called when a Paragraph node is encountered in the document.
     /// 
     public int visitParagraphStart(final Paragraph paragraph) {
         indentAndAppendLine("[Paragraph start]");
         mDocTraversalDepth++;

         return VisitorAction.CONTINUE;
     }

     /// 
     /// Called after all the child nodes of a Paragraph node have been visited.
     /// 
     public int visitParagraphEnd(final Paragraph paragraph) {
         mDocTraversalDepth--;
         indentAndAppendLine("[Paragraph end]");

         return VisitorAction.CONTINUE;
     }

     /// 
     /// Called when a Run node is encountered in the document.
     /// 
     public int visitRun(final Run run) {
         indentAndAppendLine("[Run] \"" + run.getText() + "\"");

         return VisitorAction.CONTINUE;
     }

     /// 
     /// Called when a SubDocument node is encountered in the document.
     /// 
     public int visitSubDocument(final SubDocument subDocument) {
         indentAndAppendLine("[SubDocument]");

         return VisitorAction.CONTINUE;
     }

     /// 
     /// Called when a SubDocument node is encountered in the document.
     /// 
     public int visitStructuredDocumentTagRangeStart(StructuredDocumentTagRangeStart sdtRangeStart)
     {
         indentAndAppendLine("[SdtRangeStart]");

         return VisitorAction.CONTINUE;
     }

     /// 
     /// Called when a SubDocument node is encountered in the document.
     /// 
     public int visitStructuredDocumentTagRangeEnd(StructuredDocumentTagRangeEnd sdtRangeEnd)
     {
         indentAndAppendLine("[SdtRangeEnd]");

         return VisitorAction.CONTINUE;
     }

     /// 
     /// Append a line to the StringBuilder and indent it depending on how deep the visitor is into the document tree.
     /// 
     /// 
     private void indentAndAppendLine(final String text) {
         for (int i = 0; i < mDocTraversalDepth; i++) {
             mAcceptingNodeChildTree.append("|  ");
         }

         mAcceptingNodeChildTree.append(text + "\r\n");
     }

     private int mDocTraversalDepth;
     private final StringBuilder mAcceptingNodeChildTree;
 }
 
```

**Parameters:**
| Parameter | Typ | Beschreibung |
| --- | --- | --- |
| body | [Body](../../com.aspose.words/body/) | Das Objekt, das besucht wird. |

**Returns:**
int - Ein [VisitorAction](../../com.aspose.words/visitoraction/) Wert, der angibt, wie die Aufzählung fortgesetzt werden soll. Der zurückgegebene Wert ist einer der [VisitorAction](../../com.aspose.words/visitoraction/) Konstanten.
### visitBodyStart(Body body) {#visitBodyStart-com.aspose.words.Body}
```
public int visitBodyStart(Body body)
```


Wird aufgerufen, wenn die Aufzählung der Haupttext‑Story in einem Abschnitt begonnen hat.

 **Examples:** 

Zeigt, wie ein DocumentVisitor verwendet wird, um die Knotenstruktur eines Dokuments auszugeben.

```

 public void docStructureToText() throws Exception {
     Document doc = new Document(getMyDir() + "DocumentVisitor-compatible features.docx");
     DocStructurePrinter visitor = new DocStructurePrinter();

     // When we get a composite node to accept a document visitor, the visitor visits the accepting node,
     // and then traverses all the node's children in a depth-first manner.
     // The visitor can read and modify each visited node.
     doc.accept(visitor);

     System.out.println(visitor.getText());
 }

 /// 
 /// Traverses a node's tree of child nodes.
 /// Creates a map of this tree in the form of a string.
 /// 
 public static class DocStructurePrinter extends DocumentVisitor {
     public DocStructurePrinter() {
         mAcceptingNodeChildTree = new StringBuilder();
     }

     public String getText() {
         return mAcceptingNodeChildTree.toString();
     }

     /// 
     /// Called when a Document node is encountered.
     /// 
     public int visitDocumentStart(Document doc) {
         int childNodeCount = doc.getChildNodes(NodeType.ANY, true).getCount();

         indentAndAppendLine("[Document start] Child nodes: " + childNodeCount);
         mDocTraversalDepth++;

         // Allow the visitor to continue visiting other nodes.
         return VisitorAction.CONTINUE;
     }

     /// 
     /// Called after all the child nodes of a Document node have been visited.
     /// 
     public int visitDocumentEnd(Document doc) {
         mDocTraversalDepth--;
         indentAndAppendLine("[Document end]");

         return VisitorAction.CONTINUE;
     }

     /// 
     /// Called when a Section node is encountered in the document.
     /// 
     public int visitSectionStart(final Section section) {
         // Get the index of our section within the document
         NodeCollection docSections = section.getDocument().getChildNodes(NodeType.SECTION, false);
         int sectionIndex = docSections.indexOf(section);

         indentAndAppendLine("[Section start] Section index: " + sectionIndex);
         mDocTraversalDepth++;

         return VisitorAction.CONTINUE;
     }

     /// 
     /// Called after all the child nodes of a Section node have been visited.
     /// 
     public int visitSectionEnd(final Section section) {
         mDocTraversalDepth--;
         indentAndAppendLine("[Section end]");

         return VisitorAction.CONTINUE;
     }

     /// 
     /// Called when a Body node is encountered in the document.
     /// 
     public int visitBodyStart(final Body body) {
         int paragraphCount = body.getParagraphs().getCount();
         indentAndAppendLine("[Body start] Paragraphs: " + paragraphCount);
         mDocTraversalDepth++;

         return VisitorAction.CONTINUE;
     }

     /// 
     /// Called after all the child nodes of a Body node have been visited.
     /// 
     public int visitBodyEnd(final Body body) {
         mDocTraversalDepth--;
         indentAndAppendLine("[Body end]");

         return VisitorAction.CONTINUE;
     }

     /// 
     /// Called when a Paragraph node is encountered in the document.
     /// 
     public int visitParagraphStart(final Paragraph paragraph) {
         indentAndAppendLine("[Paragraph start]");
         mDocTraversalDepth++;

         return VisitorAction.CONTINUE;
     }

     /// 
     /// Called after all the child nodes of a Paragraph node have been visited.
     /// 
     public int visitParagraphEnd(final Paragraph paragraph) {
         mDocTraversalDepth--;
         indentAndAppendLine("[Paragraph end]");

         return VisitorAction.CONTINUE;
     }

     /// 
     /// Called when a Run node is encountered in the document.
     /// 
     public int visitRun(final Run run) {
         indentAndAppendLine("[Run] \"" + run.getText() + "\"");

         return VisitorAction.CONTINUE;
     }

     /// 
     /// Called when a SubDocument node is encountered in the document.
     /// 
     public int visitSubDocument(final SubDocument subDocument) {
         indentAndAppendLine("[SubDocument]");

         return VisitorAction.CONTINUE;
     }

     /// 
     /// Called when a SubDocument node is encountered in the document.
     /// 
     public int visitStructuredDocumentTagRangeStart(StructuredDocumentTagRangeStart sdtRangeStart)
     {
         indentAndAppendLine("[SdtRangeStart]");

         return VisitorAction.CONTINUE;
     }

     /// 
     /// Called when a SubDocument node is encountered in the document.
     /// 
     public int visitStructuredDocumentTagRangeEnd(StructuredDocumentTagRangeEnd sdtRangeEnd)
     {
         indentAndAppendLine("[SdtRangeEnd]");

         return VisitorAction.CONTINUE;
     }

     /// 
     /// Append a line to the StringBuilder and indent it depending on how deep the visitor is into the document tree.
     /// 
     /// 
     private void indentAndAppendLine(final String text) {
         for (int i = 0; i < mDocTraversalDepth; i++) {
             mAcceptingNodeChildTree.append("|  ");
         }

         mAcceptingNodeChildTree.append(text + "\r\n");
     }

     private int mDocTraversalDepth;
     private final StringBuilder mAcceptingNodeChildTree;
 }
 
```

**Parameters:**
| Parameter | Typ | Beschreibung |
| --- | --- | --- |
| body | [Body](../../com.aspose.words/body/) | Das Objekt, das besucht wird. |

**Returns:**
int - Ein [VisitorAction](../../com.aspose.words/visitoraction/) Wert, der angibt, wie die Aufzählung fortgesetzt werden soll. Der zurückgegebene Wert ist einer der [VisitorAction](../../com.aspose.words/visitoraction/) Konstanten.
### visitBookmarkEnd(BookmarkEnd bookmarkEnd) {#visitBookmarkEnd-com.aspose.words.BookmarkEnd}
```
public int visitBookmarkEnd(BookmarkEnd bookmarkEnd)
```


Wird aufgerufen, wenn das Ende eines Lesezeichens im Dokument gefunden wird.

 **Examples:** 

Zeigt, wie man Lesezeichen hinzufügt und deren Inhalte aktualisiert.

```

 public void createUpdateAndPrintBookmarks() throws Exception {
     // Create a document with three bookmarks, then use a custom document visitor implementation to print their contents.
     Document doc = createDocumentWithBookmarks(3);
     BookmarkCollection bookmarks = doc.getRange().getBookmarks();
     printAllBookmarkInfo(bookmarks);

     // Bookmarks can be accessed in the bookmark collection by index or name, and their names can be updated.
     bookmarks.get(0).setName("{bookmarks[0].Name}_NewName");
     bookmarks.get("MyBookmark_2").setText("Updated text contents of {bookmarks[1].Name}");

     // Print all bookmarks again to see updated values.
     printAllBookmarkInfo(bookmarks);
 }

 /// 
 /// Create a document with a given number of bookmarks.
 /// 
 private static Document createDocumentWithBookmarks(int numberOfBookmarks) throws Exception {
     Document doc = new Document();
     DocumentBuilder builder = new DocumentBuilder(doc);

     for (int i = 1; i <= numberOfBookmarks; i++) {
         String bookmarkName = "MyBookmark_" + i;

         builder.write("Text before bookmark.");
         builder.startBookmark(bookmarkName);
         builder.write(MessageFormat.format("Text inside {0}.", bookmarkName));
         builder.endBookmark(bookmarkName);
         builder.writeln("Text after bookmark.");
     }

     return doc;
 }

 /// 
 /// Use an iterator and a visitor to print info of every bookmark in the collection.
 /// 
 private static void printAllBookmarkInfo(BookmarkCollection bookmarks) throws Exception {
     BookmarkInfoPrinter bookmarkVisitor = new BookmarkInfoPrinter();

     // Get each bookmark in the collection to accept a visitor that will print its contents.
     Iterator enumerator = bookmarks.iterator();

     while (enumerator.hasNext()) {
         Bookmark currentBookmark = enumerator.next();

         if (currentBookmark != null) {
             currentBookmark.getBookmarkStart().accept(bookmarkVisitor);
             currentBookmark.getBookmarkEnd().accept(bookmarkVisitor);

             System.out.println(currentBookmark.getBookmarkStart().getText());
         }
     }
 }

 /// 
 /// Prints contents of every visited bookmark to the console.
 /// 
 public static class BookmarkInfoPrinter extends DocumentVisitor {
     public int visitBookmarkStart(BookmarkStart bookmarkStart) throws Exception {
         System.out.println(MessageFormat.format("BookmarkStart name: \"{0}\", Content: \"{1}\"", bookmarkStart.getName(),
                 bookmarkStart.getBookmark().getText()));
         return VisitorAction.CONTINUE;
     }

     public int visitBookmarkEnd(BookmarkEnd bookmarkEnd) {
         System.out.println(MessageFormat.format("BookmarkEnd name: \"{0}\"", bookmarkEnd.getName()));
         return VisitorAction.CONTINUE;
     }
 }
 
```

**Parameters:**
| Parameter | Typ | Beschreibung |
| --- | --- | --- |
| bookmarkEnd | [BookmarkEnd](../../com.aspose.words/bookmarkend/) | Das Objekt, das besucht wird. |

**Returns:**
int - Ein [VisitorAction](../../com.aspose.words/visitoraction/) Wert, der angibt, wie die Aufzählung fortgesetzt werden soll. Der zurückgegebene Wert ist einer der [VisitorAction](../../com.aspose.words/visitoraction/) Konstanten.
### visitBookmarkStart(BookmarkStart bookmarkStart) {#visitBookmarkStart-com.aspose.words.BookmarkStart}
```
public int visitBookmarkStart(BookmarkStart bookmarkStart)
```


Wird aufgerufen, wenn der Beginn eines Lesezeichens im Dokument gefunden wird.

 **Examples:** 

Zeigt, wie man Lesezeichen hinzufügt und deren Inhalte aktualisiert.

```

 public void createUpdateAndPrintBookmarks() throws Exception {
     // Create a document with three bookmarks, then use a custom document visitor implementation to print their contents.
     Document doc = createDocumentWithBookmarks(3);
     BookmarkCollection bookmarks = doc.getRange().getBookmarks();
     printAllBookmarkInfo(bookmarks);

     // Bookmarks can be accessed in the bookmark collection by index or name, and their names can be updated.
     bookmarks.get(0).setName("{bookmarks[0].Name}_NewName");
     bookmarks.get("MyBookmark_2").setText("Updated text contents of {bookmarks[1].Name}");

     // Print all bookmarks again to see updated values.
     printAllBookmarkInfo(bookmarks);
 }

 /// 
 /// Create a document with a given number of bookmarks.
 /// 
 private static Document createDocumentWithBookmarks(int numberOfBookmarks) throws Exception {
     Document doc = new Document();
     DocumentBuilder builder = new DocumentBuilder(doc);

     for (int i = 1; i <= numberOfBookmarks; i++) {
         String bookmarkName = "MyBookmark_" + i;

         builder.write("Text before bookmark.");
         builder.startBookmark(bookmarkName);
         builder.write(MessageFormat.format("Text inside {0}.", bookmarkName));
         builder.endBookmark(bookmarkName);
         builder.writeln("Text after bookmark.");
     }

     return doc;
 }

 /// 
 /// Use an iterator and a visitor to print info of every bookmark in the collection.
 /// 
 private static void printAllBookmarkInfo(BookmarkCollection bookmarks) throws Exception {
     BookmarkInfoPrinter bookmarkVisitor = new BookmarkInfoPrinter();

     // Get each bookmark in the collection to accept a visitor that will print its contents.
     Iterator enumerator = bookmarks.iterator();

     while (enumerator.hasNext()) {
         Bookmark currentBookmark = enumerator.next();

         if (currentBookmark != null) {
             currentBookmark.getBookmarkStart().accept(bookmarkVisitor);
             currentBookmark.getBookmarkEnd().accept(bookmarkVisitor);

             System.out.println(currentBookmark.getBookmarkStart().getText());
         }
     }
 }

 /// 
 /// Prints contents of every visited bookmark to the console.
 /// 
 public static class BookmarkInfoPrinter extends DocumentVisitor {
     public int visitBookmarkStart(BookmarkStart bookmarkStart) throws Exception {
         System.out.println(MessageFormat.format("BookmarkStart name: \"{0}\", Content: \"{1}\"", bookmarkStart.getName(),
                 bookmarkStart.getBookmark().getText()));
         return VisitorAction.CONTINUE;
     }

     public int visitBookmarkEnd(BookmarkEnd bookmarkEnd) {
         System.out.println(MessageFormat.format("BookmarkEnd name: \"{0}\"", bookmarkEnd.getName()));
         return VisitorAction.CONTINUE;
     }
 }
 
```

**Parameters:**
| Parameter | Typ | Beschreibung |
| --- | --- | --- |
| bookmarkStart | [BookmarkStart](../../com.aspose.words/bookmarkstart/) | Das Objekt, das besucht wird. |

**Returns:**
int - Ein [VisitorAction](../../com.aspose.words/visitoraction/) Wert, der angibt, wie die Aufzählung fortgesetzt werden soll. Der zurückgegebene Wert ist einer der [VisitorAction](../../com.aspose.words/visitoraction/) Konstanten.
### visitBuildingBlockEnd(BuildingBlock block) {#visitBuildingBlockEnd-com.aspose.words.BuildingBlock}
```
public int visitBuildingBlockEnd(BuildingBlock block)
```


Wird aufgerufen, wenn die Aufzählung eines Bausteins beendet ist.

 **Remarks:** 

Hinweis: Ein Building-Block-Knoten und seine Kinder werden nicht besucht, wenn Sie einen Visitor über ein [Document](../../com.aspose.words/document/) ausführen. Wenn Sie einen Visitor über einen Building-Block ausführen möchten, müssen Sie den Visitor über ein [GlossaryDocument](../../com.aspose.words/glossarydocument/) ausführen oder [BuildingBlock.accept(com.aspose.words.DocumentVisitor)](../../com.aspose.words/buildingblock/\#accept-com.aspose.words.DocumentVisitor) aufrufen.

 **Examples:** 

Zeigt Möglichkeiten zum Zugriff auf Bausteine in einem Glossar-Dokument.

```

 public void glossaryDocument() throws Exception {
     Document doc = new Document();
     GlossaryDocument glossaryDoc = new GlossaryDocument();

     glossaryDoc.appendChild(createNewBuildingBlock(glossaryDoc, "Block 1"));
     glossaryDoc.appendChild(createNewBuildingBlock(glossaryDoc, "Block 2"));
     glossaryDoc.appendChild(createNewBuildingBlock(glossaryDoc, "Block 3"));
     glossaryDoc.appendChild(createNewBuildingBlock(glossaryDoc, "Block 4"));
     glossaryDoc.appendChild(createNewBuildingBlock(glossaryDoc, "Block 5"));

     Assert.assertEquals(glossaryDoc.getBuildingBlocks().getCount(), 5);

     doc.setGlossaryDocument(glossaryDoc);

     // There are various ways of accessing building blocks.
     // 1 -  Get the first/last building blocks in the collection:
     Assert.assertEquals("Block 1", glossaryDoc.getFirstBuildingBlock().getName());
     Assert.assertEquals("Block 5", glossaryDoc.getLastBuildingBlock().getName());

     // 2 -  Get a building block by index:
     Assert.assertEquals("Block 2", glossaryDoc.getBuildingBlocks().get(1).getName());
     Assert.assertEquals("Block 3", glossaryDoc.getBuildingBlocks().toArray()[2].getName());

     // 3 -  Get the first building block that matches a gallery, name and category:
     Assert.assertEquals("Block 4",
             glossaryDoc.getBuildingBlock(BuildingBlockGallery.ALL, "(Empty Category)", "Block 4").getName());

     // We will do that using a custom visitor,
     // which will give every BuildingBlock in the GlossaryDocument a unique GUID
     GlossaryDocVisitor visitor = new GlossaryDocVisitor();
     // Visit start/end of the Glossary document.
     glossaryDoc.accept(visitor);
     // Visit only start of the Glossary document.
     glossaryDoc.acceptStart(visitor);
     // Visit only end of the Glossary document.
     glossaryDoc.acceptEnd(visitor);
     System.out.println(visitor.getText());

     // In Microsoft Word, we can access the building blocks via "Insert" -> "Quick Parts" -> "Building Blocks Organizer".
     doc.save(getArtifactsDir() + "BuildingBlocks.GlossaryDocument.dotx");
 }

 public static BuildingBlock createNewBuildingBlock(final GlossaryDocument glossaryDoc, final String buildingBlockName) {
     BuildingBlock buildingBlock = new BuildingBlock(glossaryDoc);
     buildingBlock.setName(buildingBlockName);

     return buildingBlock;
 }

 /// 
 /// Gives each building block in a visited glossary document a unique GUID.
 /// Stores the GUID-building block pairs in a dictionary.
 /// 
 public static class GlossaryDocVisitor extends DocumentVisitor {
     public GlossaryDocVisitor() {
         mBlocksByGuid = new HashMap<>();
         mBuilder = new StringBuilder();
     }

     public String getText() {
         return mBuilder.toString();
     }

     public HashMap getDictionary() {
         return mBlocksByGuid;
     }

     public int visitGlossaryDocumentStart(final GlossaryDocument glossary) {
         mBuilder.append("Glossary document found!\n");
         return VisitorAction.CONTINUE;
     }

     public int visitGlossaryDocumentEnd(final GlossaryDocument glossary) {
         mBuilder.append("Reached end of glossary!\n");
         mBuilder.append("BuildingBlocks found: " + mBlocksByGuid.size() + "\r\n");
         return VisitorAction.CONTINUE;
     }

     public int visitBuildingBlockStart(final BuildingBlock block) {
         block.setGuid(UUID.randomUUID());
         mBlocksByGuid.put(block.getGuid(), block);
         return VisitorAction.CONTINUE;
     }

     public int visitBuildingBlockEnd(final BuildingBlock block) {
         mBuilder.append("\tVisited block \"" + block.getName() + "\"" + "\r\n");
         mBuilder.append("\t Type: " + block.getType() + "\r\n");
         mBuilder.append("\t Gallery: " + block.getGallery() + "\r\n");
         mBuilder.append("\t Behavior: " + block.getBehavior() + "\r\n");
         mBuilder.append("\t Description: " + block.getDescription() + "\r\n");

         return VisitorAction.CONTINUE;
     }

     private final HashMap mBlocksByGuid;
     private final StringBuilder mBuilder;
 }
 
```

**Parameters:**
| Parameter | Typ | Beschreibung |
| --- | --- | --- |
| block | [BuildingBlock](../../com.aspose.words/buildingblock/) | Das Objekt, das besucht wird. |

**Returns:**
int - Ein [VisitorAction](../../com.aspose.words/visitoraction/) Wert, der angibt, wie die Aufzählung fortgesetzt werden soll. Der zurückgegebene Wert ist einer der [VisitorAction](../../com.aspose.words/visitoraction/) Konstanten.
### visitBuildingBlockStart(BuildingBlock block) {#visitBuildingBlockStart-com.aspose.words.BuildingBlock}
```
public int visitBuildingBlockStart(BuildingBlock block)
```


Wird aufgerufen, wenn die Aufzählung eines Bausteins begonnen hat.

 **Remarks:** 

Hinweis: Ein Building-Block-Knoten und seine Kinder werden nicht besucht, wenn Sie einen Visitor über ein [Document](../../com.aspose.words/document/) ausführen. Wenn Sie einen Visitor über einen Building-Block ausführen möchten, müssen Sie den Visitor über ein [GlossaryDocument](../../com.aspose.words/glossarydocument/) ausführen oder [BuildingBlock.accept(com.aspose.words.DocumentVisitor)](../../com.aspose.words/buildingblock/\#accept-com.aspose.words.DocumentVisitor) aufrufen.

 **Examples:** 

Zeigt Möglichkeiten zum Zugriff auf Bausteine in einem Glossar-Dokument.

```

 public void glossaryDocument() throws Exception {
     Document doc = new Document();
     GlossaryDocument glossaryDoc = new GlossaryDocument();

     glossaryDoc.appendChild(createNewBuildingBlock(glossaryDoc, "Block 1"));
     glossaryDoc.appendChild(createNewBuildingBlock(glossaryDoc, "Block 2"));
     glossaryDoc.appendChild(createNewBuildingBlock(glossaryDoc, "Block 3"));
     glossaryDoc.appendChild(createNewBuildingBlock(glossaryDoc, "Block 4"));
     glossaryDoc.appendChild(createNewBuildingBlock(glossaryDoc, "Block 5"));

     Assert.assertEquals(glossaryDoc.getBuildingBlocks().getCount(), 5);

     doc.setGlossaryDocument(glossaryDoc);

     // There are various ways of accessing building blocks.
     // 1 -  Get the first/last building blocks in the collection:
     Assert.assertEquals("Block 1", glossaryDoc.getFirstBuildingBlock().getName());
     Assert.assertEquals("Block 5", glossaryDoc.getLastBuildingBlock().getName());

     // 2 -  Get a building block by index:
     Assert.assertEquals("Block 2", glossaryDoc.getBuildingBlocks().get(1).getName());
     Assert.assertEquals("Block 3", glossaryDoc.getBuildingBlocks().toArray()[2].getName());

     // 3 -  Get the first building block that matches a gallery, name and category:
     Assert.assertEquals("Block 4",
             glossaryDoc.getBuildingBlock(BuildingBlockGallery.ALL, "(Empty Category)", "Block 4").getName());

     // We will do that using a custom visitor,
     // which will give every BuildingBlock in the GlossaryDocument a unique GUID
     GlossaryDocVisitor visitor = new GlossaryDocVisitor();
     // Visit start/end of the Glossary document.
     glossaryDoc.accept(visitor);
     // Visit only start of the Glossary document.
     glossaryDoc.acceptStart(visitor);
     // Visit only end of the Glossary document.
     glossaryDoc.acceptEnd(visitor);
     System.out.println(visitor.getText());

     // In Microsoft Word, we can access the building blocks via "Insert" -> "Quick Parts" -> "Building Blocks Organizer".
     doc.save(getArtifactsDir() + "BuildingBlocks.GlossaryDocument.dotx");
 }

 public static BuildingBlock createNewBuildingBlock(final GlossaryDocument glossaryDoc, final String buildingBlockName) {
     BuildingBlock buildingBlock = new BuildingBlock(glossaryDoc);
     buildingBlock.setName(buildingBlockName);

     return buildingBlock;
 }

 /// 
 /// Gives each building block in a visited glossary document a unique GUID.
 /// Stores the GUID-building block pairs in a dictionary.
 /// 
 public static class GlossaryDocVisitor extends DocumentVisitor {
     public GlossaryDocVisitor() {
         mBlocksByGuid = new HashMap<>();
         mBuilder = new StringBuilder();
     }

     public String getText() {
         return mBuilder.toString();
     }

     public HashMap getDictionary() {
         return mBlocksByGuid;
     }

     public int visitGlossaryDocumentStart(final GlossaryDocument glossary) {
         mBuilder.append("Glossary document found!\n");
         return VisitorAction.CONTINUE;
     }

     public int visitGlossaryDocumentEnd(final GlossaryDocument glossary) {
         mBuilder.append("Reached end of glossary!\n");
         mBuilder.append("BuildingBlocks found: " + mBlocksByGuid.size() + "\r\n");
         return VisitorAction.CONTINUE;
     }

     public int visitBuildingBlockStart(final BuildingBlock block) {
         block.setGuid(UUID.randomUUID());
         mBlocksByGuid.put(block.getGuid(), block);
         return VisitorAction.CONTINUE;
     }

     public int visitBuildingBlockEnd(final BuildingBlock block) {
         mBuilder.append("\tVisited block \"" + block.getName() + "\"" + "\r\n");
         mBuilder.append("\t Type: " + block.getType() + "\r\n");
         mBuilder.append("\t Gallery: " + block.getGallery() + "\r\n");
         mBuilder.append("\t Behavior: " + block.getBehavior() + "\r\n");
         mBuilder.append("\t Description: " + block.getDescription() + "\r\n");

         return VisitorAction.CONTINUE;
     }

     private final HashMap mBlocksByGuid;
     private final StringBuilder mBuilder;
 }
 
```

**Parameters:**
| Parameter | Typ | Beschreibung |
| --- | --- | --- |
| block | [BuildingBlock](../../com.aspose.words/buildingblock/) | Das Objekt, das besucht wird. |

**Returns:**
int - Ein [VisitorAction](../../com.aspose.words/visitoraction/) Wert, der angibt, wie die Aufzählung fortgesetzt werden soll. Der zurückgegebene Wert ist einer der [VisitorAction](../../com.aspose.words/visitoraction/) Konstanten.
### visitCellEnd(Cell cell) {#visitCellEnd-com.aspose.words.Cell}
```
public int visitCellEnd(Cell cell)
```


Wird aufgerufen, wenn die Aufzählung einer Tabellenzelle beendet ist.

 **Examples:** 

Zeigt, wie man die Knotenstruktur jeder Tabelle in einem Dokument ausgibt.

```

 public void tableToText() throws Exception {
     Document doc = new Document(getMyDir() + "DocumentVisitor-compatible features.docx");
     TableStructurePrinter visitor = new TableStructurePrinter();

     // When we get a composite node to accept a document visitor, the visitor visits the accepting node,
     // and then traverses all the node's children in a depth-first manner.
     // The visitor can read and modify each visited node.
     doc.accept(visitor);

     System.out.println(visitor.getText());
 }

 /// 
 /// Traverses a node's non-binary tree of child nodes.
 /// Creates a map in the form of a string of all encountered Table nodes and their children.
 /// 
 public static class TableStructurePrinter extends DocumentVisitor {
     public TableStructurePrinter() {
         mVisitedTables = new StringBuilder();
         mVisitorIsInsideTable = false;
     }

     public String getText() {
         return mVisitedTables.toString();
     }

     /// 
     /// Called when a Run node is encountered in the document.
     /// Runs that are not within tables are not recorded.
     /// 
     public int visitRun(Run run) {
         if (mVisitorIsInsideTable) indentAndAppendLine("[Run] \"" + run.getText() + "\"");

         return VisitorAction.CONTINUE;
     }

     /// 
     /// Called when a Table is encountered in the document.
     /// 
     public int visitTableStart(final Table table) {
         int rows = 0;
         int columns = 0;

         if (table.getRows().getCount() > 0) {
             rows = table.getRows().getCount();
             columns = table.getFirstRow().getCount();
         }

         indentAndAppendLine("[Table start] Size: " + rows + "x" + columns);
         mDocTraversalDepth++;
         mVisitorIsInsideTable = true;

         return VisitorAction.CONTINUE;
     }

     /// 
     /// Called after all the child nodes of a Table node have been visited.
     /// 
     public int visitTableEnd(final Table table) {
         mDocTraversalDepth--;
         indentAndAppendLine("[Table end]");
         mVisitorIsInsideTable = false;

         return VisitorAction.CONTINUE;
     }

     /// 
     /// Called when a Row node is encountered in the document.
     /// 
     public int visitRowStart(final Row row) {
         String rowContents = row.getText().replaceAll("\\u0007", ", ").replaceAll(", , ", "");
         int rowWidth = row.indexOf(row.getLastCell()) + 1;
         int rowIndex = row.getParentTable().indexOf(row);
         String rowStatusInTable = row.isFirstRow() && row.isLastRow() ? "only" : row.isFirstRow() ? "first" : row.isLastRow() ? "last" : "";
         if (!"".equals(rowStatusInTable)) {
             rowStatusInTable = MessageFormat.format(", the {0} row in this table,", rowStatusInTable);
         }

         indentAndAppendLine(MessageFormat.format("[Row start] Row #{0}{1} width {2}, \"{3}\"", ++rowIndex, rowStatusInTable, rowWidth, rowContents));
         mDocTraversalDepth++;

         return VisitorAction.CONTINUE;
     }

     /// 
     /// Called after all the child nodes of a Row node have been visited.
     /// 
     public int visitRowEnd(final Row row) {
         mDocTraversalDepth--;
         indentAndAppendLine("[Row end]");

         return VisitorAction.CONTINUE;
     }

     /// 
     /// Called when a Cell node is encountered in the document.
     /// 
     public int visitCellStart(final Cell cell) {
         Row row = cell.getParentRow();
         Table table = row.getParentTable();
         String cellStatusInRow = cell.isFirstCell() && cell.isLastCell() ? "only" : cell.isFirstCell() ? "first" : cell.isLastCell() ? "last" : "";
         if (!"".equals(cellStatusInRow)) {
             cellStatusInRow = MessageFormat.format(", the {0} cell in this row", cellStatusInRow);
         }

         indentAndAppendLine(MessageFormat.format("[Cell start] Row {0}, Col {1}{2}", table.indexOf(row) + 1, row.indexOf(cell) + 1, cellStatusInRow));
         mDocTraversalDepth++;

         return VisitorAction.CONTINUE;
     }

     /// 
     /// Called after all the child nodes of a Cell node have been visited.
     /// 
     public int visitCellEnd(final Cell cell) {
         mDocTraversalDepth--;
         indentAndAppendLine("[Cell end]");
         return VisitorAction.CONTINUE;
     }

     /// 
     /// Append a line to the StringBuilder, and indent it depending on how deep the visitor is
     /// into the current table's tree of child nodes.
     /// 
     /// 
     private void indentAndAppendLine(final String text) {
         for (int i = 0; i < mDocTraversalDepth; i++) {
             mVisitedTables.append("|  ");
         }

         mVisitedTables.append(text + "\r\n");
     }

     private boolean mVisitorIsInsideTable;
     private int mDocTraversalDepth;
     private final  StringBuilder mVisitedTables;
 }
 
```

Zeigt, wie man eine DocumentVisitor‑Implementierung verwendet, um allen versteckten Inhalt aus einem Dokument zu entfernen.

```

 public void removeHiddenContentFromDocument() throws Exception {
     Document doc = new Document(getMyDir() + "Hidden content.docx");
     RemoveHiddenContentVisitor hiddenContentRemover = new RemoveHiddenContentVisitor();

     // Below are three types of fields which can accept a document visitor,
     // which will allow it to visit the accepting node, and then traverse its child nodes in a depth-first manner.
     // 1 -  Paragraph node:
     Paragraph para = (Paragraph) doc.getChild(NodeType.PARAGRAPH, 4, true);
     para.accept(hiddenContentRemover);

     // 2 -  Table node:
     Table table = doc.getFirstSection().getBody().getTables().get(0);
     table.accept(hiddenContentRemover);

     // 3 -  Document node:
     doc.accept(hiddenContentRemover);

     doc.save(getArtifactsDir() + "Font.RemoveHiddenContentFromDocument.docx");
 }

 /// 
 /// Removes all visited nodes marked as "hidden content".
 /// 
 public static class RemoveHiddenContentVisitor extends DocumentVisitor {
     /// 
     /// Called when a FieldStart node is encountered in the document.
     /// 
     public int visitFieldStart(FieldStart fieldStart) {
         if (fieldStart.getFont().getHidden())
             fieldStart.remove();

         return VisitorAction.CONTINUE;
     }

     /// 
     /// Called when a FieldEnd node is encountered in the document.
     /// 
     public int visitFieldEnd(FieldEnd fieldEnd) {
         if (fieldEnd.getFont().getHidden())
             fieldEnd.remove();

         return VisitorAction.CONTINUE;
     }

     /// 
     /// Called when a FieldSeparator node is encountered in the document.
     /// 
     public int visitFieldSeparator(FieldSeparator fieldSeparator) {
         if (fieldSeparator.getFont().getHidden())
             fieldSeparator.remove();

         return VisitorAction.CONTINUE;
     }

     /// 
     /// Called when a Run node is encountered in the document.
     /// 
     public int visitRun(Run run) {
         if (run.getFont().getHidden())
             run.remove();

         return VisitorAction.CONTINUE;
     }

     /// 
     /// Called when a Paragraph node is encountered in the document.
     /// 
     public int visitParagraphStart(Paragraph paragraph) {
         if (paragraph.getParagraphBreakFont().getHidden())
             paragraph.remove();

         return VisitorAction.CONTINUE;
     }

     /// 
     /// Called when a FormField is encountered in the document.
     /// 
     public int visitFormField(FormField formField) {
         if (formField.getFont().getHidden())
             formField.remove();

         return VisitorAction.CONTINUE;
     }

     /// 
     /// Called when a GroupShape is encountered in the document.
     /// 
     public int visitGroupShapeStart(GroupShape groupShape) {
         if (groupShape.getFont().getHidden())
             groupShape.remove();

         return VisitorAction.CONTINUE;
     }

     /// 
     /// Called when a Shape is encountered in the document.
     /// 
     public int visitShapeStart(Shape shape) {
         if (shape.getFont().getHidden())
             shape.remove();

         return VisitorAction.CONTINUE;
     }

     /// 
     /// Called when a Comment is encountered in the document.
     /// 
     public int visitCommentStart(Comment comment) {
         if (comment.getFont().getHidden())
             comment.remove();

         return VisitorAction.CONTINUE;
     }

     /// 
     /// Called when a Footnote is encountered in the document.
     /// 
     public int visitFootnoteStart(Footnote footnote) {
         if (footnote.getFont().getHidden())
             footnote.remove();

         return VisitorAction.CONTINUE;
     }

     /// 
     /// Called when a SpecialCharacter is encountered in the document.
     /// 
     public int visitSpecialChar(SpecialChar specialChar) {
         if (specialChar.getFont().getHidden())
             specialChar.remove();

         return VisitorAction.CONTINUE;
     }

     /// 
     /// Called when visiting of a Table node is ended in the document.
     /// 
     public int visitTableEnd(Table table) {
         // The content inside table cells may have the hidden content flag, but the tables themselves cannot.
         // If this table had nothing but hidden content, this visitor would have removed all of it,
         // and there would be no child nodes left.
         // Thus, we can also treat the table itself as hidden content and remove it.
         // Tables which are empty but do not have hidden content will have cells with empty paragraphs inside,
         // which this visitor will not remove.
         if (!table.hasChildNodes())
             table.remove();

         return VisitorAction.CONTINUE;
     }

     /// 
     /// Called when visiting of a Cell node is ended in the document.
     /// 
     public int visitCellEnd(Cell cell) {
         if (!cell.hasChildNodes() && cell.getParentNode() != null)
             cell.remove();

         return VisitorAction.CONTINUE;
     }

     /// 
     /// Called when visiting of a Row node is ended in the document.
     /// 
     public int visitRowEnd(Row row) {
         if (!row.hasChildNodes() && row.getParentNode() != null)
             row.remove();

         return VisitorAction.CONTINUE;
     }
 }
 
```

**Parameters:**
| Parameter | Typ | Beschreibung |
| --- | --- | --- |
| cell | [Cell](../../com.aspose.words/cell/) | Das Objekt, das besucht wird. |

**Returns:**
int - Ein [VisitorAction](../../com.aspose.words/visitoraction/) Wert, der angibt, wie die Aufzählung fortgesetzt werden soll. Der zurückgegebene Wert ist einer der [VisitorAction](../../com.aspose.words/visitoraction/) Konstanten.
### visitCellStart(Cell cell) {#visitCellStart-com.aspose.words.Cell}
```
public int visitCellStart(Cell cell)
```


Wird aufgerufen, wenn die Aufzählung einer Tabellenzelle begonnen hat.

 **Examples:** 

Zeigt, wie man die Knotenstruktur jeder Tabelle in einem Dokument ausgibt.

```

 public void tableToText() throws Exception {
     Document doc = new Document(getMyDir() + "DocumentVisitor-compatible features.docx");
     TableStructurePrinter visitor = new TableStructurePrinter();

     // When we get a composite node to accept a document visitor, the visitor visits the accepting node,
     // and then traverses all the node's children in a depth-first manner.
     // The visitor can read and modify each visited node.
     doc.accept(visitor);

     System.out.println(visitor.getText());
 }

 /// 
 /// Traverses a node's non-binary tree of child nodes.
 /// Creates a map in the form of a string of all encountered Table nodes and their children.
 /// 
 public static class TableStructurePrinter extends DocumentVisitor {
     public TableStructurePrinter() {
         mVisitedTables = new StringBuilder();
         mVisitorIsInsideTable = false;
     }

     public String getText() {
         return mVisitedTables.toString();
     }

     /// 
     /// Called when a Run node is encountered in the document.
     /// Runs that are not within tables are not recorded.
     /// 
     public int visitRun(Run run) {
         if (mVisitorIsInsideTable) indentAndAppendLine("[Run] \"" + run.getText() + "\"");

         return VisitorAction.CONTINUE;
     }

     /// 
     /// Called when a Table is encountered in the document.
     /// 
     public int visitTableStart(final Table table) {
         int rows = 0;
         int columns = 0;

         if (table.getRows().getCount() > 0) {
             rows = table.getRows().getCount();
             columns = table.getFirstRow().getCount();
         }

         indentAndAppendLine("[Table start] Size: " + rows + "x" + columns);
         mDocTraversalDepth++;
         mVisitorIsInsideTable = true;

         return VisitorAction.CONTINUE;
     }

     /// 
     /// Called after all the child nodes of a Table node have been visited.
     /// 
     public int visitTableEnd(final Table table) {
         mDocTraversalDepth--;
         indentAndAppendLine("[Table end]");
         mVisitorIsInsideTable = false;

         return VisitorAction.CONTINUE;
     }

     /// 
     /// Called when a Row node is encountered in the document.
     /// 
     public int visitRowStart(final Row row) {
         String rowContents = row.getText().replaceAll("\\u0007", ", ").replaceAll(", , ", "");
         int rowWidth = row.indexOf(row.getLastCell()) + 1;
         int rowIndex = row.getParentTable().indexOf(row);
         String rowStatusInTable = row.isFirstRow() && row.isLastRow() ? "only" : row.isFirstRow() ? "first" : row.isLastRow() ? "last" : "";
         if (!"".equals(rowStatusInTable)) {
             rowStatusInTable = MessageFormat.format(", the {0} row in this table,", rowStatusInTable);
         }

         indentAndAppendLine(MessageFormat.format("[Row start] Row #{0}{1} width {2}, \"{3}\"", ++rowIndex, rowStatusInTable, rowWidth, rowContents));
         mDocTraversalDepth++;

         return VisitorAction.CONTINUE;
     }

     /// 
     /// Called after all the child nodes of a Row node have been visited.
     /// 
     public int visitRowEnd(final Row row) {
         mDocTraversalDepth--;
         indentAndAppendLine("[Row end]");

         return VisitorAction.CONTINUE;
     }

     /// 
     /// Called when a Cell node is encountered in the document.
     /// 
     public int visitCellStart(final Cell cell) {
         Row row = cell.getParentRow();
         Table table = row.getParentTable();
         String cellStatusInRow = cell.isFirstCell() && cell.isLastCell() ? "only" : cell.isFirstCell() ? "first" : cell.isLastCell() ? "last" : "";
         if (!"".equals(cellStatusInRow)) {
             cellStatusInRow = MessageFormat.format(", the {0} cell in this row", cellStatusInRow);
         }

         indentAndAppendLine(MessageFormat.format("[Cell start] Row {0}, Col {1}{2}", table.indexOf(row) + 1, row.indexOf(cell) + 1, cellStatusInRow));
         mDocTraversalDepth++;

         return VisitorAction.CONTINUE;
     }

     /// 
     /// Called after all the child nodes of a Cell node have been visited.
     /// 
     public int visitCellEnd(final Cell cell) {
         mDocTraversalDepth--;
         indentAndAppendLine("[Cell end]");
         return VisitorAction.CONTINUE;
     }

     /// 
     /// Append a line to the StringBuilder, and indent it depending on how deep the visitor is
     /// into the current table's tree of child nodes.
     /// 
     /// 
     private void indentAndAppendLine(final String text) {
         for (int i = 0; i < mDocTraversalDepth; i++) {
             mVisitedTables.append("|  ");
         }

         mVisitedTables.append(text + "\r\n");
     }

     private boolean mVisitorIsInsideTable;
     private int mDocTraversalDepth;
     private final  StringBuilder mVisitedTables;
 }
 
```

**Parameters:**
| Parameter | Typ | Beschreibung |
| --- | --- | --- |
| cell | [Cell](../../com.aspose.words/cell/) | Das Objekt, das besucht wird. |

**Returns:**
int - Ein [VisitorAction](../../com.aspose.words/visitoraction/) Wert, der angibt, wie die Aufzählung fortgesetzt werden soll. Der zurückgegebene Wert ist einer der [VisitorAction](../../com.aspose.words/visitoraction/) Konstanten.
### visitCommentEnd(Comment comment) {#visitCommentEnd-com.aspose.words.Comment}
```
public int visitCommentEnd(Comment comment)
```


Wird aufgerufen, wenn die Aufzählung eines Kommentartexts beendet ist.

 **Examples:** 

Zeigt, wie man die Knotenstruktur jedes Kommentars und Kommentarbereichs in einem Dokument ausgibt.

```

 public void commentsToText() throws Exception {
     Document doc = new Document(getMyDir() + "DocumentVisitor-compatible features.docx");
     CommentStructurePrinter visitor = new CommentStructurePrinter();

     // When we get a composite node to accept a document visitor, the visitor visits the accepting node,
     // and then traverses all the node's children in a depth-first manner.
     // The visitor can read and modify each visited node.
     doc.accept(visitor);

     System.out.println(visitor.getText());
 }

 /// 
 /// Traverses a node's non-binary tree of child nodes.
 /// Creates a map in the form of a string of all encountered Comment/CommentRange nodes and their children.
 /// 
 public static class CommentStructurePrinter extends DocumentVisitor {
     public CommentStructurePrinter() {
         mBuilder = new StringBuilder();
         mVisitorIsInsideComment = false;
     }

     public String getText() {
         return mBuilder.toString();
     }

     /// 
     /// Called when a Run node is encountered in the document.
     /// A Run is only recorded if it is a child of a Comment or CommentRange node.
     /// 
     public int visitRun(final Run run) {
         if (mVisitorIsInsideComment) {
             indentAndAppendLine("[Run] \"" + run.getText() + "\"");
         }

         return VisitorAction.CONTINUE;
     }

     /// 
     /// Called when a CommentRangeStart node is encountered in the document.
     /// 
     public int visitCommentRangeStart(final CommentRangeStart commentRangeStart) {
         indentAndAppendLine("[Comment range start] ID: " + commentRangeStart.getId());
         mDocTraversalDepth++;
         mVisitorIsInsideComment = true;

         return VisitorAction.CONTINUE;
     }

     /// 
     /// Called when a CommentRangeEnd node is encountered in the document.
     /// 
     public int visitCommentRangeEnd(final CommentRangeEnd commentRangeEnd) {
         mDocTraversalDepth--;
         indentAndAppendLine("[Comment range end]");
         mVisitorIsInsideComment = false;

         return VisitorAction.CONTINUE;
     }

     /// 
     /// Called when a Comment node is encountered in the document.
     /// 
     public int visitCommentStart(final Comment comment) {
         indentAndAppendLine(MessageFormat.format("[Comment start] For comment range ID {0}, By {1} on {2}", comment.getId(),
                 comment.getAuthor(), comment.getDateTime()));
         mDocTraversalDepth++;
         mVisitorIsInsideComment = true;

         return VisitorAction.CONTINUE;
     }

     /// 
     /// Called after all the child nodes of a Comment node have been visited.
     /// 
     public int visitCommentEnd(final Comment comment) {
         mDocTraversalDepth--;
         indentAndAppendLine("[Comment end]");
         mVisitorIsInsideComment = false;

         return VisitorAction.CONTINUE;
     }

     /// 
     /// Append a line to the StringBuilder, and indent it depending on how deep the visitor is
     /// into a comment/comment range's tree of child nodes.
     /// 
     /// 
     private void indentAndAppendLine(final String text) {
         for (int i = 0; i < mDocTraversalDepth; i++) {
             mBuilder.append("|  ");
         }

         mBuilder.append(text + "\r\n");
     }

     private boolean mVisitorIsInsideComment;
     private int mDocTraversalDepth;
     private final StringBuilder mBuilder;
 }
 
```

**Parameters:**
| Parameter | Typ | Beschreibung |
| --- | --- | --- |
| comment | [Comment](../../com.aspose.words/comment/) | Das Objekt, das besucht wird. |

**Returns:**
int - Ein [VisitorAction](../../com.aspose.words/visitoraction/) Wert, der angibt, wie die Aufzählung fortgesetzt werden soll. Der zurückgegebene Wert ist einer der [VisitorAction](../../com.aspose.words/visitoraction/) Konstanten.
### visitCommentRangeEnd(CommentRangeEnd commentRangeEnd) {#visitCommentRangeEnd-com.aspose.words.CommentRangeEnd}
```
public int visitCommentRangeEnd(CommentRangeEnd commentRangeEnd)
```


Wird aufgerufen, wenn das Ende eines kommentierten Textbereichs gefunden wird.

 **Examples:** 

Zeigt, wie man die Knotenstruktur jedes Kommentars und Kommentarbereichs in einem Dokument ausgibt.

```

 public void commentsToText() throws Exception {
     Document doc = new Document(getMyDir() + "DocumentVisitor-compatible features.docx");
     CommentStructurePrinter visitor = new CommentStructurePrinter();

     // When we get a composite node to accept a document visitor, the visitor visits the accepting node,
     // and then traverses all the node's children in a depth-first manner.
     // The visitor can read and modify each visited node.
     doc.accept(visitor);

     System.out.println(visitor.getText());
 }

 /// 
 /// Traverses a node's non-binary tree of child nodes.
 /// Creates a map in the form of a string of all encountered Comment/CommentRange nodes and their children.
 /// 
 public static class CommentStructurePrinter extends DocumentVisitor {
     public CommentStructurePrinter() {
         mBuilder = new StringBuilder();
         mVisitorIsInsideComment = false;
     }

     public String getText() {
         return mBuilder.toString();
     }

     /// 
     /// Called when a Run node is encountered in the document.
     /// A Run is only recorded if it is a child of a Comment or CommentRange node.
     /// 
     public int visitRun(final Run run) {
         if (mVisitorIsInsideComment) {
             indentAndAppendLine("[Run] \"" + run.getText() + "\"");
         }

         return VisitorAction.CONTINUE;
     }

     /// 
     /// Called when a CommentRangeStart node is encountered in the document.
     /// 
     public int visitCommentRangeStart(final CommentRangeStart commentRangeStart) {
         indentAndAppendLine("[Comment range start] ID: " + commentRangeStart.getId());
         mDocTraversalDepth++;
         mVisitorIsInsideComment = true;

         return VisitorAction.CONTINUE;
     }

     /// 
     /// Called when a CommentRangeEnd node is encountered in the document.
     /// 
     public int visitCommentRangeEnd(final CommentRangeEnd commentRangeEnd) {
         mDocTraversalDepth--;
         indentAndAppendLine("[Comment range end]");
         mVisitorIsInsideComment = false;

         return VisitorAction.CONTINUE;
     }

     /// 
     /// Called when a Comment node is encountered in the document.
     /// 
     public int visitCommentStart(final Comment comment) {
         indentAndAppendLine(MessageFormat.format("[Comment start] For comment range ID {0}, By {1} on {2}", comment.getId(),
                 comment.getAuthor(), comment.getDateTime()));
         mDocTraversalDepth++;
         mVisitorIsInsideComment = true;

         return VisitorAction.CONTINUE;
     }

     /// 
     /// Called after all the child nodes of a Comment node have been visited.
     /// 
     public int visitCommentEnd(final Comment comment) {
         mDocTraversalDepth--;
         indentAndAppendLine("[Comment end]");
         mVisitorIsInsideComment = false;

         return VisitorAction.CONTINUE;
     }

     /// 
     /// Append a line to the StringBuilder, and indent it depending on how deep the visitor is
     /// into a comment/comment range's tree of child nodes.
     /// 
     /// 
     private void indentAndAppendLine(final String text) {
         for (int i = 0; i < mDocTraversalDepth; i++) {
             mBuilder.append("|  ");
         }

         mBuilder.append(text + "\r\n");
     }

     private boolean mVisitorIsInsideComment;
     private int mDocTraversalDepth;
     private final StringBuilder mBuilder;
 }
 
```

**Parameters:**
| Parameter | Typ | Beschreibung |
| --- | --- | --- |
| commentRangeEnd | [CommentRangeEnd](../../com.aspose.words/commentrangeend/) | Das Objekt, das besucht wird. |

**Returns:**
int - Ein [VisitorAction](../../com.aspose.words/visitoraction/) Wert, der angibt, wie die Aufzählung fortgesetzt werden soll. Der zurückgegebene Wert ist einer der [VisitorAction](../../com.aspose.words/visitoraction/) Konstanten.
### visitCommentRangeStart(CommentRangeStart commentRangeStart) {#visitCommentRangeStart-com.aspose.words.CommentRangeStart}
```
public int visitCommentRangeStart(CommentRangeStart commentRangeStart)
```


Wird aufgerufen, wenn der Beginn eines kommentierten Textbereichs gefunden wird.

 **Examples:** 

Zeigt, wie man die Knotenstruktur jedes Kommentars und Kommentarbereichs in einem Dokument ausgibt.

```

 public void commentsToText() throws Exception {
     Document doc = new Document(getMyDir() + "DocumentVisitor-compatible features.docx");
     CommentStructurePrinter visitor = new CommentStructurePrinter();

     // When we get a composite node to accept a document visitor, the visitor visits the accepting node,
     // and then traverses all the node's children in a depth-first manner.
     // The visitor can read and modify each visited node.
     doc.accept(visitor);

     System.out.println(visitor.getText());
 }

 /// 
 /// Traverses a node's non-binary tree of child nodes.
 /// Creates a map in the form of a string of all encountered Comment/CommentRange nodes and their children.
 /// 
 public static class CommentStructurePrinter extends DocumentVisitor {
     public CommentStructurePrinter() {
         mBuilder = new StringBuilder();
         mVisitorIsInsideComment = false;
     }

     public String getText() {
         return mBuilder.toString();
     }

     /// 
     /// Called when a Run node is encountered in the document.
     /// A Run is only recorded if it is a child of a Comment or CommentRange node.
     /// 
     public int visitRun(final Run run) {
         if (mVisitorIsInsideComment) {
             indentAndAppendLine("[Run] \"" + run.getText() + "\"");
         }

         return VisitorAction.CONTINUE;
     }

     /// 
     /// Called when a CommentRangeStart node is encountered in the document.
     /// 
     public int visitCommentRangeStart(final CommentRangeStart commentRangeStart) {
         indentAndAppendLine("[Comment range start] ID: " + commentRangeStart.getId());
         mDocTraversalDepth++;
         mVisitorIsInsideComment = true;

         return VisitorAction.CONTINUE;
     }

     /// 
     /// Called when a CommentRangeEnd node is encountered in the document.
     /// 
     public int visitCommentRangeEnd(final CommentRangeEnd commentRangeEnd) {
         mDocTraversalDepth--;
         indentAndAppendLine("[Comment range end]");
         mVisitorIsInsideComment = false;

         return VisitorAction.CONTINUE;
     }

     /// 
     /// Called when a Comment node is encountered in the document.
     /// 
     public int visitCommentStart(final Comment comment) {
         indentAndAppendLine(MessageFormat.format("[Comment start] For comment range ID {0}, By {1} on {2}", comment.getId(),
                 comment.getAuthor(), comment.getDateTime()));
         mDocTraversalDepth++;
         mVisitorIsInsideComment = true;

         return VisitorAction.CONTINUE;
     }

     /// 
     /// Called after all the child nodes of a Comment node have been visited.
     /// 
     public int visitCommentEnd(final Comment comment) {
         mDocTraversalDepth--;
         indentAndAppendLine("[Comment end]");
         mVisitorIsInsideComment = false;

         return VisitorAction.CONTINUE;
     }

     /// 
     /// Append a line to the StringBuilder, and indent it depending on how deep the visitor is
     /// into a comment/comment range's tree of child nodes.
     /// 
     /// 
     private void indentAndAppendLine(final String text) {
         for (int i = 0; i < mDocTraversalDepth; i++) {
             mBuilder.append("|  ");
         }

         mBuilder.append(text + "\r\n");
     }

     private boolean mVisitorIsInsideComment;
     private int mDocTraversalDepth;
     private final StringBuilder mBuilder;
 }
 
```

**Parameters:**
| Parameter | Typ | Beschreibung |
| --- | --- | --- |
| commentRangeStart | [CommentRangeStart](../../com.aspose.words/commentrangestart/) | Das Objekt, das besucht wird. |

**Returns:**
int - Ein [VisitorAction](../../com.aspose.words/visitoraction/) Wert, der angibt, wie die Aufzählung fortgesetzt werden soll. Der zurückgegebene Wert ist einer der [VisitorAction](../../com.aspose.words/visitoraction/) Konstanten.
### visitCommentStart(Comment comment) {#visitCommentStart-com.aspose.words.Comment}
```
public int visitCommentStart(Comment comment)
```


Wird aufgerufen, wenn die Aufzählung eines Kommentartexts begonnen hat.

 **Examples:** 

Zeigt, wie man die Knotenstruktur jedes Kommentars und Kommentarbereichs in einem Dokument ausgibt.

```

 public void commentsToText() throws Exception {
     Document doc = new Document(getMyDir() + "DocumentVisitor-compatible features.docx");
     CommentStructurePrinter visitor = new CommentStructurePrinter();

     // When we get a composite node to accept a document visitor, the visitor visits the accepting node,
     // and then traverses all the node's children in a depth-first manner.
     // The visitor can read and modify each visited node.
     doc.accept(visitor);

     System.out.println(visitor.getText());
 }

 /// 
 /// Traverses a node's non-binary tree of child nodes.
 /// Creates a map in the form of a string of all encountered Comment/CommentRange nodes and their children.
 /// 
 public static class CommentStructurePrinter extends DocumentVisitor {
     public CommentStructurePrinter() {
         mBuilder = new StringBuilder();
         mVisitorIsInsideComment = false;
     }

     public String getText() {
         return mBuilder.toString();
     }

     /// 
     /// Called when a Run node is encountered in the document.
     /// A Run is only recorded if it is a child of a Comment or CommentRange node.
     /// 
     public int visitRun(final Run run) {
         if (mVisitorIsInsideComment) {
             indentAndAppendLine("[Run] \"" + run.getText() + "\"");
         }

         return VisitorAction.CONTINUE;
     }

     /// 
     /// Called when a CommentRangeStart node is encountered in the document.
     /// 
     public int visitCommentRangeStart(final CommentRangeStart commentRangeStart) {
         indentAndAppendLine("[Comment range start] ID: " + commentRangeStart.getId());
         mDocTraversalDepth++;
         mVisitorIsInsideComment = true;

         return VisitorAction.CONTINUE;
     }

     /// 
     /// Called when a CommentRangeEnd node is encountered in the document.
     /// 
     public int visitCommentRangeEnd(final CommentRangeEnd commentRangeEnd) {
         mDocTraversalDepth--;
         indentAndAppendLine("[Comment range end]");
         mVisitorIsInsideComment = false;

         return VisitorAction.CONTINUE;
     }

     /// 
     /// Called when a Comment node is encountered in the document.
     /// 
     public int visitCommentStart(final Comment comment) {
         indentAndAppendLine(MessageFormat.format("[Comment start] For comment range ID {0}, By {1} on {2}", comment.getId(),
                 comment.getAuthor(), comment.getDateTime()));
         mDocTraversalDepth++;
         mVisitorIsInsideComment = true;

         return VisitorAction.CONTINUE;
     }

     /// 
     /// Called after all the child nodes of a Comment node have been visited.
     /// 
     public int visitCommentEnd(final Comment comment) {
         mDocTraversalDepth--;
         indentAndAppendLine("[Comment end]");
         mVisitorIsInsideComment = false;

         return VisitorAction.CONTINUE;
     }

     /// 
     /// Append a line to the StringBuilder, and indent it depending on how deep the visitor is
     /// into a comment/comment range's tree of child nodes.
     /// 
     /// 
     private void indentAndAppendLine(final String text) {
         for (int i = 0; i < mDocTraversalDepth; i++) {
             mBuilder.append("|  ");
         }

         mBuilder.append(text + "\r\n");
     }

     private boolean mVisitorIsInsideComment;
     private int mDocTraversalDepth;
     private final StringBuilder mBuilder;
 }
 
```

Zeigt, wie man eine DocumentVisitor‑Implementierung verwendet, um allen versteckten Inhalt aus einem Dokument zu entfernen.

```

 public void removeHiddenContentFromDocument() throws Exception {
     Document doc = new Document(getMyDir() + "Hidden content.docx");
     RemoveHiddenContentVisitor hiddenContentRemover = new RemoveHiddenContentVisitor();

     // Below are three types of fields which can accept a document visitor,
     // which will allow it to visit the accepting node, and then traverse its child nodes in a depth-first manner.
     // 1 -  Paragraph node:
     Paragraph para = (Paragraph) doc.getChild(NodeType.PARAGRAPH, 4, true);
     para.accept(hiddenContentRemover);

     // 2 -  Table node:
     Table table = doc.getFirstSection().getBody().getTables().get(0);
     table.accept(hiddenContentRemover);

     // 3 -  Document node:
     doc.accept(hiddenContentRemover);

     doc.save(getArtifactsDir() + "Font.RemoveHiddenContentFromDocument.docx");
 }

 /// 
 /// Removes all visited nodes marked as "hidden content".
 /// 
 public static class RemoveHiddenContentVisitor extends DocumentVisitor {
     /// 
     /// Called when a FieldStart node is encountered in the document.
     /// 
     public int visitFieldStart(FieldStart fieldStart) {
         if (fieldStart.getFont().getHidden())
             fieldStart.remove();

         return VisitorAction.CONTINUE;
     }

     /// 
     /// Called when a FieldEnd node is encountered in the document.
     /// 
     public int visitFieldEnd(FieldEnd fieldEnd) {
         if (fieldEnd.getFont().getHidden())
             fieldEnd.remove();

         return VisitorAction.CONTINUE;
     }

     /// 
     /// Called when a FieldSeparator node is encountered in the document.
     /// 
     public int visitFieldSeparator(FieldSeparator fieldSeparator) {
         if (fieldSeparator.getFont().getHidden())
             fieldSeparator.remove();

         return VisitorAction.CONTINUE;
     }

     /// 
     /// Called when a Run node is encountered in the document.
     /// 
     public int visitRun(Run run) {
         if (run.getFont().getHidden())
             run.remove();

         return VisitorAction.CONTINUE;
     }

     /// 
     /// Called when a Paragraph node is encountered in the document.
     /// 
     public int visitParagraphStart(Paragraph paragraph) {
         if (paragraph.getParagraphBreakFont().getHidden())
             paragraph.remove();

         return VisitorAction.CONTINUE;
     }

     /// 
     /// Called when a FormField is encountered in the document.
     /// 
     public int visitFormField(FormField formField) {
         if (formField.getFont().getHidden())
             formField.remove();

         return VisitorAction.CONTINUE;
     }

     /// 
     /// Called when a GroupShape is encountered in the document.
     /// 
     public int visitGroupShapeStart(GroupShape groupShape) {
         if (groupShape.getFont().getHidden())
             groupShape.remove();

         return VisitorAction.CONTINUE;
     }

     /// 
     /// Called when a Shape is encountered in the document.
     /// 
     public int visitShapeStart(Shape shape) {
         if (shape.getFont().getHidden())
             shape.remove();

         return VisitorAction.CONTINUE;
     }

     /// 
     /// Called when a Comment is encountered in the document.
     /// 
     public int visitCommentStart(Comment comment) {
         if (comment.getFont().getHidden())
             comment.remove();

         return VisitorAction.CONTINUE;
     }

     /// 
     /// Called when a Footnote is encountered in the document.
     /// 
     public int visitFootnoteStart(Footnote footnote) {
         if (footnote.getFont().getHidden())
             footnote.remove();

         return VisitorAction.CONTINUE;
     }

     /// 
     /// Called when a SpecialCharacter is encountered in the document.
     /// 
     public int visitSpecialChar(SpecialChar specialChar) {
         if (specialChar.getFont().getHidden())
             specialChar.remove();

         return VisitorAction.CONTINUE;
     }

     /// 
     /// Called when visiting of a Table node is ended in the document.
     /// 
     public int visitTableEnd(Table table) {
         // The content inside table cells may have the hidden content flag, but the tables themselves cannot.
         // If this table had nothing but hidden content, this visitor would have removed all of it,
         // and there would be no child nodes left.
         // Thus, we can also treat the table itself as hidden content and remove it.
         // Tables which are empty but do not have hidden content will have cells with empty paragraphs inside,
         // which this visitor will not remove.
         if (!table.hasChildNodes())
             table.remove();

         return VisitorAction.CONTINUE;
     }

     /// 
     /// Called when visiting of a Cell node is ended in the document.
     /// 
     public int visitCellEnd(Cell cell) {
         if (!cell.hasChildNodes() && cell.getParentNode() != null)
             cell.remove();

         return VisitorAction.CONTINUE;
     }

     /// 
     /// Called when visiting of a Row node is ended in the document.
     /// 
     public int visitRowEnd(Row row) {
         if (!row.hasChildNodes() && row.getParentNode() != null)
             row.remove();

         return VisitorAction.CONTINUE;
     }
 }
 
```

**Parameters:**
| Parameter | Typ | Beschreibung |
| --- | --- | --- |
| comment | [Comment](../../com.aspose.words/comment/) | Das Objekt, das besucht wird. |

**Returns:**
int - Ein [VisitorAction](../../com.aspose.words/visitoraction/) Wert, der angibt, wie die Aufzählung fortgesetzt werden soll. Der zurückgegebene Wert ist einer der [VisitorAction](../../com.aspose.words/visitoraction/) Konstanten.
### visitDocumentEnd(Document doc) {#visitDocumentEnd-com.aspose.words.Document}
```
public int visitDocumentEnd(Document doc)
```


Aufgerufen, wenn die Aufzählung des Dokuments abgeschlossen ist.

 **Examples:** 

Zeigt, wie ein DocumentVisitor verwendet wird, um die Knotenstruktur eines Dokuments auszugeben.

```

 public void docStructureToText() throws Exception {
     Document doc = new Document(getMyDir() + "DocumentVisitor-compatible features.docx");
     DocStructurePrinter visitor = new DocStructurePrinter();

     // When we get a composite node to accept a document visitor, the visitor visits the accepting node,
     // and then traverses all the node's children in a depth-first manner.
     // The visitor can read and modify each visited node.
     doc.accept(visitor);

     System.out.println(visitor.getText());
 }

 /// 
 /// Traverses a node's tree of child nodes.
 /// Creates a map of this tree in the form of a string.
 /// 
 public static class DocStructurePrinter extends DocumentVisitor {
     public DocStructurePrinter() {
         mAcceptingNodeChildTree = new StringBuilder();
     }

     public String getText() {
         return mAcceptingNodeChildTree.toString();
     }

     /// 
     /// Called when a Document node is encountered.
     /// 
     public int visitDocumentStart(Document doc) {
         int childNodeCount = doc.getChildNodes(NodeType.ANY, true).getCount();

         indentAndAppendLine("[Document start] Child nodes: " + childNodeCount);
         mDocTraversalDepth++;

         // Allow the visitor to continue visiting other nodes.
         return VisitorAction.CONTINUE;
     }

     /// 
     /// Called after all the child nodes of a Document node have been visited.
     /// 
     public int visitDocumentEnd(Document doc) {
         mDocTraversalDepth--;
         indentAndAppendLine("[Document end]");

         return VisitorAction.CONTINUE;
     }

     /// 
     /// Called when a Section node is encountered in the document.
     /// 
     public int visitSectionStart(final Section section) {
         // Get the index of our section within the document
         NodeCollection docSections = section.getDocument().getChildNodes(NodeType.SECTION, false);
         int sectionIndex = docSections.indexOf(section);

         indentAndAppendLine("[Section start] Section index: " + sectionIndex);
         mDocTraversalDepth++;

         return VisitorAction.CONTINUE;
     }

     /// 
     /// Called after all the child nodes of a Section node have been visited.
     /// 
     public int visitSectionEnd(final Section section) {
         mDocTraversalDepth--;
         indentAndAppendLine("[Section end]");

         return VisitorAction.CONTINUE;
     }

     /// 
     /// Called when a Body node is encountered in the document.
     /// 
     public int visitBodyStart(final Body body) {
         int paragraphCount = body.getParagraphs().getCount();
         indentAndAppendLine("[Body start] Paragraphs: " + paragraphCount);
         mDocTraversalDepth++;

         return VisitorAction.CONTINUE;
     }

     /// 
     /// Called after all the child nodes of a Body node have been visited.
     /// 
     public int visitBodyEnd(final Body body) {
         mDocTraversalDepth--;
         indentAndAppendLine("[Body end]");

         return VisitorAction.CONTINUE;
     }

     /// 
     /// Called when a Paragraph node is encountered in the document.
     /// 
     public int visitParagraphStart(final Paragraph paragraph) {
         indentAndAppendLine("[Paragraph start]");
         mDocTraversalDepth++;

         return VisitorAction.CONTINUE;
     }

     /// 
     /// Called after all the child nodes of a Paragraph node have been visited.
     /// 
     public int visitParagraphEnd(final Paragraph paragraph) {
         mDocTraversalDepth--;
         indentAndAppendLine("[Paragraph end]");

         return VisitorAction.CONTINUE;
     }

     /// 
     /// Called when a Run node is encountered in the document.
     /// 
     public int visitRun(final Run run) {
         indentAndAppendLine("[Run] \"" + run.getText() + "\"");

         return VisitorAction.CONTINUE;
     }

     /// 
     /// Called when a SubDocument node is encountered in the document.
     /// 
     public int visitSubDocument(final SubDocument subDocument) {
         indentAndAppendLine("[SubDocument]");

         return VisitorAction.CONTINUE;
     }

     /// 
     /// Called when a SubDocument node is encountered in the document.
     /// 
     public int visitStructuredDocumentTagRangeStart(StructuredDocumentTagRangeStart sdtRangeStart)
     {
         indentAndAppendLine("[SdtRangeStart]");

         return VisitorAction.CONTINUE;
     }

     /// 
     /// Called when a SubDocument node is encountered in the document.
     /// 
     public int visitStructuredDocumentTagRangeEnd(StructuredDocumentTagRangeEnd sdtRangeEnd)
     {
         indentAndAppendLine("[SdtRangeEnd]");

         return VisitorAction.CONTINUE;
     }

     /// 
     /// Append a line to the StringBuilder and indent it depending on how deep the visitor is into the document tree.
     /// 
     /// 
     private void indentAndAppendLine(final String text) {
         for (int i = 0; i < mDocTraversalDepth; i++) {
             mAcceptingNodeChildTree.append("|  ");
         }

         mAcceptingNodeChildTree.append(text + "\r\n");
     }

     private int mDocTraversalDepth;
     private final StringBuilder mAcceptingNodeChildTree;
 }
 
```

**Parameters:**
| Parameter | Typ | Beschreibung |
| --- | --- | --- |
| doc | [Document](../../com.aspose.words/document/) | Das Objekt, das besucht wird. |

**Returns:**
int - Ein [VisitorAction](../../com.aspose.words/visitoraction/) Wert, der angibt, wie die Aufzählung fortgesetzt werden soll. Der zurückgegebene Wert ist einer der [VisitorAction](../../com.aspose.words/visitoraction/) Konstanten.
### visitDocumentStart(Document doc) {#visitDocumentStart-com.aspose.words.Document}
```
public int visitDocumentStart(Document doc)
```


Aufgerufen, wenn die Aufzählung des Dokuments begonnen hat.

 **Examples:** 

Zeigt, wie ein DocumentVisitor verwendet wird, um die Knotenstruktur eines Dokuments auszugeben.

```

 public void docStructureToText() throws Exception {
     Document doc = new Document(getMyDir() + "DocumentVisitor-compatible features.docx");
     DocStructurePrinter visitor = new DocStructurePrinter();

     // When we get a composite node to accept a document visitor, the visitor visits the accepting node,
     // and then traverses all the node's children in a depth-first manner.
     // The visitor can read and modify each visited node.
     doc.accept(visitor);

     System.out.println(visitor.getText());
 }

 /// 
 /// Traverses a node's tree of child nodes.
 /// Creates a map of this tree in the form of a string.
 /// 
 public static class DocStructurePrinter extends DocumentVisitor {
     public DocStructurePrinter() {
         mAcceptingNodeChildTree = new StringBuilder();
     }

     public String getText() {
         return mAcceptingNodeChildTree.toString();
     }

     /// 
     /// Called when a Document node is encountered.
     /// 
     public int visitDocumentStart(Document doc) {
         int childNodeCount = doc.getChildNodes(NodeType.ANY, true).getCount();

         indentAndAppendLine("[Document start] Child nodes: " + childNodeCount);
         mDocTraversalDepth++;

         // Allow the visitor to continue visiting other nodes.
         return VisitorAction.CONTINUE;
     }

     /// 
     /// Called after all the child nodes of a Document node have been visited.
     /// 
     public int visitDocumentEnd(Document doc) {
         mDocTraversalDepth--;
         indentAndAppendLine("[Document end]");

         return VisitorAction.CONTINUE;
     }

     /// 
     /// Called when a Section node is encountered in the document.
     /// 
     public int visitSectionStart(final Section section) {
         // Get the index of our section within the document
         NodeCollection docSections = section.getDocument().getChildNodes(NodeType.SECTION, false);
         int sectionIndex = docSections.indexOf(section);

         indentAndAppendLine("[Section start] Section index: " + sectionIndex);
         mDocTraversalDepth++;

         return VisitorAction.CONTINUE;
     }

     /// 
     /// Called after all the child nodes of a Section node have been visited.
     /// 
     public int visitSectionEnd(final Section section) {
         mDocTraversalDepth--;
         indentAndAppendLine("[Section end]");

         return VisitorAction.CONTINUE;
     }

     /// 
     /// Called when a Body node is encountered in the document.
     /// 
     public int visitBodyStart(final Body body) {
         int paragraphCount = body.getParagraphs().getCount();
         indentAndAppendLine("[Body start] Paragraphs: " + paragraphCount);
         mDocTraversalDepth++;

         return VisitorAction.CONTINUE;
     }

     /// 
     /// Called after all the child nodes of a Body node have been visited.
     /// 
     public int visitBodyEnd(final Body body) {
         mDocTraversalDepth--;
         indentAndAppendLine("[Body end]");

         return VisitorAction.CONTINUE;
     }

     /// 
     /// Called when a Paragraph node is encountered in the document.
     /// 
     public int visitParagraphStart(final Paragraph paragraph) {
         indentAndAppendLine("[Paragraph start]");
         mDocTraversalDepth++;

         return VisitorAction.CONTINUE;
     }

     /// 
     /// Called after all the child nodes of a Paragraph node have been visited.
     /// 
     public int visitParagraphEnd(final Paragraph paragraph) {
         mDocTraversalDepth--;
         indentAndAppendLine("[Paragraph end]");

         return VisitorAction.CONTINUE;
     }

     /// 
     /// Called when a Run node is encountered in the document.
     /// 
     public int visitRun(final Run run) {
         indentAndAppendLine("[Run] \"" + run.getText() + "\"");

         return VisitorAction.CONTINUE;
     }

     /// 
     /// Called when a SubDocument node is encountered in the document.
     /// 
     public int visitSubDocument(final SubDocument subDocument) {
         indentAndAppendLine("[SubDocument]");

         return VisitorAction.CONTINUE;
     }

     /// 
     /// Called when a SubDocument node is encountered in the document.
     /// 
     public int visitStructuredDocumentTagRangeStart(StructuredDocumentTagRangeStart sdtRangeStart)
     {
         indentAndAppendLine("[SdtRangeStart]");

         return VisitorAction.CONTINUE;
     }

     /// 
     /// Called when a SubDocument node is encountered in the document.
     /// 
     public int visitStructuredDocumentTagRangeEnd(StructuredDocumentTagRangeEnd sdtRangeEnd)
     {
         indentAndAppendLine("[SdtRangeEnd]");

         return VisitorAction.CONTINUE;
     }

     /// 
     /// Append a line to the StringBuilder and indent it depending on how deep the visitor is into the document tree.
     /// 
     /// 
     private void indentAndAppendLine(final String text) {
         for (int i = 0; i < mDocTraversalDepth; i++) {
             mAcceptingNodeChildTree.append("|  ");
         }

         mAcceptingNodeChildTree.append(text + "\r\n");
     }

     private int mDocTraversalDepth;
     private final StringBuilder mAcceptingNodeChildTree;
 }
 
```

**Parameters:**
| Parameter | Typ | Beschreibung |
| --- | --- | --- |
| doc | [Document](../../com.aspose.words/document/) | Das Objekt, das besucht wird. |

**Returns:**
int - Ein [VisitorAction](../../com.aspose.words/visitoraction/) Wert, der angibt, wie die Aufzählung fortgesetzt werden soll. Der zurückgegebene Wert ist einer der [VisitorAction](../../com.aspose.words/visitoraction/) Konstanten.
### visitEditableRangeEnd(EditableRangeEnd editableRangeEnd) {#visitEditableRangeEnd-com.aspose.words.EditableRangeEnd}
```
public int visitEditableRangeEnd(EditableRangeEnd editableRangeEnd)
```


Aufgerufen, wenn das Ende eines bearbeitbaren Bereichs im Dokument gefunden wird.

 **Examples:** 

Zeigt, wie man die Knotenstruktur jedes bearbeitbaren Bereichs in einem Dokument ausgibt.

```

 public void editableRangeToText() throws Exception {
     Document doc = new Document(getMyDir() + "DocumentVisitor-compatible features.docx");
     EditableRangeStructurePrinter visitor = new EditableRangeStructurePrinter();

     // When we get a composite node to accept a document visitor, the visitor visits the accepting node,
     // and then traverses all the node's children in a depth-first manner.
     // The visitor can read and modify each visited node.
     doc.accept(visitor);

     System.out.println(visitor.getText());
 }

 /// 
 /// Traverses a node's non-binary tree of child nodes.
 /// Creates a map in the form of a string of all encountered EditableRange nodes and their children.
 /// 
 public static class EditableRangeStructurePrinter extends DocumentVisitor {
     public EditableRangeStructurePrinter() {
         mBuilder = new StringBuilder();
         mVisitorIsInsideEditableRange = false;
     }

     /// 
     /// Gets the plain text of the document that was accumulated by the visitor.
     /// 
     public String getText() {
         return mBuilder.toString();
     }

     /// 
     /// Called when a Run node is encountered in the document.
     /// 
     public int visitRun(final Run run) {
         // We want to print the contents of runs, but only if they are inside shapes, as they would be in the case of text boxes.
         if (mVisitorIsInsideEditableRange) {
             indentAndAppendLine("[Run] \"" + run.getText() + "\"");
         }

         return VisitorAction.CONTINUE;
     }

     /// 
     /// Called when an EditableRange node is encountered in the document.
     /// 
     public int visitEditableRangeStart(final EditableRangeStart editableRangeStart) {
         indentAndAppendLine("[EditableRange start] ID: " + editableRangeStart.getId() + " Owner: "
                 + editableRangeStart.getEditableRange().getSingleUser());
         mDocTraversalDepth++;
         mVisitorIsInsideEditableRange = true;

         return VisitorAction.CONTINUE;
     }

     /// 
     /// Called when the visiting of a EditableRange node is ended.
     /// 
     public int visitEditableRangeEnd(final EditableRangeEnd editableRangeEnd) {
         mDocTraversalDepth--;
         indentAndAppendLine("[EditableRange end]");
         mVisitorIsInsideEditableRange = false;

         return VisitorAction.CONTINUE;
     }

     /// 
     /// Append a line to the StringBuilder and indent it depending on how deep the visitor is into the document tree.
     /// 
     /// 
     private void indentAndAppendLine(final String text) {
         for (int i = 0; i < mDocTraversalDepth; i++) {
             mBuilder.append("|  ");
         }

         mBuilder.append(text + "\r\n");
     }

     private boolean mVisitorIsInsideEditableRange;
     private int mDocTraversalDepth;
     private final StringBuilder mBuilder;
 }
 
```

**Parameters:**
| Parameter | Typ | Beschreibung |
| --- | --- | --- |
| editableRangeEnd | [EditableRangeEnd](../../com.aspose.words/editablerangeend/) | Das Objekt, das besucht wird. |

**Returns:**
int - Ein [VisitorAction](../../com.aspose.words/visitoraction/) Wert, der angibt, wie die Aufzählung fortgesetzt werden soll. Der zurückgegebene Wert ist einer der [VisitorAction](../../com.aspose.words/visitoraction/) Konstanten.
### visitEditableRangeStart(EditableRangeStart editableRangeStart) {#visitEditableRangeStart-com.aspose.words.EditableRangeStart}
```
public int visitEditableRangeStart(EditableRangeStart editableRangeStart)
```


Aufgerufen, wenn der Beginn eines bearbeitbaren Bereichs im Dokument gefunden wird.

 **Examples:** 

Zeigt, wie man die Knotenstruktur jedes bearbeitbaren Bereichs in einem Dokument ausgibt.

```

 public void editableRangeToText() throws Exception {
     Document doc = new Document(getMyDir() + "DocumentVisitor-compatible features.docx");
     EditableRangeStructurePrinter visitor = new EditableRangeStructurePrinter();

     // When we get a composite node to accept a document visitor, the visitor visits the accepting node,
     // and then traverses all the node's children in a depth-first manner.
     // The visitor can read and modify each visited node.
     doc.accept(visitor);

     System.out.println(visitor.getText());
 }

 /// 
 /// Traverses a node's non-binary tree of child nodes.
 /// Creates a map in the form of a string of all encountered EditableRange nodes and their children.
 /// 
 public static class EditableRangeStructurePrinter extends DocumentVisitor {
     public EditableRangeStructurePrinter() {
         mBuilder = new StringBuilder();
         mVisitorIsInsideEditableRange = false;
     }

     /// 
     /// Gets the plain text of the document that was accumulated by the visitor.
     /// 
     public String getText() {
         return mBuilder.toString();
     }

     /// 
     /// Called when a Run node is encountered in the document.
     /// 
     public int visitRun(final Run run) {
         // We want to print the contents of runs, but only if they are inside shapes, as they would be in the case of text boxes.
         if (mVisitorIsInsideEditableRange) {
             indentAndAppendLine("[Run] \"" + run.getText() + "\"");
         }

         return VisitorAction.CONTINUE;
     }

     /// 
     /// Called when an EditableRange node is encountered in the document.
     /// 
     public int visitEditableRangeStart(final EditableRangeStart editableRangeStart) {
         indentAndAppendLine("[EditableRange start] ID: " + editableRangeStart.getId() + " Owner: "
                 + editableRangeStart.getEditableRange().getSingleUser());
         mDocTraversalDepth++;
         mVisitorIsInsideEditableRange = true;

         return VisitorAction.CONTINUE;
     }

     /// 
     /// Called when the visiting of a EditableRange node is ended.
     /// 
     public int visitEditableRangeEnd(final EditableRangeEnd editableRangeEnd) {
         mDocTraversalDepth--;
         indentAndAppendLine("[EditableRange end]");
         mVisitorIsInsideEditableRange = false;

         return VisitorAction.CONTINUE;
     }

     /// 
     /// Append a line to the StringBuilder and indent it depending on how deep the visitor is into the document tree.
     /// 
     /// 
     private void indentAndAppendLine(final String text) {
         for (int i = 0; i < mDocTraversalDepth; i++) {
             mBuilder.append("|  ");
         }

         mBuilder.append(text + "\r\n");
     }

     private boolean mVisitorIsInsideEditableRange;
     private int mDocTraversalDepth;
     private final StringBuilder mBuilder;
 }
 
```

**Parameters:**
| Parameter | Typ | Beschreibung |
| --- | --- | --- |
| editableRangeStart | [EditableRangeStart](../../com.aspose.words/editablerangestart/) | Das Objekt, das besucht wird. |

**Returns:**
int - Ein [VisitorAction](../../com.aspose.words/visitoraction/) Wert, der angibt, wie die Aufzählung fortgesetzt werden soll. Der zurückgegebene Wert ist einer der [VisitorAction](../../com.aspose.words/visitoraction/) Konstanten.
### visitFieldEnd(FieldEnd fieldEnd) {#visitFieldEnd-com.aspose.words.FieldEnd}
```
public int visitFieldEnd(FieldEnd fieldEnd)
```


Aufgerufen, wenn ein Feld im Dokument endet.

 **Remarks:** 

Weitere Informationen finden Sie unter [visitFieldStart(com.aspose.words.FieldStart)](../../com.aspose.words/documentvisitor/\#visitFieldStart-com.aspose.words.FieldStart).

 **Examples:** 

Zeigt, wie man die Knotenstruktur jedes Feldes in einem Dokument ausgibt.

```

 public void fieldToText() throws Exception {
     Document doc = new Document(getMyDir() + "DocumentVisitor-compatible features.docx");
     FieldStructurePrinter visitor = new FieldStructurePrinter();

     // When we get a composite node to accept a document visitor, the visitor visits the accepting node,
     // and then traverses all the node's children in a depth-first manner.
     // The visitor can read and modify each visited node.
     doc.accept(visitor);

     System.out.println(visitor.getText());
 }

 /// 
 /// Traverses a node's non-binary tree of child nodes.
 /// Creates a map in the form of a string of all encountered Field nodes and their children.
 /// 
 public static class FieldStructurePrinter extends DocumentVisitor {
     public FieldStructurePrinter() {
         mBuilder = new StringBuilder();
         mVisitorIsInsideField = false;
     }

     public String getText() {
         return mBuilder.toString();
     }

     /// 
     /// Called when a Run node is encountered in the document.
     /// 
     public int visitRun(final Run run) {
         if (mVisitorIsInsideField) {
             indentAndAppendLine("[Run] \"" + run.getText() + "\"");
         }

         return VisitorAction.CONTINUE;
     }

     /// 
     /// Called when a FieldStart node is encountered in the document.
     /// 
     public int visitFieldStart(final FieldStart fieldStart) {
         indentAndAppendLine("[Field start] FieldType: " + fieldStart.getFieldType());
         mDocTraversalDepth++;
         mVisitorIsInsideField = true;

         return VisitorAction.CONTINUE;
     }

     /// 
     /// Called when a FieldEnd node is encountered in the document.
     /// 
     public int visitFieldEnd(final FieldEnd fieldEnd) {
         mDocTraversalDepth--;
         indentAndAppendLine("[Field end]");
         mVisitorIsInsideField = false;

         return VisitorAction.CONTINUE;
     }

     /// 
     /// Called when a FieldSeparator node is encountered in the document.
     /// 
     public int visitFieldSeparator(final FieldSeparator fieldSeparator) {
         indentAndAppendLine("[FieldSeparator]");

         return VisitorAction.CONTINUE;
     }

     /// 
     /// Append a line to the StringBuilder, and indent it depending on how deep the visitor is
     /// into the field's tree of child nodes.
     /// 
     /// 
     private void indentAndAppendLine(final String text) {
         for (int i = 0; i < mDocTraversalDepth; i++) {
             mBuilder.append("|  ");
         }

         mBuilder.append(text + "\r\n");
     }

     private boolean mVisitorIsInsideField;
     private int mDocTraversalDepth;
     private final StringBuilder mBuilder;
 }
 
```

**Parameters:**
| Parameter | Typ | Beschreibung |
| --- | --- | --- |
| fieldEnd | [FieldEnd](../../com.aspose.words/fieldend/) | Das Objekt, das besucht wird. |

**Returns:**
int - Ein [VisitorAction](../../com.aspose.words/visitoraction/) Wert, der angibt, wie die Aufzählung fortgesetzt werden soll. Der zurückgegebene Wert ist einer der [VisitorAction](../../com.aspose.words/visitoraction/) Konstanten.
### visitFieldSeparator(FieldSeparator fieldSeparator) {#visitFieldSeparator-com.aspose.words.FieldSeparator}
```
public int visitFieldSeparator(FieldSeparator fieldSeparator)
```


Aufgerufen, wenn ein Feldtrennzeichen im Dokument gefunden wird.

 **Remarks:** 

Der Feldtrennzeichen trennt den Feldcode vom Feldwert im Dokument. Beachten Sie, dass einige Felder nur einen Feldcode haben und kein Feldtrennzeichen und keinen Feldwert besitzen.

Weitere Informationen finden Sie unter [visitFieldStart(com.aspose.words.FieldStart)](../../com.aspose.words/documentvisitor/\#visitFieldStart-com.aspose.words.FieldStart).

 **Examples:** 

Zeigt, wie man die Knotenstruktur jedes Feldes in einem Dokument ausgibt.

```

 public void fieldToText() throws Exception {
     Document doc = new Document(getMyDir() + "DocumentVisitor-compatible features.docx");
     FieldStructurePrinter visitor = new FieldStructurePrinter();

     // When we get a composite node to accept a document visitor, the visitor visits the accepting node,
     // and then traverses all the node's children in a depth-first manner.
     // The visitor can read and modify each visited node.
     doc.accept(visitor);

     System.out.println(visitor.getText());
 }

 /// 
 /// Traverses a node's non-binary tree of child nodes.
 /// Creates a map in the form of a string of all encountered Field nodes and their children.
 /// 
 public static class FieldStructurePrinter extends DocumentVisitor {
     public FieldStructurePrinter() {
         mBuilder = new StringBuilder();
         mVisitorIsInsideField = false;
     }

     public String getText() {
         return mBuilder.toString();
     }

     /// 
     /// Called when a Run node is encountered in the document.
     /// 
     public int visitRun(final Run run) {
         if (mVisitorIsInsideField) {
             indentAndAppendLine("[Run] \"" + run.getText() + "\"");
         }

         return VisitorAction.CONTINUE;
     }

     /// 
     /// Called when a FieldStart node is encountered in the document.
     /// 
     public int visitFieldStart(final FieldStart fieldStart) {
         indentAndAppendLine("[Field start] FieldType: " + fieldStart.getFieldType());
         mDocTraversalDepth++;
         mVisitorIsInsideField = true;

         return VisitorAction.CONTINUE;
     }

     /// 
     /// Called when a FieldEnd node is encountered in the document.
     /// 
     public int visitFieldEnd(final FieldEnd fieldEnd) {
         mDocTraversalDepth--;
         indentAndAppendLine("[Field end]");
         mVisitorIsInsideField = false;

         return VisitorAction.CONTINUE;
     }

     /// 
     /// Called when a FieldSeparator node is encountered in the document.
     /// 
     public int visitFieldSeparator(final FieldSeparator fieldSeparator) {
         indentAndAppendLine("[FieldSeparator]");

         return VisitorAction.CONTINUE;
     }

     /// 
     /// Append a line to the StringBuilder, and indent it depending on how deep the visitor is
     /// into the field's tree of child nodes.
     /// 
     /// 
     private void indentAndAppendLine(final String text) {
         for (int i = 0; i < mDocTraversalDepth; i++) {
             mBuilder.append("|  ");
         }

         mBuilder.append(text + "\r\n");
     }

     private boolean mVisitorIsInsideField;
     private int mDocTraversalDepth;
     private final StringBuilder mBuilder;
 }
 
```

**Parameters:**
| Parameter | Typ | Beschreibung |
| --- | --- | --- |
| fieldSeparator | [FieldSeparator](../../com.aspose.words/fieldseparator/) | Das Objekt, das besucht wird. |

**Returns:**
int - Ein [VisitorAction](../../com.aspose.words/visitoraction/) Wert, der angibt, wie die Aufzählung fortgesetzt werden soll. Der zurückgegebene Wert ist einer der [VisitorAction](../../com.aspose.words/visitoraction/) Konstanten.
### visitFieldStart(FieldStart fieldStart) {#visitFieldStart-com.aspose.words.FieldStart}
```
public int visitFieldStart(FieldStart fieldStart)
```


Aufgerufen, wenn ein Feld im Dokument beginnt.

 **Remarks:** 

Ein Feld in einem Word-Dokument besteht aus einem Feldcode und einem Feldwert.

Zum Beispiel kann ein Feld, das eine Seitenzahl anzeigt, wie folgt dargestellt werden:

[FieldStart]PAGE[FieldSeparator]98[FieldEnd]

Der Feldtrennzeichen trennt den Feldcode vom Feldwert im Dokument. Beachten Sie, dass einige Felder nur einen Feldcode haben und kein Feldtrennzeichen und keinen Feldwert besitzen.

Felder können verschachtelt werden.

 **Examples:** 

Zeigt, wie man die Knotenstruktur jedes Feldes in einem Dokument ausgibt.

```

 public void fieldToText() throws Exception {
     Document doc = new Document(getMyDir() + "DocumentVisitor-compatible features.docx");
     FieldStructurePrinter visitor = new FieldStructurePrinter();

     // When we get a composite node to accept a document visitor, the visitor visits the accepting node,
     // and then traverses all the node's children in a depth-first manner.
     // The visitor can read and modify each visited node.
     doc.accept(visitor);

     System.out.println(visitor.getText());
 }

 /// 
 /// Traverses a node's non-binary tree of child nodes.
 /// Creates a map in the form of a string of all encountered Field nodes and their children.
 /// 
 public static class FieldStructurePrinter extends DocumentVisitor {
     public FieldStructurePrinter() {
         mBuilder = new StringBuilder();
         mVisitorIsInsideField = false;
     }

     public String getText() {
         return mBuilder.toString();
     }

     /// 
     /// Called when a Run node is encountered in the document.
     /// 
     public int visitRun(final Run run) {
         if (mVisitorIsInsideField) {
             indentAndAppendLine("[Run] \"" + run.getText() + "\"");
         }

         return VisitorAction.CONTINUE;
     }

     /// 
     /// Called when a FieldStart node is encountered in the document.
     /// 
     public int visitFieldStart(final FieldStart fieldStart) {
         indentAndAppendLine("[Field start] FieldType: " + fieldStart.getFieldType());
         mDocTraversalDepth++;
         mVisitorIsInsideField = true;

         return VisitorAction.CONTINUE;
     }

     /// 
     /// Called when a FieldEnd node is encountered in the document.
     /// 
     public int visitFieldEnd(final FieldEnd fieldEnd) {
         mDocTraversalDepth--;
         indentAndAppendLine("[Field end]");
         mVisitorIsInsideField = false;

         return VisitorAction.CONTINUE;
     }

     /// 
     /// Called when a FieldSeparator node is encountered in the document.
     /// 
     public int visitFieldSeparator(final FieldSeparator fieldSeparator) {
         indentAndAppendLine("[FieldSeparator]");

         return VisitorAction.CONTINUE;
     }

     /// 
     /// Append a line to the StringBuilder, and indent it depending on how deep the visitor is
     /// into the field's tree of child nodes.
     /// 
     /// 
     private void indentAndAppendLine(final String text) {
         for (int i = 0; i < mDocTraversalDepth; i++) {
             mBuilder.append("|  ");
         }

         mBuilder.append(text + "\r\n");
     }

     private boolean mVisitorIsInsideField;
     private int mDocTraversalDepth;
     private final StringBuilder mBuilder;
 }
 
```

**Parameters:**
| Parameter | Typ | Beschreibung |
| --- | --- | --- |
| fieldStart | [FieldStart](../../com.aspose.words/fieldstart/) | Das Objekt, das besucht wird. |

**Returns:**
int - Ein [VisitorAction](../../com.aspose.words/visitoraction/) Wert, der angibt, wie die Aufzählung fortgesetzt werden soll. Der zurückgegebene Wert ist einer der [VisitorAction](../../com.aspose.words/visitoraction/) Konstanten.
### visitFootnoteEnd(Footnote footnote) {#visitFootnoteEnd-com.aspose.words.Footnote}
```
public int visitFootnoteEnd(Footnote footnote)
```


Aufgerufen, wenn die Aufzählung eines Fuß- oder Endnoten-Textes abgeschlossen ist.

 **Examples:** 

Zeigt, wie die Knotenstruktur jeder Fußnote in einem Dokument ausgegeben wird.

```

 public void footnoteToText() throws Exception {
     Document doc = new Document(getMyDir() + "DocumentVisitor-compatible features.docx");
     FootnoteStructurePrinter visitor = new FootnoteStructurePrinter();

     // When we get a composite node to accept a document visitor, the visitor visits the accepting node,
     // and then traverses all the node's children in a depth-first manner.
     // The visitor can read and modify each visited node.
     doc.accept(visitor);

     System.out.println(visitor.getText());
 }

 /// 
 /// Traverses a node's non-binary tree of child nodes.
 /// Creates a map in the form of a string of all encountered Footnote nodes and their children.
 /// 
 public static class FootnoteStructurePrinter extends DocumentVisitor {
     public FootnoteStructurePrinter() {
         mBuilder = new StringBuilder();
         mVisitorIsInsideFootnote = false;
     }

     /// 
     /// Gets the plain text of the document that was accumulated by the visitor.
     /// 
     public String getText() {
         return mBuilder.toString();
     }

     /// 
     /// Called when a Footnote node is encountered in the document.
     /// 
     public int visitFootnoteStart(final Footnote footnote) {
         indentAndAppendLine("[Footnote start] Type: " + footnote.getFootnoteType());
         mDocTraversalDepth++;
         mVisitorIsInsideFootnote = true;

         return VisitorAction.CONTINUE;
     }

     /// 
     /// Called after all the child nodes of a Footnote node have been visited.
     /// 
     public int visitFootnoteEnd(final Footnote footnote) {
         mDocTraversalDepth--;
         indentAndAppendLine("[Footnote end]");
         mVisitorIsInsideFootnote = false;

         return VisitorAction.CONTINUE;
     }

     /// 
     /// Called when a Run node is encountered in the document.
     /// 
     public int visitRun(final Run run) {
         if (mVisitorIsInsideFootnote) {
             indentAndAppendLine("[Run] \"" + run.getText() + "\"");
         }

         return VisitorAction.CONTINUE;
     }

     /// 
     /// Append a line to the StringBuilder and indent it depending on how deep the visitor is into the document tree.
     /// 
     /// 
     private void indentAndAppendLine(final String text) {
         for (int i = 0; i < mDocTraversalDepth; i++) {
             mBuilder.append("|  ");
         }

         mBuilder.append(text + "\r\n");
     }

     private boolean mVisitorIsInsideFootnote;
     private int mDocTraversalDepth;
     private final StringBuilder mBuilder;
 }
 
```

**Parameters:**
| Parameter | Typ | Beschreibung |
| --- | --- | --- |
| footnote | [Footnote](../../com.aspose.words/footnote/) | Das Objekt, das besucht wird. |

**Returns:**
int - Ein [VisitorAction](../../com.aspose.words/visitoraction/) Wert, der angibt, wie die Aufzählung fortgesetzt werden soll. Der zurückgegebene Wert ist einer der [VisitorAction](../../com.aspose.words/visitoraction/) Konstanten.
### visitFootnoteStart(Footnote footnote) {#visitFootnoteStart-com.aspose.words.Footnote}
```
public int visitFootnoteStart(Footnote footnote)
```


Aufgerufen, wenn die Aufzählung eines Fuß- oder Endnoten-Textes begonnen hat.

 **Examples:** 

Zeigt, wie die Knotenstruktur jeder Fußnote in einem Dokument ausgegeben wird.

```

 public void footnoteToText() throws Exception {
     Document doc = new Document(getMyDir() + "DocumentVisitor-compatible features.docx");
     FootnoteStructurePrinter visitor = new FootnoteStructurePrinter();

     // When we get a composite node to accept a document visitor, the visitor visits the accepting node,
     // and then traverses all the node's children in a depth-first manner.
     // The visitor can read and modify each visited node.
     doc.accept(visitor);

     System.out.println(visitor.getText());
 }

 /// 
 /// Traverses a node's non-binary tree of child nodes.
 /// Creates a map in the form of a string of all encountered Footnote nodes and their children.
 /// 
 public static class FootnoteStructurePrinter extends DocumentVisitor {
     public FootnoteStructurePrinter() {
         mBuilder = new StringBuilder();
         mVisitorIsInsideFootnote = false;
     }

     /// 
     /// Gets the plain text of the document that was accumulated by the visitor.
     /// 
     public String getText() {
         return mBuilder.toString();
     }

     /// 
     /// Called when a Footnote node is encountered in the document.
     /// 
     public int visitFootnoteStart(final Footnote footnote) {
         indentAndAppendLine("[Footnote start] Type: " + footnote.getFootnoteType());
         mDocTraversalDepth++;
         mVisitorIsInsideFootnote = true;

         return VisitorAction.CONTINUE;
     }

     /// 
     /// Called after all the child nodes of a Footnote node have been visited.
     /// 
     public int visitFootnoteEnd(final Footnote footnote) {
         mDocTraversalDepth--;
         indentAndAppendLine("[Footnote end]");
         mVisitorIsInsideFootnote = false;

         return VisitorAction.CONTINUE;
     }

     /// 
     /// Called when a Run node is encountered in the document.
     /// 
     public int visitRun(final Run run) {
         if (mVisitorIsInsideFootnote) {
             indentAndAppendLine("[Run] \"" + run.getText() + "\"");
         }

         return VisitorAction.CONTINUE;
     }

     /// 
     /// Append a line to the StringBuilder and indent it depending on how deep the visitor is into the document tree.
     /// 
     /// 
     private void indentAndAppendLine(final String text) {
         for (int i = 0; i < mDocTraversalDepth; i++) {
             mBuilder.append("|  ");
         }

         mBuilder.append(text + "\r\n");
     }

     private boolean mVisitorIsInsideFootnote;
     private int mDocTraversalDepth;
     private final StringBuilder mBuilder;
 }
 
```

Zeigt, wie man eine DocumentVisitor‑Implementierung verwendet, um allen versteckten Inhalt aus einem Dokument zu entfernen.

```

 public void removeHiddenContentFromDocument() throws Exception {
     Document doc = new Document(getMyDir() + "Hidden content.docx");
     RemoveHiddenContentVisitor hiddenContentRemover = new RemoveHiddenContentVisitor();

     // Below are three types of fields which can accept a document visitor,
     // which will allow it to visit the accepting node, and then traverse its child nodes in a depth-first manner.
     // 1 -  Paragraph node:
     Paragraph para = (Paragraph) doc.getChild(NodeType.PARAGRAPH, 4, true);
     para.accept(hiddenContentRemover);

     // 2 -  Table node:
     Table table = doc.getFirstSection().getBody().getTables().get(0);
     table.accept(hiddenContentRemover);

     // 3 -  Document node:
     doc.accept(hiddenContentRemover);

     doc.save(getArtifactsDir() + "Font.RemoveHiddenContentFromDocument.docx");
 }

 /// 
 /// Removes all visited nodes marked as "hidden content".
 /// 
 public static class RemoveHiddenContentVisitor extends DocumentVisitor {
     /// 
     /// Called when a FieldStart node is encountered in the document.
     /// 
     public int visitFieldStart(FieldStart fieldStart) {
         if (fieldStart.getFont().getHidden())
             fieldStart.remove();

         return VisitorAction.CONTINUE;
     }

     /// 
     /// Called when a FieldEnd node is encountered in the document.
     /// 
     public int visitFieldEnd(FieldEnd fieldEnd) {
         if (fieldEnd.getFont().getHidden())
             fieldEnd.remove();

         return VisitorAction.CONTINUE;
     }

     /// 
     /// Called when a FieldSeparator node is encountered in the document.
     /// 
     public int visitFieldSeparator(FieldSeparator fieldSeparator) {
         if (fieldSeparator.getFont().getHidden())
             fieldSeparator.remove();

         return VisitorAction.CONTINUE;
     }

     /// 
     /// Called when a Run node is encountered in the document.
     /// 
     public int visitRun(Run run) {
         if (run.getFont().getHidden())
             run.remove();

         return VisitorAction.CONTINUE;
     }

     /// 
     /// Called when a Paragraph node is encountered in the document.
     /// 
     public int visitParagraphStart(Paragraph paragraph) {
         if (paragraph.getParagraphBreakFont().getHidden())
             paragraph.remove();

         return VisitorAction.CONTINUE;
     }

     /// 
     /// Called when a FormField is encountered in the document.
     /// 
     public int visitFormField(FormField formField) {
         if (formField.getFont().getHidden())
             formField.remove();

         return VisitorAction.CONTINUE;
     }

     /// 
     /// Called when a GroupShape is encountered in the document.
     /// 
     public int visitGroupShapeStart(GroupShape groupShape) {
         if (groupShape.getFont().getHidden())
             groupShape.remove();

         return VisitorAction.CONTINUE;
     }

     /// 
     /// Called when a Shape is encountered in the document.
     /// 
     public int visitShapeStart(Shape shape) {
         if (shape.getFont().getHidden())
             shape.remove();

         return VisitorAction.CONTINUE;
     }

     /// 
     /// Called when a Comment is encountered in the document.
     /// 
     public int visitCommentStart(Comment comment) {
         if (comment.getFont().getHidden())
             comment.remove();

         return VisitorAction.CONTINUE;
     }

     /// 
     /// Called when a Footnote is encountered in the document.
     /// 
     public int visitFootnoteStart(Footnote footnote) {
         if (footnote.getFont().getHidden())
             footnote.remove();

         return VisitorAction.CONTINUE;
     }

     /// 
     /// Called when a SpecialCharacter is encountered in the document.
     /// 
     public int visitSpecialChar(SpecialChar specialChar) {
         if (specialChar.getFont().getHidden())
             specialChar.remove();

         return VisitorAction.CONTINUE;
     }

     /// 
     /// Called when visiting of a Table node is ended in the document.
     /// 
     public int visitTableEnd(Table table) {
         // The content inside table cells may have the hidden content flag, but the tables themselves cannot.
         // If this table had nothing but hidden content, this visitor would have removed all of it,
         // and there would be no child nodes left.
         // Thus, we can also treat the table itself as hidden content and remove it.
         // Tables which are empty but do not have hidden content will have cells with empty paragraphs inside,
         // which this visitor will not remove.
         if (!table.hasChildNodes())
             table.remove();

         return VisitorAction.CONTINUE;
     }

     /// 
     /// Called when visiting of a Cell node is ended in the document.
     /// 
     public int visitCellEnd(Cell cell) {
         if (!cell.hasChildNodes() && cell.getParentNode() != null)
             cell.remove();

         return VisitorAction.CONTINUE;
     }

     /// 
     /// Called when visiting of a Row node is ended in the document.
     /// 
     public int visitRowEnd(Row row) {
         if (!row.hasChildNodes() && row.getParentNode() != null)
             row.remove();

         return VisitorAction.CONTINUE;
     }
 }
 
```

**Parameters:**
| Parameter | Typ | Beschreibung |
| --- | --- | --- |
| footnote | [Footnote](../../com.aspose.words/footnote/) | Das Objekt, das besucht wird. |

**Returns:**
int - Ein [VisitorAction](../../com.aspose.words/visitoraction/) Wert, der angibt, wie die Aufzählung fortgesetzt werden soll. Der zurückgegebene Wert ist einer der [VisitorAction](../../com.aspose.words/visitoraction/) Konstanten.
### visitFormField(FormField formField) {#visitFormField-com.aspose.words.FormField}
```
public int visitFormField(FormField formField)
```


Aufgerufen, wenn ein Formularfeld im Dokument gefunden wird.

 **Examples:** 

Zeigt, wie man eine DocumentVisitor‑Implementierung verwendet, um allen versteckten Inhalt aus einem Dokument zu entfernen.

```

 public void removeHiddenContentFromDocument() throws Exception {
     Document doc = new Document(getMyDir() + "Hidden content.docx");
     RemoveHiddenContentVisitor hiddenContentRemover = new RemoveHiddenContentVisitor();

     // Below are three types of fields which can accept a document visitor,
     // which will allow it to visit the accepting node, and then traverse its child nodes in a depth-first manner.
     // 1 -  Paragraph node:
     Paragraph para = (Paragraph) doc.getChild(NodeType.PARAGRAPH, 4, true);
     para.accept(hiddenContentRemover);

     // 2 -  Table node:
     Table table = doc.getFirstSection().getBody().getTables().get(0);
     table.accept(hiddenContentRemover);

     // 3 -  Document node:
     doc.accept(hiddenContentRemover);

     doc.save(getArtifactsDir() + "Font.RemoveHiddenContentFromDocument.docx");
 }

 /// 
 /// Removes all visited nodes marked as "hidden content".
 /// 
 public static class RemoveHiddenContentVisitor extends DocumentVisitor {
     /// 
     /// Called when a FieldStart node is encountered in the document.
     /// 
     public int visitFieldStart(FieldStart fieldStart) {
         if (fieldStart.getFont().getHidden())
             fieldStart.remove();

         return VisitorAction.CONTINUE;
     }

     /// 
     /// Called when a FieldEnd node is encountered in the document.
     /// 
     public int visitFieldEnd(FieldEnd fieldEnd) {
         if (fieldEnd.getFont().getHidden())
             fieldEnd.remove();

         return VisitorAction.CONTINUE;
     }

     /// 
     /// Called when a FieldSeparator node is encountered in the document.
     /// 
     public int visitFieldSeparator(FieldSeparator fieldSeparator) {
         if (fieldSeparator.getFont().getHidden())
             fieldSeparator.remove();

         return VisitorAction.CONTINUE;
     }

     /// 
     /// Called when a Run node is encountered in the document.
     /// 
     public int visitRun(Run run) {
         if (run.getFont().getHidden())
             run.remove();

         return VisitorAction.CONTINUE;
     }

     /// 
     /// Called when a Paragraph node is encountered in the document.
     /// 
     public int visitParagraphStart(Paragraph paragraph) {
         if (paragraph.getParagraphBreakFont().getHidden())
             paragraph.remove();

         return VisitorAction.CONTINUE;
     }

     /// 
     /// Called when a FormField is encountered in the document.
     /// 
     public int visitFormField(FormField formField) {
         if (formField.getFont().getHidden())
             formField.remove();

         return VisitorAction.CONTINUE;
     }

     /// 
     /// Called when a GroupShape is encountered in the document.
     /// 
     public int visitGroupShapeStart(GroupShape groupShape) {
         if (groupShape.getFont().getHidden())
             groupShape.remove();

         return VisitorAction.CONTINUE;
     }

     /// 
     /// Called when a Shape is encountered in the document.
     /// 
     public int visitShapeStart(Shape shape) {
         if (shape.getFont().getHidden())
             shape.remove();

         return VisitorAction.CONTINUE;
     }

     /// 
     /// Called when a Comment is encountered in the document.
     /// 
     public int visitCommentStart(Comment comment) {
         if (comment.getFont().getHidden())
             comment.remove();

         return VisitorAction.CONTINUE;
     }

     /// 
     /// Called when a Footnote is encountered in the document.
     /// 
     public int visitFootnoteStart(Footnote footnote) {
         if (footnote.getFont().getHidden())
             footnote.remove();

         return VisitorAction.CONTINUE;
     }

     /// 
     /// Called when a SpecialCharacter is encountered in the document.
     /// 
     public int visitSpecialChar(SpecialChar specialChar) {
         if (specialChar.getFont().getHidden())
             specialChar.remove();

         return VisitorAction.CONTINUE;
     }

     /// 
     /// Called when visiting of a Table node is ended in the document.
     /// 
     public int visitTableEnd(Table table) {
         // The content inside table cells may have the hidden content flag, but the tables themselves cannot.
         // If this table had nothing but hidden content, this visitor would have removed all of it,
         // and there would be no child nodes left.
         // Thus, we can also treat the table itself as hidden content and remove it.
         // Tables which are empty but do not have hidden content will have cells with empty paragraphs inside,
         // which this visitor will not remove.
         if (!table.hasChildNodes())
             table.remove();

         return VisitorAction.CONTINUE;
     }

     /// 
     /// Called when visiting of a Cell node is ended in the document.
     /// 
     public int visitCellEnd(Cell cell) {
         if (!cell.hasChildNodes() && cell.getParentNode() != null)
             cell.remove();

         return VisitorAction.CONTINUE;
     }

     /// 
     /// Called when visiting of a Row node is ended in the document.
     /// 
     public int visitRowEnd(Row row) {
         if (!row.hasChildNodes() && row.getParentNode() != null)
             row.remove();

         return VisitorAction.CONTINUE;
     }
 }
 
```

**Parameters:**
| Parameter | Typ | Beschreibung |
| --- | --- | --- |
| formField | [FormField](../../com.aspose.words/formfield/) | Das Objekt, das besucht wird. |

**Returns:**
int - Ein [VisitorAction](../../com.aspose.words/visitoraction/) Wert, der angibt, wie die Aufzählung fortgesetzt werden soll. Der zurückgegebene Wert ist einer der [VisitorAction](../../com.aspose.words/visitoraction/) Konstanten.
### visitGlossaryDocumentEnd(GlossaryDocument glossary) {#visitGlossaryDocumentEnd-com.aspose.words.GlossaryDocument}
```
public int visitGlossaryDocumentEnd(GlossaryDocument glossary)
```


Aufgerufen, wenn die Aufzählung eines Glossar-Dokuments abgeschlossen ist.

 **Remarks:** 

Hinweis: Ein Glossar-Dokumentknoten und seine Unterknoten werden nicht besucht, wenn Sie einen Visitor über ein [Document](../../com.aspose.words/document/) ausführen. Wenn Sie einen Visitor über ein Glossar-Dokument ausführen möchten, müssen Sie [GlossaryDocument.accept(com.aspose.words.DocumentVisitor)](../../com.aspose.words/glossarydocument/\#accept-com.aspose.words.DocumentVisitor) aufrufen.

 **Examples:** 

Zeigt Möglichkeiten zum Zugriff auf Bausteine in einem Glossar-Dokument.

```

 public void glossaryDocument() throws Exception {
     Document doc = new Document();
     GlossaryDocument glossaryDoc = new GlossaryDocument();

     glossaryDoc.appendChild(createNewBuildingBlock(glossaryDoc, "Block 1"));
     glossaryDoc.appendChild(createNewBuildingBlock(glossaryDoc, "Block 2"));
     glossaryDoc.appendChild(createNewBuildingBlock(glossaryDoc, "Block 3"));
     glossaryDoc.appendChild(createNewBuildingBlock(glossaryDoc, "Block 4"));
     glossaryDoc.appendChild(createNewBuildingBlock(glossaryDoc, "Block 5"));

     Assert.assertEquals(glossaryDoc.getBuildingBlocks().getCount(), 5);

     doc.setGlossaryDocument(glossaryDoc);

     // There are various ways of accessing building blocks.
     // 1 -  Get the first/last building blocks in the collection:
     Assert.assertEquals("Block 1", glossaryDoc.getFirstBuildingBlock().getName());
     Assert.assertEquals("Block 5", glossaryDoc.getLastBuildingBlock().getName());

     // 2 -  Get a building block by index:
     Assert.assertEquals("Block 2", glossaryDoc.getBuildingBlocks().get(1).getName());
     Assert.assertEquals("Block 3", glossaryDoc.getBuildingBlocks().toArray()[2].getName());

     // 3 -  Get the first building block that matches a gallery, name and category:
     Assert.assertEquals("Block 4",
             glossaryDoc.getBuildingBlock(BuildingBlockGallery.ALL, "(Empty Category)", "Block 4").getName());

     // We will do that using a custom visitor,
     // which will give every BuildingBlock in the GlossaryDocument a unique GUID
     GlossaryDocVisitor visitor = new GlossaryDocVisitor();
     // Visit start/end of the Glossary document.
     glossaryDoc.accept(visitor);
     // Visit only start of the Glossary document.
     glossaryDoc.acceptStart(visitor);
     // Visit only end of the Glossary document.
     glossaryDoc.acceptEnd(visitor);
     System.out.println(visitor.getText());

     // In Microsoft Word, we can access the building blocks via "Insert" -> "Quick Parts" -> "Building Blocks Organizer".
     doc.save(getArtifactsDir() + "BuildingBlocks.GlossaryDocument.dotx");
 }

 public static BuildingBlock createNewBuildingBlock(final GlossaryDocument glossaryDoc, final String buildingBlockName) {
     BuildingBlock buildingBlock = new BuildingBlock(glossaryDoc);
     buildingBlock.setName(buildingBlockName);

     return buildingBlock;
 }

 /// 
 /// Gives each building block in a visited glossary document a unique GUID.
 /// Stores the GUID-building block pairs in a dictionary.
 /// 
 public static class GlossaryDocVisitor extends DocumentVisitor {
     public GlossaryDocVisitor() {
         mBlocksByGuid = new HashMap<>();
         mBuilder = new StringBuilder();
     }

     public String getText() {
         return mBuilder.toString();
     }

     public HashMap getDictionary() {
         return mBlocksByGuid;
     }

     public int visitGlossaryDocumentStart(final GlossaryDocument glossary) {
         mBuilder.append("Glossary document found!\n");
         return VisitorAction.CONTINUE;
     }

     public int visitGlossaryDocumentEnd(final GlossaryDocument glossary) {
         mBuilder.append("Reached end of glossary!\n");
         mBuilder.append("BuildingBlocks found: " + mBlocksByGuid.size() + "\r\n");
         return VisitorAction.CONTINUE;
     }

     public int visitBuildingBlockStart(final BuildingBlock block) {
         block.setGuid(UUID.randomUUID());
         mBlocksByGuid.put(block.getGuid(), block);
         return VisitorAction.CONTINUE;
     }

     public int visitBuildingBlockEnd(final BuildingBlock block) {
         mBuilder.append("\tVisited block \"" + block.getName() + "\"" + "\r\n");
         mBuilder.append("\t Type: " + block.getType() + "\r\n");
         mBuilder.append("\t Gallery: " + block.getGallery() + "\r\n");
         mBuilder.append("\t Behavior: " + block.getBehavior() + "\r\n");
         mBuilder.append("\t Description: " + block.getDescription() + "\r\n");

         return VisitorAction.CONTINUE;
     }

     private final HashMap mBlocksByGuid;
     private final StringBuilder mBuilder;
 }
 
```

**Parameters:**
| Parameter | Typ | Beschreibung |
| --- | --- | --- |
| glossary | [GlossaryDocument](../../com.aspose.words/glossarydocument/) | Das Objekt, das besucht wird. |

**Returns:**
int - Ein [VisitorAction](../../com.aspose.words/visitoraction/) Wert, der angibt, wie die Aufzählung fortgesetzt werden soll. Der zurückgegebene Wert ist einer der [VisitorAction](../../com.aspose.words/visitoraction/) Konstanten.
### visitGlossaryDocumentStart(GlossaryDocument glossary) {#visitGlossaryDocumentStart-com.aspose.words.GlossaryDocument}
```
public int visitGlossaryDocumentStart(GlossaryDocument glossary)
```


Aufgerufen, wenn die Aufzählung eines Glossar-Dokuments begonnen hat.

 **Remarks:** 

Hinweis: Ein Glossar-Dokumentknoten und seine Unterknoten werden nicht besucht, wenn Sie einen Visitor über ein [Document](../../com.aspose.words/document/) ausführen. Wenn Sie einen Visitor über ein Glossar-Dokument ausführen möchten, müssen Sie [GlossaryDocument.accept(com.aspose.words.DocumentVisitor)](../../com.aspose.words/glossarydocument/\#accept-com.aspose.words.DocumentVisitor) aufrufen.

 **Examples:** 

Zeigt Möglichkeiten zum Zugriff auf Bausteine in einem Glossar-Dokument.

```

 public void glossaryDocument() throws Exception {
     Document doc = new Document();
     GlossaryDocument glossaryDoc = new GlossaryDocument();

     glossaryDoc.appendChild(createNewBuildingBlock(glossaryDoc, "Block 1"));
     glossaryDoc.appendChild(createNewBuildingBlock(glossaryDoc, "Block 2"));
     glossaryDoc.appendChild(createNewBuildingBlock(glossaryDoc, "Block 3"));
     glossaryDoc.appendChild(createNewBuildingBlock(glossaryDoc, "Block 4"));
     glossaryDoc.appendChild(createNewBuildingBlock(glossaryDoc, "Block 5"));

     Assert.assertEquals(glossaryDoc.getBuildingBlocks().getCount(), 5);

     doc.setGlossaryDocument(glossaryDoc);

     // There are various ways of accessing building blocks.
     // 1 -  Get the first/last building blocks in the collection:
     Assert.assertEquals("Block 1", glossaryDoc.getFirstBuildingBlock().getName());
     Assert.assertEquals("Block 5", glossaryDoc.getLastBuildingBlock().getName());

     // 2 -  Get a building block by index:
     Assert.assertEquals("Block 2", glossaryDoc.getBuildingBlocks().get(1).getName());
     Assert.assertEquals("Block 3", glossaryDoc.getBuildingBlocks().toArray()[2].getName());

     // 3 -  Get the first building block that matches a gallery, name and category:
     Assert.assertEquals("Block 4",
             glossaryDoc.getBuildingBlock(BuildingBlockGallery.ALL, "(Empty Category)", "Block 4").getName());

     // We will do that using a custom visitor,
     // which will give every BuildingBlock in the GlossaryDocument a unique GUID
     GlossaryDocVisitor visitor = new GlossaryDocVisitor();
     // Visit start/end of the Glossary document.
     glossaryDoc.accept(visitor);
     // Visit only start of the Glossary document.
     glossaryDoc.acceptStart(visitor);
     // Visit only end of the Glossary document.
     glossaryDoc.acceptEnd(visitor);
     System.out.println(visitor.getText());

     // In Microsoft Word, we can access the building blocks via "Insert" -> "Quick Parts" -> "Building Blocks Organizer".
     doc.save(getArtifactsDir() + "BuildingBlocks.GlossaryDocument.dotx");
 }

 public static BuildingBlock createNewBuildingBlock(final GlossaryDocument glossaryDoc, final String buildingBlockName) {
     BuildingBlock buildingBlock = new BuildingBlock(glossaryDoc);
     buildingBlock.setName(buildingBlockName);

     return buildingBlock;
 }

 /// 
 /// Gives each building block in a visited glossary document a unique GUID.
 /// Stores the GUID-building block pairs in a dictionary.
 /// 
 public static class GlossaryDocVisitor extends DocumentVisitor {
     public GlossaryDocVisitor() {
         mBlocksByGuid = new HashMap<>();
         mBuilder = new StringBuilder();
     }

     public String getText() {
         return mBuilder.toString();
     }

     public HashMap getDictionary() {
         return mBlocksByGuid;
     }

     public int visitGlossaryDocumentStart(final GlossaryDocument glossary) {
         mBuilder.append("Glossary document found!\n");
         return VisitorAction.CONTINUE;
     }

     public int visitGlossaryDocumentEnd(final GlossaryDocument glossary) {
         mBuilder.append("Reached end of glossary!\n");
         mBuilder.append("BuildingBlocks found: " + mBlocksByGuid.size() + "\r\n");
         return VisitorAction.CONTINUE;
     }

     public int visitBuildingBlockStart(final BuildingBlock block) {
         block.setGuid(UUID.randomUUID());
         mBlocksByGuid.put(block.getGuid(), block);
         return VisitorAction.CONTINUE;
     }

     public int visitBuildingBlockEnd(final BuildingBlock block) {
         mBuilder.append("\tVisited block \"" + block.getName() + "\"" + "\r\n");
         mBuilder.append("\t Type: " + block.getType() + "\r\n");
         mBuilder.append("\t Gallery: " + block.getGallery() + "\r\n");
         mBuilder.append("\t Behavior: " + block.getBehavior() + "\r\n");
         mBuilder.append("\t Description: " + block.getDescription() + "\r\n");

         return VisitorAction.CONTINUE;
     }

     private final HashMap mBlocksByGuid;
     private final StringBuilder mBuilder;
 }
 
```

**Parameters:**
| Parameter | Typ | Beschreibung |
| --- | --- | --- |
| glossary | [GlossaryDocument](../../com.aspose.words/glossarydocument/) | Das Objekt, das besucht wird. |

**Returns:**
int - Ein [VisitorAction](../../com.aspose.words/visitoraction/) Wert, der angibt, wie die Aufzählung fortgesetzt werden soll. Der zurückgegebene Wert ist einer der [VisitorAction](../../com.aspose.words/visitoraction/) Konstanten.
### visitGroupShapeEnd(GroupShape groupShape) {#visitGroupShapeEnd-com.aspose.words.GroupShape}
```
public int visitGroupShapeEnd(GroupShape groupShape)
```


Aufgerufen, wenn die Aufzählung einer Gruppenform abgeschlossen ist.

 **Examples:** 

Zeigt, wie eine Gruppe von Formen erstellt und ihr Inhalt mit einem Document Visitor ausgegeben wird.

```

 public void groupOfShapes() throws Exception {
     Document doc = new Document();
     DocumentBuilder builder = new DocumentBuilder(doc);

     // If you need to create "NonPrimitive" shapes, such as SingleCornerSnipped, TopCornersSnipped, DiagonalCornersSnipped,
     // TopCornersOneRoundedOneSnipped, SingleCornerRounded, TopCornersRounded, DiagonalCornersRounded
     // please use DocumentBuilder.InsertShape methods.
     Shape balloon = new Shape(doc, ShapeType.BALLOON);
     balloon.setWidth(200.0);
     balloon.setHeight(200.0);
     balloon.setStrokeColor(Color.RED);

     Shape cube = new Shape(doc, ShapeType.CUBE);
     cube.setWidth(100.0);
     cube.setHeight(100.0);
     cube.setStrokeColor(Color.BLUE);

     GroupShape group = new GroupShape(doc);
     group.appendChild(balloon);
     group.appendChild(cube);

     Assert.assertTrue(group.isGroup());
     builder.insertNode(group);

     ShapeInfoPrinter printer = new ShapeInfoPrinter();
     group.accept(printer);

     System.out.println(printer.getText());
 }

 /// 
 /// Prints the contents of a visited shape group to the console.
 /// 
 public static class ShapeInfoPrinter extends DocumentVisitor {
     public ShapeInfoPrinter() {
         mBuilder = new StringBuilder();
     }

     public String getText() {
         return mBuilder.toString();
     }

     public int visitGroupShapeStart(final GroupShape groupShape) {
         mBuilder.append("Shape group started:\r\n");
         return VisitorAction.CONTINUE;
     }

     public int visitGroupShapeEnd(final GroupShape groupShape) {
         mBuilder.append("End of shape group\r\n");
         return VisitorAction.CONTINUE;
     }

     public int visitShapeStart(final Shape shape) {
         mBuilder.append("\tShape - " + shape.getShapeType() + ":\r\n");
         mBuilder.append("\t\tWidth: " + shape.getWidth() + "\r\n");
         mBuilder.append("\t\tHeight: " + shape.getHeight() + "\r\n");
         mBuilder.append("\t\tStroke color: " + shape.getStroke().getColor() + "\r\n");
         mBuilder.append("\t\tFill color: " + shape.getFill().getForeColor() + "\r\n");
         return VisitorAction.CONTINUE;
     }

     public int visitShapeEnd(final Shape shape) {
         mBuilder.append("\tEnd of shape\r\n");
         return VisitorAction.CONTINUE;
     }

     private final StringBuilder mBuilder;
 }
 
```

**Parameters:**
| Parameter | Typ | Beschreibung |
| --- | --- | --- |
| groupShape | [GroupShape](../../com.aspose.words/groupshape/) | Das Objekt, das besucht wird. |

**Returns:**
int - Ein [VisitorAction](../../com.aspose.words/visitoraction/) Wert, der angibt, wie die Aufzählung fortgesetzt werden soll. Der zurückgegebene Wert ist einer der [VisitorAction](../../com.aspose.words/visitoraction/) Konstanten.
### visitGroupShapeStart(GroupShape groupShape) {#visitGroupShapeStart-com.aspose.words.GroupShape}
```
public int visitGroupShapeStart(GroupShape groupShape)
```


Aufgerufen, wenn die Aufzählung einer Gruppenform begonnen hat.

 **Examples:** 

Zeigt, wie eine Gruppe von Formen erstellt und ihr Inhalt mit einem Document Visitor ausgegeben wird.

```

 public void groupOfShapes() throws Exception {
     Document doc = new Document();
     DocumentBuilder builder = new DocumentBuilder(doc);

     // If you need to create "NonPrimitive" shapes, such as SingleCornerSnipped, TopCornersSnipped, DiagonalCornersSnipped,
     // TopCornersOneRoundedOneSnipped, SingleCornerRounded, TopCornersRounded, DiagonalCornersRounded
     // please use DocumentBuilder.InsertShape methods.
     Shape balloon = new Shape(doc, ShapeType.BALLOON);
     balloon.setWidth(200.0);
     balloon.setHeight(200.0);
     balloon.setStrokeColor(Color.RED);

     Shape cube = new Shape(doc, ShapeType.CUBE);
     cube.setWidth(100.0);
     cube.setHeight(100.0);
     cube.setStrokeColor(Color.BLUE);

     GroupShape group = new GroupShape(doc);
     group.appendChild(balloon);
     group.appendChild(cube);

     Assert.assertTrue(group.isGroup());
     builder.insertNode(group);

     ShapeInfoPrinter printer = new ShapeInfoPrinter();
     group.accept(printer);

     System.out.println(printer.getText());
 }

 /// 
 /// Prints the contents of a visited shape group to the console.
 /// 
 public static class ShapeInfoPrinter extends DocumentVisitor {
     public ShapeInfoPrinter() {
         mBuilder = new StringBuilder();
     }

     public String getText() {
         return mBuilder.toString();
     }

     public int visitGroupShapeStart(final GroupShape groupShape) {
         mBuilder.append("Shape group started:\r\n");
         return VisitorAction.CONTINUE;
     }

     public int visitGroupShapeEnd(final GroupShape groupShape) {
         mBuilder.append("End of shape group\r\n");
         return VisitorAction.CONTINUE;
     }

     public int visitShapeStart(final Shape shape) {
         mBuilder.append("\tShape - " + shape.getShapeType() + ":\r\n");
         mBuilder.append("\t\tWidth: " + shape.getWidth() + "\r\n");
         mBuilder.append("\t\tHeight: " + shape.getHeight() + "\r\n");
         mBuilder.append("\t\tStroke color: " + shape.getStroke().getColor() + "\r\n");
         mBuilder.append("\t\tFill color: " + shape.getFill().getForeColor() + "\r\n");
         return VisitorAction.CONTINUE;
     }

     public int visitShapeEnd(final Shape shape) {
         mBuilder.append("\tEnd of shape\r\n");
         return VisitorAction.CONTINUE;
     }

     private final StringBuilder mBuilder;
 }
 
```

Zeigt, wie man eine DocumentVisitor‑Implementierung verwendet, um allen versteckten Inhalt aus einem Dokument zu entfernen.

```

 public void removeHiddenContentFromDocument() throws Exception {
     Document doc = new Document(getMyDir() + "Hidden content.docx");
     RemoveHiddenContentVisitor hiddenContentRemover = new RemoveHiddenContentVisitor();

     // Below are three types of fields which can accept a document visitor,
     // which will allow it to visit the accepting node, and then traverse its child nodes in a depth-first manner.
     // 1 -  Paragraph node:
     Paragraph para = (Paragraph) doc.getChild(NodeType.PARAGRAPH, 4, true);
     para.accept(hiddenContentRemover);

     // 2 -  Table node:
     Table table = doc.getFirstSection().getBody().getTables().get(0);
     table.accept(hiddenContentRemover);

     // 3 -  Document node:
     doc.accept(hiddenContentRemover);

     doc.save(getArtifactsDir() + "Font.RemoveHiddenContentFromDocument.docx");
 }

 /// 
 /// Removes all visited nodes marked as "hidden content".
 /// 
 public static class RemoveHiddenContentVisitor extends DocumentVisitor {
     /// 
     /// Called when a FieldStart node is encountered in the document.
     /// 
     public int visitFieldStart(FieldStart fieldStart) {
         if (fieldStart.getFont().getHidden())
             fieldStart.remove();

         return VisitorAction.CONTINUE;
     }

     /// 
     /// Called when a FieldEnd node is encountered in the document.
     /// 
     public int visitFieldEnd(FieldEnd fieldEnd) {
         if (fieldEnd.getFont().getHidden())
             fieldEnd.remove();

         return VisitorAction.CONTINUE;
     }

     /// 
     /// Called when a FieldSeparator node is encountered in the document.
     /// 
     public int visitFieldSeparator(FieldSeparator fieldSeparator) {
         if (fieldSeparator.getFont().getHidden())
             fieldSeparator.remove();

         return VisitorAction.CONTINUE;
     }

     /// 
     /// Called when a Run node is encountered in the document.
     /// 
     public int visitRun(Run run) {
         if (run.getFont().getHidden())
             run.remove();

         return VisitorAction.CONTINUE;
     }

     /// 
     /// Called when a Paragraph node is encountered in the document.
     /// 
     public int visitParagraphStart(Paragraph paragraph) {
         if (paragraph.getParagraphBreakFont().getHidden())
             paragraph.remove();

         return VisitorAction.CONTINUE;
     }

     /// 
     /// Called when a FormField is encountered in the document.
     /// 
     public int visitFormField(FormField formField) {
         if (formField.getFont().getHidden())
             formField.remove();

         return VisitorAction.CONTINUE;
     }

     /// 
     /// Called when a GroupShape is encountered in the document.
     /// 
     public int visitGroupShapeStart(GroupShape groupShape) {
         if (groupShape.getFont().getHidden())
             groupShape.remove();

         return VisitorAction.CONTINUE;
     }

     /// 
     /// Called when a Shape is encountered in the document.
     /// 
     public int visitShapeStart(Shape shape) {
         if (shape.getFont().getHidden())
             shape.remove();

         return VisitorAction.CONTINUE;
     }

     /// 
     /// Called when a Comment is encountered in the document.
     /// 
     public int visitCommentStart(Comment comment) {
         if (comment.getFont().getHidden())
             comment.remove();

         return VisitorAction.CONTINUE;
     }

     /// 
     /// Called when a Footnote is encountered in the document.
     /// 
     public int visitFootnoteStart(Footnote footnote) {
         if (footnote.getFont().getHidden())
             footnote.remove();

         return VisitorAction.CONTINUE;
     }

     /// 
     /// Called when a SpecialCharacter is encountered in the document.
     /// 
     public int visitSpecialChar(SpecialChar specialChar) {
         if (specialChar.getFont().getHidden())
             specialChar.remove();

         return VisitorAction.CONTINUE;
     }

     /// 
     /// Called when visiting of a Table node is ended in the document.
     /// 
     public int visitTableEnd(Table table) {
         // The content inside table cells may have the hidden content flag, but the tables themselves cannot.
         // If this table had nothing but hidden content, this visitor would have removed all of it,
         // and there would be no child nodes left.
         // Thus, we can also treat the table itself as hidden content and remove it.
         // Tables which are empty but do not have hidden content will have cells with empty paragraphs inside,
         // which this visitor will not remove.
         if (!table.hasChildNodes())
             table.remove();

         return VisitorAction.CONTINUE;
     }

     /// 
     /// Called when visiting of a Cell node is ended in the document.
     /// 
     public int visitCellEnd(Cell cell) {
         if (!cell.hasChildNodes() && cell.getParentNode() != null)
             cell.remove();

         return VisitorAction.CONTINUE;
     }

     /// 
     /// Called when visiting of a Row node is ended in the document.
     /// 
     public int visitRowEnd(Row row) {
         if (!row.hasChildNodes() && row.getParentNode() != null)
             row.remove();

         return VisitorAction.CONTINUE;
     }
 }
 
```

**Parameters:**
| Parameter | Typ | Beschreibung |
| --- | --- | --- |
| groupShape | [GroupShape](../../com.aspose.words/groupshape/) | Das Objekt, das besucht wird. |

**Returns:**
int - Ein [VisitorAction](../../com.aspose.words/visitoraction/) Wert, der angibt, wie die Aufzählung fortgesetzt werden soll. Der zurückgegebene Wert ist einer der [VisitorAction](../../com.aspose.words/visitoraction/) Konstanten.
### visitHeaderFooterEnd(HeaderFooter headerFooter) {#visitHeaderFooterEnd-com.aspose.words.HeaderFooter}
```
public int visitHeaderFooterEnd(HeaderFooter headerFooter)
```


Aufgerufen, wenn die Aufzählung einer Kopf- oder Fußzeile in einem Abschnitt abgeschlossen ist.

 **Examples:** 

Zeigt, wie die Knotenstruktur jeder Kopf- und Fußzeile in einem Dokument ausgegeben wird.

```

 public void headerFooterToText() throws Exception {
     Document doc = new Document(getMyDir() + "DocumentVisitor-compatible features.docx");
     HeaderFooterStructurePrinter visitor = new HeaderFooterStructurePrinter();

     // When we get a composite node to accept a document visitor, the visitor visits the accepting node,
     // and then traverses all the node's children in a depth-first manner.
     // The visitor can read and modify each visited node.
     doc.accept(visitor);

     System.out.println(visitor.getText());

     // An alternative way of accessing a document's header/footers section-by-section is by accessing the collection.
     HeaderFooter[] headerFooters = doc.getFirstSection().getHeadersFooters().toArray();
     Assert.assertEquals(3, headerFooters.length);
 }

 /// 
 /// Traverses a node's non-binary tree of child nodes.
 /// Creates a map in the form of a string of all encountered HeaderFooter nodes and their children.
 /// 
 public static class HeaderFooterStructurePrinter extends DocumentVisitor {
     public HeaderFooterStructurePrinter() {
         mBuilder = new StringBuilder();
         mVisitorIsInsideHeaderFooter = false;
     }

     public String getText() {
         return mBuilder.toString();
     }

     /// 
     /// Called when a Run node is encountered in the document.
     /// 
     public int visitRun(final Run run) {
         if (mVisitorIsInsideHeaderFooter) indentAndAppendLine("[Run] \"" + run.getText() + "\"");

         return VisitorAction.CONTINUE;
     }

     /// 
     /// Called when a HeaderFooter node is encountered in the document.
     /// 
     public int visitHeaderFooterStart(final HeaderFooter headerFooter) {
         indentAndAppendLine("[HeaderFooter start] HeaderFooterType: " + headerFooter.getHeaderFooterType());
         mDocTraversalDepth++;
         mVisitorIsInsideHeaderFooter = true;

         return VisitorAction.CONTINUE;
     }

     /// 
     /// Called after all the child nodes of a HeaderFooter node have been visited.
     /// 
     public int visitHeaderFooterEnd(final HeaderFooter headerFooter) {
         mDocTraversalDepth--;
         indentAndAppendLine("[HeaderFooter end]");
         mVisitorIsInsideHeaderFooter = false;

         return VisitorAction.CONTINUE;
     }

     /// 
     /// Append a line to the StringBuilder, and indent it depending on how deep the visitor is into the document tree.
     /// 
     /// 
     private void indentAndAppendLine(final String text) {
         for (int i = 0; i < mDocTraversalDepth; i++) {
             mBuilder.append("|  ");
         }

         mBuilder.append(text + "\r\n");
     }

     private boolean mVisitorIsInsideHeaderFooter;
     private int mDocTraversalDepth;
     private final StringBuilder mBuilder;
 }
 
```

**Parameters:**
| Parameter | Typ | Beschreibung |
| --- | --- | --- |
| headerFooter | [HeaderFooter](../../com.aspose.words/headerfooter/) | Das Objekt, das besucht wird. |

**Returns:**
int - Ein [VisitorAction](../../com.aspose.words/visitoraction/) Wert, der angibt, wie die Aufzählung fortgesetzt werden soll. Der zurückgegebene Wert ist einer der [VisitorAction](../../com.aspose.words/visitoraction/) Konstanten.
### visitHeaderFooterStart(HeaderFooter headerFooter) {#visitHeaderFooterStart-com.aspose.words.HeaderFooter}
```
public int visitHeaderFooterStart(HeaderFooter headerFooter)
```


Aufgerufen, wenn die Aufzählung einer Kopf- oder Fußzeile in einem Abschnitt begonnen hat.

 **Examples:** 

Zeigt, wie die Knotenstruktur jeder Kopf- und Fußzeile in einem Dokument ausgegeben wird.

```

 public void headerFooterToText() throws Exception {
     Document doc = new Document(getMyDir() + "DocumentVisitor-compatible features.docx");
     HeaderFooterStructurePrinter visitor = new HeaderFooterStructurePrinter();

     // When we get a composite node to accept a document visitor, the visitor visits the accepting node,
     // and then traverses all the node's children in a depth-first manner.
     // The visitor can read and modify each visited node.
     doc.accept(visitor);

     System.out.println(visitor.getText());

     // An alternative way of accessing a document's header/footers section-by-section is by accessing the collection.
     HeaderFooter[] headerFooters = doc.getFirstSection().getHeadersFooters().toArray();
     Assert.assertEquals(3, headerFooters.length);
 }

 /// 
 /// Traverses a node's non-binary tree of child nodes.
 /// Creates a map in the form of a string of all encountered HeaderFooter nodes and their children.
 /// 
 public static class HeaderFooterStructurePrinter extends DocumentVisitor {
     public HeaderFooterStructurePrinter() {
         mBuilder = new StringBuilder();
         mVisitorIsInsideHeaderFooter = false;
     }

     public String getText() {
         return mBuilder.toString();
     }

     /// 
     /// Called when a Run node is encountered in the document.
     /// 
     public int visitRun(final Run run) {
         if (mVisitorIsInsideHeaderFooter) indentAndAppendLine("[Run] \"" + run.getText() + "\"");

         return VisitorAction.CONTINUE;
     }

     /// 
     /// Called when a HeaderFooter node is encountered in the document.
     /// 
     public int visitHeaderFooterStart(final HeaderFooter headerFooter) {
         indentAndAppendLine("[HeaderFooter start] HeaderFooterType: " + headerFooter.getHeaderFooterType());
         mDocTraversalDepth++;
         mVisitorIsInsideHeaderFooter = true;

         return VisitorAction.CONTINUE;
     }

     /// 
     /// Called after all the child nodes of a HeaderFooter node have been visited.
     /// 
     public int visitHeaderFooterEnd(final HeaderFooter headerFooter) {
         mDocTraversalDepth--;
         indentAndAppendLine("[HeaderFooter end]");
         mVisitorIsInsideHeaderFooter = false;

         return VisitorAction.CONTINUE;
     }

     /// 
     /// Append a line to the StringBuilder, and indent it depending on how deep the visitor is into the document tree.
     /// 
     /// 
     private void indentAndAppendLine(final String text) {
         for (int i = 0; i < mDocTraversalDepth; i++) {
             mBuilder.append("|  ");
         }

         mBuilder.append(text + "\r\n");
     }

     private boolean mVisitorIsInsideHeaderFooter;
     private int mDocTraversalDepth;
     private final StringBuilder mBuilder;
 }
 
```

**Parameters:**
| Parameter | Typ | Beschreibung |
| --- | --- | --- |
| headerFooter | [HeaderFooter](../../com.aspose.words/headerfooter/) | Das Objekt, das besucht wird. |

**Returns:**
int - Ein [VisitorAction](../../com.aspose.words/visitoraction/) Wert, der angibt, wie die Aufzählung fortgesetzt werden soll. Der zurückgegebene Wert ist einer der [VisitorAction](../../com.aspose.words/visitoraction/) Konstanten.
### visitOfficeMathEnd(OfficeMath officeMath) {#visitOfficeMathEnd-com.aspose.words.OfficeMath}
```
public int visitOfficeMathEnd(OfficeMath officeMath)
```


Aufgerufen, wenn die Aufzählung eines Office‑Math‑Objekts abgeschlossen ist.

 **Examples:** 

Zeigt, wie die Knotenstruktur jedes Office-Math-Knotens in einem Dokument ausgegeben wird.

```

 public void officeMathToText() throws Exception {
     Document doc = new Document(getMyDir() + "DocumentVisitor-compatible features.docx");
     OfficeMathStructurePrinter visitor = new OfficeMathStructurePrinter();

     // When we get a composite node to accept a document visitor, the visitor visits the accepting node,
     // and then traverses all the node's children in a depth-first manner.
     // The visitor can read and modify each visited node.
     doc.accept(visitor);

     System.out.println(visitor.getText());
 }

 /// 
 /// Traverses a node's non-binary tree of child nodes.
 /// Creates a map in the form of a string of all encountered OfficeMath nodes and their children.
 /// 
 public static class OfficeMathStructurePrinter extends DocumentVisitor {
     public OfficeMathStructurePrinter() {
         mBuilder = new StringBuilder();
         mVisitorIsInsideOfficeMath = false;
     }

     /// 
     /// Gets the plain text of the document that was accumulated by the visitor.
     /// 
     public String getText() {
         return mBuilder.toString();
     }

     /// 
     /// Called when a Run node is encountered in the document.
     /// 
     public int visitRun(final Run run) {
         if (mVisitorIsInsideOfficeMath) {
             indentAndAppendLine("[Run] \"" + run.getText() + "\"");
         }

         return VisitorAction.CONTINUE;
     }

     /// 
     /// Called when an OfficeMath node is encountered in the document.
     /// 
     public int visitOfficeMathStart(final OfficeMath officeMath) {
         indentAndAppendLine("[OfficeMath start] Math object type: " + officeMath.getMathObjectType());
         mDocTraversalDepth++;
         mVisitorIsInsideOfficeMath = true;

         return VisitorAction.CONTINUE;
     }

     /// 
     /// Called after all the child nodes of an OfficeMath node have been visited.
     /// 
     public int visitOfficeMathEnd(final OfficeMath officeMath) {
         mDocTraversalDepth--;
         indentAndAppendLine("[OfficeMath end]");
         mVisitorIsInsideOfficeMath = false;

         return VisitorAction.CONTINUE;
     }

     /// 
     /// Append a line to the StringBuilder and indent it depending on how deep the visitor is into the document tree.
     /// 
     /// 
     private void indentAndAppendLine(final String text) {
         for (int i = 0; i < mDocTraversalDepth; i++) {
             mBuilder.append("|  ");
         }

         mBuilder.append(text + "\r\n");
     }

     private boolean mVisitorIsInsideOfficeMath;
     private int mDocTraversalDepth;
     private final StringBuilder mBuilder;
 }
 
```

**Parameters:**
| Parameter | Typ | Beschreibung |
| --- | --- | --- |
| officeMath | [OfficeMath](../../com.aspose.words/officemath/) | Das Objekt, das besucht wird. |

**Returns:**
int - Ein [VisitorAction](../../com.aspose.words/visitoraction/) Wert, der angibt, wie die Aufzählung fortgesetzt werden soll. Der zurückgegebene Wert ist einer der [VisitorAction](../../com.aspose.words/visitoraction/) Konstanten.
### visitOfficeMathStart(OfficeMath officeMath) {#visitOfficeMathStart-com.aspose.words.OfficeMath}
```
public int visitOfficeMathStart(OfficeMath officeMath)
```


Aufgerufen, wenn die Aufzählung eines Office‑Math‑Objekts begonnen hat.

 **Examples:** 

Zeigt, wie die Knotenstruktur jedes Office-Math-Knotens in einem Dokument ausgegeben wird.

```

 public void officeMathToText() throws Exception {
     Document doc = new Document(getMyDir() + "DocumentVisitor-compatible features.docx");
     OfficeMathStructurePrinter visitor = new OfficeMathStructurePrinter();

     // When we get a composite node to accept a document visitor, the visitor visits the accepting node,
     // and then traverses all the node's children in a depth-first manner.
     // The visitor can read and modify each visited node.
     doc.accept(visitor);

     System.out.println(visitor.getText());
 }

 /// 
 /// Traverses a node's non-binary tree of child nodes.
 /// Creates a map in the form of a string of all encountered OfficeMath nodes and their children.
 /// 
 public static class OfficeMathStructurePrinter extends DocumentVisitor {
     public OfficeMathStructurePrinter() {
         mBuilder = new StringBuilder();
         mVisitorIsInsideOfficeMath = false;
     }

     /// 
     /// Gets the plain text of the document that was accumulated by the visitor.
     /// 
     public String getText() {
         return mBuilder.toString();
     }

     /// 
     /// Called when a Run node is encountered in the document.
     /// 
     public int visitRun(final Run run) {
         if (mVisitorIsInsideOfficeMath) {
             indentAndAppendLine("[Run] \"" + run.getText() + "\"");
         }

         return VisitorAction.CONTINUE;
     }

     /// 
     /// Called when an OfficeMath node is encountered in the document.
     /// 
     public int visitOfficeMathStart(final OfficeMath officeMath) {
         indentAndAppendLine("[OfficeMath start] Math object type: " + officeMath.getMathObjectType());
         mDocTraversalDepth++;
         mVisitorIsInsideOfficeMath = true;

         return VisitorAction.CONTINUE;
     }

     /// 
     /// Called after all the child nodes of an OfficeMath node have been visited.
     /// 
     public int visitOfficeMathEnd(final OfficeMath officeMath) {
         mDocTraversalDepth--;
         indentAndAppendLine("[OfficeMath end]");
         mVisitorIsInsideOfficeMath = false;

         return VisitorAction.CONTINUE;
     }

     /// 
     /// Append a line to the StringBuilder and indent it depending on how deep the visitor is into the document tree.
     /// 
     /// 
     private void indentAndAppendLine(final String text) {
         for (int i = 0; i < mDocTraversalDepth; i++) {
             mBuilder.append("|  ");
         }

         mBuilder.append(text + "\r\n");
     }

     private boolean mVisitorIsInsideOfficeMath;
     private int mDocTraversalDepth;
     private final StringBuilder mBuilder;
 }
 
```

**Parameters:**
| Parameter | Typ | Beschreibung |
| --- | --- | --- |
| officeMath | [OfficeMath](../../com.aspose.words/officemath/) | Das Objekt, das besucht wird. |

**Returns:**
int - Ein [VisitorAction](../../com.aspose.words/visitoraction/) Wert, der angibt, wie die Aufzählung fortgesetzt werden soll. Der zurückgegebene Wert ist einer der [VisitorAction](../../com.aspose.words/visitoraction/) Konstanten.
### visitParagraphEnd(Paragraph paragraph) {#visitParagraphEnd-com.aspose.words.Paragraph}
```
public int visitParagraphEnd(Paragraph paragraph)
```


Aufgerufen, wenn die Aufzählung eines Absatzes abgeschlossen ist.

 **Examples:** 

Zeigt, wie ein DocumentVisitor verwendet wird, um die Knotenstruktur eines Dokuments auszugeben.

```

 public void docStructureToText() throws Exception {
     Document doc = new Document(getMyDir() + "DocumentVisitor-compatible features.docx");
     DocStructurePrinter visitor = new DocStructurePrinter();

     // When we get a composite node to accept a document visitor, the visitor visits the accepting node,
     // and then traverses all the node's children in a depth-first manner.
     // The visitor can read and modify each visited node.
     doc.accept(visitor);

     System.out.println(visitor.getText());
 }

 /// 
 /// Traverses a node's tree of child nodes.
 /// Creates a map of this tree in the form of a string.
 /// 
 public static class DocStructurePrinter extends DocumentVisitor {
     public DocStructurePrinter() {
         mAcceptingNodeChildTree = new StringBuilder();
     }

     public String getText() {
         return mAcceptingNodeChildTree.toString();
     }

     /// 
     /// Called when a Document node is encountered.
     /// 
     public int visitDocumentStart(Document doc) {
         int childNodeCount = doc.getChildNodes(NodeType.ANY, true).getCount();

         indentAndAppendLine("[Document start] Child nodes: " + childNodeCount);
         mDocTraversalDepth++;

         // Allow the visitor to continue visiting other nodes.
         return VisitorAction.CONTINUE;
     }

     /// 
     /// Called after all the child nodes of a Document node have been visited.
     /// 
     public int visitDocumentEnd(Document doc) {
         mDocTraversalDepth--;
         indentAndAppendLine("[Document end]");

         return VisitorAction.CONTINUE;
     }

     /// 
     /// Called when a Section node is encountered in the document.
     /// 
     public int visitSectionStart(final Section section) {
         // Get the index of our section within the document
         NodeCollection docSections = section.getDocument().getChildNodes(NodeType.SECTION, false);
         int sectionIndex = docSections.indexOf(section);

         indentAndAppendLine("[Section start] Section index: " + sectionIndex);
         mDocTraversalDepth++;

         return VisitorAction.CONTINUE;
     }

     /// 
     /// Called after all the child nodes of a Section node have been visited.
     /// 
     public int visitSectionEnd(final Section section) {
         mDocTraversalDepth--;
         indentAndAppendLine("[Section end]");

         return VisitorAction.CONTINUE;
     }

     /// 
     /// Called when a Body node is encountered in the document.
     /// 
     public int visitBodyStart(final Body body) {
         int paragraphCount = body.getParagraphs().getCount();
         indentAndAppendLine("[Body start] Paragraphs: " + paragraphCount);
         mDocTraversalDepth++;

         return VisitorAction.CONTINUE;
     }

     /// 
     /// Called after all the child nodes of a Body node have been visited.
     /// 
     public int visitBodyEnd(final Body body) {
         mDocTraversalDepth--;
         indentAndAppendLine("[Body end]");

         return VisitorAction.CONTINUE;
     }

     /// 
     /// Called when a Paragraph node is encountered in the document.
     /// 
     public int visitParagraphStart(final Paragraph paragraph) {
         indentAndAppendLine("[Paragraph start]");
         mDocTraversalDepth++;

         return VisitorAction.CONTINUE;
     }

     /// 
     /// Called after all the child nodes of a Paragraph node have been visited.
     /// 
     public int visitParagraphEnd(final Paragraph paragraph) {
         mDocTraversalDepth--;
         indentAndAppendLine("[Paragraph end]");

         return VisitorAction.CONTINUE;
     }

     /// 
     /// Called when a Run node is encountered in the document.
     /// 
     public int visitRun(final Run run) {
         indentAndAppendLine("[Run] \"" + run.getText() + "\"");

         return VisitorAction.CONTINUE;
     }

     /// 
     /// Called when a SubDocument node is encountered in the document.
     /// 
     public int visitSubDocument(final SubDocument subDocument) {
         indentAndAppendLine("[SubDocument]");

         return VisitorAction.CONTINUE;
     }

     /// 
     /// Called when a SubDocument node is encountered in the document.
     /// 
     public int visitStructuredDocumentTagRangeStart(StructuredDocumentTagRangeStart sdtRangeStart)
     {
         indentAndAppendLine("[SdtRangeStart]");

         return VisitorAction.CONTINUE;
     }

     /// 
     /// Called when a SubDocument node is encountered in the document.
     /// 
     public int visitStructuredDocumentTagRangeEnd(StructuredDocumentTagRangeEnd sdtRangeEnd)
     {
         indentAndAppendLine("[SdtRangeEnd]");

         return VisitorAction.CONTINUE;
     }

     /// 
     /// Append a line to the StringBuilder and indent it depending on how deep the visitor is into the document tree.
     /// 
     /// 
     private void indentAndAppendLine(final String text) {
         for (int i = 0; i < mDocTraversalDepth; i++) {
             mAcceptingNodeChildTree.append("|  ");
         }

         mAcceptingNodeChildTree.append(text + "\r\n");
     }

     private int mDocTraversalDepth;
     private final StringBuilder mAcceptingNodeChildTree;
 }
 
```

**Parameters:**
| Parameter | Typ | Beschreibung |
| --- | --- | --- |
| paragraph | [Paragraph](../../com.aspose.words/paragraph/) | Das Objekt, das besucht wird. |

**Returns:**
int - Ein [VisitorAction](../../com.aspose.words/visitoraction/) Wert, der angibt, wie die Aufzählung fortgesetzt werden soll. Der zurückgegebene Wert ist einer der [VisitorAction](../../com.aspose.words/visitoraction/) Konstanten.
### visitParagraphStart(Paragraph paragraph) {#visitParagraphStart-com.aspose.words.Paragraph}
```
public int visitParagraphStart(Paragraph paragraph)
```


Aufgerufen, wenn die Aufzählung eines Absatzes begonnen hat.

 **Examples:** 

Zeigt, wie ein DocumentVisitor verwendet wird, um die Knotenstruktur eines Dokuments auszugeben.

```

 public void docStructureToText() throws Exception {
     Document doc = new Document(getMyDir() + "DocumentVisitor-compatible features.docx");
     DocStructurePrinter visitor = new DocStructurePrinter();

     // When we get a composite node to accept a document visitor, the visitor visits the accepting node,
     // and then traverses all the node's children in a depth-first manner.
     // The visitor can read and modify each visited node.
     doc.accept(visitor);

     System.out.println(visitor.getText());
 }

 /// 
 /// Traverses a node's tree of child nodes.
 /// Creates a map of this tree in the form of a string.
 /// 
 public static class DocStructurePrinter extends DocumentVisitor {
     public DocStructurePrinter() {
         mAcceptingNodeChildTree = new StringBuilder();
     }

     public String getText() {
         return mAcceptingNodeChildTree.toString();
     }

     /// 
     /// Called when a Document node is encountered.
     /// 
     public int visitDocumentStart(Document doc) {
         int childNodeCount = doc.getChildNodes(NodeType.ANY, true).getCount();

         indentAndAppendLine("[Document start] Child nodes: " + childNodeCount);
         mDocTraversalDepth++;

         // Allow the visitor to continue visiting other nodes.
         return VisitorAction.CONTINUE;
     }

     /// 
     /// Called after all the child nodes of a Document node have been visited.
     /// 
     public int visitDocumentEnd(Document doc) {
         mDocTraversalDepth--;
         indentAndAppendLine("[Document end]");

         return VisitorAction.CONTINUE;
     }

     /// 
     /// Called when a Section node is encountered in the document.
     /// 
     public int visitSectionStart(final Section section) {
         // Get the index of our section within the document
         NodeCollection docSections = section.getDocument().getChildNodes(NodeType.SECTION, false);
         int sectionIndex = docSections.indexOf(section);

         indentAndAppendLine("[Section start] Section index: " + sectionIndex);
         mDocTraversalDepth++;

         return VisitorAction.CONTINUE;
     }

     /// 
     /// Called after all the child nodes of a Section node have been visited.
     /// 
     public int visitSectionEnd(final Section section) {
         mDocTraversalDepth--;
         indentAndAppendLine("[Section end]");

         return VisitorAction.CONTINUE;
     }

     /// 
     /// Called when a Body node is encountered in the document.
     /// 
     public int visitBodyStart(final Body body) {
         int paragraphCount = body.getParagraphs().getCount();
         indentAndAppendLine("[Body start] Paragraphs: " + paragraphCount);
         mDocTraversalDepth++;

         return VisitorAction.CONTINUE;
     }

     /// 
     /// Called after all the child nodes of a Body node have been visited.
     /// 
     public int visitBodyEnd(final Body body) {
         mDocTraversalDepth--;
         indentAndAppendLine("[Body end]");

         return VisitorAction.CONTINUE;
     }

     /// 
     /// Called when a Paragraph node is encountered in the document.
     /// 
     public int visitParagraphStart(final Paragraph paragraph) {
         indentAndAppendLine("[Paragraph start]");
         mDocTraversalDepth++;

         return VisitorAction.CONTINUE;
     }

     /// 
     /// Called after all the child nodes of a Paragraph node have been visited.
     /// 
     public int visitParagraphEnd(final Paragraph paragraph) {
         mDocTraversalDepth--;
         indentAndAppendLine("[Paragraph end]");

         return VisitorAction.CONTINUE;
     }

     /// 
     /// Called when a Run node is encountered in the document.
     /// 
     public int visitRun(final Run run) {
         indentAndAppendLine("[Run] \"" + run.getText() + "\"");

         return VisitorAction.CONTINUE;
     }

     /// 
     /// Called when a SubDocument node is encountered in the document.
     /// 
     public int visitSubDocument(final SubDocument subDocument) {
         indentAndAppendLine("[SubDocument]");

         return VisitorAction.CONTINUE;
     }

     /// 
     /// Called when a SubDocument node is encountered in the document.
     /// 
     public int visitStructuredDocumentTagRangeStart(StructuredDocumentTagRangeStart sdtRangeStart)
     {
         indentAndAppendLine("[SdtRangeStart]");

         return VisitorAction.CONTINUE;
     }

     /// 
     /// Called when a SubDocument node is encountered in the document.
     /// 
     public int visitStructuredDocumentTagRangeEnd(StructuredDocumentTagRangeEnd sdtRangeEnd)
     {
         indentAndAppendLine("[SdtRangeEnd]");

         return VisitorAction.CONTINUE;
     }

     /// 
     /// Append a line to the StringBuilder and indent it depending on how deep the visitor is into the document tree.
     /// 
     /// 
     private void indentAndAppendLine(final String text) {
         for (int i = 0; i < mDocTraversalDepth; i++) {
             mAcceptingNodeChildTree.append("|  ");
         }

         mAcceptingNodeChildTree.append(text + "\r\n");
     }

     private int mDocTraversalDepth;
     private final StringBuilder mAcceptingNodeChildTree;
 }
 
```

Zeigt, wie man eine DocumentVisitor‑Implementierung verwendet, um allen versteckten Inhalt aus einem Dokument zu entfernen.

```

 public void removeHiddenContentFromDocument() throws Exception {
     Document doc = new Document(getMyDir() + "Hidden content.docx");
     RemoveHiddenContentVisitor hiddenContentRemover = new RemoveHiddenContentVisitor();

     // Below are three types of fields which can accept a document visitor,
     // which will allow it to visit the accepting node, and then traverse its child nodes in a depth-first manner.
     // 1 -  Paragraph node:
     Paragraph para = (Paragraph) doc.getChild(NodeType.PARAGRAPH, 4, true);
     para.accept(hiddenContentRemover);

     // 2 -  Table node:
     Table table = doc.getFirstSection().getBody().getTables().get(0);
     table.accept(hiddenContentRemover);

     // 3 -  Document node:
     doc.accept(hiddenContentRemover);

     doc.save(getArtifactsDir() + "Font.RemoveHiddenContentFromDocument.docx");
 }

 /// 
 /// Removes all visited nodes marked as "hidden content".
 /// 
 public static class RemoveHiddenContentVisitor extends DocumentVisitor {
     /// 
     /// Called when a FieldStart node is encountered in the document.
     /// 
     public int visitFieldStart(FieldStart fieldStart) {
         if (fieldStart.getFont().getHidden())
             fieldStart.remove();

         return VisitorAction.CONTINUE;
     }

     /// 
     /// Called when a FieldEnd node is encountered in the document.
     /// 
     public int visitFieldEnd(FieldEnd fieldEnd) {
         if (fieldEnd.getFont().getHidden())
             fieldEnd.remove();

         return VisitorAction.CONTINUE;
     }

     /// 
     /// Called when a FieldSeparator node is encountered in the document.
     /// 
     public int visitFieldSeparator(FieldSeparator fieldSeparator) {
         if (fieldSeparator.getFont().getHidden())
             fieldSeparator.remove();

         return VisitorAction.CONTINUE;
     }

     /// 
     /// Called when a Run node is encountered in the document.
     /// 
     public int visitRun(Run run) {
         if (run.getFont().getHidden())
             run.remove();

         return VisitorAction.CONTINUE;
     }

     /// 
     /// Called when a Paragraph node is encountered in the document.
     /// 
     public int visitParagraphStart(Paragraph paragraph) {
         if (paragraph.getParagraphBreakFont().getHidden())
             paragraph.remove();

         return VisitorAction.CONTINUE;
     }

     /// 
     /// Called when a FormField is encountered in the document.
     /// 
     public int visitFormField(FormField formField) {
         if (formField.getFont().getHidden())
             formField.remove();

         return VisitorAction.CONTINUE;
     }

     /// 
     /// Called when a GroupShape is encountered in the document.
     /// 
     public int visitGroupShapeStart(GroupShape groupShape) {
         if (groupShape.getFont().getHidden())
             groupShape.remove();

         return VisitorAction.CONTINUE;
     }

     /// 
     /// Called when a Shape is encountered in the document.
     /// 
     public int visitShapeStart(Shape shape) {
         if (shape.getFont().getHidden())
             shape.remove();

         return VisitorAction.CONTINUE;
     }

     /// 
     /// Called when a Comment is encountered in the document.
     /// 
     public int visitCommentStart(Comment comment) {
         if (comment.getFont().getHidden())
             comment.remove();

         return VisitorAction.CONTINUE;
     }

     /// 
     /// Called when a Footnote is encountered in the document.
     /// 
     public int visitFootnoteStart(Footnote footnote) {
         if (footnote.getFont().getHidden())
             footnote.remove();

         return VisitorAction.CONTINUE;
     }

     /// 
     /// Called when a SpecialCharacter is encountered in the document.
     /// 
     public int visitSpecialChar(SpecialChar specialChar) {
         if (specialChar.getFont().getHidden())
             specialChar.remove();

         return VisitorAction.CONTINUE;
     }

     /// 
     /// Called when visiting of a Table node is ended in the document.
     /// 
     public int visitTableEnd(Table table) {
         // The content inside table cells may have the hidden content flag, but the tables themselves cannot.
         // If this table had nothing but hidden content, this visitor would have removed all of it,
         // and there would be no child nodes left.
         // Thus, we can also treat the table itself as hidden content and remove it.
         // Tables which are empty but do not have hidden content will have cells with empty paragraphs inside,
         // which this visitor will not remove.
         if (!table.hasChildNodes())
             table.remove();

         return VisitorAction.CONTINUE;
     }

     /// 
     /// Called when visiting of a Cell node is ended in the document.
     /// 
     public int visitCellEnd(Cell cell) {
         if (!cell.hasChildNodes() && cell.getParentNode() != null)
             cell.remove();

         return VisitorAction.CONTINUE;
     }

     /// 
     /// Called when visiting of a Row node is ended in the document.
     /// 
     public int visitRowEnd(Row row) {
         if (!row.hasChildNodes() && row.getParentNode() != null)
             row.remove();

         return VisitorAction.CONTINUE;
     }
 }
 
```

**Parameters:**
| Parameter | Typ | Beschreibung |
| --- | --- | --- |
| paragraph | [Paragraph](../../com.aspose.words/paragraph/) | Das Objekt, das besucht wird. |

**Returns:**
int - Ein [VisitorAction](../../com.aspose.words/visitoraction/) Wert, der angibt, wie die Aufzählung fortgesetzt werden soll. Der zurückgegebene Wert ist einer der [VisitorAction](../../com.aspose.words/visitoraction/) Konstanten.
### visitRowEnd(Row row) {#visitRowEnd-com.aspose.words.Row}
```
public int visitRowEnd(Row row)
```


Aufgerufen, wenn die Aufzählung einer Tabellenzeile abgeschlossen ist.

 **Examples:** 

Zeigt, wie man die Knotenstruktur jeder Tabelle in einem Dokument ausgibt.

```

 public void tableToText() throws Exception {
     Document doc = new Document(getMyDir() + "DocumentVisitor-compatible features.docx");
     TableStructurePrinter visitor = new TableStructurePrinter();

     // When we get a composite node to accept a document visitor, the visitor visits the accepting node,
     // and then traverses all the node's children in a depth-first manner.
     // The visitor can read and modify each visited node.
     doc.accept(visitor);

     System.out.println(visitor.getText());
 }

 /// 
 /// Traverses a node's non-binary tree of child nodes.
 /// Creates a map in the form of a string of all encountered Table nodes and their children.
 /// 
 public static class TableStructurePrinter extends DocumentVisitor {
     public TableStructurePrinter() {
         mVisitedTables = new StringBuilder();
         mVisitorIsInsideTable = false;
     }

     public String getText() {
         return mVisitedTables.toString();
     }

     /// 
     /// Called when a Run node is encountered in the document.
     /// Runs that are not within tables are not recorded.
     /// 
     public int visitRun(Run run) {
         if (mVisitorIsInsideTable) indentAndAppendLine("[Run] \"" + run.getText() + "\"");

         return VisitorAction.CONTINUE;
     }

     /// 
     /// Called when a Table is encountered in the document.
     /// 
     public int visitTableStart(final Table table) {
         int rows = 0;
         int columns = 0;

         if (table.getRows().getCount() > 0) {
             rows = table.getRows().getCount();
             columns = table.getFirstRow().getCount();
         }

         indentAndAppendLine("[Table start] Size: " + rows + "x" + columns);
         mDocTraversalDepth++;
         mVisitorIsInsideTable = true;

         return VisitorAction.CONTINUE;
     }

     /// 
     /// Called after all the child nodes of a Table node have been visited.
     /// 
     public int visitTableEnd(final Table table) {
         mDocTraversalDepth--;
         indentAndAppendLine("[Table end]");
         mVisitorIsInsideTable = false;

         return VisitorAction.CONTINUE;
     }

     /// 
     /// Called when a Row node is encountered in the document.
     /// 
     public int visitRowStart(final Row row) {
         String rowContents = row.getText().replaceAll("\\u0007", ", ").replaceAll(", , ", "");
         int rowWidth = row.indexOf(row.getLastCell()) + 1;
         int rowIndex = row.getParentTable().indexOf(row);
         String rowStatusInTable = row.isFirstRow() && row.isLastRow() ? "only" : row.isFirstRow() ? "first" : row.isLastRow() ? "last" : "";
         if (!"".equals(rowStatusInTable)) {
             rowStatusInTable = MessageFormat.format(", the {0} row in this table,", rowStatusInTable);
         }

         indentAndAppendLine(MessageFormat.format("[Row start] Row #{0}{1} width {2}, \"{3}\"", ++rowIndex, rowStatusInTable, rowWidth, rowContents));
         mDocTraversalDepth++;

         return VisitorAction.CONTINUE;
     }

     /// 
     /// Called after all the child nodes of a Row node have been visited.
     /// 
     public int visitRowEnd(final Row row) {
         mDocTraversalDepth--;
         indentAndAppendLine("[Row end]");

         return VisitorAction.CONTINUE;
     }

     /// 
     /// Called when a Cell node is encountered in the document.
     /// 
     public int visitCellStart(final Cell cell) {
         Row row = cell.getParentRow();
         Table table = row.getParentTable();
         String cellStatusInRow = cell.isFirstCell() && cell.isLastCell() ? "only" : cell.isFirstCell() ? "first" : cell.isLastCell() ? "last" : "";
         if (!"".equals(cellStatusInRow)) {
             cellStatusInRow = MessageFormat.format(", the {0} cell in this row", cellStatusInRow);
         }

         indentAndAppendLine(MessageFormat.format("[Cell start] Row {0}, Col {1}{2}", table.indexOf(row) + 1, row.indexOf(cell) + 1, cellStatusInRow));
         mDocTraversalDepth++;

         return VisitorAction.CONTINUE;
     }

     /// 
     /// Called after all the child nodes of a Cell node have been visited.
     /// 
     public int visitCellEnd(final Cell cell) {
         mDocTraversalDepth--;
         indentAndAppendLine("[Cell end]");
         return VisitorAction.CONTINUE;
     }

     /// 
     /// Append a line to the StringBuilder, and indent it depending on how deep the visitor is
     /// into the current table's tree of child nodes.
     /// 
     /// 
     private void indentAndAppendLine(final String text) {
         for (int i = 0; i < mDocTraversalDepth; i++) {
             mVisitedTables.append("|  ");
         }

         mVisitedTables.append(text + "\r\n");
     }

     private boolean mVisitorIsInsideTable;
     private int mDocTraversalDepth;
     private final  StringBuilder mVisitedTables;
 }
 
```

Zeigt, wie man eine DocumentVisitor‑Implementierung verwendet, um allen versteckten Inhalt aus einem Dokument zu entfernen.

```

 public void removeHiddenContentFromDocument() throws Exception {
     Document doc = new Document(getMyDir() + "Hidden content.docx");
     RemoveHiddenContentVisitor hiddenContentRemover = new RemoveHiddenContentVisitor();

     // Below are three types of fields which can accept a document visitor,
     // which will allow it to visit the accepting node, and then traverse its child nodes in a depth-first manner.
     // 1 -  Paragraph node:
     Paragraph para = (Paragraph) doc.getChild(NodeType.PARAGRAPH, 4, true);
     para.accept(hiddenContentRemover);

     // 2 -  Table node:
     Table table = doc.getFirstSection().getBody().getTables().get(0);
     table.accept(hiddenContentRemover);

     // 3 -  Document node:
     doc.accept(hiddenContentRemover);

     doc.save(getArtifactsDir() + "Font.RemoveHiddenContentFromDocument.docx");
 }

 /// 
 /// Removes all visited nodes marked as "hidden content".
 /// 
 public static class RemoveHiddenContentVisitor extends DocumentVisitor {
     /// 
     /// Called when a FieldStart node is encountered in the document.
     /// 
     public int visitFieldStart(FieldStart fieldStart) {
         if (fieldStart.getFont().getHidden())
             fieldStart.remove();

         return VisitorAction.CONTINUE;
     }

     /// 
     /// Called when a FieldEnd node is encountered in the document.
     /// 
     public int visitFieldEnd(FieldEnd fieldEnd) {
         if (fieldEnd.getFont().getHidden())
             fieldEnd.remove();

         return VisitorAction.CONTINUE;
     }

     /// 
     /// Called when a FieldSeparator node is encountered in the document.
     /// 
     public int visitFieldSeparator(FieldSeparator fieldSeparator) {
         if (fieldSeparator.getFont().getHidden())
             fieldSeparator.remove();

         return VisitorAction.CONTINUE;
     }

     /// 
     /// Called when a Run node is encountered in the document.
     /// 
     public int visitRun(Run run) {
         if (run.getFont().getHidden())
             run.remove();

         return VisitorAction.CONTINUE;
     }

     /// 
     /// Called when a Paragraph node is encountered in the document.
     /// 
     public int visitParagraphStart(Paragraph paragraph) {
         if (paragraph.getParagraphBreakFont().getHidden())
             paragraph.remove();

         return VisitorAction.CONTINUE;
     }

     /// 
     /// Called when a FormField is encountered in the document.
     /// 
     public int visitFormField(FormField formField) {
         if (formField.getFont().getHidden())
             formField.remove();

         return VisitorAction.CONTINUE;
     }

     /// 
     /// Called when a GroupShape is encountered in the document.
     /// 
     public int visitGroupShapeStart(GroupShape groupShape) {
         if (groupShape.getFont().getHidden())
             groupShape.remove();

         return VisitorAction.CONTINUE;
     }

     /// 
     /// Called when a Shape is encountered in the document.
     /// 
     public int visitShapeStart(Shape shape) {
         if (shape.getFont().getHidden())
             shape.remove();

         return VisitorAction.CONTINUE;
     }

     /// 
     /// Called when a Comment is encountered in the document.
     /// 
     public int visitCommentStart(Comment comment) {
         if (comment.getFont().getHidden())
             comment.remove();

         return VisitorAction.CONTINUE;
     }

     /// 
     /// Called when a Footnote is encountered in the document.
     /// 
     public int visitFootnoteStart(Footnote footnote) {
         if (footnote.getFont().getHidden())
             footnote.remove();

         return VisitorAction.CONTINUE;
     }

     /// 
     /// Called when a SpecialCharacter is encountered in the document.
     /// 
     public int visitSpecialChar(SpecialChar specialChar) {
         if (specialChar.getFont().getHidden())
             specialChar.remove();

         return VisitorAction.CONTINUE;
     }

     /// 
     /// Called when visiting of a Table node is ended in the document.
     /// 
     public int visitTableEnd(Table table) {
         // The content inside table cells may have the hidden content flag, but the tables themselves cannot.
         // If this table had nothing but hidden content, this visitor would have removed all of it,
         // and there would be no child nodes left.
         // Thus, we can also treat the table itself as hidden content and remove it.
         // Tables which are empty but do not have hidden content will have cells with empty paragraphs inside,
         // which this visitor will not remove.
         if (!table.hasChildNodes())
             table.remove();

         return VisitorAction.CONTINUE;
     }

     /// 
     /// Called when visiting of a Cell node is ended in the document.
     /// 
     public int visitCellEnd(Cell cell) {
         if (!cell.hasChildNodes() && cell.getParentNode() != null)
             cell.remove();

         return VisitorAction.CONTINUE;
     }

     /// 
     /// Called when visiting of a Row node is ended in the document.
     /// 
     public int visitRowEnd(Row row) {
         if (!row.hasChildNodes() && row.getParentNode() != null)
             row.remove();

         return VisitorAction.CONTINUE;
     }
 }
 
```

**Parameters:**
| Parameter | Typ | Beschreibung |
| --- | --- | --- |
| row | [Row](../../com.aspose.words/row/) | Das Objekt, das besucht wird. |

**Returns:**
int - Ein [VisitorAction](../../com.aspose.words/visitoraction/) Wert, der angibt, wie die Aufzählung fortgesetzt werden soll. Der zurückgegebene Wert ist einer der [VisitorAction](../../com.aspose.words/visitoraction/) Konstanten.
### visitRowStart(Row row) {#visitRowStart-com.aspose.words.Row}
```
public int visitRowStart(Row row)
```


Aufgerufen, wenn die Aufzählung einer Tabellenzeile begonnen hat.

 **Examples:** 

Zeigt, wie man die Knotenstruktur jeder Tabelle in einem Dokument ausgibt.

```

 public void tableToText() throws Exception {
     Document doc = new Document(getMyDir() + "DocumentVisitor-compatible features.docx");
     TableStructurePrinter visitor = new TableStructurePrinter();

     // When we get a composite node to accept a document visitor, the visitor visits the accepting node,
     // and then traverses all the node's children in a depth-first manner.
     // The visitor can read and modify each visited node.
     doc.accept(visitor);

     System.out.println(visitor.getText());
 }

 /// 
 /// Traverses a node's non-binary tree of child nodes.
 /// Creates a map in the form of a string of all encountered Table nodes and their children.
 /// 
 public static class TableStructurePrinter extends DocumentVisitor {
     public TableStructurePrinter() {
         mVisitedTables = new StringBuilder();
         mVisitorIsInsideTable = false;
     }

     public String getText() {
         return mVisitedTables.toString();
     }

     /// 
     /// Called when a Run node is encountered in the document.
     /// Runs that are not within tables are not recorded.
     /// 
     public int visitRun(Run run) {
         if (mVisitorIsInsideTable) indentAndAppendLine("[Run] \"" + run.getText() + "\"");

         return VisitorAction.CONTINUE;
     }

     /// 
     /// Called when a Table is encountered in the document.
     /// 
     public int visitTableStart(final Table table) {
         int rows = 0;
         int columns = 0;

         if (table.getRows().getCount() > 0) {
             rows = table.getRows().getCount();
             columns = table.getFirstRow().getCount();
         }

         indentAndAppendLine("[Table start] Size: " + rows + "x" + columns);
         mDocTraversalDepth++;
         mVisitorIsInsideTable = true;

         return VisitorAction.CONTINUE;
     }

     /// 
     /// Called after all the child nodes of a Table node have been visited.
     /// 
     public int visitTableEnd(final Table table) {
         mDocTraversalDepth--;
         indentAndAppendLine("[Table end]");
         mVisitorIsInsideTable = false;

         return VisitorAction.CONTINUE;
     }

     /// 
     /// Called when a Row node is encountered in the document.
     /// 
     public int visitRowStart(final Row row) {
         String rowContents = row.getText().replaceAll("\\u0007", ", ").replaceAll(", , ", "");
         int rowWidth = row.indexOf(row.getLastCell()) + 1;
         int rowIndex = row.getParentTable().indexOf(row);
         String rowStatusInTable = row.isFirstRow() && row.isLastRow() ? "only" : row.isFirstRow() ? "first" : row.isLastRow() ? "last" : "";
         if (!"".equals(rowStatusInTable)) {
             rowStatusInTable = MessageFormat.format(", the {0} row in this table,", rowStatusInTable);
         }

         indentAndAppendLine(MessageFormat.format("[Row start] Row #{0}{1} width {2}, \"{3}\"", ++rowIndex, rowStatusInTable, rowWidth, rowContents));
         mDocTraversalDepth++;

         return VisitorAction.CONTINUE;
     }

     /// 
     /// Called after all the child nodes of a Row node have been visited.
     /// 
     public int visitRowEnd(final Row row) {
         mDocTraversalDepth--;
         indentAndAppendLine("[Row end]");

         return VisitorAction.CONTINUE;
     }

     /// 
     /// Called when a Cell node is encountered in the document.
     /// 
     public int visitCellStart(final Cell cell) {
         Row row = cell.getParentRow();
         Table table = row.getParentTable();
         String cellStatusInRow = cell.isFirstCell() && cell.isLastCell() ? "only" : cell.isFirstCell() ? "first" : cell.isLastCell() ? "last" : "";
         if (!"".equals(cellStatusInRow)) {
             cellStatusInRow = MessageFormat.format(", the {0} cell in this row", cellStatusInRow);
         }

         indentAndAppendLine(MessageFormat.format("[Cell start] Row {0}, Col {1}{2}", table.indexOf(row) + 1, row.indexOf(cell) + 1, cellStatusInRow));
         mDocTraversalDepth++;

         return VisitorAction.CONTINUE;
     }

     /// 
     /// Called after all the child nodes of a Cell node have been visited.
     /// 
     public int visitCellEnd(final Cell cell) {
         mDocTraversalDepth--;
         indentAndAppendLine("[Cell end]");
         return VisitorAction.CONTINUE;
     }

     /// 
     /// Append a line to the StringBuilder, and indent it depending on how deep the visitor is
     /// into the current table's tree of child nodes.
     /// 
     /// 
     private void indentAndAppendLine(final String text) {
         for (int i = 0; i < mDocTraversalDepth; i++) {
             mVisitedTables.append("|  ");
         }

         mVisitedTables.append(text + "\r\n");
     }

     private boolean mVisitorIsInsideTable;
     private int mDocTraversalDepth;
     private final  StringBuilder mVisitedTables;
 }
 
```

**Parameters:**
| Parameter | Typ | Beschreibung |
| --- | --- | --- |
| row | [Row](../../com.aspose.words/row/) | Das Objekt, das besucht wird. |

**Returns:**
int - Ein [VisitorAction](../../com.aspose.words/visitoraction/) Wert, der angibt, wie die Aufzählung fortgesetzt werden soll. Der zurückgegebene Wert ist einer der [VisitorAction](../../com.aspose.words/visitoraction/) Konstanten.
### visitRun(Run run) {#visitRun-com.aspose.words.Run}
```
public int visitRun(Run run)
```


Aufgerufen, wenn ein Textlauf im Dokument gefunden wird.

 **Examples:** 

Zeigt, wie ein DocumentVisitor verwendet wird, um die Knotenstruktur eines Dokuments auszugeben.

```

 public void docStructureToText() throws Exception {
     Document doc = new Document(getMyDir() + "DocumentVisitor-compatible features.docx");
     DocStructurePrinter visitor = new DocStructurePrinter();

     // When we get a composite node to accept a document visitor, the visitor visits the accepting node,
     // and then traverses all the node's children in a depth-first manner.
     // The visitor can read and modify each visited node.
     doc.accept(visitor);

     System.out.println(visitor.getText());
 }

 /// 
 /// Traverses a node's tree of child nodes.
 /// Creates a map of this tree in the form of a string.
 /// 
 public static class DocStructurePrinter extends DocumentVisitor {
     public DocStructurePrinter() {
         mAcceptingNodeChildTree = new StringBuilder();
     }

     public String getText() {
         return mAcceptingNodeChildTree.toString();
     }

     /// 
     /// Called when a Document node is encountered.
     /// 
     public int visitDocumentStart(Document doc) {
         int childNodeCount = doc.getChildNodes(NodeType.ANY, true).getCount();

         indentAndAppendLine("[Document start] Child nodes: " + childNodeCount);
         mDocTraversalDepth++;

         // Allow the visitor to continue visiting other nodes.
         return VisitorAction.CONTINUE;
     }

     /// 
     /// Called after all the child nodes of a Document node have been visited.
     /// 
     public int visitDocumentEnd(Document doc) {
         mDocTraversalDepth--;
         indentAndAppendLine("[Document end]");

         return VisitorAction.CONTINUE;
     }

     /// 
     /// Called when a Section node is encountered in the document.
     /// 
     public int visitSectionStart(final Section section) {
         // Get the index of our section within the document
         NodeCollection docSections = section.getDocument().getChildNodes(NodeType.SECTION, false);
         int sectionIndex = docSections.indexOf(section);

         indentAndAppendLine("[Section start] Section index: " + sectionIndex);
         mDocTraversalDepth++;

         return VisitorAction.CONTINUE;
     }

     /// 
     /// Called after all the child nodes of a Section node have been visited.
     /// 
     public int visitSectionEnd(final Section section) {
         mDocTraversalDepth--;
         indentAndAppendLine("[Section end]");

         return VisitorAction.CONTINUE;
     }

     /// 
     /// Called when a Body node is encountered in the document.
     /// 
     public int visitBodyStart(final Body body) {
         int paragraphCount = body.getParagraphs().getCount();
         indentAndAppendLine("[Body start] Paragraphs: " + paragraphCount);
         mDocTraversalDepth++;

         return VisitorAction.CONTINUE;
     }

     /// 
     /// Called after all the child nodes of a Body node have been visited.
     /// 
     public int visitBodyEnd(final Body body) {
         mDocTraversalDepth--;
         indentAndAppendLine("[Body end]");

         return VisitorAction.CONTINUE;
     }

     /// 
     /// Called when a Paragraph node is encountered in the document.
     /// 
     public int visitParagraphStart(final Paragraph paragraph) {
         indentAndAppendLine("[Paragraph start]");
         mDocTraversalDepth++;

         return VisitorAction.CONTINUE;
     }

     /// 
     /// Called after all the child nodes of a Paragraph node have been visited.
     /// 
     public int visitParagraphEnd(final Paragraph paragraph) {
         mDocTraversalDepth--;
         indentAndAppendLine("[Paragraph end]");

         return VisitorAction.CONTINUE;
     }

     /// 
     /// Called when a Run node is encountered in the document.
     /// 
     public int visitRun(final Run run) {
         indentAndAppendLine("[Run] \"" + run.getText() + "\"");

         return VisitorAction.CONTINUE;
     }

     /// 
     /// Called when a SubDocument node is encountered in the document.
     /// 
     public int visitSubDocument(final SubDocument subDocument) {
         indentAndAppendLine("[SubDocument]");

         return VisitorAction.CONTINUE;
     }

     /// 
     /// Called when a SubDocument node is encountered in the document.
     /// 
     public int visitStructuredDocumentTagRangeStart(StructuredDocumentTagRangeStart sdtRangeStart)
     {
         indentAndAppendLine("[SdtRangeStart]");

         return VisitorAction.CONTINUE;
     }

     /// 
     /// Called when a SubDocument node is encountered in the document.
     /// 
     public int visitStructuredDocumentTagRangeEnd(StructuredDocumentTagRangeEnd sdtRangeEnd)
     {
         indentAndAppendLine("[SdtRangeEnd]");

         return VisitorAction.CONTINUE;
     }

     /// 
     /// Append a line to the StringBuilder and indent it depending on how deep the visitor is into the document tree.
     /// 
     /// 
     private void indentAndAppendLine(final String text) {
         for (int i = 0; i < mDocTraversalDepth; i++) {
             mAcceptingNodeChildTree.append("|  ");
         }

         mAcceptingNodeChildTree.append(text + "\r\n");
     }

     private int mDocTraversalDepth;
     private final StringBuilder mAcceptingNodeChildTree;
 }
 
```

**Parameters:**
| Parameter | Typ | Beschreibung |
| --- | --- | --- |
| run | [Run](../../com.aspose.words/run/) | Das Objekt, das besucht wird. |

**Returns:**
int - Ein [VisitorAction](../../com.aspose.words/visitoraction/) Wert, der angibt, wie die Aufzählung fortgesetzt werden soll. Der zurückgegebene Wert ist einer der [VisitorAction](../../com.aspose.words/visitoraction/) Konstanten.
### visitSectionEnd(Section section) {#visitSectionEnd-com.aspose.words.Section}
```
public int visitSectionEnd(Section section)
```


Aufgerufen, wenn die Aufzählung eines Abschnitts abgeschlossen ist.

 **Examples:** 

Zeigt, wie ein DocumentVisitor verwendet wird, um die Knotenstruktur eines Dokuments auszugeben.

```

 public void docStructureToText() throws Exception {
     Document doc = new Document(getMyDir() + "DocumentVisitor-compatible features.docx");
     DocStructurePrinter visitor = new DocStructurePrinter();

     // When we get a composite node to accept a document visitor, the visitor visits the accepting node,
     // and then traverses all the node's children in a depth-first manner.
     // The visitor can read and modify each visited node.
     doc.accept(visitor);

     System.out.println(visitor.getText());
 }

 /// 
 /// Traverses a node's tree of child nodes.
 /// Creates a map of this tree in the form of a string.
 /// 
 public static class DocStructurePrinter extends DocumentVisitor {
     public DocStructurePrinter() {
         mAcceptingNodeChildTree = new StringBuilder();
     }

     public String getText() {
         return mAcceptingNodeChildTree.toString();
     }

     /// 
     /// Called when a Document node is encountered.
     /// 
     public int visitDocumentStart(Document doc) {
         int childNodeCount = doc.getChildNodes(NodeType.ANY, true).getCount();

         indentAndAppendLine("[Document start] Child nodes: " + childNodeCount);
         mDocTraversalDepth++;

         // Allow the visitor to continue visiting other nodes.
         return VisitorAction.CONTINUE;
     }

     /// 
     /// Called after all the child nodes of a Document node have been visited.
     /// 
     public int visitDocumentEnd(Document doc) {
         mDocTraversalDepth--;
         indentAndAppendLine("[Document end]");

         return VisitorAction.CONTINUE;
     }

     /// 
     /// Called when a Section node is encountered in the document.
     /// 
     public int visitSectionStart(final Section section) {
         // Get the index of our section within the document
         NodeCollection docSections = section.getDocument().getChildNodes(NodeType.SECTION, false);
         int sectionIndex = docSections.indexOf(section);

         indentAndAppendLine("[Section start] Section index: " + sectionIndex);
         mDocTraversalDepth++;

         return VisitorAction.CONTINUE;
     }

     /// 
     /// Called after all the child nodes of a Section node have been visited.
     /// 
     public int visitSectionEnd(final Section section) {
         mDocTraversalDepth--;
         indentAndAppendLine("[Section end]");

         return VisitorAction.CONTINUE;
     }

     /// 
     /// Called when a Body node is encountered in the document.
     /// 
     public int visitBodyStart(final Body body) {
         int paragraphCount = body.getParagraphs().getCount();
         indentAndAppendLine("[Body start] Paragraphs: " + paragraphCount);
         mDocTraversalDepth++;

         return VisitorAction.CONTINUE;
     }

     /// 
     /// Called after all the child nodes of a Body node have been visited.
     /// 
     public int visitBodyEnd(final Body body) {
         mDocTraversalDepth--;
         indentAndAppendLine("[Body end]");

         return VisitorAction.CONTINUE;
     }

     /// 
     /// Called when a Paragraph node is encountered in the document.
     /// 
     public int visitParagraphStart(final Paragraph paragraph) {
         indentAndAppendLine("[Paragraph start]");
         mDocTraversalDepth++;

         return VisitorAction.CONTINUE;
     }

     /// 
     /// Called after all the child nodes of a Paragraph node have been visited.
     /// 
     public int visitParagraphEnd(final Paragraph paragraph) {
         mDocTraversalDepth--;
         indentAndAppendLine("[Paragraph end]");

         return VisitorAction.CONTINUE;
     }

     /// 
     /// Called when a Run node is encountered in the document.
     /// 
     public int visitRun(final Run run) {
         indentAndAppendLine("[Run] \"" + run.getText() + "\"");

         return VisitorAction.CONTINUE;
     }

     /// 
     /// Called when a SubDocument node is encountered in the document.
     /// 
     public int visitSubDocument(final SubDocument subDocument) {
         indentAndAppendLine("[SubDocument]");

         return VisitorAction.CONTINUE;
     }

     /// 
     /// Called when a SubDocument node is encountered in the document.
     /// 
     public int visitStructuredDocumentTagRangeStart(StructuredDocumentTagRangeStart sdtRangeStart)
     {
         indentAndAppendLine("[SdtRangeStart]");

         return VisitorAction.CONTINUE;
     }

     /// 
     /// Called when a SubDocument node is encountered in the document.
     /// 
     public int visitStructuredDocumentTagRangeEnd(StructuredDocumentTagRangeEnd sdtRangeEnd)
     {
         indentAndAppendLine("[SdtRangeEnd]");

         return VisitorAction.CONTINUE;
     }

     /// 
     /// Append a line to the StringBuilder and indent it depending on how deep the visitor is into the document tree.
     /// 
     /// 
     private void indentAndAppendLine(final String text) {
         for (int i = 0; i < mDocTraversalDepth; i++) {
             mAcceptingNodeChildTree.append("|  ");
         }

         mAcceptingNodeChildTree.append(text + "\r\n");
     }

     private int mDocTraversalDepth;
     private final StringBuilder mAcceptingNodeChildTree;
 }
 
```

**Parameters:**
| Parameter | Typ | Beschreibung |
| --- | --- | --- |
| section | [Section](../../com.aspose.words/section/) | Das Objekt, das besucht wird. |

**Returns:**
int - Ein [VisitorAction](../../com.aspose.words/visitoraction/) Wert, der angibt, wie die Aufzählung fortgesetzt werden soll. Der zurückgegebene Wert ist einer der [VisitorAction](../../com.aspose.words/visitoraction/) Konstanten.
### visitSectionStart(Section section) {#visitSectionStart-com.aspose.words.Section}
```
public int visitSectionStart(Section section)
```


Aufgerufen, wenn die Aufzählung eines Abschnitts begonnen hat.

 **Examples:** 

Zeigt, wie ein DocumentVisitor verwendet wird, um die Knotenstruktur eines Dokuments auszugeben.

```

 public void docStructureToText() throws Exception {
     Document doc = new Document(getMyDir() + "DocumentVisitor-compatible features.docx");
     DocStructurePrinter visitor = new DocStructurePrinter();

     // When we get a composite node to accept a document visitor, the visitor visits the accepting node,
     // and then traverses all the node's children in a depth-first manner.
     // The visitor can read and modify each visited node.
     doc.accept(visitor);

     System.out.println(visitor.getText());
 }

 /// 
 /// Traverses a node's tree of child nodes.
 /// Creates a map of this tree in the form of a string.
 /// 
 public static class DocStructurePrinter extends DocumentVisitor {
     public DocStructurePrinter() {
         mAcceptingNodeChildTree = new StringBuilder();
     }

     public String getText() {
         return mAcceptingNodeChildTree.toString();
     }

     /// 
     /// Called when a Document node is encountered.
     /// 
     public int visitDocumentStart(Document doc) {
         int childNodeCount = doc.getChildNodes(NodeType.ANY, true).getCount();

         indentAndAppendLine("[Document start] Child nodes: " + childNodeCount);
         mDocTraversalDepth++;

         // Allow the visitor to continue visiting other nodes.
         return VisitorAction.CONTINUE;
     }

     /// 
     /// Called after all the child nodes of a Document node have been visited.
     /// 
     public int visitDocumentEnd(Document doc) {
         mDocTraversalDepth--;
         indentAndAppendLine("[Document end]");

         return VisitorAction.CONTINUE;
     }

     /// 
     /// Called when a Section node is encountered in the document.
     /// 
     public int visitSectionStart(final Section section) {
         // Get the index of our section within the document
         NodeCollection docSections = section.getDocument().getChildNodes(NodeType.SECTION, false);
         int sectionIndex = docSections.indexOf(section);

         indentAndAppendLine("[Section start] Section index: " + sectionIndex);
         mDocTraversalDepth++;

         return VisitorAction.CONTINUE;
     }

     /// 
     /// Called after all the child nodes of a Section node have been visited.
     /// 
     public int visitSectionEnd(final Section section) {
         mDocTraversalDepth--;
         indentAndAppendLine("[Section end]");

         return VisitorAction.CONTINUE;
     }

     /// 
     /// Called when a Body node is encountered in the document.
     /// 
     public int visitBodyStart(final Body body) {
         int paragraphCount = body.getParagraphs().getCount();
         indentAndAppendLine("[Body start] Paragraphs: " + paragraphCount);
         mDocTraversalDepth++;

         return VisitorAction.CONTINUE;
     }

     /// 
     /// Called after all the child nodes of a Body node have been visited.
     /// 
     public int visitBodyEnd(final Body body) {
         mDocTraversalDepth--;
         indentAndAppendLine("[Body end]");

         return VisitorAction.CONTINUE;
     }

     /// 
     /// Called when a Paragraph node is encountered in the document.
     /// 
     public int visitParagraphStart(final Paragraph paragraph) {
         indentAndAppendLine("[Paragraph start]");
         mDocTraversalDepth++;

         return VisitorAction.CONTINUE;
     }

     /// 
     /// Called after all the child nodes of a Paragraph node have been visited.
     /// 
     public int visitParagraphEnd(final Paragraph paragraph) {
         mDocTraversalDepth--;
         indentAndAppendLine("[Paragraph end]");

         return VisitorAction.CONTINUE;
     }

     /// 
     /// Called when a Run node is encountered in the document.
     /// 
     public int visitRun(final Run run) {
         indentAndAppendLine("[Run] \"" + run.getText() + "\"");

         return VisitorAction.CONTINUE;
     }

     /// 
     /// Called when a SubDocument node is encountered in the document.
     /// 
     public int visitSubDocument(final SubDocument subDocument) {
         indentAndAppendLine("[SubDocument]");

         return VisitorAction.CONTINUE;
     }

     /// 
     /// Called when a SubDocument node is encountered in the document.
     /// 
     public int visitStructuredDocumentTagRangeStart(StructuredDocumentTagRangeStart sdtRangeStart)
     {
         indentAndAppendLine("[SdtRangeStart]");

         return VisitorAction.CONTINUE;
     }

     /// 
     /// Called when a SubDocument node is encountered in the document.
     /// 
     public int visitStructuredDocumentTagRangeEnd(StructuredDocumentTagRangeEnd sdtRangeEnd)
     {
         indentAndAppendLine("[SdtRangeEnd]");

         return VisitorAction.CONTINUE;
     }

     /// 
     /// Append a line to the StringBuilder and indent it depending on how deep the visitor is into the document tree.
     /// 
     /// 
     private void indentAndAppendLine(final String text) {
         for (int i = 0; i < mDocTraversalDepth; i++) {
             mAcceptingNodeChildTree.append("|  ");
         }

         mAcceptingNodeChildTree.append(text + "\r\n");
     }

     private int mDocTraversalDepth;
     private final StringBuilder mAcceptingNodeChildTree;
 }
 
```

**Parameters:**
| Parameter | Typ | Beschreibung |
| --- | --- | --- |
| section | [Section](../../com.aspose.words/section/) | Das Objekt, das besucht wird. |

**Returns:**
int - Ein [VisitorAction](../../com.aspose.words/visitoraction/) Wert, der angibt, wie die Aufzählung fortgesetzt werden soll. Der zurückgegebene Wert ist einer der [VisitorAction](../../com.aspose.words/visitoraction/) Konstanten.
### visitShapeEnd(Shape shape) {#visitShapeEnd-com.aspose.words.Shape}
```
public int visitShapeEnd(Shape shape)
```


Aufgerufen, wenn die Aufzählung einer Form beendet ist.

 **Examples:** 

Zeigt, wie eine Gruppe von Formen erstellt und ihr Inhalt mit einem Document Visitor ausgegeben wird.

```

 public void groupOfShapes() throws Exception {
     Document doc = new Document();
     DocumentBuilder builder = new DocumentBuilder(doc);

     // If you need to create "NonPrimitive" shapes, such as SingleCornerSnipped, TopCornersSnipped, DiagonalCornersSnipped,
     // TopCornersOneRoundedOneSnipped, SingleCornerRounded, TopCornersRounded, DiagonalCornersRounded
     // please use DocumentBuilder.InsertShape methods.
     Shape balloon = new Shape(doc, ShapeType.BALLOON);
     balloon.setWidth(200.0);
     balloon.setHeight(200.0);
     balloon.setStrokeColor(Color.RED);

     Shape cube = new Shape(doc, ShapeType.CUBE);
     cube.setWidth(100.0);
     cube.setHeight(100.0);
     cube.setStrokeColor(Color.BLUE);

     GroupShape group = new GroupShape(doc);
     group.appendChild(balloon);
     group.appendChild(cube);

     Assert.assertTrue(group.isGroup());
     builder.insertNode(group);

     ShapeInfoPrinter printer = new ShapeInfoPrinter();
     group.accept(printer);

     System.out.println(printer.getText());
 }

 /// 
 /// Prints the contents of a visited shape group to the console.
 /// 
 public static class ShapeInfoPrinter extends DocumentVisitor {
     public ShapeInfoPrinter() {
         mBuilder = new StringBuilder();
     }

     public String getText() {
         return mBuilder.toString();
     }

     public int visitGroupShapeStart(final GroupShape groupShape) {
         mBuilder.append("Shape group started:\r\n");
         return VisitorAction.CONTINUE;
     }

     public int visitGroupShapeEnd(final GroupShape groupShape) {
         mBuilder.append("End of shape group\r\n");
         return VisitorAction.CONTINUE;
     }

     public int visitShapeStart(final Shape shape) {
         mBuilder.append("\tShape - " + shape.getShapeType() + ":\r\n");
         mBuilder.append("\t\tWidth: " + shape.getWidth() + "\r\n");
         mBuilder.append("\t\tHeight: " + shape.getHeight() + "\r\n");
         mBuilder.append("\t\tStroke color: " + shape.getStroke().getColor() + "\r\n");
         mBuilder.append("\t\tFill color: " + shape.getFill().getForeColor() + "\r\n");
         return VisitorAction.CONTINUE;
     }

     public int visitShapeEnd(final Shape shape) {
         mBuilder.append("\tEnd of shape\r\n");
         return VisitorAction.CONTINUE;
     }

     private final StringBuilder mBuilder;
 }
 
```

**Parameters:**
| Parameter | Typ | Beschreibung |
| --- | --- | --- |
| shape | [Shape](../../com.aspose.words/shape/) | Das Objekt, das besucht wird. |

**Returns:**
int - Ein [VisitorAction](../../com.aspose.words/visitoraction/) Wert, der angibt, wie die Aufzählung fortgesetzt werden soll. Der zurückgegebene Wert ist einer der [VisitorAction](../../com.aspose.words/visitoraction/) Konstanten.
### visitShapeStart(Shape shape) {#visitShapeStart-com.aspose.words.Shape}
```
public int visitShapeStart(Shape shape)
```


Aufgerufen, wenn die Aufzählung einer Form begonnen hat.

 **Examples:** 

Zeigt, wie eine Gruppe von Formen erstellt und ihr Inhalt mit einem Document Visitor ausgegeben wird.

```

 public void groupOfShapes() throws Exception {
     Document doc = new Document();
     DocumentBuilder builder = new DocumentBuilder(doc);

     // If you need to create "NonPrimitive" shapes, such as SingleCornerSnipped, TopCornersSnipped, DiagonalCornersSnipped,
     // TopCornersOneRoundedOneSnipped, SingleCornerRounded, TopCornersRounded, DiagonalCornersRounded
     // please use DocumentBuilder.InsertShape methods.
     Shape balloon = new Shape(doc, ShapeType.BALLOON);
     balloon.setWidth(200.0);
     balloon.setHeight(200.0);
     balloon.setStrokeColor(Color.RED);

     Shape cube = new Shape(doc, ShapeType.CUBE);
     cube.setWidth(100.0);
     cube.setHeight(100.0);
     cube.setStrokeColor(Color.BLUE);

     GroupShape group = new GroupShape(doc);
     group.appendChild(balloon);
     group.appendChild(cube);

     Assert.assertTrue(group.isGroup());
     builder.insertNode(group);

     ShapeInfoPrinter printer = new ShapeInfoPrinter();
     group.accept(printer);

     System.out.println(printer.getText());
 }

 /// 
 /// Prints the contents of a visited shape group to the console.
 /// 
 public static class ShapeInfoPrinter extends DocumentVisitor {
     public ShapeInfoPrinter() {
         mBuilder = new StringBuilder();
     }

     public String getText() {
         return mBuilder.toString();
     }

     public int visitGroupShapeStart(final GroupShape groupShape) {
         mBuilder.append("Shape group started:\r\n");
         return VisitorAction.CONTINUE;
     }

     public int visitGroupShapeEnd(final GroupShape groupShape) {
         mBuilder.append("End of shape group\r\n");
         return VisitorAction.CONTINUE;
     }

     public int visitShapeStart(final Shape shape) {
         mBuilder.append("\tShape - " + shape.getShapeType() + ":\r\n");
         mBuilder.append("\t\tWidth: " + shape.getWidth() + "\r\n");
         mBuilder.append("\t\tHeight: " + shape.getHeight() + "\r\n");
         mBuilder.append("\t\tStroke color: " + shape.getStroke().getColor() + "\r\n");
         mBuilder.append("\t\tFill color: " + shape.getFill().getForeColor() + "\r\n");
         return VisitorAction.CONTINUE;
     }

     public int visitShapeEnd(final Shape shape) {
         mBuilder.append("\tEnd of shape\r\n");
         return VisitorAction.CONTINUE;
     }

     private final StringBuilder mBuilder;
 }
 
```

Zeigt, wie man eine DocumentVisitor‑Implementierung verwendet, um allen versteckten Inhalt aus einem Dokument zu entfernen.

```

 public void removeHiddenContentFromDocument() throws Exception {
     Document doc = new Document(getMyDir() + "Hidden content.docx");
     RemoveHiddenContentVisitor hiddenContentRemover = new RemoveHiddenContentVisitor();

     // Below are three types of fields which can accept a document visitor,
     // which will allow it to visit the accepting node, and then traverse its child nodes in a depth-first manner.
     // 1 -  Paragraph node:
     Paragraph para = (Paragraph) doc.getChild(NodeType.PARAGRAPH, 4, true);
     para.accept(hiddenContentRemover);

     // 2 -  Table node:
     Table table = doc.getFirstSection().getBody().getTables().get(0);
     table.accept(hiddenContentRemover);

     // 3 -  Document node:
     doc.accept(hiddenContentRemover);

     doc.save(getArtifactsDir() + "Font.RemoveHiddenContentFromDocument.docx");
 }

 /// 
 /// Removes all visited nodes marked as "hidden content".
 /// 
 public static class RemoveHiddenContentVisitor extends DocumentVisitor {
     /// 
     /// Called when a FieldStart node is encountered in the document.
     /// 
     public int visitFieldStart(FieldStart fieldStart) {
         if (fieldStart.getFont().getHidden())
             fieldStart.remove();

         return VisitorAction.CONTINUE;
     }

     /// 
     /// Called when a FieldEnd node is encountered in the document.
     /// 
     public int visitFieldEnd(FieldEnd fieldEnd) {
         if (fieldEnd.getFont().getHidden())
             fieldEnd.remove();

         return VisitorAction.CONTINUE;
     }

     /// 
     /// Called when a FieldSeparator node is encountered in the document.
     /// 
     public int visitFieldSeparator(FieldSeparator fieldSeparator) {
         if (fieldSeparator.getFont().getHidden())
             fieldSeparator.remove();

         return VisitorAction.CONTINUE;
     }

     /// 
     /// Called when a Run node is encountered in the document.
     /// 
     public int visitRun(Run run) {
         if (run.getFont().getHidden())
             run.remove();

         return VisitorAction.CONTINUE;
     }

     /// 
     /// Called when a Paragraph node is encountered in the document.
     /// 
     public int visitParagraphStart(Paragraph paragraph) {
         if (paragraph.getParagraphBreakFont().getHidden())
             paragraph.remove();

         return VisitorAction.CONTINUE;
     }

     /// 
     /// Called when a FormField is encountered in the document.
     /// 
     public int visitFormField(FormField formField) {
         if (formField.getFont().getHidden())
             formField.remove();

         return VisitorAction.CONTINUE;
     }

     /// 
     /// Called when a GroupShape is encountered in the document.
     /// 
     public int visitGroupShapeStart(GroupShape groupShape) {
         if (groupShape.getFont().getHidden())
             groupShape.remove();

         return VisitorAction.CONTINUE;
     }

     /// 
     /// Called when a Shape is encountered in the document.
     /// 
     public int visitShapeStart(Shape shape) {
         if (shape.getFont().getHidden())
             shape.remove();

         return VisitorAction.CONTINUE;
     }

     /// 
     /// Called when a Comment is encountered in the document.
     /// 
     public int visitCommentStart(Comment comment) {
         if (comment.getFont().getHidden())
             comment.remove();

         return VisitorAction.CONTINUE;
     }

     /// 
     /// Called when a Footnote is encountered in the document.
     /// 
     public int visitFootnoteStart(Footnote footnote) {
         if (footnote.getFont().getHidden())
             footnote.remove();

         return VisitorAction.CONTINUE;
     }

     /// 
     /// Called when a SpecialCharacter is encountered in the document.
     /// 
     public int visitSpecialChar(SpecialChar specialChar) {
         if (specialChar.getFont().getHidden())
             specialChar.remove();

         return VisitorAction.CONTINUE;
     }

     /// 
     /// Called when visiting of a Table node is ended in the document.
     /// 
     public int visitTableEnd(Table table) {
         // The content inside table cells may have the hidden content flag, but the tables themselves cannot.
         // If this table had nothing but hidden content, this visitor would have removed all of it,
         // and there would be no child nodes left.
         // Thus, we can also treat the table itself as hidden content and remove it.
         // Tables which are empty but do not have hidden content will have cells with empty paragraphs inside,
         // which this visitor will not remove.
         if (!table.hasChildNodes())
             table.remove();

         return VisitorAction.CONTINUE;
     }

     /// 
     /// Called when visiting of a Cell node is ended in the document.
     /// 
     public int visitCellEnd(Cell cell) {
         if (!cell.hasChildNodes() && cell.getParentNode() != null)
             cell.remove();

         return VisitorAction.CONTINUE;
     }

     /// 
     /// Called when visiting of a Row node is ended in the document.
     /// 
     public int visitRowEnd(Row row) {
         if (!row.hasChildNodes() && row.getParentNode() != null)
             row.remove();

         return VisitorAction.CONTINUE;
     }
 }
 
```

**Parameters:**
| Parameter | Typ | Beschreibung |
| --- | --- | --- |
| shape | [Shape](../../com.aspose.words/shape/) | Das Objekt, das besucht wird. |

**Returns:**
int - Ein [VisitorAction](../../com.aspose.words/visitoraction/) Wert, der angibt, wie die Aufzählung fortgesetzt werden soll. Der zurückgegebene Wert ist einer der [VisitorAction](../../com.aspose.words/visitoraction/) Konstanten.
### visitSmartTagEnd(SmartTag smartTag) {#visitSmartTagEnd-com.aspose.words.SmartTag}
```
public int visitSmartTagEnd(SmartTag smartTag)
```


Aufgerufen, wenn die Aufzählung eines Smart-Tags beendet ist.

 **Examples:** 

Zeigt, wie die Knotenstruktur jedes Smart Tags in einem Dokument ausgegeben wird.

```

 public void smartTagToText() throws Exception {
     Document doc = new Document(getMyDir() + "Smart tags.doc");
     SmartTagStructurePrinter visitor = new SmartTagStructurePrinter();

     // When we get a composite node to accept a document visitor, the visitor visits the accepting node,
     // and then traverses all the node's children in a depth-first manner.
     // The visitor can read and modify each visited node.
     doc.accept(visitor);

     System.out.println(visitor.getText());
 }

 /// 
 /// Traverses a node's non-binary tree of child nodes.
 /// Creates a map in the form of a string of all encountered SmartTag nodes and their children.
 /// 
 public static class SmartTagStructurePrinter extends DocumentVisitor {
     public SmartTagStructurePrinter() {
         mBuilder = new StringBuilder();
         mVisitorIsInsideSmartTag = false;
     }

     /// 
     /// Gets the plain text of the document that was accumulated by the visitor.
     /// 
     public String getText() {
         return mBuilder.toString();
     }

     /// 
     /// Called when a Run node is encountered in the document.
     /// 
     public int visitRun(final Run run) {
         if (mVisitorIsInsideSmartTag) {
             indentAndAppendLine("[Run] \"" + run.getText() + "\"");
         }

         return VisitorAction.CONTINUE;
     }

     /// 
     /// Called when a SmartTag node is encountered in the document.
     /// 
     public int visitSmartTagStart(final SmartTag smartTag) {
         indentAndAppendLine("[SmartTag start] Name: " + smartTag.getElement());
         mDocTraversalDepth++;
         mVisitorIsInsideSmartTag = true;

         return VisitorAction.CONTINUE;
     }

     /// 
     /// Called after all the child nodes of a SmartTag node have been visited.
     /// 
     public int visitSmartTagEnd(final SmartTag smartTag) {
         mDocTraversalDepth--;
         indentAndAppendLine("[SmartTag end]");
         mVisitorIsInsideSmartTag = false;

         return VisitorAction.CONTINUE;
     }

     /// 
     /// Append a line to the StringBuilder and indent it depending on how deep the visitor is into the document tree.
     /// 
     /// 
     private void indentAndAppendLine(final String text) {
         for (int i = 0; i < mDocTraversalDepth; i++) {
             mBuilder.append("|  ");
         }

         mBuilder.append(text + "\r\n");
     }

     private boolean mVisitorIsInsideSmartTag;
     private int mDocTraversalDepth;
     private final StringBuilder mBuilder;
 }
 
```

**Parameters:**
| Parameter | Typ | Beschreibung |
| --- | --- | --- |
| smartTag | [SmartTag](../../com.aspose.words/smarttag/) | Das Objekt, das besucht wird. |

**Returns:**
int - Ein [VisitorAction](../../com.aspose.words/visitoraction/) Wert, der angibt, wie die Aufzählung fortgesetzt werden soll. Der zurückgegebene Wert ist einer der [VisitorAction](../../com.aspose.words/visitoraction/) Konstanten.
### visitSmartTagStart(SmartTag smartTag) {#visitSmartTagStart-com.aspose.words.SmartTag}
```
public int visitSmartTagStart(SmartTag smartTag)
```


Aufgerufen, wenn die Aufzählung eines Smart-Tags begonnen hat.

 **Examples:** 

Zeigt, wie die Knotenstruktur jedes Smart Tags in einem Dokument ausgegeben wird.

```

 public void smartTagToText() throws Exception {
     Document doc = new Document(getMyDir() + "Smart tags.doc");
     SmartTagStructurePrinter visitor = new SmartTagStructurePrinter();

     // When we get a composite node to accept a document visitor, the visitor visits the accepting node,
     // and then traverses all the node's children in a depth-first manner.
     // The visitor can read and modify each visited node.
     doc.accept(visitor);

     System.out.println(visitor.getText());
 }

 /// 
 /// Traverses a node's non-binary tree of child nodes.
 /// Creates a map in the form of a string of all encountered SmartTag nodes and their children.
 /// 
 public static class SmartTagStructurePrinter extends DocumentVisitor {
     public SmartTagStructurePrinter() {
         mBuilder = new StringBuilder();
         mVisitorIsInsideSmartTag = false;
     }

     /// 
     /// Gets the plain text of the document that was accumulated by the visitor.
     /// 
     public String getText() {
         return mBuilder.toString();
     }

     /// 
     /// Called when a Run node is encountered in the document.
     /// 
     public int visitRun(final Run run) {
         if (mVisitorIsInsideSmartTag) {
             indentAndAppendLine("[Run] \"" + run.getText() + "\"");
         }

         return VisitorAction.CONTINUE;
     }

     /// 
     /// Called when a SmartTag node is encountered in the document.
     /// 
     public int visitSmartTagStart(final SmartTag smartTag) {
         indentAndAppendLine("[SmartTag start] Name: " + smartTag.getElement());
         mDocTraversalDepth++;
         mVisitorIsInsideSmartTag = true;

         return VisitorAction.CONTINUE;
     }

     /// 
     /// Called after all the child nodes of a SmartTag node have been visited.
     /// 
     public int visitSmartTagEnd(final SmartTag smartTag) {
         mDocTraversalDepth--;
         indentAndAppendLine("[SmartTag end]");
         mVisitorIsInsideSmartTag = false;

         return VisitorAction.CONTINUE;
     }

     /// 
     /// Append a line to the StringBuilder and indent it depending on how deep the visitor is into the document tree.
     /// 
     /// 
     private void indentAndAppendLine(final String text) {
         for (int i = 0; i < mDocTraversalDepth; i++) {
             mBuilder.append("|  ");
         }

         mBuilder.append(text + "\r\n");
     }

     private boolean mVisitorIsInsideSmartTag;
     private int mDocTraversalDepth;
     private final StringBuilder mBuilder;
 }
 
```

**Parameters:**
| Parameter | Typ | Beschreibung |
| --- | --- | --- |
| smartTag | [SmartTag](../../com.aspose.words/smarttag/) | Das Objekt, das besucht wird. |

**Returns:**
int - Ein [VisitorAction](../../com.aspose.words/visitoraction/) Wert, der angibt, wie die Aufzählung fortgesetzt werden soll. Der zurückgegebene Wert ist einer der [VisitorAction](../../com.aspose.words/visitoraction/) Konstanten.
### visitSpecialChar(SpecialChar specialChar) {#visitSpecialChar-com.aspose.words.SpecialChar}
```
public int visitSpecialChar(SpecialChar specialChar)
```


Aufgerufen, wenn ein [SpecialChar](../../com.aspose.words/specialchar/) Knoten im Dokument gefunden wird.

 **Remarks:** 

Diese Methode darf nicht für generische Steuerzeichen (siehe [ControlChar](../../com.aspose.words/controlchar/)) aufgerufen werden, die im Dokument vorkommen können.

 **Examples:** 

Zeigt, wie man eine DocumentVisitor‑Implementierung verwendet, um allen versteckten Inhalt aus einem Dokument zu entfernen.

```

 public void removeHiddenContentFromDocument() throws Exception {
     Document doc = new Document(getMyDir() + "Hidden content.docx");
     RemoveHiddenContentVisitor hiddenContentRemover = new RemoveHiddenContentVisitor();

     // Below are three types of fields which can accept a document visitor,
     // which will allow it to visit the accepting node, and then traverse its child nodes in a depth-first manner.
     // 1 -  Paragraph node:
     Paragraph para = (Paragraph) doc.getChild(NodeType.PARAGRAPH, 4, true);
     para.accept(hiddenContentRemover);

     // 2 -  Table node:
     Table table = doc.getFirstSection().getBody().getTables().get(0);
     table.accept(hiddenContentRemover);

     // 3 -  Document node:
     doc.accept(hiddenContentRemover);

     doc.save(getArtifactsDir() + "Font.RemoveHiddenContentFromDocument.docx");
 }

 /// 
 /// Removes all visited nodes marked as "hidden content".
 /// 
 public static class RemoveHiddenContentVisitor extends DocumentVisitor {
     /// 
     /// Called when a FieldStart node is encountered in the document.
     /// 
     public int visitFieldStart(FieldStart fieldStart) {
         if (fieldStart.getFont().getHidden())
             fieldStart.remove();

         return VisitorAction.CONTINUE;
     }

     /// 
     /// Called when a FieldEnd node is encountered in the document.
     /// 
     public int visitFieldEnd(FieldEnd fieldEnd) {
         if (fieldEnd.getFont().getHidden())
             fieldEnd.remove();

         return VisitorAction.CONTINUE;
     }

     /// 
     /// Called when a FieldSeparator node is encountered in the document.
     /// 
     public int visitFieldSeparator(FieldSeparator fieldSeparator) {
         if (fieldSeparator.getFont().getHidden())
             fieldSeparator.remove();

         return VisitorAction.CONTINUE;
     }

     /// 
     /// Called when a Run node is encountered in the document.
     /// 
     public int visitRun(Run run) {
         if (run.getFont().getHidden())
             run.remove();

         return VisitorAction.CONTINUE;
     }

     /// 
     /// Called when a Paragraph node is encountered in the document.
     /// 
     public int visitParagraphStart(Paragraph paragraph) {
         if (paragraph.getParagraphBreakFont().getHidden())
             paragraph.remove();

         return VisitorAction.CONTINUE;
     }

     /// 
     /// Called when a FormField is encountered in the document.
     /// 
     public int visitFormField(FormField formField) {
         if (formField.getFont().getHidden())
             formField.remove();

         return VisitorAction.CONTINUE;
     }

     /// 
     /// Called when a GroupShape is encountered in the document.
     /// 
     public int visitGroupShapeStart(GroupShape groupShape) {
         if (groupShape.getFont().getHidden())
             groupShape.remove();

         return VisitorAction.CONTINUE;
     }

     /// 
     /// Called when a Shape is encountered in the document.
     /// 
     public int visitShapeStart(Shape shape) {
         if (shape.getFont().getHidden())
             shape.remove();

         return VisitorAction.CONTINUE;
     }

     /// 
     /// Called when a Comment is encountered in the document.
     /// 
     public int visitCommentStart(Comment comment) {
         if (comment.getFont().getHidden())
             comment.remove();

         return VisitorAction.CONTINUE;
     }

     /// 
     /// Called when a Footnote is encountered in the document.
     /// 
     public int visitFootnoteStart(Footnote footnote) {
         if (footnote.getFont().getHidden())
             footnote.remove();

         return VisitorAction.CONTINUE;
     }

     /// 
     /// Called when a SpecialCharacter is encountered in the document.
     /// 
     public int visitSpecialChar(SpecialChar specialChar) {
         if (specialChar.getFont().getHidden())
             specialChar.remove();

         return VisitorAction.CONTINUE;
     }

     /// 
     /// Called when visiting of a Table node is ended in the document.
     /// 
     public int visitTableEnd(Table table) {
         // The content inside table cells may have the hidden content flag, but the tables themselves cannot.
         // If this table had nothing but hidden content, this visitor would have removed all of it,
         // and there would be no child nodes left.
         // Thus, we can also treat the table itself as hidden content and remove it.
         // Tables which are empty but do not have hidden content will have cells with empty paragraphs inside,
         // which this visitor will not remove.
         if (!table.hasChildNodes())
             table.remove();

         return VisitorAction.CONTINUE;
     }

     /// 
     /// Called when visiting of a Cell node is ended in the document.
     /// 
     public int visitCellEnd(Cell cell) {
         if (!cell.hasChildNodes() && cell.getParentNode() != null)
             cell.remove();

         return VisitorAction.CONTINUE;
     }

     /// 
     /// Called when visiting of a Row node is ended in the document.
     /// 
     public int visitRowEnd(Row row) {
         if (!row.hasChildNodes() && row.getParentNode() != null)
             row.remove();

         return VisitorAction.CONTINUE;
     }
 }
 
```

**Parameters:**
| Parameter | Typ | Beschreibung |
| --- | --- | --- |
| specialChar | [SpecialChar](../../com.aspose.words/specialchar/) | Das Objekt, das besucht wird. |

**Returns:**
int - Ein [VisitorAction](../../com.aspose.words/visitoraction/) Wert, der angibt, wie die Aufzählung fortgesetzt werden soll. Der zurückgegebene Wert ist einer der [VisitorAction](../../com.aspose.words/visitoraction/) Konstanten.
### visitStructuredDocumentTagEnd(StructuredDocumentTag sdt) {#visitStructuredDocumentTagEnd-com.aspose.words.StructuredDocumentTag}
```
public int visitStructuredDocumentTagEnd(StructuredDocumentTag sdt)
```


Aufgerufen, wenn die Aufzählung eines strukturierten Dokument-Tags beendet ist.

 **Examples:** 

Zeigt, wie die Knotenstruktur jedes strukturierten Dokument-Tags in einem Dokument ausgegeben wird.

```

 public void structuredDocumentTagToText() throws Exception {
     Document doc = new Document(getMyDir() + "DocumentVisitor-compatible features.docx");
     StructuredDocumentTagNodePrinter visitor = new StructuredDocumentTagNodePrinter();

     // When we get a composite node to accept a document visitor, the visitor visits the accepting node,
     // and then traverses all the node's children in a depth-first manner.
     // The visitor can read and modify each visited node.
     doc.accept(visitor);

     System.out.println(visitor.getText());
 }

 /// 
 /// Traverses a node's non-binary tree of child nodes.
 /// Creates a map in the form of a string of all encountered StructuredDocumentTag nodes and their children.
 /// 
 public static class StructuredDocumentTagNodePrinter extends DocumentVisitor {
     public StructuredDocumentTagNodePrinter() {
         mBuilder = new StringBuilder();
         mVisitorIsInsideStructuredDocumentTag = false;
     }

     /// 
     /// Gets the plain text of the document that was accumulated by the visitor.
     /// 
     public String getText() {
         return mBuilder.toString();
     }

     /// 
     /// Called when a Run node is encountered in the document.
     /// 
     public int visitRun(final Run run) {
         if (mVisitorIsInsideStructuredDocumentTag) {
             indentAndAppendLine("[Run] \"" + run.getText() + "\"");
         }

         return VisitorAction.CONTINUE;
     }

     /// 
     /// Called when a StructuredDocumentTag node is encountered in the document.
     /// 
     public int visitStructuredDocumentTagStart(final StructuredDocumentTag sdt) {
         indentAndAppendLine("[StructuredDocumentTag start] Title: " + sdt.getTitle());
         mDocTraversalDepth++;

         return VisitorAction.CONTINUE;
     }

     /// 
     /// Called after all the child nodes of a StructuredDocumentTag node have been visited.
     /// 
     public int visitStructuredDocumentTagEnd(final StructuredDocumentTag sdt) {
         mDocTraversalDepth--;
         indentAndAppendLine("[StructuredDocumentTag end]");

         return VisitorAction.CONTINUE;
     }

     /// 
     /// Append a line to the StringBuilder and indent it depending on how deep the visitor is into the document tree.
     /// 
     /// 
     private void indentAndAppendLine(final String text) {
         for (int i = 0; i < mDocTraversalDepth; i++) {
             mBuilder.append("|  ");
         }

         mBuilder.append(text + "\r\n");
     }

     private final boolean mVisitorIsInsideStructuredDocumentTag;
     private int mDocTraversalDepth;
     private final StringBuilder mBuilder;
 }
 
```

**Parameters:**
| Parameter | Typ | Beschreibung |
| --- | --- | --- |
| sdt | [StructuredDocumentTag](../../com.aspose.words/structureddocumenttag/) | Das Objekt, das besucht wird. |

**Returns:**
int - Ein [VisitorAction](../../com.aspose.words/visitoraction/) Wert, der angibt, wie die Aufzählung fortgesetzt werden soll. Der zurückgegebene Wert ist einer der [VisitorAction](../../com.aspose.words/visitoraction/) Konstanten.
### visitStructuredDocumentTagRangeEnd(StructuredDocumentTagRangeEnd sdtRangeEnd) {#visitStructuredDocumentTagRangeEnd-com.aspose.words.StructuredDocumentTagRangeEnd}
```
public int visitStructuredDocumentTagRangeEnd(StructuredDocumentTagRangeEnd sdtRangeEnd)
```


Aufgerufen, wenn ein StructuredDocumentTagRangeEnd gefunden wird.

 **Examples:** 

Zeigt, wie ein DocumentVisitor verwendet wird, um die Knotenstruktur eines Dokuments auszugeben.

```

 public void docStructureToText() throws Exception {
     Document doc = new Document(getMyDir() + "DocumentVisitor-compatible features.docx");
     DocStructurePrinter visitor = new DocStructurePrinter();

     // When we get a composite node to accept a document visitor, the visitor visits the accepting node,
     // and then traverses all the node's children in a depth-first manner.
     // The visitor can read and modify each visited node.
     doc.accept(visitor);

     System.out.println(visitor.getText());
 }

 /// 
 /// Traverses a node's tree of child nodes.
 /// Creates a map of this tree in the form of a string.
 /// 
 public static class DocStructurePrinter extends DocumentVisitor {
     public DocStructurePrinter() {
         mAcceptingNodeChildTree = new StringBuilder();
     }

     public String getText() {
         return mAcceptingNodeChildTree.toString();
     }

     /// 
     /// Called when a Document node is encountered.
     /// 
     public int visitDocumentStart(Document doc) {
         int childNodeCount = doc.getChildNodes(NodeType.ANY, true).getCount();

         indentAndAppendLine("[Document start] Child nodes: " + childNodeCount);
         mDocTraversalDepth++;

         // Allow the visitor to continue visiting other nodes.
         return VisitorAction.CONTINUE;
     }

     /// 
     /// Called after all the child nodes of a Document node have been visited.
     /// 
     public int visitDocumentEnd(Document doc) {
         mDocTraversalDepth--;
         indentAndAppendLine("[Document end]");

         return VisitorAction.CONTINUE;
     }

     /// 
     /// Called when a Section node is encountered in the document.
     /// 
     public int visitSectionStart(final Section section) {
         // Get the index of our section within the document
         NodeCollection docSections = section.getDocument().getChildNodes(NodeType.SECTION, false);
         int sectionIndex = docSections.indexOf(section);

         indentAndAppendLine("[Section start] Section index: " + sectionIndex);
         mDocTraversalDepth++;

         return VisitorAction.CONTINUE;
     }

     /// 
     /// Called after all the child nodes of a Section node have been visited.
     /// 
     public int visitSectionEnd(final Section section) {
         mDocTraversalDepth--;
         indentAndAppendLine("[Section end]");

         return VisitorAction.CONTINUE;
     }

     /// 
     /// Called when a Body node is encountered in the document.
     /// 
     public int visitBodyStart(final Body body) {
         int paragraphCount = body.getParagraphs().getCount();
         indentAndAppendLine("[Body start] Paragraphs: " + paragraphCount);
         mDocTraversalDepth++;

         return VisitorAction.CONTINUE;
     }

     /// 
     /// Called after all the child nodes of a Body node have been visited.
     /// 
     public int visitBodyEnd(final Body body) {
         mDocTraversalDepth--;
         indentAndAppendLine("[Body end]");

         return VisitorAction.CONTINUE;
     }

     /// 
     /// Called when a Paragraph node is encountered in the document.
     /// 
     public int visitParagraphStart(final Paragraph paragraph) {
         indentAndAppendLine("[Paragraph start]");
         mDocTraversalDepth++;

         return VisitorAction.CONTINUE;
     }

     /// 
     /// Called after all the child nodes of a Paragraph node have been visited.
     /// 
     public int visitParagraphEnd(final Paragraph paragraph) {
         mDocTraversalDepth--;
         indentAndAppendLine("[Paragraph end]");

         return VisitorAction.CONTINUE;
     }

     /// 
     /// Called when a Run node is encountered in the document.
     /// 
     public int visitRun(final Run run) {
         indentAndAppendLine("[Run] \"" + run.getText() + "\"");

         return VisitorAction.CONTINUE;
     }

     /// 
     /// Called when a SubDocument node is encountered in the document.
     /// 
     public int visitSubDocument(final SubDocument subDocument) {
         indentAndAppendLine("[SubDocument]");

         return VisitorAction.CONTINUE;
     }

     /// 
     /// Called when a SubDocument node is encountered in the document.
     /// 
     public int visitStructuredDocumentTagRangeStart(StructuredDocumentTagRangeStart sdtRangeStart)
     {
         indentAndAppendLine("[SdtRangeStart]");

         return VisitorAction.CONTINUE;
     }

     /// 
     /// Called when a SubDocument node is encountered in the document.
     /// 
     public int visitStructuredDocumentTagRangeEnd(StructuredDocumentTagRangeEnd sdtRangeEnd)
     {
         indentAndAppendLine("[SdtRangeEnd]");

         return VisitorAction.CONTINUE;
     }

     /// 
     /// Append a line to the StringBuilder and indent it depending on how deep the visitor is into the document tree.
     /// 
     /// 
     private void indentAndAppendLine(final String text) {
         for (int i = 0; i < mDocTraversalDepth; i++) {
             mAcceptingNodeChildTree.append("|  ");
         }

         mAcceptingNodeChildTree.append(text + "\r\n");
     }

     private int mDocTraversalDepth;
     private final StringBuilder mAcceptingNodeChildTree;
 }
 
```

**Parameters:**
| Parameter | Typ | Beschreibung |
| --- | --- | --- |
| sdtRangeEnd | [StructuredDocumentTagRangeEnd](../../com.aspose.words/structureddocumenttagrangeend/) |  |

**Returns:**
int
### visitStructuredDocumentTagRangeStart(StructuredDocumentTagRangeStart sdtRangeStart) {#visitStructuredDocumentTagRangeStart-com.aspose.words.StructuredDocumentTagRangeStart}
```
public int visitStructuredDocumentTagRangeStart(StructuredDocumentTagRangeStart sdtRangeStart)
```


Aufgerufen, wenn ein StructuredDocumentTagRangeStart gefunden wird.

 **Examples:** 

Zeigt, wie ein DocumentVisitor verwendet wird, um die Knotenstruktur eines Dokuments auszugeben.

```

 public void docStructureToText() throws Exception {
     Document doc = new Document(getMyDir() + "DocumentVisitor-compatible features.docx");
     DocStructurePrinter visitor = new DocStructurePrinter();

     // When we get a composite node to accept a document visitor, the visitor visits the accepting node,
     // and then traverses all the node's children in a depth-first manner.
     // The visitor can read and modify each visited node.
     doc.accept(visitor);

     System.out.println(visitor.getText());
 }

 /// 
 /// Traverses a node's tree of child nodes.
 /// Creates a map of this tree in the form of a string.
 /// 
 public static class DocStructurePrinter extends DocumentVisitor {
     public DocStructurePrinter() {
         mAcceptingNodeChildTree = new StringBuilder();
     }

     public String getText() {
         return mAcceptingNodeChildTree.toString();
     }

     /// 
     /// Called when a Document node is encountered.
     /// 
     public int visitDocumentStart(Document doc) {
         int childNodeCount = doc.getChildNodes(NodeType.ANY, true).getCount();

         indentAndAppendLine("[Document start] Child nodes: " + childNodeCount);
         mDocTraversalDepth++;

         // Allow the visitor to continue visiting other nodes.
         return VisitorAction.CONTINUE;
     }

     /// 
     /// Called after all the child nodes of a Document node have been visited.
     /// 
     public int visitDocumentEnd(Document doc) {
         mDocTraversalDepth--;
         indentAndAppendLine("[Document end]");

         return VisitorAction.CONTINUE;
     }

     /// 
     /// Called when a Section node is encountered in the document.
     /// 
     public int visitSectionStart(final Section section) {
         // Get the index of our section within the document
         NodeCollection docSections = section.getDocument().getChildNodes(NodeType.SECTION, false);
         int sectionIndex = docSections.indexOf(section);

         indentAndAppendLine("[Section start] Section index: " + sectionIndex);
         mDocTraversalDepth++;

         return VisitorAction.CONTINUE;
     }

     /// 
     /// Called after all the child nodes of a Section node have been visited.
     /// 
     public int visitSectionEnd(final Section section) {
         mDocTraversalDepth--;
         indentAndAppendLine("[Section end]");

         return VisitorAction.CONTINUE;
     }

     /// 
     /// Called when a Body node is encountered in the document.
     /// 
     public int visitBodyStart(final Body body) {
         int paragraphCount = body.getParagraphs().getCount();
         indentAndAppendLine("[Body start] Paragraphs: " + paragraphCount);
         mDocTraversalDepth++;

         return VisitorAction.CONTINUE;
     }

     /// 
     /// Called after all the child nodes of a Body node have been visited.
     /// 
     public int visitBodyEnd(final Body body) {
         mDocTraversalDepth--;
         indentAndAppendLine("[Body end]");

         return VisitorAction.CONTINUE;
     }

     /// 
     /// Called when a Paragraph node is encountered in the document.
     /// 
     public int visitParagraphStart(final Paragraph paragraph) {
         indentAndAppendLine("[Paragraph start]");
         mDocTraversalDepth++;

         return VisitorAction.CONTINUE;
     }

     /// 
     /// Called after all the child nodes of a Paragraph node have been visited.
     /// 
     public int visitParagraphEnd(final Paragraph paragraph) {
         mDocTraversalDepth--;
         indentAndAppendLine("[Paragraph end]");

         return VisitorAction.CONTINUE;
     }

     /// 
     /// Called when a Run node is encountered in the document.
     /// 
     public int visitRun(final Run run) {
         indentAndAppendLine("[Run] \"" + run.getText() + "\"");

         return VisitorAction.CONTINUE;
     }

     /// 
     /// Called when a SubDocument node is encountered in the document.
     /// 
     public int visitSubDocument(final SubDocument subDocument) {
         indentAndAppendLine("[SubDocument]");

         return VisitorAction.CONTINUE;
     }

     /// 
     /// Called when a SubDocument node is encountered in the document.
     /// 
     public int visitStructuredDocumentTagRangeStart(StructuredDocumentTagRangeStart sdtRangeStart)
     {
         indentAndAppendLine("[SdtRangeStart]");

         return VisitorAction.CONTINUE;
     }

     /// 
     /// Called when a SubDocument node is encountered in the document.
     /// 
     public int visitStructuredDocumentTagRangeEnd(StructuredDocumentTagRangeEnd sdtRangeEnd)
     {
         indentAndAppendLine("[SdtRangeEnd]");

         return VisitorAction.CONTINUE;
     }

     /// 
     /// Append a line to the StringBuilder and indent it depending on how deep the visitor is into the document tree.
     /// 
     /// 
     private void indentAndAppendLine(final String text) {
         for (int i = 0; i < mDocTraversalDepth; i++) {
             mAcceptingNodeChildTree.append("|  ");
         }

         mAcceptingNodeChildTree.append(text + "\r\n");
     }

     private int mDocTraversalDepth;
     private final StringBuilder mAcceptingNodeChildTree;
 }
 
```

**Parameters:**
| Parameter | Typ | Beschreibung |
| --- | --- | --- |
| sdtRangeStart | [StructuredDocumentTagRangeStart](../../com.aspose.words/structureddocumenttagrangestart/) |  |

**Returns:**
int
### visitStructuredDocumentTagStart(StructuredDocumentTag sdt) {#visitStructuredDocumentTagStart-com.aspose.words.StructuredDocumentTag}
```
public int visitStructuredDocumentTagStart(StructuredDocumentTag sdt)
```


Aufgerufen, wenn die Aufzählung eines strukturierten Dokument-Tags begonnen hat.

 **Examples:** 

Zeigt, wie die Knotenstruktur jedes strukturierten Dokument-Tags in einem Dokument ausgegeben wird.

```

 public void structuredDocumentTagToText() throws Exception {
     Document doc = new Document(getMyDir() + "DocumentVisitor-compatible features.docx");
     StructuredDocumentTagNodePrinter visitor = new StructuredDocumentTagNodePrinter();

     // When we get a composite node to accept a document visitor, the visitor visits the accepting node,
     // and then traverses all the node's children in a depth-first manner.
     // The visitor can read and modify each visited node.
     doc.accept(visitor);

     System.out.println(visitor.getText());
 }

 /// 
 /// Traverses a node's non-binary tree of child nodes.
 /// Creates a map in the form of a string of all encountered StructuredDocumentTag nodes and their children.
 /// 
 public static class StructuredDocumentTagNodePrinter extends DocumentVisitor {
     public StructuredDocumentTagNodePrinter() {
         mBuilder = new StringBuilder();
         mVisitorIsInsideStructuredDocumentTag = false;
     }

     /// 
     /// Gets the plain text of the document that was accumulated by the visitor.
     /// 
     public String getText() {
         return mBuilder.toString();
     }

     /// 
     /// Called when a Run node is encountered in the document.
     /// 
     public int visitRun(final Run run) {
         if (mVisitorIsInsideStructuredDocumentTag) {
             indentAndAppendLine("[Run] \"" + run.getText() + "\"");
         }

         return VisitorAction.CONTINUE;
     }

     /// 
     /// Called when a StructuredDocumentTag node is encountered in the document.
     /// 
     public int visitStructuredDocumentTagStart(final StructuredDocumentTag sdt) {
         indentAndAppendLine("[StructuredDocumentTag start] Title: " + sdt.getTitle());
         mDocTraversalDepth++;

         return VisitorAction.CONTINUE;
     }

     /// 
     /// Called after all the child nodes of a StructuredDocumentTag node have been visited.
     /// 
     public int visitStructuredDocumentTagEnd(final StructuredDocumentTag sdt) {
         mDocTraversalDepth--;
         indentAndAppendLine("[StructuredDocumentTag end]");

         return VisitorAction.CONTINUE;
     }

     /// 
     /// Append a line to the StringBuilder and indent it depending on how deep the visitor is into the document tree.
     /// 
     /// 
     private void indentAndAppendLine(final String text) {
         for (int i = 0; i < mDocTraversalDepth; i++) {
             mBuilder.append("|  ");
         }

         mBuilder.append(text + "\r\n");
     }

     private final boolean mVisitorIsInsideStructuredDocumentTag;
     private int mDocTraversalDepth;
     private final StringBuilder mBuilder;
 }
 
```

**Parameters:**
| Parameter | Typ | Beschreibung |
| --- | --- | --- |
| sdt | [StructuredDocumentTag](../../com.aspose.words/structureddocumenttag/) | Das Objekt, das besucht wird. |

**Returns:**
int - Ein [VisitorAction](../../com.aspose.words/visitoraction/) Wert, der angibt, wie die Aufzählung fortgesetzt werden soll. Der zurückgegebene Wert ist einer der [VisitorAction](../../com.aspose.words/visitoraction/) Konstanten.
### visitSubDocument(SubDocument subDocument) {#visitSubDocument-com.aspose.words.SubDocument}
```
public int visitSubDocument(SubDocument subDocument)
```


Aufgerufen, wenn ein Unterdokument gefunden wird.

 **Examples:** 

Zeigt, wie ein DocumentVisitor verwendet wird, um die Knotenstruktur eines Dokuments auszugeben.

```

 public void docStructureToText() throws Exception {
     Document doc = new Document(getMyDir() + "DocumentVisitor-compatible features.docx");
     DocStructurePrinter visitor = new DocStructurePrinter();

     // When we get a composite node to accept a document visitor, the visitor visits the accepting node,
     // and then traverses all the node's children in a depth-first manner.
     // The visitor can read and modify each visited node.
     doc.accept(visitor);

     System.out.println(visitor.getText());
 }

 /// 
 /// Traverses a node's tree of child nodes.
 /// Creates a map of this tree in the form of a string.
 /// 
 public static class DocStructurePrinter extends DocumentVisitor {
     public DocStructurePrinter() {
         mAcceptingNodeChildTree = new StringBuilder();
     }

     public String getText() {
         return mAcceptingNodeChildTree.toString();
     }

     /// 
     /// Called when a Document node is encountered.
     /// 
     public int visitDocumentStart(Document doc) {
         int childNodeCount = doc.getChildNodes(NodeType.ANY, true).getCount();

         indentAndAppendLine("[Document start] Child nodes: " + childNodeCount);
         mDocTraversalDepth++;

         // Allow the visitor to continue visiting other nodes.
         return VisitorAction.CONTINUE;
     }

     /// 
     /// Called after all the child nodes of a Document node have been visited.
     /// 
     public int visitDocumentEnd(Document doc) {
         mDocTraversalDepth--;
         indentAndAppendLine("[Document end]");

         return VisitorAction.CONTINUE;
     }

     /// 
     /// Called when a Section node is encountered in the document.
     /// 
     public int visitSectionStart(final Section section) {
         // Get the index of our section within the document
         NodeCollection docSections = section.getDocument().getChildNodes(NodeType.SECTION, false);
         int sectionIndex = docSections.indexOf(section);

         indentAndAppendLine("[Section start] Section index: " + sectionIndex);
         mDocTraversalDepth++;

         return VisitorAction.CONTINUE;
     }

     /// 
     /// Called after all the child nodes of a Section node have been visited.
     /// 
     public int visitSectionEnd(final Section section) {
         mDocTraversalDepth--;
         indentAndAppendLine("[Section end]");

         return VisitorAction.CONTINUE;
     }

     /// 
     /// Called when a Body node is encountered in the document.
     /// 
     public int visitBodyStart(final Body body) {
         int paragraphCount = body.getParagraphs().getCount();
         indentAndAppendLine("[Body start] Paragraphs: " + paragraphCount);
         mDocTraversalDepth++;

         return VisitorAction.CONTINUE;
     }

     /// 
     /// Called after all the child nodes of a Body node have been visited.
     /// 
     public int visitBodyEnd(final Body body) {
         mDocTraversalDepth--;
         indentAndAppendLine("[Body end]");

         return VisitorAction.CONTINUE;
     }

     /// 
     /// Called when a Paragraph node is encountered in the document.
     /// 
     public int visitParagraphStart(final Paragraph paragraph) {
         indentAndAppendLine("[Paragraph start]");
         mDocTraversalDepth++;

         return VisitorAction.CONTINUE;
     }

     /// 
     /// Called after all the child nodes of a Paragraph node have been visited.
     /// 
     public int visitParagraphEnd(final Paragraph paragraph) {
         mDocTraversalDepth--;
         indentAndAppendLine("[Paragraph end]");

         return VisitorAction.CONTINUE;
     }

     /// 
     /// Called when a Run node is encountered in the document.
     /// 
     public int visitRun(final Run run) {
         indentAndAppendLine("[Run] \"" + run.getText() + "\"");

         return VisitorAction.CONTINUE;
     }

     /// 
     /// Called when a SubDocument node is encountered in the document.
     /// 
     public int visitSubDocument(final SubDocument subDocument) {
         indentAndAppendLine("[SubDocument]");

         return VisitorAction.CONTINUE;
     }

     /// 
     /// Called when a SubDocument node is encountered in the document.
     /// 
     public int visitStructuredDocumentTagRangeStart(StructuredDocumentTagRangeStart sdtRangeStart)
     {
         indentAndAppendLine("[SdtRangeStart]");

         return VisitorAction.CONTINUE;
     }

     /// 
     /// Called when a SubDocument node is encountered in the document.
     /// 
     public int visitStructuredDocumentTagRangeEnd(StructuredDocumentTagRangeEnd sdtRangeEnd)
     {
         indentAndAppendLine("[SdtRangeEnd]");

         return VisitorAction.CONTINUE;
     }

     /// 
     /// Append a line to the StringBuilder and indent it depending on how deep the visitor is into the document tree.
     /// 
     /// 
     private void indentAndAppendLine(final String text) {
         for (int i = 0; i < mDocTraversalDepth; i++) {
             mAcceptingNodeChildTree.append("|  ");
         }

         mAcceptingNodeChildTree.append(text + "\r\n");
     }

     private int mDocTraversalDepth;
     private final StringBuilder mAcceptingNodeChildTree;
 }
 
```

**Parameters:**
| Parameter | Typ | Beschreibung |
| --- | --- | --- |
| subDocument | [SubDocument](../../com.aspose.words/subdocument/) | Das Objekt, das besucht wird. |

**Returns:**
int - Ein [VisitorAction](../../com.aspose.words/visitoraction/) Wert, der angibt, wie die Aufzählung fortgesetzt werden soll. Der zurückgegebene Wert ist einer der [VisitorAction](../../com.aspose.words/visitoraction/) Konstanten.
### visitTableEnd(Table table) {#visitTableEnd-com.aspose.words.Table}
```
public int visitTableEnd(Table table)
```


Aufgerufen, wenn die Aufzählung einer Tabelle beendet ist.

 **Examples:** 

Zeigt, wie man die Knotenstruktur jeder Tabelle in einem Dokument ausgibt.

```

 public void tableToText() throws Exception {
     Document doc = new Document(getMyDir() + "DocumentVisitor-compatible features.docx");
     TableStructurePrinter visitor = new TableStructurePrinter();

     // When we get a composite node to accept a document visitor, the visitor visits the accepting node,
     // and then traverses all the node's children in a depth-first manner.
     // The visitor can read and modify each visited node.
     doc.accept(visitor);

     System.out.println(visitor.getText());
 }

 /// 
 /// Traverses a node's non-binary tree of child nodes.
 /// Creates a map in the form of a string of all encountered Table nodes and their children.
 /// 
 public static class TableStructurePrinter extends DocumentVisitor {
     public TableStructurePrinter() {
         mVisitedTables = new StringBuilder();
         mVisitorIsInsideTable = false;
     }

     public String getText() {
         return mVisitedTables.toString();
     }

     /// 
     /// Called when a Run node is encountered in the document.
     /// Runs that are not within tables are not recorded.
     /// 
     public int visitRun(Run run) {
         if (mVisitorIsInsideTable) indentAndAppendLine("[Run] \"" + run.getText() + "\"");

         return VisitorAction.CONTINUE;
     }

     /// 
     /// Called when a Table is encountered in the document.
     /// 
     public int visitTableStart(final Table table) {
         int rows = 0;
         int columns = 0;

         if (table.getRows().getCount() > 0) {
             rows = table.getRows().getCount();
             columns = table.getFirstRow().getCount();
         }

         indentAndAppendLine("[Table start] Size: " + rows + "x" + columns);
         mDocTraversalDepth++;
         mVisitorIsInsideTable = true;

         return VisitorAction.CONTINUE;
     }

     /// 
     /// Called after all the child nodes of a Table node have been visited.
     /// 
     public int visitTableEnd(final Table table) {
         mDocTraversalDepth--;
         indentAndAppendLine("[Table end]");
         mVisitorIsInsideTable = false;

         return VisitorAction.CONTINUE;
     }

     /// 
     /// Called when a Row node is encountered in the document.
     /// 
     public int visitRowStart(final Row row) {
         String rowContents = row.getText().replaceAll("\\u0007", ", ").replaceAll(", , ", "");
         int rowWidth = row.indexOf(row.getLastCell()) + 1;
         int rowIndex = row.getParentTable().indexOf(row);
         String rowStatusInTable = row.isFirstRow() && row.isLastRow() ? "only" : row.isFirstRow() ? "first" : row.isLastRow() ? "last" : "";
         if (!"".equals(rowStatusInTable)) {
             rowStatusInTable = MessageFormat.format(", the {0} row in this table,", rowStatusInTable);
         }

         indentAndAppendLine(MessageFormat.format("[Row start] Row #{0}{1} width {2}, \"{3}\"", ++rowIndex, rowStatusInTable, rowWidth, rowContents));
         mDocTraversalDepth++;

         return VisitorAction.CONTINUE;
     }

     /// 
     /// Called after all the child nodes of a Row node have been visited.
     /// 
     public int visitRowEnd(final Row row) {
         mDocTraversalDepth--;
         indentAndAppendLine("[Row end]");

         return VisitorAction.CONTINUE;
     }

     /// 
     /// Called when a Cell node is encountered in the document.
     /// 
     public int visitCellStart(final Cell cell) {
         Row row = cell.getParentRow();
         Table table = row.getParentTable();
         String cellStatusInRow = cell.isFirstCell() && cell.isLastCell() ? "only" : cell.isFirstCell() ? "first" : cell.isLastCell() ? "last" : "";
         if (!"".equals(cellStatusInRow)) {
             cellStatusInRow = MessageFormat.format(", the {0} cell in this row", cellStatusInRow);
         }

         indentAndAppendLine(MessageFormat.format("[Cell start] Row {0}, Col {1}{2}", table.indexOf(row) + 1, row.indexOf(cell) + 1, cellStatusInRow));
         mDocTraversalDepth++;

         return VisitorAction.CONTINUE;
     }

     /// 
     /// Called after all the child nodes of a Cell node have been visited.
     /// 
     public int visitCellEnd(final Cell cell) {
         mDocTraversalDepth--;
         indentAndAppendLine("[Cell end]");
         return VisitorAction.CONTINUE;
     }

     /// 
     /// Append a line to the StringBuilder, and indent it depending on how deep the visitor is
     /// into the current table's tree of child nodes.
     /// 
     /// 
     private void indentAndAppendLine(final String text) {
         for (int i = 0; i < mDocTraversalDepth; i++) {
             mVisitedTables.append("|  ");
         }

         mVisitedTables.append(text + "\r\n");
     }

     private boolean mVisitorIsInsideTable;
     private int mDocTraversalDepth;
     private final  StringBuilder mVisitedTables;
 }
 
```

Zeigt, wie man eine DocumentVisitor‑Implementierung verwendet, um allen versteckten Inhalt aus einem Dokument zu entfernen.

```

 public void removeHiddenContentFromDocument() throws Exception {
     Document doc = new Document(getMyDir() + "Hidden content.docx");
     RemoveHiddenContentVisitor hiddenContentRemover = new RemoveHiddenContentVisitor();

     // Below are three types of fields which can accept a document visitor,
     // which will allow it to visit the accepting node, and then traverse its child nodes in a depth-first manner.
     // 1 -  Paragraph node:
     Paragraph para = (Paragraph) doc.getChild(NodeType.PARAGRAPH, 4, true);
     para.accept(hiddenContentRemover);

     // 2 -  Table node:
     Table table = doc.getFirstSection().getBody().getTables().get(0);
     table.accept(hiddenContentRemover);

     // 3 -  Document node:
     doc.accept(hiddenContentRemover);

     doc.save(getArtifactsDir() + "Font.RemoveHiddenContentFromDocument.docx");
 }

 /// 
 /// Removes all visited nodes marked as "hidden content".
 /// 
 public static class RemoveHiddenContentVisitor extends DocumentVisitor {
     /// 
     /// Called when a FieldStart node is encountered in the document.
     /// 
     public int visitFieldStart(FieldStart fieldStart) {
         if (fieldStart.getFont().getHidden())
             fieldStart.remove();

         return VisitorAction.CONTINUE;
     }

     /// 
     /// Called when a FieldEnd node is encountered in the document.
     /// 
     public int visitFieldEnd(FieldEnd fieldEnd) {
         if (fieldEnd.getFont().getHidden())
             fieldEnd.remove();

         return VisitorAction.CONTINUE;
     }

     /// 
     /// Called when a FieldSeparator node is encountered in the document.
     /// 
     public int visitFieldSeparator(FieldSeparator fieldSeparator) {
         if (fieldSeparator.getFont().getHidden())
             fieldSeparator.remove();

         return VisitorAction.CONTINUE;
     }

     /// 
     /// Called when a Run node is encountered in the document.
     /// 
     public int visitRun(Run run) {
         if (run.getFont().getHidden())
             run.remove();

         return VisitorAction.CONTINUE;
     }

     /// 
     /// Called when a Paragraph node is encountered in the document.
     /// 
     public int visitParagraphStart(Paragraph paragraph) {
         if (paragraph.getParagraphBreakFont().getHidden())
             paragraph.remove();

         return VisitorAction.CONTINUE;
     }

     /// 
     /// Called when a FormField is encountered in the document.
     /// 
     public int visitFormField(FormField formField) {
         if (formField.getFont().getHidden())
             formField.remove();

         return VisitorAction.CONTINUE;
     }

     /// 
     /// Called when a GroupShape is encountered in the document.
     /// 
     public int visitGroupShapeStart(GroupShape groupShape) {
         if (groupShape.getFont().getHidden())
             groupShape.remove();

         return VisitorAction.CONTINUE;
     }

     /// 
     /// Called when a Shape is encountered in the document.
     /// 
     public int visitShapeStart(Shape shape) {
         if (shape.getFont().getHidden())
             shape.remove();

         return VisitorAction.CONTINUE;
     }

     /// 
     /// Called when a Comment is encountered in the document.
     /// 
     public int visitCommentStart(Comment comment) {
         if (comment.getFont().getHidden())
             comment.remove();

         return VisitorAction.CONTINUE;
     }

     /// 
     /// Called when a Footnote is encountered in the document.
     /// 
     public int visitFootnoteStart(Footnote footnote) {
         if (footnote.getFont().getHidden())
             footnote.remove();

         return VisitorAction.CONTINUE;
     }

     /// 
     /// Called when a SpecialCharacter is encountered in the document.
     /// 
     public int visitSpecialChar(SpecialChar specialChar) {
         if (specialChar.getFont().getHidden())
             specialChar.remove();

         return VisitorAction.CONTINUE;
     }

     /// 
     /// Called when visiting of a Table node is ended in the document.
     /// 
     public int visitTableEnd(Table table) {
         // The content inside table cells may have the hidden content flag, but the tables themselves cannot.
         // If this table had nothing but hidden content, this visitor would have removed all of it,
         // and there would be no child nodes left.
         // Thus, we can also treat the table itself as hidden content and remove it.
         // Tables which are empty but do not have hidden content will have cells with empty paragraphs inside,
         // which this visitor will not remove.
         if (!table.hasChildNodes())
             table.remove();

         return VisitorAction.CONTINUE;
     }

     /// 
     /// Called when visiting of a Cell node is ended in the document.
     /// 
     public int visitCellEnd(Cell cell) {
         if (!cell.hasChildNodes() && cell.getParentNode() != null)
             cell.remove();

         return VisitorAction.CONTINUE;
     }

     /// 
     /// Called when visiting of a Row node is ended in the document.
     /// 
     public int visitRowEnd(Row row) {
         if (!row.hasChildNodes() && row.getParentNode() != null)
             row.remove();

         return VisitorAction.CONTINUE;
     }
 }
 
```

**Parameters:**
| Parameter | Typ | Beschreibung |
| --- | --- | --- |
| table | [Table](../../com.aspose.words/table/) | Das Objekt, das besucht wird. |

**Returns:**
int - Ein [VisitorAction](../../com.aspose.words/visitoraction/) Wert, der angibt, wie die Aufzählung fortgesetzt werden soll. Der zurückgegebene Wert ist einer der [VisitorAction](../../com.aspose.words/visitoraction/) Konstanten.
### visitTableStart(Table table) {#visitTableStart-com.aspose.words.Table}
```
public int visitTableStart(Table table)
```


Aufgerufen, wenn die Aufzählung einer Tabelle begonnen hat.

 **Examples:** 

Zeigt, wie man die Knotenstruktur jeder Tabelle in einem Dokument ausgibt.

```

 public void tableToText() throws Exception {
     Document doc = new Document(getMyDir() + "DocumentVisitor-compatible features.docx");
     TableStructurePrinter visitor = new TableStructurePrinter();

     // When we get a composite node to accept a document visitor, the visitor visits the accepting node,
     // and then traverses all the node's children in a depth-first manner.
     // The visitor can read and modify each visited node.
     doc.accept(visitor);

     System.out.println(visitor.getText());
 }

 /// 
 /// Traverses a node's non-binary tree of child nodes.
 /// Creates a map in the form of a string of all encountered Table nodes and their children.
 /// 
 public static class TableStructurePrinter extends DocumentVisitor {
     public TableStructurePrinter() {
         mVisitedTables = new StringBuilder();
         mVisitorIsInsideTable = false;
     }

     public String getText() {
         return mVisitedTables.toString();
     }

     /// 
     /// Called when a Run node is encountered in the document.
     /// Runs that are not within tables are not recorded.
     /// 
     public int visitRun(Run run) {
         if (mVisitorIsInsideTable) indentAndAppendLine("[Run] \"" + run.getText() + "\"");

         return VisitorAction.CONTINUE;
     }

     /// 
     /// Called when a Table is encountered in the document.
     /// 
     public int visitTableStart(final Table table) {
         int rows = 0;
         int columns = 0;

         if (table.getRows().getCount() > 0) {
             rows = table.getRows().getCount();
             columns = table.getFirstRow().getCount();
         }

         indentAndAppendLine("[Table start] Size: " + rows + "x" + columns);
         mDocTraversalDepth++;
         mVisitorIsInsideTable = true;

         return VisitorAction.CONTINUE;
     }

     /// 
     /// Called after all the child nodes of a Table node have been visited.
     /// 
     public int visitTableEnd(final Table table) {
         mDocTraversalDepth--;
         indentAndAppendLine("[Table end]");
         mVisitorIsInsideTable = false;

         return VisitorAction.CONTINUE;
     }

     /// 
     /// Called when a Row node is encountered in the document.
     /// 
     public int visitRowStart(final Row row) {
         String rowContents = row.getText().replaceAll("\\u0007", ", ").replaceAll(", , ", "");
         int rowWidth = row.indexOf(row.getLastCell()) + 1;
         int rowIndex = row.getParentTable().indexOf(row);
         String rowStatusInTable = row.isFirstRow() && row.isLastRow() ? "only" : row.isFirstRow() ? "first" : row.isLastRow() ? "last" : "";
         if (!"".equals(rowStatusInTable)) {
             rowStatusInTable = MessageFormat.format(", the {0} row in this table,", rowStatusInTable);
         }

         indentAndAppendLine(MessageFormat.format("[Row start] Row #{0}{1} width {2}, \"{3}\"", ++rowIndex, rowStatusInTable, rowWidth, rowContents));
         mDocTraversalDepth++;

         return VisitorAction.CONTINUE;
     }

     /// 
     /// Called after all the child nodes of a Row node have been visited.
     /// 
     public int visitRowEnd(final Row row) {
         mDocTraversalDepth--;
         indentAndAppendLine("[Row end]");

         return VisitorAction.CONTINUE;
     }

     /// 
     /// Called when a Cell node is encountered in the document.
     /// 
     public int visitCellStart(final Cell cell) {
         Row row = cell.getParentRow();
         Table table = row.getParentTable();
         String cellStatusInRow = cell.isFirstCell() && cell.isLastCell() ? "only" : cell.isFirstCell() ? "first" : cell.isLastCell() ? "last" : "";
         if (!"".equals(cellStatusInRow)) {
             cellStatusInRow = MessageFormat.format(", the {0} cell in this row", cellStatusInRow);
         }

         indentAndAppendLine(MessageFormat.format("[Cell start] Row {0}, Col {1}{2}", table.indexOf(row) + 1, row.indexOf(cell) + 1, cellStatusInRow));
         mDocTraversalDepth++;

         return VisitorAction.CONTINUE;
     }

     /// 
     /// Called after all the child nodes of a Cell node have been visited.
     /// 
     public int visitCellEnd(final Cell cell) {
         mDocTraversalDepth--;
         indentAndAppendLine("[Cell end]");
         return VisitorAction.CONTINUE;
     }

     /// 
     /// Append a line to the StringBuilder, and indent it depending on how deep the visitor is
     /// into the current table's tree of child nodes.
     /// 
     /// 
     private void indentAndAppendLine(final String text) {
         for (int i = 0; i < mDocTraversalDepth; i++) {
             mVisitedTables.append("|  ");
         }

         mVisitedTables.append(text + "\r\n");
     }

     private boolean mVisitorIsInsideTable;
     private int mDocTraversalDepth;
     private final  StringBuilder mVisitedTables;
 }
 
```

**Parameters:**
| Parameter | Typ | Beschreibung |
| --- | --- | --- |
| table | [Table](../../com.aspose.words/table/) | Das Objekt, das besucht wird. |

**Returns:**
int - Ein [VisitorAction](../../com.aspose.words/visitoraction/) Wert, der angibt, wie die Aufzählung fortgesetzt werden soll. Der zurückgegebene Wert ist einer der [VisitorAction](../../com.aspose.words/visitoraction/) Konstanten.
