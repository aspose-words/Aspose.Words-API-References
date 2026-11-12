---
title: "CommentRangeEnd"
linktitle: "CommentRangeEnd"
second_title: "Aspose.Words для Java"
description: "Обозначает конец области текста, к которой привязан комментарий, в Java."
type: docs
weight: 111
url: /ru/java/com.aspose.words/commentrangeend/
---

**Inheritance:**
java.lang.Object, [com.aspose.words.Node](../../com.aspose.words/node/)
```
public class CommentRangeEnd extends Node
```

Обозначает конец области текста, к которой привязан комментарий.

Чтобы узнать больше, посетите статью документации [ Working with Comments ][Working with Comments].

 **Remarks:** 

Чтобы создать комментарий, привязанный к области текста, необходимо создать [Comment](../../com.aspose.words/comment/) и затем создать [CommentRangeStart](../../com.aspose.words/commentrangestart/) и [CommentRangeEnd](../../com.aspose.words/commentrangeend/), установив их идентификаторы в одинаковое значение, получаемое через [Comment.getId()](../../com.aspose.words/comment/\#getId) / [Comment.setId(int)](../../com.aspose.words/comment/\#setId-int).

[CommentRangeEnd](../../com.aspose.words/commentrangeend/) is an inline-level node and can only be a child of [Paragraph](../../com.aspose.words/paragraph/).

 **Examples:** 

Показывает, как вывести содержимое всех комментариев и их диапазонов комментариев с помощью посетителя документа.

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
## Конструкторы

| Конструктор | Описание |
| --- | --- |
| [CommentRangeEnd(DocumentBase doc, int id)](#CommentRangeEnd-com.aspose.words.DocumentBase-int) | Инициализирует новый экземпляр этого класса. |
## Методы

| Метод | Описание |
| --- | --- |
| [accept(DocumentVisitor visitor)](#accept-com.aspose.words.DocumentVisitor) | Принимает посетителя. |
| [deepClone(boolean isCloneChildren)](#deepClone-boolean) | Создаёт дубликат узла. |
| [getAncestor(int ancestorType)](#getAncestor-int) |  |
| [getAncestor(Class ancestorType)](#getAncestor-java.lang.Class) | Получает первого предка указанного типа объекта. |
| [getCustomNodeId()](#getCustomNodeId) | Указывает пользовательский идентификатор узла. |
| [getDisplacedByCustomXml()](#getDisplacedByCustomXml) |  |
| [getDocument()](#getDocument) | Получает документ, к которому принадлежит этот узел. |
| [getId()](#getId) | Указывает идентификатор комментария, к которому привязана эта область. |
| [getIdInternal()](#getIdInternal) |  |
| [getNextSibling()](#getNextSibling) | Получает узел, непосредственно следующий за этим узлом. |
| [getNodeType()](#getNodeType) | Возвращает [NodeType.COMMENT\_RANGE\_END](../../com.aspose.words/nodetype/\#COMMENT-RANGE-END). |
| [getParentIdInternal()](#getParentIdInternal) |  |
| [getParentNode()](#getParentNode) | Получает непосредственного родителя этого узла. |
| [getPreviousSibling()](#getPreviousSibling) | Получает узел, непосредственно предшествующий этому узлу. |
| [getRange()](#getRange) | Возвращает объект [Range](../../com.aspose.words/range/), представляющий часть документа, содержащуюся в этом узле. |
| [getText()](#getText) | Получает текст этого узла и всех его дочерних элементов. |
| [isComposite()](#isComposite) | Возвращает  true  если этот узел может содержать другие узлы. |
| [nextPreOrder(Node rootNode)](#nextPreOrder-com.aspose.words.Node) | Получает следующий узел согласно алгоритму обхода дерева в порядке предобхода. |
| [nodeTypeToString(int nodeType)](#nodeTypeToString-int) |  |
| [previousPreOrder(Node rootNode)](#previousPreOrder-com.aspose.words.Node) | Получает предыдущий узел в соответствии с алгоритмом обхода дерева в порядке предобхода. |
| [remove()](#remove) | Удаляет себя из родителя. |
| [setCustomNodeId(int value)](#setCustomNodeId-int) | Указывает пользовательский идентификатор узла. |
| [setDisplacedByCustomXml(int value)](#setDisplacedByCustomXml-int) |  |
| [setId(int value)](#setId-int) | Указывает идентификатор комментария, к которому привязана эта область. |
| [setIdInternal(int value)](#setIdInternal-int) |  |
| [setParentIdInternal(int value)](#setParentIdInternal-int) |  |
| [toString()](#toString) |  |
| [toString(SaveOptions saveOptions)](#toString-com.aspose.words.SaveOptions) | Экспортирует содержимое узла в строку, используя указанные параметры сохранения. |
| [toString(int saveFormat)](#toString-int) |  |
### CommentRangeEnd(DocumentBase doc, int id) {#CommentRangeEnd-com.aspose.words.DocumentBase-int}
```
public CommentRangeEnd(DocumentBase doc, int id)
```


Инициализирует новый экземпляр этого класса.

 **Remarks:** 

Когда создаётся [CommentRangeEnd](../../com.aspose.words/commentrangeend/), он принадлежит указанному документу, но ещё не является частью документа, и [Node.getParentNode()](../../com.aspose.words/node/\#getParentNode) возвращает null.

Чтобы добавить [CommentRangeEnd](../../com.aspose.words/commentrangeend/) в документ, используйте InsertAfter или InsertBefore в абзаце, где вы хотите вставить комментарий.

 **Examples:** 

Показывает, как вывести содержимое всех комментариев и их диапазонов комментариев с помощью посетителя документа.

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
| Параметр | Тип | Описание |
| --- | --- | --- |
| doc | [DocumentBase](../../com.aspose.words/documentbase/) | Документ‑владелец. |
| id | int | Идентификатор комментария, к которому привязан данный объект. |

### accept(DocumentVisitor visitor) {#accept-com.aspose.words.DocumentVisitor}
```
public boolean accept(DocumentVisitor visitor)
```


Принимает посетителя.

 **Remarks:** 

Вызывает [DocumentVisitor.visitCommentRangeEnd(com.aspose.words.CommentRangeEnd)](../../com.aspose.words/documentvisitor/\#visitCommentRangeEnd-com.aspose.words.CommentRangeEnd).

Для получения дополнительной информации см. шаблон проектирования Visitor.

 **Examples:** 

Показывает, как вывести содержимое всех комментариев и их диапазонов комментариев с помощью посетителя документа.

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
| Параметр | Тип | Описание |
| --- | --- | --- |
| visitor | [DocumentVisitor](../../com.aspose.words/documentvisitor/) | Посетитель, который будет обходить узел. |

**Returns:**
boolean — false, если посетитель запросил остановку перечисления.
### deepClone(boolean isCloneChildren) {#deepClone-boolean}
```
public Node deepClone(boolean isCloneChildren)
```


Создаёт дубликат узла.

 **Remarks:** 

Этот метод служит конструктором копирования для узлов. Клонированный узел не имеет родителя, но принадлежит тому же документу, что и оригинальный узел.

Этот метод всегда выполняет глубокое копирование узла. Параметр  isCloneChildren  указывает, следует ли также копировать все дочерние узлы.

 **Examples:** 

Показывает, как клонировать составной узел.

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
| Параметр | Тип | Описание |
| --- | --- | --- |
| isCloneChildren | boolean | true, чтобы рекурсивно клонировать поддерево под указанным узлом; false, чтобы клонировать только сам узел. |

**Returns:**
[Node](../../com.aspose.words/node/) - The cloned node.
### getAncestor(int ancestorType) {#getAncestor-int}
```
public CompositeNode getAncestor(int ancestorType)
```




**Parameters:**
| Параметр | Тип | Описание |
| --- | --- | --- |
| ancestorType | int |  |

**Returns:**
[CompositeNode](../../com.aspose.words/compositenode/)
### getAncestor(Class ancestorType) {#getAncestor-java.lang.Class}
```
public CompositeNode getAncestor(Class ancestorType)
```


Получает первого предка указанного типа объекта.

 **Remarks:** 

Тип предка совпадает, если он равен  ancestorType  или наследуется от  ancestorType .

 **Examples:** 

Показывает, как определить, вложены ли таблицы.

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
| Параметр | Тип | Описание |
| --- | --- | --- |
| ancestorType | java.lang.Class | Тип объекта предка, который нужно получить. |

**Returns:**
[CompositeNode](../../com.aspose.words/compositenode/) - The ancestor of the specified type or  null  if no ancestor of this type was found.
### getCustomNodeId() {#getCustomNodeId}
```
public int getCustomNodeId()
```


Указывает пользовательский идентификатор узла.

 **Remarks:** 

По умолчанию равно нулю.

Этот идентификатор можно установить и использовать произвольно. Например, в качестве ключа для получения внешних данных.

Важно: указанное значение не сохраняется в выходной файл и существует только в течение жизни узла.

 **Examples:** 

Показывает, как пройтись по коллекции дочерних узлов составного узла.

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
int — соответствующее значение  int .
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


Получает документ, к которому принадлежит этот узел.

 **Remarks:** 

Узел всегда принадлежит документу, даже если он только что создан и ещё не добавлен в дерево, или если он был удалён из дерева.

 **Examples:** 

Показывает, как создать узел и установить его владелец‑документ.

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


Указывает идентификатор комментария, к которому привязана эта область.

 **Examples:** 

Показывает, как вывести содержимое всех комментариев и их диапазонов комментариев с помощью посетителя документа.

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
int — соответствующее значение  int .
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


Получает узел, непосредственно следующий за этим узлом.

 **Remarks:** 

Если следующего узла нет, возвращается  null  .

 **Examples:** 

Показывает, как обходить дерево дочерних узлов составного узла.

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

Показывает, как использовать свойство NextSibling узла для перечисления его непосредственных дочерних элементов.

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


Возвращает [NodeType.COMMENT\_RANGE\_END](../../com.aspose.words/nodetype/\#COMMENT-RANGE-END).

 **Examples:** 

Показывает, как обходить дерево дочерних узлов составного узла.

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
int — [NodeType.COMMENT\_RANGE\_END](../../com.aspose.words/nodetype/\#COMMENT-RANGE-END). Возвращаемое значение является одной из констант [NodeType](../../com.aspose.words/nodetype/).
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


Получает непосредственного родителя этого узла.

 **Remarks:** 

Если узел только что создан и ещё не добавлен в дерево, или если он был удалён из дерева, родитель является  null .

 **Examples:** 

Показывает, как получить доступ к родительскому узлу.

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

Показывает, как создать узел и установить его владелец‑документ.

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


Получает узел, непосредственно предшествующий этому узлу.

 **Remarks:** 

Если предыдущего узла нет, возвращается  null .

 **Examples:** 

Показывает, как использовать методы Node и CompositeNode для удаления раздела перед последним разделом в документе.

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


Возвращает объект [Range](../../com.aspose.words/range/), представляющий часть документа, содержащуюся в этом узле.

 **Examples:** 

Показывает, как удалить все узлы из диапазона.

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


Получает текст этого узла и всех его дочерних элементов.

 **Remarks:** 

Возвращаемая строка включает все управляющие и специальные символы, как описано в [ControlChar](../../com.aspose.words/controlchar/).

 **Examples:** 

Показывает, как использовать управляющие символы.

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

Показывает, как вручную создать документ Aspose.Words.

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


Возвращает  true  , если этот узел может содержать другие узлы. (197141,6)

 **Examples:** 

Показывает, как обходить дерево дочерних узлов составного узла.

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
boolean -  true , если этот узел может содержать другие узлы.
### nextPreOrder(Node rootNode) {#nextPreOrder-com.aspose.words.Node}
```
public Node nextPreOrder(Node rootNode)
```


Получает следующий узел согласно алгоритму обхода дерева в порядке предобхода.

 **Examples:** 

Показывает, как обходить дерево узлов документа, используя алгоритм обхода в порядке предшествования, и удалять любые найденные фигуры с изображением.

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
| Параметр | Тип | Описание |
| --- | --- | --- |
| rootNode | [Node](../../com.aspose.words/node/) | Верхний узел (ограничение) обхода. |

**Returns:**
[Node](../../com.aspose.words/node/) - Next node in pre-order order. Null if reached the  rootNode .
### nodeTypeToString(int nodeType) {#nodeTypeToString-int}
```
public static String nodeTypeToString(int nodeType)
```




**Parameters:**
| Параметр | Тип | Описание |
| --- | --- | --- |
| nodeType | int |  |

**Returns:**
java.lang.String
### previousPreOrder(Node rootNode) {#previousPreOrder-com.aspose.words.Node}
```
public Node previousPreOrder(Node rootNode)
```


Получает предыдущий узел в соответствии с алгоритмом обхода дерева в порядке предобхода.

 **Examples:** 

Показывает, как обходить дерево узлов документа, используя алгоритм обхода в порядке предшествования, и удалять любые найденные фигуры с изображением.

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
| Параметр | Тип | Описание |
| --- | --- | --- |
| rootNode | [Node](../../com.aspose.words/node/) | Верхний узел (ограничение) обхода. |

**Returns:**
[Node](../../com.aspose.words/node/) - Previous node in pre-order order. Null if reached the  rootNode .
### remove() {#remove}
```
public void remove()
```


Удаляет себя из родителя.

 **Examples:** 

Показывает, как удалить из документа все фигуры с изображениями.

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

Показывает, как удалить из составного узла все дочерние узлы определённого типа.

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


Указывает пользовательский идентификатор узла.

 **Remarks:** 

По умолчанию равно нулю.

Этот идентификатор можно установить и использовать произвольно. Например, в качестве ключа для получения внешних данных.

Важно: указанное значение не сохраняется в выходной файл и существует только в течение жизни узла.

 **Examples:** 

Показывает, как пройтись по коллекции дочерних узлов составного узла.

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
| Параметр | Тип | Описание |
| --- | --- | --- |
| значение | int | Соответствующее  int  значение. |

### setDisplacedByCustomXml(int value) {#setDisplacedByCustomXml-int}
```
public void setDisplacedByCustomXml(int value)
```




**Parameters:**
| Параметр | Тип | Описание |
| --- | --- | --- |
| значение | int |  |

### setId(int value) {#setId-int}
```
public void setId(int value)
```


Указывает идентификатор комментария, к которому привязана эта область.

 **Examples:** 

Показывает, как вывести содержимое всех комментариев и их диапазонов комментариев с помощью посетителя документа.

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
| Параметр | Тип | Описание |
| --- | --- | --- |
| значение | int | Соответствующее  int  значение. |

### setIdInternal(int value) {#setIdInternal-int}
```
public void setIdInternal(int value)
```




**Parameters:**
| Параметр | Тип | Описание |
| --- | --- | --- |
| значение | int |  |

### setParentIdInternal(int value) {#setParentIdInternal-int}
```
public void setParentIdInternal(int value)
```




**Parameters:**
| Параметр | Тип | Описание |
| --- | --- | --- |
| значение | int |  |

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


Экспортирует содержимое узла в строку, используя указанные параметры сохранения.

 **Examples:** 

Экспортирует содержимое узла в String в формате HTML.

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
| Параметр | Тип | Описание |
| --- | --- | --- |
| saveOptions | [SaveOptions](../../com.aspose.words/saveoptions/) | Указывает параметры, которые управляют тем, как сохраняется узел. |

**Returns:**
java.lang.String - Содержимое узла в указанном формате.
### toString(int saveFormat) {#toString-int}
```
public String toString(int saveFormat)
```




**Parameters:**
| Параметр | Тип | Описание |
| --- | --- | --- |
| saveFormat | int |  |

**Returns:**
java.lang.String
