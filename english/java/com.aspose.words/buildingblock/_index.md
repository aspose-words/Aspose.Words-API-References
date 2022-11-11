---
title: BuildingBlock
second_title: Aspose.Words for Java API Reference
description: Represents a glossary document entry such as a Building Block AutoText or an AutoCorrect entry.
type: docs
weight: 41
url: /java/com.aspose.words/buildingblock/
---

**Inheritance:**
java.lang.Object, [com.aspose.words.Node](../../com.aspose.words/node), [com.aspose.words.CompositeNode](../../com.aspose.words/compositenode)
```
public class BuildingBlock extends CompositeNode
```

Represents a glossary document entry such as a Building Block, AutoText or an AutoCorrect entry.

To learn more, visit the **Aspose.Words Document Object Model (DOM)** documentation article.

[BuildingBlock](../../com.aspose.words/buildingblock) can contain only [Section](../../com.aspose.words/section) nodes.

[BuildingBlock](../../com.aspose.words/buildingblock) can only be a child of [GlossaryDocument](../../com.aspose.words/glossarydocument).

You can create new building blocks and insert them into a glossary document. You can modify or delete existing building blocks. You can copy or move building blocks between documents. You can insert content of a building block into a document.

Corresponds to the **docPart**, **docPartPr** and **docPartBody** elements in OOXML.
## Constructors

| Constructor | Description |
| --- | --- |
| [BuildingBlock(GlossaryDocument glossaryDoc)](#BuildingBlock-com.aspose.words.GlossaryDocument-) | Initializes a new instance of this class. |
## Methods

| Method | Description |
| --- | --- |
| [accept(DocumentVisitor visitor)](#accept-com.aspose.words.DocumentVisitor-) | Accepts a visitor. |
| [appendChild(Node newChild)](#appendChild-com.aspose.words.Node-) | Adds the specified node to the end of the list of child nodes for this node. |
| [dd()](#dd--) |  |
| [deepClone(boolean isCloneChildren)](#deepClone-boolean-) | Creates a duplicate of the node. |
| [equals(Object arg0)](#equals-java.lang.Object-) |  |
| [getAncestor(int ancestorType)](#getAncestor-int-) |  |
| [getAncestor(Class ancestorType)](#getAncestor-java.lang.Class-) | Gets the first ancestor of the specified object type. |
| [getBehavior()](#getBehavior--) | Specifies the behavior that shall be applied when the contents of the building block is inserted into the main document. |
| [getCategory()](#getCategory--) | Specifies the second-level categorization for the building block. |
| [getChild(int nodeType, int index, boolean isDeep)](#getChild-int-int-boolean-) |  |
| [getChildNodes()](#getChildNodes--) | Gets all immediate child nodes of this node. |
| [getChildNodes(int nodeType, boolean isDeep)](#getChildNodes-int-boolean-) |  |
| [getClass()](#getClass--) |  |
| [getContainer()](#getContainer--) |  |
| [getCount()](#getCount--) | Gets the number of immediate children of this node. |
| [getCurrentNode()](#getCurrentNode--) |  |
| [getCustomNodeId()](#getCustomNodeId--) | Specifies custom node identifier. |
| [getDescription()](#getDescription--) | Gets the description associated with this building block. |
| [getDocument()](#getDocument--) | Gets the document to which this node belongs. |
| [getFirstChild()](#getFirstChild--) | Gets the first child of the node. |
| [getFirstSection()](#getFirstSection--) | Gets the first section in the building block. |
| [getGallery()](#getGallery--) | Specifies the first-level categorization for the building block for the purposes of classification or user interface sorting. |
| [getGuid()](#getGuid--) | Gets an identifier (a 128-bit GUID) that uniquely identifies this building block. |
| [getLastChild()](#getLastChild--) | Gets the last child of the node. |
| [getLastSection()](#getLastSection--) | Gets the last section in the building block. |
| [getName()](#getName--) | Gets the name of this building block. |
| [getNextMatchingNode(Node curNode)](#getNextMatchingNode-com.aspose.words.Node-) |  |
| [getNextSibling()](#getNextSibling--) | Gets the node immediately following this node. |
| [getNodeType()](#getNodeType--) | Returns the [NodeType.BUILDING\_BLOCK](../../com.aspose.words/nodetype\#BUILDING-BLOCK) value. |
| [getParentNode()](#getParentNode--) | Gets the immediate parent of this node. |
| [getPreviousSibling()](#getPreviousSibling--) | Gets the node immediately preceding this node. |
| [getRange()](#getRange--) | Returns a **Range** object that represents the portion of a document that is contained in this node. |
| [getSections()](#getSections--) | Returns a collection that represents all sections in the building block. |
| [getText()](#getText--) | Gets the text of this node and of all its children. |
| [getType()](#getType--) | Specifies the building block type. |
| [hasChildNodes()](#hasChildNodes--) | Returns true if this node has any child nodes. |
| [hashCode()](#hashCode--) |  |
| [indexOf(Node child)](#indexOf-com.aspose.words.Node-) | Returns the index of the specified child node in the child node array. |
| [insertAfter(Node newChild, Node refChild)](#insertAfter-com.aspose.words.Node-com.aspose.words.Node-) | Inserts the specified node immediately after the specified reference node. |
| [insertBefore(Node newChild, Node refChild)](#insertBefore-com.aspose.words.Node-com.aspose.words.Node-) | Inserts the specified node immediately before the specified reference node. |
| [isComposite()](#isComposite--) | Returns true as this node can have child nodes. |
| [iterator()](#iterator--) | Provides support for the for each style iteration over the child nodes of this node. |
| [nextPreOrder(Node rootNode)](#nextPreOrder-com.aspose.words.Node-) | Gets next node according to the pre-order tree traversal algorithm. |
| [nodeTypeToString(int nodeType)](#nodeTypeToString-int-) |  |
| [notify()](#notify--) |  |
| [notifyAll()](#notifyAll--) |  |
| [prependChild(Node newChild)](#prependChild-com.aspose.words.Node-) | Adds the specified node to the beginning of the list of child nodes for this node. |
| [previousPreOrder(Node rootNode)](#previousPreOrder-com.aspose.words.Node-) | Gets the previous node according to the pre-order tree traversal algorithm. |
| [remove()](#remove--) | Removes itself from the parent. |
| [removeAllChildren()](#removeAllChildren--) | Removes all the child nodes of the current node. |
| [removeChild(Node oldChild)](#removeChild-com.aspose.words.Node-) | Removes the specified child node. |
| [removeSmartTags()](#removeSmartTags--) | Removes all [SmartTag](../../com.aspose.words/smarttag) descendant nodes of the current node. |
| [selectNodes(String xpath)](#selectNodes-java.lang.String-) | Selects a list of nodes matching the XPath expression. |
| [selectSingleNode(String xpath)](#selectSingleNode-java.lang.String-) | Selects the first Node that matches the XPath expression. |
| [setBehavior(int value)](#setBehavior-int-) | Specifies the behavior that shall be applied when the contents of the building block is inserted into the main document. |
| [setCategory(String value)](#setCategory-java.lang.String-) | Specifies the second-level categorization for the building block. |
| [setCustomNodeId(int value)](#setCustomNodeId-int-) | Specifies custom node identifier. |
| [setDescription(String value)](#setDescription-java.lang.String-) | Sets the description associated with this building block. |
| [setGallery(int value)](#setGallery-int-) | Specifies the first-level categorization for the building block for the purposes of classification or user interface sorting. |
| [setGuid(UUID value)](#setGuid-java.util.UUID-) | Sets an identifier (a 128-bit GUID) that uniquely identifies this building block. |
| [setName(String value)](#setName-java.lang.String-) | Sets the name of this building block. |
| [setType(int value)](#setType-int-) | Specifies the building block type. |
| [toString()](#toString--) |  |
| [toString(SaveOptions saveOptions)](#toString-com.aspose.words.SaveOptions-) | Exports the content of the node into a string using the specified save options. |
| [toString(int saveFormat)](#toString-int-) |  |
| [wait()](#wait--) |  |
| [wait(long arg0)](#wait-long-) |  |
| [wait(long arg0, int arg1)](#wait-long-int-) |  |
### BuildingBlock(GlossaryDocument glossaryDoc) {#BuildingBlock-com.aspose.words.GlossaryDocument-}
```
public BuildingBlock(GlossaryDocument glossaryDoc)
```


Initializes a new instance of this class.

When [BuildingBlock](../../com.aspose.words/buildingblock) is created, it belongs to the specified glossary document, but is not yet part of the glossary document and [Node.getParentNode()](../../com.aspose.words/node\#getParentNode--) is  null .

To append [BuildingBlock](../../com.aspose.words/buildingblock) to a [GlossaryDocument](../../com.aspose.words/glossarydocument) use [CompositeNode.appendChild(com.aspose.words.Node)](../../com.aspose.words/compositenode\#appendChild-com.aspose.words.Node-).

**Parameters:**
| Parameter | Type | Description |
| --- | --- | --- |
| glossaryDoc | [GlossaryDocument](../../com.aspose.words/glossarydocument) | The owner document. |

### accept(DocumentVisitor visitor) {#accept-com.aspose.words.DocumentVisitor-}
```
public boolean accept(DocumentVisitor visitor)
```


Accepts a visitor.

Enumerates over this node and all of its children. Each node calls a corresponding method on DocumentVisitor.

For more info see the Visitor design pattern.

**Parameters:**
| Parameter | Type | Description |
| --- | --- | --- |
| visitor | [DocumentVisitor](../../com.aspose.words/documentvisitor) | The visitor that will visit the nodes. |

**Returns:**
boolean - True if all nodes were visited; false if DocumentVisitor stopped the operation before visiting all nodes.

Calls [DocumentVisitor.visitBuildingBlockStart(com.aspose.words.BuildingBlock)](../../com.aspose.words/documentvisitor\#visitBuildingBlockStart-com.aspose.words.BuildingBlock-), then calls [Node.accept(com.aspose.words.DocumentVisitor)](../../com.aspose.words/node\#accept-com.aspose.words.DocumentVisitor-) for all child nodes of this building block, then calls [DocumentVisitor.visitBuildingBlockEnd(com.aspose.words.BuildingBlock)](../../com.aspose.words/documentvisitor\#visitBuildingBlockEnd-com.aspose.words.BuildingBlock-).

Note: A building block node and its children are not visited when you execute a Visitor over a [Document](../../com.aspose.words/document). If you want to execute a Visitor over a building block, you need to execute the visitor over [GlossaryDocument](../../com.aspose.words/glossarydocument) or call [accept(com.aspose.words.DocumentVisitor)](../../com.aspose.words/buildingblock\#accept-com.aspose.words.DocumentVisitor-).
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
### dd() {#dd--}
```
public void dd()
```




### deepClone(boolean isCloneChildren) {#deepClone-boolean-}
```
public Node deepClone(boolean isCloneChildren)
```


Creates a duplicate of the node.

This method serves as a copy constructor for nodes. The cloned node has no parent, but belongs to the same document as the original node.

This method always performs a deep copy of the node. The *isCloneChildren* parameter specifies whether to perform copy all child nodes as well.

**Parameters:**
| Parameter | Type | Description |
| --- | --- | --- |
| isCloneChildren | boolean | True to recursively clone the subtree under the specified node; false to clone only the node itself. |

**Returns:**
[Node](../../com.aspose.words/node) - The cloned node.
### equals(Object arg0) {#equals-java.lang.Object-}
```
public boolean equals(Object arg0)
```




**Parameters:**
| Parameter | Type | Description |
| --- | --- | --- |
| arg0 | java.lang.Object |  |

**Returns:**
boolean
### getAncestor(int ancestorType) {#getAncestor-int-}
```
public CompositeNode getAncestor(int ancestorType)
```




**Parameters:**
| Parameter | Type | Description |
| --- | --- | --- |
| ancestorType | int |  |

**Returns:**
[CompositeNode](../../com.aspose.words/compositenode)
### getAncestor(Class ancestorType) {#getAncestor-java.lang.Class-}
```
public CompositeNode getAncestor(Class ancestorType)
```


Gets the first ancestor of the specified object type.

**Parameters:**
| Parameter | Type | Description |
| --- | --- | --- |
| ancestorType | java.lang.Class | The object type of the ancestor to retrieve. |

**Returns:**
[CompositeNode](../../com.aspose.words/compositenode) - The ancestor of the specified type or null if no ancestor of this type was found.

The ancestor type matches if it is equal to ancestorType or derived from ancestorType.
### getBehavior() {#getBehavior--}
```
public int getBehavior()
```


Specifies the behavior that shall be applied when the contents of the building block is inserted into the main document.

**Returns:**
int - The corresponding  int  value. The returned value is one of [BuildingBlockBehavior](../../com.aspose.words/buildingblockbehavior) constants.
### getCategory() {#getCategory--}
```
public String getCategory()
```


Specifies the second-level categorization for the building block.

Building blocks in Microsoft Word user interface are arranged into Galleries. Each [getGallery()](../../com.aspose.words/buildingblock\#getGallery--) / [setGallery(int)](../../com.aspose.words/buildingblock\#setGallery-int-) can have multiple Categories. Each block within a [getCategory()](../../com.aspose.words/buildingblock\#getCategory--) / [setCategory(java.lang.String)](../../com.aspose.words/buildingblock\#setCategory-java.lang.String-) has a [getName()](../../com.aspose.words/buildingblock\#getName--) / [setName(java.lang.String)](../../com.aspose.words/buildingblock\#setName-java.lang.String-).

Cannot be  null  and cannot be an empty string.

Corresponds to the **docPartPr.category.name** element in OOXML.

**Returns:**
java.lang.String - The corresponding java.lang.String value.
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
### getChildNodes() {#getChildNodes--}
```
public NodeCollection getChildNodes()
```


Gets all immediate child nodes of this node.

Note, [getChildNodes()](../../com.aspose.words/compositenode\#getChildNodes--) is equivalent to calling  GetChildNodes(NodeType.Any, false)  and creates and returns a new collection every time it is accessed.

If there are no child nodes, this property returns an empty collection.

**Returns:**
[NodeCollection](../../com.aspose.words/nodecollection) - All immediate child nodes of this node.
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
### getClass() {#getClass--}
```
public final native Class<?> getClass()
```




**Returns:**
java.lang.Class<?>
### getContainer() {#getContainer--}
```
public CompositeNode getContainer()
```




**Returns:**
[CompositeNode](../../com.aspose.words/compositenode)
### getCount() {#getCount--}
```
public int getCount()
```


Gets the number of immediate children of this node.

**Returns:**
int - The number of immediate children of this node.
### getCurrentNode() {#getCurrentNode--}
```
public Node getCurrentNode()
```




**Returns:**
[Node](../../com.aspose.words/node)
### getCustomNodeId() {#getCustomNodeId--}
```
public int getCustomNodeId()
```


Specifies custom node identifier.

Default is zero.

This identifier can be set and used arbitrarily. For example, as a key to get external data.

Important note, specified value is not saved to an output file and exists only during the node lifetime.

**Returns:**
int - The corresponding  int  value.
### getDescription() {#getDescription--}
```
public String getDescription()
```


Gets the description associated with this building block.

The description may contain any string content, usually additional information.

Cannot be  null , but can be an empty string.

Corresponds to the **docPartPr.description** element in OOXML.

**Returns:**
java.lang.String - The description associated with this building block.
### getDocument() {#getDocument--}
```
public DocumentBase getDocument()
```


Gets the document to which this node belongs.

The node always belongs to a document even if it has just been created and not yet added to the tree, or if it has been removed from the tree.

**Returns:**
[DocumentBase](../../com.aspose.words/documentbase) - The document to which this node belongs.
### getFirstChild() {#getFirstChild--}
```
public Node getFirstChild()
```


Gets the first child of the node. If there is no first child node, a null is returned.

**Returns:**
[Node](../../com.aspose.words/node) - The first child of the node.
### getFirstSection() {#getFirstSection--}
```
public Section getFirstSection()
```


Gets the first section in the building block. Returns  null  if there are no sections.

**Returns:**
[Section](../../com.aspose.words/section) - The first section in the building block.
### getGallery() {#getGallery--}
```
public int getGallery()
```


Specifies the first-level categorization for the building block for the purposes of classification or user interface sorting.

Building blocks in Microsoft Word user interface are arranged into Galleries. Each [getGallery()](../../com.aspose.words/buildingblock\#getGallery--) / [setGallery(int)](../../com.aspose.words/buildingblock\#setGallery-int-) can have multiple Categories. Each block within a [getCategory()](../../com.aspose.words/buildingblock\#getCategory--) / [setCategory(java.lang.String)](../../com.aspose.words/buildingblock\#setCategory-java.lang.String-) has a [getName()](../../com.aspose.words/buildingblock\#getName--) / [setName(java.lang.String)](../../com.aspose.words/buildingblock\#setName-java.lang.String-).

Corresponds to the **docPartPr.category.gallery** element in OOXML.

**Returns:**
int - The corresponding  int  value. The returned value is one of [BuildingBlockGallery](../../com.aspose.words/buildingblockgallery) constants.
### getGuid() {#getGuid--}
```
public UUID getGuid()
```


Gets an identifier (a 128-bit GUID) that uniquely identifies this building block.

Can be used by an application to uniquely reference a building block regardless of different naming due to localization.

Corresponds to the **docPartPr.guid** element in OOXML.

**Returns:**
java.util.UUID - An identifier (a 128-bit GUID) that uniquely identifies this building block.
### getLastChild() {#getLastChild--}
```
public Node getLastChild()
```


Gets the last child of the node. If there is no last child node, a null is returned.

**Returns:**
[Node](../../com.aspose.words/node) - The last child of the node.
### getLastSection() {#getLastSection--}
```
public Section getLastSection()
```


Gets the last section in the building block. Returns  null  if there are no sections.

**Returns:**
[Section](../../com.aspose.words/section) - The last section in the building block.
### getName() {#getName--}
```
public String getName()
```


Gets the name of this building block.

The name may contain any string content, usually a friendly identifier. Multiple building blocks can have the same name.

Cannot be  null  and cannot be an empty string.

Corresponds to the **docPartPr.name** element in OOXML.

**Returns:**
java.lang.String - The name of this building block.
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
### getNextSibling() {#getNextSibling--}
```
public Node getNextSibling()
```


Gets the node immediately following this node. If there is no next node, a null is returned.

**Returns:**
[Node](../../com.aspose.words/node) - The node immediately following this node.
### getNodeType() {#getNodeType--}
```
public int getNodeType()
```


Returns the [NodeType.BUILDING\_BLOCK](../../com.aspose.words/nodetype\#BUILDING-BLOCK) value.

**Returns:**
int - The [NodeType.BUILDING\_BLOCK](../../com.aspose.words/nodetype\#BUILDING-BLOCK) value. The returned value is one of [NodeType](../../com.aspose.words/nodetype) constants.
### getParentNode() {#getParentNode--}
```
public CompositeNode getParentNode()
```


Gets the immediate parent of this node.

If a node has just been created and not yet added to the tree, or if it has been removed from the tree, the parent is null.

**Returns:**
[CompositeNode](../../com.aspose.words/compositenode) - The immediate parent of this node.
### getPreviousSibling() {#getPreviousSibling--}
```
public Node getPreviousSibling()
```


Gets the node immediately preceding this node. If there is no preceding node, a null is returned.

**Returns:**
[Node](../../com.aspose.words/node) - The node immediately preceding this node.
### getRange() {#getRange--}
```
public Range getRange()
```


Returns a **Range** object that represents the portion of a document that is contained in this node.

**Returns:**
[Range](../../com.aspose.words/range) - A **Range** object that represents the portion of a document that is contained in this node.
### getSections() {#getSections--}
```
public SectionCollection getSections()
```


Returns a collection that represents all sections in the building block.

**Returns:**
[SectionCollection](../../com.aspose.words/sectioncollection) - A collection that represents all sections in the building block.
### getText() {#getText--}
```
public String getText()
```


Gets the text of this node and of all its children.

The returned string includes all control and special characters as described in [ControlChar](../../com.aspose.words/controlchar).

**Returns:**
java.lang.String
### getType() {#getType--}
```
public int getType()
```


Specifies the building block type.

The building block type can influence the visibility and behavior of the building block in Microsoft Word.

Corresponds to the **docPartPr.types** element in OOXML.

**Returns:**
int - The corresponding  int  value. The returned value is one of [BuildingBlockType](../../com.aspose.words/buildingblocktype) constants.
### hasChildNodes() {#hasChildNodes--}
```
public boolean hasChildNodes()
```


Returns true if this node has any child nodes.

**Returns:**
boolean - True if this node has any child nodes.
### hashCode() {#hashCode--}
```
public native int hashCode()
```




**Returns:**
int
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
### isComposite() {#isComposite--}
```
public boolean isComposite()
```


Returns true as this node can have child nodes.

**Returns:**
boolean - True as this node can have child nodes.
### iterator() {#iterator--}
```
public Iterator iterator()
```


Provides support for the for each style iteration over the child nodes of this node.

**Returns:**
java.util.Iterator
### nextPreOrder(Node rootNode) {#nextPreOrder-com.aspose.words.Node-}
```
public Node nextPreOrder(Node rootNode)
```


Gets next node according to the pre-order tree traversal algorithm.

**Parameters:**
| Parameter | Type | Description |
| --- | --- | --- |
| rootNode | [Node](../../com.aspose.words/node) | The top node (limit) of traversal. |

**Returns:**
[Node](../../com.aspose.words/node) - Next node in pre-order order. Null if reached the rootNode.
### nodeTypeToString(int nodeType) {#nodeTypeToString-int-}
```
public static String nodeTypeToString(int nodeType)
```




**Parameters:**
| Parameter | Type | Description |
| --- | --- | --- |
| nodeType | int |  |

**Returns:**
java.lang.String
### notify() {#notify--}
```
public final native void notify()
```




### notifyAll() {#notifyAll--}
```
public final native void notifyAll()
```




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
### previousPreOrder(Node rootNode) {#previousPreOrder-com.aspose.words.Node-}
```
public Node previousPreOrder(Node rootNode)
```


Gets the previous node according to the pre-order tree traversal algorithm.

**Parameters:**
| Parameter | Type | Description |
| --- | --- | --- |
| rootNode | [Node](../../com.aspose.words/node) | The top node (limit) of traversal. |

**Returns:**
[Node](../../com.aspose.words/node) - Previous node in pre-order order. Null if reached the rootNode.
### remove() {#remove--}
```
public void remove()
```


Removes itself from the parent.

### removeAllChildren() {#removeAllChildren--}
```
public void removeAllChildren()
```


Removes all the child nodes of the current node.

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
### removeSmartTags() {#removeSmartTags--}
```
public void removeSmartTags()
```


Removes all [SmartTag](../../com.aspose.words/smarttag) descendant nodes of the current node. This method does not remove the content of the smart tags.

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
### setBehavior(int value) {#setBehavior-int-}
```
public void setBehavior(int value)
```


Specifies the behavior that shall be applied when the contents of the building block is inserted into the main document.

**Parameters:**
| Parameter | Type | Description |
| --- | --- | --- |
| value | int | The corresponding  int  value. The value must be one of [BuildingBlockBehavior](../../com.aspose.words/buildingblockbehavior) constants. |

### setCategory(String value) {#setCategory-java.lang.String-}
```
public void setCategory(String value)
```


Specifies the second-level categorization for the building block.

Building blocks in Microsoft Word user interface are arranged into Galleries. Each [getGallery()](../../com.aspose.words/buildingblock\#getGallery--) / [setGallery(int)](../../com.aspose.words/buildingblock\#setGallery-int-) can have multiple Categories. Each block within a [getCategory()](../../com.aspose.words/buildingblock\#getCategory--) / [setCategory(java.lang.String)](../../com.aspose.words/buildingblock\#setCategory-java.lang.String-) has a [getName()](../../com.aspose.words/buildingblock\#getName--) / [setName(java.lang.String)](../../com.aspose.words/buildingblock\#setName-java.lang.String-).

Cannot be  null  and cannot be an empty string.

Corresponds to the **docPartPr.category.name** element in OOXML.

**Parameters:**
| Parameter | Type | Description |
| --- | --- | --- |
| value | java.lang.String | The corresponding java.lang.String value. |

### setCustomNodeId(int value) {#setCustomNodeId-int-}
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

### setDescription(String value) {#setDescription-java.lang.String-}
```
public void setDescription(String value)
```


Sets the description associated with this building block.

The description may contain any string content, usually additional information.

Cannot be  null , but can be an empty string.

Corresponds to the **docPartPr.description** element in OOXML.

**Parameters:**
| Parameter | Type | Description |
| --- | --- | --- |
| value | java.lang.String | The description associated with this building block. |

### setGallery(int value) {#setGallery-int-}
```
public void setGallery(int value)
```


Specifies the first-level categorization for the building block for the purposes of classification or user interface sorting.

Building blocks in Microsoft Word user interface are arranged into Galleries. Each [getGallery()](../../com.aspose.words/buildingblock\#getGallery--) / [setGallery(int)](../../com.aspose.words/buildingblock\#setGallery-int-) can have multiple Categories. Each block within a [getCategory()](../../com.aspose.words/buildingblock\#getCategory--) / [setCategory(java.lang.String)](../../com.aspose.words/buildingblock\#setCategory-java.lang.String-) has a [getName()](../../com.aspose.words/buildingblock\#getName--) / [setName(java.lang.String)](../../com.aspose.words/buildingblock\#setName-java.lang.String-).

Corresponds to the **docPartPr.category.gallery** element in OOXML.

**Parameters:**
| Parameter | Type | Description |
| --- | --- | --- |
| value | int | The corresponding  int  value. The value must be one of [BuildingBlockGallery](../../com.aspose.words/buildingblockgallery) constants. |

### setGuid(UUID value) {#setGuid-java.util.UUID-}
```
public void setGuid(UUID value)
```


Sets an identifier (a 128-bit GUID) that uniquely identifies this building block.

Can be used by an application to uniquely reference a building block regardless of different naming due to localization.

Corresponds to the **docPartPr.guid** element in OOXML.

**Parameters:**
| Parameter | Type | Description |
| --- | --- | --- |
| value | java.util.UUID | An identifier (a 128-bit GUID) that uniquely identifies this building block. |

### setName(String value) {#setName-java.lang.String-}
```
public void setName(String value)
```


Sets the name of this building block.

The name may contain any string content, usually a friendly identifier. Multiple building blocks can have the same name.

Cannot be  null  and cannot be an empty string.

Corresponds to the **docPartPr.name** element in OOXML.

**Parameters:**
| Parameter | Type | Description |
| --- | --- | --- |
| value | java.lang.String | The name of this building block. |

### setType(int value) {#setType-int-}
```
public void setType(int value)
```


Specifies the building block type.

The building block type can influence the visibility and behavior of the building block in Microsoft Word.

Corresponds to the **docPartPr.types** element in OOXML.

**Parameters:**
| Parameter | Type | Description |
| --- | --- | --- |
| value | int | The corresponding  int  value. The value must be one of [BuildingBlockType](../../com.aspose.words/buildingblocktype) constants. |

### toString() {#toString--}
```
public String toString()
```




**Returns:**
java.lang.String
### toString(SaveOptions saveOptions) {#toString-com.aspose.words.SaveOptions-}
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
### toString(int saveFormat) {#toString-int-}
```
public String toString(int saveFormat)
```




**Parameters:**
| Parameter | Type | Description |
| --- | --- | --- |
| saveFormat | int |  |

**Returns:**
java.lang.String
### wait() {#wait--}
```
public final void wait()
```




### wait(long arg0) {#wait-long-}
```
public final native void wait(long arg0)
```




**Parameters:**
| Parameter | Type | Description |
| --- | --- | --- |
| arg0 | long |  |

### wait(long arg0, int arg1) {#wait-long-int-}
```
public final void wait(long arg0, int arg1)
```




**Parameters:**
| Parameter | Type | Description |
| --- | --- | --- |
| arg0 | long |  |
| arg1 | int |  |

