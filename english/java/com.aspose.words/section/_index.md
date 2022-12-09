---
title: Section
second_title: Aspose.Words for Java API Reference
description: Represents a single section in a document.
type: docs
weight: 512
url: /java/com.aspose.words/section/
---

**Inheritance:**
java.lang.Object, [com.aspose.words.Node](../../com.aspose.words/node), [com.aspose.words.CompositeNode](../../com.aspose.words/compositenode)
```
public class Section extends CompositeNode
```

Represents a single section in a document.

To learn more, visit the [ Working with Sections ][Working with Sections] documentation article.

[Section](../../com.aspose.words/section) can have one [Body](../../com.aspose.words/body) and maximum one [HeaderFooter](../../com.aspose.words/headerfooter) of each [HeaderFooterType](../../com.aspose.words/headerfootertype). [Body](../../com.aspose.words/body) and [HeaderFooter](../../com.aspose.words/headerfooter) nodes can be in any order inside [Section](../../com.aspose.words/section).

A minimal valid section needs to have [Body](../../com.aspose.words/body) with one [Paragraph](../../com.aspose.words/paragraph).

Each section has its own set of properties that specify page size, orientation, margins etc.

You can create a copy of a section using [Node.deepClone(boolean)](../../com.aspose.words/node\#deepClone-boolean). The copy can be inserted into the same or different document.

To add, insert or remove a whole section including section break and section properties use methods of the [Document.getSections()](../../com.aspose.words/document\#getSections) object.

To copy and insert just content of the section excluding the section break and section properties use [appendContent(com.aspose.words.Section)](../../com.aspose.words/section\#appendContent-com.aspose.words.Section) and [prependContent(com.aspose.words.Section)](../../com.aspose.words/section\#prependContent-com.aspose.words.Section) methods.


[Working with Sections]: https://docs.aspose.com/words/java/working-with-sections/
## Constructors

| Constructor | Description |
| --- | --- |
| [Section(DocumentBase doc)](#Section-com.aspose.words.DocumentBase) | Initializes a new instance of the Section class. |
## Methods

| Method | Description |
| --- | --- |
| [accept(DocumentVisitor visitor)](#accept-com.aspose.words.DocumentVisitor) | Accepts a visitor. |
| [appendChild(Node newChild)](#appendChild-com.aspose.words.Node) | Adds the specified node to the end of the list of child nodes for this node. |
| [appendContent(Section sourceSection)](#appendContent-com.aspose.words.Section) | Inserts a copy of content of the source section at the end of this section. |
| [clearContent()](#clearContent) | Clears the section. |
| [clearHeadersFooters()](#clearHeadersFooters) | Clears the headers and footers of this section. |
| [clearSectionAttrs()](#clearSectionAttrs) |  |
| [dd()](#dd) |  |
| [deepClone()](#deepClone) | Creates a duplicate of this section. |
| [deepClone(boolean isCloneChildren)](#deepClone-boolean) | Creates a duplicate of the node. |
| [deleteHeaderFooterShapes()](#deleteHeaderFooterShapes) | Deletes all shapes (drawing objects) from the headers and footers of this section. |
| [ensureMinimum()](#ensureMinimum) | Ensures that the section has [getBody()](../../com.aspose.words/section\#getBody) with one [Paragraph](../../com.aspose.words/paragraph). |
| [equals(Object arg0)](#equals-java.lang.Object) |  |
| [fetchInheritedSectionAttr(int key)](#fetchInheritedSectionAttr-int) |  |
| [fetchSectionAttr(int key)](#fetchSectionAttr-int) |  |
| [getAncestor(int ancestorType)](#getAncestor-int) |  |
| [getAncestor(Class ancestorType)](#getAncestor-java.lang.Class) | Gets the first ancestor of the specified object type. |
| [getBody()](#getBody) | Returns the [Body](../../com.aspose.words/body) child node of the section. |
| [getChild(int nodeType, int index, boolean isDeep)](#getChild-int-int-boolean) |  |
| [getChildNodes()](#getChildNodes) | Gets all immediate child nodes of this node. |
| [getChildNodes(int nodeType, boolean isDeep)](#getChildNodes-int-boolean) |  |
| [getClass()](#getClass) |  |
| [getContainer()](#getContainer) |  |
| [getCount()](#getCount) | Gets the number of immediate children of this node. |
| [getCurrentNode()](#getCurrentNode) |  |
| [getCustomNodeId()](#getCustomNodeId) | Specifies custom node identifier. |
| [getDirectSectionAttr(int key)](#getDirectSectionAttr-int) |  |
| [getDocument()](#getDocument) | Gets the document to which this node belongs. |
| [getFirstChild()](#getFirstChild) | Gets the first child of the node. |
| [getHeadersFooters()](#getHeadersFooters) | Provides access to the headers and footers nodes of the section. |
| [getLastChild()](#getLastChild) | Gets the last child of the node. |
| [getNextMatchingNode(Node curNode)](#getNextMatchingNode-com.aspose.words.Node) |  |
| [getNextSibling()](#getNextSibling) | Gets the node immediately following this node. |
| [getNodeType()](#getNodeType) | Returns [NodeType.SECTION](../../com.aspose.words/nodetype\#SECTION). |
| [getPageSetup()](#getPageSetup) | Returns an object that represents page setup and section properties. |
| [getParentNode()](#getParentNode) | Gets the immediate parent of this node. |
| [getPreviousSibling()](#getPreviousSibling) | Gets the node immediately preceding this node. |
| [getProtectedForForms()](#getProtectedForForms) | True if the section is protected for forms. |
| [getRange()](#getRange) | Returns a [Range](../../com.aspose.words/range) object that represents the portion of a document that is contained in this node. |
| [getText()](#getText) | Gets the text of this node and of all its children. |
| [hasChildNodes()](#hasChildNodes) | Returns  true  if this node has any child nodes. |
| [hashCode()](#hashCode) |  |
| [indexOf(Node child)](#indexOf-com.aspose.words.Node) | Returns the index of the specified child node in the child node array. |
| [insertAfter(Node newChild, Node refChild)](#insertAfter-com.aspose.words.Node-com.aspose.words.Node) | Inserts the specified node immediately after the specified reference node. |
| [insertBefore(Node newChild, Node refChild)](#insertBefore-com.aspose.words.Node-com.aspose.words.Node) | Inserts the specified node immediately before the specified reference node. |
| [isComposite()](#isComposite) | Returns  true  as this node can have child nodes. |
| [iterator()](#iterator) | Provides support for the for each style iteration over the child nodes of this node. |
| [nextPreOrder(Node rootNode)](#nextPreOrder-com.aspose.words.Node) | Gets next node according to the pre-order tree traversal algorithm. |
| [nodeTypeToString(int nodeType)](#nodeTypeToString-int) |  |
| [notify()](#notify) |  |
| [notifyAll()](#notifyAll) |  |
| [prependChild(Node newChild)](#prependChild-com.aspose.words.Node) | Adds the specified node to the beginning of the list of child nodes for this node. |
| [prependContent(Section sourceSection)](#prependContent-com.aspose.words.Section) | Inserts a copy of content of the source section at the beginning of this section. |
| [previousPreOrder(Node rootNode)](#previousPreOrder-com.aspose.words.Node) | Gets the previous node according to the pre-order tree traversal algorithm. |
| [remove()](#remove) | Removes itself from the parent. |
| [removeAllChildren()](#removeAllChildren) | Removes all the child nodes of the current node. |
| [removeChild(Node oldChild)](#removeChild-com.aspose.words.Node) | Removes the specified child node. |
| [removeSmartTags()](#removeSmartTags) | Removes all [SmartTag](../../com.aspose.words/smarttag) descendant nodes of the current node. |
| [selectNodes(String xpath)](#selectNodes-java.lang.String) | Selects a list of nodes matching the XPath expression. |
| [selectSingleNode(String xpath)](#selectSingleNode-java.lang.String) | Selects the first [Node](../../com.aspose.words/node) that matches the XPath expression. |
| [setCustomNodeId(int value)](#setCustomNodeId-int) | Specifies custom node identifier. |
| [setProtectedForForms(boolean value)](#setProtectedForForms-boolean) | True if the section is protected for forms. |
| [setSectionAttr(int key, Object value)](#setSectionAttr-int-java.lang.Object) |  |
| [toString()](#toString) |  |
| [toString(SaveOptions saveOptions)](#toString-com.aspose.words.SaveOptions) | Exports the content of the node into a string using the specified save options. |
| [toString(int saveFormat)](#toString-int) |  |
| [wait()](#wait) |  |
| [wait(long arg0)](#wait-long) |  |
| [wait(long arg0, int arg1)](#wait-long-int) |  |
### Section(DocumentBase doc) {#Section-com.aspose.words.DocumentBase}
```
public Section(DocumentBase doc)
```


Initializes a new instance of the Section class.

When the section is created, it belongs to the specified document, but is not yet part of the document and [Node.getParentNode()](../../com.aspose.words/node\#getParentNode) is  null .

To include [Section](../../com.aspose.words/section) into a document use [CompositeNode.insertAfter(com.aspose.words.Node, com.aspose.words.Node)](../../com.aspose.words/compositenode\#insertAfter-com.aspose.words.Node--com.aspose.words.Node) and [CompositeNode.insertBefore(com.aspose.words.Node, com.aspose.words.Node)](../../com.aspose.words/compositenode\#insertBefore-com.aspose.words.Node--com.aspose.words.Node) methods of the [Document](../../com.aspose.words/document) OR [NodeCollection.add(com.aspose.words.Node)](../../com.aspose.words/nodecollection\#add-com.aspose.words.Node) and [NodeCollection.insert(int, com.aspose.words.Node)](../../com.aspose.words/nodecollection\#insert-int--com.aspose.words.Node) methods of the [Document.getSections()](../../com.aspose.words/document\#getSections) property.

**Parameters:**
| Parameter | Type | Description |
| --- | --- | --- |
| doc | [DocumentBase](../../com.aspose.words/documentbase) | The owner document. |

### accept(DocumentVisitor visitor) {#accept-com.aspose.words.DocumentVisitor}
```
public boolean accept(DocumentVisitor visitor)
```


Accepts a visitor.

Enumerates over this node and all of its children. Each node calls a corresponding method on [DocumentVisitor](../../com.aspose.words/documentvisitor).

For more info see the Visitor design pattern.

**Parameters:**
| Parameter | Type | Description |
| --- | --- | --- |
| visitor | [DocumentVisitor](../../com.aspose.words/documentvisitor) | The visitor that will visit the nodes. |

**Returns:**
boolean - True if all nodes were visited; false if [DocumentVisitor](../../com.aspose.words/documentvisitor) stopped the operation before visiting all nodes. Calls [DocumentVisitor.visitSectionStart(com.aspose.words.Section)](../../com.aspose.words/documentvisitor\#visitSectionStart-com.aspose.words.Section), then calls [Node.accept(com.aspose.words.DocumentVisitor)](../../com.aspose.words/node\#accept-com.aspose.words.DocumentVisitor) for all child nodes of the section and calls [DocumentVisitor.visitSectionEnd(com.aspose.words.Section)](../../com.aspose.words/documentvisitor\#visitSectionEnd-com.aspose.words.Section) at the end.
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
### appendContent(Section sourceSection) {#appendContent-com.aspose.words.Section}
```
public void appendContent(Section sourceSection)
```


Inserts a copy of content of the source section at the end of this section.

Only content of [getBody()](../../com.aspose.words/section\#getBody) of the source section is copied, page setup, headers and footers are not copied.

The nodes are automatically imported if the source section belongs to a different document.

No new section is created in the destination document.

**Parameters:**
| Parameter | Type | Description |
| --- | --- | --- |
| sourceSection | [Section](../../com.aspose.words/section) | The section to copy content from. |

### clearContent() {#clearContent}
```
public void clearContent()
```


Clears the section.

The text of [getBody()](../../com.aspose.words/section\#getBody) is cleared, only one empty paragraph is left that represents the section break.

The text of all headers and footers is cleared, but [HeaderFooter](../../com.aspose.words/headerfooter) objects themselves are not removed.

### clearHeadersFooters() {#clearHeadersFooters}
```
public void clearHeadersFooters()
```


Clears the headers and footers of this section.

The text of all headers and footers is cleared, but [HeaderFooter](../../com.aspose.words/headerfooter) objects themselves are not removed.

This makes headers and footers of this section linked to headers and footers of the previous section.

### clearSectionAttrs() {#clearSectionAttrs}
```
public void clearSectionAttrs()
```




### dd() {#dd}
```
public void dd()
```




### deepClone() {#deepClone}
```
public Section deepClone()
```


Creates a duplicate of this section.

**Returns:**
[Section](../../com.aspose.words/section)
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
### deleteHeaderFooterShapes() {#deleteHeaderFooterShapes}
```
public void deleteHeaderFooterShapes()
```


Deletes all shapes (drawing objects) from the headers and footers of this section.

### ensureMinimum() {#ensureMinimum}
```
public void ensureMinimum()
```


Ensures that the section has [getBody()](../../com.aspose.words/section\#getBody) with one [Paragraph](../../com.aspose.words/paragraph).

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
### fetchInheritedSectionAttr(int key) {#fetchInheritedSectionAttr-int}
```
public Object fetchInheritedSectionAttr(int key)
```




**Parameters:**
| Parameter | Type | Description |
| --- | --- | --- |
| key | int |  |

**Returns:**
java.lang.Object
### fetchSectionAttr(int key) {#fetchSectionAttr-int}
```
public Object fetchSectionAttr(int key)
```




**Parameters:**
| Parameter | Type | Description |
| --- | --- | --- |
| key | int |  |

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
### getBody() {#getBody}
```
public Body getBody()
```


Returns the [Body](../../com.aspose.words/body) child node of the section.

[Body](../../com.aspose.words/body) contains main text of the section.

Returns  null  if the section does not have a [Body](../../com.aspose.words/body) node among its children.

**Returns:**
[Body](../../com.aspose.words/body) - The [Body](../../com.aspose.words/body) child node of the section.
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
### getDirectSectionAttr(int key) {#getDirectSectionAttr-int}
```
public Object getDirectSectionAttr(int key)
```




**Parameters:**
| Parameter | Type | Description |
| --- | --- | --- |
| key | int |  |

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
### getFirstChild() {#getFirstChild}
```
public Node getFirstChild()
```


Gets the first child of the node. If there is no first child node, a  null  is returned.

**Returns:**
[Node](../../com.aspose.words/node) - The first child of the node.
### getHeadersFooters() {#getHeadersFooters}
```
public HeaderFooterCollection getHeadersFooters()
```


Provides access to the headers and footers nodes of the section.

**Returns:**
[HeaderFooterCollection](../../com.aspose.words/headerfootercollection) - The corresponding [HeaderFooterCollection](../../com.aspose.words/headerfootercollection) value.
### getLastChild() {#getLastChild}
```
public Node getLastChild()
```


Gets the last child of the node. If there is no last child node, a  null  is returned.

**Returns:**
[Node](../../com.aspose.words/node) - The last child of the node.
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
public int getNodeType()
```


Returns [NodeType.SECTION](../../com.aspose.words/nodetype\#SECTION).

**Returns:**
int - \{[NodeType.SECTION](../../com.aspose.words/nodetype\#SECTION). The returned value is one of [NodeType](../../com.aspose.words/nodetype) constants.
### getPageSetup() {#getPageSetup}
```
public PageSetup getPageSetup()
```


Returns an object that represents page setup and section properties.

**Returns:**
[PageSetup](../../com.aspose.words/pagesetup) - An object that represents page setup and section properties.
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
### getProtectedForForms() {#getProtectedForForms}
```
public boolean getProtectedForForms()
```


True if the section is protected for forms. When a section is protected for forms, users can select and modify text only in form fields in Microsoft Word.

**Returns:**
boolean - The corresponding  boolean  value.
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
### prependContent(Section sourceSection) {#prependContent-com.aspose.words.Section}
```
public void prependContent(Section sourceSection)
```


Inserts a copy of content of the source section at the beginning of this section.

Only content of [getBody()](../../com.aspose.words/section\#getBody) of the source section is copied, page setup, headers and footers are not copied.

The nodes are automatically imported if the source section belongs to a different document.

No new section is created in the destination document.

**Parameters:**
| Parameter | Type | Description |
| --- | --- | --- |
| sourceSection | [Section](../../com.aspose.words/section) | The section to copy content from. |

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

### setProtectedForForms(boolean value) {#setProtectedForForms-boolean}
```
public void setProtectedForForms(boolean value)
```


True if the section is protected for forms. When a section is protected for forms, users can select and modify text only in form fields in Microsoft Word.

**Parameters:**
| Parameter | Type | Description |
| --- | --- | --- |
| value | boolean | The corresponding  boolean  value. |

### setSectionAttr(int key, Object value) {#setSectionAttr-int-java.lang.Object}
```
public void setSectionAttr(int key, Object value)
```




**Parameters:**
| Parameter | Type | Description |
| --- | --- | --- |
| key | int |  |
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

