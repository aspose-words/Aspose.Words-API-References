---
title: DocumentBase
second_title: Aspose.Words for Java API Reference
description: Provides the abstract base class for a main document and a glossary document of a Word document.
type: docs
weight: 122
url: /java/com.aspose.words/documentbase/
---

**Inheritance:**
java.lang.Object, [com.aspose.words.Node](../../com.aspose.words/node), [com.aspose.words.CompositeNode](../../com.aspose.words/compositenode)
```
public abstract class DocumentBase extends CompositeNode
```

Provides the abstract base class for a main document and a glossary document of a Word document.

To learn more, visit the [ Aspose.Words Document Object Model (DOM) ][Aspose.Words Document Object Model _DOM_] documentation article.

Aspose.Words represents a Word document as a tree of nodes. [DocumentBase](../../com.aspose.words/documentbase) is a root node of the tree that contains all other nodes of the document.

[DocumentBase](../../com.aspose.words/documentbase) also stores document-wide information such as [getStyles()](../../com.aspose.words/documentbase\#getStyles) and [getLists()](../../com.aspose.words/documentbase\#getLists) that the tree nodes might refer to.


[Aspose.Words Document Object Model _DOM_]: https://docs.aspose.com/words/java/aspose-words-document-object-model/
## Methods

| Method | Description |
| --- | --- |
| [accept(DocumentVisitor visitor)](#accept-com.aspose.words.DocumentVisitor) | Accepts a visitor. |
| [appendChild(Node newChild)](#appendChild-com.aspose.words.Node) | Adds the specified node to the end of the list of child nodes for this node. |
| [dd()](#dd) |  |
| [deepClone(boolean isCloneChildren)](#deepClone-boolean) | Creates a duplicate of the node. |
| [equals(Object arg0)](#equals-java.lang.Object) |  |
| [getAncestor(int ancestorType)](#getAncestor-int) |  |
| [getAncestor(Class ancestorType)](#getAncestor-java.lang.Class) | Gets the first ancestor of the specified object type. |
| [getBackgroundShape()](#getBackgroundShape) | Gets the background shape of the document. |
| [getChild(int nodeType, int index, boolean isDeep)](#getChild-int-int-boolean) |  |
| [getChildNodes()](#getChildNodes) | Gets all immediate child nodes of this node. |
| [getChildNodes(int nodeType, boolean isDeep)](#getChildNodes-int-boolean) |  |
| [getClass()](#getClass) |  |
| [getContainer()](#getContainer) |  |
| [getCount()](#getCount) | Gets the number of immediate children of this node. |
| [getCurrentNode()](#getCurrentNode) |  |
| [getCustomNodeId()](#getCustomNodeId) | Specifies custom node identifier. |
| [getDocument()](#getDocument) |  |
| [getFirstChild()](#getFirstChild) | Gets the first child of the node. |
| [getFontInfos()](#getFontInfos) | Provides access to properties of fonts used in this document. |
| [getLastChild()](#getLastChild) | Gets the last child of the node. |
| [getLists()](#getLists) | Provides access to the list formatting used in the document. |
| [getNextMatchingNode(Node curNode)](#getNextMatchingNode-com.aspose.words.Node) |  |
| [getNextSibling()](#getNextSibling) | Gets the node immediately following this node. |
| [getNodeChangingCallback()](#getNodeChangingCallback) | Called when a node is inserted or removed in the document. |
| [getNodeType()](#getNodeType) | Gets the type of this node. |
| [getPageColor()](#getPageColor) | Gets the page color of the document. |
| [getParentNode()](#getParentNode) | Gets the immediate parent of this node. |
| [getPreviousSibling()](#getPreviousSibling) | Gets the node immediately preceding this node. |
| [getRange()](#getRange) | Returns a [Range](../../com.aspose.words/range) object that represents the portion of a document that is contained in this node. |
| [getResourceLoadingCallback()](#getResourceLoadingCallback) | Allows to control how external resources are loaded. |
| [getStyles()](#getStyles) | Returns a collection of styles defined in the document. |
| [getText()](#getText) | Gets the text of this node and of all its children. |
| [getWarningCallback()](#getWarningCallback) | Called during various document processing procedures when an issue is detected that might result in data or formatting fidelity loss. |
| [hasChildNodes()](#hasChildNodes) | Returns  true  if this node has any child nodes. |
| [hashCode()](#hashCode) |  |
| [importNode(Node srcNode, boolean isImportChildren)](#importNode-com.aspose.words.Node-boolean) | Imports a node from another document to the current document. |
| [importNode(Node srcNode, boolean isImportChildren, int importFormatMode)](#importNode-com.aspose.words.Node-boolean-int) |  |
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
| [previousPreOrder(Node rootNode)](#previousPreOrder-com.aspose.words.Node) | Gets the previous node according to the pre-order tree traversal algorithm. |
| [remove()](#remove) | Removes itself from the parent. |
| [removeAllChildren()](#removeAllChildren) | Removes all the child nodes of the current node. |
| [removeChild(Node oldChild)](#removeChild-com.aspose.words.Node) | Removes the specified child node. |
| [removeSmartTags()](#removeSmartTags) | Removes all [SmartTag](../../com.aspose.words/smarttag) descendant nodes of the current node. |
| [selectNodes(String xpath)](#selectNodes-java.lang.String) | Selects a list of nodes matching the XPath expression. |
| [selectSingleNode(String xpath)](#selectSingleNode-java.lang.String) | Selects the first [Node](../../com.aspose.words/node) that matches the XPath expression. |
| [setBackgroundShape(Shape value)](#setBackgroundShape-com.aspose.words.Shape) | Sets the background shape of the document. |
| [setCustomNodeId(int value)](#setCustomNodeId-int) | Specifies custom node identifier. |
| [setNodeChangingCallback(INodeChangingCallback value)](#setNodeChangingCallback-com.aspose.words.INodeChangingCallback) | Called when a node is inserted or removed in the document. |
| [setPageColor(Color value)](#setPageColor-java.awt.Color) | Sets the page color of the document. |
| [setResourceLoadingCallback(IResourceLoadingCallback value)](#setResourceLoadingCallback-com.aspose.words.IResourceLoadingCallback) | Allows to control how external resources are loaded. |
| [setWarningCallback(IWarningCallback value)](#setWarningCallback-com.aspose.words.IWarningCallback) | Called during various document processing procedures when an issue is detected that might result in data or formatting fidelity loss. |
| [toString()](#toString) |  |
| [toString(SaveOptions saveOptions)](#toString-com.aspose.words.SaveOptions) | Exports the content of the node into a string using the specified save options. |
| [toString(int saveFormat)](#toString-int) |  |
| [wait()](#wait) |  |
| [wait(long arg0)](#wait-long) |  |
| [wait(long arg0, int arg1)](#wait-long-int) |  |
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
### getBackgroundShape() {#getBackgroundShape}
```
public Shape getBackgroundShape()
```


Gets the background shape of the document. Can be  null .

Microsoft Word allows only a shape that has its [ShapeBase.getShapeType()](../../com.aspose.words/shapebase\#getShapeType) property equal to [ShapeType.RECTANGLE](../../com.aspose.words/shapetype\#RECTANGLE) to be used as a background shape for a document.

Microsoft Word supports only the fill properties of a background shape. All other properties are ignored.

Setting this property to a non-null value will also set the [ViewOptions.getDisplayBackgroundShape()](../../com.aspose.words/viewoptions\#getDisplayBackgroundShape) / [ViewOptions.setDisplayBackgroundShape(boolean)](../../com.aspose.words/viewoptions\#setDisplayBackgroundShape-boolean) to  true .

**Returns:**
[Shape](../../com.aspose.words/shape) - The background shape of the document.
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
### getDocument() {#getDocument}
```
public DocumentBase getDocument()
```


Gets the document to which this node belongs.

The node always belongs to a document even if it has just been created and not yet added to the tree, or if it has been removed from the tree.

**Returns:**
[DocumentBase](../../com.aspose.words/documentbase)
### getFirstChild() {#getFirstChild}
```
public Node getFirstChild()
```


Gets the first child of the node. If there is no first child node, a  null  is returned.

**Returns:**
[Node](../../com.aspose.words/node) - The first child of the node.
### getFontInfos() {#getFontInfos}
```
public FontInfoCollection getFontInfos()
```


Provides access to properties of fonts used in this document.

This collection of font definitions is loaded as is from the document. Font definitions might be optional, missing or incomplete in some documents.

Do not rely on this collection to ascertain that a particular font is used in the document. You should only use this collection to get information about fonts that might be used in the document.

**Returns:**
[FontInfoCollection](../../com.aspose.words/fontinfocollection) - The corresponding [FontInfoCollection](../../com.aspose.words/fontinfocollection) value.
### getLastChild() {#getLastChild}
```
public Node getLastChild()
```


Gets the last child of the node. If there is no last child node, a  null  is returned.

**Returns:**
[Node](../../com.aspose.words/node) - The last child of the node.
### getLists() {#getLists}
```
public ListCollection getLists()
```


Provides access to the list formatting used in the document.

For more information see the description of the [ListCollection](../../com.aspose.words/listcollection) class.

**Returns:**
[ListCollection](../../com.aspose.words/listcollection) - The corresponding [ListCollection](../../com.aspose.words/listcollection) value.
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
### getNodeChangingCallback() {#getNodeChangingCallback}
```
public INodeChangingCallback getNodeChangingCallback()
```


Called when a node is inserted or removed in the document.

**Returns:**
[INodeChangingCallback](../../com.aspose.words/inodechangingcallback) - The corresponding [INodeChangingCallback](../../com.aspose.words/inodechangingcallback) value.
### getNodeType() {#getNodeType}
```
public abstract int getNodeType()
```


Gets the type of this node.

**Returns:**
int - The type of this node. The returned value is one of [NodeType](../../com.aspose.words/nodetype) constants.
### getPageColor() {#getPageColor}
```
public Color getPageColor()
```


Gets the page color of the document. This property is a simpler version of [getBackgroundShape()](../../com.aspose.words/documentbase\#getBackgroundShape) / [setBackgroundShape(com.aspose.words.Shape)](../../com.aspose.words/documentbase\#setBackgroundShape-com.aspose.words.Shape).

This property provides a simple way to specify a solid page color for the document. Setting this property creates and sets an appropriate [getBackgroundShape()](../../com.aspose.words/documentbase\#getBackgroundShape) / [setBackgroundShape(com.aspose.words.Shape)](../../com.aspose.words/documentbase\#setBackgroundShape-com.aspose.words.Shape).

If the page color is not set (e.g. there is no background shape in the document) returns a zero color.

**Returns:**
java.awt.Color - The page color of the document.
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
### getResourceLoadingCallback() {#getResourceLoadingCallback}
```
public IResourceLoadingCallback getResourceLoadingCallback()
```


Allows to control how external resources are loaded.

**Returns:**
[IResourceLoadingCallback](../../com.aspose.words/iresourceloadingcallback) - The corresponding [IResourceLoadingCallback](../../com.aspose.words/iresourceloadingcallback) value.
### getStyles() {#getStyles}
```
public StyleCollection getStyles()
```


Returns a collection of styles defined in the document.

For more information see the description of the [StyleCollection](../../com.aspose.words/stylecollection) class.

**Returns:**
[StyleCollection](../../com.aspose.words/stylecollection) - A collection of styles defined in the document.
### getText() {#getText}
```
public String getText()
```


Gets the text of this node and of all its children.

The returned string includes all control and special characters as described in [ControlChar](../../com.aspose.words/controlchar).

**Returns:**
java.lang.String
### getWarningCallback() {#getWarningCallback}
```
public IWarningCallback getWarningCallback()
```


Called during various document processing procedures when an issue is detected that might result in data or formatting fidelity loss. Document may generate warnings at any stage of its existence, so it's important to setup warning callback as early as possible to avoid the warnings loss. E.g. such properties as [Document.getPageCount()](../../com.aspose.words/document\#getPageCount) actually build the document layout which is used later for rendering, and the layout warnings may be lost if warning callback is specified just for the rendering calls later.

**Returns:**
[IWarningCallback](../../com.aspose.words/iwarningcallback) - The corresponding [IWarningCallback](../../com.aspose.words/iwarningcallback) value.
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
### importNode(Node srcNode, boolean isImportChildren) {#importNode-com.aspose.words.Node-boolean}
```
public Node importNode(Node srcNode, boolean isImportChildren)
```


Imports a node from another document to the current document.

Imports a node from another document to the current document.

This method uses the [ImportFormatMode.USE\_DESTINATION\_STYLES](../../com.aspose.words/importformatmode\#USE-DESTINATION-STYLES) option to resolve formatting.

Importing a node creates a copy of the source node belonging to the importing document. The returned node has no parent. The source node is not altered or removed from the original document.

Before a node from another document can be inserted into this document, it must be imported. During import, document-specific properties such as references to styles and lists are translated from the original to the importing document. After the node was imported, it can be inserted into the appropriate place in the document using [CompositeNode.insertBefore(com.aspose.words.Node, com.aspose.words.Node)](../../com.aspose.words/compositenode\#insertBefore-com.aspose.words.Node--com.aspose.words.Node) or [CompositeNode.insertAfter(com.aspose.words.Node, com.aspose.words.Node)](../../com.aspose.words/compositenode\#insertAfter-com.aspose.words.Node--com.aspose.words.Node).

If the source node already belongs to the destination document, then simply a deep clone of the source node is created.

**Parameters:**
| Parameter | Type | Description |
| --- | --- | --- |
| srcNode | [Node](../../com.aspose.words/node) | The node being imported. |
| isImportChildren | boolean | \{ true  to import all child nodes recursively; otherwise,  false . |

**Returns:**
[Node](../../com.aspose.words/node) - The cloned node that belongs to the current document.
### importNode(Node srcNode, boolean isImportChildren, int importFormatMode) {#importNode-com.aspose.words.Node-boolean-int}
```
public Node importNode(Node srcNode, boolean isImportChildren, int importFormatMode)
```




**Parameters:**
| Parameter | Type | Description |
| --- | --- | --- |
| srcNode | [Node](../../com.aspose.words/node) |  |
| isImportChildren | boolean |  |
| importFormatMode | int |  |

**Returns:**
[Node](../../com.aspose.words/node)
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
### setBackgroundShape(Shape value) {#setBackgroundShape-com.aspose.words.Shape}
```
public void setBackgroundShape(Shape value)
```


Sets the background shape of the document. Can be  null .

Microsoft Word allows only a shape that has its [ShapeBase.getShapeType()](../../com.aspose.words/shapebase\#getShapeType) property equal to [ShapeType.RECTANGLE](../../com.aspose.words/shapetype\#RECTANGLE) to be used as a background shape for a document.

Microsoft Word supports only the fill properties of a background shape. All other properties are ignored.

Setting this property to a non-null value will also set the [ViewOptions.getDisplayBackgroundShape()](../../com.aspose.words/viewoptions\#getDisplayBackgroundShape) / [ViewOptions.setDisplayBackgroundShape(boolean)](../../com.aspose.words/viewoptions\#setDisplayBackgroundShape-boolean) to  true .

**Parameters:**
| Parameter | Type | Description |
| --- | --- | --- |
| value | [Shape](../../com.aspose.words/shape) | The background shape of the document. |

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

### setNodeChangingCallback(INodeChangingCallback value) {#setNodeChangingCallback-com.aspose.words.INodeChangingCallback}
```
public void setNodeChangingCallback(INodeChangingCallback value)
```


Called when a node is inserted or removed in the document.

**Parameters:**
| Parameter | Type | Description |
| --- | --- | --- |
| value | [INodeChangingCallback](../../com.aspose.words/inodechangingcallback) | The corresponding [INodeChangingCallback](../../com.aspose.words/inodechangingcallback) value. |

### setPageColor(Color value) {#setPageColor-java.awt.Color}
```
public void setPageColor(Color value)
```


Sets the page color of the document. This property is a simpler version of [getBackgroundShape()](../../com.aspose.words/documentbase\#getBackgroundShape) / [setBackgroundShape(com.aspose.words.Shape)](../../com.aspose.words/documentbase\#setBackgroundShape-com.aspose.words.Shape).

This property provides a simple way to specify a solid page color for the document. Setting this property creates and sets an appropriate [getBackgroundShape()](../../com.aspose.words/documentbase\#getBackgroundShape) / [setBackgroundShape(com.aspose.words.Shape)](../../com.aspose.words/documentbase\#setBackgroundShape-com.aspose.words.Shape).

If the page color is not set (e.g. there is no background shape in the document) returns a zero color.

**Parameters:**
| Parameter | Type | Description |
| --- | --- | --- |
| value | java.awt.Color | The page color of the document. |

### setResourceLoadingCallback(IResourceLoadingCallback value) {#setResourceLoadingCallback-com.aspose.words.IResourceLoadingCallback}
```
public void setResourceLoadingCallback(IResourceLoadingCallback value)
```


Allows to control how external resources are loaded.

**Parameters:**
| Parameter | Type | Description |
| --- | --- | --- |
| value | [IResourceLoadingCallback](../../com.aspose.words/iresourceloadingcallback) | The corresponding [IResourceLoadingCallback](../../com.aspose.words/iresourceloadingcallback) value. |

### setWarningCallback(IWarningCallback value) {#setWarningCallback-com.aspose.words.IWarningCallback}
```
public void setWarningCallback(IWarningCallback value)
```


Called during various document processing procedures when an issue is detected that might result in data or formatting fidelity loss. Document may generate warnings at any stage of its existence, so it's important to setup warning callback as early as possible to avoid the warnings loss. E.g. such properties as [Document.getPageCount()](../../com.aspose.words/document\#getPageCount) actually build the document layout which is used later for rendering, and the layout warnings may be lost if warning callback is specified just for the rendering calls later.

**Parameters:**
| Parameter | Type | Description |
| --- | --- | --- |
| value | [IWarningCallback](../../com.aspose.words/iwarningcallback) | The corresponding [IWarningCallback](../../com.aspose.words/iwarningcallback) value. |

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

