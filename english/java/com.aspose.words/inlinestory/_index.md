---
title: InlineStory
second_title: Aspose.Words for Java API Reference
description: Base class for inline-level nodes that can contain paragraphs and tables.
type: docs
weight: 352
url: /java/com.aspose.words/inlinestory/
---

**Inheritance:**
java.lang.Object, [com.aspose.words.Node](../../com.aspose.words/node), [com.aspose.words.CompositeNode](../../com.aspose.words/compositenode)
```
public abstract class InlineStory extends CompositeNode
```

Base class for inline-level nodes that can contain paragraphs and tables.

To learn more, visit the [ Logical Levels of Nodes in a Document ][Logical Levels of Nodes in a Document] documentation article.

[InlineStory](../../com.aspose.words/inlinestory) is a container for block-level nodes [Paragraph](../../com.aspose.words/paragraph) and [Table](../../com.aspose.words/table).

The classes that derive from [InlineStory](../../com.aspose.words/inlinestory) are inline-level nodes that can contain their own text (paragraphs and tables). For example, a [Comment](../../com.aspose.words/comment) node contains text of a comment and a [Footnote](../../com.aspose.words/footnote) contains text of a footnote.


[Logical Levels of Nodes in a Document]: https://docs.aspose.com/words/java/logical-levels-of-nodes-in-a-document/
## Constructors

| Constructor | Description |
| --- | --- |
| [InlineStory()](#InlineStory) |  |
## Methods

| Method | Description |
| --- | --- |
| [accept(DocumentVisitor visitor)](#accept-com.aspose.words.DocumentVisitor) | Accepts a visitor. |
| [appendChild(Node newChild)](#appendChild-com.aspose.words.Node) | Adds the specified node to the end of the list of child nodes for this node. |
| [clearRunAttrs()](#clearRunAttrs) |  |
| [dd()](#dd) |  |
| [deepClone(boolean isCloneChildren)](#deepClone-boolean) | Creates a duplicate of the node. |
| [ensureMinimum()](#ensureMinimum) | If the last child is not a paragraph, creates and appends one empty paragraph. |
| [equals(Object arg0)](#equals-java.lang.Object) |  |
| [fetchInheritedRunAttr(int fontAttr)](#fetchInheritedRunAttr-int) |  |
| [getAncestor(int ancestorType)](#getAncestor-int) |  |
| [getAncestor(Class ancestorType)](#getAncestor-java.lang.Class) | Gets the first ancestor of the specified object type. |
| [getChild(int nodeType, int index, boolean isDeep)](#getChild-int-int-boolean) |  |
| [getChildNodes()](#getChildNodes) | Gets all immediate child nodes of this node. |
| [getChildNodes(int nodeType, boolean isDeep)](#getChildNodes-int-boolean) |  |
| [getClass()](#getClass) |  |
| [getContainer()](#getContainer) |  |
| [getCount()](#getCount) | Gets the number of immediate children of this node. |
| [getCurrentNode()](#getCurrentNode) |  |
| [getCustomNodeId()](#getCustomNodeId) | Specifies custom node identifier. |
| [getDirectRunAttr(int fontAttr)](#getDirectRunAttr-int) |  |
| [getDocument()](#getDocument) | Gets the document to which this node belongs. |
| [getDocument_IInline()](#getDocument-IInline) |  |
| [getFirstChild()](#getFirstChild) | Gets the first child of the node. |
| [getFirstParagraph()](#getFirstParagraph) | Gets the first paragraph in the story. |
| [getFont()](#getFont) | Provides access to the font formatting of the anchor character of this object. |
| [getLastChild()](#getLastChild) | Gets the last child of the node. |
| [getLastParagraph()](#getLastParagraph) | Gets the last paragraph in the story. |
| [getNextMatchingNode(Node curNode)](#getNextMatchingNode-com.aspose.words.Node) |  |
| [getNextSibling()](#getNextSibling) | Gets the node immediately following this node. |
| [getNodeType()](#getNodeType) | Gets the type of this node. |
| [getParagraphs()](#getParagraphs) | Gets a collection of paragraphs that are immediate children of the story. |
| [getParentNode()](#getParentNode) | Gets the immediate parent of this node. |
| [getParentParagraph()](#getParentParagraph) | Retrieves the parent [Paragraph](../../com.aspose.words/paragraph) of this node. |
| [getParentParagraph_IInline()](#getParentParagraph-IInline) |  |
| [getPreviousSibling()](#getPreviousSibling) | Gets the node immediately preceding this node. |
| [getRange()](#getRange) | Returns a [Range](../../com.aspose.words/range) object that represents the portion of a document that is contained in this node. |
| [getStoryType()](#getStoryType) | Returns the type of the story. |
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
| [removeChild(Node oldChild)](#removeChild-com.aspose.words.Node) | Removes the specified child node. |
| [removeRunAttr(int key)](#removeRunAttr-int) |  |
| [removeSmartTags()](#removeSmartTags) | Removes all [SmartTag](../../com.aspose.words/smarttag) descendant nodes of the current node. |
| [selectNodes(String xpath)](#selectNodes-java.lang.String) | Selects a list of nodes matching the XPath expression. |
| [selectSingleNode(String xpath)](#selectSingleNode-java.lang.String) | Selects the first [Node](../../com.aspose.words/node) that matches the XPath expression. |
| [setCustomNodeId(int value)](#setCustomNodeId-int) | Specifies custom node identifier. |
| [setRunAttr(int fontAttr, Object value)](#setRunAttr-int-java.lang.Object) |  |
| [toString()](#toString) |  |
| [toString(SaveOptions saveOptions)](#toString-com.aspose.words.SaveOptions) | Exports the content of the node into a string using the specified save options. |
| [toString(int saveFormat)](#toString-int) |  |
| [wait()](#wait) |  |
| [wait(long arg0)](#wait-long) |  |
| [wait(long arg0, int arg1)](#wait-long-int) |  |
### InlineStory() {#InlineStory}
```
public InlineStory()
```


### accept(DocumentVisitor visitor) {#accept-com.aspose.words.DocumentVisitor}
```
public abstract boolean accept(DocumentVisitor visitor)
```


Accepts a visitor.

Enumerates over this node and all of its children. Each node calls a corresponding method on [DocumentVisitor](../../com.aspose.words/documentvisitor).

For more info see the Visitor design pattern.

**Parameters:**
| Parameter | Type | Description |
| --- | --- | --- |
| visitor | [DocumentVisitor](../../com.aspose.words/documentvisitor) | The visitor that will visit the nodes. |

**Returns:**
boolean - True if all nodes were visited; false if [DocumentVisitor](../../com.aspose.words/documentvisitor) stopped the operation before visiting all nodes.
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
| newChild | [Node](../../com.aspose.words/node) | The node to add. |

**Returns:**
[Node](../../com.aspose.words/node) - The node added.
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
[Node](../../com.aspose.words/node) - The cloned node.
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
[Node](../../com.aspose.words/node)
### getChildNodes() {#getChildNodes}
```
public NodeCollection getChildNodes()
```


Gets all immediate child nodes of this node.

Note, [getChildNodes()](../../com.aspose.words/compositenode\#getChildNodes) is equivalent to calling **M:Aspose.Words.CompositeNode.GetChildNodes(Aspose.Words.NodeType,System.Boolean)** with arguments ( [NodeType.ANY](../../com.aspose.words/nodetype\#ANY),  false ) and creates and returns a new collection every time it is accessed.

If there are no child nodes, this property returns an empty collection.

**Returns:**
[NodeCollection](../../com.aspose.words/nodecollection) - All immediate child nodes of this node.
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
[NodeCollection](../../com.aspose.words/nodecollection)
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
[CompositeNode](../../com.aspose.words/compositenode)
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
[Node](../../com.aspose.words/node)
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
### getDirectRunAttr(int fontAttr) {#getDirectRunAttr-int}
```
public Object getDirectRunAttr(int fontAttr)
```




**Parameters:**
| Parameter | Type | Description |
| --- | --- | --- |
| fontAttr | int |  |

**Returns:**
java.lang.Object
### getDocument() {#getDocument}
```
public DocumentBase getDocument()
```


Gets the document to which this node belongs.

The node always belongs to a document even if it has just been created and not yet added to the tree, or if it has been removed from the tree.

**Returns:**
[DocumentBase](../../com.aspose.words/documentbase) - The document to which this node belongs.
### getDocument_IInline() {#getDocument-IInline}
```
public DocumentBase getDocument_IInline()
```




**Returns:**
[DocumentBase](../../com.aspose.words/documentbase)
### getFirstChild() {#getFirstChild}
```
public Node getFirstChild()
```


Gets the first child of the node. If there is no first child node, a  null  is returned.

**Returns:**
[Node](../../com.aspose.words/node) - The first child of the node.
### getFirstParagraph() {#getFirstParagraph}
```
public Paragraph getFirstParagraph()
```


Gets the first paragraph in the story.

**Returns:**
[Paragraph](../../com.aspose.words/paragraph) - The first paragraph in the story.
### getFont() {#getFont}
```
public Font getFont()
```


Provides access to the font formatting of the anchor character of this object.

**Returns:**
[Font](../../com.aspose.words/font) - The corresponding [Font](../../com.aspose.words/font) value.
### getLastChild() {#getLastChild}
```
public Node getLastChild()
```


Gets the last child of the node. If there is no last child node, a  null  is returned.

**Returns:**
[Node](../../com.aspose.words/node) - The last child of the node.
### getLastParagraph() {#getLastParagraph}
```
public Paragraph getLastParagraph()
```


Gets the last paragraph in the story.

**Returns:**
[Paragraph](../../com.aspose.words/paragraph) - The last paragraph in the story.
### getNextMatchingNode(Node curNode) {#getNextMatchingNode-com.aspose.words.Node}
```
public Node getNextMatchingNode(Node curNode)
```




**Parameters:**
| Parameter | Type | Description |
| --- | --- | --- |
| curNode | [Node](../../com.aspose.words/node) |  |

**Returns:**
[Node](../../com.aspose.words/node)
### getNextSibling() {#getNextSibling}
```
public Node getNextSibling()
```


Gets the node immediately following this node. If there is no next node, a  null  is returned.

**Returns:**
[Node](../../com.aspose.words/node) - The node immediately following this node.
### getNodeType() {#getNodeType}
```
public abstract int getNodeType()
```


Gets the type of this node.

**Returns:**
int - The type of this node. The returned value is one of [NodeType](../../com.aspose.words/nodetype) constants.
### getParagraphs() {#getParagraphs}
```
public ParagraphCollection getParagraphs()
```


Gets a collection of paragraphs that are immediate children of the story.

**Returns:**
[ParagraphCollection](../../com.aspose.words/paragraphcollection) - A collection of paragraphs that are immediate children of the story.
### getParentNode() {#getParentNode}
```
public CompositeNode getParentNode()
```


Gets the immediate parent of this node.

If a node has just been created and not yet added to the tree, or if it has been removed from the tree, the parent is  null .

**Returns:**
[CompositeNode](../../com.aspose.words/compositenode) - The immediate parent of this node.
### getParentParagraph() {#getParentParagraph}
```
public Paragraph getParentParagraph()
```


Retrieves the parent [Paragraph](../../com.aspose.words/paragraph) of this node.

**Returns:**
[Paragraph](../../com.aspose.words/paragraph) - The corresponding [Paragraph](../../com.aspose.words/paragraph) value.
### getParentParagraph_IInline() {#getParentParagraph-IInline}
```
public Paragraph getParentParagraph_IInline()
```




**Returns:**
[Paragraph](../../com.aspose.words/paragraph)
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
### getStoryType() {#getStoryType}
```
public abstract int getStoryType()
```


Returns the type of the story.

**Returns:**
int - The type of the story. The returned value is one of [StoryType](../../com.aspose.words/storytype) constants.
### getTables() {#getTables}
```
public TableCollection getTables()
```


Gets a collection of tables that are immediate children of the story.

**Returns:**
[TableCollection](../../com.aspose.words/tablecollection) - A collection of tables that are immediate children of the story.
### getText() {#getText}
```
public String getText()
```


Gets the text of this node and of all its children.

The returned string includes all control and special characters as described in [ControlChar](../../com.aspose.words/controlchar).

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
| child | [Node](../../com.aspose.words/node) |  |

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
| newChild | [Node](../../com.aspose.words/node) | The [Node](../../com.aspose.words/node) to insert. |
| refChild | [Node](../../com.aspose.words/node) | The [Node](../../com.aspose.words/node) that is the reference node. The  newChild  is placed after the  refChild . |

**Returns:**
[Node](../../com.aspose.words/node) - The inserted node.
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
| newChild | [Node](../../com.aspose.words/node) | The [Node](../../com.aspose.words/node) to insert. |
| refChild | [Node](../../com.aspose.words/node) | The [Node](../../com.aspose.words/node) that is the reference node. The  newChild  is placed before this node. |

**Returns:**
[Node](../../com.aspose.words/node) - The inserted node.
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
| newChild | [Node](../../com.aspose.words/node) | The node to add. |

**Returns:**
[Node](../../com.aspose.words/node) - The node added.
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

### removeAllChildren() {#removeAllChildren}
```
public void removeAllChildren()
```


Removes all the child nodes of the current node.

### removeChild(Node oldChild) {#removeChild-com.aspose.words.Node}
```
public Node removeChild(Node oldChild)
```


Removes the specified child node.

The parent of  oldChild  is set to  null  after the node is removed.

**Parameters:**
| Parameter | Type | Description |
| --- | --- | --- |
| oldChild | [Node](../../com.aspose.words/node) | The node to remove. |

**Returns:**
[Node](../../com.aspose.words/node) - The removed node.
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


Removes all [SmartTag](../../com.aspose.words/smarttag) descendant nodes of the current node. This method does not remove the content of the smart tags.

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
[NodeList](../../com.aspose.words/nodelist) - A list of nodes matching the XPath query.
### selectSingleNode(String xpath) {#selectSingleNode-java.lang.String}
```
public Node selectSingleNode(String xpath)
```


Selects the first [Node](../../com.aspose.words/node) that matches the XPath expression.

Only expressions with element names are supported at the moment. Expressions that use attribute names are not supported.

**Parameters:**
| Parameter | Type | Description |
| --- | --- | --- |
| xpath | java.lang.String | The XPath expression. |

**Returns:**
[Node](../../com.aspose.words/node) - The first [Node](../../com.aspose.words/node) that matches the XPath query or  null  if no matching node is found.
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

