---
title: LayoutCollector
linktitle: LayoutCollector
second_title: Aspose.Words for Java
description: This class allows to compute page numbers of document nodes in Java.
type: docs
weight: 389
url: /java/com.aspose.words/layoutcollector/
---

**Inheritance:**
java.lang.Object
```
public class LayoutCollector
```

This class allows to compute page numbers of document nodes.

To learn more, visit the [ Converting to Fixed-page Format ][Converting to Fixed-page Format] documentation article.

 **Remarks:** 

When you create a [LayoutCollector](../../com.aspose.words/layoutcollector/) and specify a [Document](../../com.aspose.words/document/) document object to attach to, the collector will record mapping of document nodes to layout objects when the document is formatted into pages.

You will be able to find out on which page a particular document node (e.g. run, paragraph or table cell) is located by using the [getStartPageIndex(com.aspose.words.Node)](../../com.aspose.words/layoutcollector/\#getStartPageIndex-com.aspose.words.Node), [getEndPageIndex(com.aspose.words.Node)](../../com.aspose.words/layoutcollector/\#getEndPageIndex-com.aspose.words.Node) and [getNumPagesSpanned(com.aspose.words.Node)](../../com.aspose.words/layoutcollector/\#getNumPagesSpanned-com.aspose.words.Node) methods. These methods automatically build page layout model of the document and update fields if required.

When you no longer need to collect layout information, it is best to set the [getDocument()](../../com.aspose.words/layoutcollector/\#getDocument) / [setDocument(com.aspose.words.Document)](../../com.aspose.words/layoutcollector/\#setDocument-com.aspose.words.Document) property to  null  to avoid unnecessary collection of more layout mappings.

 **Examples:** 

Shows how to see the the ranges of pages that a node spans.

```

 Document doc = new Document();
 LayoutCollector layoutCollector = new LayoutCollector(doc);

 // Call the "GetNumPagesSpanned" method to count how many pages the content of our document spans.
 // Since the document is empty, that number of pages is currently zero.
 Assert.assertEquals(doc, layoutCollector.getDocument());
 Assert.assertEquals(0, layoutCollector.getNumPagesSpanned(doc));

 // Populate the document with 5 pages of content.
 DocumentBuilder builder = new DocumentBuilder(doc);
 builder.write("Section 1");
 builder.insertBreak(BreakType.PAGE_BREAK);
 builder.insertBreak(BreakType.PAGE_BREAK);
 builder.insertBreak(BreakType.SECTION_BREAK_EVEN_PAGE);
 builder.write("Section 2");
 builder.insertBreak(BreakType.PAGE_BREAK);
 builder.insertBreak(BreakType.PAGE_BREAK);

 // Before the layout collector, we need to call the "UpdatePageLayout" method to give us
 // an accurate figure for any layout-related metric, such as the page count.
 Assert.assertEquals(0, layoutCollector.getNumPagesSpanned(doc));

 layoutCollector.clear();
 doc.updatePageLayout();

 Assert.assertEquals(5, layoutCollector.getNumPagesSpanned(doc));

 // We can see the numbers of the start and end pages of any node and their overall page spans.
 NodeCollection nodes = doc.getChildNodes(NodeType.ANY, true);
 for (Node node : (Iterable) nodes) {
     System.out.println(MessageFormat.format("->  NodeType.{0}: ", node.getNodeType()));
     System.out.println(MessageFormat.format("\tStarts on page {0}, ends on page {1},", layoutCollector.getStartPageIndex(node), layoutCollector.getEndPageIndex(node)) +
             MessageFormat.format(" spanning {0} pages.", layoutCollector.getNumPagesSpanned(node)));
 }

 // We can iterate over the layout entities using a LayoutEnumerator.
 LayoutEnumerator layoutEnumerator = new LayoutEnumerator(doc);

 Assert.assertEquals(LayoutEntityType.PAGE, layoutEnumerator.getType());

 // The LayoutEnumerator can traverse the collection of layout entities like a tree.
 // We can also apply it to any node's corresponding layout entity.
 layoutEnumerator.setCurrent(layoutCollector.getEntity(doc.getChild(NodeType.PARAGRAPH, 1, true)));

 Assert.assertEquals(LayoutEntityType.SPAN, layoutEnumerator.getType());
 Assert.assertEquals("�", layoutEnumerator.getText());
 
```


[Converting to Fixed-page Format]: https://docs.aspose.com/words/java/converting-to-fixed-page-format/
## Constructors

| Constructor | Description |
| --- | --- |
| [LayoutCollector(Document doc)](#LayoutCollector-com.aspose.words.Document) | Initializes an instance of this class. |
## Methods

| Method | Description |
| --- | --- |
| [clear()](#clear) | Clears all collected layout data. |
| [getDocument()](#getDocument) | Gets the document this collector instance is attached to. |
| [getEndPageIndex(Node node)](#getEndPageIndex-com.aspose.words.Node) | Gets 1-based index of the page where node ends. |
| [getEntity(Node node)](#getEntity-com.aspose.words.Node) | Returns an opaque position of the [LayoutEnumerator](../../com.aspose.words/layoutenumerator/) which corresponds to the specified node. |
| [getNumPagesSpanned(Node node)](#getNumPagesSpanned-com.aspose.words.Node) | Gets number of pages the specified node spans. |
| [getStartPageIndex(Node node)](#getStartPageIndex-com.aspose.words.Node) | Gets 1-based index of the page where node begins. |
| [setDocument(Document value)](#setDocument-com.aspose.words.Document) | Sets the document this collector instance is attached to. |
### LayoutCollector(Document doc) {#LayoutCollector-com.aspose.words.Document}
```
public LayoutCollector(Document doc)
```


Initializes an instance of this class.

 **Examples:** 

Shows how to see the the ranges of pages that a node spans.

```

 Document doc = new Document();
 LayoutCollector layoutCollector = new LayoutCollector(doc);

 // Call the "GetNumPagesSpanned" method to count how many pages the content of our document spans.
 // Since the document is empty, that number of pages is currently zero.
 Assert.assertEquals(doc, layoutCollector.getDocument());
 Assert.assertEquals(0, layoutCollector.getNumPagesSpanned(doc));

 // Populate the document with 5 pages of content.
 DocumentBuilder builder = new DocumentBuilder(doc);
 builder.write("Section 1");
 builder.insertBreak(BreakType.PAGE_BREAK);
 builder.insertBreak(BreakType.PAGE_BREAK);
 builder.insertBreak(BreakType.SECTION_BREAK_EVEN_PAGE);
 builder.write("Section 2");
 builder.insertBreak(BreakType.PAGE_BREAK);
 builder.insertBreak(BreakType.PAGE_BREAK);

 // Before the layout collector, we need to call the "UpdatePageLayout" method to give us
 // an accurate figure for any layout-related metric, such as the page count.
 Assert.assertEquals(0, layoutCollector.getNumPagesSpanned(doc));

 layoutCollector.clear();
 doc.updatePageLayout();

 Assert.assertEquals(5, layoutCollector.getNumPagesSpanned(doc));

 // We can see the numbers of the start and end pages of any node and their overall page spans.
 NodeCollection nodes = doc.getChildNodes(NodeType.ANY, true);
 for (Node node : (Iterable) nodes) {
     System.out.println(MessageFormat.format("->  NodeType.{0}: ", node.getNodeType()));
     System.out.println(MessageFormat.format("\tStarts on page {0}, ends on page {1},", layoutCollector.getStartPageIndex(node), layoutCollector.getEndPageIndex(node)) +
             MessageFormat.format(" spanning {0} pages.", layoutCollector.getNumPagesSpanned(node)));
 }

 // We can iterate over the layout entities using a LayoutEnumerator.
 LayoutEnumerator layoutEnumerator = new LayoutEnumerator(doc);

 Assert.assertEquals(LayoutEntityType.PAGE, layoutEnumerator.getType());

 // The LayoutEnumerator can traverse the collection of layout entities like a tree.
 // We can also apply it to any node's corresponding layout entity.
 layoutEnumerator.setCurrent(layoutCollector.getEntity(doc.getChild(NodeType.PARAGRAPH, 1, true)));

 Assert.assertEquals(LayoutEntityType.SPAN, layoutEnumerator.getType());
 Assert.assertEquals("�", layoutEnumerator.getText());
 
```

**Parameters:**
| Parameter | Type | Description |
| --- | --- | --- |
| doc | [Document](../../com.aspose.words/document/) | The document to which this collector instance will be attached to. |

### clear() {#clear}
```
public void clear()
```


Clears all collected layout data. Call this method after document was manually updated, or layout was rebuilt.

 **Examples:** 

Shows how to see the the ranges of pages that a node spans.

```

 Document doc = new Document();
 LayoutCollector layoutCollector = new LayoutCollector(doc);

 // Call the "GetNumPagesSpanned" method to count how many pages the content of our document spans.
 // Since the document is empty, that number of pages is currently zero.
 Assert.assertEquals(doc, layoutCollector.getDocument());
 Assert.assertEquals(0, layoutCollector.getNumPagesSpanned(doc));

 // Populate the document with 5 pages of content.
 DocumentBuilder builder = new DocumentBuilder(doc);
 builder.write("Section 1");
 builder.insertBreak(BreakType.PAGE_BREAK);
 builder.insertBreak(BreakType.PAGE_BREAK);
 builder.insertBreak(BreakType.SECTION_BREAK_EVEN_PAGE);
 builder.write("Section 2");
 builder.insertBreak(BreakType.PAGE_BREAK);
 builder.insertBreak(BreakType.PAGE_BREAK);

 // Before the layout collector, we need to call the "UpdatePageLayout" method to give us
 // an accurate figure for any layout-related metric, such as the page count.
 Assert.assertEquals(0, layoutCollector.getNumPagesSpanned(doc));

 layoutCollector.clear();
 doc.updatePageLayout();

 Assert.assertEquals(5, layoutCollector.getNumPagesSpanned(doc));

 // We can see the numbers of the start and end pages of any node and their overall page spans.
 NodeCollection nodes = doc.getChildNodes(NodeType.ANY, true);
 for (Node node : (Iterable) nodes) {
     System.out.println(MessageFormat.format("->  NodeType.{0}: ", node.getNodeType()));
     System.out.println(MessageFormat.format("\tStarts on page {0}, ends on page {1},", layoutCollector.getStartPageIndex(node), layoutCollector.getEndPageIndex(node)) +
             MessageFormat.format(" spanning {0} pages.", layoutCollector.getNumPagesSpanned(node)));
 }

 // We can iterate over the layout entities using a LayoutEnumerator.
 LayoutEnumerator layoutEnumerator = new LayoutEnumerator(doc);

 Assert.assertEquals(LayoutEntityType.PAGE, layoutEnumerator.getType());

 // The LayoutEnumerator can traverse the collection of layout entities like a tree.
 // We can also apply it to any node's corresponding layout entity.
 layoutEnumerator.setCurrent(layoutCollector.getEntity(doc.getChild(NodeType.PARAGRAPH, 1, true)));

 Assert.assertEquals(LayoutEntityType.SPAN, layoutEnumerator.getType());
 Assert.assertEquals("�", layoutEnumerator.getText());
 
```

### getDocument() {#getDocument}
```
public Document getDocument()
```


Gets the document this collector instance is attached to.

 **Remarks:** 

If you need to access page indexes of the document nodes you need to set this property to point to a document instance, before page layout of the document is built. It is best to set this property to  null  afterwards, otherwise the collector continues to accumulate information from subsequent rebuilds of the document's page layout.

 **Examples:** 

Shows how to see the the ranges of pages that a node spans.

```

 Document doc = new Document();
 LayoutCollector layoutCollector = new LayoutCollector(doc);

 // Call the "GetNumPagesSpanned" method to count how many pages the content of our document spans.
 // Since the document is empty, that number of pages is currently zero.
 Assert.assertEquals(doc, layoutCollector.getDocument());
 Assert.assertEquals(0, layoutCollector.getNumPagesSpanned(doc));

 // Populate the document with 5 pages of content.
 DocumentBuilder builder = new DocumentBuilder(doc);
 builder.write("Section 1");
 builder.insertBreak(BreakType.PAGE_BREAK);
 builder.insertBreak(BreakType.PAGE_BREAK);
 builder.insertBreak(BreakType.SECTION_BREAK_EVEN_PAGE);
 builder.write("Section 2");
 builder.insertBreak(BreakType.PAGE_BREAK);
 builder.insertBreak(BreakType.PAGE_BREAK);

 // Before the layout collector, we need to call the "UpdatePageLayout" method to give us
 // an accurate figure for any layout-related metric, such as the page count.
 Assert.assertEquals(0, layoutCollector.getNumPagesSpanned(doc));

 layoutCollector.clear();
 doc.updatePageLayout();

 Assert.assertEquals(5, layoutCollector.getNumPagesSpanned(doc));

 // We can see the numbers of the start and end pages of any node and their overall page spans.
 NodeCollection nodes = doc.getChildNodes(NodeType.ANY, true);
 for (Node node : (Iterable) nodes) {
     System.out.println(MessageFormat.format("->  NodeType.{0}: ", node.getNodeType()));
     System.out.println(MessageFormat.format("\tStarts on page {0}, ends on page {1},", layoutCollector.getStartPageIndex(node), layoutCollector.getEndPageIndex(node)) +
             MessageFormat.format(" spanning {0} pages.", layoutCollector.getNumPagesSpanned(node)));
 }

 // We can iterate over the layout entities using a LayoutEnumerator.
 LayoutEnumerator layoutEnumerator = new LayoutEnumerator(doc);

 Assert.assertEquals(LayoutEntityType.PAGE, layoutEnumerator.getType());

 // The LayoutEnumerator can traverse the collection of layout entities like a tree.
 // We can also apply it to any node's corresponding layout entity.
 layoutEnumerator.setCurrent(layoutCollector.getEntity(doc.getChild(NodeType.PARAGRAPH, 1, true)));

 Assert.assertEquals(LayoutEntityType.SPAN, layoutEnumerator.getType());
 Assert.assertEquals("�", layoutEnumerator.getText());
 
```

**Returns:**
[Document](../../com.aspose.words/document/) - The document this collector instance is attached to.
### getEndPageIndex(Node node) {#getEndPageIndex-com.aspose.words.Node}
```
public int getEndPageIndex(Node node)
```


Gets 1-based index of the page where node ends. Returns 0 if node cannot be mapped to a page.

 **Examples:** 

Shows how to see the the ranges of pages that a node spans.

```

 Document doc = new Document();
 LayoutCollector layoutCollector = new LayoutCollector(doc);

 // Call the "GetNumPagesSpanned" method to count how many pages the content of our document spans.
 // Since the document is empty, that number of pages is currently zero.
 Assert.assertEquals(doc, layoutCollector.getDocument());
 Assert.assertEquals(0, layoutCollector.getNumPagesSpanned(doc));

 // Populate the document with 5 pages of content.
 DocumentBuilder builder = new DocumentBuilder(doc);
 builder.write("Section 1");
 builder.insertBreak(BreakType.PAGE_BREAK);
 builder.insertBreak(BreakType.PAGE_BREAK);
 builder.insertBreak(BreakType.SECTION_BREAK_EVEN_PAGE);
 builder.write("Section 2");
 builder.insertBreak(BreakType.PAGE_BREAK);
 builder.insertBreak(BreakType.PAGE_BREAK);

 // Before the layout collector, we need to call the "UpdatePageLayout" method to give us
 // an accurate figure for any layout-related metric, such as the page count.
 Assert.assertEquals(0, layoutCollector.getNumPagesSpanned(doc));

 layoutCollector.clear();
 doc.updatePageLayout();

 Assert.assertEquals(5, layoutCollector.getNumPagesSpanned(doc));

 // We can see the numbers of the start and end pages of any node and their overall page spans.
 NodeCollection nodes = doc.getChildNodes(NodeType.ANY, true);
 for (Node node : (Iterable) nodes) {
     System.out.println(MessageFormat.format("->  NodeType.{0}: ", node.getNodeType()));
     System.out.println(MessageFormat.format("\tStarts on page {0}, ends on page {1},", layoutCollector.getStartPageIndex(node), layoutCollector.getEndPageIndex(node)) +
             MessageFormat.format(" spanning {0} pages.", layoutCollector.getNumPagesSpanned(node)));
 }

 // We can iterate over the layout entities using a LayoutEnumerator.
 LayoutEnumerator layoutEnumerator = new LayoutEnumerator(doc);

 Assert.assertEquals(LayoutEntityType.PAGE, layoutEnumerator.getType());

 // The LayoutEnumerator can traverse the collection of layout entities like a tree.
 // We can also apply it to any node's corresponding layout entity.
 layoutEnumerator.setCurrent(layoutCollector.getEntity(doc.getChild(NodeType.PARAGRAPH, 1, true)));

 Assert.assertEquals(LayoutEntityType.SPAN, layoutEnumerator.getType());
 Assert.assertEquals("�", layoutEnumerator.getText());
 
```

**Parameters:**
| Parameter | Type | Description |
| --- | --- | --- |
| node | [Node](../../com.aspose.words/node/) |  |

**Returns:**
int
### getEntity(Node node) {#getEntity-com.aspose.words.Node}
```
public Object getEntity(Node node)
```


Returns an opaque position of the [LayoutEnumerator](../../com.aspose.words/layoutenumerator/) which corresponds to the specified node. You can use returned value as an argument to [LayoutEnumerator.getCurrent()](../../com.aspose.words/layoutenumerator/\#getCurrent) / [LayoutEnumerator.setCurrent(java.lang.Object)](../../com.aspose.words/layoutenumerator/\#setCurrent-java.lang.Object) given the document being enumerated and the document of the node are the same.

 **Remarks:** 

This method works for only [Paragraph](../../com.aspose.words/paragraph/) nodes, as well as indivisible inline nodes, e.g. [BookmarkStart](../../com.aspose.words/bookmarkstart/) or [Shape](../../com.aspose.words/shape/). It doesn't work for [Run](../../com.aspose.words/run/), [Cell](../../com.aspose.words/cell/) [Row](../../com.aspose.words/row/) or [Table](../../com.aspose.words/table/) nodes, and nodes within header/footer.

Note that the entity returned for a [Paragraph](../../com.aspose.words/paragraph/) node is a paragraph break span. Use the appropriate method to ascend to the parent line

If you need to navigate to a [Run](../../com.aspose.words/run/) of text then you can insert bookmark right before it and then navigate to the bookmark instead.

If you need to navigate to a [Cell](../../com.aspose.words/cell/) node then you can move to a [Paragraph](../../com.aspose.words/paragraph/) node in this cell and then ascend to a parent entity. The same approach can be used for [Row](../../com.aspose.words/row/) and [Table](../../com.aspose.words/table/) nodes.

 **Examples:** 

Shows how to see the the ranges of pages that a node spans.

```

 Document doc = new Document();
 LayoutCollector layoutCollector = new LayoutCollector(doc);

 // Call the "GetNumPagesSpanned" method to count how many pages the content of our document spans.
 // Since the document is empty, that number of pages is currently zero.
 Assert.assertEquals(doc, layoutCollector.getDocument());
 Assert.assertEquals(0, layoutCollector.getNumPagesSpanned(doc));

 // Populate the document with 5 pages of content.
 DocumentBuilder builder = new DocumentBuilder(doc);
 builder.write("Section 1");
 builder.insertBreak(BreakType.PAGE_BREAK);
 builder.insertBreak(BreakType.PAGE_BREAK);
 builder.insertBreak(BreakType.SECTION_BREAK_EVEN_PAGE);
 builder.write("Section 2");
 builder.insertBreak(BreakType.PAGE_BREAK);
 builder.insertBreak(BreakType.PAGE_BREAK);

 // Before the layout collector, we need to call the "UpdatePageLayout" method to give us
 // an accurate figure for any layout-related metric, such as the page count.
 Assert.assertEquals(0, layoutCollector.getNumPagesSpanned(doc));

 layoutCollector.clear();
 doc.updatePageLayout();

 Assert.assertEquals(5, layoutCollector.getNumPagesSpanned(doc));

 // We can see the numbers of the start and end pages of any node and their overall page spans.
 NodeCollection nodes = doc.getChildNodes(NodeType.ANY, true);
 for (Node node : (Iterable) nodes) {
     System.out.println(MessageFormat.format("->  NodeType.{0}: ", node.getNodeType()));
     System.out.println(MessageFormat.format("\tStarts on page {0}, ends on page {1},", layoutCollector.getStartPageIndex(node), layoutCollector.getEndPageIndex(node)) +
             MessageFormat.format(" spanning {0} pages.", layoutCollector.getNumPagesSpanned(node)));
 }

 // We can iterate over the layout entities using a LayoutEnumerator.
 LayoutEnumerator layoutEnumerator = new LayoutEnumerator(doc);

 Assert.assertEquals(LayoutEntityType.PAGE, layoutEnumerator.getType());

 // The LayoutEnumerator can traverse the collection of layout entities like a tree.
 // We can also apply it to any node's corresponding layout entity.
 layoutEnumerator.setCurrent(layoutCollector.getEntity(doc.getChild(NodeType.PARAGRAPH, 1, true)));

 Assert.assertEquals(LayoutEntityType.SPAN, layoutEnumerator.getType());
 Assert.assertEquals("�", layoutEnumerator.getText());
 
```

**Parameters:**
| Parameter | Type | Description |
| --- | --- | --- |
| node | [Node](../../com.aspose.words/node/) |  |

**Returns:**
java.lang.Object
### getNumPagesSpanned(Node node) {#getNumPagesSpanned-com.aspose.words.Node}
```
public int getNumPagesSpanned(Node node)
```


Gets number of pages the specified node spans. 0 if node is within a single page. This is the same as [getEndPageIndex(com.aspose.words.Node)](../../com.aspose.words/layoutcollector/\#getEndPageIndex-com.aspose.words.Node) - [getStartPageIndex(com.aspose.words.Node)](../../com.aspose.words/layoutcollector/\#getStartPageIndex-com.aspose.words.Node).

 **Examples:** 

Shows how to see the the ranges of pages that a node spans.

```

 Document doc = new Document();
 LayoutCollector layoutCollector = new LayoutCollector(doc);

 // Call the "GetNumPagesSpanned" method to count how many pages the content of our document spans.
 // Since the document is empty, that number of pages is currently zero.
 Assert.assertEquals(doc, layoutCollector.getDocument());
 Assert.assertEquals(0, layoutCollector.getNumPagesSpanned(doc));

 // Populate the document with 5 pages of content.
 DocumentBuilder builder = new DocumentBuilder(doc);
 builder.write("Section 1");
 builder.insertBreak(BreakType.PAGE_BREAK);
 builder.insertBreak(BreakType.PAGE_BREAK);
 builder.insertBreak(BreakType.SECTION_BREAK_EVEN_PAGE);
 builder.write("Section 2");
 builder.insertBreak(BreakType.PAGE_BREAK);
 builder.insertBreak(BreakType.PAGE_BREAK);

 // Before the layout collector, we need to call the "UpdatePageLayout" method to give us
 // an accurate figure for any layout-related metric, such as the page count.
 Assert.assertEquals(0, layoutCollector.getNumPagesSpanned(doc));

 layoutCollector.clear();
 doc.updatePageLayout();

 Assert.assertEquals(5, layoutCollector.getNumPagesSpanned(doc));

 // We can see the numbers of the start and end pages of any node and their overall page spans.
 NodeCollection nodes = doc.getChildNodes(NodeType.ANY, true);
 for (Node node : (Iterable) nodes) {
     System.out.println(MessageFormat.format("->  NodeType.{0}: ", node.getNodeType()));
     System.out.println(MessageFormat.format("\tStarts on page {0}, ends on page {1},", layoutCollector.getStartPageIndex(node), layoutCollector.getEndPageIndex(node)) +
             MessageFormat.format(" spanning {0} pages.", layoutCollector.getNumPagesSpanned(node)));
 }

 // We can iterate over the layout entities using a LayoutEnumerator.
 LayoutEnumerator layoutEnumerator = new LayoutEnumerator(doc);

 Assert.assertEquals(LayoutEntityType.PAGE, layoutEnumerator.getType());

 // The LayoutEnumerator can traverse the collection of layout entities like a tree.
 // We can also apply it to any node's corresponding layout entity.
 layoutEnumerator.setCurrent(layoutCollector.getEntity(doc.getChild(NodeType.PARAGRAPH, 1, true)));

 Assert.assertEquals(LayoutEntityType.SPAN, layoutEnumerator.getType());
 Assert.assertEquals("�", layoutEnumerator.getText());
 
```

**Parameters:**
| Parameter | Type | Description |
| --- | --- | --- |
| node | [Node](../../com.aspose.words/node/) |  |

**Returns:**
int
### getStartPageIndex(Node node) {#getStartPageIndex-com.aspose.words.Node}
```
public int getStartPageIndex(Node node)
```


Gets 1-based index of the page where node begins. Returns 0 if node cannot be mapped to a page.

 **Examples:** 

Shows how to see the the ranges of pages that a node spans.

```

 Document doc = new Document();
 LayoutCollector layoutCollector = new LayoutCollector(doc);

 // Call the "GetNumPagesSpanned" method to count how many pages the content of our document spans.
 // Since the document is empty, that number of pages is currently zero.
 Assert.assertEquals(doc, layoutCollector.getDocument());
 Assert.assertEquals(0, layoutCollector.getNumPagesSpanned(doc));

 // Populate the document with 5 pages of content.
 DocumentBuilder builder = new DocumentBuilder(doc);
 builder.write("Section 1");
 builder.insertBreak(BreakType.PAGE_BREAK);
 builder.insertBreak(BreakType.PAGE_BREAK);
 builder.insertBreak(BreakType.SECTION_BREAK_EVEN_PAGE);
 builder.write("Section 2");
 builder.insertBreak(BreakType.PAGE_BREAK);
 builder.insertBreak(BreakType.PAGE_BREAK);

 // Before the layout collector, we need to call the "UpdatePageLayout" method to give us
 // an accurate figure for any layout-related metric, such as the page count.
 Assert.assertEquals(0, layoutCollector.getNumPagesSpanned(doc));

 layoutCollector.clear();
 doc.updatePageLayout();

 Assert.assertEquals(5, layoutCollector.getNumPagesSpanned(doc));

 // We can see the numbers of the start and end pages of any node and their overall page spans.
 NodeCollection nodes = doc.getChildNodes(NodeType.ANY, true);
 for (Node node : (Iterable) nodes) {
     System.out.println(MessageFormat.format("->  NodeType.{0}: ", node.getNodeType()));
     System.out.println(MessageFormat.format("\tStarts on page {0}, ends on page {1},", layoutCollector.getStartPageIndex(node), layoutCollector.getEndPageIndex(node)) +
             MessageFormat.format(" spanning {0} pages.", layoutCollector.getNumPagesSpanned(node)));
 }

 // We can iterate over the layout entities using a LayoutEnumerator.
 LayoutEnumerator layoutEnumerator = new LayoutEnumerator(doc);

 Assert.assertEquals(LayoutEntityType.PAGE, layoutEnumerator.getType());

 // The LayoutEnumerator can traverse the collection of layout entities like a tree.
 // We can also apply it to any node's corresponding layout entity.
 layoutEnumerator.setCurrent(layoutCollector.getEntity(doc.getChild(NodeType.PARAGRAPH, 1, true)));

 Assert.assertEquals(LayoutEntityType.SPAN, layoutEnumerator.getType());
 Assert.assertEquals("�", layoutEnumerator.getText());
 
```

**Parameters:**
| Parameter | Type | Description |
| --- | --- | --- |
| node | [Node](../../com.aspose.words/node/) |  |

**Returns:**
int
### setDocument(Document value) {#setDocument-com.aspose.words.Document}
```
public void setDocument(Document value)
```


Sets the document this collector instance is attached to.

 **Remarks:** 

If you need to access page indexes of the document nodes you need to set this property to point to a document instance, before page layout of the document is built. It is best to set this property to  null  afterwards, otherwise the collector continues to accumulate information from subsequent rebuilds of the document's page layout.

 **Examples:** 

Shows how to see the the ranges of pages that a node spans.

```

 Document doc = new Document();
 LayoutCollector layoutCollector = new LayoutCollector(doc);

 // Call the "GetNumPagesSpanned" method to count how many pages the content of our document spans.
 // Since the document is empty, that number of pages is currently zero.
 Assert.assertEquals(doc, layoutCollector.getDocument());
 Assert.assertEquals(0, layoutCollector.getNumPagesSpanned(doc));

 // Populate the document with 5 pages of content.
 DocumentBuilder builder = new DocumentBuilder(doc);
 builder.write("Section 1");
 builder.insertBreak(BreakType.PAGE_BREAK);
 builder.insertBreak(BreakType.PAGE_BREAK);
 builder.insertBreak(BreakType.SECTION_BREAK_EVEN_PAGE);
 builder.write("Section 2");
 builder.insertBreak(BreakType.PAGE_BREAK);
 builder.insertBreak(BreakType.PAGE_BREAK);

 // Before the layout collector, we need to call the "UpdatePageLayout" method to give us
 // an accurate figure for any layout-related metric, such as the page count.
 Assert.assertEquals(0, layoutCollector.getNumPagesSpanned(doc));

 layoutCollector.clear();
 doc.updatePageLayout();

 Assert.assertEquals(5, layoutCollector.getNumPagesSpanned(doc));

 // We can see the numbers of the start and end pages of any node and their overall page spans.
 NodeCollection nodes = doc.getChildNodes(NodeType.ANY, true);
 for (Node node : (Iterable) nodes) {
     System.out.println(MessageFormat.format("->  NodeType.{0}: ", node.getNodeType()));
     System.out.println(MessageFormat.format("\tStarts on page {0}, ends on page {1},", layoutCollector.getStartPageIndex(node), layoutCollector.getEndPageIndex(node)) +
             MessageFormat.format(" spanning {0} pages.", layoutCollector.getNumPagesSpanned(node)));
 }

 // We can iterate over the layout entities using a LayoutEnumerator.
 LayoutEnumerator layoutEnumerator = new LayoutEnumerator(doc);

 Assert.assertEquals(LayoutEntityType.PAGE, layoutEnumerator.getType());

 // The LayoutEnumerator can traverse the collection of layout entities like a tree.
 // We can also apply it to any node's corresponding layout entity.
 layoutEnumerator.setCurrent(layoutCollector.getEntity(doc.getChild(NodeType.PARAGRAPH, 1, true)));

 Assert.assertEquals(LayoutEntityType.SPAN, layoutEnumerator.getType());
 Assert.assertEquals("�", layoutEnumerator.getText());
 
```

**Parameters:**
| Parameter | Type | Description |
| --- | --- | --- |
| value | [Document](../../com.aspose.words/document/) | The document this collector instance is attached to. |

