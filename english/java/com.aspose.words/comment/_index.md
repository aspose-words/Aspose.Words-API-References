---
title: Comment
linktitle: Comment
second_title: Aspose.Words for Java API Reference
description: Represents a container for text of a comment in Java.
type: docs
weight: 77
url: /java/com.aspose.words/comment/
---

**Inheritance:**
java.lang.Object, [com.aspose.words.Node](../../com.aspose.words/node/), [com.aspose.words.CompositeNode](../../com.aspose.words/compositenode/), [com.aspose.words.InlineStory](../../com.aspose.words/inlinestory/)
```
public class Comment extends InlineStory
```

Represents a container for text of a comment.

To learn more, visit the [ Working with Comments ][Working with Comments] documentation article.

A comment is an annotation which is anchored to a region of text or to a position in text. A comment can contain an arbitrary amount of block-level content.

If a [Comment](../../com.aspose.words/comment/) object occurs on its own, the comment is anchored to the position of the [Comment](../../com.aspose.words/comment/) object.

To anchor a comment to a region of text three objects are required: [Comment](../../com.aspose.words/comment/), [CommentRangeStart](../../com.aspose.words/commentrangestart/) and [CommentRangeEnd](../../com.aspose.words/commentrangeend/). All three objects need to share the same [getId()](../../com.aspose.words/comment/\#getId) value.

[Comment](../../com.aspose.words/comment/) is an inline-level node and can only be a child of [Paragraph](../../com.aspose.words/paragraph/).

[Comment](../../com.aspose.words/comment/) can contain [Paragraph](../../com.aspose.words/paragraph/) and [Table](../../com.aspose.words/table/) child nodes.


[Working with Comments]: https://docs.aspose.com/words/java/working-with-comments/
## Constructors

| Constructor | Description |
| --- | --- |
| [Comment(DocumentBase doc)](#Comment-com.aspose.words.DocumentBase) | Initializes a new instance of the [Comment](../../com.aspose.words/comment/) class. |
| [Comment(DocumentBase doc, String author, String initial, Date dateTime)](#Comment-com.aspose.words.DocumentBase-java.lang.String-java.lang.String-java.util.Date) | Initializes a new instance of the [Comment](../../com.aspose.words/comment/) class. |
## Methods

| Method | Description |
| --- | --- |
| [accept(DocumentVisitor visitor)](#accept-com.aspose.words.DocumentVisitor) | Accepts a visitor. |
| [addReply(String author, String initial, Date dateTime, String text)](#addReply-java.lang.String-java.lang.String-java.util.Date-java.lang.String) | Adds a reply to this comment. |
| [appendChild(Node newChild)](#appendChild-com.aspose.words.Node) | Adds the specified node to the end of the list of child nodes for this node. |
| [clearRunAttrs()](#clearRunAttrs) |  |
| [dd()](#dd) |  |
| [deepClone(boolean isCloneChildren)](#deepClone-boolean) | Creates a duplicate of the node. |
| [ensureMinimum()](#ensureMinimum) | If the last child is not a paragraph, creates and appends one empty paragraph. |
| [equals(Object arg0)](#equals-java.lang.Object) |  |
| [fetchInheritedRunAttr(int fontAttr)](#fetchInheritedRunAttr-int) |  |
| [getAncestor()](#getAncestor) | Returns the parent [Comment](../../com.aspose.words/comment/) object. |
| [getAncestor(int ancestorType)](#getAncestor-int) |  |
| [getAncestor(Class ancestorType)](#getAncestor-java.lang.Class) | Gets the first ancestor of the specified object type. |
| [getAuthor()](#getAuthor) | Gets the author name for a comment. |
| [getChild(int nodeType, int index, boolean isDeep)](#getChild-int-int-boolean) |  |
| [getChildNodes()](#getChildNodes) | Gets all immediate child nodes of this node. |
| [getChildNodes(int nodeType, boolean isDeep)](#getChildNodes-int-boolean) |  |
| [getClass()](#getClass) |  |
| [getContainer()](#getContainer) |  |
| [getCount()](#getCount) | Gets the number of immediate children of this node. |
| [getCurrentNode()](#getCurrentNode) |  |
| [getCustomNodeId()](#getCustomNodeId) | Specifies custom node identifier. |
| [getDateTime()](#getDateTime) | Gets the date and time that the comment was made. |
| [getDirectRunAttr(int key)](#getDirectRunAttr-int) |  |
| [getDirectRunAttr(int key, int revisionsView)](#getDirectRunAttr-int-int) |  |
| [getDocument()](#getDocument) | Gets the document to which this node belongs. |
| [getDocument_IInline()](#getDocument-IInline) |  |
| [getDone()](#getDone) | Gets flag indicating that the comment has been marked done. |
| [getFirstChild()](#getFirstChild) | Gets the first child of the node. |
| [getFirstParagraph()](#getFirstParagraph) | Gets the first paragraph in the story. |
| [getFont()](#getFont) | Provides access to the font formatting of the anchor character of this object. |
| [getId()](#getId) | Gets the comment identifier. |
| [getIdInternal()](#getIdInternal) |  |
| [getInitial()](#getInitial) | Gets the initials of the user associated with a specific comment. |
| [getLastChild()](#getLastChild) | Gets the last child of the node. |
| [getLastParagraph()](#getLastParagraph) | Gets the last paragraph in the story. |
| [getNextMatchingNode(Node curNode)](#getNextMatchingNode-com.aspose.words.Node) |  |
| [getNextSibling()](#getNextSibling) | Gets the node immediately following this node. |
| [getNodeType()](#getNodeType) | Returns [NodeType.COMMENT](../../com.aspose.words/nodetype/\#COMMENT). |
| [getParagraphs()](#getParagraphs) | Gets a collection of paragraphs that are immediate children of the story. |
| [getParentIdInternal()](#getParentIdInternal) |  |
| [getParentNode()](#getParentNode) | Gets the immediate parent of this node. |
| [getParentParagraph()](#getParentParagraph) | Retrieves the parent [Paragraph](../../com.aspose.words/paragraph/) of this node. |
| [getParentParagraph_IInline()](#getParentParagraph-IInline) |  |
| [getPreviousSibling()](#getPreviousSibling) | Gets the node immediately preceding this node. |
| [getRange()](#getRange) | Returns a [Range](../../com.aspose.words/range/) object that represents the portion of a document that is contained in this node. |
| [getReplies()](#getReplies) | Returns a collection of [Comment](../../com.aspose.words/comment/) objects that are immediate children of the specified comment. |
| [getStoryType()](#getStoryType) | Returns [StoryType.COMMENTS](../../com.aspose.words/storytype/\#COMMENTS). |
| [getTables()](#getTables) | Gets a collection of tables that are immediate children of the story. |
| [getText()](#getText) | Gets the text of this node and of all its children. |
| [hasChildNodes()](#hasChildNodes) | Returns  true  if this node has any child nodes. |
| [hashCode()](#hashCode) |  |
| [indexOf(Node child)](#indexOf-com.aspose.words.Node) | Returns the index of the specified child node in the child node array. |
| [insertAfter(Node newChild, Node refChild)](#insertAfter-com.aspose.words.Node-com.aspose.words.Node) | Inserts the specified node immediately after the specified reference node. |
| [insertBefore(Node newChild, Node refChild)](#insertBefore-com.aspose.words.Node-com.aspose.words.Node) | Inserts the specified node immediately before the specified reference node. |
| [isComposite()](#isComposite) | Returns  true  as this node can have child nodes. |
| [isDeleteRevision()](#isDeleteRevision) | Returns true if this object was deleted in Microsoft Word while change tracking was enabled. |
| [isInsertRevision()](#isInsertRevision) | Returns true if this object was inserted in Microsoft Word while change tracking was enabled. |
| [isMoveFromRevision()](#isMoveFromRevision) | Returns  true  if this object was moved (deleted) in Microsoft Word while change tracking was enabled. |
| [isMoveToRevision()](#isMoveToRevision) | Returns  true  if this object was moved (inserted) in Microsoft Word while change tracking was enabled. |
| [iterator()](#iterator) | Provides support for the for each style iteration over the child nodes of this node. |
| [nextPreOrder(Node rootNode)](#nextPreOrder-com.aspose.words.Node) | Gets next node according to the pre-order tree traversal algorithm. |
| [nodeTypeToString(int nodeType)](#nodeTypeToString-int) |  |
| [notify()](#notify) |  |
| [notifyAll()](#notifyAll) |  |
| [prependChild(Node newChild)](#prependChild-com.aspose.words.Node) | Adds the specified node to the beginning of the list of child nodes for this node. |
| [previousPreOrder(Node rootNode)](#previousPreOrder-com.aspose.words.Node) | Gets the previous node according to the pre-order tree traversal algorithm. |
| [remove()](#remove) | Removes itself from the parent. |
| [removeAllChildren()](#removeAllChildren) | Removes all the child nodes of the current node. |
| [removeAllReplies()](#removeAllReplies) | Removes all replies to this comment. |
| [removeChild(Node oldChild)](#removeChild-com.aspose.words.Node) | Removes the specified child node. |
| [removeMoveRevisions()](#removeMoveRevisions) |  |
| [removeReply(Comment reply)](#removeReply-com.aspose.words.Comment) | Removes the specified reply to this comment. |
| [removeRunAttr(int key)](#removeRunAttr-int) |  |
| [removeSmartTags()](#removeSmartTags) | Removes all [SmartTag](../../com.aspose.words/smarttag/) descendant nodes of the current node. |
| [selectNodes(String xpath)](#selectNodes-java.lang.String) | Selects a list of nodes matching the XPath expression. |
| [selectSingleNode(String xpath)](#selectSingleNode-java.lang.String) | Selects the first [Node](../../com.aspose.words/node/) that matches the XPath expression. |
| [setAuthor(String value)](#setAuthor-java.lang.String) | Sets the author name for a comment. |
| [setCustomNodeId(int value)](#setCustomNodeId-int) | Specifies custom node identifier. |
| [setDateTime(Date value)](#setDateTime-java.util.Date) | Gets the date and time that the comment was made. |
| [setDone(boolean value)](#setDone-boolean) | Sets flag indicating that the comment has been marked done. |
| [setIdInternal(int value)](#setIdInternal-int) |  |
| [setInitial(String value)](#setInitial-java.lang.String) | Sets the initials of the user associated with a specific comment. |
| [setParentIdInternal(int value)](#setParentIdInternal-int) |  |
| [setRunAttr(int fontAttr, Object value)](#setRunAttr-int-java.lang.Object) |  |
| [setText(String text)](#setText-java.lang.String) | This is a convenience method that allows to easily set text of the comment. |
| [toString()](#toString) |  |
| [toString(SaveOptions saveOptions)](#toString-com.aspose.words.SaveOptions) | Exports the content of the node into a string using the specified save options. |
| [toString(int saveFormat)](#toString-int) |  |
| [wait()](#wait) |  |
| [wait(long arg0)](#wait-long) |  |
| [wait(long arg0, int arg1)](#wait-long-int) |  |
### Comment(DocumentBase doc) {#Comment-com.aspose.words.DocumentBase}
```
public Comment(DocumentBase doc)
```


Initializes a new instance of the [Comment](../../com.aspose.words/comment/) class.

When [Comment](../../com.aspose.words/comment/) is created, it belongs to the specified document, but is not yet part of the document and [Node.getParentNode()](../../com.aspose.words/node/\#getParentNode) is  null .

To append [Comment](../../com.aspose.words/comment/) to the document use [CompositeNode.insertAfter(com.aspose.words.Node, com.aspose.words.Node)](../../com.aspose.words/compositenode/\#insertAfter-com.aspose.words.Node--com.aspose.words.Node) or [CompositeNode.insertBefore(com.aspose.words.Node, com.aspose.words.Node)](../../com.aspose.words/compositenode/\#insertBefore-com.aspose.words.Node--com.aspose.words.Node) on the paragraph where you want the comment inserted.

After creating a comment, don't forget to set its [getAuthor()](../../com.aspose.words/comment/\#getAuthor) / [setAuthor(java.lang.String)](../../com.aspose.words/comment/\#setAuthor-java.lang.String), [getInitial()](../../com.aspose.words/comment/\#getInitial) / [setInitial(java.lang.String)](../../com.aspose.words/comment/\#setInitial-java.lang.String) and [getDateTime()](../../com.aspose.words/comment/\#getDateTime) / [setDateTime(java.util.Date)](../../com.aspose.words/comment/\#setDateTime-java.util.Date) properties.

**Parameters:**
| Parameter | Type | Description |
| --- | --- | --- |
| doc | [DocumentBase](../../com.aspose.words/documentbase/) | The owner document. |

### Comment(DocumentBase doc, String author, String initial, Date dateTime) {#Comment-com.aspose.words.DocumentBase-java.lang.String-java.lang.String-java.util.Date}
```
public Comment(DocumentBase doc, String author, String initial, Date dateTime)
```


Initializes a new instance of the [Comment](../../com.aspose.words/comment/) class.

**Parameters:**
| Parameter | Type | Description |
| --- | --- | --- |
| doc | [DocumentBase](../../com.aspose.words/documentbase/) | The owner document. |
| author | java.lang.String | The author name for the comment. Cannot be  null . |
| initial | java.lang.String | The author initials for the comment. Cannot be  null . |
| dateTime | java.util.Date | The date and time for the comment. |

### accept(DocumentVisitor visitor) {#accept-com.aspose.words.DocumentVisitor}
```
public boolean accept(DocumentVisitor visitor)
```


Accepts a visitor.

Enumerates over this node and all of its children. Each node calls a corresponding method on [DocumentVisitor](../../com.aspose.words/documentvisitor/).

For more info see the Visitor design pattern.

**Parameters:**
| Parameter | Type | Description |
| --- | --- | --- |
| visitor | [DocumentVisitor](../../com.aspose.words/documentvisitor/) | The visitor that will visit the nodes. |

**Returns:**
boolean - True if all nodes were visited; false if [DocumentVisitor](../../com.aspose.words/documentvisitor/) stopped the operation before visiting all nodes. Calls [DocumentVisitor.visitCommentStart(com.aspose.words.Comment)](../../com.aspose.words/documentvisitor/\#visitCommentStart-com.aspose.words.Comment), then calls [Node.accept(com.aspose.words.DocumentVisitor)](../../com.aspose.words/node/\#accept-com.aspose.words.DocumentVisitor) for all child nodes of the comment and calls [DocumentVisitor.visitCommentEnd(com.aspose.words.Comment)](../../com.aspose.words/documentvisitor/\#visitCommentEnd-com.aspose.words.Comment) at the end.
### addReply(String author, String initial, Date dateTime, String text) {#addReply-java.lang.String-java.lang.String-java.util.Date-java.lang.String}
```
public Comment addReply(String author, String initial, Date dateTime, String text)
```


Adds a reply to this comment.

**Parameters:**
| Parameter | Type | Description |
| --- | --- | --- |
| author | java.lang.String | The author name for the reply. |
| initial | java.lang.String | The author initials for the reply. |
| dateTime | java.util.Date | The date and time for the reply. |
| text | java.lang.String | The reply text. |

**Returns:**
[Comment](../../com.aspose.words/comment/) - The created [Comment](../../com.aspose.words/comment/) node for the reply. Due to the existing MS Office limitations only 1 level of replies is allowed in the document. An exception of type java.lang.IllegalStateException will be raised if this method is called on the existing Reply comment.
### appendChild(Node newChild) {#appendChild-com.aspose.words.Node}
```
public Node appendChild(Node newChild)
```


Adds the specified node to the end of the list of child nodes for this node.

If the  newChild  is already in the tree, it is first removed.

If the node being inserted was created from another document, you should use **M:Aspose.Words.DocumentBase.ImportNode(Aspose.Words.Node,System.Boolean,Aspose.Words.ImportFormatMode)** to import the node to the current document. The imported node can then be inserted into the current document.

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




### dd() {#dd}
```
public void dd()
```




### deepClone(boolean isCloneChildren) {#deepClone-boolean}
```
public Node deepClone(boolean isCloneChildren)
```


Creates a duplicate of the node.

This method serves as a copy constructor for nodes. The cloned node has no parent, but belongs to the same document as the original node.

This method always performs a deep copy of the node. The  isCloneChildren  parameter specifies whether to perform copy all child nodes as well.

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

### equals(Object arg0) {#equals-java.lang.Object}
```
public boolean equals(Object arg0)
```




**Parameters:**
| Parameter | Type | Description |
| --- | --- | --- |
| arg0 | java.lang.Object |  |

**Returns:**
boolean
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
### getAncestor() {#getAncestor}
```
public Comment getAncestor()
```


Returns the parent [Comment](../../com.aspose.words/comment/) object. Returns  null  for top-level comments.

**Returns:**
[Comment](../../com.aspose.words/comment/) - The parent [Comment](../../com.aspose.words/comment/) object.
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

**Parameters:**
| Parameter | Type | Description |
| --- | --- | --- |
| ancestorType | java.lang.Class | The object type of the ancestor to retrieve. |

**Returns:**
[CompositeNode](../../com.aspose.words/compositenode/) - The ancestor of the specified type or  null  if no ancestor of this type was found.

The ancestor type matches if it is equal to  ancestorType  or derived from  ancestorType .
### getAuthor() {#getAuthor}
```
public String getAuthor()
```


Gets the author name for a comment.

Cannot be  null .

Default is empty string.

**Returns:**
java.lang.String - The author name for a comment.
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
### getChildNodes() {#getChildNodes}
```
public NodeCollection getChildNodes()
```


Gets all immediate child nodes of this node.

Note, [getChildNodes()](../../com.aspose.words/compositenode/\#getChildNodes) is equivalent to calling **M:Aspose.Words.CompositeNode.GetChildNodes(Aspose.Words.NodeType,System.Boolean)** with arguments ( [NodeType.ANY](../../com.aspose.words/nodetype/\#ANY),  false ) and creates and returns a new collection every time it is accessed.

If there are no child nodes, this property returns an empty collection.

**Returns:**
[NodeCollection](../../com.aspose.words/nodecollection/) - All immediate child nodes of this node.
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
### getClass() {#getClass}
```
public final native Class<?> getClass()
```




**Returns:**
java.lang.Class<?>
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

Default is zero.

This identifier can be set and used arbitrarily. For example, as a key to get external data.

Important note, specified value is not saved to an output file and exists only during the node lifetime.

**Returns:**
int - The corresponding  int  value.
### getDateTime() {#getDateTime}
```
public Date getDateTime()
```


Gets the date and time that the comment was made.

Default is 03.01.0001.

**Returns:**
java.util.Date - The date and time that the comment was made.
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

The node always belongs to a document even if it has just been created and not yet added to the tree, or if it has been removed from the tree.

**Returns:**
[DocumentBase](../../com.aspose.words/documentbase/) - The document to which this node belongs.
### getDocument_IInline() {#getDocument-IInline}
```
public DocumentBase getDocument_IInline()
```




**Returns:**
[DocumentBase](../../com.aspose.words/documentbase/)
### getDone() {#getDone}
```
public boolean getDone()
```


Gets flag indicating that the comment has been marked done.

**Returns:**
boolean - Flag indicating that the comment has been marked done.
### getFirstChild() {#getFirstChild}
```
public Node getFirstChild()
```


Gets the first child of the node. If there is no first child node, a  null  is returned.

**Returns:**
[Node](../../com.aspose.words/node/) - The first child of the node.
### getFirstParagraph() {#getFirstParagraph}
```
public Paragraph getFirstParagraph()
```


Gets the first paragraph in the story.

**Returns:**
[Paragraph](../../com.aspose.words/paragraph/) - The first paragraph in the story.
### getFont() {#getFont}
```
public Font getFont()
```


Provides access to the font formatting of the anchor character of this object.

**Returns:**
[Font](../../com.aspose.words/font/) - The corresponding [Font](../../com.aspose.words/font/) value.
### getId() {#getId}
```
public int getId()
```


Gets the comment identifier.

The comment identifier allows to anchor a comment to a region of text in the document. The region must be demarcated using the [CommentRangeStart](../../com.aspose.words/commentrangestart/) and [CommentRangeEnd](../../com.aspose.words/commentrangeend/) object sharing the same identifier value as the [Comment](../../com.aspose.words/comment/) object.

You would use this value when looking for the [CommentRangeStart](../../com.aspose.words/commentrangestart/) and [CommentRangeEnd](../../com.aspose.words/commentrangeend/) nodes that are linked to this comment.

Comment identifiers are supposed to be unique across a document and Aspose.Words automatically maintains comment identifiers when loading, saving and combining documents.

**Returns:**
int - The comment identifier.
### getIdInternal() {#getIdInternal}
```
public int getIdInternal()
```




**Returns:**
int
### getInitial() {#getInitial}
```
public String getInitial()
```


Gets the initials of the user associated with a specific comment.

Cannot be  null .

Default is empty string.

**Returns:**
java.lang.String - The initials of the user associated with a specific comment.
### getLastChild() {#getLastChild}
```
public Node getLastChild()
```


Gets the last child of the node. If there is no last child node, a  null  is returned.

**Returns:**
[Node](../../com.aspose.words/node/) - The last child of the node.
### getLastParagraph() {#getLastParagraph}
```
public Paragraph getLastParagraph()
```


Gets the last paragraph in the story.

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


Gets the node immediately following this node. If there is no next node, a  null  is returned.

**Returns:**
[Node](../../com.aspose.words/node/) - The node immediately following this node.
### getNodeType() {#getNodeType}
```
public int getNodeType()
```


Returns [NodeType.COMMENT](../../com.aspose.words/nodetype/\#COMMENT).

**Returns:**
int - \{[NodeType.COMMENT](../../com.aspose.words/nodetype/\#COMMENT). The returned value is one of [NodeType](../../com.aspose.words/nodetype/) constants.
### getParagraphs() {#getParagraphs}
```
public ParagraphCollection getParagraphs()
```


Gets a collection of paragraphs that are immediate children of the story.

**Returns:**
[ParagraphCollection](../../com.aspose.words/paragraphcollection/) - A collection of paragraphs that are immediate children of the story.
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


Gets the immediate parent of this node.

If a node has just been created and not yet added to the tree, or if it has been removed from the tree, the parent is  null .

**Returns:**
[CompositeNode](../../com.aspose.words/compositenode/) - The immediate parent of this node.
### getParentParagraph() {#getParentParagraph}
```
public Paragraph getParentParagraph()
```


Retrieves the parent [Paragraph](../../com.aspose.words/paragraph/) of this node.

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


Gets the node immediately preceding this node. If there is no preceding node, a  null  is returned.

**Returns:**
[Node](../../com.aspose.words/node/) - The node immediately preceding this node.
### getRange() {#getRange}
```
public Range getRange()
```


Returns a [Range](../../com.aspose.words/range/) object that represents the portion of a document that is contained in this node.

**Returns:**
[Range](../../com.aspose.words/range/) - A [Range](../../com.aspose.words/range/) object that represents the portion of a document that is contained in this node.
### getReplies() {#getReplies}
```
public CommentCollection getReplies()
```


Returns a collection of [Comment](../../com.aspose.words/comment/) objects that are immediate children of the specified comment.

**Returns:**
[CommentCollection](../../com.aspose.words/commentcollection/) - A collection of [Comment](../../com.aspose.words/comment/) objects that are immediate children of the specified comment.
### getStoryType() {#getStoryType}
```
public int getStoryType()
```


Returns [StoryType.COMMENTS](../../com.aspose.words/storytype/\#COMMENTS).

**Returns:**
int - \{[StoryType.COMMENTS](../../com.aspose.words/storytype/\#COMMENTS). The returned value is one of [StoryType](../../com.aspose.words/storytype/) constants.
### getTables() {#getTables}
```
public TableCollection getTables()
```


Gets a collection of tables that are immediate children of the story.

**Returns:**
[TableCollection](../../com.aspose.words/tablecollection/) - A collection of tables that are immediate children of the story.
### getText() {#getText}
```
public String getText()
```


Gets the text of this node and of all its children.

The returned string includes all control and special characters as described in [ControlChar](../../com.aspose.words/controlchar/).

**Returns:**
java.lang.String
### hasChildNodes() {#hasChildNodes}
```
public boolean hasChildNodes()
```


Returns  true  if this node has any child nodes.

**Returns:**
boolean - \{ true  if this node has any child nodes.
### hashCode() {#hashCode}
```
public native int hashCode()
```




**Returns:**
int
### indexOf(Node child) {#indexOf-com.aspose.words.Node}
```
public int indexOf(Node child)
```


Returns the index of the specified child node in the child node array. Returns -1 if the node is not found in the child nodes.

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

If  refChild  is  null , inserts  newChild  at the beginning of the list of child nodes.

If the  newChild  is already in the tree, it is first removed.

If the node being inserted was created from another document, you should use **M:Aspose.Words.DocumentBase.ImportNode(Aspose.Words.Node,System.Boolean,Aspose.Words.ImportFormatMode)** to import the node to the current document. The imported node can then be inserted into the current document.

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

If  refChild  is  null , inserts  newChild  at the end of the list of child nodes.

If the  newChild  is already in the tree, it is first removed.

If the node being inserted was created from another document, you should use **M:Aspose.Words.DocumentBase.ImportNode(Aspose.Words.Node,System.Boolean,Aspose.Words.ImportFormatMode)** to import the node to the current document. The imported node can then be inserted into the current document.

**Parameters:**
| Parameter | Type | Description |
| --- | --- | --- |
| newChild | [Node](../../com.aspose.words/node/) | The [Node](../../com.aspose.words/node/) to insert. |
| refChild | [Node](../../com.aspose.words/node/) | The [Node](../../com.aspose.words/node/) that is the reference node. The  newChild  is placed before this node. |

**Returns:**
[Node](../../com.aspose.words/node/) - The inserted node.
### isComposite() {#isComposite}
```
public boolean isComposite()
```


Returns  true  as this node can have child nodes.

**Returns:**
boolean - \{ true  as this node can have child nodes.
### isDeleteRevision() {#isDeleteRevision}
```
public boolean isDeleteRevision()
```


Returns true if this object was deleted in Microsoft Word while change tracking was enabled.

**Returns:**
boolean - True if this object was deleted in Microsoft Word while change tracking was enabled.
### isInsertRevision() {#isInsertRevision}
```
public boolean isInsertRevision()
```


Returns true if this object was inserted in Microsoft Word while change tracking was enabled.

**Returns:**
boolean - True if this object was inserted in Microsoft Word while change tracking was enabled.
### isMoveFromRevision() {#isMoveFromRevision}
```
public boolean isMoveFromRevision()
```


Returns  true  if this object was moved (deleted) in Microsoft Word while change tracking was enabled.

**Returns:**
boolean - \{ true  if this object was moved (deleted) in Microsoft Word while change tracking was enabled.
### isMoveToRevision() {#isMoveToRevision}
```
public boolean isMoveToRevision()
```


Returns  true  if this object was moved (inserted) in Microsoft Word while change tracking was enabled.

**Returns:**
boolean - \{ true  if this object was moved (inserted) in Microsoft Word while change tracking was enabled.
### iterator() {#iterator}
```
public Iterator iterator()
```


Provides support for the for each style iteration over the child nodes of this node.

**Returns:**
java.util.Iterator
### nextPreOrder(Node rootNode) {#nextPreOrder-com.aspose.words.Node}
```
public Node nextPreOrder(Node rootNode)
```


Gets next node according to the pre-order tree traversal algorithm.

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
### notify() {#notify}
```
public final native void notify()
```




### notifyAll() {#notifyAll}
```
public final native void notifyAll()
```




### prependChild(Node newChild) {#prependChild-com.aspose.words.Node}
```
public Node prependChild(Node newChild)
```


Adds the specified node to the beginning of the list of child nodes for this node.

If the  newChild  is already in the tree, it is first removed.

If the node being inserted was created from another document, you should use **M:Aspose.Words.DocumentBase.ImportNode(Aspose.Words.Node,System.Boolean,Aspose.Words.ImportFormatMode)** to import the node to the current document. The imported node can then be inserted into the current document.

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

### removeAllChildren() {#removeAllChildren}
```
public void removeAllChildren()
```


Removes all the child nodes of the current node.

### removeAllReplies() {#removeAllReplies}
```
public void removeAllReplies()
```


Removes all replies to this comment. All constituent nodes of the replies will be deleted from the document.

### removeChild(Node oldChild) {#removeChild-com.aspose.words.Node}
```
public Node removeChild(Node oldChild)
```


Removes the specified child node.

The parent of  oldChild  is set to  null  after the node is removed.

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




### removeReply(Comment reply) {#removeReply-com.aspose.words.Comment}
```
public void removeReply(Comment reply)
```


Removes the specified reply to this comment. All constituent nodes of the reply will be deleted from the document.

**Parameters:**
| Parameter | Type | Description |
| --- | --- | --- |
| reply | [Comment](../../com.aspose.words/comment/) | The comment node of the deleting reply. |

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


Removes all [SmartTag](../../com.aspose.words/smarttag/) descendant nodes of the current node. This method does not remove the content of the smart tags.

### selectNodes(String xpath) {#selectNodes-java.lang.String}
```
public NodeList selectNodes(String xpath)
```


Selects a list of nodes matching the XPath expression.

Only expressions with element names are supported at the moment. Expressions that use attribute names are not supported.

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

Only expressions with element names are supported at the moment. Expressions that use attribute names are not supported.

**Parameters:**
| Parameter | Type | Description |
| --- | --- | --- |
| xpath | java.lang.String | The XPath expression. |

**Returns:**
[Node](../../com.aspose.words/node/) - The first [Node](../../com.aspose.words/node/) that matches the XPath query or  null  if no matching node is found.
### setAuthor(String value) {#setAuthor-java.lang.String}
```
public void setAuthor(String value)
```


Sets the author name for a comment.

Cannot be  null .

Default is empty string.

**Parameters:**
| Parameter | Type | Description |
| --- | --- | --- |
| value | java.lang.String | The author name for a comment. |

### setCustomNodeId(int value) {#setCustomNodeId-int}
```
public void setCustomNodeId(int value)
```


Specifies custom node identifier.

Default is zero.

This identifier can be set and used arbitrarily. For example, as a key to get external data.

Important note, specified value is not saved to an output file and exists only during the node lifetime.

**Parameters:**
| Parameter | Type | Description |
| --- | --- | --- |
| value | int | The corresponding  int  value. |

### setDateTime(Date value) {#setDateTime-java.util.Date}
```
public void setDateTime(Date value)
```


Gets the date and time that the comment was made.

Default is 03.01.0001.

**Parameters:**
| Parameter | Type | Description |
| --- | --- | --- |
| value | java.util.Date | The date and time that the comment was made. |

### setDone(boolean value) {#setDone-boolean}
```
public void setDone(boolean value)
```


Sets flag indicating that the comment has been marked done.

**Parameters:**
| Parameter | Type | Description |
| --- | --- | --- |
| value | boolean | Flag indicating that the comment has been marked done. |

### setIdInternal(int value) {#setIdInternal-int}
```
public void setIdInternal(int value)
```




**Parameters:**
| Parameter | Type | Description |
| --- | --- | --- |
| value | int |  |

### setInitial(String value) {#setInitial-java.lang.String}
```
public void setInitial(String value)
```


Sets the initials of the user associated with a specific comment.

Cannot be  null .

Default is empty string.

**Parameters:**
| Parameter | Type | Description |
| --- | --- | --- |
| value | java.lang.String | The initials of the user associated with a specific comment. |

### setParentIdInternal(int value) {#setParentIdInternal-int}
```
public void setParentIdInternal(int value)
```




**Parameters:**
| Parameter | Type | Description |
| --- | --- | --- |
| value | int |  |

### setRunAttr(int fontAttr, Object value) {#setRunAttr-int-java.lang.Object}
```
public void setRunAttr(int fontAttr, Object value)
```




**Parameters:**
| Parameter | Type | Description |
| --- | --- | --- |
| fontAttr | int |  |
| value | java.lang.Object |  |

### setText(String text) {#setText-java.lang.String}
```
public void setText(String text)
```


This is a convenience method that allows to easily set text of the comment.

This method allows to quickly set text of a comment from a string. The string can contain paragraph breaks, this will create paragraphs of text in the comment accordingly. If you want to insert more complex elements into the comment, for example bookmarks or tables or apply rich formatting, then you need to use the appropriate node classes to build up the comment text.

**Parameters:**
| Parameter | Type | Description |
| --- | --- | --- |
| text | java.lang.String | The new text of the comment. |

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
### wait() {#wait}
```
public final void wait()
```




### wait(long arg0) {#wait-long}
```
public final native void wait(long arg0)
```




**Parameters:**
| Parameter | Type | Description |
| --- | --- | --- |
| arg0 | long |  |

### wait(long arg0, int arg1) {#wait-long-int}
```
public final void wait(long arg0, int arg1)
```




**Parameters:**
| Parameter | Type | Description |
| --- | --- | --- |
| arg0 | long |  |
| arg1 | int |  |

