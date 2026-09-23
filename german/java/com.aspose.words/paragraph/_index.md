---
title: "Paragraph"
linktitle: "Paragraph"
second_title: "Aspose.Words für Java"
description: "Stellt einen Textabsatz in Java dar."
type: docs
weight: 522
url: /de/java/com.aspose.words/paragraph/
---

**Inheritance:**
java.lang.Object, [com.aspose.words.Node](../../com.aspose.words/node/), [com.aspose.words.CompositeNode](../../com.aspose.words/compositenode/)
```
public class Paragraph extends CompositeNode
```

Stellt einen Textabsatz dar.

Um mehr zu erfahren, besuchen Sie den [ Working with Paragraphs ][Working with Paragraphs] Dokumentationsartikel.

 **Remarks:** 

[Paragraph](../../com.aspose.words/paragraph/) is a block-level node and can be a child of classes derived from [Story](../../com.aspose.words/story/) or [InlineStory](../../com.aspose.words/inlinestory/).

[Paragraph](../../com.aspose.words/paragraph/) can contain any number of inline-level nodes and bookmarks.

Die vollständige Liste der Kindknoten, die innerhalb eines Absatzes auftreten können, besteht aus [BookmarkStart](../../com.aspose.words/bookmarkstart/), [BookmarkEnd](../../com.aspose.words/bookmarkend/), [FieldStart](../../com.aspose.words/fieldstart/), [FieldSeparator](../../com.aspose.words/fieldseparator/), [FieldEnd](../../com.aspose.words/fieldend/), [FormField](../../com.aspose.words/formfield/), [Comment](../../com.aspose.words/comment/), [Footnote](../../com.aspose.words/footnote/), [Run](../../com.aspose.words/run/), [SpecialChar](../../com.aspose.words/specialchar/), [Shape](../../com.aspose.words/shape/), [GroupShape](../../com.aspose.words/groupshape/), [SmartTag](../../com.aspose.words/smarttag/).

Ein gültiger Absatz in Microsoft Word endet immer mit einem Absatzumbruchzeichen und ein minimal gültiger Absatz besteht nur aus einem Absatzumbruch. Die [Paragraph](../../com.aspose.words/paragraph/) Klasse fügt automatisch das passende Absatzumbruchzeichen am Ende hinzu und dieses Zeichen ist kein Teil der Kindknoten der [Paragraph](../../com.aspose.words/paragraph/), daher kann ein [Paragraph](../../com.aspose.words/paragraph/) leer sein.

Schließen Sie das Zeichen für das Absatzende [ControlChar.PARAGRAPH\_BREAK](../../com.aspose.words/controlchar/\#PARAGRAPH-BREAK) oder das Zeichen für das Zellenende [ControlChar.CELL](../../com.aspose.words/controlchar/\#CELL) nicht im Text des Absatzes ein, da es den Absatz ungültig machen kann, wenn das Dokument in Microsoft Word geöffnet wird.

 **Examples:** 

Zeigt, wie man ein Aspose.Words-Dokument von Hand erstellt.

```

 Document doc = new Document();

 // A blank document contains one section, one body and one paragraph.
 // Call the "RemoveAllChildren" method to remove all those nodes,
 // and end up with a document node with no children.
 doc.removeAllChildren();

 // This document now has no composite child nodes that we can add content to.
 // If we wish to edit it, we will need to repopulate its node collection.
 // First, create a new section, and then append it as a child to the root document node.
 Section section = new Section(doc);
 doc.appendChild(section);

 // Set some page setup properties for the section.
 section.getPageSetup().setSectionStart(SectionStart.NEW_PAGE);
 section.getPageSetup().setPaperSize(PaperSize.LETTER);

 // A section needs a body, which will contain and display all its contents
 // on the page between the section's header and footer.
 Body body = new Body(doc);
 section.appendChild(body);

 // Create a paragraph, set some formatting properties, and then append it as a child to the body.
 Paragraph para = new Paragraph(doc);

 para.getParagraphFormat().setStyleName("Heading 1");
 para.getParagraphFormat().setAlignment(ParagraphAlignment.CENTER);

 body.appendChild(para);

 // Finally, add some content to do the document. Create a run,
 // set its appearance and contents, and then append it as a child to the paragraph.
 Run run = new Run(doc);
 run.setText("Hello World!");
 run.getFont().setColor(Color.RED);
 para.appendChild(run);

 Assert.assertEquals("Hello World!", doc.getText().trim());

 doc.save(getArtifactsDir() + "Section.CreateManually.docx");
 
```


[Working with Paragraphs]: https://docs.aspose.com/words/java/working-with-paragraphs/
## Konstruktoren

| Konstruktor | Beschreibung |
| --- | --- |
| [Paragraph(DocumentBase doc)](#Paragraph-com.aspose.words.DocumentBase) | Initialisiert eine neue Instanz der [Paragraph](../../com.aspose.words/paragraph/) Klasse. |
## Methoden

| Methode | Beschreibung |
| --- | --- |
| [accept(DocumentVisitor visitor)](#accept-com.aspose.words.DocumentVisitor) | Akzeptiert einen Besucher. |
| [acceptEnd(DocumentVisitor visitor)](#acceptEnd-com.aspose.words.DocumentVisitor) | Akzeptiert einen Besucher, um das Ende des Absatzes des Dokuments zu besuchen. |
| [acceptStart(DocumentVisitor visitor)](#acceptStart-com.aspose.words.DocumentVisitor) | Akzeptiert einen Besucher, um den Anfang des Absatzes des Dokuments zu besuchen. |
| [appendChild(Node newChild)](#appendChild-com.aspose.words.Node) | Fügt den angegebenen Knoten am Ende der Liste von Kindknoten dieses Knotens hinzu. |
| [appendField(int fieldType, boolean updateField)](#appendField-int-boolean) |  |
| [appendField(String fieldCode)](#appendField-java.lang.String) | Fügt diesem Absatz ein Feld hinzu. |
| [appendField(String fieldCode, String fieldValue)](#appendField-java.lang.String-java.lang.String) | Fügt diesem Absatz ein Feld hinzu. |
| [clearParaAttrs()](#clearParaAttrs) |  |
| [clearRunAttrs()](#clearRunAttrs) |  |
| [deepClone(boolean isCloneChildren)](#deepClone-boolean) | Erstellt ein Duplikat des Knotens. |
| [fetchInheritedParaAttr(int key)](#fetchInheritedParaAttr-int) |  |
| [fetchInheritedRunAttr(int key)](#fetchInheritedRunAttr-int) |  |
| [fetchParaAttr(int key)](#fetchParaAttr-int) |  |
| [getAncestor(int ancestorType)](#getAncestor-int) |  |
| [getAncestor(Class ancestorType)](#getAncestor-java.lang.Class) | Ermittelt den ersten Vorfahren des angegebenen Objekttyps. |
| [getBreakIsStyleSeparator()](#getBreakIsStyleSeparator) | True, wenn dieser Absatzumbruch ein Stiltrennzeichen ist. |
| [getChild(int nodeType, int index, boolean isDeep)](#getChild-int-int-boolean) |  |
| [getChildNodes(int nodeType, boolean isDeep)](#getChildNodes-int-boolean) |  |
| [getContainer()](#getContainer) |  |
| [getCount()](#getCount) | Ermittelt die Anzahl der unmittelbaren Kindknoten dieses Knotens. |
| [getCurrentNode()](#getCurrentNode) |  |
| [getCustomNodeId()](#getCustomNodeId) | Gibt eine benutzerdefinierte Knotenkennung an. |
| [getDirectParaAttr(int key)](#getDirectParaAttr-int) |  |
| [getDirectParaAttr(int key, int revisionsView)](#getDirectParaAttr-int-int) |  |
| [getDirectRunAttr(int key)](#getDirectRunAttr-int) |  |
| [getDirectRunAttr(int key, int revisionsView)](#getDirectRunAttr-int-int) |  |
| [getDocument()](#getDocument) | Ermittelt das Dokument, zu dem dieser Knoten gehört. |
| [getEffectiveTabStops()](#getEffectiveTabStops) | Gibt ein Array aller Tabstopps zurück, die auf diesen Absatz angewendet wurden, einschließlich der indirekt durch Stile oder Listen angewendeten. |
| [getFirstChild()](#getFirstChild) | Ermittelt das erste Kind des Knotens. |
| [getFrameFormat()](#getFrameFormat) | Stellt Zugriff auf die Rahmenformatierungseigenschaften bereit. |
| [getLastChild()](#getLastChild) | Ermittelt das letzte Kind des Knotens. |
| [getListFormat()](#getListFormat) | Stellt Zugriff auf die Listformatierungseigenschaften des Absatzes bereit. |
| [getListLabel()](#getListLabel) | Liefert ein [getListLabel()](../../com.aspose.words/paragraph/\#getListLabel)-Objekt, das Zugriff auf den Listennummerierungswert und die Formatierung für diesen Absatz bietet. |
| [getNextMatchingNode(Node curNode)](#getNextMatchingNode-com.aspose.words.Node) |  |
| [getNextSibling()](#getNextSibling) | Ermittelt den Knoten, der unmittelbar auf diesen Knoten folgt. |
| [getNodeType()](#getNodeType) | Gibt [NodeType.PARAGRAPH](../../com.aspose.words/nodetype/\#PARAGRAPH) zurück. |
| [getParagraphBreakFont()](#getParagraphBreakFont) | Stellt Zugriff auf die Schriftformatierung des Absatzumbruchzeichens bereit. |
| [getParagraphFormat()](#getParagraphFormat) | Stellt Zugriff auf die Absatzformatierungseigenschaften bereit. |
| [getParentNode()](#getParentNode) | Ermittelt den unmittelbaren übergeordneten Knoten dieses Knotens. |
| [getParentSection()](#getParentSection) | Ruft die übergeordnete [Section](../../com.aspose.words/section/) des Absatzes ab. |
| [getParentStory()](#getParentStory) | Ruft die übergeordnete Story auf Abschnittsebene ab, die entweder [Body](../../com.aspose.words/body/) oder [HeaderFooter](../../com.aspose.words/headerfooter/) sein kann. |
| [getPreviousSibling()](#getPreviousSibling) | Ermittelt den Knoten, der unmittelbar vor diesem Knoten liegt. |
| [getRange()](#getRange) | Gibt ein [Range](../../com.aspose.words/range/)-Objekt zurück, das den Teil eines Dokuments darstellt, der in diesem Knoten enthalten ist. |
| [getRuns()](#getRuns) | Stellt Zugriff auf die typisierte Sammlung von Textstücken innerhalb des Absatzes bereit. |
| [getText()](#getText) | Liefert den Text dieses Absatzes einschließlich des Absatzendezeichens. |
| [hasChildNodes()](#hasChildNodes) | Gibt  true  zurück, wenn dieser Knoten Kindknoten hat. |
| [indexOf(Node child)](#indexOf-com.aspose.words.Node) | Gibt den Index des angegebenen Kindknotens im Kindknoten-Array zurück. |
| [insertAfter(Node newChild, Node refChild)](#insertAfter-com.aspose.words.Node-com.aspose.words.Node) | Fügt den angegebenen Knoten unmittelbar nach dem angegebenen Referenzknoten ein. |
| [insertBefore(Node newChild, Node refChild)](#insertBefore-com.aspose.words.Node-com.aspose.words.Node) | Fügt den angegebenen Knoten unmittelbar vor dem angegebenen Referenzknoten ein. |
| [insertField(int fieldType, boolean updateField, Node refNode, boolean isAfter)](#insertField-int-boolean-com.aspose.words.Node-boolean) |  |
| [insertField(String fieldCode, Node refNode, boolean isAfter)](#insertField-java.lang.String-com.aspose.words.Node-boolean) | Fügt ein Feld in diesen Absatz ein. |
| [insertField(String fieldCode, String fieldValue, Node refNode, boolean isAfter)](#insertField-java.lang.String-java.lang.String-com.aspose.words.Node-boolean) | Fügt ein Feld in diesen Absatz ein. |
| [isComposite()](#isComposite) | Gibt  true  zurück, da dieser Knoten Kindknoten haben kann. |
| [isDeleteRevision()](#isDeleteRevision) | Gibt true zurück, wenn dieses Objekt in Microsoft Word gelöscht wurde, während die Änderungsverfolgung aktiviert war. |
| [isEndOfCell()](#isEndOfCell) | True, wenn dieser Absatz der letzte Absatz in einer [Cell](../../com.aspose.words/cell/) ist; andernfalls false. |
| [isEndOfDocument()](#isEndOfDocument) | True, wenn dieser Absatz der letzte Absatz im letzten Abschnitt des Dokuments ist. |
| [isEndOfHeaderFooter()](#isEndOfHeaderFooter) | True, wenn dieser Absatz der letzte Absatz im [HeaderFooter](../../com.aspose.words/headerfooter/) (Haupttext-Story) einer [Section](../../com.aspose.words/section/) ist; andernfalls false. |
| [isEndOfSection()](#isEndOfSection) | True, wenn dieser Absatz der letzte Absatz im [Body](../../com.aspose.words/body/) (Haupttext-Story) einer [Section](../../com.aspose.words/section/) ist; andernfalls false. |
| [isFormatRevision()](#isFormatRevision) | Gibt true zurück, wenn die Formatierung des Objekts in Microsoft Word geändert wurde, während die Änderungsverfolgung aktiviert war. |
| [isInCell()](#isInCell) | True, wenn dieser Absatz ein unmittelbares Kind einer [Cell](../../com.aspose.words/cell/) ist; andernfalls false. |
| [isInsertRevision()](#isInsertRevision) | Gibt true zurück, wenn dieses Objekt in Microsoft Word eingefügt wurde, während die Änderungsverfolgung aktiviert war. |
| [isListItem()](#isListItem) | True, wenn der Absatz ein Element in einer Aufzählungs- oder nummerierten Liste in der Originalrevision ist. |
| [isMoveFromRevision()](#isMoveFromRevision) | Gibt  true  zurück, wenn dieses Objekt in Microsoft Word verschoben (gelöscht) wurde, während die Änderungsverfolgung aktiviert war. |
| [isMoveToRevision()](#isMoveToRevision) | Gibt  true  zurück, wenn dieses Objekt in Microsoft Word verschoben (eingefügt) wurde, während die Änderungsverfolgung aktiviert war. |
| [iterator()](#iterator) | Bietet Unterstützung für die foreach‑artige Iteration über die Kindknoten dieses Knotens. |
| [joinRunsWithSameFormatting()](#joinRunsWithSameFormatting) | Verbindet Laufabschnitte mit derselben Formatierung im Absatz. |
| [joinRunsWithSameFormatting(JoinRunsOptions options)](#joinRunsWithSameFormatting-com.aspose.words.JoinRunsOptions) | Verbindet Laufabschnitte mit derselben Formatierung im Absatz. |
| [nextPreOrder(Node rootNode)](#nextPreOrder-com.aspose.words.Node) | Ermittelt den nächsten Knoten gemäß dem Preorder-Baumdurchlauf-Algorithmus. |
| [nodeTypeToString(int nodeType)](#nodeTypeToString-int) |  |
| [prependChild(Node newChild)](#prependChild-com.aspose.words.Node) | Fügt den angegebenen Knoten am Anfang der Liste der Kindknoten dieses Knotens hinzu. |
| [previousPreOrder(Node rootNode)](#previousPreOrder-com.aspose.words.Node) | Ermittelt den vorherigen Knoten gemäß dem Preorder-Baumdurchlauf-Algorithmus. |
| [remove()](#remove) | Entfernt sich selbst vom übergeordneten Element. |
| [removeAllChildren()](#removeAllChildren) | Entfernt alle Kindknoten des aktuellen Knotens. |
| [removeChild(Node oldChild)](#removeChild-com.aspose.words.Node) | Entfernt den angegebenen Kindknoten. |
| [removeMoveRevisions()](#removeMoveRevisions) |  |
| [removeParaAttr(int key)](#removeParaAttr-int) |  |
| [removeRunAttr(int key)](#removeRunAttr-int) |  |
| [removeSmartTags()](#removeSmartTags) | Entfernt alle [SmartTag](../../com.aspose.words/smarttag/) Nachfahrenknoten des aktuellen Knotens. |
| [selectNodes(String xpath)](#selectNodes-java.lang.String) | Wählt eine Liste von Knoten aus, die dem XPath-Ausdruck entsprechen. |
| [selectSingleNode(String xpath)](#selectSingleNode-java.lang.String) | Wählt den ersten [Node](../../com.aspose.words/node/) aus, der dem XPath-Ausdruck entspricht. |
| [setCustomNodeId(int value)](#setCustomNodeId-int) | Gibt eine benutzerdefinierte Knotenkennung an. |
| [setParaAttr(int key, Object value)](#setParaAttr-int-java.lang.Object) |  |
| [setRunAttr(int key, Object value)](#setRunAttr-int-java.lang.Object) |  |
| [toString()](#toString) |  |
| [toString(SaveOptions saveOptions)](#toString-com.aspose.words.SaveOptions) | Exportiert den Inhalt des Knotens in einen String unter Verwendung der angegebenen Speicheroptionen. |
| [toString(int saveFormat)](#toString-int) |  |
### Paragraph(DocumentBase doc) {#Paragraph-com.aspose.words.DocumentBase}
```
public Paragraph(DocumentBase doc)
```


Initialisiert eine neue Instanz der [Paragraph](../../com.aspose.words/paragraph/) Klasse.

 **Remarks:** 

Wenn [Paragraph](../../com.aspose.words/paragraph/) erstellt wird, gehört es zum angegebenen Dokument, ist jedoch noch nicht Teil des Dokuments und [Node.getParentNode()](../../com.aspose.words/node/\#getParentNode) ist null.

Um [Paragraph](../../com.aspose.words/paragraph/) an das Dokument anzuhängen, verwenden Sie [CompositeNode.insertAfter(com.aspose.words.Node, com.aspose.words.Node)](../../com.aspose.words/compositenode/\#insertAfter-com.aspose.words.Node--com.aspose.words.Node) oder [CompositeNode.insertBefore(com.aspose.words.Node, com.aspose.words.Node)](../../com.aspose.words/compositenode/\#insertBefore-com.aspose.words.Node--com.aspose.words.Node) in der Story, in der Sie den Absatz einfügen möchten.

 **Examples:** 

Zeigt, wie man ein Aspose.Words-Dokument von Hand erstellt.

```

 Document doc = new Document();

 // A blank document contains one section, one body and one paragraph.
 // Call the "RemoveAllChildren" method to remove all those nodes,
 // and end up with a document node with no children.
 doc.removeAllChildren();

 // This document now has no composite child nodes that we can add content to.
 // If we wish to edit it, we will need to repopulate its node collection.
 // First, create a new section, and then append it as a child to the root document node.
 Section section = new Section(doc);
 doc.appendChild(section);

 // Set some page setup properties for the section.
 section.getPageSetup().setSectionStart(SectionStart.NEW_PAGE);
 section.getPageSetup().setPaperSize(PaperSize.LETTER);

 // A section needs a body, which will contain and display all its contents
 // on the page between the section's header and footer.
 Body body = new Body(doc);
 section.appendChild(body);

 // Create a paragraph, set some formatting properties, and then append it as a child to the body.
 Paragraph para = new Paragraph(doc);

 para.getParagraphFormat().setStyleName("Heading 1");
 para.getParagraphFormat().setAlignment(ParagraphAlignment.CENTER);

 body.appendChild(para);

 // Finally, add some content to do the document. Create a run,
 // set its appearance and contents, and then append it as a child to the paragraph.
 Run run = new Run(doc);
 run.setText("Hello World!");
 run.getFont().setColor(Color.RED);
 para.appendChild(run);

 Assert.assertEquals("Hello World!", doc.getText().trim());

 doc.save(getArtifactsDir() + "Section.CreateManually.docx");
 
```

**Parameters:**
| Parameter | Typ | Beschreibung |
| --- | --- | --- |
| doc | [DocumentBase](../../com.aspose.words/documentbase/) | Das übergeordnete Dokument. |

### accept(DocumentVisitor visitor) {#accept-com.aspose.words.DocumentVisitor}
```
public boolean accept(DocumentVisitor visitor)
```


Akzeptiert einen Besucher.

 **Remarks:** 

Enumeriert diesen Knoten und alle seine Kinder. Jeder Knoten ruft die entsprechende Methode auf [DocumentVisitor](../../com.aspose.words/documentvisitor/).

Weitere Informationen finden Sie im Visitor-Entwurfsmuster.

Ruft [DocumentVisitor.visitParagraphStart(com.aspose.words.Paragraph)](../../com.aspose.words/documentvisitor/\#visitParagraphStart-com.aspose.words.Paragraph) auf, ruft dann [Node.accept(com.aspose.words.DocumentVisitor)](../../com.aspose.words/node/\#accept-com.aspose.words.DocumentVisitor) für alle Kindknoten des Absatzes auf und ruft am Ende [DocumentVisitor.visitParagraphEnd(com.aspose.words.Paragraph)](../../com.aspose.words/documentvisitor/\#visitParagraphEnd-com.aspose.words.Paragraph) auf.

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
| visitor | [DocumentVisitor](../../com.aspose.words/documentvisitor/) | Der Visitor, der die Knoten besuchen wird. |

**Returns:**
boolean - True, wenn alle Knoten besucht wurden; false, wenn [DocumentVisitor](../../com.aspose.words/documentvisitor/) die Operation beendet hat, bevor alle Knoten besucht wurden.
### acceptEnd(DocumentVisitor visitor) {#acceptEnd-com.aspose.words.DocumentVisitor}
```
public int acceptEnd(DocumentVisitor visitor)
```


Akzeptiert einen Besucher, um das Ende des Absatzes des Dokuments zu besuchen.

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
| visitor | [DocumentVisitor](../../com.aspose.words/documentvisitor/) | Der Dokumentbesucher. |

**Returns:**
int - Die vom Besucher auszuführende Aktion. Der zurückgegebene Wert ist einer der Konstanten von [VisitorAction](../../com.aspose.words/visitoraction/).
### acceptStart(DocumentVisitor visitor) {#acceptStart-com.aspose.words.DocumentVisitor}
```
public int acceptStart(DocumentVisitor visitor)
```


Akzeptiert einen Besucher, um den Anfang des Absatzes des Dokuments zu besuchen.

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
| visitor | [DocumentVisitor](../../com.aspose.words/documentvisitor/) | Der Dokumentbesucher. |

**Returns:**
int - Die vom Besucher auszuführende Aktion. Der zurückgegebene Wert ist einer der Konstanten von [VisitorAction](../../com.aspose.words/visitoraction/).
### appendChild(Node newChild) {#appendChild-com.aspose.words.Node}
```
public Node appendChild(Node newChild)
```


Fügt den angegebenen Knoten am Ende der Liste von Kindknoten dieses Knotens hinzu.

 **Remarks:** 

Wenn der  newChild  bereits im Baum ist, wird er zuerst entfernt.

Wenn der einzufügende Knoten aus einem anderen Dokument erstellt wurde, sollten Sie **M:Aspose.Words.DocumentBase.ImportNode(Aspose.Words.Node,System.Boolean,Aspose.Words.ImportFormatMode)** verwenden, um den Knoten in das aktuelle Dokument zu importieren. Der importierte Knoten kann dann in das aktuelle Dokument eingefügt werden.

 **Examples:** 

Zeigt, wie man ein Aspose.Words-Dokument von Hand erstellt.

```

 Document doc = new Document();

 // A blank document contains one section, one body and one paragraph.
 // Call the "RemoveAllChildren" method to remove all those nodes,
 // and end up with a document node with no children.
 doc.removeAllChildren();

 // This document now has no composite child nodes that we can add content to.
 // If we wish to edit it, we will need to repopulate its node collection.
 // First, create a new section, and then append it as a child to the root document node.
 Section section = new Section(doc);
 doc.appendChild(section);

 // Set some page setup properties for the section.
 section.getPageSetup().setSectionStart(SectionStart.NEW_PAGE);
 section.getPageSetup().setPaperSize(PaperSize.LETTER);

 // A section needs a body, which will contain and display all its contents
 // on the page between the section's header and footer.
 Body body = new Body(doc);
 section.appendChild(body);

 // Create a paragraph, set some formatting properties, and then append it as a child to the body.
 Paragraph para = new Paragraph(doc);

 para.getParagraphFormat().setStyleName("Heading 1");
 para.getParagraphFormat().setAlignment(ParagraphAlignment.CENTER);

 body.appendChild(para);

 // Finally, add some content to do the document. Create a run,
 // set its appearance and contents, and then append it as a child to the paragraph.
 Run run = new Run(doc);
 run.setText("Hello World!");
 run.getFont().setColor(Color.RED);
 para.appendChild(run);

 Assert.assertEquals("Hello World!", doc.getText().trim());

 doc.save(getArtifactsDir() + "Section.CreateManually.docx");
 
```

**Parameters:**
| Parameter | Typ | Beschreibung |
| --- | --- | --- |
| newChild | [Node](../../com.aspose.words/node/) | Der hinzuzufügende Knoten. |

**Returns:**
[Node](../../com.aspose.words/node/) - The node added.
### appendField(int fieldType, boolean updateField) {#appendField-int-boolean}
```
public Field appendField(int fieldType, boolean updateField)
```




**Parameters:**
| Parameter | Typ | Beschreibung |
| --- | --- | --- |
| fieldType | int |  |
| updateField | boolean |  |

**Returns:**
[Field](../../com.aspose.words/field/)
### appendField(String fieldCode) {#appendField-java.lang.String}
```
public Field appendField(String fieldCode)
```


Fügt diesem Absatz ein Feld hinzu.

 **Examples:** 

Zeigt verschiedene Möglichkeiten, Felder an einen Absatz anzuhängen.

```

 Document doc = new Document();
 Paragraph paragraph = doc.getFirstSection().getBody().getFirstParagraph();

 // Below are three ways of appending a field to the end of a paragraph.
 // 1 -  Append a DATE field using a field type, and then update it:
 paragraph.appendField(FieldType.FIELD_DATE, true);

 // 2 -  Append a TIME field using a field code:
 paragraph.appendField(" TIME  \\@ \"HH:mm:ss\" ");

 // 3 -  Append a QUOTE field using a field code, and get it to display a placeholder value:
 paragraph.appendField(" QUOTE \"Real value\"", "Placeholder value");

 Assert.assertEquals("Placeholder value", doc.getRange().getFields().get(2).getResult());

 // This field will display its placeholder value until we update it.
 doc.updateFields();

 Assert.assertEquals("Real value", doc.getRange().getFields().get(2).getResult());

 doc.save(getArtifactsDir() + "Paragraph.AppendField.docx");
 
```

**Parameters:**
| Parameter | Typ | Beschreibung |
| --- | --- | --- |
| fieldCode | java.lang.String | Der Feldcode, der angehängt werden soll (ohne geschweifte Klammern). |

**Returns:**
[Field](../../com.aspose.words/field/) - A [Field](../../com.aspose.words/field/) object that represents the appended field.
### appendField(String fieldCode, String fieldValue) {#appendField-java.lang.String-java.lang.String}
```
public Field appendField(String fieldCode, String fieldValue)
```


Fügt diesem Absatz ein Feld hinzu.

 **Examples:** 

Zeigt verschiedene Möglichkeiten, Felder an einen Absatz anzuhängen.

```

 Document doc = new Document();
 Paragraph paragraph = doc.getFirstSection().getBody().getFirstParagraph();

 // Below are three ways of appending a field to the end of a paragraph.
 // 1 -  Append a DATE field using a field type, and then update it:
 paragraph.appendField(FieldType.FIELD_DATE, true);

 // 2 -  Append a TIME field using a field code:
 paragraph.appendField(" TIME  \\@ \"HH:mm:ss\" ");

 // 3 -  Append a QUOTE field using a field code, and get it to display a placeholder value:
 paragraph.appendField(" QUOTE \"Real value\"", "Placeholder value");

 Assert.assertEquals("Placeholder value", doc.getRange().getFields().get(2).getResult());

 // This field will display its placeholder value until we update it.
 doc.updateFields();

 Assert.assertEquals("Real value", doc.getRange().getFields().get(2).getResult());

 doc.save(getArtifactsDir() + "Paragraph.AppendField.docx");
 
```

**Parameters:**
| Parameter | Typ | Beschreibung |
| --- | --- | --- |
| fieldCode | java.lang.String | Der Feldcode, der angehängt werden soll (ohne geschweifte Klammern). |
| fieldValue | java.lang.String | Der Feldwert, der angehängt werden soll. Übergeben Sie  null  für Felder, die keinen Wert haben. |

**Returns:**
[Field](../../com.aspose.words/field/) - A [Field](../../com.aspose.words/field/) object that represents the appended field.
### clearParaAttrs() {#clearParaAttrs}
```
public void clearParaAttrs()
```




### clearRunAttrs() {#clearRunAttrs}
```
public void clearRunAttrs()
```




### deepClone(boolean isCloneChildren) {#deepClone-boolean}
```
public Node deepClone(boolean isCloneChildren)
```


Erstellt ein Duplikat des Knotens.

 **Remarks:** 

Diese Methode dient als Kopierkonstruktor für Knoten. Der geklonte Knoten hat keinen übergeordneten Knoten, gehört jedoch zum selben Dokument wie der ursprüngliche Knoten.

Diese Methode führt immer eine tiefe Kopie des Knotens aus. Der Parameter isCloneChildren gibt an, ob ebenfalls alle Kindknoten kopiert werden sollen.

 **Examples:** 

Zeigt, wie ein zusammengesetzter Knoten geklont wird.

```

 Document doc = new Document();
 Paragraph para = doc.getFirstSection().getBody().getFirstParagraph();
 para.appendChild(new Run(doc, "Hello world!"));

 // Below are two ways of cloning a composite node.
 // 1 -  Create a clone of a node, and create a clone of each of its child nodes as well.
 Node cloneWithChildren = para.deepClone(true);

 Assert.assertTrue(((CompositeNode) cloneWithChildren).hasChildNodes());
 Assert.assertEquals("Hello world!", cloneWithChildren.getText().trim());

 // 2 -  Create a clone of a node just by itself without any children.
 Node cloneWithoutChildren = para.deepClone(false);

 Assert.assertFalse(((CompositeNode) cloneWithoutChildren).hasChildNodes());
 Assert.assertEquals("", cloneWithoutChildren.getText().trim());
 
```

**Parameters:**
| Parameter | Typ | Beschreibung |
| --- | --- | --- |
| isCloneChildren | boolean | True, um den Unterbaum unter dem angegebenen Knoten rekursiv zu klonen; false, um nur den Knoten selbst zu klonen. |

**Returns:**
[Node](../../com.aspose.words/node/) - The cloned node.
### fetchInheritedParaAttr(int key) {#fetchInheritedParaAttr-int}
```
public Object fetchInheritedParaAttr(int key)
```




**Parameters:**
| Parameter | Typ | Beschreibung |
| --- | --- | --- |
| key | int |  |

**Returns:**
java.lang.Object
### fetchInheritedRunAttr(int key) {#fetchInheritedRunAttr-int}
```
public Object fetchInheritedRunAttr(int key)
```




**Parameters:**
| Parameter | Typ | Beschreibung |
| --- | --- | --- |
| key | int |  |

**Returns:**
java.lang.Object
### fetchParaAttr(int key) {#fetchParaAttr-int}
```
public Object fetchParaAttr(int key)
```




**Parameters:**
| Parameter | Typ | Beschreibung |
| --- | --- | --- |
| key | int |  |

**Returns:**
java.lang.Object
### getAncestor(int ancestorType) {#getAncestor-int}
```
public CompositeNode getAncestor(int ancestorType)
```




**Parameters:**
| Parameter | Typ | Beschreibung |
| --- | --- | --- |
| ancestorType | int |  |

**Returns:**
[CompositeNode](../../com.aspose.words/compositenode/)
### getAncestor(Class ancestorType) {#getAncestor-java.lang.Class}
```
public CompositeNode getAncestor(Class ancestorType)
```


Ermittelt den ersten Vorfahren des angegebenen Objekttyps.

 **Remarks:** 

Der Ancestor-Typ stimmt überein, wenn er gleich ancestorType ist oder von ancestorType abgeleitet ist.

 **Examples:** 

Zeigt, wie man herausfindet, ob Tabellen verschachtelt sind.

```

 public void calculateDepthOfNestedTables() throws Exception {
     Document doc = new Document(getMyDir() + "Nested tables.docx");
     NodeCollection tables = doc.getChildNodes(NodeType.TABLE, true);
     for (int i = 0; i < tables.getCount(); i++) {
         Table table = (Table) tables.get(i);

         // Find out if any cells in the table have other tables as children.
         int count = getChildTableCount(table);
         System.out.print(MessageFormat.format("Table #{0} has {1} tables directly within its cells", i, count));

         // Find out if the table is nested inside another table, and, if so, at what depth.
         int tableDepth = getNestedDepthOfTable(table);

         if (tableDepth > 0)
             System.out.println(MessageFormat.format("Table #{0} is nested inside another table at depth of {1}", i, tableDepth));
         else
             System.out.println(MessageFormat.format("Table #{0} is a non nested table (is not a child of another table)", i));
     }
 }

 // Calculates what level a table is nested inside other tables.
 //
 // Returns An integer containing the level the table is nested at.
 // 0 = Table is not nested inside any other table
 // 1 = Table is nested within one parent table
 // 2 = Table is nested within two parent tables etc..
 private static int getNestedDepthOfTable(final Table table) {
     int depth = 0;
     Node parent = table.getAncestor(table.getNodeType());

     while (parent != null) {
         depth++;
         parent = parent.getAncestor(Table.class);
     }

     return depth;
 }

 // Determines if a table contains any immediate child table within its cells.
 // Does not recursively traverse through those tables to check for further tables.
 //
 // Returns true if at least one child cell contains a table.
 // Returns false if no cells in the table contains a table.
 private static int getChildTableCount(final Table table) {
     int childTableCount = 0;

     for (Row row : table.getRows()) {
         for (Cell cell : row.getCells()) {
             TableCollection childTables = cell.getTables();

             if (childTables.getCount() > 0) childTableCount++;
         }
     }

     return childTableCount;
 }
 
```

**Parameters:**
| Parameter | Typ | Beschreibung |
| --- | --- | --- |
| ancestorType | java.lang.Class | Der Objekttyp des abzurufenden Ancestors. |

**Returns:**
[CompositeNode](../../com.aspose.words/compositenode/) - The ancestor of the specified type or  null  if no ancestor of this type was found.
### getBreakIsStyleSeparator() {#getBreakIsStyleSeparator}
```
public boolean getBreakIsStyleSeparator()
```


True, wenn dieser Absatzumbruch ein Stiltrennzeichen ist. Ein Stiltrennzeichen ermöglicht, dass ein Absatz aus Teilen besteht, die unterschiedliche Absatzformate haben.

 **Examples:** 

Zeigt, wie man Text in dieselbe Zeile wie eine Inhaltsverzeichnis‑Überschrift schreibt und ihn nicht im Inhaltsverzeichnis erscheinen lässt.

```

 Document doc = new Document();
 DocumentBuilder builder = new DocumentBuilder(doc);

 builder.insertTableOfContents("\\o \\h \\z \\u");
 builder.insertBreak(BreakType.PAGE_BREAK);

 // Insert a paragraph with a style that the TOC will pick up as an entry.
 builder.getParagraphFormat().setStyleIdentifier(StyleIdentifier.HEADING_1);

 // Both these strings are in the same paragraph and will therefore show up on the same TOC entry.
 builder.write("Heading 1. ");
 builder.write("Will appear in the TOC. ");

 // If we insert a style separator, we can write more text in the same paragraph
 // and use a different style without showing up in the TOC.
 // If we use a heading type style after the separator, we can draw multiple TOC entries from one document text line.
 builder.insertStyleSeparator();
 builder.getParagraphFormat().setStyleIdentifier(StyleIdentifier.QUOTE);
 builder.write("Won't appear in the TOC. ");

 Assert.assertTrue(doc.getFirstSection().getBody().getParagraphs().get(0).getBreakIsStyleSeparator());

 doc.updateFields();
 doc.save(getArtifactsDir() + "Paragraph.BreakIsStyleSeparator.docx");
 
```

**Returns:**
boolean - Der entsprechende  boolean  Wert.
### getChild(int nodeType, int index, boolean isDeep) {#getChild-int-int-boolean}
```
public Node getChild(int nodeType, int index, boolean isDeep)
```




**Parameters:**
| Parameter | Typ | Beschreibung |
| --- | --- | --- |
| nodeType | int |  |
| Index | int |  |
| isDeep | boolean |  |

**Returns:**
[Node](../../com.aspose.words/node/)
### getChildNodes(int nodeType, boolean isDeep) {#getChildNodes-int-boolean}
```
public NodeCollection getChildNodes(int nodeType, boolean isDeep)
```




**Parameters:**
| Parameter | Typ | Beschreibung |
| --- | --- | --- |
| nodeType | int |  |
| isDeep | boolean |  |

**Returns:**
[NodeCollection](../../com.aspose.words/nodecollection/)
### getContainer() {#getContainer}
```
public CompositeNode getContainer()
```




**Returns:**
[CompositeNode](../../com.aspose.words/compositenode/)
### getCount() {#getCount}
```
public int getCount()
```


Ermittelt die Anzahl der unmittelbaren Kindknoten dieses Knotens.

 **Examples:** 

Zeigt, wie man Kindknoten in der Sammlung von Kindknoten eines CompositeNode hinzufügt, aktualisiert und löscht.

```

 Document doc = new Document();

 // An empty document, by default, has one paragraph.
 Assert.assertEquals(1, doc.getFirstSection().getBody().getParagraphs().getCount());

 // Composite nodes such as our paragraph can contain other composite and inline nodes as children.
 Paragraph paragraph = doc.getFirstSection().getBody().getFirstParagraph();
 Run paragraphText = new Run(doc, "Initial text. ");
 paragraph.appendChild(paragraphText);

 // Create three more run nodes.
 Run run1 = new Run(doc, "Run 1. ");
 Run run2 = new Run(doc, "Run 2. ");
 Run run3 = new Run(doc, "Run 3. ");

 // The document body will not display these runs until we insert them into a composite node
 // that itself is a part of the document's node tree, as we did with the first run.
 // We can determine where the text contents of nodes that we insert
 // appears in the document by specifying an insertion location relative to another node in the paragraph.
 Assert.assertEquals("Initial text.", paragraph.getText().trim());

 // Insert the second run into the paragraph in front of the initial run.
 paragraph.insertBefore(run2, paragraphText);

 Assert.assertEquals("Run 2. Initial text.", paragraph.getText().trim());

 // Insert the third run after the initial run.
 paragraph.insertAfter(run3, paragraphText);

 Assert.assertEquals("Run 2. Initial text. Run 3.", paragraph.getText().trim());

 // Insert the first run to the start of the paragraph's child nodes collection.
 paragraph.prependChild(run1);

 Assert.assertEquals("Run 1. Run 2. Initial text. Run 3.", paragraph.getText().trim());
 Assert.assertEquals(4, paragraph.getChildNodes(NodeType.ANY, true).getCount());

 // We can modify the contents of the run by editing and deleting existing child nodes.
 ((Run) paragraph.getChildNodes(NodeType.RUN, true).get(1)).setText("Updated run 2. ");
 paragraph.getChildNodes(NodeType.RUN, true).remove(paragraphText);

 Assert.assertEquals("Run 1. Updated run 2. Run 3.", paragraph.getText().trim());
 Assert.assertEquals(3, paragraph.getChildNodes(NodeType.ANY, true).getCount());
 
```

**Returns:**
int - Die Anzahl der unmittelbaren Kindknoten dieses Knotens.
### getCurrentNode() {#getCurrentNode}
```
public Node getCurrentNode()
```




**Returns:**
[Node](../../com.aspose.words/node/)
### getCustomNodeId() {#getCustomNodeId}
```
public int getCustomNodeId()
```


Gibt eine benutzerdefinierte Knotenkennung an.

 **Remarks:** 

Standardwert ist 0.

Dieser Bezeichner kann beliebig gesetzt und verwendet werden. Zum Beispiel als Schlüssel, um externe Daten abzurufen.

Wichtiger Hinweis: Der angegebene Wert wird nicht in einer Ausgabedatei gespeichert und existiert nur während der Lebensdauer des Knotens.

 **Examples:** 

Zeigt, wie man die Sammlung von Kindknoten eines zusammengesetzten Knotens durchläuft.

```

 Document doc = new Document();

 // Add two runs and one shape as child nodes to the first paragraph of this document.
 Paragraph paragraph = (Paragraph) doc.getChild(NodeType.PARAGRAPH, 0, true);
 paragraph.appendChild(new Run(doc, "Hello world! "));

 Shape shape = new Shape(doc, ShapeType.RECTANGLE);
 shape.setWidth(200.0);
 shape.setHeight(200.0);
 // Note that the 'CustomNodeId' is not saved to an output file and exists only during the node lifetime.
 shape.setCustomNodeId(100);
 shape.setWrapType(WrapType.INLINE);
 paragraph.appendChild(shape);

 paragraph.appendChild(new Run(doc, "Hello again!"));

 // Iterate through the paragraph's collection of immediate children,
 // and print any runs or shapes that we find within.
 NodeCollection children = paragraph.getChildNodes(NodeType.ANY, false);

 Assert.assertEquals(3, paragraph.getChildNodes(NodeType.ANY, false).getCount());

 for (Node child : (Iterable) children)
     switch (child.getNodeType()) {
         case NodeType.RUN:
             System.out.println("Run contents:");
             System.out.println(MessageFormat.format("\t\"{0}\"", child.getText().trim()));
             break;
         case NodeType.SHAPE:
             Shape childShape = (Shape)child;
             System.out.println("Shape:");
             System.out.println(MessageFormat.format("\t{0}, {1}x{2}", childShape.getShapeType(), childShape.getWidth(), childShape.getHeight()));
             break;
     }
 
```

**Returns:**
int - Der entsprechende int-Wert.
### getDirectParaAttr(int key) {#getDirectParaAttr-int}
```
public Object getDirectParaAttr(int key)
```




**Parameters:**
| Parameter | Typ | Beschreibung |
| --- | --- | --- |
| key | int |  |

**Returns:**
java.lang.Object
### getDirectParaAttr(int key, int revisionsView) {#getDirectParaAttr-int-int}
```
public Object getDirectParaAttr(int key, int revisionsView)
```




**Parameters:**
| Parameter | Typ | Beschreibung |
| --- | --- | --- |
| key | int |  |
| revisionsView | int |  |

**Returns:**
java.lang.Object
### getDirectRunAttr(int key) {#getDirectRunAttr-int}
```
public Object getDirectRunAttr(int key)
```




**Parameters:**
| Parameter | Typ | Beschreibung |
| --- | --- | --- |
| key | int |  |

**Returns:**
java.lang.Object
### getDirectRunAttr(int key, int revisionsView) {#getDirectRunAttr-int-int}
```
public Object getDirectRunAttr(int key, int revisionsView)
```




**Parameters:**
| Parameter | Typ | Beschreibung |
| --- | --- | --- |
| key | int |  |
| revisionsView | int |  |

**Returns:**
java.lang.Object
### getDocument() {#getDocument}
```
public DocumentBase getDocument()
```


Ermittelt das Dokument, zu dem dieser Knoten gehört.

 **Remarks:** 

Der Knoten gehört immer zu einem Dokument, selbst wenn er gerade erst erstellt wurde und noch nicht zum Baum hinzugefügt wurde oder wenn er aus dem Baum entfernt wurde.

 **Examples:** 

Zeigt, wie man einen Knoten erstellt und sein zugehöriges Dokument festlegt.

```

 Document doc = new Document();
 Paragraph para = new Paragraph(doc);
 para.appendChild(new Run(doc, "Hello world!"));

 // We have not yet appended this paragraph as a child to any composite node.
 Assert.assertNull(para.getParentNode());

 // If a node is an appropriate child node type of another composite node,
 // we can attach it as a child only if both nodes have the same owner document.
 // The owner document is the document we passed to the node's constructor.
 // We have not attached this paragraph to the document, so the document does not contain its text.
 Assert.assertEquals(para.getDocument(), doc);
 Assert.assertEquals("", doc.getText().trim());

 // Since the document owns this paragraph, we can apply one of its styles to the paragraph's contents.
 para.getParagraphFormat().setStyleName("Heading 1");

 // Add this node to the document, and then verify its contents.
 doc.getFirstSection().getBody().appendChild(para);

 Assert.assertEquals(doc.getFirstSection().getBody(), para.getParentNode());
 Assert.assertEquals("Hello world!", doc.getText().trim());
 
```

**Returns:**
[DocumentBase](../../com.aspose.words/documentbase/) - The document to which this node belongs.
### getEffectiveTabStops() {#getEffectiveTabStops}
```
public TabStop[] getEffectiveTabStops()
```


Gibt ein Array aller Tabstopps zurück, die auf diesen Absatz angewendet wurden, einschließlich der indirekt durch Stile oder Listen angewendeten.

 **Examples:** 

Zeigt, wie benutzerdefinierte Tabstopps für einen Absatz festgelegt werden.

```

 Document doc = new Document();
 Paragraph para = doc.getFirstSection().getBody().getFirstParagraph();

 // If we are in a paragraph with no tab stops in this collection,
 // the cursor will jump 36 points each time we press the Tab key in Microsoft Word.
 Assert.assertEquals(0, doc.getFirstSection().getBody().getFirstParagraph().getEffectiveTabStops().length);

 // We can add custom tab stops in Microsoft Word if we enable the ruler via the "View" tab.
 // Each unit on this ruler is two default tab stops, which is 72 points.
 // We can add custom tab stops programmatically like this.
 TabStopCollection tabStops = doc.getFirstSection().getBody().getFirstParagraph().getParagraphFormat().getTabStops();
 tabStops.add(72.0, TabAlignment.LEFT, TabLeader.DOTS);
 tabStops.add(216.0, TabAlignment.CENTER, TabLeader.DASHES);
 tabStops.add(360.0, TabAlignment.RIGHT, TabLeader.LINE);

 // We can see these tab stops in Microsoft Word by enabling the ruler via "View" -> "Show" -> "Ruler".
 Assert.assertEquals(3, para.getEffectiveTabStops().length);

 // Any tab characters we add will make use of the tab stops on the ruler and may,
 // depending on the tab leader's value, leave a line between the tab departure and arrival destinations.
 para.appendChild(new Run(doc, "\tTab 1\tTab 2\tTab 3"));

 doc.save(getArtifactsDir() + "Paragraph.TabStops.docx");
 
```

**Returns:**
com.aspose.words.TabStop[]
### getFirstChild() {#getFirstChild}
```
public Node getFirstChild()
```


Ermittelt das erste Kind des Knotens.

 **Remarks:** 

Wenn es keinen ersten Kindknoten gibt, wird ein  null  zurückgegeben.

 **Examples:** 

Zeigt, wie man den Baum von Kindknoten eines zusammengesetzten Knotens durchläuft.

```

 public void recurseChildren() throws Exception {
     Document doc = new Document(getMyDir() + "Paragraphs.docx");

     // Any node that can contain child nodes, such as the document itself, is composite.
     Assert.assertTrue(doc.isComposite());

     // Invoke the recursive function that will go through and print all the child nodes of a composite node.
     traverseAllNodes(doc, 0);
 }

 /// 
 /// Recursively traverses a node tree while printing the type of each node
 /// with an indent depending on depth as well as the contents of all inline nodes.
 /// 
 public void traverseAllNodes(CompositeNode parentNode, int depth) {
     for (Node childNode = parentNode.getFirstChild(); childNode != null; childNode = childNode.getNextSibling()) {
         System.out.println(MessageFormat.format("{0}{1}", String.format("    ", depth), Node.nodeTypeToString(childNode.getNodeType())));

         // Recurse into the node if it is a composite node. Otherwise, print its contents if it is an inline node.
         if (childNode.isComposite()) {
             System.out.println();
             traverseAllNodes((CompositeNode) childNode, depth + 1);
         } else if (childNode instanceof Inline) {
             System.out.println(MessageFormat.format(" - \"{0}\"", childNode.getText().trim()));
         } else {
             System.out.println();
         }
     }
 }
 
```

Zeigt, wie man die Eigenschaft NextSibling eines Knotens verwendet, um seine unmittelbaren Kinder zu enumerieren.

```

 Document doc = new Document(getMyDir() + "Paragraphs.docx");

 for (Node node = doc.getFirstSection().getBody().getFirstChild(); node != null; node = node.getNextSibling()) {
     System.out.println(Node.nodeTypeToString(node.getNodeType()));
 }
 
```

**Returns:**
[Node](../../com.aspose.words/node/) - The first child of the node.
### getFrameFormat() {#getFrameFormat}
```
public FrameFormat getFrameFormat()
```


Stellt Zugriff auf die Rahmenformatierungseigenschaften bereit.

 **Examples:** 

Zeigt, wie Informationen zu Formatierungseigenschaften von Absätzen, die Frames sind, abgerufen werden.

```

 Document doc = new Document(getMyDir() + "Paragraph frame.docx");

 Paragraph paragraphFrame = IterableUtils.find(doc.getFirstSection().getBody().getParagraphs(), p -> p.getFrameFormat().isFrame());

 Assert.assertEquals(233.3d, paragraphFrame.getFrameFormat().getWidth());
 Assert.assertEquals(138.8d, paragraphFrame.getFrameFormat().getHeight());
 Assert.assertEquals(HeightRule.AT_LEAST, paragraphFrame.getFrameFormat().getHeightRule());
 Assert.assertEquals(HorizontalAlignment.DEFAULT, paragraphFrame.getFrameFormat().getHorizontalAlignment());
 Assert.assertEquals(VerticalAlignment.DEFAULT, paragraphFrame.getFrameFormat().getVerticalAlignment());
 Assert.assertEquals(34.05d, paragraphFrame.getFrameFormat().getHorizontalPosition());
 Assert.assertEquals(RelativeHorizontalPosition.PAGE, paragraphFrame.getFrameFormat().getRelativeHorizontalPosition());
 Assert.assertEquals(9.0d, paragraphFrame.getFrameFormat().getHorizontalDistanceFromText());
 Assert.assertEquals(20.5d, paragraphFrame.getFrameFormat().getVerticalPosition());
 Assert.assertEquals(RelativeVerticalPosition.PARAGRAPH, paragraphFrame.getFrameFormat().getRelativeVerticalPosition());
 Assert.assertEquals(0.0d, paragraphFrame.getFrameFormat().getVerticalDistanceFromText());
 
```

**Returns:**
[FrameFormat](../../com.aspose.words/frameformat/) - The corresponding [FrameFormat](../../com.aspose.words/frameformat/) value.
### getLastChild() {#getLastChild}
```
public Node getLastChild()
```


Ermittelt das letzte Kind des Knotens.

 **Remarks:** 

Wenn es keinen letzten Kindknoten gibt, wird ein  null  zurückgegeben.

 **Examples:** 

Zeigt, wie man Methoden von Node und CompositeNode verwendet, um einen Abschnitt vor dem letzten Abschnitt im Dokument zu entfernen.

```

 Document doc = new Document();
 DocumentBuilder builder = new DocumentBuilder(doc);

 builder.writeln("Section 1 text.");
 builder.insertBreak(BreakType.SECTION_BREAK_CONTINUOUS);
 builder.writeln("Section 2 text.");

 // Both sections are siblings of each other.
 Section lastSection = (Section) doc.getLastChild();
 Section firstSection = (Section) lastSection.getPreviousSibling();

 // Remove a section based on its sibling relationship with another section.
 if (lastSection.getPreviousSibling() != null)
     doc.removeChild(firstSection);

 // The section we removed was the first one, leaving the document with only the second.
 Assert.assertEquals("Section 2 text.", doc.getText().trim());
 
```

**Returns:**
[Node](../../com.aspose.words/node/) - The last child of the node.
### getListFormat() {#getListFormat}
```
public ListFormat getListFormat()
```


Stellt Zugriff auf die Listformatierungseigenschaften des Absatzes bereit.

 **Examples:** 

Zeigt, wie alle Absätze in einem Dokument, die Listenelemente sind, ausgegeben werden.

```

 Document doc = new Document();
 DocumentBuilder builder = new DocumentBuilder(doc);

 builder.getListFormat().applyNumberDefault();
 builder.writeln("Numbered list item 1");
 builder.writeln("Numbered list item 2");
 builder.writeln("Numbered list item 3");
 builder.getListFormat().removeNumbers();

 builder.getListFormat().applyBulletDefault();
 builder.writeln("Bulleted list item 1");
 builder.writeln("Bulleted list item 2");
 builder.writeln("Bulleted list item 3");
 builder.getListFormat().removeNumbers();

 NodeCollection paras = doc.getChildNodes(NodeType.PARAGRAPH, true);
 for (Paragraph para : (Iterable) paras) {
     if (para.getListFormat().isListItem()) {
         System.out.println(java.text.MessageFormat.format("*** A paragraph belongs to list {0}", para.getListFormat().getList().getListId()));
         System.out.println(para.getText());
     }
 }
 
```

**Returns:**
[ListFormat](../../com.aspose.words/listformat/) - The corresponding [ListFormat](../../com.aspose.words/listformat/) value.
### getListLabel() {#getListLabel}
```
public ListLabel getListLabel()
```


Liefert ein [getListLabel()](../../com.aspose.words/paragraph/\#getListLabel)-Objekt, das Zugriff auf den Listennummerierungswert und die Formatierung für diesen Absatz bietet.

 **Examples:** 

Zeigt, wie die List-Labels aller Absätze, die Listenelemente sind, extrahiert werden können.

```
{@code
 Document doc = new Document(getMyDir() + "Rendering.docx");
 doc.updateListLabels();
 int listParaCount = 1;

 for (Paragraph paragraph : (Iterable) doc.getChildNodes(NodeType.PARAGRAPH, true)) {
     // Find if we have the paragraph list. In our document, our list uses plain Arabic numbers,
     // which start at three and ends at six.
     if (paragraph.getListFormat().isListItem()) {
         System.out.println(MessageFormat.format("List item paragraph #{0}", listParaCount));

         // This is the text we get when getting when we output this node to text format.
         // This text output will omit list labels. Trim any paragraph formatting characters.
         String paragraphText = paragraph.toString(SaveFormat.TEXT).trim();
         System.out.println("Exported Text: " + paragraphText);

         ListLabel label = paragraph.getListLabel();

         // This gets the position of the paragraph in the current level of the list. If we have a list with multiple levels,
         // this will tell us what position it is on that level.
         System.out.println("\tNumerical Id: {label.LabelValue}");

         // Combine them together to include the list label with the text in the output.
         System.out.println("\tList label combined with text: {label.LabelString} {paragraphText}");
     }
 }
```

**Returns:**
[ListLabel](../../com.aspose.words/listlabel/) - A [getListLabel()](../../com.aspose.words/paragraph/\#getListLabel) object that provides access to list numbering value and formatting for this paragraph.
### getNextMatchingNode(Node curNode) {#getNextMatchingNode-com.aspose.words.Node}
```
public Node getNextMatchingNode(Node curNode)
```




**Parameters:**
| Parameter | Typ | Beschreibung |
| --- | --- | --- |
| curNode | [Node](../../com.aspose.words/node/) |  |

**Returns:**
[Node](../../com.aspose.words/node/)
### getNextSibling() {#getNextSibling}
```
public Node getNextSibling()
```


Ermittelt den Knoten, der unmittelbar auf diesen Knoten folgt.

 **Remarks:** 

Wenn es keinen nächsten Knoten gibt, wird ein  null  zurückgegeben.

 **Examples:** 

Zeigt, wie man den Baum von Kindknoten eines zusammengesetzten Knotens durchläuft.

```

 public void recurseChildren() throws Exception {
     Document doc = new Document(getMyDir() + "Paragraphs.docx");

     // Any node that can contain child nodes, such as the document itself, is composite.
     Assert.assertTrue(doc.isComposite());

     // Invoke the recursive function that will go through and print all the child nodes of a composite node.
     traverseAllNodes(doc, 0);
 }

 /// 
 /// Recursively traverses a node tree while printing the type of each node
 /// with an indent depending on depth as well as the contents of all inline nodes.
 /// 
 public void traverseAllNodes(CompositeNode parentNode, int depth) {
     for (Node childNode = parentNode.getFirstChild(); childNode != null; childNode = childNode.getNextSibling()) {
         System.out.println(MessageFormat.format("{0}{1}", String.format("    ", depth), Node.nodeTypeToString(childNode.getNodeType())));

         // Recurse into the node if it is a composite node. Otherwise, print its contents if it is an inline node.
         if (childNode.isComposite()) {
             System.out.println();
             traverseAllNodes((CompositeNode) childNode, depth + 1);
         } else if (childNode instanceof Inline) {
             System.out.println(MessageFormat.format(" - \"{0}\"", childNode.getText().trim()));
         } else {
             System.out.println();
         }
     }
 }
 
```

Zeigt, wie man die Eigenschaft NextSibling eines Knotens verwendet, um seine unmittelbaren Kinder zu enumerieren.

```

 Document doc = new Document(getMyDir() + "Paragraphs.docx");

 for (Node node = doc.getFirstSection().getBody().getFirstChild(); node != null; node = node.getNextSibling()) {
     System.out.println(Node.nodeTypeToString(node.getNodeType()));
 }
 
```

**Returns:**
[Node](../../com.aspose.words/node/) - The node immediately following this node.
### getNodeType() {#getNodeType}
```
public int getNodeType()
```


Gibt [NodeType.PARAGRAPH](../../com.aspose.words/nodetype/\#PARAGRAPH) zurück.

 **Examples:** 

Zeigt, wie man den Baum von Kindknoten eines zusammengesetzten Knotens durchläuft.

```

 public void recurseChildren() throws Exception {
     Document doc = new Document(getMyDir() + "Paragraphs.docx");

     // Any node that can contain child nodes, such as the document itself, is composite.
     Assert.assertTrue(doc.isComposite());

     // Invoke the recursive function that will go through and print all the child nodes of a composite node.
     traverseAllNodes(doc, 0);
 }

 /// 
 /// Recursively traverses a node tree while printing the type of each node
 /// with an indent depending on depth as well as the contents of all inline nodes.
 /// 
 public void traverseAllNodes(CompositeNode parentNode, int depth) {
     for (Node childNode = parentNode.getFirstChild(); childNode != null; childNode = childNode.getNextSibling()) {
         System.out.println(MessageFormat.format("{0}{1}", String.format("    ", depth), Node.nodeTypeToString(childNode.getNodeType())));

         // Recurse into the node if it is a composite node. Otherwise, print its contents if it is an inline node.
         if (childNode.isComposite()) {
             System.out.println();
             traverseAllNodes((CompositeNode) childNode, depth + 1);
         } else if (childNode instanceof Inline) {
             System.out.println(MessageFormat.format(" - \"{0}\"", childNode.getText().trim()));
         } else {
             System.out.println();
         }
     }
 }
 
```

**Returns:**
int - [NodeType.PARAGRAPH](../../com.aspose.words/nodetype/\#PARAGRAPH). Der zurückgegebene Wert ist einer der Konstanten von [NodeType](../../com.aspose.words/nodetype/).
### getParagraphBreakFont() {#getParagraphBreakFont}
```
public Font getParagraphBreakFont()
```


Stellt Zugriff auf die Schriftformatierung des Absatzumbruchzeichens bereit.

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

**Returns:**
[Font](../../com.aspose.words/font/) - The corresponding [Font](../../com.aspose.words/font/) value.
### getParagraphFormat() {#getParagraphFormat}
```
public ParagraphFormat getParagraphFormat()
```


Stellt Zugriff auf die Absatzformatierungseigenschaften bereit.

 **Examples:** 

Zeigt, wie man ein Aspose.Words-Dokument von Hand erstellt.

```

 Document doc = new Document();

 // A blank document contains one section, one body and one paragraph.
 // Call the "RemoveAllChildren" method to remove all those nodes,
 // and end up with a document node with no children.
 doc.removeAllChildren();

 // This document now has no composite child nodes that we can add content to.
 // If we wish to edit it, we will need to repopulate its node collection.
 // First, create a new section, and then append it as a child to the root document node.
 Section section = new Section(doc);
 doc.appendChild(section);

 // Set some page setup properties for the section.
 section.getPageSetup().setSectionStart(SectionStart.NEW_PAGE);
 section.getPageSetup().setPaperSize(PaperSize.LETTER);

 // A section needs a body, which will contain and display all its contents
 // on the page between the section's header and footer.
 Body body = new Body(doc);
 section.appendChild(body);

 // Create a paragraph, set some formatting properties, and then append it as a child to the body.
 Paragraph para = new Paragraph(doc);

 para.getParagraphFormat().setStyleName("Heading 1");
 para.getParagraphFormat().setAlignment(ParagraphAlignment.CENTER);

 body.appendChild(para);

 // Finally, add some content to do the document. Create a run,
 // set its appearance and contents, and then append it as a child to the paragraph.
 Run run = new Run(doc);
 run.setText("Hello World!");
 run.getFont().setColor(Color.RED);
 para.appendChild(run);

 Assert.assertEquals("Hello World!", doc.getText().trim());

 doc.save(getArtifactsDir() + "Section.CreateManually.docx");
 
```

**Returns:**
[ParagraphFormat](../../com.aspose.words/paragraphformat/) - The corresponding [ParagraphFormat](../../com.aspose.words/paragraphformat/) value.
### getParentNode() {#getParentNode}
```
public CompositeNode getParentNode()
```


Ermittelt den unmittelbaren übergeordneten Knoten dieses Knotens.

 **Remarks:** 

Wenn ein Knoten gerade erstellt wurde und noch nicht zum Baum hinzugefügt wurde, oder wenn er aus dem Baum entfernt wurde, ist der übergeordnete Knoten  null .

 **Examples:** 

Zeigt, wie man auf den übergeordneten Knoten eines Knotens zugreift.

```

 Document doc = new Document();
 Paragraph para = doc.getFirstSection().getBody().getFirstParagraph();

 // Append a child Run node to the document's first paragraph.
 Run run = new Run(doc, "Hello world!");
 para.appendChild(run);

 // The paragraph is the parent node of the run node. We can trace this lineage
 // all the way to the document node, which is the root of the document's node tree.
 Assert.assertEquals(para, run.getParentNode());
 Assert.assertEquals(doc.getFirstSection().getBody(), para.getParentNode());
 Assert.assertEquals(doc.getFirstSection(), doc.getFirstSection().getBody().getParentNode());
 Assert.assertEquals(doc, doc.getFirstSection().getParentNode());
 
```

Zeigt, wie man einen Knoten erstellt und sein zugehöriges Dokument festlegt.

```

 Document doc = new Document();
 Paragraph para = new Paragraph(doc);
 para.appendChild(new Run(doc, "Hello world!"));

 // We have not yet appended this paragraph as a child to any composite node.
 Assert.assertNull(para.getParentNode());

 // If a node is an appropriate child node type of another composite node,
 // we can attach it as a child only if both nodes have the same owner document.
 // The owner document is the document we passed to the node's constructor.
 // We have not attached this paragraph to the document, so the document does not contain its text.
 Assert.assertEquals(para.getDocument(), doc);
 Assert.assertEquals("", doc.getText().trim());

 // Since the document owns this paragraph, we can apply one of its styles to the paragraph's contents.
 para.getParagraphFormat().setStyleName("Heading 1");

 // Add this node to the document, and then verify its contents.
 doc.getFirstSection().getBody().appendChild(para);

 Assert.assertEquals(doc.getFirstSection().getBody(), para.getParentNode());
 Assert.assertEquals("Hello world!", doc.getText().trim());
 
```

**Returns:**
[CompositeNode](../../com.aspose.words/compositenode/) - The immediate parent of this node.
### getParentSection() {#getParentSection}
```
public Section getParentSection()
```


Ruft die übergeordnete [Section](../../com.aspose.words/section/) des Absatzes ab.

 **Examples:** 

Zeigt, wie man einen Header und einen Footer erstellt.

```

 Document doc = new Document();

 // Create a header and append a paragraph to it. The text in that paragraph
 // will appear at the top of every page of this section, above the main body text.
 HeaderFooter header = new HeaderFooter(doc, HeaderFooterType.HEADER_PRIMARY);
 doc.getFirstSection().getHeadersFooters().add(header);

 Paragraph para = header.appendParagraph("My header.");

 Assert.assertTrue(header.isHeader());
 Assert.assertTrue(para.isEndOfHeaderFooter());

 // Create a footer and append a paragraph to it. The text in that paragraph
 // will appear at the bottom of every page of this section, below the main body text.
 HeaderFooter footer = new HeaderFooter(doc, HeaderFooterType.FOOTER_PRIMARY);
 doc.getFirstSection().getHeadersFooters().add(footer);

 para = footer.appendParagraph("My footer.");

 Assert.assertFalse(footer.isHeader());
 Assert.assertTrue(para.isEndOfHeaderFooter());

 Assert.assertEquals(para.getParentStory(), footer);
 Assert.assertEquals(para.getParentSection(), footer.getParentSection());
 Assert.assertEquals(header.getParentSection(), footer.getParentSection());

 doc.save(getArtifactsDir() + "HeaderFooter.Create.docx");
 
```

**Returns:**
[Section](../../com.aspose.words/section/) - The corresponding [Section](../../com.aspose.words/section/) value.
### getParentStory() {#getParentStory}
```
public Story getParentStory()
```


Ruft die übergeordnete Story auf Abschnittsebene ab, die entweder [Body](../../com.aspose.words/body/) oder [HeaderFooter](../../com.aspose.words/headerfooter/) sein kann.

 **Examples:** 

Zeigt, wie man einen Header und einen Footer erstellt.

```

 Document doc = new Document();

 // Create a header and append a paragraph to it. The text in that paragraph
 // will appear at the top of every page of this section, above the main body text.
 HeaderFooter header = new HeaderFooter(doc, HeaderFooterType.HEADER_PRIMARY);
 doc.getFirstSection().getHeadersFooters().add(header);

 Paragraph para = header.appendParagraph("My header.");

 Assert.assertTrue(header.isHeader());
 Assert.assertTrue(para.isEndOfHeaderFooter());

 // Create a footer and append a paragraph to it. The text in that paragraph
 // will appear at the bottom of every page of this section, below the main body text.
 HeaderFooter footer = new HeaderFooter(doc, HeaderFooterType.FOOTER_PRIMARY);
 doc.getFirstSection().getHeadersFooters().add(footer);

 para = footer.appendParagraph("My footer.");

 Assert.assertFalse(footer.isHeader());
 Assert.assertTrue(para.isEndOfHeaderFooter());

 Assert.assertEquals(para.getParentStory(), footer);
 Assert.assertEquals(para.getParentSection(), footer.getParentSection());
 Assert.assertEquals(header.getParentSection(), footer.getParentSection());

 doc.save(getArtifactsDir() + "HeaderFooter.Create.docx");
 
```

**Returns:**
[Story](../../com.aspose.words/story/) - The corresponding [Story](../../com.aspose.words/story/) value.
### getPreviousSibling() {#getPreviousSibling}
```
public Node getPreviousSibling()
```


Ermittelt den Knoten, der unmittelbar vor diesem Knoten liegt.

 **Remarks:** 

Wenn es keinen vorhergehenden Knoten gibt, wird ein  null  zurückgegeben.

 **Examples:** 

Zeigt, wie man Methoden von Node und CompositeNode verwendet, um einen Abschnitt vor dem letzten Abschnitt im Dokument zu entfernen.

```

 Document doc = new Document();
 DocumentBuilder builder = new DocumentBuilder(doc);

 builder.writeln("Section 1 text.");
 builder.insertBreak(BreakType.SECTION_BREAK_CONTINUOUS);
 builder.writeln("Section 2 text.");

 // Both sections are siblings of each other.
 Section lastSection = (Section) doc.getLastChild();
 Section firstSection = (Section) lastSection.getPreviousSibling();

 // Remove a section based on its sibling relationship with another section.
 if (lastSection.getPreviousSibling() != null)
     doc.removeChild(firstSection);

 // The section we removed was the first one, leaving the document with only the second.
 Assert.assertEquals("Section 2 text.", doc.getText().trim());
 
```

**Returns:**
[Node](../../com.aspose.words/node/) - The node immediately preceding this node.
### getRange() {#getRange}
```
public Range getRange()
```


Gibt ein [Range](../../com.aspose.words/range/)-Objekt zurück, das den Teil eines Dokuments darstellt, der in diesem Knoten enthalten ist.

 **Examples:** 

Zeigt, wie man alle Knoten aus einem Bereich löscht.

```

 Document doc = new Document();
 DocumentBuilder builder = new DocumentBuilder(doc);

 // Add text to the first section in the document, and then add another section.
 builder.write("Section 1. ");
 builder.insertBreak(BreakType.SECTION_BREAK_CONTINUOUS);
 builder.write("Section 2.");

 Assert.assertEquals("Section 1. \fSection 2.", doc.getText().trim());

 // Remove the first section entirely by removing all the nodes
 // within its range, including the section itself.
 doc.getSections().get(0).getRange().delete();

 Assert.assertEquals(1, doc.getSections().getCount());
 Assert.assertEquals("Section 2.", doc.getText().trim());
 
```

**Returns:**
[Range](../../com.aspose.words/range/) - A [Range](../../com.aspose.words/range/) object that represents the portion of a document that is contained in this node.
### getRuns() {#getRuns}
```
public RunCollection getRuns()
```


Stellt Zugriff auf die typisierte Sammlung von Textstücken innerhalb des Absatzes bereit.

 **Examples:** 

Zeigt, wie der Revisionstyp eines Inline‑Knotens ermittelt wird.

```

 Document doc = new Document(getMyDir() + "Revision runs.docx");

 // When we edit the document while the "Track Changes" option, found in via Review -> Tracking,
 // is turned on in Microsoft Word, the changes we apply count as revisions.
 // When editing a document using Aspose.Words, we can begin tracking revisions by
 // invoking the document's "StartTrackRevisions" method and stop tracking by using the "StopTrackRevisions" method.
 // We can either accept revisions to assimilate them into the document
 // or reject them to change the proposed change effectively.
 Assert.assertEquals(6, doc.getRevisions().getCount());

 // The parent node of a revision is the run that the revision concerns. A Run is an Inline node.
 Run run = (Run) doc.getRevisions().get(0).getParentNode();

 Paragraph firstParagraph = run.getParentParagraph();
 RunCollection runs = firstParagraph.getRuns();

 Assert.assertEquals(runs.getCount(), 6);

 // Below are five types of revisions that can flag an Inline node.
 // 1 -  An "insert" revision:
 // This revision occurs when we insert text while tracking changes.
 Assert.assertTrue(runs.get(2).isInsertRevision());

 // 2 -  A "format" revision:
 // This revision occurs when we change the formatting of text while tracking changes.
 Assert.assertTrue(runs.get(2).isFormatRevision());

 // 3 -  A "move from" revision:
 // When we highlight text in Microsoft Word, and then drag it to a different place in the document
 // while tracking changes, two revisions appear.
 // The "move from" revision is a copy of the text originally before we moved it.
 Assert.assertTrue(runs.get(4).isMoveFromRevision());

 // 4 -  A "move to" revision:
 // The "move to" revision is the text that we moved in its new position in the document.
 // "Move from" and "move to" revisions appear in pairs for every move revision we carry out.
 // Accepting a move revision deletes the "move from" revision and its text,
 // and keeps the text from the "move to" revision.
 // Rejecting a move revision conversely keeps the "move from" revision and deletes the "move to" revision.
 Assert.assertTrue(runs.get(1).isMoveToRevision());

 // 5 -  A "delete" revision:
 // This revision occurs when we delete text while tracking changes. When we delete text like this,
 // it will stay in the document as a revision until we either accept the revision,
 // which will delete the text for good, or reject the revision, which will keep the text we deleted where it was.
 Assert.assertTrue(runs.get(5).isDeleteRevision());
 
```

**Returns:**
[RunCollection](../../com.aspose.words/runcollection/) - The corresponding [RunCollection](../../com.aspose.words/runcollection/) value.
### getText() {#getText}
```
public String getText()
```


Liefert den Text dieses Absatzes einschließlich des Absatzendezeichens.

 **Remarks:** 

Der Text aller Kindknoten wird verkettet und das Absatzende‑Zeichen wird wie folgt angehängt:

 *  If the paragraph is the last paragraph of [Body](../../com.aspose.words/body/), then [ControlChar.SECTION\_BREAK](../../com.aspose.words/controlchar/\#SECTION-BREAK) (\\x000c) is appended.
 *  If the paragraph is the last paragraph of [Cell](../../com.aspose.words/cell/), then [ControlChar.CELL](../../com.aspose.words/controlchar/\#CELL) (\\x0007) is appended.
 *  For all other paragraphs [ControlChar.PARAGRAPH\_BREAK](../../com.aspose.words/controlchar/\#PARAGRAPH-BREAK) (\\r) is appended.

Der zurückgegebene String enthält alle Steuer- und Sonderzeichen, wie in [ControlChar](../../com.aspose.words/controlchar/) beschrieben.

 **Examples:** 

Zeigt, wie man Kindknoten in der Sammlung von Kindknoten eines CompositeNode hinzufügt, aktualisiert und löscht.

```

 Document doc = new Document();

 // An empty document, by default, has one paragraph.
 Assert.assertEquals(1, doc.getFirstSection().getBody().getParagraphs().getCount());

 // Composite nodes such as our paragraph can contain other composite and inline nodes as children.
 Paragraph paragraph = doc.getFirstSection().getBody().getFirstParagraph();
 Run paragraphText = new Run(doc, "Initial text. ");
 paragraph.appendChild(paragraphText);

 // Create three more run nodes.
 Run run1 = new Run(doc, "Run 1. ");
 Run run2 = new Run(doc, "Run 2. ");
 Run run3 = new Run(doc, "Run 3. ");

 // The document body will not display these runs until we insert them into a composite node
 // that itself is a part of the document's node tree, as we did with the first run.
 // We can determine where the text contents of nodes that we insert
 // appears in the document by specifying an insertion location relative to another node in the paragraph.
 Assert.assertEquals("Initial text.", paragraph.getText().trim());

 // Insert the second run into the paragraph in front of the initial run.
 paragraph.insertBefore(run2, paragraphText);

 Assert.assertEquals("Run 2. Initial text.", paragraph.getText().trim());

 // Insert the third run after the initial run.
 paragraph.insertAfter(run3, paragraphText);

 Assert.assertEquals("Run 2. Initial text. Run 3.", paragraph.getText().trim());

 // Insert the first run to the start of the paragraph's child nodes collection.
 paragraph.prependChild(run1);

 Assert.assertEquals("Run 1. Run 2. Initial text. Run 3.", paragraph.getText().trim());
 Assert.assertEquals(4, paragraph.getChildNodes(NodeType.ANY, true).getCount());

 // We can modify the contents of the run by editing and deleting existing child nodes.
 ((Run) paragraph.getChildNodes(NodeType.RUN, true).get(1)).setText("Updated run 2. ");
 paragraph.getChildNodes(NodeType.RUN, true).remove(paragraphText);

 Assert.assertEquals("Run 1. Updated run 2. Run 3.", paragraph.getText().trim());
 Assert.assertEquals(3, paragraph.getChildNodes(NodeType.ANY, true).getCount());
 
```

**Returns:**
java.lang.String
### hasChildNodes() {#hasChildNodes}
```
public boolean hasChildNodes()
```


Gibt  true  zurück, wenn dieser Knoten Kindknoten hat.

 **Examples:** 

Zeigt, wie man die Zeilen aus zwei Tabellen zu einer kombiniert.

```

 Document doc = new Document(getMyDir() + "Tables.docx");

 // Below are two ways of getting a table from a document.
 // 1 -  From the "Tables" collection of a Body node:
 Table firstTable = doc.getFirstSection().getBody().getTables().get(0);

 // 2 -  Using the "GetChild" method:
 Table secondTable = (Table) doc.getChild(NodeType.TABLE, 1, true);

 // Append all rows from the current table to the next.
 while (secondTable.hasChildNodes())
     firstTable.getRows().add(secondTable.getFirstRow());

 // Remove the empty table container.
 secondTable.remove();

 doc.save(getArtifactsDir() + "Table.CombineTables.docx");
 
```

**Returns:**
boolean -  true  wenn dieser Knoten Kindknoten hat.
### indexOf(Node child) {#indexOf-com.aspose.words.Node}
```
public int indexOf(Node child)
```


Gibt den Index des angegebenen Kindknotens im Kindknoten-Array zurück.

 **Remarks:** 

Gibt -1 zurück, wenn der Knoten in den Kindknoten nicht gefunden wird.

 **Examples:** 

Zeigt, wie man den Index eines bestimmten Kindknotens vom übergeordneten Knoten erhält.

```

 Document doc = new Document(getMyDir() + "Rendering.docx");

 Body body = doc.getFirstSection().getBody();

 // Retrieve the index of the last paragraph in the body of the first section.
 Assert.assertEquals(24, body.getChildNodes(NodeType.ANY, false).indexOf(body.getLastParagraph()));
 
```

**Parameters:**
| Parameter | Typ | Beschreibung |
| --- | --- | --- |
| child | [Node](../../com.aspose.words/node/) |  |

**Returns:**
int
### insertAfter(Node newChild, Node refChild) {#insertAfter-com.aspose.words.Node-com.aspose.words.Node}
```
public Node insertAfter(Node newChild, Node refChild)
```


Fügt den angegebenen Knoten unmittelbar nach dem angegebenen Referenzknoten ein.

 **Remarks:** 

Wenn  refChild  null ist, wird  newChild  am Anfang der Liste der Kindknoten eingefügt.

Wenn der  newChild  bereits im Baum ist, wird er zuerst entfernt.

Wenn der einzufügende Knoten aus einem anderen Dokument erstellt wurde, sollten Sie **M:Aspose.Words.DocumentBase.ImportNode(Aspose.Words.Node,System.Boolean,Aspose.Words.ImportFormatMode)** verwenden, um den Knoten in das aktuelle Dokument zu importieren. Der importierte Knoten kann dann in das aktuelle Dokument eingefügt werden.

 **Examples:** 

Zeigt, wie man Kindknoten in der Sammlung von Kindknoten eines CompositeNode hinzufügt, aktualisiert und löscht.

```

 Document doc = new Document();

 // An empty document, by default, has one paragraph.
 Assert.assertEquals(1, doc.getFirstSection().getBody().getParagraphs().getCount());

 // Composite nodes such as our paragraph can contain other composite and inline nodes as children.
 Paragraph paragraph = doc.getFirstSection().getBody().getFirstParagraph();
 Run paragraphText = new Run(doc, "Initial text. ");
 paragraph.appendChild(paragraphText);

 // Create three more run nodes.
 Run run1 = new Run(doc, "Run 1. ");
 Run run2 = new Run(doc, "Run 2. ");
 Run run3 = new Run(doc, "Run 3. ");

 // The document body will not display these runs until we insert them into a composite node
 // that itself is a part of the document's node tree, as we did with the first run.
 // We can determine where the text contents of nodes that we insert
 // appears in the document by specifying an insertion location relative to another node in the paragraph.
 Assert.assertEquals("Initial text.", paragraph.getText().trim());

 // Insert the second run into the paragraph in front of the initial run.
 paragraph.insertBefore(run2, paragraphText);

 Assert.assertEquals("Run 2. Initial text.", paragraph.getText().trim());

 // Insert the third run after the initial run.
 paragraph.insertAfter(run3, paragraphText);

 Assert.assertEquals("Run 2. Initial text. Run 3.", paragraph.getText().trim());

 // Insert the first run to the start of the paragraph's child nodes collection.
 paragraph.prependChild(run1);

 Assert.assertEquals("Run 1. Run 2. Initial text. Run 3.", paragraph.getText().trim());
 Assert.assertEquals(4, paragraph.getChildNodes(NodeType.ANY, true).getCount());

 // We can modify the contents of the run by editing and deleting existing child nodes.
 ((Run) paragraph.getChildNodes(NodeType.RUN, true).get(1)).setText("Updated run 2. ");
 paragraph.getChildNodes(NodeType.RUN, true).remove(paragraphText);

 Assert.assertEquals("Run 1. Updated run 2. Run 3.", paragraph.getText().trim());
 Assert.assertEquals(3, paragraph.getChildNodes(NodeType.ANY, true).getCount());
 
```

Zeigt, wie man alle Textfeldformen durch Bildformen ersetzt.

```

 Document doc = new Document(getMyDir() + "Textboxes in drawing canvas.docx");

 List shapeList = Arrays.stream(doc.getChildNodes(NodeType.SHAPE, true).toArray())
         .filter(Shape.class::isInstance)
         .map(Shape.class::cast)
         .collect(Collectors.toList());

 Assert.assertEquals(3, IterableUtils.countMatches(shapeList, s -> s.getShapeType() == ShapeType.TEXT_BOX));
 Assert.assertEquals(1, IterableUtils.countMatches(shapeList, s -> s.getShapeType() == ShapeType.IMAGE));

 for (Shape shape : shapeList) {
     if (((shape.getShapeType()) == (ShapeType.TEXT_BOX))) {
         Shape replacementShape = new Shape(doc, ShapeType.IMAGE);
         replacementShape.getImageData().setImage(getImageDir() + "Logo.jpg");
         replacementShape.setLeft(shape.getLeft());
         replacementShape.setTop(shape.getTop());
         replacementShape.setWidth(shape.getWidth());
         replacementShape.setHeight(shape.getHeight());
         replacementShape.setRelativeHorizontalPosition(shape.getRelativeHorizontalPosition());
         replacementShape.setRelativeVerticalPosition(shape.getRelativeVerticalPosition());
         replacementShape.setHorizontalAlignment(shape.getHorizontalAlignment());
         replacementShape.setVerticalAlignment(shape.getVerticalAlignment());
         replacementShape.setWrapType(shape.getWrapType());
         replacementShape.setWrapSide(shape.getWrapSide());

         shape.getParentNode().insertAfter(replacementShape, shape);
         shape.remove();
     }
 }

 shapeList = Arrays.stream(doc.getChildNodes(NodeType.SHAPE, true).toArray())
         .filter(Shape.class::isInstance)
         .map(Shape.class::cast)
         .collect(Collectors.toList());

 Assert.assertEquals(0, IterableUtils.countMatches(shapeList, s -> s.getShapeType() == ShapeType.TEXT_BOX));
 Assert.assertEquals(4, IterableUtils.countMatches(shapeList, s -> s.getShapeType() == ShapeType.IMAGE));

 doc.save(getArtifactsDir() + "Shape.ReplaceTextboxesWithImages.docx");
 
```

**Parameters:**
| Parameter | Typ | Beschreibung |
| --- | --- | --- |
| newChild | [Node](../../com.aspose.words/node/) | Der [Node](../../com.aspose.words/node/) zum Einfügen. |
| refChild | [Node](../../com.aspose.words/node/) | Der [Node](../../com.aspose.words/node/), der der Referenzknoten ist. Der  newChild  wird nach dem  refChild  platziert. |

**Returns:**
[Node](../../com.aspose.words/node/) - The inserted node.
### insertBefore(Node newChild, Node refChild) {#insertBefore-com.aspose.words.Node-com.aspose.words.Node}
```
public Node insertBefore(Node newChild, Node refChild)
```


Fügt den angegebenen Knoten unmittelbar vor dem angegebenen Referenzknoten ein.

 **Remarks:** 

Wenn  refChild  null ist, wird  newChild  am Ende der Liste der Kindknoten eingefügt.

Wenn der  newChild  bereits im Baum ist, wird er zuerst entfernt.

Wenn der einzufügende Knoten aus einem anderen Dokument erstellt wurde, sollten Sie **M:Aspose.Words.DocumentBase.ImportNode(Aspose.Words.Node,System.Boolean,Aspose.Words.ImportFormatMode)** verwenden, um den Knoten in das aktuelle Dokument zu importieren. Der importierte Knoten kann dann in das aktuelle Dokument eingefügt werden.

 **Examples:** 

Zeigt, wie man Kindknoten in der Sammlung von Kindknoten eines CompositeNode hinzufügt, aktualisiert und löscht.

```

 Document doc = new Document();

 // An empty document, by default, has one paragraph.
 Assert.assertEquals(1, doc.getFirstSection().getBody().getParagraphs().getCount());

 // Composite nodes such as our paragraph can contain other composite and inline nodes as children.
 Paragraph paragraph = doc.getFirstSection().getBody().getFirstParagraph();
 Run paragraphText = new Run(doc, "Initial text. ");
 paragraph.appendChild(paragraphText);

 // Create three more run nodes.
 Run run1 = new Run(doc, "Run 1. ");
 Run run2 = new Run(doc, "Run 2. ");
 Run run3 = new Run(doc, "Run 3. ");

 // The document body will not display these runs until we insert them into a composite node
 // that itself is a part of the document's node tree, as we did with the first run.
 // We can determine where the text contents of nodes that we insert
 // appears in the document by specifying an insertion location relative to another node in the paragraph.
 Assert.assertEquals("Initial text.", paragraph.getText().trim());

 // Insert the second run into the paragraph in front of the initial run.
 paragraph.insertBefore(run2, paragraphText);

 Assert.assertEquals("Run 2. Initial text.", paragraph.getText().trim());

 // Insert the third run after the initial run.
 paragraph.insertAfter(run3, paragraphText);

 Assert.assertEquals("Run 2. Initial text. Run 3.", paragraph.getText().trim());

 // Insert the first run to the start of the paragraph's child nodes collection.
 paragraph.prependChild(run1);

 Assert.assertEquals("Run 1. Run 2. Initial text. Run 3.", paragraph.getText().trim());
 Assert.assertEquals(4, paragraph.getChildNodes(NodeType.ANY, true).getCount());

 // We can modify the contents of the run by editing and deleting existing child nodes.
 ((Run) paragraph.getChildNodes(NodeType.RUN, true).get(1)).setText("Updated run 2. ");
 paragraph.getChildNodes(NodeType.RUN, true).remove(paragraphText);

 Assert.assertEquals("Run 1. Updated run 2. Run 3.", paragraph.getText().trim());
 Assert.assertEquals(3, paragraph.getChildNodes(NodeType.ANY, true).getCount());
 
```

**Parameters:**
| Parameter | Typ | Beschreibung |
| --- | --- | --- |
| newChild | [Node](../../com.aspose.words/node/) | Der [Node](../../com.aspose.words/node/) zum Einfügen. |
| refChild | [Node](../../com.aspose.words/node/) | Der [Node](../../com.aspose.words/node/), der der Referenzknoten ist. Der  newChild  wird vor diesem Knoten platziert. |

**Returns:**
[Node](../../com.aspose.words/node/) - The inserted node.
### insertField(int fieldType, boolean updateField, Node refNode, boolean isAfter) {#insertField-int-boolean-com.aspose.words.Node-boolean}
```
public Field insertField(int fieldType, boolean updateField, Node refNode, boolean isAfter)
```




**Parameters:**
| Parameter | Typ | Beschreibung |
| --- | --- | --- |
| fieldType | int |  |
| updateField | boolean |  |
| refNode | [Node](../../com.aspose.words/node/) |  |
| isAfter | boolean |  |

**Returns:**
[Field](../../com.aspose.words/field/)
### insertField(String fieldCode, Node refNode, boolean isAfter) {#insertField-java.lang.String-com.aspose.words.Node-boolean}
```
public Field insertField(String fieldCode, Node refNode, boolean isAfter)
```


Fügt ein Feld in diesen Absatz ein.

 **Examples:** 

Zeigt verschiedene Möglichkeiten, Felder zu einem Absatz hinzuzufügen.

```

 Document doc = new Document();
 Paragraph para = doc.getFirstSection().getBody().getFirstParagraph();

 // Below are three ways of inserting a field into a paragraph.
 // 1 -  Insert an AUTHOR field into a paragraph after one of the paragraph's child nodes:
 Run run = new Run(doc);
 {
     run.setText("This run was written by ");
 }
 para.appendChild(run);

 doc.getBuiltInDocumentProperties().get("Author").setValue("John Doe");
 para.insertField(FieldType.FIELD_AUTHOR, true, run, true);

 // 2 -  Insert a QUOTE field after one of the paragraph's child nodes:
 run = new Run(doc);
 {
     run.setText(".");
 }
 para.appendChild(run);

 Field field = para.insertField(" QUOTE \" Real value\" ", run, true);

 // 3 -  Insert a QUOTE field before one of the paragraph's child nodes,
 // and get it to display a placeholder value:
 para.insertField(" QUOTE \" Real value.\"", " Placeholder value.", field.getStart(), false);

 Assert.assertEquals(" Placeholder value.", doc.getRange().getFields().get(1).getResult());

 // This field will display its placeholder value until we update it.
 doc.updateFields();

 Assert.assertEquals(" Real value.", doc.getRange().getFields().get(1).getResult());

 doc.save(getArtifactsDir() + "Paragraph.InsertField.docx");
 
```

**Parameters:**
| Parameter | Typ | Beschreibung |
| --- | --- | --- |
| fieldCode | java.lang.String | Der einzufügende Feldcode (ohne geschweifte Klammern). |
| refNode | [Node](../../com.aspose.words/node/) | Referenzknoten innerhalb dieses Absatzes (wenn  refNode  null ist, wird am Ende des Absatzes angehängt). |
| isAfter | boolean | Ob das Feld nach oder vor dem Referenzknoten eingefügt werden soll. |

**Returns:**
[Field](../../com.aspose.words/field/) - A [Field](../../com.aspose.words/field/) object that represents the inserted field.
### insertField(String fieldCode, String fieldValue, Node refNode, boolean isAfter) {#insertField-java.lang.String-java.lang.String-com.aspose.words.Node-boolean}
```
public Field insertField(String fieldCode, String fieldValue, Node refNode, boolean isAfter)
```


Fügt ein Feld in diesen Absatz ein.

 **Examples:** 

Zeigt verschiedene Möglichkeiten, Felder zu einem Absatz hinzuzufügen.

```

 Document doc = new Document();
 Paragraph para = doc.getFirstSection().getBody().getFirstParagraph();

 // Below are three ways of inserting a field into a paragraph.
 // 1 -  Insert an AUTHOR field into a paragraph after one of the paragraph's child nodes:
 Run run = new Run(doc);
 {
     run.setText("This run was written by ");
 }
 para.appendChild(run);

 doc.getBuiltInDocumentProperties().get("Author").setValue("John Doe");
 para.insertField(FieldType.FIELD_AUTHOR, true, run, true);

 // 2 -  Insert a QUOTE field after one of the paragraph's child nodes:
 run = new Run(doc);
 {
     run.setText(".");
 }
 para.appendChild(run);

 Field field = para.insertField(" QUOTE \" Real value\" ", run, true);

 // 3 -  Insert a QUOTE field before one of the paragraph's child nodes,
 // and get it to display a placeholder value:
 para.insertField(" QUOTE \" Real value.\"", " Placeholder value.", field.getStart(), false);

 Assert.assertEquals(" Placeholder value.", doc.getRange().getFields().get(1).getResult());

 // This field will display its placeholder value until we update it.
 doc.updateFields();

 Assert.assertEquals(" Real value.", doc.getRange().getFields().get(1).getResult());

 doc.save(getArtifactsDir() + "Paragraph.InsertField.docx");
 
```

**Parameters:**
| Parameter | Typ | Beschreibung |
| --- | --- | --- |
| fieldCode | java.lang.String | Der einzufügende Feldcode (ohne geschweifte Klammern). |
| fieldValue | java.lang.String | Der einzufügende Feldwert. Übergeben Sie  null  für Felder, die keinen Wert haben. |
| refNode | [Node](../../com.aspose.words/node/) | Referenzknoten innerhalb dieses Absatzes (wenn  refNode  null ist, wird am Ende des Absatzes angehängt). |
| isAfter | boolean | Ob das Feld nach oder vor dem Referenzknoten eingefügt werden soll. |

**Returns:**
[Field](../../com.aspose.words/field/) - A [Field](../../com.aspose.words/field/) object that represents the inserted field.
### isComposite() {#isComposite}
```
public boolean isComposite()
```


Gibt  true  zurück, da dieser Knoten Kindknoten haben kann.

 **Examples:** 

Zeigt, wie man den Baum von Kindknoten eines zusammengesetzten Knotens durchläuft.

```

 public void recurseChildren() throws Exception {
     Document doc = new Document(getMyDir() + "Paragraphs.docx");

     // Any node that can contain child nodes, such as the document itself, is composite.
     Assert.assertTrue(doc.isComposite());

     // Invoke the recursive function that will go through and print all the child nodes of a composite node.
     traverseAllNodes(doc, 0);
 }

 /// 
 /// Recursively traverses a node tree while printing the type of each node
 /// with an indent depending on depth as well as the contents of all inline nodes.
 /// 
 public void traverseAllNodes(CompositeNode parentNode, int depth) {
     for (Node childNode = parentNode.getFirstChild(); childNode != null; childNode = childNode.getNextSibling()) {
         System.out.println(MessageFormat.format("{0}{1}", String.format("    ", depth), Node.nodeTypeToString(childNode.getNodeType())));

         // Recurse into the node if it is a composite node. Otherwise, print its contents if it is an inline node.
         if (childNode.isComposite()) {
             System.out.println();
             traverseAllNodes((CompositeNode) childNode, depth + 1);
         } else if (childNode instanceof Inline) {
             System.out.println(MessageFormat.format(" - \"{0}\"", childNode.getText().trim()));
         } else {
             System.out.println();
         }
     }
 }
 
```

**Returns:**
boolean -  true  da dieser Knoten Kindknoten haben kann.
### isDeleteRevision() {#isDeleteRevision}
```
public boolean isDeleteRevision()
```


Gibt true zurück, wenn dieses Objekt in Microsoft Word gelöscht wurde, während die Änderungsverfolgung aktiviert war.

 **Examples:** 

Zeigt, wie man mit Revisionsabsätzen arbeitet.

```

 Document doc = new Document();
 Body body = doc.getFirstSection().getBody();
 Paragraph para = body.getFirstParagraph();

 para.appendChild(new Run(doc, "Paragraph 1. "));
 body.appendParagraph("Paragraph 2. ");
 body.appendParagraph("Paragraph 3. ");

 // The above paragraphs are not revisions.
 // Paragraphs that we add after starting revision tracking will register as "Insert" revisions.
 doc.startTrackRevisions("John Doe", new Date());

 para = body.appendParagraph("Paragraph 4. ");

 Assert.assertTrue(para.isInsertRevision());

 // Paragraphs that we remove after starting revision tracking will register as "Delete" revisions.
 ParagraphCollection paragraphs = body.getParagraphs();

 Assert.assertEquals(4, paragraphs.getCount());

 para = paragraphs.get(2);
 para.remove();

 // Such paragraphs will remain until we either accept or reject the delete revision.
 // Accepting the revision will remove the paragraph for good,
 // and rejecting the revision will leave it in the document as if we never deleted it.
 Assert.assertEquals(4, paragraphs.getCount());
 Assert.assertTrue(para.isDeleteRevision());

 // Accept the revision, and then verify that the paragraph is gone.
 doc.acceptAllRevisions();

 Assert.assertEquals(paragraphs.getCount(), 3);
 Assert.assertEquals(para.getCount(), 0);
 Assert.assertEquals(
         "Paragraph 1. \r" +
                 "Paragraph 2. \r" +
                 "Paragraph 4.", doc.getText().trim());
 
```

**Returns:**
boolean - True, wenn dieses Objekt in Microsoft Word gelöscht wurde, während die Änderungsverfolgung aktiviert war.
### isEndOfCell() {#isEndOfCell}
```
public boolean isEndOfCell()
```


True, wenn dieser Absatz der letzte Absatz in einer [Cell](../../com.aspose.words/cell/) ist; andernfalls false.

 **Examples:** 

Zeigt, wie man eine Tabelle so einstellt, dass sie auf derselben Seite zusammenbleibt.

```

 Document doc = new Document(getMyDir() + "Table spanning two pages.docx");
 Table table = doc.getFirstSection().getBody().getTables().get(0);

 // Enabling KeepWithNext for every paragraph in the table except for the
 // last ones in the last row will prevent the table from splitting across multiple pages.
 for (Cell cell : (Iterable) table.getChildNodes(NodeType.CELL, true))
     for (Paragraph para : cell.getParagraphs()) {
         Assert.assertTrue(para.isInCell());

         if (!(cell.getParentRow().isLastRow() && para.isEndOfCell()))
             para.getParagraphFormat().setKeepWithNext(true);
     }

 doc.save(getArtifactsDir() + "Table.KeepTableTogether.docx");
 
```

**Returns:**
boolean - Der entsprechende  boolean  Wert.
### isEndOfDocument() {#isEndOfDocument}
```
public boolean isEndOfDocument()
```


True, wenn dieser Absatz der letzte Absatz im letzten Abschnitt des Dokuments ist.

 **Examples:** 

Zeigt, wie ein Absatz in das Dokument eingefügt wird.

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
boolean - Der entsprechende  boolean  Wert.
### isEndOfHeaderFooter() {#isEndOfHeaderFooter}
```
public boolean isEndOfHeaderFooter()
```


True, wenn dieser Absatz der letzte Absatz im [HeaderFooter](../../com.aspose.words/headerfooter/) (Haupttext-Story) einer [Section](../../com.aspose.words/section/) ist; andernfalls false.

 **Examples:** 

Zeigt, wie man einen Header und einen Footer erstellt.

```

 Document doc = new Document();

 // Create a header and append a paragraph to it. The text in that paragraph
 // will appear at the top of every page of this section, above the main body text.
 HeaderFooter header = new HeaderFooter(doc, HeaderFooterType.HEADER_PRIMARY);
 doc.getFirstSection().getHeadersFooters().add(header);

 Paragraph para = header.appendParagraph("My header.");

 Assert.assertTrue(header.isHeader());
 Assert.assertTrue(para.isEndOfHeaderFooter());

 // Create a footer and append a paragraph to it. The text in that paragraph
 // will appear at the bottom of every page of this section, below the main body text.
 HeaderFooter footer = new HeaderFooter(doc, HeaderFooterType.FOOTER_PRIMARY);
 doc.getFirstSection().getHeadersFooters().add(footer);

 para = footer.appendParagraph("My footer.");

 Assert.assertFalse(footer.isHeader());
 Assert.assertTrue(para.isEndOfHeaderFooter());

 Assert.assertEquals(para.getParentStory(), footer);
 Assert.assertEquals(para.getParentSection(), footer.getParentSection());
 Assert.assertEquals(header.getParentSection(), footer.getParentSection());

 doc.save(getArtifactsDir() + "HeaderFooter.Create.docx");
 
```

**Returns:**
boolean - Der entsprechende  boolean  Wert.
### isEndOfSection() {#isEndOfSection}
```
public boolean isEndOfSection()
```


True, wenn dieser Absatz der letzte Absatz im [Body](../../com.aspose.words/body/) (Haupttext-Story) einer [Section](../../com.aspose.words/section/) ist; andernfalls false.

 **Examples:** 

Zeigt, wie der Inhalt eines Dokuments in ein Lesezeichen in einem anderen Dokument eingefügt wird.

```

 public void insertAtBookmark() throws Exception {
     Document doc = new Document();
     DocumentBuilder builder = new DocumentBuilder(doc);

     builder.startBookmark("InsertionPoint");
     builder.write("We will insert a document here: ");
     builder.endBookmark("InsertionPoint");

     Document docToInsert = new Document();
     builder = new DocumentBuilder(docToInsert);

     builder.write("Hello world!");

     docToInsert.save(getArtifactsDir() + "NodeImporter.InsertAtMergeField.docx");

     Bookmark bookmark = doc.getRange().getBookmarks().get("InsertionPoint");
     insertDocument(bookmark.getBookmarkStart().getParentNode(), docToInsert);

     Assert.assertEquals("We will insert a document here: " +
             "\rHello world!", doc.getText().trim());
 }

 /// 
 /// Inserts the contents of a document after the specified node.
 /// 
 static void insertDocument(Node insertionDestination, Document docToInsert) {
     if (((insertionDestination.getNodeType()) == (NodeType.PARAGRAPH)) || ((insertionDestination.getNodeType()) == (NodeType.TABLE))) {
         CompositeNode destinationParent = insertionDestination.getParentNode();

         NodeImporter importer =
                 new NodeImporter(docToInsert, insertionDestination.getDocument(), ImportFormatMode.KEEP_SOURCE_FORMATTING);

         // Loop through all block-level nodes in the section's body,
         // then clone and insert every node that is not the last empty paragraph of a section.
         for (Section srcSection : docToInsert.getSections())
             for (Node srcNode : srcSection.getBody()) {
                 if (((srcNode.getNodeType()) == (NodeType.PARAGRAPH))) {
                     Paragraph para = (Paragraph) srcNode;
                     if (para.isEndOfSection() && !para.hasChildNodes())
                         continue;
                 }

                 Node newNode = importer.importNode(srcNode, true);

                 destinationParent.insertAfter(newNode, insertionDestination);
                 insertionDestination = newNode;
             }
     } else {
         throw new IllegalArgumentException("The destination node should be either a paragraph or table.");
     }
 }
 
```

**Returns:**
boolean - Der entsprechende  boolean  Wert.
### isFormatRevision() {#isFormatRevision}
```
public boolean isFormatRevision()
```


Gibt true zurück, wenn die Formatierung des Objekts in Microsoft Word geändert wurde, während die Änderungsverfolgung aktiviert war.

 **Examples:** 

Zeigt, wie man prüft, ob ein Absatz eine Formatrevision ist.

```

 Document doc = new Document(getMyDir() + "Format revision.docx");

 // This paragraph is a "Format" revision, which occurs when we change the formatting of existing text
 // while tracking revisions in Microsoft Word via "Review" -> "Track changes".
 Assert.assertTrue(doc.getFirstSection().getBody().getFirstParagraph().isFormatRevision());
 
```

**Returns:**
boolean - True, wenn die Formatierung des Objekts in Microsoft Word geändert wurde, während die Änderungsverfolgung aktiviert war.
### isInCell() {#isInCell}
```
public boolean isInCell()
```


True, wenn dieser Absatz ein unmittelbares Kind einer [Cell](../../com.aspose.words/cell/) ist; andernfalls false.

 **Examples:** 

Zeigt, wie man eine Tabelle so einstellt, dass sie auf derselben Seite zusammenbleibt.

```

 Document doc = new Document(getMyDir() + "Table spanning two pages.docx");
 Table table = doc.getFirstSection().getBody().getTables().get(0);

 // Enabling KeepWithNext for every paragraph in the table except for the
 // last ones in the last row will prevent the table from splitting across multiple pages.
 for (Cell cell : (Iterable) table.getChildNodes(NodeType.CELL, true))
     for (Paragraph para : cell.getParagraphs()) {
         Assert.assertTrue(para.isInCell());

         if (!(cell.getParentRow().isLastRow() && para.isEndOfCell()))
             para.getParagraphFormat().setKeepWithNext(true);
     }

 doc.save(getArtifactsDir() + "Table.KeepTableTogether.docx");
 
```

**Returns:**
boolean - Der entsprechende  boolean  Wert.
### isInsertRevision() {#isInsertRevision}
```
public boolean isInsertRevision()
```


Gibt true zurück, wenn dieses Objekt in Microsoft Word eingefügt wurde, während die Änderungsverfolgung aktiviert war.

 **Examples:** 

Zeigt, wie man mit Revisionsabsätzen arbeitet.

```

 Document doc = new Document();
 Body body = doc.getFirstSection().getBody();
 Paragraph para = body.getFirstParagraph();

 para.appendChild(new Run(doc, "Paragraph 1. "));
 body.appendParagraph("Paragraph 2. ");
 body.appendParagraph("Paragraph 3. ");

 // The above paragraphs are not revisions.
 // Paragraphs that we add after starting revision tracking will register as "Insert" revisions.
 doc.startTrackRevisions("John Doe", new Date());

 para = body.appendParagraph("Paragraph 4. ");

 Assert.assertTrue(para.isInsertRevision());

 // Paragraphs that we remove after starting revision tracking will register as "Delete" revisions.
 ParagraphCollection paragraphs = body.getParagraphs();

 Assert.assertEquals(4, paragraphs.getCount());

 para = paragraphs.get(2);
 para.remove();

 // Such paragraphs will remain until we either accept or reject the delete revision.
 // Accepting the revision will remove the paragraph for good,
 // and rejecting the revision will leave it in the document as if we never deleted it.
 Assert.assertEquals(4, paragraphs.getCount());
 Assert.assertTrue(para.isDeleteRevision());

 // Accept the revision, and then verify that the paragraph is gone.
 doc.acceptAllRevisions();

 Assert.assertEquals(paragraphs.getCount(), 3);
 Assert.assertEquals(para.getCount(), 0);
 Assert.assertEquals(
         "Paragraph 1. \r" +
                 "Paragraph 2. \r" +
                 "Paragraph 4.", doc.getText().trim());
 
```

**Returns:**
boolean - True, wenn dieses Objekt in Microsoft Word eingefügt wurde, während die Änderungsverfolgung aktiviert war.
### isListItem() {#isListItem}
```
public boolean isListItem()
```


True, wenn der Absatz ein Element in einer Aufzählungs- oder nummerierten Liste in der Originalrevision ist.

 **Examples:** 

Zeigt, wie man eine Liste in einer anderen Liste verschachtelt.

```

 Document doc = new Document();
 DocumentBuilder builder = new DocumentBuilder(doc);

 // A list allows us to organize and decorate sets of paragraphs with prefix symbols and indents.
 // We can create nested lists by increasing the indent level.
 // We can begin and end a list by using a document builder's "ListFormat" property.
 // Each paragraph that we add between a list's start and the end will become an item in the list.
 // Create an outline list for the headings.
 List outlineList = doc.getLists().add(ListTemplate.OUTLINE_NUMBERS);
 builder.getListFormat().setList(outlineList);
 builder.getParagraphFormat().setStyleIdentifier(StyleIdentifier.HEADING_1);
 builder.writeln("This is my Chapter 1");

 // Create a numbered list.
 List numberedList = doc.getLists().add(ListTemplate.NUMBER_DEFAULT);
 builder.getListFormat().setList(numberedList);
 builder.getParagraphFormat().setStyleIdentifier(StyleIdentifier.NORMAL);
 builder.writeln("Numbered list item 1.");

 // Every paragraph that comprises a list will have this flag.
 Assert.assertTrue(builder.getCurrentParagraph().isListItem());
 Assert.assertTrue(builder.getParagraphFormat().isListItem());

 // Create a bulleted list.
 List bulletedList = doc.getLists().add(ListTemplate.BULLET_DEFAULT);
 builder.getListFormat().setList(bulletedList);
 builder.getParagraphFormat().setLeftIndent(72.0);
 builder.writeln("Bulleted list item 1.");
 builder.writeln("Bulleted list item 2.");
 builder.getParagraphFormat().clearFormatting();

 // Revert to the numbered list.
 builder.getListFormat().setList(numberedList);
 builder.writeln("Numbered list item 2.");
 builder.writeln("Numbered list item 3.");

 // Revert to the outline list.
 builder.getListFormat().setList(outlineList);
 builder.getParagraphFormat().setStyleIdentifier(StyleIdentifier.HEADING_1);
 builder.writeln("This is my Chapter 2");

 builder.getParagraphFormat().clearFormatting();

 builder.getDocument().save(getArtifactsDir() + "Lists.NestedLists.docx");
 
```

**Returns:**
boolean - Der entsprechende  boolean  Wert.
### isMoveFromRevision() {#isMoveFromRevision}
```
public boolean isMoveFromRevision()
```


Gibt  true  zurück, wenn dieses Objekt in Microsoft Word verschoben (gelöscht) wurde, während die Änderungsverfolgung aktiviert war.

 **Examples:** 

Zeigt, wie geprüft wird, ob ein Absatz eine Verschiebungsrevision ist.

```

 Document doc = new Document(getMyDir() + "Revisions.docx");

 // This document contains "Move" revisions, which appear when we highlight text with the cursor,
 // and then drag it to move it to another location
 // while tracking revisions in Microsoft Word via "Review" -> "Track changes".
 Assert.assertEquals(6, IterableUtils.countMatches(doc.getRevisions(), r -> r.getRevisionType() == RevisionType.MOVING));

 ParagraphCollection paragraphs = doc.getFirstSection().getBody().getParagraphs();

 // Move revisions consist of pairs of "Move from", and "Move to" revisions.
 // These revisions are potential changes to the document that we can either accept or reject.
 // Before we accept/reject a move revision, the document
 // must keep track of both the departure and arrival destinations of the text.
 // The second and the fourth paragraph define one such revision, and thus both have the same contents.
 Assert.assertEquals(paragraphs.get(1).getText(), paragraphs.get(3).getText());

 // The "Move from" revision is the paragraph where we dragged the text from.
 // If we accept the revision, this paragraph will disappear,
 // and the other will remain and no longer be a revision.
 Assert.assertTrue(paragraphs.get(1).isMoveFromRevision());

 // The "Move to" revision is the paragraph where we dragged the text to.
 // If we reject the revision, this paragraph instead will disappear, and the other will remain.
 Assert.assertTrue(paragraphs.get(3).isMoveToRevision());
 
```

**Returns:**
boolean -  true  wenn dieses Objekt in Microsoft Word verschoben (gelöscht) wurde, während die Änderungsverfolgung aktiviert war.
### isMoveToRevision() {#isMoveToRevision}
```
public boolean isMoveToRevision()
```


Gibt  true  zurück, wenn dieses Objekt in Microsoft Word verschoben (eingefügt) wurde, während die Änderungsverfolgung aktiviert war.

 **Examples:** 

Zeigt, wie geprüft wird, ob ein Absatz eine Verschiebungsrevision ist.

```

 Document doc = new Document(getMyDir() + "Revisions.docx");

 // This document contains "Move" revisions, which appear when we highlight text with the cursor,
 // and then drag it to move it to another location
 // while tracking revisions in Microsoft Word via "Review" -> "Track changes".
 Assert.assertEquals(6, IterableUtils.countMatches(doc.getRevisions(), r -> r.getRevisionType() == RevisionType.MOVING));

 ParagraphCollection paragraphs = doc.getFirstSection().getBody().getParagraphs();

 // Move revisions consist of pairs of "Move from", and "Move to" revisions.
 // These revisions are potential changes to the document that we can either accept or reject.
 // Before we accept/reject a move revision, the document
 // must keep track of both the departure and arrival destinations of the text.
 // The second and the fourth paragraph define one such revision, and thus both have the same contents.
 Assert.assertEquals(paragraphs.get(1).getText(), paragraphs.get(3).getText());

 // The "Move from" revision is the paragraph where we dragged the text from.
 // If we accept the revision, this paragraph will disappear,
 // and the other will remain and no longer be a revision.
 Assert.assertTrue(paragraphs.get(1).isMoveFromRevision());

 // The "Move to" revision is the paragraph where we dragged the text to.
 // If we reject the revision, this paragraph instead will disappear, and the other will remain.
 Assert.assertTrue(paragraphs.get(3).isMoveToRevision());
 
```

**Returns:**
boolean -  true  wenn dieses Objekt in Microsoft Word verschoben (eingefügt) wurde, während die Änderungsverfolgung aktiviert war.
### iterator() {#iterator}
```
public Iterator iterator()
```


Bietet Unterstützung für die foreach‑artige Iteration über die Kindknoten dieses Knotens.

 **Examples:** 

Zeigt, wie man alle Kommentare eines Dokuments und deren Antworten ausdruckt.

```

 Document doc = new Document(getMyDir() + "Comments.docx");

 NodeCollection comments = doc.getChildNodes(NodeType.COMMENT, true);
 // If a comment has no ancestor, it is a "top-level" comment as opposed to a reply-type comment.
 // Print all top-level comments along with any replies they may have.
 for (Comment comment : (Iterable) comments) {
     if (comment.getAncestor() == null) {
         System.out.println("Top-level comment:");
         System.out.println("\t\"{comment.GetText().Trim()}\", by {comment.Author}");
         System.out.println("Has {comment.Replies.Count} replies");
         for (Comment commentReply : comment.getReplies()) {
             System.out.println("\t\"{commentReply.GetText().Trim()}\", by {commentReply.Author}");
         }
         System.out.println();
     }
 }
 
```

**Returns:**
java.util.Iterator
### joinRunsWithSameFormatting() {#joinRunsWithSameFormatting}
```
public int joinRunsWithSameFormatting()
```


Verbindet Laufabschnitte mit derselben Formatierung im Absatz.

 **Examples:** 

Zeigt, wie man Absätze vereinfacht, indem überflüssige Läufe zusammengeführt werden.

```

 Document doc = new Document();
 DocumentBuilder builder = new DocumentBuilder(doc);

 // Insert four runs of text into the paragraph.
 builder.write("Run 1. ");
 builder.write("Run 2. ");
 builder.write("Run 3. ");
 builder.write("Run 4. ");

 // If we open this document in Microsoft Word, the paragraph will look like one seamless text body.
 // However, it will consist of four separate runs with the same formatting. Fragmented paragraphs like this
 // may occur when we manually edit parts of one paragraph many times in Microsoft Word.
 Paragraph para = builder.getCurrentParagraph();

 Assert.assertEquals(4, para.getRuns().getCount());

 // Change the style of the last run to set it apart from the first three.
 para.getRuns().get(3).getFont().setStyleIdentifier(StyleIdentifier.EMPHASIS);

 // We can run the "JoinRunsWithSameFormatting" method to optimize the document's contents
 // by merging similar runs into one, reducing their overall count.
 // This method also returns the number of runs that this method merged.
 // These two merges occurred to combine Runs #1, #2, and #3,
 // while leaving out Run #4 because it has an incompatible style.
 Assert.assertEquals(2, para.joinRunsWithSameFormatting());

 // The number of runs left will equal the original count
 // minus the number of run merges that the "JoinRunsWithSameFormatting" method carried out.
 Assert.assertEquals(2, para.getRuns().getCount());
 Assert.assertEquals("Run 1. Run 2. Run 3. ", para.getRuns().get(0).getText());
 Assert.assertEquals("Run 4. ", para.getRuns().get(1).getText());
 
```

**Returns:**
int - Anzahl der durchgeführten Zusammenführungen. Wenn **N** benachbarte Läufe zusammengeführt werden, zählen sie als **N - 1** Zusammenführungen.
### joinRunsWithSameFormatting(JoinRunsOptions options) {#joinRunsWithSameFormatting-com.aspose.words.JoinRunsOptions}
```
public int joinRunsWithSameFormatting(JoinRunsOptions options)
```


Verbindet Laufabschnitte mit derselben Formatierung im Absatz.

 **Examples:** 

Zeigt, wie man Runs mit derselben Formatierung zusammenführt, wobei redundante und unbedeutende Attribute ignoriert werden.

```

 Document doc = new Document();
 DocumentBuilder builder = new DocumentBuilder(doc);

 // Create runs with identical visible formatting but some internal differences.
 builder.getFont().setName("Arial");
 builder.getFont().setSize(12.0);
 builder.write("Hello ");
 builder.write("world");

 // Verify runs before join.
 Assert.assertEquals(2, doc.getFirstSection().getBody().getFirstParagraph().getRuns().getCount());
 Assert.assertEquals("Hello ", doc.getFirstSection().getBody().getFirstParagraph().getRuns().get(0).getText());
 Assert.assertEquals("world", doc.getFirstSection().getBody().getFirstParagraph().getRuns().get(1).getText());

 // Configure options to ignore redundant and insignificant attributes during join.
 JoinRunsOptions options = new JoinRunsOptions();
 options.setIgnoreRedundant(true); // Ignore redundant run properties that don't affect appearance.
 options.setIgnoreInsignificant(true); // Ignore insignificant differences like whitespace-only runs.

 // Join runs that have the same visible formatting using the extended options.
 doc.getFirstSection().getBody().getFirstParagraph().joinRunsWithSameFormatting(options);

 // Verify that runs were successfully joined.
 Assert.assertEquals(1, doc.getFirstSection().getBody().getFirstParagraph().getRuns().getCount());
 Assert.assertEquals("Hello world", doc.getFirstSection().getBody().getFirstParagraph().getRuns().get(0).getText());

 doc.save(getArtifactsDir() + "Paragraph.JoinRunsWithSameFormattingWithOptions.docx");
 
```

**Parameters:**
| Parameter | Typ | Beschreibung |
| --- | --- | --- |
| options | [JoinRunsOptions](../../com.aspose.words/joinrunsoptions/) | Zusätzliche Optionen |

**Returns:**
int - Anzahl der durchgeführten Zusammenführungen. Wenn **N** benachbarte Läufe zusammengeführt werden, zählen sie als **N - 1** Zusammenführungen.
### nextPreOrder(Node rootNode) {#nextPreOrder-com.aspose.words.Node}
```
public Node nextPreOrder(Node rootNode)
```


Ermittelt den nächsten Knoten gemäß dem Preorder-Baumdurchlauf-Algorithmus.

 **Examples:** 

Zeigt, wie man den Knotbaum des Dokuments mit dem Preorder‑Durchlaufalgorithmus durchläuft und jede gefundene Form mit einem Bild löscht.

```

 Document doc = new Document(getMyDir() + "Images.docx");
 ArrayList shapes = (ArrayList) IterableUtils.toList(doc.getChildNodes(NodeType.SHAPE, true));

 Assert.assertEquals(9, IterableUtils.countMatches(shapes, s -> {
     try {
         return s.hasImage();
     } catch (Exception e) {
         e.printStackTrace();
     }
     return false;
 }));

 Node curNode = doc;
 while (curNode != null) {
     Node nextNode = curNode.nextPreOrder(doc);

     if (curNode.previousPreOrder(doc) != null && nextNode != null)
         Assert.assertEquals(curNode, nextNode.previousPreOrder(doc));

     if (curNode.getNodeType() == NodeType.SHAPE && ((Shape) curNode).hasImage())
         curNode.remove();

     curNode = nextNode;
 }

 shapes = (ArrayList) IterableUtils.toList(doc.getChildNodes(NodeType.SHAPE, true));

 Assert.assertEquals(0, IterableUtils.countMatches(shapes, s -> {
     try {
         return s.hasImage();
     } catch (Exception e) {
         e.printStackTrace();
     }
     return false;
 }));
 
```

**Parameters:**
| Parameter | Typ | Beschreibung |
| --- | --- | --- |
| rootNode | [Node](../../com.aspose.words/node/) | Der oberste Knoten (Grenze) des Durchlaufs. |

**Returns:**
[Node](../../com.aspose.words/node/) - Next node in pre-order order. Null if reached the  rootNode .
### nodeTypeToString(int nodeType) {#nodeTypeToString-int}
```
public static String nodeTypeToString(int nodeType)
```




**Parameters:**
| Parameter | Typ | Beschreibung |
| --- | --- | --- |
| nodeType | int |  |

**Returns:**
java.lang.String
### prependChild(Node newChild) {#prependChild-com.aspose.words.Node}
```
public Node prependChild(Node newChild)
```


Fügt den angegebenen Knoten am Anfang der Liste der Kindknoten dieses Knotens hinzu.

 **Remarks:** 

Wenn der  newChild  bereits im Baum ist, wird er zuerst entfernt.

Wenn der einzufügende Knoten aus einem anderen Dokument erstellt wurde, sollten Sie **M:Aspose.Words.DocumentBase.ImportNode(Aspose.Words.Node,System.Boolean,Aspose.Words.ImportFormatMode)** verwenden, um den Knoten in das aktuelle Dokument zu importieren. Der importierte Knoten kann dann in das aktuelle Dokument eingefügt werden.

 **Examples:** 

Zeigt, wie man Kindknoten in der Sammlung von Kindknoten eines CompositeNode hinzufügt, aktualisiert und löscht.

```

 Document doc = new Document();

 // An empty document, by default, has one paragraph.
 Assert.assertEquals(1, doc.getFirstSection().getBody().getParagraphs().getCount());

 // Composite nodes such as our paragraph can contain other composite and inline nodes as children.
 Paragraph paragraph = doc.getFirstSection().getBody().getFirstParagraph();
 Run paragraphText = new Run(doc, "Initial text. ");
 paragraph.appendChild(paragraphText);

 // Create three more run nodes.
 Run run1 = new Run(doc, "Run 1. ");
 Run run2 = new Run(doc, "Run 2. ");
 Run run3 = new Run(doc, "Run 3. ");

 // The document body will not display these runs until we insert them into a composite node
 // that itself is a part of the document's node tree, as we did with the first run.
 // We can determine where the text contents of nodes that we insert
 // appears in the document by specifying an insertion location relative to another node in the paragraph.
 Assert.assertEquals("Initial text.", paragraph.getText().trim());

 // Insert the second run into the paragraph in front of the initial run.
 paragraph.insertBefore(run2, paragraphText);

 Assert.assertEquals("Run 2. Initial text.", paragraph.getText().trim());

 // Insert the third run after the initial run.
 paragraph.insertAfter(run3, paragraphText);

 Assert.assertEquals("Run 2. Initial text. Run 3.", paragraph.getText().trim());

 // Insert the first run to the start of the paragraph's child nodes collection.
 paragraph.prependChild(run1);

 Assert.assertEquals("Run 1. Run 2. Initial text. Run 3.", paragraph.getText().trim());
 Assert.assertEquals(4, paragraph.getChildNodes(NodeType.ANY, true).getCount());

 // We can modify the contents of the run by editing and deleting existing child nodes.
 ((Run) paragraph.getChildNodes(NodeType.RUN, true).get(1)).setText("Updated run 2. ");
 paragraph.getChildNodes(NodeType.RUN, true).remove(paragraphText);

 Assert.assertEquals("Run 1. Updated run 2. Run 3.", paragraph.getText().trim());
 Assert.assertEquals(3, paragraph.getChildNodes(NodeType.ANY, true).getCount());
 
```

**Parameters:**
| Parameter | Typ | Beschreibung |
| --- | --- | --- |
| newChild | [Node](../../com.aspose.words/node/) | Der hinzuzufügende Knoten. |

**Returns:**
[Node](../../com.aspose.words/node/) - The node added.
### previousPreOrder(Node rootNode) {#previousPreOrder-com.aspose.words.Node}
```
public Node previousPreOrder(Node rootNode)
```


Ermittelt den vorherigen Knoten gemäß dem Preorder-Baumdurchlauf-Algorithmus.

 **Examples:** 

Zeigt, wie man den Knotbaum des Dokuments mit dem Preorder‑Durchlaufalgorithmus durchläuft und jede gefundene Form mit einem Bild löscht.

```

 Document doc = new Document(getMyDir() + "Images.docx");
 ArrayList shapes = (ArrayList) IterableUtils.toList(doc.getChildNodes(NodeType.SHAPE, true));

 Assert.assertEquals(9, IterableUtils.countMatches(shapes, s -> {
     try {
         return s.hasImage();
     } catch (Exception e) {
         e.printStackTrace();
     }
     return false;
 }));

 Node curNode = doc;
 while (curNode != null) {
     Node nextNode = curNode.nextPreOrder(doc);

     if (curNode.previousPreOrder(doc) != null && nextNode != null)
         Assert.assertEquals(curNode, nextNode.previousPreOrder(doc));

     if (curNode.getNodeType() == NodeType.SHAPE && ((Shape) curNode).hasImage())
         curNode.remove();

     curNode = nextNode;
 }

 shapes = (ArrayList) IterableUtils.toList(doc.getChildNodes(NodeType.SHAPE, true));

 Assert.assertEquals(0, IterableUtils.countMatches(shapes, s -> {
     try {
         return s.hasImage();
     } catch (Exception e) {
         e.printStackTrace();
     }
     return false;
 }));
 
```

**Parameters:**
| Parameter | Typ | Beschreibung |
| --- | --- | --- |
| rootNode | [Node](../../com.aspose.words/node/) | Der oberste Knoten (Grenze) des Durchlaufs. |

**Returns:**
[Node](../../com.aspose.words/node/) - Previous node in pre-order order. Null if reached the  rootNode .
### remove() {#remove}
```
public void remove()
```


Entfernt sich selbst vom übergeordneten Element.

 **Examples:** 

Zeigt, wie man alle Formen mit Bildern aus einem Dokument löscht.

```

 Document doc = new Document(getMyDir() + "Images.docx");
 ArrayList shapes = (ArrayList) IterableUtils.toList(doc.getChildNodes(NodeType.SHAPE, true));

 Assert.assertEquals(9, IterableUtils.countMatches(shapes, s -> {
     try {
         return s.hasImage();
     } catch (Exception e) {
         e.printStackTrace();
     }
     return false;
 }));

 for (Shape shape : shapes)
     if (shape.hasImage())
         shape.remove();

 shapes = (ArrayList) IterableUtils.toList(doc.getChildNodes(NodeType.SHAPE, true));

 Assert.assertEquals(0, IterableUtils.countMatches(shapes, s -> {
     try {
         return s.hasImage();
     } catch (Exception e) {
         e.printStackTrace();
     }
     return false;
 }));
 
```

Zeigt, wie man alle Kindknoten eines bestimmten Typs aus einem zusammengesetzten Knoten entfernt.

```

 Document doc = new Document(getMyDir() + "Tables.docx");

 Assert.assertEquals(2, doc.getChildNodes(NodeType.TABLE, true).getCount());

 Node curNode = doc.getFirstSection().getBody().getFirstChild();

 while (curNode != null) {
     // Save the next sibling node as a variable in case we want to move to it after deleting this node.
     Node nextNode = curNode.getNextSibling();

     // A section body can contain Paragraph and Table nodes.
     // If the node is a Table, remove it from the parent.
     if (curNode.getNodeType() == NodeType.TABLE) {
         curNode.remove();
     }

     curNode = nextNode;
 }

 Assert.assertEquals(0, doc.getChildNodes(NodeType.TABLE, true).getCount());
 
```

### removeAllChildren() {#removeAllChildren}
```
public void removeAllChildren()
```


Entfernt alle Kindknoten des aktuellen Knotens.

 **Examples:** 

Zeigt, wie man ein Aspose.Words-Dokument von Hand erstellt.

```

 Document doc = new Document();

 // A blank document contains one section, one body and one paragraph.
 // Call the "RemoveAllChildren" method to remove all those nodes,
 // and end up with a document node with no children.
 doc.removeAllChildren();

 // This document now has no composite child nodes that we can add content to.
 // If we wish to edit it, we will need to repopulate its node collection.
 // First, create a new section, and then append it as a child to the root document node.
 Section section = new Section(doc);
 doc.appendChild(section);

 // Set some page setup properties for the section.
 section.getPageSetup().setSectionStart(SectionStart.NEW_PAGE);
 section.getPageSetup().setPaperSize(PaperSize.LETTER);

 // A section needs a body, which will contain and display all its contents
 // on the page between the section's header and footer.
 Body body = new Body(doc);
 section.appendChild(body);

 // Create a paragraph, set some formatting properties, and then append it as a child to the body.
 Paragraph para = new Paragraph(doc);

 para.getParagraphFormat().setStyleName("Heading 1");
 para.getParagraphFormat().setAlignment(ParagraphAlignment.CENTER);

 body.appendChild(para);

 // Finally, add some content to do the document. Create a run,
 // set its appearance and contents, and then append it as a child to the paragraph.
 Run run = new Run(doc);
 run.setText("Hello World!");
 run.getFont().setColor(Color.RED);
 para.appendChild(run);

 Assert.assertEquals("Hello World!", doc.getText().trim());

 doc.save(getArtifactsDir() + "Section.CreateManually.docx");
 
```

### removeChild(Node oldChild) {#removeChild-com.aspose.words.Node}
```
public Node removeChild(Node oldChild)
```


Entfernt den angegebenen Kindknoten.

 **Remarks:** 

Das übergeordnete Element von  oldChild  wird nach dem Entfernen des Knotens auf  null  gesetzt.

 **Examples:** 

Zeigt, wie man Methoden von Node und CompositeNode verwendet, um einen Abschnitt vor dem letzten Abschnitt im Dokument zu entfernen.

```

 Document doc = new Document();
 DocumentBuilder builder = new DocumentBuilder(doc);

 builder.writeln("Section 1 text.");
 builder.insertBreak(BreakType.SECTION_BREAK_CONTINUOUS);
 builder.writeln("Section 2 text.");

 // Both sections are siblings of each other.
 Section lastSection = (Section) doc.getLastChild();
 Section firstSection = (Section) lastSection.getPreviousSibling();

 // Remove a section based on its sibling relationship with another section.
 if (lastSection.getPreviousSibling() != null)
     doc.removeChild(firstSection);

 // The section we removed was the first one, leaving the document with only the second.
 Assert.assertEquals("Section 2 text.", doc.getText().trim());
 
```

**Parameters:**
| Parameter | Typ | Beschreibung |
| --- | --- | --- |
| oldChild | [Node](../../com.aspose.words/node/) | Der zu entfernende Knoten. |

**Returns:**
[Node](../../com.aspose.words/node/) - The removed node.
### removeMoveRevisions() {#removeMoveRevisions}
```
public void removeMoveRevisions()
```




### removeParaAttr(int key) {#removeParaAttr-int}
```
public void removeParaAttr(int key)
```




**Parameters:**
| Parameter | Typ | Beschreibung |
| --- | --- | --- |
| key | int |  |

### removeRunAttr(int key) {#removeRunAttr-int}
```
public void removeRunAttr(int key)
```




**Parameters:**
| Parameter | Typ | Beschreibung |
| --- | --- | --- |
| key | int |  |

### removeSmartTags() {#removeSmartTags}
```
public void removeSmartTags()
```


Entfernt alle [SmartTag](../../com.aspose.words/smarttag/) Nachfahrenknoten des aktuellen Knotens.

 **Remarks:** 

Diese Methode entfernt nicht den Inhalt der SmartTags.

 **Examples:** 

Entfernt alle SmartTags aus den Nachfolgerknoten eines zusammengesetzten Knotens.

```

 Document doc = new Document(getMyDir() + "Smart tags.doc");

 Assert.assertEquals(8, doc.getChildNodes(NodeType.SMART_TAG, true).getCount());

 doc.removeSmartTags();

 Assert.assertEquals(0, doc.getChildNodes(NodeType.SMART_TAG, true).getCount());
 
```

Zeigt, wie man Smart Tags erstellt.

```

 public void create() throws Exception {
     Document doc = new Document();

     // A smart tag appears in a document with Microsoft Word recognizes a part of its text as some form of data,
     // such as a name, date, or address, and converts it to a hyperlink that displays a purple dotted underline.
     SmartTag smartTag = new SmartTag(doc);

     // Smart tags are composite nodes that contain their recognized text in its entirety.
     // Add contents to this smart tag manually.
     smartTag.appendChild(new Run(doc, "May 29, 2019"));

     // Microsoft Word may recognize the above contents as being a date.
     // Smart tags use the "Element" property to reflect the type of data they contain.
     smartTag.setElement("date");

     // Some smart tag types process their contents further into custom XML properties.
     smartTag.getProperties().add(new CustomXmlProperty("Day", "", "29"));
     smartTag.getProperties().add(new CustomXmlProperty("Month", "", "5"));
     smartTag.getProperties().add(new CustomXmlProperty("Year", "", "2019"));

     // Set the smart tag's URI to the default value.
     smartTag.setUri("urn:schemas-microsoft-com:office:smarttags");

     doc.getFirstSection().getBody().getFirstParagraph().appendChild(smartTag);
     doc.getFirstSection().getBody().getFirstParagraph().appendChild(new Run(doc, " is a date. "));

     // Create another smart tag for a stock ticker.
     smartTag = new SmartTag(doc);
     smartTag.setElement("stockticker");
     smartTag.setUri("urn:schemas-microsoft-com:office:smarttags");

     smartTag.appendChild(new Run(doc, "MSFT"));

     doc.getFirstSection().getBody().getFirstParagraph().appendChild(smartTag);
     doc.getFirstSection().getBody().getFirstParagraph().appendChild(new Run(doc, " is a stock ticker."));

     // Print all the smart tags in our document using a document visitor.
     doc.accept(new SmartTagPrinter());

     // Older versions of Microsoft Word support smart tags.
     doc.save(getArtifactsDir() + "SmartTag.Create.doc");

     // Use the "RemoveSmartTags" method to remove all smart tags from a document.
     Assert.assertEquals(2, doc.getChildNodes(NodeType.SMART_TAG, true).getCount());

     doc.removeSmartTags();

     Assert.assertEquals(0, doc.getChildNodes(NodeType.SMART_TAG, true).getCount());
 }

 /// 
 /// Prints visited smart tags and their contents.
 /// 
 private static class SmartTagPrinter extends DocumentVisitor {
     /// 
     /// Called when a SmartTag node is encountered in the document.
     /// 
     public int visitSmartTagStart(SmartTag smartTag) {
         System.out.println("Smart tag type: {smartTag.Element}");
         return VisitorAction.CONTINUE;
     }

     /// 
     /// Called when the visiting of a SmartTag node is ended.
     /// 
     public int visitSmartTagEnd(SmartTag smartTag) {
         System.out.println("\tContents: \"{smartTag.ToString(SaveFormat.Text)}\"");

         if (smartTag.getProperties().getCount() == 0) {
             System.out.println("\tContains no properties");
         } else {
             System.out.println("\tProperties: ");
             String[] properties = new String[smartTag.getProperties().getCount()];
             int index = 0;

             for (CustomXmlProperty cxp : smartTag.getProperties())
                 properties[index++] = MessageFormat.format("\"{0}\" = \"{1}\"", cxp.getName(), cxp.getValue());

             System.out.println(StringUtils.join(properties, ", "));
         }

         return VisitorAction.CONTINUE;
     }
 }
 
```

### selectNodes(String xpath) {#selectNodes-java.lang.String}
```
public NodeList selectNodes(String xpath)
```


Wählt eine Liste von Knoten aus, die dem XPath-Ausdruck entsprechen.

 **Remarks:** 

Derzeit werden nur Ausdrücke mit Elementnamen unterstützt. Ausdrücke, die Attributnamen verwenden, werden nicht unterstützt.

 **Examples:** 

Zeigt, wie man bestimmte Knoten mithilfe eines XPath-Ausdrucks auswählt.

```

 Document doc = new Document(getMyDir() + "Tables.docx");

 // This expression will extract all paragraph nodes,
 // which are descendants of any table node in the document.
 NodeList nodeList = doc.selectNodes("//Table//Paragraph");

 // Iterate through the list with an enumerator and print the contents of every paragraph in each cell of the table.
 int index = 0;

 Iterator e = nodeList.iterator();
 while (e.hasNext()) {
     Node currentNode = e.next();
     System.out.println(MessageFormat.format("Table paragraph index {0}, contents: \"{1}\"", index++, currentNode.getText().trim()));
 }

 // This expression will select any paragraphs that are direct children of any Body node in the document.
 nodeList = doc.selectNodes("//Body/Paragraph");

 // We can treat the list as an array.
 Assert.assertEquals(nodeList.toArray().length, 4);

 // Use SelectSingleNode to select the first result of the same expression as above.
 Node node = doc.selectSingleNode("//Body/Paragraph");

 Assert.assertEquals(Paragraph.class, node.getClass());
 
```

Zeigt, wie man einen XPath-Ausdruck verwendet, um zu prüfen, ob ein Knoten innerhalb eines Feldes liegt.

```

 Document doc = new Document(getMyDir() + "Mail merge destination - Northwind employees.docx");

 // The NodeList that results from this XPath expression will contain all nodes we find inside a field.
 // However, FieldStart and FieldEnd nodes can be on the list if there are nested fields in the path.
 // Currently does not find rare fields in which the FieldCode or FieldResult spans across multiple paragraphs.
 NodeList resultList =
         doc.selectNodes("//FieldStart/following-sibling::node()[following-sibling::FieldEnd]");
 Run[] runs = Arrays.stream(resultList.toArray()).filter(n -> n.getNodeType() == NodeType.RUN).toArray(Run[]::new);
 Run run = runs[0];

 // Check if the specified run is one of the nodes that are inside the field.
 System.out.println(MessageFormat.format("Contents of the first Run node that''s part of a field: {0}", run.getText().trim()));
 
```

**Parameters:**
| Parameter | Typ | Beschreibung |
| --- | --- | --- |
| xpath | java.lang.String | Der XPath-Ausdruck. |

**Returns:**
[NodeList](../../com.aspose.words/nodelist/) - A list of nodes matching the XPath query.
### selectSingleNode(String xpath) {#selectSingleNode-java.lang.String}
```
public Node selectSingleNode(String xpath)
```


Wählt den ersten [Node](../../com.aspose.words/node/) aus, der dem XPath-Ausdruck entspricht.

 **Remarks:** 

Derzeit werden nur Ausdrücke mit Elementnamen unterstützt. Ausdrücke, die Attributnamen verwenden, werden nicht unterstützt.

 **Examples:** 

Zeigt, wie man bestimmte Knoten mithilfe eines XPath-Ausdrucks auswählt.

```

 Document doc = new Document(getMyDir() + "Tables.docx");

 // This expression will extract all paragraph nodes,
 // which are descendants of any table node in the document.
 NodeList nodeList = doc.selectNodes("//Table//Paragraph");

 // Iterate through the list with an enumerator and print the contents of every paragraph in each cell of the table.
 int index = 0;

 Iterator e = nodeList.iterator();
 while (e.hasNext()) {
     Node currentNode = e.next();
     System.out.println(MessageFormat.format("Table paragraph index {0}, contents: \"{1}\"", index++, currentNode.getText().trim()));
 }

 // This expression will select any paragraphs that are direct children of any Body node in the document.
 nodeList = doc.selectNodes("//Body/Paragraph");

 // We can treat the list as an array.
 Assert.assertEquals(nodeList.toArray().length, 4);

 // Use SelectSingleNode to select the first result of the same expression as above.
 Node node = doc.selectSingleNode("//Body/Paragraph");

 Assert.assertEquals(Paragraph.class, node.getClass());
 
```

**Parameters:**
| Parameter | Typ | Beschreibung |
| --- | --- | --- |
| xpath | java.lang.String | Der XPath-Ausdruck. |

**Returns:**
[Node](../../com.aspose.words/node/) - The first [Node](../../com.aspose.words/node/) that matches the XPath query or  null  if no matching node is found.
### setCustomNodeId(int value) {#setCustomNodeId-int}
```
public void setCustomNodeId(int value)
```


Gibt eine benutzerdefinierte Knotenkennung an.

 **Remarks:** 

Standardwert ist 0.

Dieser Bezeichner kann beliebig gesetzt und verwendet werden. Zum Beispiel als Schlüssel, um externe Daten abzurufen.

Wichtiger Hinweis: Der angegebene Wert wird nicht in einer Ausgabedatei gespeichert und existiert nur während der Lebensdauer des Knotens.

 **Examples:** 

Zeigt, wie man die Sammlung von Kindknoten eines zusammengesetzten Knotens durchläuft.

```

 Document doc = new Document();

 // Add two runs and one shape as child nodes to the first paragraph of this document.
 Paragraph paragraph = (Paragraph) doc.getChild(NodeType.PARAGRAPH, 0, true);
 paragraph.appendChild(new Run(doc, "Hello world! "));

 Shape shape = new Shape(doc, ShapeType.RECTANGLE);
 shape.setWidth(200.0);
 shape.setHeight(200.0);
 // Note that the 'CustomNodeId' is not saved to an output file and exists only during the node lifetime.
 shape.setCustomNodeId(100);
 shape.setWrapType(WrapType.INLINE);
 paragraph.appendChild(shape);

 paragraph.appendChild(new Run(doc, "Hello again!"));

 // Iterate through the paragraph's collection of immediate children,
 // and print any runs or shapes that we find within.
 NodeCollection children = paragraph.getChildNodes(NodeType.ANY, false);

 Assert.assertEquals(3, paragraph.getChildNodes(NodeType.ANY, false).getCount());

 for (Node child : (Iterable) children)
     switch (child.getNodeType()) {
         case NodeType.RUN:
             System.out.println("Run contents:");
             System.out.println(MessageFormat.format("\t\"{0}\"", child.getText().trim()));
             break;
         case NodeType.SHAPE:
             Shape childShape = (Shape)child;
             System.out.println("Shape:");
             System.out.println(MessageFormat.format("\t{0}, {1}x{2}", childShape.getShapeType(), childShape.getWidth(), childShape.getHeight()));
             break;
     }
 
```

**Parameters:**
| Parameter | Typ | Beschreibung |
| --- | --- | --- |
| Wert | int | Der entsprechende  int  Wert. |

### setParaAttr(int key, Object value) {#setParaAttr-int-java.lang.Object}
```
public void setParaAttr(int key, Object value)
```




**Parameters:**
| Parameter | Typ | Beschreibung |
| --- | --- | --- |
| key | int |  |
| Wert | java.lang.Object |  |

### setRunAttr(int key, Object value) {#setRunAttr-int-java.lang.Object}
```
public void setRunAttr(int key, Object value)
```




**Parameters:**
| Parameter | Typ | Beschreibung |
| --- | --- | --- |
| key | int |  |
| Wert | java.lang.Object |  |

### toString() {#toString}
```
public String toString()
```




**Returns:**
java.lang.String
### toString(SaveOptions saveOptions) {#toString-com.aspose.words.SaveOptions}
```
public String toString(SaveOptions saveOptions)
```


Exportiert den Inhalt des Knotens in einen String unter Verwendung der angegebenen Speicheroptionen.

 **Examples:** 

Exportiert den Inhalt eines Knotens als String im HTML-Format.

```

 Document doc = new Document(getMyDir() + "Document.docx");

 Node node = doc.getLastSection().getBody().getLastParagraph();

 // When we call the ToString method using the html SaveFormat overload,
 // it converts the node's contents to their raw html representation.
 Assert.assertEquals(" " +
         "Hello World!" +
         "", node.toString(SaveFormat.HTML));

 // We can also modify the result of this conversion using a SaveOptions object.
 HtmlSaveOptions saveOptions = new HtmlSaveOptions();
 saveOptions.setExportRelativeFontSize(true);

 Assert.assertEquals(" " +
         "Hello World!" +
         "", node.toString(saveOptions));
 
```

**Parameters:**
| Parameter | Typ | Beschreibung |
| --- | --- | --- |
| saveOptions | [SaveOptions](../../com.aspose.words/saveoptions/) | Gibt die Optionen an, die steuern, wie der Knoten gespeichert wird. |

**Returns:**
java.lang.String - Der Inhalt des Knotens im angegebenen Format.
### toString(int saveFormat) {#toString-int}
```
public String toString(int saveFormat)
```




**Parameters:**
| Parameter | Typ | Beschreibung |
| --- | --- | --- |
| saveFormat | int |  |

**Returns:**
java.lang.String
