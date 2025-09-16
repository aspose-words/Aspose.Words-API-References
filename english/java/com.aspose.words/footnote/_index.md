---
title: Footnote
linktitle: Footnote
second_title: Aspose.Words for Java
description: Represents a container for text of a footnote or endnote in Java.
type: docs
weight: 338
url: /java/com.aspose.words/footnote/
---

**Inheritance:**
java.lang.Object, [com.aspose.words.Node](../../com.aspose.words/node/), [com.aspose.words.CompositeNode](../../com.aspose.words/compositenode/), [com.aspose.words.InlineStory](../../com.aspose.words/inlinestory/)
```
public class Footnote extends InlineStory
```

Represents a container for text of a footnote or endnote.

To learn more, visit the [ Working with Footnote and Endnote ][Working with Footnote and Endnote] documentation article.

 **Remarks:** 

The [Footnote](../../com.aspose.words/footnote/) class is used to represent both footnotes and endnotes in a Word document.

[Footnote](../../com.aspose.words/footnote/) is an inline-level node and can only be a child of [Paragraph](../../com.aspose.words/paragraph/).

[Footnote](../../com.aspose.words/footnote/) can contain [Paragraph](../../com.aspose.words/paragraph/) and [Table](../../com.aspose.words/table/) child nodes.

 **Examples:** 

Shows how to insert and customize footnotes.

```

 Document doc = new Document();
 DocumentBuilder builder = new DocumentBuilder(doc);

 // Add text, and reference it with a footnote. This footnote will place a small superscript reference
 // mark after the text that it references and create an entry below the main body text at the bottom of the page.
 // This entry will contain the footnote's reference mark and the reference text,
 // which we will pass to the document builder's "InsertFootnote" method.
 builder.write("Main body text.");
 Footnote footnote = builder.insertFootnote(FootnoteType.FOOTNOTE, "Footnote text.");

 // If this property is set to "true", then our footnote's reference mark
 // will be its index among all the section's footnotes.
 // This is the first footnote, so the reference mark will be "1".
 Assert.assertTrue(footnote.isAuto());

 // We can move the document builder inside the footnote to edit its reference text.
 builder.moveTo(footnote.getFirstParagraph());
 builder.write(" More text added by a DocumentBuilder.");
 builder.moveToDocumentEnd();

 Assert.assertEquals(footnote.getParagraphs().get(0).toString(SaveFormat.TEXT).trim(), "Footnote text. More text added by a DocumentBuilder.");

 builder.write(" More main body text.");
 footnote = builder.insertFootnote(FootnoteType.FOOTNOTE, "Footnote text.");

 // We can set a custom reference mark which the footnote will use instead of its index number.
 footnote.setReferenceMark("RefMark");

 Assert.assertFalse(footnote.isAuto());

 // A bookmark with the "IsAuto" flag set to true will still show its real index
 // even if previous bookmarks display custom reference marks, so this bookmark's reference mark will be a "3".
 builder.write(" More main body text.");
 footnote = builder.insertFootnote(FootnoteType.FOOTNOTE, "Footnote text.");

 Assert.assertTrue(footnote.isAuto());

 doc.save(getArtifactsDir() + "InlineStory.AddFootnote.docx");
 
```


[Working with Footnote and Endnote]: https://docs.aspose.com/words/java/working-with-footnote-and-endnote/
## Constructors

| Constructor | Description |
| --- | --- |
| [Footnote(DocumentBase doc, int footnoteType)](#Footnote-com.aspose.words.DocumentBase-int) | Initializes a new instance of this class. |
## Methods

| Method | Description |
| --- | --- |
| [accept(DocumentVisitor visitor)](#accept-com.aspose.words.DocumentVisitor) | Accepts a visitor. |
| [acceptEnd(DocumentVisitor visitor)](#acceptEnd-com.aspose.words.DocumentVisitor) | Accepts a visitor for visiting the end of the footnote. |
| [acceptStart(DocumentVisitor visitor)](#acceptStart-com.aspose.words.DocumentVisitor) | Accepts a visitor for visiting the start of the footnote. |
| [appendChild(Node newChild)](#appendChild-com.aspose.words.Node) | Adds the specified node to the end of the list of child nodes for this node. |
| [clearRunAttrs()](#clearRunAttrs) |  |
| [deepClone(boolean isCloneChildren)](#deepClone-boolean) | Creates a duplicate of the node. |
| [ensureMinimum()](#ensureMinimum) | If the last child is not a paragraph, creates and appends one empty paragraph. |
| [fetchInheritedRunAttr(int fontAttr)](#fetchInheritedRunAttr-int) |  |
| [getActualReferenceMark()](#getActualReferenceMark) | Gets the actual text of the reference mark displayed in the document for this footnote. |
| [getAncestor(int ancestorType)](#getAncestor-int) |  |
| [getAncestor(Class ancestorType)](#getAncestor-java.lang.Class) | Gets the first ancestor of the specified object type. |
| [getChild(int nodeType, int index, boolean isDeep)](#getChild-int-int-boolean) |  |
| [getChildNodes(int nodeType, boolean isDeep)](#getChildNodes-int-boolean) |  |
| [getContainer()](#getContainer) |  |
| [getCount()](#getCount) | Gets the number of immediate children of this node. |
| [getCurrentNode()](#getCurrentNode) |  |
| [getCustomNodeId()](#getCustomNodeId) | Specifies custom node identifier. |
| [getDirectRunAttr(int key)](#getDirectRunAttr-int) |  |
| [getDirectRunAttr(int key, int revisionsView)](#getDirectRunAttr-int-int) |  |
| [getDocument()](#getDocument) | Gets the document to which this node belongs. |
| [getDocument_IInline()](#getDocument-IInline) |  |
| [getFirstChild()](#getFirstChild) | Gets the first child of the node. |
| [getFirstParagraph()](#getFirstParagraph) | Gets the first paragraph in the story. |
| [getFont()](#getFont) | Provides access to the font formatting of the anchor character of this object. |
| [getFootnoteType()](#getFootnoteType) | Returns a value that specifies whether this is a footnote or endnote. |
| [getLastChild()](#getLastChild) | Gets the last child of the node. |
| [getLastParagraph()](#getLastParagraph) | Gets the last paragraph in the story. |
| [getNextMatchingNode(Node curNode)](#getNextMatchingNode-com.aspose.words.Node) |  |
| [getNextSibling()](#getNextSibling) | Gets the node immediately following this node. |
| [getNodeType()](#getNodeType) | Returns [NodeType.FOOTNOTE](../../com.aspose.words/nodetype/\#FOOTNOTE). |
| [getParagraphs()](#getParagraphs) | Gets a collection of paragraphs that are immediate children of the story. |
| [getParentNode()](#getParentNode) | Gets the immediate parent of this node. |
| [getParentParagraph()](#getParentParagraph) | Retrieves the parent [Paragraph](../../com.aspose.words/paragraph/) of this node. |
| [getParentParagraph_IInline()](#getParentParagraph-IInline) |  |
| [getPreviousSibling()](#getPreviousSibling) | Gets the node immediately preceding this node. |
| [getRange()](#getRange) | Returns a [Range](../../com.aspose.words/range/) object that represents the portion of a document that is contained in this node. |
| [getReferenceMark()](#getReferenceMark) | Gets/sets custom reference mark to be used for this footnote. |
| [getStoryType()](#getStoryType) | Returns [StoryType.FOOTNOTES](../../com.aspose.words/storytype/\#FOOTNOTES) or [StoryType.ENDNOTES](../../com.aspose.words/storytype/\#ENDNOTES). |
| [getTables()](#getTables) | Gets a collection of tables that are immediate children of the story. |
| [getText()](#getText) | Gets the text of this node and of all its children. |
| [hasChildNodes()](#hasChildNodes) | Returns  true  if this node has any child nodes. |
| [indexOf(Node child)](#indexOf-com.aspose.words.Node) | Returns the index of the specified child node in the child node array. |
| [insertAfter(Node newChild, Node refChild)](#insertAfter-com.aspose.words.Node-com.aspose.words.Node) | Inserts the specified node immediately after the specified reference node. |
| [insertBefore(Node newChild, Node refChild)](#insertBefore-com.aspose.words.Node-com.aspose.words.Node) | Inserts the specified node immediately before the specified reference node. |
| [isAuto()](#isAuto) | Holds a value that specifies whether this is a auto-numbered footnote or footnote with user defined custom reference mark. |
| [isAuto(boolean value)](#isAuto-boolean) | Holds a value that specifies whether this is a auto-numbered footnote or footnote with user defined custom reference mark. |
| [isComposite()](#isComposite) | Returns  true  as this node can have child nodes. |
| [isDeleteRevision()](#isDeleteRevision) | Returns true if this object was deleted in Microsoft Word while change tracking was enabled. |
| [isInsertRevision()](#isInsertRevision) | Returns true if this object was inserted in Microsoft Word while change tracking was enabled. |
| [isMoveFromRevision()](#isMoveFromRevision) | Returns  true  if this object was moved (deleted) in Microsoft Word while change tracking was enabled. |
| [isMoveToRevision()](#isMoveToRevision) | Returns  true  if this object was moved (inserted) in Microsoft Word while change tracking was enabled. |
| [iterator()](#iterator) | Provides support for the for each style iteration over the child nodes of this node. |
| [nextPreOrder(Node rootNode)](#nextPreOrder-com.aspose.words.Node) | Gets next node according to the pre-order tree traversal algorithm. |
| [nodeTypeToString(int nodeType)](#nodeTypeToString-int) |  |
| [prependChild(Node newChild)](#prependChild-com.aspose.words.Node) | Adds the specified node to the beginning of the list of child nodes for this node. |
| [previousPreOrder(Node rootNode)](#previousPreOrder-com.aspose.words.Node) | Gets the previous node according to the pre-order tree traversal algorithm. |
| [remove()](#remove) | Removes itself from the parent. |
| [removeAllChildren()](#removeAllChildren) | Removes all the child nodes of the current node. |
| [removeChild(Node oldChild)](#removeChild-com.aspose.words.Node) | Removes the specified child node. |
| [removeMoveRevisions()](#removeMoveRevisions) |  |
| [removeRunAttr(int key)](#removeRunAttr-int) |  |
| [removeSmartTags()](#removeSmartTags) | Removes all [SmartTag](../../com.aspose.words/smarttag/) descendant nodes of the current node. |
| [selectNodes(String xpath)](#selectNodes-java.lang.String) | Selects a list of nodes matching the XPath expression. |
| [selectSingleNode(String xpath)](#selectSingleNode-java.lang.String) | Selects the first [Node](../../com.aspose.words/node/) that matches the XPath expression. |
| [setCustomNodeId(int value)](#setCustomNodeId-int) | Specifies custom node identifier. |
| [setReferenceMark(String value)](#setReferenceMark-java.lang.String) | Gets/sets custom reference mark to be used for this footnote. |
| [setRunAttr(int fontAttr, Object value)](#setRunAttr-int-java.lang.Object) |  |
| [toString()](#toString) |  |
| [toString(SaveOptions saveOptions)](#toString-com.aspose.words.SaveOptions) | Exports the content of the node into a string using the specified save options. |
| [toString(int saveFormat)](#toString-int) |  |
### Footnote(DocumentBase doc, int footnoteType) {#Footnote-com.aspose.words.DocumentBase-int}
```
public Footnote(DocumentBase doc, int footnoteType)
```


Initializes a new instance of this class.

**Parameters:**
| Parameter | Type | Description |
| --- | --- | --- |
| doc | [DocumentBase](../../com.aspose.words/documentbase/) |  |
| footnoteType | int |  |

### accept(DocumentVisitor visitor) {#accept-com.aspose.words.DocumentVisitor}
```
public boolean accept(DocumentVisitor visitor)
```


Accepts a visitor.

 **Remarks:** 

Enumerates over this node and all of its children. Each node calls a corresponding method on [DocumentVisitor](../../com.aspose.words/documentvisitor/).

For more info see the Visitor design pattern.

Calls DocumentVisitor.VisitFootnoteStart, then calls Accept for all child nodes of the footnote and calls DocumentVisitor.VisitFootnoteEnd at the end.

 **Examples:** 

Shows how to print the node structure of every footnote in a document.

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
| Parameter | Type | Description |
| --- | --- | --- |
| visitor | [DocumentVisitor](../../com.aspose.words/documentvisitor/) | The visitor that will visit the nodes. |

**Returns:**
boolean - True if all nodes were visited; false if [DocumentVisitor](../../com.aspose.words/documentvisitor/) stopped the operation before visiting all nodes.
### acceptEnd(DocumentVisitor visitor) {#acceptEnd-com.aspose.words.DocumentVisitor}
```
public int acceptEnd(DocumentVisitor visitor)
```


Accepts a visitor for visiting the end of the footnote.

 **Examples:** 

Shows how to print the node structure of every footnote in a document.

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
| Parameter | Type | Description |
| --- | --- | --- |
| visitor | [DocumentVisitor](../../com.aspose.words/documentvisitor/) | The document visitor. |

**Returns:**
int - The action to be taken by the visitor. The returned value is one of [VisitorAction](../../com.aspose.words/visitoraction/) constants.
### acceptStart(DocumentVisitor visitor) {#acceptStart-com.aspose.words.DocumentVisitor}
```
public int acceptStart(DocumentVisitor visitor)
```


Accepts a visitor for visiting the start of the footnote.

 **Examples:** 

Shows how to print the node structure of every footnote in a document.

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
| Parameter | Type | Description |
| --- | --- | --- |
| visitor | [DocumentVisitor](../../com.aspose.words/documentvisitor/) | The document visitor. |

**Returns:**
int - The action to be taken by the visitor. The returned value is one of [VisitorAction](../../com.aspose.words/visitoraction/) constants.
### appendChild(Node newChild) {#appendChild-com.aspose.words.Node}
```
public Node appendChild(Node newChild)
```


Adds the specified node to the end of the list of child nodes for this node.

 **Remarks:** 

If the  newChild  is already in the tree, it is first removed.

If the node being inserted was created from another document, you should use **M:Aspose.Words.DocumentBase.ImportNode(Aspose.Words.Node,System.Boolean,Aspose.Words.ImportFormatMode)** to import the node to the current document. The imported node can then be inserted into the current document.

 **Examples:** 

Shows how to construct an Aspose.Words document by hand.

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
| Parameter | Type | Description |
| --- | --- | --- |
| newChild | [Node](../../com.aspose.words/node/) | The node to add. |

**Returns:**
[Node](../../com.aspose.words/node/) - The node added.
### clearRunAttrs() {#clearRunAttrs}
```
public void clearRunAttrs()
```




### deepClone(boolean isCloneChildren) {#deepClone-boolean}
```
public Node deepClone(boolean isCloneChildren)
```


Creates a duplicate of the node.

 **Remarks:** 

This method serves as a copy constructor for nodes. The cloned node has no parent, but belongs to the same document as the original node.

This method always performs a deep copy of the node. The  isCloneChildren  parameter specifies whether to perform copy all child nodes as well.

 **Examples:** 

Shows how to clone a composite node.

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
| Parameter | Type | Description |
| --- | --- | --- |
| isCloneChildren | boolean | True to recursively clone the subtree under the specified node; false to clone only the node itself. |

**Returns:**
[Node](../../com.aspose.words/node/) - The cloned node.
### ensureMinimum() {#ensureMinimum}
```
public void ensureMinimum()
```


If the last child is not a paragraph, creates and appends one empty paragraph.

 **Examples:** 

Shows how to insert InlineStory nodes.

```

 Document doc = new Document();
 DocumentBuilder builder = new DocumentBuilder(doc);
 Footnote footnote = builder.insertFootnote(FootnoteType.FOOTNOTE, null);

 // Table nodes have an "EnsureMinimum()" method that makes sure the table has at least one cell.
 Table table = new Table(doc);
 table.ensureMinimum();

 // We can place a table inside a footnote, which will make it appear at the referencing page's footer.
 Assert.assertEquals(footnote.getTables().getCount(), 0);
 footnote.appendChild(table);
 Assert.assertEquals(footnote.getTables().getCount(), 1);
 Assert.assertEquals(footnote.getLastChild().getNodeType(), NodeType.TABLE);

 // An InlineStory has an "EnsureMinimum()" method as well, but in this case,
 // it makes sure the last child of the node is a paragraph,
 // for us to be able to click and write text easily in Microsoft Word.
 footnote.ensureMinimum();
 Assert.assertEquals(footnote.getLastChild().getNodeType(), NodeType.PARAGRAPH);

 // Edit the appearance of the anchor, which is the small superscript number
 // in the main text that points to the footnote.
 footnote.getFont().setName("Arial");
 footnote.getFont().setColor(Color.GREEN);

 // All inline story nodes have their respective story types.
 Assert.assertEquals(footnote.getStoryType(), StoryType.FOOTNOTES);

 // A comment is another type of inline story.
 Comment comment = (Comment) builder.getCurrentParagraph().appendChild(new Comment(doc, "John Doe", "J. D.", new Date()));

 // The parent paragraph of an inline story node will be the one from the main document body.
 Assert.assertEquals(doc.getFirstSection().getBody().getFirstParagraph(), comment.getParentParagraph());

 // However, the last paragraph is the one from the comment text contents,
 // which will be outside the main document body in a speech bubble.
 // A comment will not have any child nodes by default,
 // so we can apply the EnsureMinimum() method to place a paragraph here as well.
 Assert.assertNull(comment.getLastParagraph());
 comment.ensureMinimum();
 Assert.assertEquals(comment.getLastChild().getNodeType(), NodeType.PARAGRAPH);

 // Once we have a paragraph, we can move the builder to do it and write our comment.
 builder.moveTo(comment.getLastParagraph());
 builder.write("My comment.");

 Assert.assertEquals(comment.getStoryType(), StoryType.COMMENTS);

 doc.save(getArtifactsDir() + "InlineStory.InsertInlineStoryNodes.docx");
 
```

### fetchInheritedRunAttr(int fontAttr) {#fetchInheritedRunAttr-int}
```
public Object fetchInheritedRunAttr(int fontAttr)
```




**Parameters:**
| Parameter | Type | Description |
| --- | --- | --- |
| fontAttr | int |  |

**Returns:**
java.lang.Object
### getActualReferenceMark() {#getActualReferenceMark}
```
public String getActualReferenceMark()
```


Gets the actual text of the reference mark displayed in the document for this footnote.

 **Remarks:** 

To initially populate values of this property for all reference marks of the document, or to update the values after changes in the document that might affect the reference marks, you must execute the [Document.updateActualReferenceMarks()](../../com.aspose.words/document/\#updateActualReferenceMarks) method. Updating fields ( [Document.updateFields()](../../com.aspose.words/document/\#updateFields)) may also be necessary to get the correct result.

 **Examples:** 

Shows how to get actual footnote reference mark.

```

 Document doc = new Document(getMyDir() + "Footnotes and endnotes.docx");

 Footnote footnote = (Footnote)doc.getChild(NodeType.FOOTNOTE, 1, true);
 doc.updateFields();
 doc.updateActualReferenceMarks();

 Assert.assertEquals("1", footnote.getActualReferenceMark());
 
```

**Returns:**
java.lang.String - The actual text of the reference mark displayed in the document for this footnote.
### getAncestor(int ancestorType) {#getAncestor-int}
```
public CompositeNode getAncestor(int ancestorType)
```




**Parameters:**
| Parameter | Type | Description |
| --- | --- | --- |
| ancestorType | int |  |

**Returns:**
[CompositeNode](../../com.aspose.words/compositenode/)
### getAncestor(Class ancestorType) {#getAncestor-java.lang.Class}
```
public CompositeNode getAncestor(Class ancestorType)
```


Gets the first ancestor of the specified object type.

 **Remarks:** 

The ancestor type matches if it is equal to  ancestorType  or derived from  ancestorType .

 **Examples:** 

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

**Parameters:**
| Parameter | Type | Description |
| --- | --- | --- |
| ancestorType | java.lang.Class | The object type of the ancestor to retrieve. |

**Returns:**
[CompositeNode](../../com.aspose.words/compositenode/) - The ancestor of the specified type or  null  if no ancestor of this type was found.
### getChild(int nodeType, int index, boolean isDeep) {#getChild-int-int-boolean}
```
public Node getChild(int nodeType, int index, boolean isDeep)
```




**Parameters:**
| Parameter | Type | Description |
| --- | --- | --- |
| nodeType | int |  |
| index | int |  |
| isDeep | boolean |  |

**Returns:**
[Node](../../com.aspose.words/node/)
### getChildNodes(int nodeType, boolean isDeep) {#getChildNodes-int-boolean}
```
public NodeCollection getChildNodes(int nodeType, boolean isDeep)
```




**Parameters:**
| Parameter | Type | Description |
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


Gets the number of immediate children of this node.

 **Examples:** 

Shows how to add, update and delete child nodes in a CompositeNode's collection of children.

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
int - The number of immediate children of this node.
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


Specifies custom node identifier.

 **Remarks:** 

Default is zero.

This identifier can be set and used arbitrarily. For example, as a key to get external data.

Important note, specified value is not saved to an output file and exists only during the node lifetime.

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

**Returns:**
int - The corresponding  int  value.
### getDirectRunAttr(int key) {#getDirectRunAttr-int}
```
public Object getDirectRunAttr(int key)
```




**Parameters:**
| Parameter | Type | Description |
| --- | --- | --- |
| key | int |  |

**Returns:**
java.lang.Object
### getDirectRunAttr(int key, int revisionsView) {#getDirectRunAttr-int-int}
```
public Object getDirectRunAttr(int key, int revisionsView)
```




**Parameters:**
| Parameter | Type | Description |
| --- | --- | --- |
| key | int |  |
| revisionsView | int |  |

**Returns:**
java.lang.Object
### getDocument() {#getDocument}
```
public DocumentBase getDocument()
```


Gets the document to which this node belongs.

 **Remarks:** 

The node always belongs to a document even if it has just been created and not yet added to the tree, or if it has been removed from the tree.

 **Examples:** 

Shows how to create a node and set its owning document.

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
### getDocument_IInline() {#getDocument-IInline}
```
public DocumentBase getDocument_IInline()
```




**Returns:**
[DocumentBase](../../com.aspose.words/documentbase/)
### getFirstChild() {#getFirstChild}
```
public Node getFirstChild()
```


Gets the first child of the node.

 **Remarks:** 

If there is no first child node, a  null  is returned.

 **Examples:** 

Shows how to use a node's NextSibling property to enumerate through its immediate children.

```

 Document doc = new Document(getMyDir() + "Paragraphs.docx");

 for (Node node = doc.getFirstSection().getBody().getFirstChild(); node != null; node = node.getNextSibling()) {
     System.out.println(Node.nodeTypeToString(node.getNodeType()));
 }
 
```

Shows how to traverse a composite node's tree of child nodes.

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
[Node](../../com.aspose.words/node/) - The first child of the node.
### getFirstParagraph() {#getFirstParagraph}
```
public Paragraph getFirstParagraph()
```


Gets the first paragraph in the story.

 **Examples:** 

Shows how to add a comment to a paragraph.

```

 Document doc = new Document();
 DocumentBuilder builder = new DocumentBuilder(doc);
 builder.write("Hello world!");

 Comment comment = new Comment(doc, "John Doe", "JD", new Date());
 builder.getCurrentParagraph().appendChild(comment);
 builder.moveTo(comment.appendChild(new Paragraph(doc)));
 builder.write("Comment text.");

 Assert.assertEquals(new Date(), comment.getDateTime());

 // In Microsoft Word, we can right-click this comment in the document body to edit it, or reply to it.
 doc.save(getArtifactsDir() + "InlineStory.AddComment.docx");
 
```

Shows how to insert and customize footnotes.

```

 Document doc = new Document();
 DocumentBuilder builder = new DocumentBuilder(doc);

 // Add text, and reference it with a footnote. This footnote will place a small superscript reference
 // mark after the text that it references and create an entry below the main body text at the bottom of the page.
 // This entry will contain the footnote's reference mark and the reference text,
 // which we will pass to the document builder's "InsertFootnote" method.
 builder.write("Main body text.");
 Footnote footnote = builder.insertFootnote(FootnoteType.FOOTNOTE, "Footnote text.");

 // If this property is set to "true", then our footnote's reference mark
 // will be its index among all the section's footnotes.
 // This is the first footnote, so the reference mark will be "1".
 Assert.assertTrue(footnote.isAuto());

 // We can move the document builder inside the footnote to edit its reference text.
 builder.moveTo(footnote.getFirstParagraph());
 builder.write(" More text added by a DocumentBuilder.");
 builder.moveToDocumentEnd();

 Assert.assertEquals(footnote.getParagraphs().get(0).toString(SaveFormat.TEXT).trim(), "Footnote text. More text added by a DocumentBuilder.");

 builder.write(" More main body text.");
 footnote = builder.insertFootnote(FootnoteType.FOOTNOTE, "Footnote text.");

 // We can set a custom reference mark which the footnote will use instead of its index number.
 footnote.setReferenceMark("RefMark");

 Assert.assertFalse(footnote.isAuto());

 // A bookmark with the "IsAuto" flag set to true will still show its real index
 // even if previous bookmarks display custom reference marks, so this bookmark's reference mark will be a "3".
 builder.write(" More main body text.");
 footnote = builder.insertFootnote(FootnoteType.FOOTNOTE, "Footnote text.");

 Assert.assertTrue(footnote.isAuto());

 doc.save(getArtifactsDir() + "InlineStory.AddFootnote.docx");
 
```

**Returns:**
[Paragraph](../../com.aspose.words/paragraph/) - The first paragraph in the story.
### getFont() {#getFont}
```
public Font getFont()
```


Provides access to the font formatting of the anchor character of this object.

 **Examples:** 

Shows how to insert InlineStory nodes.

```

 Document doc = new Document();
 DocumentBuilder builder = new DocumentBuilder(doc);
 Footnote footnote = builder.insertFootnote(FootnoteType.FOOTNOTE, null);

 // Table nodes have an "EnsureMinimum()" method that makes sure the table has at least one cell.
 Table table = new Table(doc);
 table.ensureMinimum();

 // We can place a table inside a footnote, which will make it appear at the referencing page's footer.
 Assert.assertEquals(footnote.getTables().getCount(), 0);
 footnote.appendChild(table);
 Assert.assertEquals(footnote.getTables().getCount(), 1);
 Assert.assertEquals(footnote.getLastChild().getNodeType(), NodeType.TABLE);

 // An InlineStory has an "EnsureMinimum()" method as well, but in this case,
 // it makes sure the last child of the node is a paragraph,
 // for us to be able to click and write text easily in Microsoft Word.
 footnote.ensureMinimum();
 Assert.assertEquals(footnote.getLastChild().getNodeType(), NodeType.PARAGRAPH);

 // Edit the appearance of the anchor, which is the small superscript number
 // in the main text that points to the footnote.
 footnote.getFont().setName("Arial");
 footnote.getFont().setColor(Color.GREEN);

 // All inline story nodes have their respective story types.
 Assert.assertEquals(footnote.getStoryType(), StoryType.FOOTNOTES);

 // A comment is another type of inline story.
 Comment comment = (Comment) builder.getCurrentParagraph().appendChild(new Comment(doc, "John Doe", "J. D.", new Date()));

 // The parent paragraph of an inline story node will be the one from the main document body.
 Assert.assertEquals(doc.getFirstSection().getBody().getFirstParagraph(), comment.getParentParagraph());

 // However, the last paragraph is the one from the comment text contents,
 // which will be outside the main document body in a speech bubble.
 // A comment will not have any child nodes by default,
 // so we can apply the EnsureMinimum() method to place a paragraph here as well.
 Assert.assertNull(comment.getLastParagraph());
 comment.ensureMinimum();
 Assert.assertEquals(comment.getLastChild().getNodeType(), NodeType.PARAGRAPH);

 // Once we have a paragraph, we can move the builder to do it and write our comment.
 builder.moveTo(comment.getLastParagraph());
 builder.write("My comment.");

 Assert.assertEquals(comment.getStoryType(), StoryType.COMMENTS);

 doc.save(getArtifactsDir() + "InlineStory.InsertInlineStoryNodes.docx");
 
```

**Returns:**
[Font](../../com.aspose.words/font/) - The corresponding [Font](../../com.aspose.words/font/) value.
### getFootnoteType() {#getFootnoteType}
```
public int getFootnoteType()
```


Returns a value that specifies whether this is a footnote or endnote.

 **Examples:** 

Shows the difference between footnotes and endnotes.

```

 Document doc = new Document();
 DocumentBuilder builder = new DocumentBuilder(doc);

 // Below are two ways of attaching numbered references to the text. Both these references will add a
 // small superscript reference mark at the location that we insert them.
 // The reference mark, by default, is the index number of the reference among all the references in the document.
 // Each reference will also create an entry, which will have the same reference mark as in the body text
 // and reference text, which we will pass to the document builder's "InsertFootnote" method.
 // 1 -  A footnote, whose entry will appear on the same page as the text that it references:
 builder.write("Footnote referenced main body text.");
 Footnote footnote = builder.insertFootnote(FootnoteType.FOOTNOTE, "Footnote text, will appear at the bottom of the page that contains the referenced text.");

 // 2 -  An endnote, whose entry will appear at the end of the document:
 builder.write("Endnote referenced main body text.");
 Footnote endnote = builder.insertFootnote(FootnoteType.ENDNOTE, "Endnote text, will appear at the very end of the document.");

 builder.insertBreak(BreakType.SECTION_BREAK_NEW_PAGE);
 builder.insertBreak(BreakType.SECTION_BREAK_NEW_PAGE);

 Assert.assertEquals(footnote.getFootnoteType(), FootnoteType.FOOTNOTE);
 Assert.assertEquals(endnote.getFootnoteType(), FootnoteType.ENDNOTE);

 doc.save(getArtifactsDir() + "InlineStory.FootnoteEndnote.docx");
 
```

**Returns:**
int - A value that specifies whether this is a footnote or endnote. The returned value is one of [FootnoteType](../../com.aspose.words/footnotetype/) constants.
### getLastChild() {#getLastChild}
```
public Node getLastChild()
```


Gets the last child of the node.

 **Remarks:** 

If there is no last child node, a  null  is returned.

 **Examples:** 

Shows how to use of methods of Node and CompositeNode to remove a section before the last section in the document.

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
### getLastParagraph() {#getLastParagraph}
```
public Paragraph getLastParagraph()
```


Gets the last paragraph in the story.

 **Examples:** 

Shows how to insert InlineStory nodes.

```

 Document doc = new Document();
 DocumentBuilder builder = new DocumentBuilder(doc);
 Footnote footnote = builder.insertFootnote(FootnoteType.FOOTNOTE, null);

 // Table nodes have an "EnsureMinimum()" method that makes sure the table has at least one cell.
 Table table = new Table(doc);
 table.ensureMinimum();

 // We can place a table inside a footnote, which will make it appear at the referencing page's footer.
 Assert.assertEquals(footnote.getTables().getCount(), 0);
 footnote.appendChild(table);
 Assert.assertEquals(footnote.getTables().getCount(), 1);
 Assert.assertEquals(footnote.getLastChild().getNodeType(), NodeType.TABLE);

 // An InlineStory has an "EnsureMinimum()" method as well, but in this case,
 // it makes sure the last child of the node is a paragraph,
 // for us to be able to click and write text easily in Microsoft Word.
 footnote.ensureMinimum();
 Assert.assertEquals(footnote.getLastChild().getNodeType(), NodeType.PARAGRAPH);

 // Edit the appearance of the anchor, which is the small superscript number
 // in the main text that points to the footnote.
 footnote.getFont().setName("Arial");
 footnote.getFont().setColor(Color.GREEN);

 // All inline story nodes have their respective story types.
 Assert.assertEquals(footnote.getStoryType(), StoryType.FOOTNOTES);

 // A comment is another type of inline story.
 Comment comment = (Comment) builder.getCurrentParagraph().appendChild(new Comment(doc, "John Doe", "J. D.", new Date()));

 // The parent paragraph of an inline story node will be the one from the main document body.
 Assert.assertEquals(doc.getFirstSection().getBody().getFirstParagraph(), comment.getParentParagraph());

 // However, the last paragraph is the one from the comment text contents,
 // which will be outside the main document body in a speech bubble.
 // A comment will not have any child nodes by default,
 // so we can apply the EnsureMinimum() method to place a paragraph here as well.
 Assert.assertNull(comment.getLastParagraph());
 comment.ensureMinimum();
 Assert.assertEquals(comment.getLastChild().getNodeType(), NodeType.PARAGRAPH);

 // Once we have a paragraph, we can move the builder to do it and write our comment.
 builder.moveTo(comment.getLastParagraph());
 builder.write("My comment.");

 Assert.assertEquals(comment.getStoryType(), StoryType.COMMENTS);

 doc.save(getArtifactsDir() + "InlineStory.InsertInlineStoryNodes.docx");
 
```

**Returns:**
[Paragraph](../../com.aspose.words/paragraph/) - The last paragraph in the story.
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
### getNextSibling() {#getNextSibling}
```
public Node getNextSibling()
```


Gets the node immediately following this node.

 **Remarks:** 

If there is no next node, a  null  is returned.

 **Examples:** 

Shows how to use a node's NextSibling property to enumerate through its immediate children.

```

 Document doc = new Document(getMyDir() + "Paragraphs.docx");

 for (Node node = doc.getFirstSection().getBody().getFirstChild(); node != null; node = node.getNextSibling()) {
     System.out.println(Node.nodeTypeToString(node.getNodeType()));
 }
 
```

Shows how to traverse a composite node's tree of child nodes.

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
[Node](../../com.aspose.words/node/) - The node immediately following this node.
### getNodeType() {#getNodeType}
```
public int getNodeType()
```


Returns [NodeType.FOOTNOTE](../../com.aspose.words/nodetype/\#FOOTNOTE).

 **Examples:** 

Shows how to traverse a composite node's tree of child nodes.

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
int - [NodeType.FOOTNOTE](../../com.aspose.words/nodetype/\#FOOTNOTE). The returned value is one of [NodeType](../../com.aspose.words/nodetype/) constants.
### getParagraphs() {#getParagraphs}
```
public ParagraphCollection getParagraphs()
```


Gets a collection of paragraphs that are immediate children of the story.

 **Examples:** 

Shows how to add a comment to a paragraph.

```

 Document doc = new Document();
 DocumentBuilder builder = new DocumentBuilder(doc);
 builder.write("Hello world!");

 Comment comment = new Comment(doc, "John Doe", "JD", new Date());
 builder.getCurrentParagraph().appendChild(comment);
 builder.moveTo(comment.appendChild(new Paragraph(doc)));
 builder.write("Comment text.");

 Assert.assertEquals(new Date(), comment.getDateTime());

 // In Microsoft Word, we can right-click this comment in the document body to edit it, or reply to it.
 doc.save(getArtifactsDir() + "InlineStory.AddComment.docx");
 
```

Shows how to insert and customize footnotes.

```

 Document doc = new Document();
 DocumentBuilder builder = new DocumentBuilder(doc);

 // Add text, and reference it with a footnote. This footnote will place a small superscript reference
 // mark after the text that it references and create an entry below the main body text at the bottom of the page.
 // This entry will contain the footnote's reference mark and the reference text,
 // which we will pass to the document builder's "InsertFootnote" method.
 builder.write("Main body text.");
 Footnote footnote = builder.insertFootnote(FootnoteType.FOOTNOTE, "Footnote text.");

 // If this property is set to "true", then our footnote's reference mark
 // will be its index among all the section's footnotes.
 // This is the first footnote, so the reference mark will be "1".
 Assert.assertTrue(footnote.isAuto());

 // We can move the document builder inside the footnote to edit its reference text.
 builder.moveTo(footnote.getFirstParagraph());
 builder.write(" More text added by a DocumentBuilder.");
 builder.moveToDocumentEnd();

 Assert.assertEquals(footnote.getParagraphs().get(0).toString(SaveFormat.TEXT).trim(), "Footnote text. More text added by a DocumentBuilder.");

 builder.write(" More main body text.");
 footnote = builder.insertFootnote(FootnoteType.FOOTNOTE, "Footnote text.");

 // We can set a custom reference mark which the footnote will use instead of its index number.
 footnote.setReferenceMark("RefMark");

 Assert.assertFalse(footnote.isAuto());

 // A bookmark with the "IsAuto" flag set to true will still show its real index
 // even if previous bookmarks display custom reference marks, so this bookmark's reference mark will be a "3".
 builder.write(" More main body text.");
 footnote = builder.insertFootnote(FootnoteType.FOOTNOTE, "Footnote text.");

 Assert.assertTrue(footnote.isAuto());

 doc.save(getArtifactsDir() + "InlineStory.AddFootnote.docx");
 
```

**Returns:**
[ParagraphCollection](../../com.aspose.words/paragraphcollection/) - A collection of paragraphs that are immediate children of the story.
### getParentNode() {#getParentNode}
```
public CompositeNode getParentNode()
```


Gets the immediate parent of this node.

 **Remarks:** 

If a node has just been created and not yet added to the tree, or if it has been removed from the tree, the parent is  null .

 **Examples:** 

Shows how to access a node's parent node.

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

Shows how to create a node and set its owning document.

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
### getParentParagraph() {#getParentParagraph}
```
public Paragraph getParentParagraph()
```


Retrieves the parent [Paragraph](../../com.aspose.words/paragraph/) of this node.

 **Examples:** 

Shows how to insert InlineStory nodes.

```

 Document doc = new Document();
 DocumentBuilder builder = new DocumentBuilder(doc);
 Footnote footnote = builder.insertFootnote(FootnoteType.FOOTNOTE, null);

 // Table nodes have an "EnsureMinimum()" method that makes sure the table has at least one cell.
 Table table = new Table(doc);
 table.ensureMinimum();

 // We can place a table inside a footnote, which will make it appear at the referencing page's footer.
 Assert.assertEquals(footnote.getTables().getCount(), 0);
 footnote.appendChild(table);
 Assert.assertEquals(footnote.getTables().getCount(), 1);
 Assert.assertEquals(footnote.getLastChild().getNodeType(), NodeType.TABLE);

 // An InlineStory has an "EnsureMinimum()" method as well, but in this case,
 // it makes sure the last child of the node is a paragraph,
 // for us to be able to click and write text easily in Microsoft Word.
 footnote.ensureMinimum();
 Assert.assertEquals(footnote.getLastChild().getNodeType(), NodeType.PARAGRAPH);

 // Edit the appearance of the anchor, which is the small superscript number
 // in the main text that points to the footnote.
 footnote.getFont().setName("Arial");
 footnote.getFont().setColor(Color.GREEN);

 // All inline story nodes have their respective story types.
 Assert.assertEquals(footnote.getStoryType(), StoryType.FOOTNOTES);

 // A comment is another type of inline story.
 Comment comment = (Comment) builder.getCurrentParagraph().appendChild(new Comment(doc, "John Doe", "J. D.", new Date()));

 // The parent paragraph of an inline story node will be the one from the main document body.
 Assert.assertEquals(doc.getFirstSection().getBody().getFirstParagraph(), comment.getParentParagraph());

 // However, the last paragraph is the one from the comment text contents,
 // which will be outside the main document body in a speech bubble.
 // A comment will not have any child nodes by default,
 // so we can apply the EnsureMinimum() method to place a paragraph here as well.
 Assert.assertNull(comment.getLastParagraph());
 comment.ensureMinimum();
 Assert.assertEquals(comment.getLastChild().getNodeType(), NodeType.PARAGRAPH);

 // Once we have a paragraph, we can move the builder to do it and write our comment.
 builder.moveTo(comment.getLastParagraph());
 builder.write("My comment.");

 Assert.assertEquals(comment.getStoryType(), StoryType.COMMENTS);

 doc.save(getArtifactsDir() + "InlineStory.InsertInlineStoryNodes.docx");
 
```

**Returns:**
[Paragraph](../../com.aspose.words/paragraph/) - The corresponding [Paragraph](../../com.aspose.words/paragraph/) value.
### getParentParagraph_IInline() {#getParentParagraph-IInline}
```
public Paragraph getParentParagraph_IInline()
```




**Returns:**
[Paragraph](../../com.aspose.words/paragraph/)
### getPreviousSibling() {#getPreviousSibling}
```
public Node getPreviousSibling()
```


Gets the node immediately preceding this node.

 **Remarks:** 

If there is no preceding node, a  null  is returned.

 **Examples:** 

Shows how to use of methods of Node and CompositeNode to remove a section before the last section in the document.

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


Returns a [Range](../../com.aspose.words/range/) object that represents the portion of a document that is contained in this node.

 **Examples:** 

Shows how to delete all the nodes from a range.

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
### getReferenceMark() {#getReferenceMark}
```
public String getReferenceMark()
```


Gets/sets custom reference mark to be used for this footnote. Default value is **empty string**, meaning auto-numbered footnotes are used.

 **Remarks:** 

If this property is set to **empty string** or  null , then [isAuto()](../../com.aspose.words/footnote/\#isAuto) / [isAuto(boolean)](../../com.aspose.words/footnote/\#isAuto-boolean) property will automatically be set to  true , if set to anything else then [isAuto()](../../com.aspose.words/footnote/\#isAuto) / [isAuto(boolean)](../../com.aspose.words/footnote/\#isAuto-boolean) will be set to  false .

RTF-format can only store 1 symbol as custom reference mark, so upon export only the first symbol will be written others will be discard.

 **Examples:** 

Shows how to insert and customize footnotes.

```

 Document doc = new Document();
 DocumentBuilder builder = new DocumentBuilder(doc);

 // Add text, and reference it with a footnote. This footnote will place a small superscript reference
 // mark after the text that it references and create an entry below the main body text at the bottom of the page.
 // This entry will contain the footnote's reference mark and the reference text,
 // which we will pass to the document builder's "InsertFootnote" method.
 builder.write("Main body text.");
 Footnote footnote = builder.insertFootnote(FootnoteType.FOOTNOTE, "Footnote text.");

 // If this property is set to "true", then our footnote's reference mark
 // will be its index among all the section's footnotes.
 // This is the first footnote, so the reference mark will be "1".
 Assert.assertTrue(footnote.isAuto());

 // We can move the document builder inside the footnote to edit its reference text.
 builder.moveTo(footnote.getFirstParagraph());
 builder.write(" More text added by a DocumentBuilder.");
 builder.moveToDocumentEnd();

 Assert.assertEquals(footnote.getParagraphs().get(0).toString(SaveFormat.TEXT).trim(), "Footnote text. More text added by a DocumentBuilder.");

 builder.write(" More main body text.");
 footnote = builder.insertFootnote(FootnoteType.FOOTNOTE, "Footnote text.");

 // We can set a custom reference mark which the footnote will use instead of its index number.
 footnote.setReferenceMark("RefMark");

 Assert.assertFalse(footnote.isAuto());

 // A bookmark with the "IsAuto" flag set to true will still show its real index
 // even if previous bookmarks display custom reference marks, so this bookmark's reference mark will be a "3".
 builder.write(" More main body text.");
 footnote = builder.insertFootnote(FootnoteType.FOOTNOTE, "Footnote text.");

 Assert.assertTrue(footnote.isAuto());

 doc.save(getArtifactsDir() + "InlineStory.AddFootnote.docx");
 
```

**Returns:**
java.lang.String - The corresponding java.lang.String value.
### getStoryType() {#getStoryType}
```
public int getStoryType()
```


Returns [StoryType.FOOTNOTES](../../com.aspose.words/storytype/\#FOOTNOTES) or [StoryType.ENDNOTES](../../com.aspose.words/storytype/\#ENDNOTES).

 **Examples:** 

Shows how to insert InlineStory nodes.

```

 Document doc = new Document();
 DocumentBuilder builder = new DocumentBuilder(doc);
 Footnote footnote = builder.insertFootnote(FootnoteType.FOOTNOTE, null);

 // Table nodes have an "EnsureMinimum()" method that makes sure the table has at least one cell.
 Table table = new Table(doc);
 table.ensureMinimum();

 // We can place a table inside a footnote, which will make it appear at the referencing page's footer.
 Assert.assertEquals(footnote.getTables().getCount(), 0);
 footnote.appendChild(table);
 Assert.assertEquals(footnote.getTables().getCount(), 1);
 Assert.assertEquals(footnote.getLastChild().getNodeType(), NodeType.TABLE);

 // An InlineStory has an "EnsureMinimum()" method as well, but in this case,
 // it makes sure the last child of the node is a paragraph,
 // for us to be able to click and write text easily in Microsoft Word.
 footnote.ensureMinimum();
 Assert.assertEquals(footnote.getLastChild().getNodeType(), NodeType.PARAGRAPH);

 // Edit the appearance of the anchor, which is the small superscript number
 // in the main text that points to the footnote.
 footnote.getFont().setName("Arial");
 footnote.getFont().setColor(Color.GREEN);

 // All inline story nodes have their respective story types.
 Assert.assertEquals(footnote.getStoryType(), StoryType.FOOTNOTES);

 // A comment is another type of inline story.
 Comment comment = (Comment) builder.getCurrentParagraph().appendChild(new Comment(doc, "John Doe", "J. D.", new Date()));

 // The parent paragraph of an inline story node will be the one from the main document body.
 Assert.assertEquals(doc.getFirstSection().getBody().getFirstParagraph(), comment.getParentParagraph());

 // However, the last paragraph is the one from the comment text contents,
 // which will be outside the main document body in a speech bubble.
 // A comment will not have any child nodes by default,
 // so we can apply the EnsureMinimum() method to place a paragraph here as well.
 Assert.assertNull(comment.getLastParagraph());
 comment.ensureMinimum();
 Assert.assertEquals(comment.getLastChild().getNodeType(), NodeType.PARAGRAPH);

 // Once we have a paragraph, we can move the builder to do it and write our comment.
 builder.moveTo(comment.getLastParagraph());
 builder.write("My comment.");

 Assert.assertEquals(comment.getStoryType(), StoryType.COMMENTS);

 doc.save(getArtifactsDir() + "InlineStory.InsertInlineStoryNodes.docx");
 
```

**Returns:**
int - [StoryType.FOOTNOTES](../../com.aspose.words/storytype/\#FOOTNOTES) or [StoryType.ENDNOTES](../../com.aspose.words/storytype/\#ENDNOTES). The returned value is one of [StoryType](../../com.aspose.words/storytype/) constants.
### getTables() {#getTables}
```
public TableCollection getTables()
```


Gets a collection of tables that are immediate children of the story.

 **Examples:** 

Shows how to insert InlineStory nodes.

```

 Document doc = new Document();
 DocumentBuilder builder = new DocumentBuilder(doc);
 Footnote footnote = builder.insertFootnote(FootnoteType.FOOTNOTE, null);

 // Table nodes have an "EnsureMinimum()" method that makes sure the table has at least one cell.
 Table table = new Table(doc);
 table.ensureMinimum();

 // We can place a table inside a footnote, which will make it appear at the referencing page's footer.
 Assert.assertEquals(footnote.getTables().getCount(), 0);
 footnote.appendChild(table);
 Assert.assertEquals(footnote.getTables().getCount(), 1);
 Assert.assertEquals(footnote.getLastChild().getNodeType(), NodeType.TABLE);

 // An InlineStory has an "EnsureMinimum()" method as well, but in this case,
 // it makes sure the last child of the node is a paragraph,
 // for us to be able to click and write text easily in Microsoft Word.
 footnote.ensureMinimum();
 Assert.assertEquals(footnote.getLastChild().getNodeType(), NodeType.PARAGRAPH);

 // Edit the appearance of the anchor, which is the small superscript number
 // in the main text that points to the footnote.
 footnote.getFont().setName("Arial");
 footnote.getFont().setColor(Color.GREEN);

 // All inline story nodes have their respective story types.
 Assert.assertEquals(footnote.getStoryType(), StoryType.FOOTNOTES);

 // A comment is another type of inline story.
 Comment comment = (Comment) builder.getCurrentParagraph().appendChild(new Comment(doc, "John Doe", "J. D.", new Date()));

 // The parent paragraph of an inline story node will be the one from the main document body.
 Assert.assertEquals(doc.getFirstSection().getBody().getFirstParagraph(), comment.getParentParagraph());

 // However, the last paragraph is the one from the comment text contents,
 // which will be outside the main document body in a speech bubble.
 // A comment will not have any child nodes by default,
 // so we can apply the EnsureMinimum() method to place a paragraph here as well.
 Assert.assertNull(comment.getLastParagraph());
 comment.ensureMinimum();
 Assert.assertEquals(comment.getLastChild().getNodeType(), NodeType.PARAGRAPH);

 // Once we have a paragraph, we can move the builder to do it and write our comment.
 builder.moveTo(comment.getLastParagraph());
 builder.write("My comment.");

 Assert.assertEquals(comment.getStoryType(), StoryType.COMMENTS);

 doc.save(getArtifactsDir() + "InlineStory.InsertInlineStoryNodes.docx");
 
```

**Returns:**
[TableCollection](../../com.aspose.words/tablecollection/) - A collection of tables that are immediate children of the story.
### getText() {#getText}
```
public String getText()
```


Gets the text of this node and of all its children.

 **Remarks:** 

The returned string includes all control and special characters as described in [ControlChar](../../com.aspose.words/controlchar/).

 **Examples:** 

Shows the difference between calling the GetText and ToString methods on a node.

```

 Document doc = new Document();

 DocumentBuilder builder = new DocumentBuilder(doc);
 builder.insertField("MERGEFIELD Field");

 // GetText will retrieve the visible text as well as field codes and special characters.
 Assert.assertEquals("MERGEFIELD Field«Field»\f", doc.getText());

 // ToString will give us the document's appearance if saved to a passed save format.
 Assert.assertEquals("«Field»\r\n", doc.toString(SaveFormat.TEXT));
 
```

Shows how to output all paragraphs in a document that are list items.

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
java.lang.String
### hasChildNodes() {#hasChildNodes}
```
public boolean hasChildNodes()
```


Returns  true  if this node has any child nodes.

 **Examples:** 

Shows how to combine the rows from two tables into one.

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
boolean -  true  if this node has any child nodes.
### indexOf(Node child) {#indexOf-com.aspose.words.Node}
```
public int indexOf(Node child)
```


Returns the index of the specified child node in the child node array.

 **Remarks:** 

Returns -1 if the node is not found in the child nodes.

 **Examples:** 

Shows how to get the index of a given child node from its parent.

```

 Document doc = new Document(getMyDir() + "Rendering.docx");

 Body body = doc.getFirstSection().getBody();

 // Retrieve the index of the last paragraph in the body of the first section.
 Assert.assertEquals(24, body.getChildNodes(NodeType.ANY, false).indexOf(body.getLastParagraph()));
 
```

**Parameters:**
| Parameter | Type | Description |
| --- | --- | --- |
| child | [Node](../../com.aspose.words/node/) |  |

**Returns:**
int
### insertAfter(Node newChild, Node refChild) {#insertAfter-com.aspose.words.Node-com.aspose.words.Node}
```
public Node insertAfter(Node newChild, Node refChild)
```


Inserts the specified node immediately after the specified reference node.

 **Remarks:** 

If  refChild  is  null , inserts  newChild  at the beginning of the list of child nodes.

If the  newChild  is already in the tree, it is first removed.

If the node being inserted was created from another document, you should use **M:Aspose.Words.DocumentBase.ImportNode(Aspose.Words.Node,System.Boolean,Aspose.Words.ImportFormatMode)** to import the node to the current document. The imported node can then be inserted into the current document.

 **Examples:** 

Shows how to replace all textbox shapes with image shapes.

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

Shows how to add, update and delete child nodes in a CompositeNode's collection of children.

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
| Parameter | Type | Description |
| --- | --- | --- |
| newChild | [Node](../../com.aspose.words/node/) | The [Node](../../com.aspose.words/node/) to insert. |
| refChild | [Node](../../com.aspose.words/node/) | The [Node](../../com.aspose.words/node/) that is the reference node. The  newChild  is placed after the  refChild . |

**Returns:**
[Node](../../com.aspose.words/node/) - The inserted node.
### insertBefore(Node newChild, Node refChild) {#insertBefore-com.aspose.words.Node-com.aspose.words.Node}
```
public Node insertBefore(Node newChild, Node refChild)
```


Inserts the specified node immediately before the specified reference node.

 **Remarks:** 

If  refChild  is  null , inserts  newChild  at the end of the list of child nodes.

If the  newChild  is already in the tree, it is first removed.

If the node being inserted was created from another document, you should use **M:Aspose.Words.DocumentBase.ImportNode(Aspose.Words.Node,System.Boolean,Aspose.Words.ImportFormatMode)** to import the node to the current document. The imported node can then be inserted into the current document.

 **Examples:** 

Shows how to add, update and delete child nodes in a CompositeNode's collection of children.

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
| Parameter | Type | Description |
| --- | --- | --- |
| newChild | [Node](../../com.aspose.words/node/) | The [Node](../../com.aspose.words/node/) to insert. |
| refChild | [Node](../../com.aspose.words/node/) | The [Node](../../com.aspose.words/node/) that is the reference node. The  newChild  is placed before this node. |

**Returns:**
[Node](../../com.aspose.words/node/) - The inserted node.
### isAuto() {#isAuto}
```
public boolean isAuto()
```


Holds a value that specifies whether this is a auto-numbered footnote or footnote with user defined custom reference mark.

 **Remarks:** 

[getReferenceMark()](../../com.aspose.words/footnote/\#getReferenceMark) / [setReferenceMark(java.lang.String)](../../com.aspose.words/footnote/\#setReferenceMark-java.lang.String) initialized with empty string if [isAuto()](../../com.aspose.words/footnote/\#isAuto) / [isAuto(boolean)](../../com.aspose.words/footnote/\#isAuto-boolean) set to  false .

 **Examples:** 

Shows how to insert and customize footnotes.

```

 Document doc = new Document();
 DocumentBuilder builder = new DocumentBuilder(doc);

 // Add text, and reference it with a footnote. This footnote will place a small superscript reference
 // mark after the text that it references and create an entry below the main body text at the bottom of the page.
 // This entry will contain the footnote's reference mark and the reference text,
 // which we will pass to the document builder's "InsertFootnote" method.
 builder.write("Main body text.");
 Footnote footnote = builder.insertFootnote(FootnoteType.FOOTNOTE, "Footnote text.");

 // If this property is set to "true", then our footnote's reference mark
 // will be its index among all the section's footnotes.
 // This is the first footnote, so the reference mark will be "1".
 Assert.assertTrue(footnote.isAuto());

 // We can move the document builder inside the footnote to edit its reference text.
 builder.moveTo(footnote.getFirstParagraph());
 builder.write(" More text added by a DocumentBuilder.");
 builder.moveToDocumentEnd();

 Assert.assertEquals(footnote.getParagraphs().get(0).toString(SaveFormat.TEXT).trim(), "Footnote text. More text added by a DocumentBuilder.");

 builder.write(" More main body text.");
 footnote = builder.insertFootnote(FootnoteType.FOOTNOTE, "Footnote text.");

 // We can set a custom reference mark which the footnote will use instead of its index number.
 footnote.setReferenceMark("RefMark");

 Assert.assertFalse(footnote.isAuto());

 // A bookmark with the "IsAuto" flag set to true will still show its real index
 // even if previous bookmarks display custom reference marks, so this bookmark's reference mark will be a "3".
 builder.write(" More main body text.");
 footnote = builder.insertFootnote(FootnoteType.FOOTNOTE, "Footnote text.");

 Assert.assertTrue(footnote.isAuto());

 doc.save(getArtifactsDir() + "InlineStory.AddFootnote.docx");
 
```

**Returns:**
boolean - The corresponding  boolean  value.
### isAuto(boolean value) {#isAuto-boolean}
```
public void isAuto(boolean value)
```


Holds a value that specifies whether this is a auto-numbered footnote or footnote with user defined custom reference mark.

 **Remarks:** 

[getReferenceMark()](../../com.aspose.words/footnote/\#getReferenceMark) / [setReferenceMark(java.lang.String)](../../com.aspose.words/footnote/\#setReferenceMark-java.lang.String) initialized with empty string if [isAuto()](../../com.aspose.words/footnote/\#isAuto) / [isAuto(boolean)](../../com.aspose.words/footnote/\#isAuto-boolean) set to  false .

 **Examples:** 

Shows how to insert and customize footnotes.

```

 Document doc = new Document();
 DocumentBuilder builder = new DocumentBuilder(doc);

 // Add text, and reference it with a footnote. This footnote will place a small superscript reference
 // mark after the text that it references and create an entry below the main body text at the bottom of the page.
 // This entry will contain the footnote's reference mark and the reference text,
 // which we will pass to the document builder's "InsertFootnote" method.
 builder.write("Main body text.");
 Footnote footnote = builder.insertFootnote(FootnoteType.FOOTNOTE, "Footnote text.");

 // If this property is set to "true", then our footnote's reference mark
 // will be its index among all the section's footnotes.
 // This is the first footnote, so the reference mark will be "1".
 Assert.assertTrue(footnote.isAuto());

 // We can move the document builder inside the footnote to edit its reference text.
 builder.moveTo(footnote.getFirstParagraph());
 builder.write(" More text added by a DocumentBuilder.");
 builder.moveToDocumentEnd();

 Assert.assertEquals(footnote.getParagraphs().get(0).toString(SaveFormat.TEXT).trim(), "Footnote text. More text added by a DocumentBuilder.");

 builder.write(" More main body text.");
 footnote = builder.insertFootnote(FootnoteType.FOOTNOTE, "Footnote text.");

 // We can set a custom reference mark which the footnote will use instead of its index number.
 footnote.setReferenceMark("RefMark");

 Assert.assertFalse(footnote.isAuto());

 // A bookmark with the "IsAuto" flag set to true will still show its real index
 // even if previous bookmarks display custom reference marks, so this bookmark's reference mark will be a "3".
 builder.write(" More main body text.");
 footnote = builder.insertFootnote(FootnoteType.FOOTNOTE, "Footnote text.");

 Assert.assertTrue(footnote.isAuto());

 doc.save(getArtifactsDir() + "InlineStory.AddFootnote.docx");
 
```

**Parameters:**
| Parameter | Type | Description |
| --- | --- | --- |
| value | boolean | The corresponding  boolean  value. |

### isComposite() {#isComposite}
```
public boolean isComposite()
```


Returns  true  as this node can have child nodes.

 **Examples:** 

Shows how to traverse a composite node's tree of child nodes.

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
boolean -  true  as this node can have child nodes.
### isDeleteRevision() {#isDeleteRevision}
```
public boolean isDeleteRevision()
```


Returns true if this object was deleted in Microsoft Word while change tracking was enabled.

 **Examples:** 

Shows how to view revision-related properties of InlineStory nodes.

```

 Document doc = new Document(getMyDir() + "Revision footnotes.docx");

 // When we edit the document while the "Track Changes" option, found in via Review -> Tracking,
 // is turned on in Microsoft Word, the changes we apply count as revisions.
 // When editing a document using Aspose.Words, we can begin tracking revisions by
 // invoking the document's "StartTrackRevisions" method and stop tracking by using the "StopTrackRevisions" method.
 // We can either accept revisions to assimilate them into the document
 // or reject them to undo and discard the proposed change.
 Assert.assertTrue(doc.hasRevisions());

 NodeCollection footnotes = doc.getChildNodes(NodeType.FOOTNOTE, true);
 Assert.assertEquals(5, footnotes.getCount());

 // Below are five types of revisions that can flag an InlineStory node.
 // 1 -  An "insert" revision:
 // This revision occurs when we insert text while tracking changes.
 Footnote footnote = (Footnote) footnotes.get(2);
 Assert.assertTrue(footnote.isInsertRevision());

 // 2 -  A "move from" revision:
 // When we highlight text in Microsoft Word, and then drag it to a different place in the document
 // while tracking changes, two revisions appear.
 // The "move from" revision is a copy of the text originally before we moved it.
 footnote = (Footnote) footnotes.get(4);
 Assert.assertTrue(footnote.isMoveFromRevision());

 // 3 -  A "move to" revision:
 // The "move to" revision is the text that we moved in its new position in the document.
 // "Move from" and "move to" revisions appear in pairs for every move revision we carry out.
 // Accepting a move revision deletes the "move from" revision and its text,
 // and keeps the text from the "move to" revision.
 // Rejecting a move revision conversely keeps the "move from" revision and deletes the "move to" revision.
 footnote = (Footnote) footnotes.get(1);
 Assert.assertTrue(footnote.isMoveToRevision());

 // 4 -  A "delete" revision:
 // This revision occurs when we delete text while tracking changes. When we delete text like this,
 // it will stay in the document as a revision until we either accept the revision,
 // which will delete the text for good, or reject the revision, which will keep the text we deleted where it was.
 footnote = (Footnote) footnotes.get(3);
 Assert.assertTrue(footnote.isDeleteRevision());
 
```

**Returns:**
boolean - True if this object was deleted in Microsoft Word while change tracking was enabled.
### isInsertRevision() {#isInsertRevision}
```
public boolean isInsertRevision()
```


Returns true if this object was inserted in Microsoft Word while change tracking was enabled.

 **Examples:** 

Shows how to view revision-related properties of InlineStory nodes.

```

 Document doc = new Document(getMyDir() + "Revision footnotes.docx");

 // When we edit the document while the "Track Changes" option, found in via Review -> Tracking,
 // is turned on in Microsoft Word, the changes we apply count as revisions.
 // When editing a document using Aspose.Words, we can begin tracking revisions by
 // invoking the document's "StartTrackRevisions" method and stop tracking by using the "StopTrackRevisions" method.
 // We can either accept revisions to assimilate them into the document
 // or reject them to undo and discard the proposed change.
 Assert.assertTrue(doc.hasRevisions());

 NodeCollection footnotes = doc.getChildNodes(NodeType.FOOTNOTE, true);
 Assert.assertEquals(5, footnotes.getCount());

 // Below are five types of revisions that can flag an InlineStory node.
 // 1 -  An "insert" revision:
 // This revision occurs when we insert text while tracking changes.
 Footnote footnote = (Footnote) footnotes.get(2);
 Assert.assertTrue(footnote.isInsertRevision());

 // 2 -  A "move from" revision:
 // When we highlight text in Microsoft Word, and then drag it to a different place in the document
 // while tracking changes, two revisions appear.
 // The "move from" revision is a copy of the text originally before we moved it.
 footnote = (Footnote) footnotes.get(4);
 Assert.assertTrue(footnote.isMoveFromRevision());

 // 3 -  A "move to" revision:
 // The "move to" revision is the text that we moved in its new position in the document.
 // "Move from" and "move to" revisions appear in pairs for every move revision we carry out.
 // Accepting a move revision deletes the "move from" revision and its text,
 // and keeps the text from the "move to" revision.
 // Rejecting a move revision conversely keeps the "move from" revision and deletes the "move to" revision.
 footnote = (Footnote) footnotes.get(1);
 Assert.assertTrue(footnote.isMoveToRevision());

 // 4 -  A "delete" revision:
 // This revision occurs when we delete text while tracking changes. When we delete text like this,
 // it will stay in the document as a revision until we either accept the revision,
 // which will delete the text for good, or reject the revision, which will keep the text we deleted where it was.
 footnote = (Footnote) footnotes.get(3);
 Assert.assertTrue(footnote.isDeleteRevision());
 
```

**Returns:**
boolean - True if this object was inserted in Microsoft Word while change tracking was enabled.
### isMoveFromRevision() {#isMoveFromRevision}
```
public boolean isMoveFromRevision()
```


Returns  true  if this object was moved (deleted) in Microsoft Word while change tracking was enabled.

 **Examples:** 

Shows how to view revision-related properties of InlineStory nodes.

```

 Document doc = new Document(getMyDir() + "Revision footnotes.docx");

 // When we edit the document while the "Track Changes" option, found in via Review -> Tracking,
 // is turned on in Microsoft Word, the changes we apply count as revisions.
 // When editing a document using Aspose.Words, we can begin tracking revisions by
 // invoking the document's "StartTrackRevisions" method and stop tracking by using the "StopTrackRevisions" method.
 // We can either accept revisions to assimilate them into the document
 // or reject them to undo and discard the proposed change.
 Assert.assertTrue(doc.hasRevisions());

 NodeCollection footnotes = doc.getChildNodes(NodeType.FOOTNOTE, true);
 Assert.assertEquals(5, footnotes.getCount());

 // Below are five types of revisions that can flag an InlineStory node.
 // 1 -  An "insert" revision:
 // This revision occurs when we insert text while tracking changes.
 Footnote footnote = (Footnote) footnotes.get(2);
 Assert.assertTrue(footnote.isInsertRevision());

 // 2 -  A "move from" revision:
 // When we highlight text in Microsoft Word, and then drag it to a different place in the document
 // while tracking changes, two revisions appear.
 // The "move from" revision is a copy of the text originally before we moved it.
 footnote = (Footnote) footnotes.get(4);
 Assert.assertTrue(footnote.isMoveFromRevision());

 // 3 -  A "move to" revision:
 // The "move to" revision is the text that we moved in its new position in the document.
 // "Move from" and "move to" revisions appear in pairs for every move revision we carry out.
 // Accepting a move revision deletes the "move from" revision and its text,
 // and keeps the text from the "move to" revision.
 // Rejecting a move revision conversely keeps the "move from" revision and deletes the "move to" revision.
 footnote = (Footnote) footnotes.get(1);
 Assert.assertTrue(footnote.isMoveToRevision());

 // 4 -  A "delete" revision:
 // This revision occurs when we delete text while tracking changes. When we delete text like this,
 // it will stay in the document as a revision until we either accept the revision,
 // which will delete the text for good, or reject the revision, which will keep the text we deleted where it was.
 footnote = (Footnote) footnotes.get(3);
 Assert.assertTrue(footnote.isDeleteRevision());
 
```

**Returns:**
boolean -  true  if this object was moved (deleted) in Microsoft Word while change tracking was enabled.
### isMoveToRevision() {#isMoveToRevision}
```
public boolean isMoveToRevision()
```


Returns  true  if this object was moved (inserted) in Microsoft Word while change tracking was enabled.

 **Examples:** 

Shows how to view revision-related properties of InlineStory nodes.

```

 Document doc = new Document(getMyDir() + "Revision footnotes.docx");

 // When we edit the document while the "Track Changes" option, found in via Review -> Tracking,
 // is turned on in Microsoft Word, the changes we apply count as revisions.
 // When editing a document using Aspose.Words, we can begin tracking revisions by
 // invoking the document's "StartTrackRevisions" method and stop tracking by using the "StopTrackRevisions" method.
 // We can either accept revisions to assimilate them into the document
 // or reject them to undo and discard the proposed change.
 Assert.assertTrue(doc.hasRevisions());

 NodeCollection footnotes = doc.getChildNodes(NodeType.FOOTNOTE, true);
 Assert.assertEquals(5, footnotes.getCount());

 // Below are five types of revisions that can flag an InlineStory node.
 // 1 -  An "insert" revision:
 // This revision occurs when we insert text while tracking changes.
 Footnote footnote = (Footnote) footnotes.get(2);
 Assert.assertTrue(footnote.isInsertRevision());

 // 2 -  A "move from" revision:
 // When we highlight text in Microsoft Word, and then drag it to a different place in the document
 // while tracking changes, two revisions appear.
 // The "move from" revision is a copy of the text originally before we moved it.
 footnote = (Footnote) footnotes.get(4);
 Assert.assertTrue(footnote.isMoveFromRevision());

 // 3 -  A "move to" revision:
 // The "move to" revision is the text that we moved in its new position in the document.
 // "Move from" and "move to" revisions appear in pairs for every move revision we carry out.
 // Accepting a move revision deletes the "move from" revision and its text,
 // and keeps the text from the "move to" revision.
 // Rejecting a move revision conversely keeps the "move from" revision and deletes the "move to" revision.
 footnote = (Footnote) footnotes.get(1);
 Assert.assertTrue(footnote.isMoveToRevision());

 // 4 -  A "delete" revision:
 // This revision occurs when we delete text while tracking changes. When we delete text like this,
 // it will stay in the document as a revision until we either accept the revision,
 // which will delete the text for good, or reject the revision, which will keep the text we deleted where it was.
 footnote = (Footnote) footnotes.get(3);
 Assert.assertTrue(footnote.isDeleteRevision());
 
```

**Returns:**
boolean -  true  if this object was moved (inserted) in Microsoft Word while change tracking was enabled.
### iterator() {#iterator}
```
public Iterator iterator()
```


Provides support for the for each style iteration over the child nodes of this node.

 **Examples:** 

Shows how to print all of a document's comments and their replies.

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
### nextPreOrder(Node rootNode) {#nextPreOrder-com.aspose.words.Node}
```
public Node nextPreOrder(Node rootNode)
```


Gets next node according to the pre-order tree traversal algorithm.

 **Examples:** 

Shows how to traverse the document's node tree using the pre-order traversal algorithm, and delete any encountered shape with an image.

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
| Parameter | Type | Description |
| --- | --- | --- |
| rootNode | [Node](../../com.aspose.words/node/) | The top node (limit) of traversal. |

**Returns:**
[Node](../../com.aspose.words/node/) - Next node in pre-order order. Null if reached the  rootNode .
### nodeTypeToString(int nodeType) {#nodeTypeToString-int}
```
public static String nodeTypeToString(int nodeType)
```




**Parameters:**
| Parameter | Type | Description |
| --- | --- | --- |
| nodeType | int |  |

**Returns:**
java.lang.String
### prependChild(Node newChild) {#prependChild-com.aspose.words.Node}
```
public Node prependChild(Node newChild)
```


Adds the specified node to the beginning of the list of child nodes for this node.

 **Remarks:** 

If the  newChild  is already in the tree, it is first removed.

If the node being inserted was created from another document, you should use **M:Aspose.Words.DocumentBase.ImportNode(Aspose.Words.Node,System.Boolean,Aspose.Words.ImportFormatMode)** to import the node to the current document. The imported node can then be inserted into the current document.

 **Examples:** 

Shows how to add, update and delete child nodes in a CompositeNode's collection of children.

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
| Parameter | Type | Description |
| --- | --- | --- |
| newChild | [Node](../../com.aspose.words/node/) | The node to add. |

**Returns:**
[Node](../../com.aspose.words/node/) - The node added.
### previousPreOrder(Node rootNode) {#previousPreOrder-com.aspose.words.Node}
```
public Node previousPreOrder(Node rootNode)
```


Gets the previous node according to the pre-order tree traversal algorithm.

 **Examples:** 

Shows how to traverse the document's node tree using the pre-order traversal algorithm, and delete any encountered shape with an image.

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
| Parameter | Type | Description |
| --- | --- | --- |
| rootNode | [Node](../../com.aspose.words/node/) | The top node (limit) of traversal. |

**Returns:**
[Node](../../com.aspose.words/node/) - Previous node in pre-order order. Null if reached the  rootNode .
### remove() {#remove}
```
public void remove()
```


Removes itself from the parent.

 **Examples:** 

Shows how to remove all child nodes of a specific type from a composite node.

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

Shows how to delete all shapes with images from a document.

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

### removeAllChildren() {#removeAllChildren}
```
public void removeAllChildren()
```


Removes all the child nodes of the current node.

 **Examples:** 

Shows how to construct an Aspose.Words document by hand.

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


Removes the specified child node.

 **Remarks:** 

The parent of  oldChild  is set to  null  after the node is removed.

 **Examples:** 

Shows how to use of methods of Node and CompositeNode to remove a section before the last section in the document.

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
| Parameter | Type | Description |
| --- | --- | --- |
| oldChild | [Node](../../com.aspose.words/node/) | The node to remove. |

**Returns:**
[Node](../../com.aspose.words/node/) - The removed node.
### removeMoveRevisions() {#removeMoveRevisions}
```
public void removeMoveRevisions()
```




### removeRunAttr(int key) {#removeRunAttr-int}
```
public void removeRunAttr(int key)
```




**Parameters:**
| Parameter | Type | Description |
| --- | --- | --- |
| key | int |  |

### removeSmartTags() {#removeSmartTags}
```
public void removeSmartTags()
```


Removes all [SmartTag](../../com.aspose.words/smarttag/) descendant nodes of the current node.

 **Remarks:** 

This method does not remove the content of the smart tags.

 **Examples:** 

Removes all smart tags from descendant nodes of a composite node.

```

 Document doc = new Document(getMyDir() + "Smart tags.doc");

 Assert.assertEquals(8, doc.getChildNodes(NodeType.SMART_TAG, true).getCount());

 doc.removeSmartTags();

 Assert.assertEquals(0, doc.getChildNodes(NodeType.SMART_TAG, true).getCount());
 
```

Shows how to create smart tags.

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


Selects a list of nodes matching the XPath expression.

 **Remarks:** 

Only expressions with element names are supported at the moment. Expressions that use attribute names are not supported.

 **Examples:** 

Shows how to use an XPath expression to test whether a node is inside a field.

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

Shows how to select certain nodes by using an XPath expression.

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
| Parameter | Type | Description |
| --- | --- | --- |
| xpath | java.lang.String | The XPath expression. |

**Returns:**
[NodeList](../../com.aspose.words/nodelist/) - A list of nodes matching the XPath query.
### selectSingleNode(String xpath) {#selectSingleNode-java.lang.String}
```
public Node selectSingleNode(String xpath)
```


Selects the first [Node](../../com.aspose.words/node/) that matches the XPath expression.

 **Remarks:** 

Only expressions with element names are supported at the moment. Expressions that use attribute names are not supported.

 **Examples:** 

Shows how to select certain nodes by using an XPath expression.

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
| Parameter | Type | Description |
| --- | --- | --- |
| xpath | java.lang.String | The XPath expression. |

**Returns:**
[Node](../../com.aspose.words/node/) - The first [Node](../../com.aspose.words/node/) that matches the XPath query or  null  if no matching node is found.
### setCustomNodeId(int value) {#setCustomNodeId-int}
```
public void setCustomNodeId(int value)
```


Specifies custom node identifier.

 **Remarks:** 

Default is zero.

This identifier can be set and used arbitrarily. For example, as a key to get external data.

Important note, specified value is not saved to an output file and exists only during the node lifetime.

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

**Parameters:**
| Parameter | Type | Description |
| --- | --- | --- |
| value | int | The corresponding  int  value. |

### setReferenceMark(String value) {#setReferenceMark-java.lang.String}
```
public void setReferenceMark(String value)
```


Gets/sets custom reference mark to be used for this footnote. Default value is **empty string**, meaning auto-numbered footnotes are used.

 **Remarks:** 

If this property is set to **empty string** or  null , then [isAuto()](../../com.aspose.words/footnote/\#isAuto) / [isAuto(boolean)](../../com.aspose.words/footnote/\#isAuto-boolean) property will automatically be set to  true , if set to anything else then [isAuto()](../../com.aspose.words/footnote/\#isAuto) / [isAuto(boolean)](../../com.aspose.words/footnote/\#isAuto-boolean) will be set to  false .

RTF-format can only store 1 symbol as custom reference mark, so upon export only the first symbol will be written others will be discard.

 **Examples:** 

Shows how to insert and customize footnotes.

```

 Document doc = new Document();
 DocumentBuilder builder = new DocumentBuilder(doc);

 // Add text, and reference it with a footnote. This footnote will place a small superscript reference
 // mark after the text that it references and create an entry below the main body text at the bottom of the page.
 // This entry will contain the footnote's reference mark and the reference text,
 // which we will pass to the document builder's "InsertFootnote" method.
 builder.write("Main body text.");
 Footnote footnote = builder.insertFootnote(FootnoteType.FOOTNOTE, "Footnote text.");

 // If this property is set to "true", then our footnote's reference mark
 // will be its index among all the section's footnotes.
 // This is the first footnote, so the reference mark will be "1".
 Assert.assertTrue(footnote.isAuto());

 // We can move the document builder inside the footnote to edit its reference text.
 builder.moveTo(footnote.getFirstParagraph());
 builder.write(" More text added by a DocumentBuilder.");
 builder.moveToDocumentEnd();

 Assert.assertEquals(footnote.getParagraphs().get(0).toString(SaveFormat.TEXT).trim(), "Footnote text. More text added by a DocumentBuilder.");

 builder.write(" More main body text.");
 footnote = builder.insertFootnote(FootnoteType.FOOTNOTE, "Footnote text.");

 // We can set a custom reference mark which the footnote will use instead of its index number.
 footnote.setReferenceMark("RefMark");

 Assert.assertFalse(footnote.isAuto());

 // A bookmark with the "IsAuto" flag set to true will still show its real index
 // even if previous bookmarks display custom reference marks, so this bookmark's reference mark will be a "3".
 builder.write(" More main body text.");
 footnote = builder.insertFootnote(FootnoteType.FOOTNOTE, "Footnote text.");

 Assert.assertTrue(footnote.isAuto());

 doc.save(getArtifactsDir() + "InlineStory.AddFootnote.docx");
 
```

**Parameters:**
| Parameter | Type | Description |
| --- | --- | --- |
| value | java.lang.String | The corresponding java.lang.String value. |

### setRunAttr(int fontAttr, Object value) {#setRunAttr-int-java.lang.Object}
```
public void setRunAttr(int fontAttr, Object value)
```




**Parameters:**
| Parameter | Type | Description |
| --- | --- | --- |
| fontAttr | int |  |
| value | java.lang.Object |  |

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


Exports the content of the node into a string using the specified save options.

 **Examples:** 

Exports the content of a node to String in HTML format.

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
| Parameter | Type | Description |
| --- | --- | --- |
| saveOptions | [SaveOptions](../../com.aspose.words/saveoptions/) | Specifies the options that control how the node is saved. |

**Returns:**
java.lang.String - The content of the node in the specified format.
### toString(int saveFormat) {#toString-int}
```
public String toString(int saveFormat)
```




**Parameters:**
| Parameter | Type | Description |
| --- | --- | --- |
| saveFormat | int |  |

**Returns:**
java.lang.String
