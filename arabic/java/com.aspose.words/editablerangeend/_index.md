---
title: "EditableRangeEnd"
linktitle: "EditableRangeEnd"
second_title: "Aspose.Words لـ Java"
description: "يمثل نهاية نطاق قابل للتحرير في مستند Word بلغة Java."
type: docs
weight: 180
url: /ar/java/com.aspose.words/editablerangeend/
---

**Inheritance:**
java.lang.Object، [com.aspose.words.Node](../../com.aspose.words/node/)
```
public class EditableRangeEnd extends Node
```

يمثل نهاية نطاق قابل للتحرير في مستند Word.

لمزيد من المعلومات، قم بزيارة مقالة وثائق [ Aspose.Words Document Object Model (DOM) ][Aspose.Words Document Object Model _DOM_]

 **Remarks:** 

يتكون نطاق قابل للتحرير كامل في مستند Word من [getEditableRangeStart()](../../com.aspose.words/editablerangeend/\#getEditableRangeStart) و[EditableRangeEnd](../../com.aspose.words/editablerangeend/) المتطابقين مع نفس المعرف.

[getEditableRangeStart()](../../com.aspose.words/editablerangeend/\#getEditableRangeStart) and [EditableRangeEnd](../../com.aspose.words/editablerangeend/) are just markers inside a document that specify where the editable range starts and ends.

استخدم الفئة [EditableRange](../../com.aspose.words/editablerange/) كـ \"واجهة\" للعمل مع نطاق قابل للتحرير ككائن واحد.

حاليًا يتم دعم النطاقات القابلة للتحرير فقط على مستوى السطر داخل [Paragraph](../../com.aspose.words/paragraph/)، لكن بداية النطاق القابل للتحرير ونهايته يمكن أن تكون في فقرات مختلفة.

 **Examples:** 

يوضح كيفية تقييد حقوق التحرير للنطاقات القابلة للتحرير لمجموعة/مستخدم معين.

```

 public void visitor() throws Exception {
     Document doc = new Document();
     doc.protect(ProtectionType.READ_ONLY, "MyPassword");

     DocumentBuilder builder = new DocumentBuilder(doc);
     builder.writeln("Hello world! Since we have set the document's protection level to read-only," +
             " we cannot edit this paragraph without the password.");

     // When we write-protect documents, editable ranges allow us to pick specific areas that users may edit.
     // There are two mutually exclusive ways to narrow down the list of allowed editors.
     // 1 -  Specify a user:
     EditableRange editableRange = builder.startEditableRange().getEditableRange();
     editableRange.setSingleUser("john.doe@myoffice.com");
     builder.writeln(MessageFormat.format("This paragraph is inside the first editable range, can only be edited by {0}.", editableRange.getSingleUser()));
     builder.endEditableRange();

     Assert.assertEquals(EditorType.UNSPECIFIED, editableRange.getEditorGroup());

     // 2 -  Specify a group that allowed users are associated with:
     editableRange = builder.startEditableRange().getEditableRange();
     editableRange.setEditorGroup(EditorType.ADMINISTRATORS);
     builder.writeln(MessageFormat.format("This paragraph is inside the first editable range, can only be edited by {0}.", editableRange.getEditorGroup()));
     builder.endEditableRange();

     Assert.assertEquals("", editableRange.getSingleUser());

     builder.writeln("This paragraph is outside the editable range, and cannot be edited by anybody.");

     // Print details and contents of every editable range in the document.
     EditableRangePrinter editableRangePrinter = new EditableRangePrinter();

     doc.accept(editableRangePrinter);

     System.out.println(editableRangePrinter.toText());
 }

 /// 
 /// Collects properties and contents of visited editable ranges in a string.
 /// 
 public static class EditableRangePrinter extends DocumentVisitor {
     public EditableRangePrinter() {
         mBuilder = new StringBuilder();
     }

     public String toText() {
         return mBuilder.toString();
     }

     public void reset() {
         mBuilder.setLength(0);
         mInsideEditableRange = false;
     }

     /// 
     /// Called when an EditableRangeStart node is encountered in the document.
     /// 
     public int visitEditableRangeStart(EditableRangeStart editableRangeStart) {
         mBuilder.append(" -- Editable range found! -- ");
         mBuilder.append("\tID:\t\t" + editableRangeStart.getId());
         if (editableRangeStart.getEditableRange().getSingleUser().equals(""))
             mBuilder.append("\tGroup:\t" + editableRangeStart.getEditableRange().getEditorGroup());
         else
             mBuilder.append("\tUser:\t" + editableRangeStart.getEditableRange().getSingleUser());
         mBuilder.append("\tContents:");

         mInsideEditableRange = true;

         return VisitorAction.CONTINUE;
     }

     /// 
     /// Called when an EditableRangeEnd node is encountered in the document.
     /// 
     public int visitEditableRangeEnd(final EditableRangeEnd editableRangeEnd) {
         mBuilder.append(" -- End of editable range -- " + "\r\n");

         mInsideEditableRange = false;

         return VisitorAction.CONTINUE;
     }

     /// 
     /// Called when a Run node is encountered in the document. This visitor only records runs that are inside editable ranges.
     /// 
     public int visitRun(final Run run) {
         if (mInsideEditableRange) {
             mBuilder.append("\t\"" + run.getText() + "\"" + "\r\n");
         }

         return VisitorAction.CONTINUE;
     }

     private boolean mInsideEditableRange;
     private final StringBuilder mBuilder;
 }
 
```


[Aspose.Words Document Object Model _DOM_]: https://docs.aspose.com/words/java/aspose-words-document-object-model/
## الطرق

| طريقة | الوصف |
| --- | --- |
| [accept(DocumentVisitor visitor)](#accept-com.aspose.words.DocumentVisitor) | يقبل زائرًا. |
| [deepClone(boolean isCloneChildren)](#deepClone-boolean) | ينشئ نسخة مكررة من العقدة. |
| [getAncestor(int ancestorType)](#getAncestor-int) |  |
| [getAncestor(Class ancestorType)](#getAncestor-java.lang.Class) | يحصل على السلف الأول لنوع الكائن المحدد. |
| [getCustomNodeId()](#getCustomNodeId) | يحدد معرف عقدة مخصص. |
| [getDisplacedByCustomXml()](#getDisplacedByCustomXml) |  |
| [getDocument()](#getDocument) | يحصل على المستند الذي تنتمي إليه هذه العقدة. |
| [getEditableRangeStart()](#getEditableRangeStart) | [EditableRangeStart](../../com.aspose.words/editablerangestart/) المقابل، يتم استلامه بالمعرف. |
| [getId()](#getId) | يحدد معرف النطاق القابل للتحرير. |
| [getIdInternal()](#getIdInternal) |  |
| [getNextSibling()](#getNextSibling) | يحصل على العقدة التي تلي هذه العقدة مباشرةً. |
| [getNodeType()](#getNodeType) | يرجع [NodeType.EDITABLE\_RANGE\_END](../../com.aspose.words/nodetype/\#EDITABLE-RANGE-END). |
| [getParentIdInternal()](#getParentIdInternal) |  |
| [getParentNode()](#getParentNode) | يحصل على الوالد المباشر لهذه العقدة. |
| [getPreviousSibling()](#getPreviousSibling) | يحصل على العقدة التي تسبق هذه العقدة مباشرةً. |
| [getRange()](#getRange) | يعيد كائن [Range](../../com.aspose.words/range/) الذي يمثل الجزء من المستند الموجود في هذه العقدة. |
| [getText()](#getText) | يحصل على نص هذه العقدة وجميع أبنائها. |
| [isComposite()](#isComposite) | يعيد  true  إذا كان بإمكان هذه العقدة احتواء عقد أخرى. |
| [nextPreOrder(Node rootNode)](#nextPreOrder-com.aspose.words.Node) | يحصل على العقدة التالية وفقًا لخوارزمية استعراض الشجرة بترتيب ما قبل. |
| [nodeTypeToString(int nodeType)](#nodeTypeToString-int) |  |
| [previousPreOrder(Node rootNode)](#previousPreOrder-com.aspose.words.Node) | يحصل على العقدة السابقة وفقًا لخوارزمية استعراض الشجرة بترتيب ما قبل الترتيب. |
| [remove()](#remove) | يزيل نفسه من العنصر الأصل. |
| [setCustomNodeId(int value)](#setCustomNodeId-int) | يحدد معرف عقدة مخصص. |
| [setDisplacedByCustomXml(int value)](#setDisplacedByCustomXml-int) |  |
| [setId(int value)](#setId-int) | يحدد معرف النطاق القابل للتحرير. |
| [setIdInternal(int value)](#setIdInternal-int) |  |
| [setParentIdInternal(int value)](#setParentIdInternal-int) |  |
| [toString()](#toString) |  |
| [toString(SaveOptions saveOptions)](#toString-com.aspose.words.SaveOptions) | يصدّر محتوى العقدة إلى سلسلة نصية باستخدام خيارات الحفظ المحددة. |
| [toString(int saveFormat)](#toString-int) |  |
### accept(DocumentVisitor visitor) {#accept-com.aspose.words.DocumentVisitor}
```
public boolean accept(DocumentVisitor visitor)
```


يقبل زائرًا.

 **Remarks:** 

ينادي [DocumentVisitor.visitEditableRangeEnd(com.aspose.words.EditableRangeEnd)](../../com.aspose.words/documentvisitor/\#visitEditableRangeEnd-com.aspose.words.EditableRangeEnd).

لمزيد من المعلومات راجع نمط التصميم Visitor.

 **Examples:** 

يوضح كيفية تقييد حقوق التحرير للنطاقات القابلة للتحرير لمجموعة/مستخدم معين.

```

 public void visitor() throws Exception {
     Document doc = new Document();
     doc.protect(ProtectionType.READ_ONLY, "MyPassword");

     DocumentBuilder builder = new DocumentBuilder(doc);
     builder.writeln("Hello world! Since we have set the document's protection level to read-only," +
             " we cannot edit this paragraph without the password.");

     // When we write-protect documents, editable ranges allow us to pick specific areas that users may edit.
     // There are two mutually exclusive ways to narrow down the list of allowed editors.
     // 1 -  Specify a user:
     EditableRange editableRange = builder.startEditableRange().getEditableRange();
     editableRange.setSingleUser("john.doe@myoffice.com");
     builder.writeln(MessageFormat.format("This paragraph is inside the first editable range, can only be edited by {0}.", editableRange.getSingleUser()));
     builder.endEditableRange();

     Assert.assertEquals(EditorType.UNSPECIFIED, editableRange.getEditorGroup());

     // 2 -  Specify a group that allowed users are associated with:
     editableRange = builder.startEditableRange().getEditableRange();
     editableRange.setEditorGroup(EditorType.ADMINISTRATORS);
     builder.writeln(MessageFormat.format("This paragraph is inside the first editable range, can only be edited by {0}.", editableRange.getEditorGroup()));
     builder.endEditableRange();

     Assert.assertEquals("", editableRange.getSingleUser());

     builder.writeln("This paragraph is outside the editable range, and cannot be edited by anybody.");

     // Print details and contents of every editable range in the document.
     EditableRangePrinter editableRangePrinter = new EditableRangePrinter();

     doc.accept(editableRangePrinter);

     System.out.println(editableRangePrinter.toText());
 }

 /// 
 /// Collects properties and contents of visited editable ranges in a string.
 /// 
 public static class EditableRangePrinter extends DocumentVisitor {
     public EditableRangePrinter() {
         mBuilder = new StringBuilder();
     }

     public String toText() {
         return mBuilder.toString();
     }

     public void reset() {
         mBuilder.setLength(0);
         mInsideEditableRange = false;
     }

     /// 
     /// Called when an EditableRangeStart node is encountered in the document.
     /// 
     public int visitEditableRangeStart(EditableRangeStart editableRangeStart) {
         mBuilder.append(" -- Editable range found! -- ");
         mBuilder.append("\tID:\t\t" + editableRangeStart.getId());
         if (editableRangeStart.getEditableRange().getSingleUser().equals(""))
             mBuilder.append("\tGroup:\t" + editableRangeStart.getEditableRange().getEditorGroup());
         else
             mBuilder.append("\tUser:\t" + editableRangeStart.getEditableRange().getSingleUser());
         mBuilder.append("\tContents:");

         mInsideEditableRange = true;

         return VisitorAction.CONTINUE;
     }

     /// 
     /// Called when an EditableRangeEnd node is encountered in the document.
     /// 
     public int visitEditableRangeEnd(final EditableRangeEnd editableRangeEnd) {
         mBuilder.append(" -- End of editable range -- " + "\r\n");

         mInsideEditableRange = false;

         return VisitorAction.CONTINUE;
     }

     /// 
     /// Called when a Run node is encountered in the document. This visitor only records runs that are inside editable ranges.
     /// 
     public int visitRun(final Run run) {
         if (mInsideEditableRange) {
             mBuilder.append("\t\"" + run.getText() + "\"" + "\r\n");
         }

         return VisitorAction.CONTINUE;
     }

     private boolean mInsideEditableRange;
     private final StringBuilder mBuilder;
 }
 
```

**Parameters:**
| معامل | نوع | الوصف |
| --- | --- | --- |
| visitor | [DocumentVisitor](../../com.aspose.words/documentvisitor/) | الزائر الذي سيزور العقدة. |

**Returns:**
منطقي - false إذا طلب الزائر إيقاف التعداد.
### deepClone(boolean isCloneChildren) {#deepClone-boolean}
```
public Node deepClone(boolean isCloneChildren)
```


ينشئ نسخة مكررة من العقدة.

 **Remarks:** 

هذه الطريقة تعمل كمنشئ نسخ للعقد. العقدة المستنسخة لا تمتلك عنصرًا أصليًا، لكنها تنتمي إلى نفس المستند مثل العقدة الأصلية.

هذه الطريقة دائمًا تنفّذ نسخة عميقة من العقدة. المعامل  isCloneChildren  يحدد ما إذا كان يجب نسخ جميع العقد الفرعية أيضًا.

 **Examples:** 

يوضح كيفية استنساخ عقدة مركبة.

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
| معامل | نوع | الوصف |
| --- | --- | --- |
| isCloneChildren | boolean | صحيح لاستنساخ الشجرة الفرعية تحت العقدة المحددة بشكل متكرر؛ خطأ لاستنساخ العقدة نفسها فقط. |

**Returns:**
[Node](../../com.aspose.words/node/) - The cloned node.
### getAncestor(int ancestorType) {#getAncestor-int}
```
public CompositeNode getAncestor(int ancestorType)
```




**Parameters:**
| معامل | نوع | الوصف |
| --- | --- | --- |
| ancestorType | int |  |

**Returns:**
[CompositeNode](../../com.aspose.words/compositenode/)
### getAncestor(Class ancestorType) {#getAncestor-java.lang.Class}
```
public CompositeNode getAncestor(Class ancestorType)
```


يحصل على السلف الأول لنوع الكائن المحدد.

 **Remarks:** 

يتطابق نوع السلف إذا كان مساويًا لـ  ancestorType  أو مشتقًا من  ancestorType .

 **Examples:** 

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

**Parameters:**
| معامل | نوع | الوصف |
| --- | --- | --- |
| ancestorType | java.lang.Class | نوع الكائن للسلف الذي سيتم استرجاعه. |

**Returns:**
[CompositeNode](../../com.aspose.words/compositenode/) - The ancestor of the specified type or  null  if no ancestor of this type was found.
### getCustomNodeId() {#getCustomNodeId}
```
public int getCustomNodeId()
```


يحدد معرف عقدة مخصص.

 **Remarks:** 

القيمة الافتراضية هي صفر.

يمكن تعيين هذا المعرف واستخدامه بحرية. على سبيل المثال، كمفتاح للحصول على بيانات خارجية.

ملاحظة مهمة، القيمة المحددة لا تُحفظ في ملف الإخراج وتوجد فقط خلال عمر العقدة.

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

**Returns:**
int - القيمة المقابلة  int .
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


يحصل على المستند الذي تنتمي إليه هذه العقدة.

 **Remarks:** 

العقدة دائمًا تنتمي إلى مستند حتى إذا تم إنشاؤها للتو ولم تُضاف بعد إلى الشجرة، أو إذا تمت إزالتها من الشجرة.

 **Examples:** 

يوضح كيفية إنشاء عقدة وتعيين المستند المالك لها.

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
### getEditableRangeStart() {#getEditableRangeStart}
```
public EditableRangeStart getEditableRangeStart()
```


[EditableRangeStart](../../com.aspose.words/editablerangestart/) المقابل، يتم استلامه بالمعرف.

 **Examples:** 

يوضح كيفية العمل مع نطاق قابل للتحرير.

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
[EditableRangeStart](../../com.aspose.words/editablerangestart/) - The corresponding [EditableRangeStart](../../com.aspose.words/editablerangestart/) value.
### getId() {#getId}
```
public int getId()
```


يحدد معرف النطاق القابل للتحرير.

 **Examples:** 

يوضح كيفية العمل مع نطاق قابل للتحرير.

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
int - القيمة المقابلة  int .
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


يحصل على العقدة التي تلي هذه العقدة مباشرةً.

 **Remarks:** 

إذا لم يكن هناك عقدة تالية، يتم إرجاع  null  .

 **Examples:** 

يوضح كيفية استعراض شجرة العقد الفرعية لعقدة مركبة.

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

يوضح كيفية استخدام خاصية NextSibling للعقدة لتعداد أطفالها المباشرين.

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


يرجع [NodeType.EDITABLE\_RANGE\_END](../../com.aspose.words/nodetype/\#EDITABLE-RANGE-END).

 **Examples:** 

يوضح كيفية العمل مع نطاق قابل للتحرير.

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
int - [NodeType.EDITABLE\_RANGE\_END](../../com.aspose.words/nodetype/\#EDITABLE-RANGE-END). القيمة المرجعة هي واحدة من ثوابت [NodeType](../../com.aspose.words/nodetype/).
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


يحصل على الوالد المباشر لهذه العقدة.

 **Remarks:** 

إذا تم إنشاء عقدة للتو ولم تُضاف بعد إلى الشجرة، أو إذا أُزيلت من الشجرة، فإن الأصل هو  null .

 **Examples:** 

يوضح كيفية الوصول إلى عقدة الأصل للعقدة.

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

يوضح كيفية إنشاء عقدة وتعيين المستند المالك لها.

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


يحصل على العقدة التي تسبق هذه العقدة مباشرةً.

 **Remarks:** 

إذا لم يكن هناك عقدة سابقة، يتم إرجاع  null  .

 **Examples:** 

يوضح كيفية استخدام طرق Node و CompositeNode لإزالة قسم قبل القسم الأخير في المستند.

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


يعيد كائن [Range](../../com.aspose.words/range/) الذي يمثل الجزء من المستند الموجود في هذه العقدة.

 **Examples:** 

يوضح كيفية حذف جميع العقد من نطاق.

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


يحصل على نص هذه العقدة وجميع أبنائها.

 **Remarks:** 

السلسلة المرجعة تشمل جميع أحرف التحكم والرموز الخاصة كما هو موضح في [ControlChar](../../com.aspose.words/controlchar/).

 **Examples:** 

يوضح كيفية استخدام أحرف التحكم.

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

يوضح كيفية إنشاء مستند Aspose.Words يدوياً.

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


يرجع  true  إذا كان بإمكان هذه العقدة احتواء عقد أخرى. (197141,6)

 **Examples:** 

يوضح كيفية استعراض شجرة العقد الفرعية لعقدة مركبة.

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
boolean -  true  إذا كان بإمكان هذه العقدة احتواء عقد أخرى.
### nextPreOrder(Node rootNode) {#nextPreOrder-com.aspose.words.Node}
```
public Node nextPreOrder(Node rootNode)
```


يحصل على العقدة التالية وفقًا لخوارزمية استعراض الشجرة بترتيب ما قبل.

 **Examples:** 

يوضح كيفية استعراض شجرة عقد المستند باستخدام خوارزمية الاستعراض قبل الترتيب، وحذف أي شكل يتم مواجهته يحتوي على صورة.

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
| معامل | نوع | الوصف |
| --- | --- | --- |
| rootNode | [Node](../../com.aspose.words/node/) | العقدة العليا (الحد) للاستعراض. |

**Returns:**
[Node](../../com.aspose.words/node/) - Next node in pre-order order. Null if reached the  rootNode .
### nodeTypeToString(int nodeType) {#nodeTypeToString-int}
```
public static String nodeTypeToString(int nodeType)
```




**Parameters:**
| معامل | نوع | الوصف |
| --- | --- | --- |
| nodeType | int |  |

**Returns:**
java.lang.String
### previousPreOrder(Node rootNode) {#previousPreOrder-com.aspose.words.Node}
```
public Node previousPreOrder(Node rootNode)
```


يحصل على العقدة السابقة وفقًا لخوارزمية استعراض الشجرة بترتيب ما قبل الترتيب.

 **Examples:** 

يوضح كيفية استعراض شجرة عقد المستند باستخدام خوارزمية الاستعراض قبل الترتيب، وحذف أي شكل يتم مواجهته يحتوي على صورة.

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
| معامل | نوع | الوصف |
| --- | --- | --- |
| rootNode | [Node](../../com.aspose.words/node/) | العقدة العليا (الحد) للاستعراض. |

**Returns:**
[Node](../../com.aspose.words/node/) - Previous node in pre-order order. Null if reached the  rootNode .
### remove() {#remove}
```
public void remove()
```


يزيل نفسه من العنصر الأصل.

 **Examples:** 

يوضح كيفية حذف جميع الأشكال التي تحتوي على صور من مستند.

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

يوضح كيفية إزالة جميع العقد الفرعية من نوع معين من عقدة مركبة.

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


يحدد معرف عقدة مخصص.

 **Remarks:** 

القيمة الافتراضية هي صفر.

يمكن تعيين هذا المعرف واستخدامه بحرية. على سبيل المثال، كمفتاح للحصول على بيانات خارجية.

ملاحظة مهمة، القيمة المحددة لا تُحفظ في ملف الإخراج وتوجد فقط خلال عمر العقدة.

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

**Parameters:**
| معامل | نوع | الوصف |
| --- | --- | --- |
| قيمة | int | القيمة  int  المقابلة. |

### setDisplacedByCustomXml(int value) {#setDisplacedByCustomXml-int}
```
public void setDisplacedByCustomXml(int value)
```




**Parameters:**
| معامل | نوع | الوصف |
| --- | --- | --- |
| قيمة | int |  |

### setId(int value) {#setId-int}
```
public void setId(int value)
```


يحدد معرف النطاق القابل للتحرير.

 **Examples:** 

يوضح كيفية العمل مع نطاق قابل للتحرير.

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

**Parameters:**
| معامل | نوع | الوصف |
| --- | --- | --- |
| قيمة | int | القيمة  int  المقابلة. |

### setIdInternal(int value) {#setIdInternal-int}
```
public void setIdInternal(int value)
```




**Parameters:**
| معامل | نوع | الوصف |
| --- | --- | --- |
| قيمة | int |  |

### setParentIdInternal(int value) {#setParentIdInternal-int}
```
public void setParentIdInternal(int value)
```




**Parameters:**
| معامل | نوع | الوصف |
| --- | --- | --- |
| قيمة | int |  |

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


يصدّر محتوى العقدة إلى سلسلة نصية باستخدام خيارات الحفظ المحددة.

 **Examples:** 

يصدّر محتوى عقدة إلى String بتنسيق HTML.

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
| معامل | نوع | الوصف |
| --- | --- | --- |
| saveOptions | [SaveOptions](../../com.aspose.words/saveoptions/) | يحدد الخيارات التي تتحكم في كيفية حفظ العقدة. |

**Returns:**
java.lang.String - محتوى العقدة بالتنسيق المحدد.
### toString(int saveFormat) {#toString-int}
```
public String toString(int saveFormat)
```




**Parameters:**
| معامل | نوع | الوصف |
| --- | --- | --- |
| saveFormat | int |  |

**Returns:**
java.lang.String
