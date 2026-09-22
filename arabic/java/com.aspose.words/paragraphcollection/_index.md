---
title: "ParagraphCollection"
linktitle: "ParagraphCollection"
second_title: "Aspose.Words لـ Java"
description: "يوفر وصولًا مكتوبًا إلى مجموعة من عقد الفقرة في Java."
type: docs
weight: 524
url: /ar/java/com.aspose.words/paragraphcollection/
---

**Inheritance:**
java.lang.Object، [com.aspose.words.NodeCollection](../../com.aspose.words/nodecollection/)
```
public class ParagraphCollection extends NodeCollection
```

يوفر وصولًا مكتوبًا إلى مجموعة من عقد [Paragraph](../../com.aspose.words/paragraph/).

لمزيد من المعلومات، زر مقالة الوثائق [ Working with Paragraphs ][Working with Paragraphs].

 **Examples:** 

يوضح كيفية التحقق مما إذا كانت الفقرة مراجعة نقل.

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


[Working with Paragraphs]: https://docs.aspose.com/words/java/working-with-paragraphs/
## الطرق

| طريقة | الوصف |
| --- | --- |
| [add(Node node)](#add-com.aspose.words.Node) | يضيف عقدة إلى نهاية المجموعة. |
| [clear()](#clear) | يزيل جميع العقد من هذه المجموعة ومن المستند. |
| [contains(Node node)](#contains-com.aspose.words.Node) | يحدد ما إذا كانت العقدة موجودة في المجموعة. |
| [get(int index)](#get-int) | يسترجع [Paragraph](../../com.aspose.words/paragraph/) عند الفهرس المحدد. |
| [getContainer()](#getContainer) |  |
| [getCount()](#getCount) | يحصل على عدد العقد في المجموعة. |
| [getCurrentNode()](#getCurrentNode) |  |
| [getNextMatchingNode(Node curNode)](#getNextMatchingNode-com.aspose.words.Node) |  |
| [indexOf(Node node)](#indexOf-com.aspose.words.Node) | يرجع الفهرس الصفري للعقدة المحددة. |
| [insert(int index, Node node)](#insert-int-com.aspose.words.Node) | يدرج عقدة في المجموعة عند الفهرس المحدد. |
| [iterator()](#iterator) | يوفر تكرارًا بسيطًا بنمط "foreach" على مجموعة العقد. |
| [remove(Node node)](#remove-com.aspose.words.Node) | يزيل العقدة من المجموعة ومن المستند. |
| [removeAt(int index)](#removeAt-int) | يزيل العقدة عند الفهرس المحدد من المجموعة ومن المستند. |
| [toArray()](#toArray) | ينسخ جميع الفقرات من المجموعة إلى مصفوفة جديدة من الفقرات. |
### add(Node node) {#add-com.aspose.words.Node}
```
public void add(Node node)
```


يضيف عقدة إلى نهاية المجموعة.

**Parameters:**
| معامل | نوع | الوصف |
| --- | --- | --- |
| node | [Node](../../com.aspose.words/node/) | العقدة التي ستُضاف إلى نهاية المجموعة. |

### clear() {#clear}
```
public void clear()
```


يزيل جميع العقد من هذه المجموعة ومن المستند.

 **Examples:** 

يظهر كيفية إزالة جميع الأقسام من مستند.

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


يحدد ما إذا كانت العقدة موجودة في المجموعة.

 **Remarks:** 

هذه الطريقة تقوم ببحث خطي؛ لذلك، وقت التنفيذ المتوسط يتناسب مع [getCount()](../../com.aspose.words/nodecollection/\#getCount).

 **Examples:** 

يظهر كيفية العمل مع NodeCollection.

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
| معامل | نوع | الوصف |
| --- | --- | --- |
| node | [Node](../../com.aspose.words/node/) | العقدة المراد تحديدها. |

**Returns:**
منطقي -  true  إذا تم العثور على العنصر في المجموعة؛ وإلا،  false .
### get(int index) {#get-int}
```
public Node get(int index)
```


يسترجع [Paragraph](../../com.aspose.words/paragraph/) عند الفهرس المحدد.

 **Remarks:** 

الفهرس يبدأ من الصفر.

يسمح بالمؤشرات السلبية وتدل على الوصول من نهاية المجموعة. على سبيل المثال -1 يعني العنصر الأخير، -2 يعني العنصر قبل الأخير الثاني وهكذا.

إذا كان الفهرس أكبر من أو يساوي عدد العناصر في القائمة، فإن هذا يُعيد إشارة فارغة.

إذا كان الفهرس سالبًا وكانت قيمته المطلقة أكبر من عدد العناصر في القائمة، فإن هذا يُعيد إشارة فارغة.

 **Examples:** 

يوضح كيفية التحقق مما إذا كانت الفقرة مراجعة نقل.

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

**Parameters:**
| معامل | نوع | الوصف |
| --- | --- | --- |
| الفهرس | int | فهرس داخل المجموعة. |

**Returns:**
[Node](../../com.aspose.words/node/) - The corresponding [Paragraph](../../com.aspose.words/paragraph/) value.
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


يحصل على عدد العقد في المجموعة.

 **Examples:** 

يوضح كيفية التجوال عبر مجموعة العقد الفرعية لعقدة مركبة.

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

يوضح كيفية معرفة ما إذا كانت الجداول متداخلة.

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
int - عدد العقد في المجموعة.
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
| معامل | نوع | الوصف |
| --- | --- | --- |
| curNode | [Node](../../com.aspose.words/node/) |  |

**Returns:**
[Node](../../com.aspose.words/node/)
### indexOf(Node node) {#indexOf-com.aspose.words.Node}
```
public int indexOf(Node node)
```


يرجع الفهرس الصفري للعقدة المحددة.

 **Remarks:** 

هذه الطريقة تقوم ببحث خطي؛ لذلك، وقت التنفيذ المتوسط يتناسب مع [getCount()](../../com.aspose.words/nodecollection/\#getCount).

 **Examples:** 

يظهر كيفية الحصول على فهرس عقدة في مجموعة.

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
| معامل | نوع | الوصف |
| --- | --- | --- |
| node | [Node](../../com.aspose.words/node/) | العقدة المراد تحديدها. |

**Returns:**
int - الفهرس الصفري للعقدة داخل المجموعة، إذا وُجد؛ وإلا، -1.
### insert(int index, Node node) {#insert-int-com.aspose.words.Node}
```
public void insert(int index, Node node)
```


يدرج عقدة في المجموعة عند الفهرس المحدد.

**Parameters:**
| معامل | نوع | الوصف |
| --- | --- | --- |
| الفهرس | int | الفهرس الصفري للعقدة. يُسمح بالمؤشرات السلبية وتدل على الوصول من نهاية القائمة. على سبيل المثال -1 يعني العقدة الأخيرة، -2 يعني العقدة قبل الأخيرة الثانية وهكذا. |
| node | [Node](../../com.aspose.words/node/) | العقدة المراد إدراجها. |

### iterator() {#iterator}
```
public Iterator iterator()
```


يوفر تكرارًا بسيطًا بنمط "foreach" على مجموعة العقد.

**Returns:**
java.util.Iterator - مكرّر.
### remove(Node node) {#remove-com.aspose.words.Node}
```
public void remove(Node node)
```


يزيل العقدة من المجموعة ومن المستند.

 **Examples:** 

يظهر كيفية العمل مع NodeCollection.

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
| معامل | نوع | الوصف |
| --- | --- | --- |
| node | [Node](../../com.aspose.words/node/) | العقدة المراد إزالتها. |

### removeAt(int index) {#removeAt-int}
```
public void removeAt(int index)
```


يزيل العقدة عند الفهرس المحدد من المجموعة ومن المستند.

 **Examples:** 

يظهر كيفية إضافة وإزالة الأقسام في مستند.

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
| معامل | نوع | الوصف |
| --- | --- | --- |
| الفهرس | int | الفهرس الصفري للعقدة. يُسمح بالمؤشرات السلبية وتدل على الوصول من نهاية القائمة. على سبيل المثال -1 يعني العقدة الأخيرة، -2 يعني العقدة قبل الأخيرة الثانية وهكذا. |

### toArray() {#toArray}
```
public Node[] toArray()
```


ينسخ جميع الفقرات من المجموعة إلى مصفوفة جديدة من الفقرات.

 **Examples:** 

يوضح كيفية إنشاء مصفوفة من NodeCollection.

```

 Document doc = new Document(getMyDir() + "Paragraphs.docx");

 Paragraph[] paras = doc.getFirstSection().getBody().getParagraphs().toArray();

 Assert.assertEquals(22, paras.length);
 
```

يوضح كيفية استخدام "hot remove" لإزالة عقدة أثناء التعداد.

```

 Document doc = new Document();
 DocumentBuilder builder = new DocumentBuilder(doc);

 builder.writeln("The first paragraph");
 builder.writeln("The second paragraph");
 builder.writeln("The third paragraph");
 builder.writeln("The fourth paragraph");

 // Remove a node from the collection in the middle of an enumeration.
 for (Paragraph para : doc.getFirstSection().getBody().getParagraphs().toArray())
     if (para.getRange().getText().contains("third"))
         para.remove();

 Assert.assertFalse(doc.getText().contains("The third paragraph"));
 
```

**Returns:**
com.aspose.words.Node[] - مصفوفة من الفقرات.
