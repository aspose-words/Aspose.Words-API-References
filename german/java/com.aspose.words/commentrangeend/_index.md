---
title: "CommentRangeEnd"
linktitle: "CommentRangeEnd"
second_title: "Aspose.Words für Java"
description: "Bezeichnet das Ende eines Textbereichs, dem in Java ein Kommentar zugeordnet ist."
type: docs
weight: 111
url: /de/java/com.aspose.words/commentrangeend/
---

**Inheritance:**
java.lang.Object, [com.aspose.words.Node](../../com.aspose.words/node/)
```
public class CommentRangeEnd extends Node
```

Bezeichnet das Ende eines Textbereichs, dem ein Kommentar zugeordnet ist.

Weitere Informationen finden Sie im Dokumentationsartikel [ Working with Comments ][Working with Comments].

 **Remarks:** 

Um einen an einen Textbereich angehefteten Kommentar zu erstellen, müssen Sie ein [Comment](../../com.aspose.words/comment/) erstellen und anschließend [CommentRangeStart](../../com.aspose.words/commentrangestart/) sowie [CommentRangeEnd](../../com.aspose.words/commentrangeend/) erzeugen und deren Kennungen auf denselben [Comment.getId()](../../com.aspose.words/comment/\#getId) / [Comment.setId(int)](../../com.aspose.words/comment/\#setId-int)-Wert setzen.

[CommentRangeEnd](../../com.aspose.words/commentrangeend/) is an inline-level node and can only be a child of [Paragraph](../../com.aspose.words/paragraph/).

 **Examples:** 

Zeigt, wie der Inhalt aller Kommentare und ihrer Kommentarbereiche mithilfe eines Dokumentbesuchers ausgegeben wird.

```

 public void createCommentsAndPrintAllInfo() throws Exception {
     Document doc = new Document();

     Comment newComment = new Comment(doc);
     {
         newComment.setAuthor("VDeryushev");
         newComment.setInitial("VD");
         newComment.setDateTime(new Date());
     }

     newComment.setText("Comment regarding text.");

     // Add text to the document, warp it in a comment range, and then add your comment.
     Paragraph para = doc.getFirstSection().getBody().getFirstParagraph();
     para.appendChild(new CommentRangeStart(doc, newComment.getId()));
     para.appendChild(new Run(doc, "Commented text."));
     para.appendChild(new CommentRangeEnd(doc, newComment.getId()));
     para.appendChild(newComment);

     // Add two replies to the comment.
     newComment.addReply("John Doe", "JD", new Date(), "New reply.");
     newComment.addReply("John Doe", "JD", new Date(), "Another reply.");

     printAllCommentInfo(doc.getChildNodes(NodeType.COMMENT, true));
 }

 /// 
 /// Iterates over every top-level comment and prints its comment range, contents, and replies.
 /// 
 private static void printAllCommentInfo(NodeCollection comments) throws Exception {
     CommentInfoPrinter commentVisitor = new CommentInfoPrinter();

     // Iterate over all top-level comments. Unlike reply-type comments, top-level comments have no ancestor.
     for (Comment comment : (Iterable) comments) {
         if (comment.getAncestor() == null) {
             // First, visit the start of the comment range.
             CommentRangeStart commentRangeStart = (CommentRangeStart) comment.getPreviousSibling().getPreviousSibling().getPreviousSibling();
             commentRangeStart.accept(commentVisitor);

             // Then, visit the comment, and any replies that it may have.
             comment.accept(commentVisitor);

             for (Comment reply : comment.getReplies())
                 reply.accept(commentVisitor);

             // Finally, visit the end of the comment range, and then print the visitor's text contents.
             CommentRangeEnd commentRangeEnd = (CommentRangeEnd) comment.getPreviousSibling();
             commentRangeEnd.accept(commentVisitor);

             System.out.println(commentVisitor.getText());
         }
     }
 }

 /// 
 /// Prints information and contents of all comments and comment ranges encountered in the document.
 /// 
 public static class CommentInfoPrinter extends DocumentVisitor {
     public CommentInfoPrinter() {
         mBuilder = new StringBuilder();
         mVisitorIsInsideComment = false;
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
     public int visitRun(Run run) {
         if (mVisitorIsInsideComment) indentAndAppendLine("[Run] \"" + run.getText() + "\"");

         return VisitorAction.CONTINUE;
     }

     /// 
     /// Called when a CommentRangeStart node is encountered in the document.
     /// 
     public int visitCommentRangeStart(CommentRangeStart commentRangeStart) {
         indentAndAppendLine("[Comment range start] ID: " + commentRangeStart.getId());
         mDocTraversalDepth++;
         mVisitorIsInsideComment = true;

         return VisitorAction.CONTINUE;
     }

     /// 
     /// Called when a CommentRangeEnd node is encountered in the document.
     /// 
     public int visitCommentRangeEnd(CommentRangeEnd commentRangeEnd) {
         mDocTraversalDepth--;
         indentAndAppendLine("[Comment range end] ID: " + commentRangeEnd.getId() + "\n");
         mVisitorIsInsideComment = false;

         return VisitorAction.CONTINUE;
     }

     /// 
     /// Called when a Comment node is encountered in the document.
     /// 
     public int visitCommentStart(Comment comment) {
         indentAndAppendLine(MessageFormat.format("[Comment start] For comment range ID {0}, By {1} on {2}", comment.getId(),
                 comment.getAuthor(), comment.getDateTime()));
         mDocTraversalDepth++;
         mVisitorIsInsideComment = true;

         return VisitorAction.CONTINUE;
     }

     /// 
     /// Called when the visiting of a Comment node is ended in the document.
     /// 
     public int visitCommentEnd(Comment comment) {
         mDocTraversalDepth--;
         indentAndAppendLine("[Comment end]");
         mVisitorIsInsideComment = false;

         return VisitorAction.CONTINUE;
     }

     /// 
     /// Append a line to the StringBuilder and indent it depending on how deep the visitor is into the document tree.
     /// 
     /// 
     private void indentAndAppendLine(String text) {
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


[Working with Comments]: https://docs.aspose.com/words/java/working-with-comments/
## Konstruktoren

| Konstruktor | Beschreibung |
| --- | --- |
| [CommentRangeEnd(DocumentBase doc, int id)](#CommentRangeEnd-com.aspose.words.DocumentBase-int) | Initialisiert eine neue Instanz dieser Klasse. |
## Methoden

| Methode | Beschreibung |
| --- | --- |
| [accept(DocumentVisitor visitor)](#accept-com.aspose.words.DocumentVisitor) | Akzeptiert einen Besucher. |
| [deepClone(boolean isCloneChildren)](#deepClone-boolean) | Erstellt ein Duplikat des Knotens. |
| [getAncestor(int ancestorType)](#getAncestor-int) |  |
| [getAncestor(Class ancestorType)](#getAncestor-java.lang.Class) | Ermittelt den ersten Vorfahren des angegebenen Objekttyps. |
| [getCustomNodeId()](#getCustomNodeId) | Gibt eine benutzerdefinierte Knotenkennung an. |
| [getDisplacedByCustomXml()](#getDisplacedByCustomXml) |  |
| [getDocument()](#getDocument) | Ermittelt das Dokument, zu dem dieser Knoten gehört. |
| [getId()](#getId) | Gibt den Bezeichner des Kommentars an, zu dem dieser Bereich verknüpft ist. |
| [getIdInternal()](#getIdInternal) |  |
| [getNextSibling()](#getNextSibling) | Ermittelt den Knoten, der unmittelbar auf diesen Knoten folgt. |
| [getNodeType()](#getNodeType) | Gibt [NodeType.COMMENT\_RANGE\_END](../../com.aspose.words/nodetype/\#COMMENT-RANGE-END) zurück. |
| [getParentIdInternal()](#getParentIdInternal) |  |
| [getParentNode()](#getParentNode) | Ermittelt den unmittelbaren übergeordneten Knoten dieses Knotens. |
| [getPreviousSibling()](#getPreviousSibling) | Ermittelt den Knoten, der unmittelbar vor diesem Knoten liegt. |
| [getRange()](#getRange) | Gibt ein [Range](../../com.aspose.words/range/)-Objekt zurück, das den Teil eines Dokuments darstellt, der in diesem Knoten enthalten ist. |
| [getText()](#getText) | Ermittelt den Text dieses Knotens und aller seiner Kinder. |
| [isComposite()](#isComposite) | Gibt  true  zurück, wenn dieser Knoten andere Knoten enthalten kann. |
| [nextPreOrder(Node rootNode)](#nextPreOrder-com.aspose.words.Node) | Ermittelt den nächsten Knoten gemäß dem Preorder-Baumdurchlauf-Algorithmus. |
| [nodeTypeToString(int nodeType)](#nodeTypeToString-int) |  |
| [previousPreOrder(Node rootNode)](#previousPreOrder-com.aspose.words.Node) | Ermittelt den vorherigen Knoten gemäß dem Preorder-Baumdurchlauf-Algorithmus. |
| [remove()](#remove) | Entfernt sich selbst vom übergeordneten Element. |
| [setCustomNodeId(int value)](#setCustomNodeId-int) | Gibt eine benutzerdefinierte Knotenkennung an. |
| [setDisplacedByCustomXml(int value)](#setDisplacedByCustomXml-int) |  |
| [setId(int value)](#setId-int) | Gibt den Bezeichner des Kommentars an, zu dem dieser Bereich verknüpft ist. |
| [setIdInternal(int value)](#setIdInternal-int) |  |
| [setParentIdInternal(int value)](#setParentIdInternal-int) |  |
| [toString()](#toString) |  |
| [toString(SaveOptions saveOptions)](#toString-com.aspose.words.SaveOptions) | Exportiert den Inhalt des Knotens in einen String unter Verwendung der angegebenen Speicheroptionen. |
| [toString(int saveFormat)](#toString-int) |  |
### CommentRangeEnd(DocumentBase doc, int id) {#CommentRangeEnd-com.aspose.words.DocumentBase-int}
```
public CommentRangeEnd(DocumentBase doc, int id)
```


Initialisiert eine neue Instanz dieser Klasse.

 **Remarks:** 

Wenn [CommentRangeEnd](../../com.aspose.words/commentrangeend/) erstellt wird, gehört es zum angegebenen Dokument, ist aber noch kein Teil des Dokuments und [Node.getParentNode()](../../com.aspose.words/node/\#getParentNode) ist null.

Um ein [CommentRangeEnd](../../com.aspose.words/commentrangeend/) an das Dokument anzuhängen, verwenden Sie InsertAfter oder InsertBefore im Absatz, in dem Sie den Kommentar einfügen möchten.

 **Examples:** 

Zeigt, wie der Inhalt aller Kommentare und ihrer Kommentarbereiche mithilfe eines Dokumentbesuchers ausgegeben wird.

```

 public void createCommentsAndPrintAllInfo() throws Exception {
     Document doc = new Document();

     Comment newComment = new Comment(doc);
     {
         newComment.setAuthor("VDeryushev");
         newComment.setInitial("VD");
         newComment.setDateTime(new Date());
     }

     newComment.setText("Comment regarding text.");

     // Add text to the document, warp it in a comment range, and then add your comment.
     Paragraph para = doc.getFirstSection().getBody().getFirstParagraph();
     para.appendChild(new CommentRangeStart(doc, newComment.getId()));
     para.appendChild(new Run(doc, "Commented text."));
     para.appendChild(new CommentRangeEnd(doc, newComment.getId()));
     para.appendChild(newComment);

     // Add two replies to the comment.
     newComment.addReply("John Doe", "JD", new Date(), "New reply.");
     newComment.addReply("John Doe", "JD", new Date(), "Another reply.");

     printAllCommentInfo(doc.getChildNodes(NodeType.COMMENT, true));
 }

 /// 
 /// Iterates over every top-level comment and prints its comment range, contents, and replies.
 /// 
 private static void printAllCommentInfo(NodeCollection comments) throws Exception {
     CommentInfoPrinter commentVisitor = new CommentInfoPrinter();

     // Iterate over all top-level comments. Unlike reply-type comments, top-level comments have no ancestor.
     for (Comment comment : (Iterable) comments) {
         if (comment.getAncestor() == null) {
             // First, visit the start of the comment range.
             CommentRangeStart commentRangeStart = (CommentRangeStart) comment.getPreviousSibling().getPreviousSibling().getPreviousSibling();
             commentRangeStart.accept(commentVisitor);

             // Then, visit the comment, and any replies that it may have.
             comment.accept(commentVisitor);

             for (Comment reply : comment.getReplies())
                 reply.accept(commentVisitor);

             // Finally, visit the end of the comment range, and then print the visitor's text contents.
             CommentRangeEnd commentRangeEnd = (CommentRangeEnd) comment.getPreviousSibling();
             commentRangeEnd.accept(commentVisitor);

             System.out.println(commentVisitor.getText());
         }
     }
 }

 /// 
 /// Prints information and contents of all comments and comment ranges encountered in the document.
 /// 
 public static class CommentInfoPrinter extends DocumentVisitor {
     public CommentInfoPrinter() {
         mBuilder = new StringBuilder();
         mVisitorIsInsideComment = false;
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
     public int visitRun(Run run) {
         if (mVisitorIsInsideComment) indentAndAppendLine("[Run] \"" + run.getText() + "\"");

         return VisitorAction.CONTINUE;
     }

     /// 
     /// Called when a CommentRangeStart node is encountered in the document.
     /// 
     public int visitCommentRangeStart(CommentRangeStart commentRangeStart) {
         indentAndAppendLine("[Comment range start] ID: " + commentRangeStart.getId());
         mDocTraversalDepth++;
         mVisitorIsInsideComment = true;

         return VisitorAction.CONTINUE;
     }

     /// 
     /// Called when a CommentRangeEnd node is encountered in the document.
     /// 
     public int visitCommentRangeEnd(CommentRangeEnd commentRangeEnd) {
         mDocTraversalDepth--;
         indentAndAppendLine("[Comment range end] ID: " + commentRangeEnd.getId() + "\n");
         mVisitorIsInsideComment = false;

         return VisitorAction.CONTINUE;
     }

     /// 
     /// Called when a Comment node is encountered in the document.
     /// 
     public int visitCommentStart(Comment comment) {
         indentAndAppendLine(MessageFormat.format("[Comment start] For comment range ID {0}, By {1} on {2}", comment.getId(),
                 comment.getAuthor(), comment.getDateTime()));
         mDocTraversalDepth++;
         mVisitorIsInsideComment = true;

         return VisitorAction.CONTINUE;
     }

     /// 
     /// Called when the visiting of a Comment node is ended in the document.
     /// 
     public int visitCommentEnd(Comment comment) {
         mDocTraversalDepth--;
         indentAndAppendLine("[Comment end]");
         mVisitorIsInsideComment = false;

         return VisitorAction.CONTINUE;
     }

     /// 
     /// Append a line to the StringBuilder and indent it depending on how deep the visitor is into the document tree.
     /// 
     /// 
     private void indentAndAppendLine(String text) {
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
| doc | [DocumentBase](../../com.aspose.words/documentbase/) | Das übergeordnete Dokument. |
| id | int | Die Kommentarkennung, mit der dieses Objekt verknüpft ist. |

### accept(DocumentVisitor visitor) {#accept-com.aspose.words.DocumentVisitor}
```
public boolean accept(DocumentVisitor visitor)
```


Akzeptiert einen Besucher.

 **Remarks:** 

Ruft [DocumentVisitor.visitCommentRangeEnd(com.aspose.words.CommentRangeEnd)](../../com.aspose.words/documentvisitor/\#visitCommentRangeEnd-com.aspose.words.CommentRangeEnd) auf.

Weitere Informationen finden Sie im Visitor-Entwurfsmuster.

 **Examples:** 

Zeigt, wie der Inhalt aller Kommentare und ihrer Kommentarbereiche mithilfe eines Dokumentbesuchers ausgegeben wird.

```

 public void createCommentsAndPrintAllInfo() throws Exception {
     Document doc = new Document();

     Comment newComment = new Comment(doc);
     {
         newComment.setAuthor("VDeryushev");
         newComment.setInitial("VD");
         newComment.setDateTime(new Date());
     }

     newComment.setText("Comment regarding text.");

     // Add text to the document, warp it in a comment range, and then add your comment.
     Paragraph para = doc.getFirstSection().getBody().getFirstParagraph();
     para.appendChild(new CommentRangeStart(doc, newComment.getId()));
     para.appendChild(new Run(doc, "Commented text."));
     para.appendChild(new CommentRangeEnd(doc, newComment.getId()));
     para.appendChild(newComment);

     // Add two replies to the comment.
     newComment.addReply("John Doe", "JD", new Date(), "New reply.");
     newComment.addReply("John Doe", "JD", new Date(), "Another reply.");

     printAllCommentInfo(doc.getChildNodes(NodeType.COMMENT, true));
 }

 /// 
 /// Iterates over every top-level comment and prints its comment range, contents, and replies.
 /// 
 private static void printAllCommentInfo(NodeCollection comments) throws Exception {
     CommentInfoPrinter commentVisitor = new CommentInfoPrinter();

     // Iterate over all top-level comments. Unlike reply-type comments, top-level comments have no ancestor.
     for (Comment comment : (Iterable) comments) {
         if (comment.getAncestor() == null) {
             // First, visit the start of the comment range.
             CommentRangeStart commentRangeStart = (CommentRangeStart) comment.getPreviousSibling().getPreviousSibling().getPreviousSibling();
             commentRangeStart.accept(commentVisitor);

             // Then, visit the comment, and any replies that it may have.
             comment.accept(commentVisitor);

             for (Comment reply : comment.getReplies())
                 reply.accept(commentVisitor);

             // Finally, visit the end of the comment range, and then print the visitor's text contents.
             CommentRangeEnd commentRangeEnd = (CommentRangeEnd) comment.getPreviousSibling();
             commentRangeEnd.accept(commentVisitor);

             System.out.println(commentVisitor.getText());
         }
     }
 }

 /// 
 /// Prints information and contents of all comments and comment ranges encountered in the document.
 /// 
 public static class CommentInfoPrinter extends DocumentVisitor {
     public CommentInfoPrinter() {
         mBuilder = new StringBuilder();
         mVisitorIsInsideComment = false;
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
     public int visitRun(Run run) {
         if (mVisitorIsInsideComment) indentAndAppendLine("[Run] \"" + run.getText() + "\"");

         return VisitorAction.CONTINUE;
     }

     /// 
     /// Called when a CommentRangeStart node is encountered in the document.
     /// 
     public int visitCommentRangeStart(CommentRangeStart commentRangeStart) {
         indentAndAppendLine("[Comment range start] ID: " + commentRangeStart.getId());
         mDocTraversalDepth++;
         mVisitorIsInsideComment = true;

         return VisitorAction.CONTINUE;
     }

     /// 
     /// Called when a CommentRangeEnd node is encountered in the document.
     /// 
     public int visitCommentRangeEnd(CommentRangeEnd commentRangeEnd) {
         mDocTraversalDepth--;
         indentAndAppendLine("[Comment range end] ID: " + commentRangeEnd.getId() + "\n");
         mVisitorIsInsideComment = false;

         return VisitorAction.CONTINUE;
     }

     /// 
     /// Called when a Comment node is encountered in the document.
     /// 
     public int visitCommentStart(Comment comment) {
         indentAndAppendLine(MessageFormat.format("[Comment start] For comment range ID {0}, By {1} on {2}", comment.getId(),
                 comment.getAuthor(), comment.getDateTime()));
         mDocTraversalDepth++;
         mVisitorIsInsideComment = true;

         return VisitorAction.CONTINUE;
     }

     /// 
     /// Called when the visiting of a Comment node is ended in the document.
     /// 
     public int visitCommentEnd(Comment comment) {
         mDocTraversalDepth--;
         indentAndAppendLine("[Comment end]");
         mVisitorIsInsideComment = false;

         return VisitorAction.CONTINUE;
     }

     /// 
     /// Append a line to the StringBuilder and indent it depending on how deep the visitor is into the document tree.
     /// 
     /// 
     private void indentAndAppendLine(String text) {
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
| visitor | [DocumentVisitor](../../com.aspose.words/documentvisitor/) | Der Besucher, der den Knoten besuchen wird. |

**Returns:**
boolean – false, falls der Besucher die Aufzählung stoppen möchte.
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
### getDisplacedByCustomXml() {#getDisplacedByCustomXml}
```
public int getDisplacedByCustomXml()
```




**Returns:**
int
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
### getId() {#getId}
```
public int getId()
```


Gibt den Bezeichner des Kommentars an, zu dem dieser Bereich verknüpft ist.

 **Examples:** 

Zeigt, wie der Inhalt aller Kommentare und ihrer Kommentarbereiche mithilfe eines Dokumentbesuchers ausgegeben wird.

```

 public void createCommentsAndPrintAllInfo() throws Exception {
     Document doc = new Document();

     Comment newComment = new Comment(doc);
     {
         newComment.setAuthor("VDeryushev");
         newComment.setInitial("VD");
         newComment.setDateTime(new Date());
     }

     newComment.setText("Comment regarding text.");

     // Add text to the document, warp it in a comment range, and then add your comment.
     Paragraph para = doc.getFirstSection().getBody().getFirstParagraph();
     para.appendChild(new CommentRangeStart(doc, newComment.getId()));
     para.appendChild(new Run(doc, "Commented text."));
     para.appendChild(new CommentRangeEnd(doc, newComment.getId()));
     para.appendChild(newComment);

     // Add two replies to the comment.
     newComment.addReply("John Doe", "JD", new Date(), "New reply.");
     newComment.addReply("John Doe", "JD", new Date(), "Another reply.");

     printAllCommentInfo(doc.getChildNodes(NodeType.COMMENT, true));
 }

 /// 
 /// Iterates over every top-level comment and prints its comment range, contents, and replies.
 /// 
 private static void printAllCommentInfo(NodeCollection comments) throws Exception {
     CommentInfoPrinter commentVisitor = new CommentInfoPrinter();

     // Iterate over all top-level comments. Unlike reply-type comments, top-level comments have no ancestor.
     for (Comment comment : (Iterable) comments) {
         if (comment.getAncestor() == null) {
             // First, visit the start of the comment range.
             CommentRangeStart commentRangeStart = (CommentRangeStart) comment.getPreviousSibling().getPreviousSibling().getPreviousSibling();
             commentRangeStart.accept(commentVisitor);

             // Then, visit the comment, and any replies that it may have.
             comment.accept(commentVisitor);

             for (Comment reply : comment.getReplies())
                 reply.accept(commentVisitor);

             // Finally, visit the end of the comment range, and then print the visitor's text contents.
             CommentRangeEnd commentRangeEnd = (CommentRangeEnd) comment.getPreviousSibling();
             commentRangeEnd.accept(commentVisitor);

             System.out.println(commentVisitor.getText());
         }
     }
 }

 /// 
 /// Prints information and contents of all comments and comment ranges encountered in the document.
 /// 
 public static class CommentInfoPrinter extends DocumentVisitor {
     public CommentInfoPrinter() {
         mBuilder = new StringBuilder();
         mVisitorIsInsideComment = false;
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
     public int visitRun(Run run) {
         if (mVisitorIsInsideComment) indentAndAppendLine("[Run] \"" + run.getText() + "\"");

         return VisitorAction.CONTINUE;
     }

     /// 
     /// Called when a CommentRangeStart node is encountered in the document.
     /// 
     public int visitCommentRangeStart(CommentRangeStart commentRangeStart) {
         indentAndAppendLine("[Comment range start] ID: " + commentRangeStart.getId());
         mDocTraversalDepth++;
         mVisitorIsInsideComment = true;

         return VisitorAction.CONTINUE;
     }

     /// 
     /// Called when a CommentRangeEnd node is encountered in the document.
     /// 
     public int visitCommentRangeEnd(CommentRangeEnd commentRangeEnd) {
         mDocTraversalDepth--;
         indentAndAppendLine("[Comment range end] ID: " + commentRangeEnd.getId() + "\n");
         mVisitorIsInsideComment = false;

         return VisitorAction.CONTINUE;
     }

     /// 
     /// Called when a Comment node is encountered in the document.
     /// 
     public int visitCommentStart(Comment comment) {
         indentAndAppendLine(MessageFormat.format("[Comment start] For comment range ID {0}, By {1} on {2}", comment.getId(),
                 comment.getAuthor(), comment.getDateTime()));
         mDocTraversalDepth++;
         mVisitorIsInsideComment = true;

         return VisitorAction.CONTINUE;
     }

     /// 
     /// Called when the visiting of a Comment node is ended in the document.
     /// 
     public int visitCommentEnd(Comment comment) {
         mDocTraversalDepth--;
         indentAndAppendLine("[Comment end]");
         mVisitorIsInsideComment = false;

         return VisitorAction.CONTINUE;
     }

     /// 
     /// Append a line to the StringBuilder and indent it depending on how deep the visitor is into the document tree.
     /// 
     /// 
     private void indentAndAppendLine(String text) {
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

**Returns:**
int - Der entsprechende int-Wert.
### getIdInternal() {#getIdInternal}
```
public int getIdInternal()
```




**Returns:**
int
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


Gibt [NodeType.COMMENT\_RANGE\_END](../../com.aspose.words/nodetype/\#COMMENT-RANGE-END) zurück.

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
int – [NodeType.COMMENT\_RANGE\_END](../../com.aspose.words/nodetype/\#COMMENT-RANGE-END). Der zurückgegebene Wert ist einer der Konstanten von [NodeType](../../com.aspose.words/nodetype/).
### getParentIdInternal() {#getParentIdInternal}
```
public int getParentIdInternal()
```




**Returns:**
int
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
### getText() {#getText}
```
public String getText()
```


Ermittelt den Text dieses Knotens und aller seiner Kinder.

 **Remarks:** 

Der zurückgegebene String enthält alle Steuer- und Sonderzeichen, wie in [ControlChar](../../com.aspose.words/controlchar/) beschrieben.

 **Examples:** 

Zeigt, wie man Steuerzeichen verwendet.

```

 Document doc = new Document();
 DocumentBuilder builder = new DocumentBuilder(doc);

 // Insert paragraphs with text with DocumentBuilder.
 builder.writeln("Hello world!");
 builder.writeln("Hello again!");

 // Converting the document to text form reveals that control characters
 // represent some of the document's structural elements, such as page breaks.
 Assert.assertEquals(MessageFormat.format("Hello world!{0}", ControlChar.CR) +
         MessageFormat.format("Hello again!{0}", ControlChar.CR) +
         ControlChar.PAGE_BREAK, doc.getText());

 // When converting a document to string form,
 // we can omit some of the control characters with the Trim method.
 Assert.assertEquals(MessageFormat.format("Hello world!{0}", ControlChar.CR) +
         "Hello again!", doc.getText().trim());
 
```

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
java.lang.String
### isComposite() {#isComposite}
```
public boolean isComposite()
```


Gibt  true  zurück, wenn dieser Knoten andere Knoten enthalten kann. (197141,6)

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
boolean -  true  wenn dieser Knoten andere Knoten enthalten kann.
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

### setDisplacedByCustomXml(int value) {#setDisplacedByCustomXml-int}
```
public void setDisplacedByCustomXml(int value)
```




**Parameters:**
| Parameter | Typ | Beschreibung |
| --- | --- | --- |
| Wert | int |  |

### setId(int value) {#setId-int}
```
public void setId(int value)
```


Gibt den Bezeichner des Kommentars an, zu dem dieser Bereich verknüpft ist.

 **Examples:** 

Zeigt, wie der Inhalt aller Kommentare und ihrer Kommentarbereiche mithilfe eines Dokumentbesuchers ausgegeben wird.

```

 public void createCommentsAndPrintAllInfo() throws Exception {
     Document doc = new Document();

     Comment newComment = new Comment(doc);
     {
         newComment.setAuthor("VDeryushev");
         newComment.setInitial("VD");
         newComment.setDateTime(new Date());
     }

     newComment.setText("Comment regarding text.");

     // Add text to the document, warp it in a comment range, and then add your comment.
     Paragraph para = doc.getFirstSection().getBody().getFirstParagraph();
     para.appendChild(new CommentRangeStart(doc, newComment.getId()));
     para.appendChild(new Run(doc, "Commented text."));
     para.appendChild(new CommentRangeEnd(doc, newComment.getId()));
     para.appendChild(newComment);

     // Add two replies to the comment.
     newComment.addReply("John Doe", "JD", new Date(), "New reply.");
     newComment.addReply("John Doe", "JD", new Date(), "Another reply.");

     printAllCommentInfo(doc.getChildNodes(NodeType.COMMENT, true));
 }

 /// 
 /// Iterates over every top-level comment and prints its comment range, contents, and replies.
 /// 
 private static void printAllCommentInfo(NodeCollection comments) throws Exception {
     CommentInfoPrinter commentVisitor = new CommentInfoPrinter();

     // Iterate over all top-level comments. Unlike reply-type comments, top-level comments have no ancestor.
     for (Comment comment : (Iterable) comments) {
         if (comment.getAncestor() == null) {
             // First, visit the start of the comment range.
             CommentRangeStart commentRangeStart = (CommentRangeStart) comment.getPreviousSibling().getPreviousSibling().getPreviousSibling();
             commentRangeStart.accept(commentVisitor);

             // Then, visit the comment, and any replies that it may have.
             comment.accept(commentVisitor);

             for (Comment reply : comment.getReplies())
                 reply.accept(commentVisitor);

             // Finally, visit the end of the comment range, and then print the visitor's text contents.
             CommentRangeEnd commentRangeEnd = (CommentRangeEnd) comment.getPreviousSibling();
             commentRangeEnd.accept(commentVisitor);

             System.out.println(commentVisitor.getText());
         }
     }
 }

 /// 
 /// Prints information and contents of all comments and comment ranges encountered in the document.
 /// 
 public static class CommentInfoPrinter extends DocumentVisitor {
     public CommentInfoPrinter() {
         mBuilder = new StringBuilder();
         mVisitorIsInsideComment = false;
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
     public int visitRun(Run run) {
         if (mVisitorIsInsideComment) indentAndAppendLine("[Run] \"" + run.getText() + "\"");

         return VisitorAction.CONTINUE;
     }

     /// 
     /// Called when a CommentRangeStart node is encountered in the document.
     /// 
     public int visitCommentRangeStart(CommentRangeStart commentRangeStart) {
         indentAndAppendLine("[Comment range start] ID: " + commentRangeStart.getId());
         mDocTraversalDepth++;
         mVisitorIsInsideComment = true;

         return VisitorAction.CONTINUE;
     }

     /// 
     /// Called when a CommentRangeEnd node is encountered in the document.
     /// 
     public int visitCommentRangeEnd(CommentRangeEnd commentRangeEnd) {
         mDocTraversalDepth--;
         indentAndAppendLine("[Comment range end] ID: " + commentRangeEnd.getId() + "\n");
         mVisitorIsInsideComment = false;

         return VisitorAction.CONTINUE;
     }

     /// 
     /// Called when a Comment node is encountered in the document.
     /// 
     public int visitCommentStart(Comment comment) {
         indentAndAppendLine(MessageFormat.format("[Comment start] For comment range ID {0}, By {1} on {2}", comment.getId(),
                 comment.getAuthor(), comment.getDateTime()));
         mDocTraversalDepth++;
         mVisitorIsInsideComment = true;

         return VisitorAction.CONTINUE;
     }

     /// 
     /// Called when the visiting of a Comment node is ended in the document.
     /// 
     public int visitCommentEnd(Comment comment) {
         mDocTraversalDepth--;
         indentAndAppendLine("[Comment end]");
         mVisitorIsInsideComment = false;

         return VisitorAction.CONTINUE;
     }

     /// 
     /// Append a line to the StringBuilder and indent it depending on how deep the visitor is into the document tree.
     /// 
     /// 
     private void indentAndAppendLine(String text) {
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
| Wert | int | Der entsprechende  int  Wert. |

### setIdInternal(int value) {#setIdInternal-int}
```
public void setIdInternal(int value)
```




**Parameters:**
| Parameter | Typ | Beschreibung |
| --- | --- | --- |
| Wert | int |  |

### setParentIdInternal(int value) {#setParentIdInternal-int}
```
public void setParentIdInternal(int value)
```




**Parameters:**
| Parameter | Typ | Beschreibung |
| --- | --- | --- |
| Wert | int |  |

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
