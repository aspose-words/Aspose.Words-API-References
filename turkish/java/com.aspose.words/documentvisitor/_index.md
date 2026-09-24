---
title: "DocumentVisitor"
linktitle: "DocumentVisitor"
second_title: "Aspose.Words Java için"
description: "Java'da özel belge ziyaretçileri için temel sınıf."
type: docs
weight: 175
url: /tr/java/com.aspose.words/documentvisitor/
---

**Inheritance:**
java.lang.Object
```
public abstract class DocumentVisitor
```

Özel belge ziyaretçileri için temel sınıf.

Daha fazla bilgi edinmek için, [ Aspose.Words Document Object Model (DOM) ][Aspose.Words Document Object Model _DOM_] dokümantasyon makalesini ziyaret edin.

 **Remarks:** 

DocumentVisitor ile [DocumentVisitor](../../com.aspose.words/documentvisitor/) belge ağacının üzerinden geçmeyi gerektiren özel işlemleri tanımlayabilir ve çalıştırabilirsiniz.

Örneğin, Aspose.Words, [DocumentVisitor](../../com.aspose.words/documentvisitor/) ve [Document](../../com.aspose.words/document/) belgeyi çeşitli formatlarda kaydetmek ve bir belgenin bir parçası üzerinde alanları veya yer imlerini bulmak gibi diğer işlemler için dahili olarak kullanır.

[DocumentVisitor](../../com.aspose.words/documentvisitor/) kullanmak için:

1.  [DocumentVisitor](../../com.aspose.words/documentvisitor/)’den türetilen bir sınıf oluşturun.
2.  Bazı veya tüm VisitXXX metodlarını geçersiz kılarak ve uygulayarak özel işlemler gerçekleştirin.
3.  Sayımını başlatmak istediğiniz [Node](../../com.aspose.words/node/) üzerinde [Node.accept(com.aspose.words.DocumentVisitor)](../../com.aspose.words/node/\#accept-com.aspose.words.DocumentVisitor) metodunu çağırın.

[DocumentVisitor](../../com.aspose.words/documentvisitor/) provides default implementations for all of the VisitXXX methods to make it easier to create new document visitors as only the methods required for the particular visitor need to be overridden. It is not necessary to override all of the visitor methods.

Daha fazla bilgi için Visitor tasarım desenine bakın.

 **Examples:** 

Bir belge ziyaretçisini kullanarak belgenin düğüm yapısını nasıl yazdıracağınızı gösterir.

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
## Yöntemler

| Yöntem | Açıklama |
| --- | --- |
| [visitAbsolutePositionTab(AbsolutePositionTab tab)](#visitAbsolutePositionTab-com.aspose.words.AbsolutePositionTab) | Belgede bir [AbsolutePositionTab](../../com.aspose.words/absolutepositiontab/) düğümüyle karşılaşıldığında çağrılır. |
| [visitBodyEnd(Body body)](#visitBodyEnd-com.aspose.words.Body) | Bir bölümdeki ana metin öyküsünün sayımı bittiğinde çağrılır. |
| [visitBodyStart(Body body)](#visitBodyStart-com.aspose.words.Body) | Bir bölümdeki ana metin öyküsünün sayımı başladığında çağrılır. |
| [visitBookmarkEnd(BookmarkEnd bookmarkEnd)](#visitBookmarkEnd-com.aspose.words.BookmarkEnd) | Belgede bir yer iminin sonuyla karşılaşıldığında çağrılır. |
| [visitBookmarkStart(BookmarkStart bookmarkStart)](#visitBookmarkStart-com.aspose.words.BookmarkStart) | Belgede bir yer iminin başlangıcıyla karşılaşıldığında çağrılır. |
| [visitBuildingBlockEnd(BuildingBlock block)](#visitBuildingBlockEnd-com.aspose.words.BuildingBlock) | Bir yapı bloğunun sayımı bittiğinde çağrılır. |
| [visitBuildingBlockStart(BuildingBlock block)](#visitBuildingBlockStart-com.aspose.words.BuildingBlock) | Bir yapı bloğunun sayımı başladığında çağrılır. |
| [visitCellEnd(Cell cell)](#visitCellEnd-com.aspose.words.Cell) | Bir tablo hücresinin sayımı bittiğinde çağrılır. |
| [visitCellStart(Cell cell)](#visitCellStart-com.aspose.words.Cell) | Bir tablo hücresinin sayımı başladığında çağrılır. |
| [visitCommentEnd(Comment comment)](#visitCommentEnd-com.aspose.words.Comment) | Bir yorum metninin sayımı bittiğinde çağrılır. |
| [visitCommentRangeEnd(CommentRangeEnd commentRangeEnd)](#visitCommentRangeEnd-com.aspose.words.CommentRangeEnd) | Yorumlanmış bir metin aralığının sonuyla karşılaşıldığında çağrılır. |
| [visitCommentRangeStart(CommentRangeStart commentRangeStart)](#visitCommentRangeStart-com.aspose.words.CommentRangeStart) | Yorumlanmış bir metin aralığının başlangıcıyla karşılaşıldığında çağrılır. |
| [visitCommentStart(Comment comment)](#visitCommentStart-com.aspose.words.Comment) | Bir yorum metninin sayımı başladığında çağrılır. |
| [visitDocumentEnd(Document doc)](#visitDocumentEnd-com.aspose.words.Document) | Belgenin sayımı tamamlandığında çağrılır. |
| [visitDocumentStart(Document doc)](#visitDocumentStart-com.aspose.words.Document) | Belgenin sayımı başladığında çağrılır. |
| [visitEditableRangeEnd(EditableRangeEnd editableRangeEnd)](#visitEditableRangeEnd-com.aspose.words.EditableRangeEnd) | Belge içinde düzenlenebilir bir aralığın sonu karşılaşıldığında çağrılır. |
| [visitEditableRangeStart(EditableRangeStart editableRangeStart)](#visitEditableRangeStart-com.aspose.words.EditableRangeStart) | Belge içinde düzenlenebilir bir aralığın başlangıcı karşılaşıldığında çağrılır. |
| [visitFieldEnd(FieldEnd fieldEnd)](#visitFieldEnd-com.aspose.words.FieldEnd) | Belge içinde bir alan sona erdiğinde çağrılır. |
| [visitFieldSeparator(FieldSeparator fieldSeparator)](#visitFieldSeparator-com.aspose.words.FieldSeparator) | Belge içinde bir alan ayırıcı karşılaşıldığında çağrılır. |
| [visitFieldStart(FieldStart fieldStart)](#visitFieldStart-com.aspose.words.FieldStart) | Belge içinde bir alan başladığında çağrılır. |
| [visitFootnoteEnd(Footnote footnote)](#visitFootnoteEnd-com.aspose.words.Footnote) | Dipnot veya sonnot metninin numaralandırması bittiğinde çağrılır. |
| [visitFootnoteStart(Footnote footnote)](#visitFootnoteStart-com.aspose.words.Footnote) | Dipnot veya sonnot metninin numaralandırması başladığında çağrılır. |
| [visitFormField(FormField formField)](#visitFormField-com.aspose.words.FormField) | Belge içinde bir form alanı karşılaşıldığında çağrılır. |
| [visitGlossaryDocumentEnd(GlossaryDocument glossary)](#visitGlossaryDocumentEnd-com.aspose.words.GlossaryDocument) | Sözlük belgesinin numaralandırması bittiğinde çağrılır. |
| [visitGlossaryDocumentStart(GlossaryDocument glossary)](#visitGlossaryDocumentStart-com.aspose.words.GlossaryDocument) | Sözlük belgesinin numaralandırması başladığında çağrılır. |
| [visitGroupShapeEnd(GroupShape groupShape)](#visitGroupShapeEnd-com.aspose.words.GroupShape) | Grup şeklinin numaralandırması bittiğinde çağrılır. |
| [visitGroupShapeStart(GroupShape groupShape)](#visitGroupShapeStart-com.aspose.words.GroupShape) | Grup şeklinin numaralandırması başladığında çağrılır. |
| [visitHeaderFooterEnd(HeaderFooter headerFooter)](#visitHeaderFooterEnd-com.aspose.words.HeaderFooter) | Bir bölümdeki üstbilgi veya altbilginin numaralandırması bittiğinde çağrılır. |
| [visitHeaderFooterStart(HeaderFooter headerFooter)](#visitHeaderFooterStart-com.aspose.words.HeaderFooter) | Bir bölümdeki üstbilgi veya altbilginin numaralandırması başladığında çağrılır. |
| [visitOfficeMathEnd(OfficeMath officeMath)](#visitOfficeMathEnd-com.aspose.words.OfficeMath) | Office Math nesnesinin numaralandırması bittiğinde çağrılır. |
| [visitOfficeMathStart(OfficeMath officeMath)](#visitOfficeMathStart-com.aspose.words.OfficeMath) | Office Math nesnesinin numaralandırması başladığında çağrılır. |
| [visitParagraphEnd(Paragraph paragraph)](#visitParagraphEnd-com.aspose.words.Paragraph) | Paragrafın numaralandırması bittiğinde çağrılır. |
| [visitParagraphStart(Paragraph paragraph)](#visitParagraphStart-com.aspose.words.Paragraph) | Paragrafın numaralandırması başladığında çağrılır. |
| [visitRowEnd(Row row)](#visitRowEnd-com.aspose.words.Row) | Tablo satırının numaralandırması bittiğinde çağrılır. |
| [visitRowStart(Row row)](#visitRowStart-com.aspose.words.Row) | Tablo satırının numaralandırması başladığında çağrılır. |
| [visitRun(Run run)](#visitRun-com.aspose.words.Run) | Metin yürütmesi karşılaşıldığında çağrılır. |
| [visitSectionEnd(Section section)](#visitSectionEnd-com.aspose.words.Section) | Bölümün numaralandırması bittiğinde çağrılır. |
| [visitSectionStart(Section section)](#visitSectionStart-com.aspose.words.Section) | Bölümün numaralandırması başladığında çağrılır. |
| [visitShapeEnd(Shape shape)](#visitShapeEnd-com.aspose.words.Shape) | Şeklin numaralandırması bittiğinde çağrılır. |
| [visitShapeStart(Shape shape)](#visitShapeStart-com.aspose.words.Shape) | Şeklin numaralandırması başladığında çağrılır. |
| [visitSmartTagEnd(SmartTag smartTag)](#visitSmartTagEnd-com.aspose.words.SmartTag) | Akıllı etiketin sayımı bittiğinde çağrılır. |
| [visitSmartTagStart(SmartTag smartTag)](#visitSmartTagStart-com.aspose.words.SmartTag) | Akıllı etiketin sayımı başladığında çağrılır. |
| [visitSpecialChar(SpecialChar specialChar)](#visitSpecialChar-com.aspose.words.SpecialChar) | Belgede bir [SpecialChar](../../com.aspose.words/specialchar/) düğümüyle karşılaşıldığında çağrılır. |
| [visitStructuredDocumentTagEnd(StructuredDocumentTag sdt)](#visitStructuredDocumentTagEnd-com.aspose.words.StructuredDocumentTag) | Yapılandırılmış belge etiketinin sayımı bittiğinde çağrılır. |
| [visitStructuredDocumentTagRangeEnd(StructuredDocumentTagRangeEnd sdtRangeEnd)](#visitStructuredDocumentTagRangeEnd-com.aspose.words.StructuredDocumentTagRangeEnd) | Bir StructuredDocumentTagRangeEnd ile karşılaşıldığında çağrılır. |
| [visitStructuredDocumentTagRangeStart(StructuredDocumentTagRangeStart sdtRangeStart)](#visitStructuredDocumentTagRangeStart-com.aspose.words.StructuredDocumentTagRangeStart) | Bir StructuredDocumentTagRangeStart ile karşılaşıldığında çağrılır. |
| [visitStructuredDocumentTagStart(StructuredDocumentTag sdt)](#visitStructuredDocumentTagStart-com.aspose.words.StructuredDocumentTag) | Yapılandırılmış belge etiketinin sayımı başladığında çağrılır. |
| [visitSubDocument(SubDocument subDocument)](#visitSubDocument-com.aspose.words.SubDocument) | Bir alt belgeyle karşılaşıldığında çağrılır. |
| [visitTableEnd(Table table)](#visitTableEnd-com.aspose.words.Table) | Tablonun sayımı bittiğinde çağrılır. |
| [visitTableStart(Table table)](#visitTableStart-com.aspose.words.Table) | Tablonun sayımı başladığında çağrılır. |
### visitAbsolutePositionTab(AbsolutePositionTab tab) {#visitAbsolutePositionTab-com.aspose.words.AbsolutePositionTab}
```
public int visitAbsolutePositionTab(AbsolutePositionTab tab)
```


Belgede bir [AbsolutePositionTab](../../com.aspose.words/absolutepositiontab/) düğümüyle karşılaşıldığında çağrılır.

 **Examples:** 

Bir belge ziyaretçisiyle mutlak konum sek karakterlerini nasıl işleneceğini gösterir.

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
| Parametre | Tür | Açıklama |
| --- | --- | --- |
| tab | [AbsolutePositionTab](../../com.aspose.words/absolutepositiontab/) | Ziyaret edilen nesne. |

**Returns:**
int - Sayımın nasıl devam edeceğini belirten bir [VisitorAction](../../com.aspose.words/visitoraction/) değeri. Döndürülen değer, [VisitorAction](../../com.aspose.words/visitoraction/) sabitlerinden biridir.
### visitBodyEnd(Body body) {#visitBodyEnd-com.aspose.words.Body}
```
public int visitBodyEnd(Body body)
```


Bir bölümdeki ana metin öyküsünün sayımı bittiğinde çağrılır.

 **Examples:** 

Bir belge ziyaretçisini kullanarak belgenin düğüm yapısını nasıl yazdıracağınızı gösterir.

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
| Parametre | Tür | Açıklama |
| --- | --- | --- |
| body | [Body](../../com.aspose.words/body/) | Ziyaret edilen nesne. |

**Returns:**
int - Sayımın nasıl devam edeceğini belirten bir [VisitorAction](../../com.aspose.words/visitoraction/) değeri. Döndürülen değer, [VisitorAction](../../com.aspose.words/visitoraction/) sabitlerinden biridir.
### visitBodyStart(Body body) {#visitBodyStart-com.aspose.words.Body}
```
public int visitBodyStart(Body body)
```


Bir bölümdeki ana metin öyküsünün sayımı başladığında çağrılır.

 **Examples:** 

Bir belge ziyaretçisini kullanarak belgenin düğüm yapısını nasıl yazdıracağınızı gösterir.

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
| Parametre | Tür | Açıklama |
| --- | --- | --- |
| body | [Body](../../com.aspose.words/body/) | Ziyaret edilen nesne. |

**Returns:**
int - Sayımın nasıl devam edeceğini belirten bir [VisitorAction](../../com.aspose.words/visitoraction/) değeri. Döndürülen değer, [VisitorAction](../../com.aspose.words/visitoraction/) sabitlerinden biridir.
### visitBookmarkEnd(BookmarkEnd bookmarkEnd) {#visitBookmarkEnd-com.aspose.words.BookmarkEnd}
```
public int visitBookmarkEnd(BookmarkEnd bookmarkEnd)
```


Belgede bir yer iminin sonuyla karşılaşıldığında çağrılır.

 **Examples:** 

Yer imleri eklemeyi ve içeriklerini güncellemeyi gösterir.

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
| Parametre | Tür | Açıklama |
| --- | --- | --- |
| bookmarkEnd | [BookmarkEnd](../../com.aspose.words/bookmarkend/) | Ziyaret edilen nesne. |

**Returns:**
int - Sayımın nasıl devam edeceğini belirten bir [VisitorAction](../../com.aspose.words/visitoraction/) değeri. Döndürülen değer, [VisitorAction](../../com.aspose.words/visitoraction/) sabitlerinden biridir.
### visitBookmarkStart(BookmarkStart bookmarkStart) {#visitBookmarkStart-com.aspose.words.BookmarkStart}
```
public int visitBookmarkStart(BookmarkStart bookmarkStart)
```


Belgede bir yer iminin başlangıcıyla karşılaşıldığında çağrılır.

 **Examples:** 

Yer imleri eklemeyi ve içeriklerini güncellemeyi gösterir.

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
| Parametre | Tür | Açıklama |
| --- | --- | --- |
| bookmarkStart | [BookmarkStart](../../com.aspose.words/bookmarkstart/) | Ziyaret edilen nesne. |

**Returns:**
int - Sayımın nasıl devam edeceğini belirten bir [VisitorAction](../../com.aspose.words/visitoraction/) değeri. Döndürülen değer, [VisitorAction](../../com.aspose.words/visitoraction/) sabitlerinden biridir.
### visitBuildingBlockEnd(BuildingBlock block) {#visitBuildingBlockEnd-com.aspose.words.BuildingBlock}
```
public int visitBuildingBlockEnd(BuildingBlock block)
```


Bir yapı bloğunun sayımı bittiğinde çağrılır.

 **Remarks:** 

Not: Bir yapı bloğu düğümü ve alt öğeleri, bir [Document](../../com.aspose.words/document/) üzerinde Visitor çalıştırdığınızda ziyaret edilmez. Bir yapı bloğu üzerinde Visitor çalıştırmak istiyorsanız, ziyaretçiyi [GlossaryDocument](../../com.aspose.words/glossarydocument/) üzerinde çalıştırmalı veya [BuildingBlock.accept(com.aspose.words.DocumentVisitor)](../../com.aspose.words/buildingblock/\#accept-com.aspose.words.DocumentVisitor) metodunu çağırmalısınız.

 **Examples:** 

Bir sözlük belgesindeki yapı bloklarına erişim yollarını gösterir.

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
| Parametre | Tür | Açıklama |
| --- | --- | --- |
| block | [BuildingBlock](../../com.aspose.words/buildingblock/) | Ziyaret edilen nesne. |

**Returns:**
int - Sayımın nasıl devam edeceğini belirten bir [VisitorAction](../../com.aspose.words/visitoraction/) değeri. Döndürülen değer, [VisitorAction](../../com.aspose.words/visitoraction/) sabitlerinden biridir.
### visitBuildingBlockStart(BuildingBlock block) {#visitBuildingBlockStart-com.aspose.words.BuildingBlock}
```
public int visitBuildingBlockStart(BuildingBlock block)
```


Bir yapı bloğunun sayımı başladığında çağrılır.

 **Remarks:** 

Not: Bir yapı bloğu düğümü ve alt öğeleri, bir [Document](../../com.aspose.words/document/) üzerinde Visitor çalıştırdığınızda ziyaret edilmez. Bir yapı bloğu üzerinde Visitor çalıştırmak istiyorsanız, ziyaretçiyi [GlossaryDocument](../../com.aspose.words/glossarydocument/) üzerinde çalıştırmalı veya [BuildingBlock.accept(com.aspose.words.DocumentVisitor)](../../com.aspose.words/buildingblock/\#accept-com.aspose.words.DocumentVisitor) metodunu çağırmalısınız.

 **Examples:** 

Bir sözlük belgesindeki yapı bloklarına erişim yollarını gösterir.

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
| Parametre | Tür | Açıklama |
| --- | --- | --- |
| block | [BuildingBlock](../../com.aspose.words/buildingblock/) | Ziyaret edilen nesne. |

**Returns:**
int - Sayımın nasıl devam edeceğini belirten bir [VisitorAction](../../com.aspose.words/visitoraction/) değeri. Döndürülen değer, [VisitorAction](../../com.aspose.words/visitoraction/) sabitlerinden biridir.
### visitCellEnd(Cell cell) {#visitCellEnd-com.aspose.words.Cell}
```
public int visitCellEnd(Cell cell)
```


Bir tablo hücresinin sayımı bittiğinde çağrılır.

 **Examples:** 

Bir belgedeki her tablonun düğüm yapısını nasıl yazdıracağınızı gösterir.

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

Bir DocumentVisitor uygulamasının nasıl kullanılacağını göstererek bir belgeden tüm gizli içeriği kaldırır.

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
| Parametre | Tür | Açıklama |
| --- | --- | --- |
| cell | [Cell](../../com.aspose.words/cell/) | Ziyaret edilen nesne. |

**Returns:**
int - Sayımın nasıl devam edeceğini belirten bir [VisitorAction](../../com.aspose.words/visitoraction/) değeri. Döndürülen değer, [VisitorAction](../../com.aspose.words/visitoraction/) sabitlerinden biridir.
### visitCellStart(Cell cell) {#visitCellStart-com.aspose.words.Cell}
```
public int visitCellStart(Cell cell)
```


Bir tablo hücresinin sayımı başladığında çağrılır.

 **Examples:** 

Bir belgedeki her tablonun düğüm yapısını nasıl yazdıracağınızı gösterir.

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
| Parametre | Tür | Açıklama |
| --- | --- | --- |
| cell | [Cell](../../com.aspose.words/cell/) | Ziyaret edilen nesne. |

**Returns:**
int - Sayımın nasıl devam edeceğini belirten bir [VisitorAction](../../com.aspose.words/visitoraction/) değeri. Döndürülen değer, [VisitorAction](../../com.aspose.words/visitoraction/) sabitlerinden biridir.
### visitCommentEnd(Comment comment) {#visitCommentEnd-com.aspose.words.Comment}
```
public int visitCommentEnd(Comment comment)
```


Bir yorum metninin sayımı bittiğinde çağrılır.

 **Examples:** 

Bir belgedeki her yorum ve yorum aralığının düğüm yapısını nasıl yazdıracağınızı gösterir.

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
| Parametre | Tür | Açıklama |
| --- | --- | --- |
| comment | [Comment](../../com.aspose.words/comment/) | Ziyaret edilen nesne. |

**Returns:**
int - Sayımın nasıl devam edeceğini belirten bir [VisitorAction](../../com.aspose.words/visitoraction/) değeri. Döndürülen değer, [VisitorAction](../../com.aspose.words/visitoraction/) sabitlerinden biridir.
### visitCommentRangeEnd(CommentRangeEnd commentRangeEnd) {#visitCommentRangeEnd-com.aspose.words.CommentRangeEnd}
```
public int visitCommentRangeEnd(CommentRangeEnd commentRangeEnd)
```


Yorumlanmış bir metin aralığının sonuyla karşılaşıldığında çağrılır.

 **Examples:** 

Bir belgedeki her yorum ve yorum aralığının düğüm yapısını nasıl yazdıracağınızı gösterir.

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
| Parametre | Tür | Açıklama |
| --- | --- | --- |
| commentRangeEnd | [CommentRangeEnd](../../com.aspose.words/commentrangeend/) | Ziyaret edilen nesne. |

**Returns:**
int - Sayımın nasıl devam edeceğini belirten bir [VisitorAction](../../com.aspose.words/visitoraction/) değeri. Döndürülen değer, [VisitorAction](../../com.aspose.words/visitoraction/) sabitlerinden biridir.
### visitCommentRangeStart(CommentRangeStart commentRangeStart) {#visitCommentRangeStart-com.aspose.words.CommentRangeStart}
```
public int visitCommentRangeStart(CommentRangeStart commentRangeStart)
```


Yorumlanmış bir metin aralığının başlangıcıyla karşılaşıldığında çağrılır.

 **Examples:** 

Bir belgedeki her yorum ve yorum aralığının düğüm yapısını nasıl yazdıracağınızı gösterir.

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
| Parametre | Tür | Açıklama |
| --- | --- | --- |
| commentRangeStart | [CommentRangeStart](../../com.aspose.words/commentrangestart/) | Ziyaret edilen nesne. |

**Returns:**
int - Sayımın nasıl devam edeceğini belirten bir [VisitorAction](../../com.aspose.words/visitoraction/) değeri. Döndürülen değer, [VisitorAction](../../com.aspose.words/visitoraction/) sabitlerinden biridir.
### visitCommentStart(Comment comment) {#visitCommentStart-com.aspose.words.Comment}
```
public int visitCommentStart(Comment comment)
```


Bir yorum metninin sayımı başladığında çağrılır.

 **Examples:** 

Bir belgedeki her yorum ve yorum aralığının düğüm yapısını nasıl yazdıracağınızı gösterir.

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

Bir DocumentVisitor uygulamasının nasıl kullanılacağını göstererek bir belgeden tüm gizli içeriği kaldırır.

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
| Parametre | Tür | Açıklama |
| --- | --- | --- |
| comment | [Comment](../../com.aspose.words/comment/) | Ziyaret edilen nesne. |

**Returns:**
int - Sayımın nasıl devam edeceğini belirten bir [VisitorAction](../../com.aspose.words/visitoraction/) değeri. Döndürülen değer, [VisitorAction](../../com.aspose.words/visitoraction/) sabitlerinden biridir.
### visitDocumentEnd(Document doc) {#visitDocumentEnd-com.aspose.words.Document}
```
public int visitDocumentEnd(Document doc)
```


Belgenin sayımı tamamlandığında çağrılır.

 **Examples:** 

Bir belge ziyaretçisini kullanarak belgenin düğüm yapısını nasıl yazdıracağınızı gösterir.

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
| Parametre | Tür | Açıklama |
| --- | --- | --- |
| doc | [Document](../../com.aspose.words/document/) | Ziyaret edilen nesne. |

**Returns:**
int - Sayımın nasıl devam edeceğini belirten bir [VisitorAction](../../com.aspose.words/visitoraction/) değeri. Döndürülen değer, [VisitorAction](../../com.aspose.words/visitoraction/) sabitlerinden biridir.
### visitDocumentStart(Document doc) {#visitDocumentStart-com.aspose.words.Document}
```
public int visitDocumentStart(Document doc)
```


Belgenin sayımı başladığında çağrılır.

 **Examples:** 

Bir belge ziyaretçisini kullanarak belgenin düğüm yapısını nasıl yazdıracağınızı gösterir.

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
| Parametre | Tür | Açıklama |
| --- | --- | --- |
| doc | [Document](../../com.aspose.words/document/) | Ziyaret edilen nesne. |

**Returns:**
int - Sayımın nasıl devam edeceğini belirten bir [VisitorAction](../../com.aspose.words/visitoraction/) değeri. Döndürülen değer, [VisitorAction](../../com.aspose.words/visitoraction/) sabitlerinden biridir.
### visitEditableRangeEnd(EditableRangeEnd editableRangeEnd) {#visitEditableRangeEnd-com.aspose.words.EditableRangeEnd}
```
public int visitEditableRangeEnd(EditableRangeEnd editableRangeEnd)
```


Belge içinde düzenlenebilir bir aralığın sonu karşılaşıldığında çağrılır.

 **Examples:** 

Bir belgedeki her düzenlenebilir aralığın düğüm yapısını nasıl yazdıracağınızı gösterir.

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
| Parametre | Tür | Açıklama |
| --- | --- | --- |
| editableRangeEnd | [EditableRangeEnd](../../com.aspose.words/editablerangeend/) | Ziyaret edilen nesne. |

**Returns:**
int - Sayımın nasıl devam edeceğini belirten bir [VisitorAction](../../com.aspose.words/visitoraction/) değeri. Döndürülen değer, [VisitorAction](../../com.aspose.words/visitoraction/) sabitlerinden biridir.
### visitEditableRangeStart(EditableRangeStart editableRangeStart) {#visitEditableRangeStart-com.aspose.words.EditableRangeStart}
```
public int visitEditableRangeStart(EditableRangeStart editableRangeStart)
```


Belge içinde düzenlenebilir bir aralığın başlangıcı karşılaşıldığında çağrılır.

 **Examples:** 

Bir belgedeki her düzenlenebilir aralığın düğüm yapısını nasıl yazdıracağınızı gösterir.

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
| Parametre | Tür | Açıklama |
| --- | --- | --- |
| editableRangeStart | [EditableRangeStart](../../com.aspose.words/editablerangestart/) | Ziyaret edilen nesne. |

**Returns:**
int - Sayımın nasıl devam edeceğini belirten bir [VisitorAction](../../com.aspose.words/visitoraction/) değeri. Döndürülen değer, [VisitorAction](../../com.aspose.words/visitoraction/) sabitlerinden biridir.
### visitFieldEnd(FieldEnd fieldEnd) {#visitFieldEnd-com.aspose.words.FieldEnd}
```
public int visitFieldEnd(FieldEnd fieldEnd)
```


Belge içinde bir alan sona erdiğinde çağrılır.

 **Remarks:** 

Daha fazla bilgi için [visitFieldStart(com.aspose.words.FieldStart)](../../com.aspose.words/documentvisitor/\#visitFieldStart-com.aspose.words.FieldStart) adresine bakın.

 **Examples:** 

Bir belgedeki her alanın düğüm yapısını nasıl yazdıracağınızı gösterir.

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
| Parametre | Tür | Açıklama |
| --- | --- | --- |
| fieldEnd | [FieldEnd](../../com.aspose.words/fieldend/) | Ziyaret edilen nesne. |

**Returns:**
int - Sayımın nasıl devam edeceğini belirten bir [VisitorAction](../../com.aspose.words/visitoraction/) değeri. Döndürülen değer, [VisitorAction](../../com.aspose.words/visitoraction/) sabitlerinden biridir.
### visitFieldSeparator(FieldSeparator fieldSeparator) {#visitFieldSeparator-com.aspose.words.FieldSeparator}
```
public int visitFieldSeparator(FieldSeparator fieldSeparator)
```


Belge içinde bir alan ayırıcı karşılaşıldığında çağrılır.

 **Remarks:** 

Alan ayırıcı, belge içinde alan kodunu alan değerinden ayırır. Bazı alanların yalnızca alan kodu olduğunu ve alan ayırıcı ve alan değerine sahip olmadığını unutmayın.

Daha fazla bilgi için [visitFieldStart(com.aspose.words.FieldStart)](../../com.aspose.words/documentvisitor/\#visitFieldStart-com.aspose.words.FieldStart) adresine bakın.

 **Examples:** 

Bir belgedeki her alanın düğüm yapısını nasıl yazdıracağınızı gösterir.

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
| Parametre | Tür | Açıklama |
| --- | --- | --- |
| fieldSeparator | [FieldSeparator](../../com.aspose.words/fieldseparator/) | Ziyaret edilen nesne. |

**Returns:**
int - Sayımın nasıl devam edeceğini belirten bir [VisitorAction](../../com.aspose.words/visitoraction/) değeri. Döndürülen değer, [VisitorAction](../../com.aspose.words/visitoraction/) sabitlerinden biridir.
### visitFieldStart(FieldStart fieldStart) {#visitFieldStart-com.aspose.words.FieldStart}
```
public int visitFieldStart(FieldStart fieldStart)
```


Belge içinde bir alan başladığında çağrılır.

 **Remarks:** 

Word belgesindeki bir alan, alan kodu ve alan değerinden oluşur.

Örneğin, sayfa numarasını gösteren bir alan aşağıdaki gibi temsil edilebilir:

[FieldStart]PAGE[FieldSeparator]98[FieldEnd]

Alan ayırıcı, belge içinde alan kodunu alan değerinden ayırır. Bazı alanların yalnızca alan kodu olduğunu ve alan ayırıcı ve alan değerine sahip olmadığını unutmayın.

Alanlar iç içe olabilir.

 **Examples:** 

Bir belgedeki her alanın düğüm yapısını nasıl yazdıracağınızı gösterir.

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
| Parametre | Tür | Açıklama |
| --- | --- | --- |
| fieldStart | [FieldStart](../../com.aspose.words/fieldstart/) | Ziyaret edilen nesne. |

**Returns:**
int - Sayımın nasıl devam edeceğini belirten bir [VisitorAction](../../com.aspose.words/visitoraction/) değeri. Döndürülen değer, [VisitorAction](../../com.aspose.words/visitoraction/) sabitlerinden biridir.
### visitFootnoteEnd(Footnote footnote) {#visitFootnoteEnd-com.aspose.words.Footnote}
```
public int visitFootnoteEnd(Footnote footnote)
```


Dipnot veya sonnot metninin numaralandırması bittiğinde çağrılır.

 **Examples:** 

Bir belgedeki her dipnotun düğüm yapısını nasıl yazdıracağınızı gösterir.

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
| Parametre | Tür | Açıklama |
| --- | --- | --- |
| footnote | [Footnote](../../com.aspose.words/footnote/) | Ziyaret edilen nesne. |

**Returns:**
int - Sayımın nasıl devam edeceğini belirten bir [VisitorAction](../../com.aspose.words/visitoraction/) değeri. Döndürülen değer, [VisitorAction](../../com.aspose.words/visitoraction/) sabitlerinden biridir.
### visitFootnoteStart(Footnote footnote) {#visitFootnoteStart-com.aspose.words.Footnote}
```
public int visitFootnoteStart(Footnote footnote)
```


Dipnot veya sonnot metninin numaralandırması başladığında çağrılır.

 **Examples:** 

Bir belgedeki her dipnotun düğüm yapısını nasıl yazdıracağınızı gösterir.

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

Bir DocumentVisitor uygulamasının nasıl kullanılacağını göstererek bir belgeden tüm gizli içeriği kaldırır.

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
| Parametre | Tür | Açıklama |
| --- | --- | --- |
| footnote | [Footnote](../../com.aspose.words/footnote/) | Ziyaret edilen nesne. |

**Returns:**
int - Sayımın nasıl devam edeceğini belirten bir [VisitorAction](../../com.aspose.words/visitoraction/) değeri. Döndürülen değer, [VisitorAction](../../com.aspose.words/visitoraction/) sabitlerinden biridir.
### visitFormField(FormField formField) {#visitFormField-com.aspose.words.FormField}
```
public int visitFormField(FormField formField)
```


Belge içinde bir form alanı karşılaşıldığında çağrılır.

 **Examples:** 

Bir DocumentVisitor uygulamasının nasıl kullanılacağını göstererek bir belgeden tüm gizli içeriği kaldırır.

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
| Parametre | Tür | Açıklama |
| --- | --- | --- |
| formField | [FormField](../../com.aspose.words/formfield/) | Ziyaret edilen nesne. |

**Returns:**
int - Sayımın nasıl devam edeceğini belirten bir [VisitorAction](../../com.aspose.words/visitoraction/) değeri. Döndürülen değer, [VisitorAction](../../com.aspose.words/visitoraction/) sabitlerinden biridir.
### visitGlossaryDocumentEnd(GlossaryDocument glossary) {#visitGlossaryDocumentEnd-com.aspose.words.GlossaryDocument}
```
public int visitGlossaryDocumentEnd(GlossaryDocument glossary)
```


Sözlük belgesinin numaralandırması bittiğinde çağrılır.

 **Remarks:** 

Not: Bir sözlük belge düğümü ve alt öğeleri, bir Visitor'ı bir [Document](../../com.aspose.words/document/) üzerinde çalıştırdığınızda ziyaret edilmez. Bir sözlük belge üzerinde Visitor çalıştırmak istiyorsanız, [GlossaryDocument.accept(com.aspose.words.DocumentVisitor)](../../com.aspose.words/glossarydocument/\#accept-com.aspose.words.DocumentVisitor) metodunu çağırmanız gerekir.

 **Examples:** 

Bir sözlük belgesindeki yapı bloklarına erişim yollarını gösterir.

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
| Parametre | Tür | Açıklama |
| --- | --- | --- |
| glossary | [GlossaryDocument](../../com.aspose.words/glossarydocument/) | Ziyaret edilen nesne. |

**Returns:**
int - Sayımın nasıl devam edeceğini belirten bir [VisitorAction](../../com.aspose.words/visitoraction/) değeri. Döndürülen değer, [VisitorAction](../../com.aspose.words/visitoraction/) sabitlerinden biridir.
### visitGlossaryDocumentStart(GlossaryDocument glossary) {#visitGlossaryDocumentStart-com.aspose.words.GlossaryDocument}
```
public int visitGlossaryDocumentStart(GlossaryDocument glossary)
```


Sözlük belgesinin numaralandırması başladığında çağrılır.

 **Remarks:** 

Not: Bir sözlük belge düğümü ve alt öğeleri, bir Visitor'ı bir [Document](../../com.aspose.words/document/) üzerinde çalıştırdığınızda ziyaret edilmez. Bir sözlük belge üzerinde Visitor çalıştırmak istiyorsanız, [GlossaryDocument.accept(com.aspose.words.DocumentVisitor)](../../com.aspose.words/glossarydocument/\#accept-com.aspose.words.DocumentVisitor) metodunu çağırmanız gerekir.

 **Examples:** 

Bir sözlük belgesindeki yapı bloklarına erişim yollarını gösterir.

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
| Parametre | Tür | Açıklama |
| --- | --- | --- |
| glossary | [GlossaryDocument](../../com.aspose.words/glossarydocument/) | Ziyaret edilen nesne. |

**Returns:**
int - Sayımın nasıl devam edeceğini belirten bir [VisitorAction](../../com.aspose.words/visitoraction/) değeri. Döndürülen değer, [VisitorAction](../../com.aspose.words/visitoraction/) sabitlerinden biridir.
### visitGroupShapeEnd(GroupShape groupShape) {#visitGroupShapeEnd-com.aspose.words.GroupShape}
```
public int visitGroupShapeEnd(GroupShape groupShape)
```


Grup şeklinin numaralandırması bittiğinde çağrılır.

 **Examples:** 

Bir şekil grubunun nasıl oluşturulacağını ve içeriğinin bir belge ziyaretçisi kullanılarak nasıl yazdırılacağını gösterir.

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
| Parametre | Tür | Açıklama |
| --- | --- | --- |
| groupShape | [GroupShape](../../com.aspose.words/groupshape/) | Ziyaret edilen nesne. |

**Returns:**
int - Sayımın nasıl devam edeceğini belirten bir [VisitorAction](../../com.aspose.words/visitoraction/) değeri. Döndürülen değer, [VisitorAction](../../com.aspose.words/visitoraction/) sabitlerinden biridir.
### visitGroupShapeStart(GroupShape groupShape) {#visitGroupShapeStart-com.aspose.words.GroupShape}
```
public int visitGroupShapeStart(GroupShape groupShape)
```


Grup şeklinin numaralandırması başladığında çağrılır.

 **Examples:** 

Bir şekil grubunun nasıl oluşturulacağını ve içeriğinin bir belge ziyaretçisi kullanılarak nasıl yazdırılacağını gösterir.

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

Bir DocumentVisitor uygulamasının nasıl kullanılacağını göstererek bir belgeden tüm gizli içeriği kaldırır.

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
| Parametre | Tür | Açıklama |
| --- | --- | --- |
| groupShape | [GroupShape](../../com.aspose.words/groupshape/) | Ziyaret edilen nesne. |

**Returns:**
int - Sayımın nasıl devam edeceğini belirten bir [VisitorAction](../../com.aspose.words/visitoraction/) değeri. Döndürülen değer, [VisitorAction](../../com.aspose.words/visitoraction/) sabitlerinden biridir.
### visitHeaderFooterEnd(HeaderFooter headerFooter) {#visitHeaderFooterEnd-com.aspose.words.HeaderFooter}
```
public int visitHeaderFooterEnd(HeaderFooter headerFooter)
```


Bir bölümdeki üstbilgi veya altbilginin numaralandırması bittiğinde çağrılır.

 **Examples:** 

Bir belgede her başlık ve altbilginin düğüm yapısının nasıl yazdırılacağını gösterir.

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
| Parametre | Tür | Açıklama |
| --- | --- | --- |
| headerFooter | [HeaderFooter](../../com.aspose.words/headerfooter/) | Ziyaret edilen nesne. |

**Returns:**
int - Sayımın nasıl devam edeceğini belirten bir [VisitorAction](../../com.aspose.words/visitoraction/) değeri. Döndürülen değer, [VisitorAction](../../com.aspose.words/visitoraction/) sabitlerinden biridir.
### visitHeaderFooterStart(HeaderFooter headerFooter) {#visitHeaderFooterStart-com.aspose.words.HeaderFooter}
```
public int visitHeaderFooterStart(HeaderFooter headerFooter)
```


Bir bölümdeki üstbilgi veya altbilginin numaralandırması başladığında çağrılır.

 **Examples:** 

Bir belgede her başlık ve altbilginin düğüm yapısının nasıl yazdırılacağını gösterir.

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
| Parametre | Tür | Açıklama |
| --- | --- | --- |
| headerFooter | [HeaderFooter](../../com.aspose.words/headerfooter/) | Ziyaret edilen nesne. |

**Returns:**
int - Sayımın nasıl devam edeceğini belirten bir [VisitorAction](../../com.aspose.words/visitoraction/) değeri. Döndürülen değer, [VisitorAction](../../com.aspose.words/visitoraction/) sabitlerinden biridir.
### visitOfficeMathEnd(OfficeMath officeMath) {#visitOfficeMathEnd-com.aspose.words.OfficeMath}
```
public int visitOfficeMathEnd(OfficeMath officeMath)
```


Office Math nesnesinin numaralandırması bittiğinde çağrılır.

 **Examples:** 

Bir belgede her Office Math düğümünün düğüm yapısının nasıl yazdırılacağını gösterir.

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
| Parametre | Tür | Açıklama |
| --- | --- | --- |
| officeMath | [OfficeMath](../../com.aspose.words/officemath/) | Ziyaret edilen nesne. |

**Returns:**
int - Sayımın nasıl devam edeceğini belirten bir [VisitorAction](../../com.aspose.words/visitoraction/) değeri. Döndürülen değer, [VisitorAction](../../com.aspose.words/visitoraction/) sabitlerinden biridir.
### visitOfficeMathStart(OfficeMath officeMath) {#visitOfficeMathStart-com.aspose.words.OfficeMath}
```
public int visitOfficeMathStart(OfficeMath officeMath)
```


Office Math nesnesinin numaralandırması başladığında çağrılır.

 **Examples:** 

Bir belgede her Office Math düğümünün düğüm yapısının nasıl yazdırılacağını gösterir.

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
| Parametre | Tür | Açıklama |
| --- | --- | --- |
| officeMath | [OfficeMath](../../com.aspose.words/officemath/) | Ziyaret edilen nesne. |

**Returns:**
int - Sayımın nasıl devam edeceğini belirten bir [VisitorAction](../../com.aspose.words/visitoraction/) değeri. Döndürülen değer, [VisitorAction](../../com.aspose.words/visitoraction/) sabitlerinden biridir.
### visitParagraphEnd(Paragraph paragraph) {#visitParagraphEnd-com.aspose.words.Paragraph}
```
public int visitParagraphEnd(Paragraph paragraph)
```


Paragrafın numaralandırması bittiğinde çağrılır.

 **Examples:** 

Bir belge ziyaretçisini kullanarak belgenin düğüm yapısını nasıl yazdıracağınızı gösterir.

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
| Parametre | Tür | Açıklama |
| --- | --- | --- |
| paragraph | [Paragraph](../../com.aspose.words/paragraph/) | Ziyaret edilen nesne. |

**Returns:**
int - Sayımın nasıl devam edeceğini belirten bir [VisitorAction](../../com.aspose.words/visitoraction/) değeri. Döndürülen değer, [VisitorAction](../../com.aspose.words/visitoraction/) sabitlerinden biridir.
### visitParagraphStart(Paragraph paragraph) {#visitParagraphStart-com.aspose.words.Paragraph}
```
public int visitParagraphStart(Paragraph paragraph)
```


Paragrafın numaralandırması başladığında çağrılır.

 **Examples:** 

Bir belge ziyaretçisini kullanarak belgenin düğüm yapısını nasıl yazdıracağınızı gösterir.

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

Bir DocumentVisitor uygulamasının nasıl kullanılacağını göstererek bir belgeden tüm gizli içeriği kaldırır.

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
| Parametre | Tür | Açıklama |
| --- | --- | --- |
| paragraph | [Paragraph](../../com.aspose.words/paragraph/) | Ziyaret edilen nesne. |

**Returns:**
int - Sayımın nasıl devam edeceğini belirten bir [VisitorAction](../../com.aspose.words/visitoraction/) değeri. Döndürülen değer, [VisitorAction](../../com.aspose.words/visitoraction/) sabitlerinden biridir.
### visitRowEnd(Row row) {#visitRowEnd-com.aspose.words.Row}
```
public int visitRowEnd(Row row)
```


Tablo satırının numaralandırması bittiğinde çağrılır.

 **Examples:** 

Bir belgedeki her tablonun düğüm yapısını nasıl yazdıracağınızı gösterir.

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

Bir DocumentVisitor uygulamasının nasıl kullanılacağını göstererek bir belgeden tüm gizli içeriği kaldırır.

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
| Parametre | Tür | Açıklama |
| --- | --- | --- |
| row | [Row](../../com.aspose.words/row/) | Ziyaret edilen nesne. |

**Returns:**
int - Sayımın nasıl devam edeceğini belirten bir [VisitorAction](../../com.aspose.words/visitoraction/) değeri. Döndürülen değer, [VisitorAction](../../com.aspose.words/visitoraction/) sabitlerinden biridir.
### visitRowStart(Row row) {#visitRowStart-com.aspose.words.Row}
```
public int visitRowStart(Row row)
```


Tablo satırının numaralandırması başladığında çağrılır.

 **Examples:** 

Bir belgedeki her tablonun düğüm yapısını nasıl yazdıracağınızı gösterir.

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
| Parametre | Tür | Açıklama |
| --- | --- | --- |
| row | [Row](../../com.aspose.words/row/) | Ziyaret edilen nesne. |

**Returns:**
int - Sayımın nasıl devam edeceğini belirten bir [VisitorAction](../../com.aspose.words/visitoraction/) değeri. Döndürülen değer, [VisitorAction](../../com.aspose.words/visitoraction/) sabitlerinden biridir.
### visitRun(Run run) {#visitRun-com.aspose.words.Run}
```
public int visitRun(Run run)
```


Metin yürütmesi karşılaşıldığında çağrılır.

 **Examples:** 

Bir belge ziyaretçisini kullanarak belgenin düğüm yapısını nasıl yazdıracağınızı gösterir.

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
| Parametre | Tür | Açıklama |
| --- | --- | --- |
| run | [Run](../../com.aspose.words/run/) | Ziyaret edilen nesne. |

**Returns:**
int - Sayımın nasıl devam edeceğini belirten bir [VisitorAction](../../com.aspose.words/visitoraction/) değeri. Döndürülen değer, [VisitorAction](../../com.aspose.words/visitoraction/) sabitlerinden biridir.
### visitSectionEnd(Section section) {#visitSectionEnd-com.aspose.words.Section}
```
public int visitSectionEnd(Section section)
```


Bölümün numaralandırması bittiğinde çağrılır.

 **Examples:** 

Bir belge ziyaretçisini kullanarak belgenin düğüm yapısını nasıl yazdıracağınızı gösterir.

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
| Parametre | Tür | Açıklama |
| --- | --- | --- |
| section | [Section](../../com.aspose.words/section/) | Ziyaret edilen nesne. |

**Returns:**
int - Sayımın nasıl devam edeceğini belirten bir [VisitorAction](../../com.aspose.words/visitoraction/) değeri. Döndürülen değer, [VisitorAction](../../com.aspose.words/visitoraction/) sabitlerinden biridir.
### visitSectionStart(Section section) {#visitSectionStart-com.aspose.words.Section}
```
public int visitSectionStart(Section section)
```


Bölümün numaralandırması başladığında çağrılır.

 **Examples:** 

Bir belge ziyaretçisini kullanarak belgenin düğüm yapısını nasıl yazdıracağınızı gösterir.

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
| Parametre | Tür | Açıklama |
| --- | --- | --- |
| section | [Section](../../com.aspose.words/section/) | Ziyaret edilen nesne. |

**Returns:**
int - Sayımın nasıl devam edeceğini belirten bir [VisitorAction](../../com.aspose.words/visitoraction/) değeri. Döndürülen değer, [VisitorAction](../../com.aspose.words/visitoraction/) sabitlerinden biridir.
### visitShapeEnd(Shape shape) {#visitShapeEnd-com.aspose.words.Shape}
```
public int visitShapeEnd(Shape shape)
```


Şeklin numaralandırması bittiğinde çağrılır.

 **Examples:** 

Bir şekil grubunun nasıl oluşturulacağını ve içeriğinin bir belge ziyaretçisi kullanılarak nasıl yazdırılacağını gösterir.

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
| Parametre | Tür | Açıklama |
| --- | --- | --- |
| shape | [Shape](../../com.aspose.words/shape/) | Ziyaret edilen nesne. |

**Returns:**
int - Sayımın nasıl devam edeceğini belirten bir [VisitorAction](../../com.aspose.words/visitoraction/) değeri. Döndürülen değer, [VisitorAction](../../com.aspose.words/visitoraction/) sabitlerinden biridir.
### visitShapeStart(Shape shape) {#visitShapeStart-com.aspose.words.Shape}
```
public int visitShapeStart(Shape shape)
```


Şeklin numaralandırması başladığında çağrılır.

 **Examples:** 

Bir şekil grubunun nasıl oluşturulacağını ve içeriğinin bir belge ziyaretçisi kullanılarak nasıl yazdırılacağını gösterir.

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

Bir DocumentVisitor uygulamasının nasıl kullanılacağını göstererek bir belgeden tüm gizli içeriği kaldırır.

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
| Parametre | Tür | Açıklama |
| --- | --- | --- |
| shape | [Shape](../../com.aspose.words/shape/) | Ziyaret edilen nesne. |

**Returns:**
int - Sayımın nasıl devam edeceğini belirten bir [VisitorAction](../../com.aspose.words/visitoraction/) değeri. Döndürülen değer, [VisitorAction](../../com.aspose.words/visitoraction/) sabitlerinden biridir.
### visitSmartTagEnd(SmartTag smartTag) {#visitSmartTagEnd-com.aspose.words.SmartTag}
```
public int visitSmartTagEnd(SmartTag smartTag)
```


Akıllı etiketin sayımı bittiğinde çağrılır.

 **Examples:** 

Bir belgede her akıllı etiketin düğüm yapısının nasıl yazdırılacağını gösterir.

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
| Parametre | Tür | Açıklama |
| --- | --- | --- |
| smartTag | [SmartTag](../../com.aspose.words/smarttag/) | Ziyaret edilen nesne. |

**Returns:**
int - Sayımın nasıl devam edeceğini belirten bir [VisitorAction](../../com.aspose.words/visitoraction/) değeri. Döndürülen değer, [VisitorAction](../../com.aspose.words/visitoraction/) sabitlerinden biridir.
### visitSmartTagStart(SmartTag smartTag) {#visitSmartTagStart-com.aspose.words.SmartTag}
```
public int visitSmartTagStart(SmartTag smartTag)
```


Akıllı etiketin sayımı başladığında çağrılır.

 **Examples:** 

Bir belgede her akıllı etiketin düğüm yapısının nasıl yazdırılacağını gösterir.

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
| Parametre | Tür | Açıklama |
| --- | --- | --- |
| smartTag | [SmartTag](../../com.aspose.words/smarttag/) | Ziyaret edilen nesne. |

**Returns:**
int - Sayımın nasıl devam edeceğini belirten bir [VisitorAction](../../com.aspose.words/visitoraction/) değeri. Döndürülen değer, [VisitorAction](../../com.aspose.words/visitoraction/) sabitlerinden biridir.
### visitSpecialChar(SpecialChar specialChar) {#visitSpecialChar-com.aspose.words.SpecialChar}
```
public int visitSpecialChar(SpecialChar specialChar)
```


Belgede bir [SpecialChar](../../com.aspose.words/specialchar/) düğümüyle karşılaşıldığında çağrılır.

 **Remarks:** 

Bu yöntem, belgede bulunabilecek genel kontrol karakterleri için (bkz. [ControlChar](../../com.aspose.words/controlchar/)) çağrılmamalıdır.

 **Examples:** 

Bir DocumentVisitor uygulamasının nasıl kullanılacağını göstererek bir belgeden tüm gizli içeriği kaldırır.

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
| Parametre | Tür | Açıklama |
| --- | --- | --- |
| specialChar | [SpecialChar](../../com.aspose.words/specialchar/) | Ziyaret edilen nesne. |

**Returns:**
int - Sayımın nasıl devam edeceğini belirten bir [VisitorAction](../../com.aspose.words/visitoraction/) değeri. Döndürülen değer, [VisitorAction](../../com.aspose.words/visitoraction/) sabitlerinden biridir.
### visitStructuredDocumentTagEnd(StructuredDocumentTag sdt) {#visitStructuredDocumentTagEnd-com.aspose.words.StructuredDocumentTag}
```
public int visitStructuredDocumentTagEnd(StructuredDocumentTag sdt)
```


Yapılandırılmış belge etiketinin sayımı bittiğinde çağrılır.

 **Examples:** 

Bir belgede her yapılandırılmış belge etiketinin düğüm yapısının nasıl yazdırılacağını gösterir.

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
| Parametre | Tür | Açıklama |
| --- | --- | --- |
| sdt | [StructuredDocumentTag](../../com.aspose.words/structureddocumenttag/) | Ziyaret edilen nesne. |

**Returns:**
int - Sayımın nasıl devam edeceğini belirten bir [VisitorAction](../../com.aspose.words/visitoraction/) değeri. Döndürülen değer, [VisitorAction](../../com.aspose.words/visitoraction/) sabitlerinden biridir.
### visitStructuredDocumentTagRangeEnd(StructuredDocumentTagRangeEnd sdtRangeEnd) {#visitStructuredDocumentTagRangeEnd-com.aspose.words.StructuredDocumentTagRangeEnd}
```
public int visitStructuredDocumentTagRangeEnd(StructuredDocumentTagRangeEnd sdtRangeEnd)
```


Bir StructuredDocumentTagRangeEnd ile karşılaşıldığında çağrılır.

 **Examples:** 

Bir belge ziyaretçisini kullanarak belgenin düğüm yapısını nasıl yazdıracağınızı gösterir.

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
| Parametre | Tür | Açıklama |
| --- | --- | --- |
| sdtRangeEnd | [StructuredDocumentTagRangeEnd](../../com.aspose.words/structureddocumenttagrangeend/) |  |

**Returns:**
int
### visitStructuredDocumentTagRangeStart(StructuredDocumentTagRangeStart sdtRangeStart) {#visitStructuredDocumentTagRangeStart-com.aspose.words.StructuredDocumentTagRangeStart}
```
public int visitStructuredDocumentTagRangeStart(StructuredDocumentTagRangeStart sdtRangeStart)
```


Bir StructuredDocumentTagRangeStart ile karşılaşıldığında çağrılır.

 **Examples:** 

Bir belge ziyaretçisini kullanarak belgenin düğüm yapısını nasıl yazdıracağınızı gösterir.

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
| Parametre | Tür | Açıklama |
| --- | --- | --- |
| sdtRangeStart | [StructuredDocumentTagRangeStart](../../com.aspose.words/structureddocumenttagrangestart/) |  |

**Returns:**
int
### visitStructuredDocumentTagStart(StructuredDocumentTag sdt) {#visitStructuredDocumentTagStart-com.aspose.words.StructuredDocumentTag}
```
public int visitStructuredDocumentTagStart(StructuredDocumentTag sdt)
```


Yapılandırılmış belge etiketinin sayımı başladığında çağrılır.

 **Examples:** 

Bir belgede her yapılandırılmış belge etiketinin düğüm yapısının nasıl yazdırılacağını gösterir.

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
| Parametre | Tür | Açıklama |
| --- | --- | --- |
| sdt | [StructuredDocumentTag](../../com.aspose.words/structureddocumenttag/) | Ziyaret edilen nesne. |

**Returns:**
int - Sayımın nasıl devam edeceğini belirten bir [VisitorAction](../../com.aspose.words/visitoraction/) değeri. Döndürülen değer, [VisitorAction](../../com.aspose.words/visitoraction/) sabitlerinden biridir.
### visitSubDocument(SubDocument subDocument) {#visitSubDocument-com.aspose.words.SubDocument}
```
public int visitSubDocument(SubDocument subDocument)
```


Bir alt belgeyle karşılaşıldığında çağrılır.

 **Examples:** 

Bir belge ziyaretçisini kullanarak belgenin düğüm yapısını nasıl yazdıracağınızı gösterir.

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
| Parametre | Tür | Açıklama |
| --- | --- | --- |
| subDocument | [SubDocument](../../com.aspose.words/subdocument/) | Ziyaret edilen nesne. |

**Returns:**
int - Sayımın nasıl devam edeceğini belirten bir [VisitorAction](../../com.aspose.words/visitoraction/) değeri. Döndürülen değer, [VisitorAction](../../com.aspose.words/visitoraction/) sabitlerinden biridir.
### visitTableEnd(Table table) {#visitTableEnd-com.aspose.words.Table}
```
public int visitTableEnd(Table table)
```


Tablonun sayımı bittiğinde çağrılır.

 **Examples:** 

Bir belgedeki her tablonun düğüm yapısını nasıl yazdıracağınızı gösterir.

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

Bir DocumentVisitor uygulamasının nasıl kullanılacağını göstererek bir belgeden tüm gizli içeriği kaldırır.

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
| Parametre | Tür | Açıklama |
| --- | --- | --- |
| table | [Table](../../com.aspose.words/table/) | Ziyaret edilen nesne. |

**Returns:**
int - Sayımın nasıl devam edeceğini belirten bir [VisitorAction](../../com.aspose.words/visitoraction/) değeri. Döndürülen değer, [VisitorAction](../../com.aspose.words/visitoraction/) sabitlerinden biridir.
### visitTableStart(Table table) {#visitTableStart-com.aspose.words.Table}
```
public int visitTableStart(Table table)
```


Tablonun sayımı başladığında çağrılır.

 **Examples:** 

Bir belgedeki her tablonun düğüm yapısını nasıl yazdıracağınızı gösterir.

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
| Parametre | Tür | Açıklama |
| --- | --- | --- |
| table | [Table](../../com.aspose.words/table/) | Ziyaret edilen nesne. |

**Returns:**
int - Sayımın nasıl devam edeceğini belirten bir [VisitorAction](../../com.aspose.words/visitoraction/) değeri. Döndürülen değer, [VisitorAction](../../com.aspose.words/visitoraction/) sabitlerinden biridir.
