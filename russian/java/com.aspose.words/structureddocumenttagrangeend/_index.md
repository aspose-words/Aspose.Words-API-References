---
title: "StructuredDocumentTagRangeEnd"
linktitle: "StructuredDocumentTagRangeEnd"
second_title: "Aspose.Words для Java"
description: "Представляет конец диапазонного структурированного тега документа, который принимает контент из нескольких разделов в Java."
type: docs
weight: 639
url: /ru/java/com.aspose.words/structureddocumenttagrangeend/
---

**Inheritance:**
java.lang.Object, [com.aspose.words.Node](../../com.aspose.words/node/)
```
public class StructuredDocumentTagRangeEnd extends Node
```

Представляет конец **ranged** структурированного тега документа, который принимает контент из нескольких разделов. См. также узел [StructuredDocumentTagRangeStart](../../com.aspose.words/structureddocumenttagrangestart/).

Чтобы узнать больше, посетите статью документации [ Structured Document Tags or Content Control ][Structured Document Tags or Content Control].

 **Remarks:** 

Может быть непосредственным дочерним элементом узла [Body](../../com.aspose.words/body/) **только**.

 **Examples:** 

Показывает, как получить свойства многоразделных структурированных тегов документа.

```

 Document doc = new Document(getMyDir() + "Multi-section structured document tags.docx");

 StructuredDocumentTagRangeStart rangeStartTag = (StructuredDocumentTagRangeStart) doc.getChildNodes(NodeType.STRUCTURED_DOCUMENT_TAG_RANGE_START, true).get(0);
 StructuredDocumentTagRangeEnd rangeEndTag = (StructuredDocumentTagRangeEnd) doc.getChildNodes(NodeType.STRUCTURED_DOCUMENT_TAG_RANGE_END, true).get(0);

 System.out.println("StructuredDocumentTagRangeStart values:");
 System.out.println(MessageFormat.format("\t|Id: {0}", rangeStartTag.getId()));
 System.out.println(MessageFormat.format("\t|Title: {0}", rangeStartTag.getTitle()));
 System.out.println(MessageFormat.format("\t|PlaceholderName: {0}", rangeStartTag.getPlaceholderName()));
 System.out.println(MessageFormat.format("\t|IsShowingPlaceholderText: {0}", rangeStartTag.isShowingPlaceholderText()));
 System.out.println(MessageFormat.format("\t|LockContentControl: {0}", rangeStartTag.getLockContentControl()));
 System.out.println(MessageFormat.format("\t|LockContents: {0}", rangeStartTag.getLockContents()));
 System.out.println(MessageFormat.format("\t|Level: {0}", rangeStartTag.getLevel()));
 System.out.println(MessageFormat.format("\t|NodeType: {0}", rangeStartTag.getNodeType()));
 System.out.println(MessageFormat.format("\t|RangeEnd: {0}", rangeStartTag.getRangeEnd()));
 System.out.println(MessageFormat.format("\t|Color: {0}", rangeStartTag.getColor()));
 System.out.println(MessageFormat.format("\t|SdtType: {0}", rangeStartTag.getSdtType()));
 System.out.println(MessageFormat.format("\t|FlatOpcContent: {0}", rangeStartTag.getWordOpenXML()));
 System.out.println(MessageFormat.format("\t|Tag: {0}\n", rangeStartTag.getTag()));

 System.out.println("StructuredDocumentTagRangeEnd values:");
 System.out.println("\t|Id: {rangeEndTag.Id}");
 System.out.println("\t|NodeType: {rangeEndTag.NodeType}");
 
```


[Structured Document Tags or Content Control]: https://docs.aspose.com/words/java/working-with-content-control-sdt/
## Конструкторы

| Конструктор | Описание |
| --- | --- |
| [StructuredDocumentTagRangeEnd(DocumentBase doc, int id)](#StructuredDocumentTagRangeEnd-com.aspose.words.DocumentBase-int) | Инициализирует новый экземпляр класса **Structured document tag range end**. |
## Методы

| Метод | Описание |
| --- | --- |
| [accept(DocumentVisitor visitor)](#accept-com.aspose.words.DocumentVisitor) | Принимает посетителя. |
| [deepClone(boolean isCloneChildren)](#deepClone-boolean) | Создаёт дубликат узла. |
| [getAncestor(int ancestorType)](#getAncestor-int) |  |
| [getAncestor(Class ancestorType)](#getAncestor-java.lang.Class) | Получает первого предка указанного типа объекта. |
| [getCustomNodeId()](#getCustomNodeId) | Указывает пользовательский идентификатор узла. |
| [getDocument()](#getDocument) | Получает документ, к которому принадлежит этот узел. |
| [getId()](#getId) | Указывает уникальный только для чтения постоянный числовой Id для этого узла **StructuredDocumentTagRange**. |
| [getNextSibling()](#getNextSibling) | Получает узел, непосредственно следующий за этим узлом. |
| [getNodeType()](#getNodeType) | Возвращает [NodeType.STRUCTURED\_DOCUMENT\_TAG\_RANGE\_END](../../com.aspose.words/nodetype/\#STRUCTURED-DOCUMENT-TAG-RANGE-END). |
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
| [toString()](#toString) |  |
| [toString(SaveOptions saveOptions)](#toString-com.aspose.words.SaveOptions) | Экспортирует содержимое узла в строку, используя указанные параметры сохранения. |
| [toString(int saveFormat)](#toString-int) |  |
### StructuredDocumentTagRangeEnd(DocumentBase doc, int id) {#StructuredDocumentTagRangeEnd-com.aspose.words.DocumentBase-int}
```
public StructuredDocumentTagRangeEnd(DocumentBase doc, int id)
```


Инициализирует новый экземпляр класса **Structured document tag range end**.

 **Examples:** 

Показывает, как создать/удалить структурированный тег документа и его содержимое.

```
{@code
 public void sdtRangeExtendedMethods() throws Exception
 {
     Document doc = new Document();
     DocumentBuilder builder = new DocumentBuilder(doc);

     builder.writeln("StructuredDocumentTag element");

     StructuredDocumentTagRangeStart rangeStart = insertStructuredDocumentTagRanges(doc);

     // Removes ranged structured document tag, but keeps content inside.
     rangeStart.removeSelfOnly();

     rangeStart = (StructuredDocumentTagRangeStart)doc.getChild(
         NodeType.STRUCTURED_DOCUMENT_TAG_RANGE_START, 0, false);
     Assert.assertEquals(null, rangeStart);

     StructuredDocumentTagRangeEnd rangeEnd = (StructuredDocumentTagRangeEnd)doc.getChild(
         NodeType.STRUCTURED_DOCUMENT_TAG_RANGE_END, 0, false);

     Assert.assertEquals(null, rangeEnd);
     Assert.assertEquals("StructuredDocumentTag element", doc.getText().trim());

     rangeStart = insertStructuredDocumentTagRanges(doc);

     Node paragraphNode = rangeStart.getLastChild();
     if (paragraphNode != null)
         Assert.assertEquals("StructuredDocumentTag element", paragraphNode.getText().trim());

     // Removes ranged structured document tag and content inside.
     rangeStart.removeAllChildren();

     paragraphNode = rangeStart.getLastChild();
     Assert.assertEquals("",  paragraphNode.getText());
 }
```

**Parameters:**
| Параметр | Тип | Описание |
| --- | --- | --- |
| doc | [DocumentBase](../../com.aspose.words/documentbase/) | Документ‑владелец. |
| id | int | Идентификатор соответствующего начала диапазона структурированного тега документа. |

### accept(DocumentVisitor visitor) {#accept-com.aspose.words.DocumentVisitor}
```
public boolean accept(DocumentVisitor visitor)
```


Принимает посетителя.

 **Remarks:** 

Перебирает этот узел и все его дочерние узлы. Каждый узел вызывает соответствующий метод у [DocumentVisitor](../../com.aspose.words/documentvisitor/).

Для получения дополнительной информации см. шаблон проектирования Visitor.

**Parameters:**
| Параметр | Тип | Описание |
| --- | --- | --- |
| visitor | [DocumentVisitor](../../com.aspose.words/documentvisitor/) | Посетитель, который будет посещать узлы. |

**Returns:**
boolean — true, если все узлы были посещены; false, если [DocumentVisitor](../../com.aspose.words/documentvisitor/) остановил операцию до посещения всех узлов.
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


Указывает уникальный только для чтения постоянный числовой Id для этого узла **StructuredDocumentTagRange**. Соответствующий узел [StructuredDocumentTagRangeStart](../../com.aspose.words/structureddocumenttagrangestart/) имеет тот же [StructuredDocumentTagRangeStart.getId()](../../com.aspose.words/structureddocumenttagrangestart/\#getId).

 **Examples:** 

Показывает, как получить свойства многоразделных структурированных тегов документа.

```

 Document doc = new Document(getMyDir() + "Multi-section structured document tags.docx");

 StructuredDocumentTagRangeStart rangeStartTag = (StructuredDocumentTagRangeStart) doc.getChildNodes(NodeType.STRUCTURED_DOCUMENT_TAG_RANGE_START, true).get(0);
 StructuredDocumentTagRangeEnd rangeEndTag = (StructuredDocumentTagRangeEnd) doc.getChildNodes(NodeType.STRUCTURED_DOCUMENT_TAG_RANGE_END, true).get(0);

 System.out.println("StructuredDocumentTagRangeStart values:");
 System.out.println(MessageFormat.format("\t|Id: {0}", rangeStartTag.getId()));
 System.out.println(MessageFormat.format("\t|Title: {0}", rangeStartTag.getTitle()));
 System.out.println(MessageFormat.format("\t|PlaceholderName: {0}", rangeStartTag.getPlaceholderName()));
 System.out.println(MessageFormat.format("\t|IsShowingPlaceholderText: {0}", rangeStartTag.isShowingPlaceholderText()));
 System.out.println(MessageFormat.format("\t|LockContentControl: {0}", rangeStartTag.getLockContentControl()));
 System.out.println(MessageFormat.format("\t|LockContents: {0}", rangeStartTag.getLockContents()));
 System.out.println(MessageFormat.format("\t|Level: {0}", rangeStartTag.getLevel()));
 System.out.println(MessageFormat.format("\t|NodeType: {0}", rangeStartTag.getNodeType()));
 System.out.println(MessageFormat.format("\t|RangeEnd: {0}", rangeStartTag.getRangeEnd()));
 System.out.println(MessageFormat.format("\t|Color: {0}", rangeStartTag.getColor()));
 System.out.println(MessageFormat.format("\t|SdtType: {0}", rangeStartTag.getSdtType()));
 System.out.println(MessageFormat.format("\t|FlatOpcContent: {0}", rangeStartTag.getWordOpenXML()));
 System.out.println(MessageFormat.format("\t|Tag: {0}\n", rangeStartTag.getTag()));

 System.out.println("StructuredDocumentTagRangeEnd values:");
 System.out.println("\t|Id: {rangeEndTag.Id}");
 System.out.println("\t|NodeType: {rangeEndTag.NodeType}");
 
```

**Returns:**
int — соответствующее значение  int .
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


Возвращает [NodeType.STRUCTURED\_DOCUMENT\_TAG\_RANGE\_END](../../com.aspose.words/nodetype/\#STRUCTURED-DOCUMENT-TAG-RANGE-END).

**Returns:**
int — [NodeType.STRUCTURED\_DOCUMENT\_TAG\_RANGE\_END](../../com.aspose.words/nodetype/\#STRUCTURED-DOCUMENT-TAG-RANGE-END). Возвращаемое значение является одной из констант [NodeType](../../com.aspose.words/nodetype/).
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
