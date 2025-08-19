---
title: HeaderFooterCollection
linktitle: HeaderFooterCollection
second_title: Aspose.Words for Java
description: Provides typed access to HeaderFooter nodes of a Section in Java.
type: docs
weight: 367
url: /java/com.aspose.words/headerfootercollection/
---

**Inheritance:**
java.lang.Object, [com.aspose.words.NodeCollection](../../com.aspose.words/nodecollection/)
```
public class HeaderFooterCollection extends NodeCollection
```

Provides typed access to [HeaderFooter](../../com.aspose.words/headerfooter/) nodes of a [Section](../../com.aspose.words/section/).

To learn more, visit the [ Working with Headers and Footers ][Working with Headers and Footers] documentation article.

 **Remarks:** 

There can be maximum of one [HeaderFooter](../../com.aspose.words/headerfooter/)

of each [HeaderFooterType](../../com.aspose.words/headerfootertype/) per [Section](../../com.aspose.words/section/).

[HeaderFooter](../../com.aspose.words/headerfooter/) objects can occur in any order in the collection.

 **Examples:** 

Shows how to delete all footers from a document.

```

 Document doc = new Document(getMyDir() + "Header and footer types.docx");

 // Iterate through each section and remove footers of every kind.
 for (Section section : doc.getSections()) {
     // There are three kinds of footer and header types.
     // 1 -  The "First" header/footer, which only appears on the first page of a section.
     HeaderFooter footer = section.getHeadersFooters().getByHeaderFooterType(HeaderFooterType.FOOTER_FIRST);
     if (footer != null) {
         footer.remove();
     }

     // 2 -  The "Primary" header/footer, which appears on odd pages.
     footer = section.getHeadersFooters().getByHeaderFooterType(HeaderFooterType.FOOTER_PRIMARY);
     if (footer != null) {
         footer.remove();
     }

     // 3 -  The "Even" header/footer, which appears on even pages.
     footer = section.getHeadersFooters().getByHeaderFooterType(HeaderFooterType.FOOTER_EVEN);
     if (footer != null) {
         footer.remove();
     }

     Assert.assertEquals(0, IterableUtils.countMatches(section.getHeadersFooters(), s -> !s.isHeader()));
 }

 doc.save(getArtifactsDir() + "HeaderFooter.RemoveFooters.docx");
 
```

Shows how to create a header and a footer.

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


[Working with Headers and Footers]: https://docs.aspose.com/words/java/working-with-headers-and-footers/
## Methods

| Method | Description |
| --- | --- |
| [add(Node node)](#add-com.aspose.words.Node) | Adds a node to the end of the collection. |
| [clear()](#clear) | Removes all nodes from this collection and from the document. |
| [contains(Node node)](#contains-com.aspose.words.Node) | Determines whether a node is in the collection. |
| [get(int index)](#get-int) | Retrieves a [HeaderFooter](../../com.aspose.words/headerfooter/) at the given index. |
| [getByHeaderFooterType(int headerFooterType)](#getByHeaderFooterType-int) |  |
| [getContainer()](#getContainer) |  |
| [getCount()](#getCount) | Gets the number of nodes in the collection. |
| [getCurrentNode()](#getCurrentNode) |  |
| [getNextMatchingNode(Node curNode)](#getNextMatchingNode-com.aspose.words.Node) |  |
| [indexOf(Node node)](#indexOf-com.aspose.words.Node) | Returns the zero-based index of the specified node. |
| [insert(int index, Node node)](#insert-int-com.aspose.words.Node) | Inserts a node into the collection at the specified index. |
| [iterator()](#iterator) | Provides a simple "foreach" style iteration over the collection of nodes. |
| [linkToPrevious(boolean isLinkToPrevious)](#linkToPrevious-boolean) | Links or unlinks all headers and footers to the corresponding headers and footers in the previous section. |
| [linkToPrevious(int headerFooterType, boolean isLinkToPrevious)](#linkToPrevious-int-boolean) |  |
| [remove(Node node)](#remove-com.aspose.words.Node) | Removes the node from the collection and from the document. |
| [removeAt(int index)](#removeAt-int) | Removes the node at the specified index from the collection and from the document. |
| [toArray()](#toArray) | Copies all  HeaderFooter  s from the collection to a new array of  HeaderFooter  s. |
### add(Node node) {#add-com.aspose.words.Node}
```
public void add(Node node)
```


Adds a node to the end of the collection.

**Parameters:**
| Parameter | Type | Description |
| --- | --- | --- |
| node | [Node](../../com.aspose.words/node/) | The node to be added to the end of the collection. |

### clear() {#clear}
```
public void clear()
```


Removes all nodes from this collection and from the document.

 **Examples:** 

Shows how to remove all sections from a document.

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


Determines whether a node is in the collection.

 **Remarks:** 

This method performs a linear search; therefore, the average execution time is proportional to [getCount()](../../com.aspose.words/nodecollection/\#getCount).

 **Examples:** 

Shows how to work with a NodeCollection.

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
| Parameter | Type | Description |
| --- | --- | --- |
| node | [Node](../../com.aspose.words/node/) | The node to locate. |

**Returns:**
boolean -  true  if item is found in the collection; otherwise,  false .
### get(int index) {#get-int}
```
public Node get(int index)
```


Retrieves a [HeaderFooter](../../com.aspose.words/headerfooter/) at the given index.

 **Remarks:** 

The index is zero-based.

Negative indexes are allowed and indicate access from the back of the collection. For example -1 means the last item, -2 means the second before last and so on.

If index is greater than or equal to the number of items in the list, this returns a null reference.

If index is negative and its absolute value is greater than the number of items in the list, this returns a null reference.

 **Examples:** 

Shows how to link headers and footers between sections.

```

 Document doc = new Document();
 DocumentBuilder builder = new DocumentBuilder(doc);

 builder.write("Section 1");
 builder.insertBreak(BreakType.SECTION_BREAK_NEW_PAGE);
 builder.write("Section 2");
 builder.insertBreak(BreakType.SECTION_BREAK_NEW_PAGE);
 builder.write("Section 3");

 // Move to the first section and create a header and a footer. By default,
 // the header and the footer will only appear on pages in the section that contains them.
 builder.moveToSection(0);

 builder.moveToHeaderFooter(HeaderFooterType.HEADER_PRIMARY);
 builder.write("This is the header, which will be displayed in sections 1 and 2.");

 builder.moveToHeaderFooter(HeaderFooterType.FOOTER_PRIMARY);
 builder.write("This is the footer, which will be displayed in sections 1, 2 and 3.");

 // We can link a section's headers/footers to the previous section's headers/footers
 // to allow the linking section to display the linked section's headers/footers.
 doc.getSections().get(1).getHeadersFooters().linkToPrevious(true);

 // Each section will still have its own header/footer objects. When we link sections,
 // the linking section will display the linked section's header/footers while keeping its own.
 Assert.assertNotEquals(doc.getSections().get(0).getHeadersFooters().get(0), doc.getSections().get(1).getHeadersFooters().get(0));
 Assert.assertNotEquals(doc.getSections().get(0).getHeadersFooters().get(0).getParentSection(), doc.getSections().get(1).getHeadersFooters().get(0).getParentSection());

 // Link the headers/footers of the third section to the headers/footers of the second section.
 // The second section already links to the first section's header/footers,
 // so linking to the second section will create a link chain.
 // The first, second, and now the third sections will all display the first section's headers.
 doc.getSections().get(2).getHeadersFooters().linkToPrevious(true);

 // We can un-link a previous section's header/footers by passing "false" when calling the LinkToPrevious method.
 doc.getSections().get(2).getHeadersFooters().linkToPrevious(false);

 // We can also select only a specific type of header/footer to link using this method.
 // The third section now will have the same footer as the second and first sections, but not the header.
 doc.getSections().get(2).getHeadersFooters().linkToPrevious(HeaderFooterType.FOOTER_PRIMARY, true);

 // The first section's header/footers cannot link themselves to anything because there is no previous section.
 Assert.assertEquals(2, doc.getSections().get(0).getHeadersFooters().getCount());
 Assert.assertEquals(0, IterableUtils.countMatches(doc.getSections().get(0).getHeadersFooters(), s -> s.isLinkedToPrevious()));

 // All the second section's header/footers are linked to the first section's headers/footers.
 Assert.assertEquals(6, doc.getSections().get(1).getHeadersFooters().getCount());
 Assert.assertEquals(6, IterableUtils.countMatches(doc.getSections().get(1).getHeadersFooters(), s -> s.isLinkedToPrevious()));

 // In the third section, only the footer is linked to the first section's footer via the second section.
 Assert.assertEquals(6, doc.getSections().get(2).getHeadersFooters().getCount());
 Assert.assertEquals(1, IterableUtils.countMatches(doc.getSections().get(2).getHeadersFooters(), s -> s.isLinkedToPrevious()));
 Assert.assertTrue(doc.getSections().get(2).getHeadersFooters().get(3).isLinkedToPrevious());

 doc.save(getArtifactsDir() + "HeaderFooter.Link.docx");
 
```

**Parameters:**
| Parameter | Type | Description |
| --- | --- | --- |
| index | int | An index into the collection. |

**Returns:**
[Node](../../com.aspose.words/node/) - The corresponding [HeaderFooter](../../com.aspose.words/headerfooter/) value.
### getByHeaderFooterType(int headerFooterType) {#getByHeaderFooterType-int}
```
public HeaderFooter getByHeaderFooterType(int headerFooterType)
```




**Parameters:**
| Parameter | Type | Description |
| --- | --- | --- |
| headerFooterType | int |  |

**Returns:**
[HeaderFooter](../../com.aspose.words/headerfooter/)
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


Gets the number of nodes in the collection.

 **Examples:** 

Shows how to traverse through a composite node's collection of child nodes.

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

Shows how to find out if a tables are nested.

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
int - The number of nodes in the collection.
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
| Parameter | Type | Description |
| --- | --- | --- |
| curNode | [Node](../../com.aspose.words/node/) |  |

**Returns:**
[Node](../../com.aspose.words/node/)
### indexOf(Node node) {#indexOf-com.aspose.words.Node}
```
public int indexOf(Node node)
```


Returns the zero-based index of the specified node.

 **Remarks:** 

This method performs a linear search; therefore, the average execution time is proportional to [getCount()](../../com.aspose.words/nodecollection/\#getCount).

 **Examples:** 

Shows how to get the index of a node in a collection.

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
| Parameter | Type | Description |
| --- | --- | --- |
| node | [Node](../../com.aspose.words/node/) | The node to locate. |

**Returns:**
int - The zero-based index of the node within the collection, if found; otherwise, -1.
### insert(int index, Node node) {#insert-int-com.aspose.words.Node}
```
public void insert(int index, Node node)
```


Inserts a node into the collection at the specified index.

**Parameters:**
| Parameter | Type | Description |
| --- | --- | --- |
| index | int | The zero-based index of the node. Negative indexes are allowed and indicate access from the back of the list. For example -1 means the last node, -2 means the second before last and so on. |
| node | [Node](../../com.aspose.words/node/) | The node to insert. |

### iterator() {#iterator}
```
public Iterator iterator()
```


Provides a simple "foreach" style iteration over the collection of nodes.

**Returns:**
java.util.Iterator - An Iterator.
### linkToPrevious(boolean isLinkToPrevious) {#linkToPrevious-boolean}
```
public void linkToPrevious(boolean isLinkToPrevious)
```


Links or unlinks all headers and footers to the corresponding headers and footers in the previous section.

 **Remarks:** 

If any of the headers or footers do not exist, creates them automatically.

 **Examples:** 

Shows how to link headers and footers between sections.

```

 Document doc = new Document();
 DocumentBuilder builder = new DocumentBuilder(doc);

 builder.write("Section 1");
 builder.insertBreak(BreakType.SECTION_BREAK_NEW_PAGE);
 builder.write("Section 2");
 builder.insertBreak(BreakType.SECTION_BREAK_NEW_PAGE);
 builder.write("Section 3");

 // Move to the first section and create a header and a footer. By default,
 // the header and the footer will only appear on pages in the section that contains them.
 builder.moveToSection(0);

 builder.moveToHeaderFooter(HeaderFooterType.HEADER_PRIMARY);
 builder.write("This is the header, which will be displayed in sections 1 and 2.");

 builder.moveToHeaderFooter(HeaderFooterType.FOOTER_PRIMARY);
 builder.write("This is the footer, which will be displayed in sections 1, 2 and 3.");

 // We can link a section's headers/footers to the previous section's headers/footers
 // to allow the linking section to display the linked section's headers/footers.
 doc.getSections().get(1).getHeadersFooters().linkToPrevious(true);

 // Each section will still have its own header/footer objects. When we link sections,
 // the linking section will display the linked section's header/footers while keeping its own.
 Assert.assertNotEquals(doc.getSections().get(0).getHeadersFooters().get(0), doc.getSections().get(1).getHeadersFooters().get(0));
 Assert.assertNotEquals(doc.getSections().get(0).getHeadersFooters().get(0).getParentSection(), doc.getSections().get(1).getHeadersFooters().get(0).getParentSection());

 // Link the headers/footers of the third section to the headers/footers of the second section.
 // The second section already links to the first section's header/footers,
 // so linking to the second section will create a link chain.
 // The first, second, and now the third sections will all display the first section's headers.
 doc.getSections().get(2).getHeadersFooters().linkToPrevious(true);

 // We can un-link a previous section's header/footers by passing "false" when calling the LinkToPrevious method.
 doc.getSections().get(2).getHeadersFooters().linkToPrevious(false);

 // We can also select only a specific type of header/footer to link using this method.
 // The third section now will have the same footer as the second and first sections, but not the header.
 doc.getSections().get(2).getHeadersFooters().linkToPrevious(HeaderFooterType.FOOTER_PRIMARY, true);

 // The first section's header/footers cannot link themselves to anything because there is no previous section.
 Assert.assertEquals(2, doc.getSections().get(0).getHeadersFooters().getCount());
 Assert.assertEquals(0, IterableUtils.countMatches(doc.getSections().get(0).getHeadersFooters(), s -> s.isLinkedToPrevious()));

 // All the second section's header/footers are linked to the first section's headers/footers.
 Assert.assertEquals(6, doc.getSections().get(1).getHeadersFooters().getCount());
 Assert.assertEquals(6, IterableUtils.countMatches(doc.getSections().get(1).getHeadersFooters(), s -> s.isLinkedToPrevious()));

 // In the third section, only the footer is linked to the first section's footer via the second section.
 Assert.assertEquals(6, doc.getSections().get(2).getHeadersFooters().getCount());
 Assert.assertEquals(1, IterableUtils.countMatches(doc.getSections().get(2).getHeadersFooters(), s -> s.isLinkedToPrevious()));
 Assert.assertTrue(doc.getSections().get(2).getHeadersFooters().get(3).isLinkedToPrevious());

 doc.save(getArtifactsDir() + "HeaderFooter.Link.docx");
 
```

**Parameters:**
| Parameter | Type | Description |
| --- | --- | --- |
| isLinkToPrevious | boolean |  true  to link the headers and footers to the previous section;  false  to unlink them. |

### linkToPrevious(int headerFooterType, boolean isLinkToPrevious) {#linkToPrevious-int-boolean}
```
public void linkToPrevious(int headerFooterType, boolean isLinkToPrevious)
```




**Parameters:**
| Parameter | Type | Description |
| --- | --- | --- |
| headerFooterType | int |  |
| isLinkToPrevious | boolean |  |

### remove(Node node) {#remove-com.aspose.words.Node}
```
public void remove(Node node)
```


Removes the node from the collection and from the document.

 **Examples:** 

Shows how to work with a NodeCollection.

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
| Parameter | Type | Description |
| --- | --- | --- |
| node | [Node](../../com.aspose.words/node/) | The node to remove. |

### removeAt(int index) {#removeAt-int}
```
public void removeAt(int index)
```


Removes the node at the specified index from the collection and from the document.

 **Examples:** 

Shows how to add and remove sections in a document.

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
| Parameter | Type | Description |
| --- | --- | --- |
| index | int | The zero-based index of the node. Negative indexes are allowed and indicate access from the back of the list. For example -1 means the last node, -2 means the second before last and so on. |

### toArray() {#toArray}
```
public HeaderFooter[] toArray()
```


Copies all  HeaderFooter  s from the collection to a new array of  HeaderFooter  s.

 **Examples:** 

Shows how to print the node structure of every header and footer in a document.

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

**Returns:**
com.aspose.words.HeaderFooter[] - An array of  HeaderFooter  s.
