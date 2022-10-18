---
title: CompositeNode
second_title: Aspose.Words for Java API Reference
description: Base class for nodes that can contain other nodes.
type: docs
weight: 87
url: /java/com.aspose.words/compositenode/
---

**Inheritance:**
java.lang.Object, [com.aspose.words.Node](../../com.aspose.words/node)

**All Implemented Interfaces:**
java.lang.Iterable
```
public abstract class CompositeNode extends Node implements Iterable
```

Base class for nodes that can contain other nodes.

To learn more, visit the **Aspose.Words Document Object Model (DOM)** documentation article.

A document is represented as a tree of nodes, similar to DOM or XmlDocument.

For more info see the Composite design pattern.

The [CompositeNode](../../com.aspose.words/compositenode) class:

 *  Provides access to the child nodes.
 *  Implements Composite operations such as insert and remove children.
 *  Provides methods for XPath navigation.
## Methods

| Method | Description |
| --- | --- |
| [isComposite()](#isComposite--) | Returns true as this node can have child nodes. |
| [hasChildNodes()](#hasChildNodes--) | Returns true if this node has any child nodes. |
| [getChildNodes()](#getChildNodes--) | Gets all immediate child nodes of this node. |
| [getFirstChild()](#getFirstChild--) | Gets the first child of the node. |
| [getLastChild()](#getLastChild--) | Gets the last child of the node. |
| [getCount()](#getCount--) | Gets the number of immediate children of this node. |
| [getText()](#getText--) | Gets the text of this node and of all its children. |
| [getChildNodes(int nodeType, boolean isDeep)](#getChildNodes-int-boolean-) |  |
| [getChild(int nodeType, int index, boolean isDeep)](#getChild-int-int-boolean-) |  |
| [selectNodes(String xpath)](#selectNodes-java.lang.String-) | Selects a list of nodes matching the XPath expression. |
| [selectSingleNode(String xpath)](#selectSingleNode-java.lang.String-) | Selects the first Node that matches the XPath expression. |
| [iterator()](#iterator--) | Provides support for the for each style iteration over the child nodes of this node. |
| [appendChild(Node newChild)](#appendChild-com.aspose.words.Node-) | Adds the specified node to the end of the list of child nodes for this node. |
| [prependChild(Node newChild)](#prependChild-com.aspose.words.Node-) | Adds the specified node to the beginning of the list of child nodes for this node. |
| [insertAfter(Node newChild, Node refChild)](#insertAfter-com.aspose.words.Node-com.aspose.words.Node-) | Inserts the specified node immediately after the specified reference node. |
| [insertBefore(Node newChild, Node refChild)](#insertBefore-com.aspose.words.Node-com.aspose.words.Node-) | Inserts the specified node immediately before the specified reference node. |
| [removeChild(Node oldChild)](#removeChild-com.aspose.words.Node-) | Removes the specified child node. |
| [removeAllChildren()](#removeAllChildren--) | Removes all the child nodes of the current node. |
| [removeSmartTags()](#removeSmartTags--) | Removes all [SmartTag](../../com.aspose.words/smarttag) descendant nodes of the current node. |
| [indexOf(Node child)](#indexOf-com.aspose.words.Node-) | Returns the index of the specified child node in the child node array. |
| [getNextMatchingNode(Node curNode)](#getNextMatchingNode-com.aspose.words.Node-) |  |
| [getCurrentNode()](#getCurrentNode--) |  |
| [getContainer()](#getContainer--) |  |
### isComposite() {#isComposite--}
```
public boolean isComposite()
```


Returns true as this node can have child nodes.

**Returns:**
boolean - True as this node can have child nodes.
### hasChildNodes() {#hasChildNodes--}
```
public boolean hasChildNodes()
```


Returns true if this node has any child nodes.

**Returns:**
boolean - True if this node has any child nodes.
### getChildNodes() {#getChildNodes--}
```
public NodeCollection getChildNodes()
```


Gets all immediate child nodes of this node.

Note, [getChildNodes()](../../com.aspose.words/compositenode\#getChildNodes--) is equivalent to calling  GetChildNodes(NodeType.Any, false)  and creates and returns a new collection every time it is accessed.

If there are no child nodes, this property returns an empty collection.

**Returns:**
[NodeCollection](../../com.aspose.words/nodecollection) - All immediate child nodes of this node.
### getFirstChild() {#getFirstChild--}
```
public Node getFirstChild()
```


Gets the first child of the node. If there is no first child node, a null is returned.

**Returns:**
[Node](../../com.aspose.words/node) - The first child of the node.
### getLastChild() {#getLastChild--}
```
public Node getLastChild()
```


Gets the last child of the node. If there is no last child node, a null is returned.

**Returns:**
[Node](../../com.aspose.words/node) - The last child of the node.
### getCount() {#getCount--}
```
public int getCount()
```


Gets the number of immediate children of this node.

**Returns:**
int - The number of immediate children of this node.
### getText() {#getText--}
```
public String getText()
```


Gets the text of this node and of all its children.

The returned string includes all control and special characters as described in [ControlChar](../../com.aspose.words/controlchar).

**Returns:**
java.lang.String
### getChildNodes(int nodeType, boolean isDeep) {#getChildNodes-int-boolean-}
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
### getChild(int nodeType, int index, boolean isDeep) {#getChild-int-int-boolean-}
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
### selectNodes(String xpath) {#selectNodes-java.lang.String-}
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
### selectSingleNode(String xpath) {#selectSingleNode-java.lang.String-}
```
public Node selectSingleNode(String xpath)
```


Selects the first Node that matches the XPath expression.

Only expressions with element names are supported at the moment. Expressions that use attribute names are not supported.

**Parameters:**
| Parameter | Type | Description |
| --- | --- | --- |
| xpath | java.lang.String | The XPath expression. |

**Returns:**
[Node](../../com.aspose.words/node) - The first Node that matches the XPath query or null if no matching node is found.
### iterator() {#iterator--}
```
public Iterator iterator()
```


Provides support for the for each style iteration over the child nodes of this node.

**Returns:**
java.util.Iterator
### appendChild(Node newChild) {#appendChild-com.aspose.words.Node-}
```
public Node appendChild(Node newChild)
```


Adds the specified node to the end of the list of child nodes for this node.

If the newChild is already in the tree, it is first removed.

If the node being inserted was created from another document, you should use **M:Aspose.Words.DocumentBase.ImportNode(Aspose.Words.Node,System.Boolean,Aspose.Words.ImportFormatMode)** to import the node to the current document. The imported node can then be inserted into the current document.

**Parameters:**
| Parameter | Type | Description |
| --- | --- | --- |
| newChild | [Node](../../com.aspose.words/node) | The node to add. |

**Returns:**
[Node](../../com.aspose.words/node) - The node added.
### prependChild(Node newChild) {#prependChild-com.aspose.words.Node-}
```
public Node prependChild(Node newChild)
```


Adds the specified node to the beginning of the list of child nodes for this node.

If the newChild is already in the tree, it is first removed.

If the node being inserted was created from another document, you should use **M:Aspose.Words.DocumentBase.ImportNode(Aspose.Words.Node,System.Boolean,Aspose.Words.ImportFormatMode)** to import the node to the current document. The imported node can then be inserted into the current document.

**Parameters:**
| Parameter | Type | Description |
| --- | --- | --- |
| newChild | [Node](../../com.aspose.words/node) | The node to add. |

**Returns:**
[Node](../../com.aspose.words/node) - The node added.
### insertAfter(Node newChild, Node refChild) {#insertAfter-com.aspose.words.Node-com.aspose.words.Node-}
```
public Node insertAfter(Node newChild, Node refChild)
```


Inserts the specified node immediately after the specified reference node.

If refChild is null, inserts newChild at the beginning of the list of child nodes.

If the newChild is already in the tree, it is first removed.

If the node being inserted was created from another document, you should use **M:Aspose.Words.DocumentBase.ImportNode(Aspose.Words.Node,System.Boolean,Aspose.Words.ImportFormatMode)** to import the node to the current document. The imported node can then be inserted into the current document.

**Parameters:**
| Parameter | Type | Description |
| --- | --- | --- |
| newChild | [Node](../../com.aspose.words/node) | The Node to insert. |
| refChild | [Node](../../com.aspose.words/node) | The Node that is the reference node. The newNode is placed after the refNode. |

**Returns:**
[Node](../../com.aspose.words/node) - The inserted node.
### insertBefore(Node newChild, Node refChild) {#insertBefore-com.aspose.words.Node-com.aspose.words.Node-}
```
public Node insertBefore(Node newChild, Node refChild)
```


Inserts the specified node immediately before the specified reference node.

If refChild is null, inserts newChild at the end of the list of child nodes.

If the newChild is already in the tree, it is first removed.

If the node being inserted was created from another document, you should use **M:Aspose.Words.DocumentBase.ImportNode(Aspose.Words.Node,System.Boolean,Aspose.Words.ImportFormatMode)** to import the node to the current document. The imported node can then be inserted into the current document.

**Parameters:**
| Parameter | Type | Description |
| --- | --- | --- |
| newChild | [Node](../../com.aspose.words/node) | The Node to insert. |
| refChild | [Node](../../com.aspose.words/node) | The Node that is the reference node. The newChild is placed before this node. |

**Returns:**
[Node](../../com.aspose.words/node) - The inserted node.
### removeChild(Node oldChild) {#removeChild-com.aspose.words.Node-}
```
public Node removeChild(Node oldChild)
```


Removes the specified child node.

The parent of oldChild is set to null after the node is removed.

**Parameters:**
| Parameter | Type | Description |
| --- | --- | --- |
| oldChild | [Node](../../com.aspose.words/node) | The node to remove. |

**Returns:**
[Node](../../com.aspose.words/node) - The removed node.
### removeAllChildren() {#removeAllChildren--}
```
public void removeAllChildren()
```


Removes all the child nodes of the current node.

### removeSmartTags() {#removeSmartTags--}
```
public void removeSmartTags()
```


Removes all [SmartTag](../../com.aspose.words/smarttag) descendant nodes of the current node. This method does not remove the content of the smart tags.

### indexOf(Node child) {#indexOf-com.aspose.words.Node-}
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
### getNextMatchingNode(Node curNode) {#getNextMatchingNode-com.aspose.words.Node-}
```
public Node getNextMatchingNode(Node curNode)
```




**Parameters:**
| Parameter | Type | Description |
| --- | --- | --- |
| curNode | [Node](../../com.aspose.words/node) |  |

**Returns:**
[Node](../../com.aspose.words/node)
### getCurrentNode() {#getCurrentNode--}
```
public Node getCurrentNode()
```




**Returns:**
[Node](../../com.aspose.words/node)
### getContainer() {#getContainer--}
```
public CompositeNode getContainer()
```




**Returns:**
[CompositeNode](../../com.aspose.words/compositenode)
