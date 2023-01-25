---
title: CommentRangeEnd
second_title: Aspose.Words for Java API Reference
description: Denotes the end of a region of text that has a comment associated with it.
type: docs
weight: 80
url: /java/com.aspose.words/commentrangeend/
---

**Inheritance:**
java.lang.Object, [com.aspose.words.Node](../../com.aspose.words/node)
```
public class CommentRangeEnd extends Node
```

Denotes the end of a region of text that has a comment associated with it.

To learn more, visit the [ Working with Comments ][Working with Comments] documentation article.

To create a comment anchored to a region of text, you need to create a [Comment](../../com.aspose.words/comment) and then create [CommentRangeStart](../../com.aspose.words/commentrangestart) and [CommentRangeEnd](../../com.aspose.words/commentrangeend) and set their identifiers to the same [Comment.getId()](../../com.aspose.words/comment\#getId) value.

[CommentRangeEnd](../../com.aspose.words/commentrangeend) is an inline-level node and can only be a child of [Paragraph](../../com.aspose.words/paragraph).


[Working with Comments]: https://docs.aspose.com/words/java/working-with-comments/
## Constructors

| Constructor | Description |
| --- | --- |
| [CommentRangeEnd(DocumentBase doc, int id)](#CommentRangeEnd-com.aspose.words.DocumentBase-int) | Initializes a new instance of this class. |
## Methods

| Method | Description |
| --- | --- |
| [accept(DocumentVisitor visitor)](#accept-com.aspose.words.DocumentVisitor) | Accepts a visitor. |
| [dd()](#dd) |  |
| [deepClone(boolean isCloneChildren)](#deepClone-boolean) | Creates a duplicate of the node. |
| [equals(Object arg0)](#equals-java.lang.Object) |  |
| [getAncestor(int ancestorType)](#getAncestor-int) |  |
| [getAncestor(Class ancestorType)](#getAncestor-java.lang.Class) | Gets the first ancestor of the specified object type. |
| [getClass()](#getClass) |  |
| [getCustomNodeId()](#getCustomNodeId) | Specifies custom node identifier. |
| [getDisplacedByCustomXml()](#getDisplacedByCustomXml) |  |
| [getDocument()](#getDocument) | Gets the document to which this node belongs. |
| [getId()](#getId) | Specifies the identifier of the comment to which this region is linked to. |
| [getIdInternal()](#getIdInternal) |  |
| [getNextSibling()](#getNextSibling) | Gets the node immediately following this node. |
| [getNodeType()](#getNodeType) | Returns [NodeType.COMMENT\_RANGE\_END](../../com.aspose.words/nodetype\#COMMENT-RANGE-END). |
| [getParentIdInternal()](#getParentIdInternal) |  |
| [getParentNode()](#getParentNode) | Gets the immediate parent of this node. |
| [getPreviousSibling()](#getPreviousSibling) | Gets the node immediately preceding this node. |
| [getRange()](#getRange) | Returns a [Range](../../com.aspose.words/range) object that represents the portion of a document that is contained in this node. |
| [getText()](#getText) | Gets the text of this node and of all its children. |
| [hashCode()](#hashCode) |  |
| [isComposite()](#isComposite) | Returns  true  if this node can contain other nodes. |
| [nextPreOrder(Node rootNode)](#nextPreOrder-com.aspose.words.Node) | Gets next node according to the pre-order tree traversal algorithm. |
| [nodeTypeToString(int nodeType)](#nodeTypeToString-int) |  |
| [notify()](#notify) |  |
| [notifyAll()](#notifyAll) |  |
| [previousPreOrder(Node rootNode)](#previousPreOrder-com.aspose.words.Node) | Gets the previous node according to the pre-order tree traversal algorithm. |
| [remove()](#remove) | Removes itself from the parent. |
| [setCustomNodeId(int value)](#setCustomNodeId-int) | Specifies custom node identifier. |
| [setDisplacedByCustomXml(int value)](#setDisplacedByCustomXml-int) |  |
| [setId(int value)](#setId-int) | Specifies the identifier of the comment to which this region is linked to. |
| [setIdInternal(int value)](#setIdInternal-int) |  |
| [setParentIdInternal(int value)](#setParentIdInternal-int) |  |
| [toString()](#toString) |  |
| [toString(SaveOptions saveOptions)](#toString-com.aspose.words.SaveOptions) | Exports the content of the node into a string using the specified save options. |
| [toString(int saveFormat)](#toString-int) |  |
| [wait()](#wait) |  |
| [wait(long arg0)](#wait-long) |  |
| [wait(long arg0, int arg1)](#wait-long-int) |  |
### CommentRangeEnd(DocumentBase doc, int id) {#CommentRangeEnd-com.aspose.words.DocumentBase-int}
```
public CommentRangeEnd(DocumentBase doc, int id)
```


Initializes a new instance of this class.

When [CommentRangeEnd](../../com.aspose.words/commentrangeend) is created, it belongs to the specified document, but is not yet part of the document and [Node.getParentNode()](../../com.aspose.words/node\#getParentNode) is  null .

To append a [CommentRangeEnd](../../com.aspose.words/commentrangeend) to the document use InsertAfter or InsertBefore on the paragraph where you want the comment inserted.

**Parameters:**
| Parameter | Type | Description |
| --- | --- | --- |
| doc | [DocumentBase](../../com.aspose.words/documentbase) | The owner document. |
| id | int | The comment identifier to which this object is linked. |

### accept(DocumentVisitor visitor) {#accept-com.aspose.words.DocumentVisitor}
```
public boolean accept(DocumentVisitor visitor)
```


Accepts a visitor.

Calls [DocumentVisitor.visitCommentRangeEnd(com.aspose.words.CommentRangeEnd)](../../com.aspose.words/documentvisitor\#visitCommentRangeEnd-com.aspose.words.CommentRangeEnd).

For more info see the Visitor design pattern.

**Parameters:**
| Parameter | Type | Description |
| --- | --- | --- |
| visitor | [DocumentVisitor](../../com.aspose.words/documentvisitor) | The visitor that will visit the node. |

**Returns:**
boolean - \{ false  if the visitor requested the enumeration to stop.
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
[Node](../../com.aspose.words/node) - The cloned node.
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
### getAncestor(int ancestorType) {#getAncestor-int}
```
public CompositeNode getAncestor(int ancestorType)
```




**Parameters:**
| Parameter | Type | Description |
| --- | --- | --- |
| ancestorType | int |  |

**Returns:**
[CompositeNode](../../com.aspose.words/compositenode)
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
[CompositeNode](../../com.aspose.words/compositenode) - The ancestor of the specified type or  null  if no ancestor of this type was found.

The ancestor type matches if it is equal to  ancestorType  or derived from  ancestorType .
### getClass() {#getClass}
```
public final native Class<?> getClass()
```




**Returns:**
java.lang.Class<?>
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


Gets the document to which this node belongs.

The node always belongs to a document even if it has just been created and not yet added to the tree, or if it has been removed from the tree.

**Returns:**
[DocumentBase](../../com.aspose.words/documentbase) - The document to which this node belongs.
### getId() {#getId}
```
public int getId()
```


Specifies the identifier of the comment to which this region is linked to.

**Returns:**
int - The corresponding  int  value.
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


Gets the node immediately following this node. If there is no next node, a  null  is returned.

**Returns:**
[Node](../../com.aspose.words/node) - The node immediately following this node.
### getNodeType() {#getNodeType}
```
public int getNodeType()
```


Returns [NodeType.COMMENT\_RANGE\_END](../../com.aspose.words/nodetype\#COMMENT-RANGE-END).

**Returns:**
int - \{[NodeType.COMMENT\_RANGE\_END](../../com.aspose.words/nodetype\#COMMENT-RANGE-END). The returned value is one of [NodeType](../../com.aspose.words/nodetype) constants.
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
[CompositeNode](../../com.aspose.words/compositenode) - The immediate parent of this node.
### getPreviousSibling() {#getPreviousSibling}
```
public Node getPreviousSibling()
```


Gets the node immediately preceding this node. If there is no preceding node, a  null  is returned.

**Returns:**
[Node](../../com.aspose.words/node) - The node immediately preceding this node.
### getRange() {#getRange}
```
public Range getRange()
```


Returns a [Range](../../com.aspose.words/range) object that represents the portion of a document that is contained in this node.

**Returns:**
[Range](../../com.aspose.words/range) - A [Range](../../com.aspose.words/range) object that represents the portion of a document that is contained in this node.
### getText() {#getText}
```
public String getText()
```


Gets the text of this node and of all its children.

The returned string includes all control and special characters as described in [ControlChar](../../com.aspose.words/controlchar).

**Returns:**
java.lang.String
### hashCode() {#hashCode}
```
public native int hashCode()
```




**Returns:**
int
### isComposite() {#isComposite}
```
public boolean isComposite()
```


Returns  true  if this node can contain other nodes. (31362,6)

**Returns:**
boolean - \{ true  if this node can contain other nodes.
### nextPreOrder(Node rootNode) {#nextPreOrder-com.aspose.words.Node}
```
public Node nextPreOrder(Node rootNode)
```


Gets next node according to the pre-order tree traversal algorithm.

**Parameters:**
| Parameter | Type | Description |
| --- | --- | --- |
| rootNode | [Node](../../com.aspose.words/node) | The top node (limit) of traversal. |

**Returns:**
[Node](../../com.aspose.words/node) - Next node in pre-order order. Null if reached the  rootNode .
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




### previousPreOrder(Node rootNode) {#previousPreOrder-com.aspose.words.Node}
```
public Node previousPreOrder(Node rootNode)
```


Gets the previous node according to the pre-order tree traversal algorithm.

**Parameters:**
| Parameter | Type | Description |
| --- | --- | --- |
| rootNode | [Node](../../com.aspose.words/node) | The top node (limit) of traversal. |

**Returns:**
[Node](../../com.aspose.words/node) - Previous node in pre-order order. Null if reached the  rootNode .
### remove() {#remove}
```
public void remove()
```


Removes itself from the parent.

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

### setDisplacedByCustomXml(int value) {#setDisplacedByCustomXml-int}
```
public void setDisplacedByCustomXml(int value)
```




**Parameters:**
| Parameter | Type | Description |
| --- | --- | --- |
| value | int |  |

### setId(int value) {#setId-int}
```
public void setId(int value)
```


Specifies the identifier of the comment to which this region is linked to.

**Parameters:**
| Parameter | Type | Description |
| --- | --- | --- |
| value | int | The corresponding  int  value. |

### setIdInternal(int value) {#setIdInternal-int}
```
public void setIdInternal(int value)
```




**Parameters:**
| Parameter | Type | Description |
| --- | --- | --- |
| value | int |  |

### setParentIdInternal(int value) {#setParentIdInternal-int}
```
public void setParentIdInternal(int value)
```




**Parameters:**
| Parameter | Type | Description |
| --- | --- | --- |
| value | int |  |

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
| saveOptions | [SaveOptions](../../com.aspose.words/saveoptions) | Specifies the options that control how the node is saved. |

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

