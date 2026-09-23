---
title: "CommentCollection"
linktitle: "CommentCollection"
second_title: "Aspose.Words для Java"
description: "Обеспечивает типизированный доступ к коллекции узлов Comment в Java."
type: docs
weight: 109
url: /ru/java/com.aspose.words/commentcollection/
---

**Inheritance:**
java.lang.Object, [com.aspose.words.NodeCollection](../../com.aspose.words/nodecollection/)
```
public class CommentCollection extends NodeCollection
```

Обеспечивает типизированный доступ к коллекции узлов [Comment](../../com.aspose.words/comment/).

Чтобы узнать больше, посетите статью документации [ Working with Comments ][Working with Comments].

 **Examples:** 

Показывает, как пометить комментарий как "done".

```

 Document doc = new Document();
 DocumentBuilder builder = new DocumentBuilder(doc);
 builder.writeln("Helo world!");

 // Insert a comment to point out an error.
 Comment comment = new Comment(doc, "John Doe", "J.D.", new Date());
 comment.setText("Fix the spelling error!");
 doc.getFirstSection().getBody().getFirstParagraph().appendChild(comment);

 // Comments have a "Done" flag, which is set to "false" by default.
 // If a comment suggests that we make a change within the document,
 // we can apply the change, and then also set the "Done" flag afterwards to indicate the correction.
 Assert.assertFalse(comment.getDone());

 doc.getFirstSection().getBody().getFirstParagraph().getRuns().get(0).setText("Hello world!");
 comment.setDone(true);

 // Comments that are "done" will differentiate themselves
 // from ones that are not "done" with a faded text color.
 comment = new Comment(doc, "John Doe", "J.D.", new Date());
 comment.setText("Add text to this paragraph.");
 builder.getCurrentParagraph().appendChild(comment);

 doc.save(getArtifactsDir() + "Comment.Done.docx");
 
```


[Working with Comments]: https://docs.aspose.com/words/java/working-with-comments/
## Методы

| Метод | Описание |
| --- | --- |
| [add(Node node)](#add-com.aspose.words.Node) | Добавляет узел в конец коллекции. |
| [clear()](#clear) | Удаляет все узлы из этой коллекции и из документа. |
| [contains(Node node)](#contains-com.aspose.words.Node) | Определяет, находится ли узел в коллекции. |
| [get(int index)](#get-int) | Получает [Comment](../../com.aspose.words/comment/) по заданному индексу. |
| [getContainer()](#getContainer) |  |
| [getCount()](#getCount) | Возвращает количество узлов в коллекции. |
| [getCurrentNode()](#getCurrentNode) |  |
| [getNextMatchingNode(Node curNode)](#getNextMatchingNode-com.aspose.words.Node) |  |
| [indexOf(Node node)](#indexOf-com.aspose.words.Node) | Возвращает нулевой индекс указанного узла. |
| [insert(int index, Node node)](#insert-int-com.aspose.words.Node) | Вставляет узел в коллекцию по указанному индексу. |
| [iterator()](#iterator) | Обеспечивает простую итерацию в стиле "foreach" по коллекции узлов. |
| [remove(Node node)](#remove-com.aspose.words.Node) | Удаляет узел из коллекции и из документа. |
| [removeAt(int index)](#removeAt-int) | Удаляет узел по указанному индексу из коллекции и из документа. |
| [toArray()](#toArray) | Копирует все узлы из коллекции в новый массив узлов. |
### add(Node node) {#add-com.aspose.words.Node}
```
public void add(Node node)
```


Добавляет узел в конец коллекции.

**Parameters:**
| Параметр | Тип | Описание |
| --- | --- | --- |
| node | [Node](../../com.aspose.words/node/) | Узел, который будет добавлен в конец коллекции. |

### clear() {#clear}
```
public void clear()
```


Удаляет все узлы из этой коллекции и из документа.

 **Examples:** 

Показывает, как удалить все разделы из документа.

```

 Document doc = new Document(getMyDir() + "Document.docx");

 // This document has one section with a few child nodes containing and displaying all the document's contents.
 Assert.assertEquals(doc.getSections().getCount(), 1);
 Assert.assertEquals(doc.getSections().get(0).getChildNodes(NodeType.ANY, true).getCount(), 17);
 Assert.assertEquals("Hello World!\r\rHello Word!\r\r\rHello World!", doc.getText().trim());

 // Clear the collection of sections, which will remove all of the document's children.
 doc.getSections().clear();

 Assert.assertEquals(0, doc.getChildNodes(NodeType.ANY, true).getCount());
 Assert.assertEquals("", doc.getText().trim());
 
```

### contains(Node node) {#contains-com.aspose.words.Node}
```
public boolean contains(Node node)
```


Определяет, находится ли узел в коллекции.

 **Remarks:** 

Этот метод выполняет линейный поиск; поэтому среднее время выполнения пропорционально [getCount()](../../com.aspose.words/nodecollection/\#getCount).

 **Examples:** 

Показывает, как работать с NodeCollection.

```

 Document doc = new Document();
 DocumentBuilder builder = new DocumentBuilder(doc);

 // Add text to the document by inserting Runs using a DocumentBuilder.
 builder.write("Run 1. ");
 builder.write("Run 2. ");

 // Every invocation of the "Write()" method creates a new Run,
 // which then appears in the parent Paragraph's RunCollection.
 RunCollection runs = doc.getFirstSection().getBody().getFirstParagraph().getRuns();

 Assert.assertEquals(2, runs.getCount());

 // We can also insert a node into the RunCollection manually.
 Run newRun = new Run(doc, "Run 3. ");
 runs.insert(3, newRun);

 Assert.assertTrue(runs.contains(newRun));
 Assert.assertEquals("Run 1. Run 2. Run 3.", doc.getText().trim());

 // Access individual runs and remove them to remove their text from the document.
 Run run = runs.get(1);
 runs.remove(run);

 Assert.assertEquals("Run 1. Run 3.", doc.getText().trim());
 Assert.assertNotNull(run);
 Assert.assertFalse(runs.contains(run));
 
```

**Parameters:**
| Параметр | Тип | Описание |
| --- | --- | --- |
| node | [Node](../../com.aspose.words/node/) | Узел для поиска. |

**Returns:**
boolean -  true  если элемент найден в коллекции; иначе,  false .
### get(int index) {#get-int}
```
public Comment get(int index)
```


Получает [Comment](../../com.aspose.words/comment/) по заданному индексу.

 **Remarks:** 

Индекс начинается с нуля.

Отрицательные индексы допускаются и указывают доступ с конца коллекции. Например, -1 означает последний элемент, -2 означает предпоследний и так далее.

Если индекс больше или равен количеству элементов в списке, возвращается null-ссылка.

Если индекс отрицательный и его абсолютное значение больше количества элементов в списке, возвращается null-ссылка.

 **Examples:** 

Показывает, как удалить ответы на комментарий.

```

 Document doc = new Document();

 Comment comment = new Comment(doc, "John Doe", "J.D.", new Date());
 comment.setText("My comment.");

 doc.getFirstSection().getBody().getFirstParagraph().appendChild(comment);

 comment.addReply("Joe Bloggs", "J.B.", new Date(), "New reply");
 comment.addReply("Joe Bloggs", "J.B.", new Date(), "Another reply");

 Assert.assertEquals(2, comment.getReplies().getCount());

 // Below are two ways of removing replies from a comment.
 // 1 -  Use the "RemoveReply" method to remove replies from a comment individually:
 comment.removeReply(comment.getReplies().get(0));

 Assert.assertEquals(1, comment.getReplies().getCount());

 // 2 -  Use the "RemoveAllReplies" method to remove all replies from a comment at once:
 comment.removeAllReplies();

 Assert.assertEquals(0, comment.getReplies().getCount());
 
```

**Parameters:**
| Параметр | Тип | Описание |
| --- | --- | --- |
| индекс | int | Индекс в коллекции. |

**Returns:**
[Comment](../../com.aspose.words/comment/) - The corresponding [Comment](../../com.aspose.words/comment/) value.
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


Возвращает количество узлов в коллекции.

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

**Returns:**
int - Количество узлов в коллекции.
### getCurrentNode() {#getCurrentNode}
```
public Node getCurrentNode()
```




**Returns:**
[Node](../../com.aspose.words/node/)
### getNextMatchingNode(Node curNode) {#getNextMatchingNode-com.aspose.words.Node}
```
public Node getNextMatchingNode(Node curNode)
```




**Parameters:**
| Параметр | Тип | Описание |
| --- | --- | --- |
| curNode | [Node](../../com.aspose.words/node/) |  |

**Returns:**
[Node](../../com.aspose.words/node/)
### indexOf(Node node) {#indexOf-com.aspose.words.Node}
```
public int indexOf(Node node)
```


Возвращает нулевой индекс указанного узла.

 **Remarks:** 

Этот метод выполняет линейный поиск; поэтому среднее время выполнения пропорционально [getCount()](../../com.aspose.words/nodecollection/\#getCount).

 **Examples:** 

Показывает, как получить индекс узла в коллекции.

```

 Document doc = new Document(getMyDir() + "Tables.docx");

 Table table = doc.getFirstSection().getBody().getTables().get(0);
 NodeCollection allTables = doc.getChildNodes(NodeType.TABLE, true);

 Assert.assertEquals(0, allTables.indexOf(table));

 Row row = table.getRows().get(2);

 Assert.assertEquals(2, table.indexOf(row));

 Cell cell = row.getLastCell();

 Assert.assertEquals(4, row.indexOf(cell));
 
```

**Parameters:**
| Параметр | Тип | Описание |
| --- | --- | --- |
| node | [Node](../../com.aspose.words/node/) | Узел для поиска. |

**Returns:**
int - Нулевой индекс узла в коллекции, если найден; иначе, -1.
### insert(int index, Node node) {#insert-int-com.aspose.words.Node}
```
public void insert(int index, Node node)
```


Вставляет узел в коллекцию по указанному индексу.

**Parameters:**
| Параметр | Тип | Описание |
| --- | --- | --- |
| индекс | int | Нулевой индекс узла. Отрицательные индексы допускаются и указывают доступ с конца списка. Например, -1 означает последний узел, -2 означает предпоследний и так далее. |
| node | [Node](../../com.aspose.words/node/) | Узел для вставки. |

### iterator() {#iterator}
```
public Iterator iterator()
```


Обеспечивает простую итерацию в стиле "foreach" по коллекции узлов.

**Returns:**
java.util.Iterator - Итератор.
### remove(Node node) {#remove-com.aspose.words.Node}
```
public void remove(Node node)
```


Удаляет узел из коллекции и из документа.

 **Examples:** 

Показывает, как работать с NodeCollection.

```

 Document doc = new Document();
 DocumentBuilder builder = new DocumentBuilder(doc);

 // Add text to the document by inserting Runs using a DocumentBuilder.
 builder.write("Run 1. ");
 builder.write("Run 2. ");

 // Every invocation of the "Write()" method creates a new Run,
 // which then appears in the parent Paragraph's RunCollection.
 RunCollection runs = doc.getFirstSection().getBody().getFirstParagraph().getRuns();

 Assert.assertEquals(2, runs.getCount());

 // We can also insert a node into the RunCollection manually.
 Run newRun = new Run(doc, "Run 3. ");
 runs.insert(3, newRun);

 Assert.assertTrue(runs.contains(newRun));
 Assert.assertEquals("Run 1. Run 2. Run 3.", doc.getText().trim());

 // Access individual runs and remove them to remove their text from the document.
 Run run = runs.get(1);
 runs.remove(run);

 Assert.assertEquals("Run 1. Run 3.", doc.getText().trim());
 Assert.assertNotNull(run);
 Assert.assertFalse(runs.contains(run));
 
```

**Parameters:**
| Параметр | Тип | Описание |
| --- | --- | --- |
| node | [Node](../../com.aspose.words/node/) | Узел для удаления. |

### removeAt(int index) {#removeAt-int}
```
public void removeAt(int index)
```


Удаляет узел по указанному индексу из коллекции и из документа.

 **Examples:** 

Показывает, как добавить и удалить разделы в документе.

```

 Document doc = new Document();
 DocumentBuilder builder = new DocumentBuilder(doc);

 builder.write("Section 1");
 builder.insertBreak(BreakType.SECTION_BREAK_NEW_PAGE);
 builder.write("Section 2");

 Assert.assertEquals("Section 1\fSection 2", doc.getText().trim());

 // Delete the first section from the document.
 doc.getSections().removeAt(0);

 Assert.assertEquals("Section 2", doc.getText().trim());

 // Append a copy of what is now the first section to the end of the document.
 int lastSectionIdx = doc.getSections().getCount() - 1;
 Section newSection = doc.getSections().get(lastSectionIdx).deepClone();
 doc.getSections().add(newSection);

 Assert.assertEquals("Section 2\fSection 2", doc.getText().trim());
 
```

**Parameters:**
| Параметр | Тип | Описание |
| --- | --- | --- |
| индекс | int | Нулевой индекс узла. Отрицательные индексы допускаются и указывают доступ с конца списка. Например, -1 означает последний узел, -2 означает предпоследний и так далее. |

### toArray() {#toArray}
```
public Node[] toArray()
```


Копирует все узлы из коллекции в новый массив узлов.

 **Remarks:** 

Не следует добавлять/удалять узлы во время итерации по коллекции узлов, так как это делает итератор недействительным и требует обновления живых коллекций.

Чтобы иметь возможность добавлять/удалять узлы во время итерации, используйте этот метод для копирования узлов в массив фиксированного размера, а затем итерации по массиву.

 **Examples:** 

Показывает, как заменить все формы текстовых полей на формы изображений.

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

**Returns:**
com.aspose.words.Node[] — массив узлов.
