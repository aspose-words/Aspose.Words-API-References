---
title: StructuredDocumentTagRangeStart
second_title: Aspose.Words for Java API Reference
description: Represents a start of ranged structured document tag which accepts multi-sections content.
type: docs
weight: 535
url: /java/com.aspose.words/structureddocumenttagrangestart/
---

**Inheritance:**
java.lang.Object, [com.aspose.words.Node](../../com.aspose.words/node)

**All Implemented Interfaces:**
[com.aspose.words.IStructuredDocumentTag](../../com.aspose.words/istructureddocumenttag), java.lang.Iterable
```
public class StructuredDocumentTagRangeStart extends Node implements IStructuredDocumentTag, Iterable
```

Represents a start of **ranged** structured document tag which accepts multi-sections content. See also [StructuredDocumentTagRangeEnd](../../com.aspose.words/structureddocumenttagrangeend).

To learn more, visit the **Structured Document Tags or Content Control** documentation article.

Can be immediate child of [Body](../../com.aspose.words/body) node **only**.
## Constructors

| Constructor | Description |
| --- | --- |
| [StructuredDocumentTagRangeStart(DocumentBase doc, int type)](#StructuredDocumentTagRangeStart-com.aspose.words.DocumentBase-int-) | Initializes a new instance of this class. |
## Methods

| Method | Description |
| --- | --- |
| [accept(DocumentVisitor visitor)](#accept-com.aspose.words.DocumentVisitor-) |  |
| [appendChild(Node newChild)](#appendChild-com.aspose.words.Node-) | Adds the specified node to the end of the stdContent range. |
| [dd()](#dd--) |  |
| [deepClone(boolean isCloneChildren)](#deepClone-boolean-) | Creates a duplicate of the node. |
| [equals(Object arg0)](#equals-java.lang.Object-) |  |
| [getAncestor(int ancestorType)](#getAncestor-int-) |  |
| [getAncestor(Class ancestorType)](#getAncestor-java.lang.Class-) | Gets the first ancestor of the specified object type. |
| [getChildNodes()](#getChildNodes--) | Gets all nodes between this range start node and the range end node. |
| [getChildNodes(int nodeType, boolean isDeep)](#getChildNodes-int-boolean-) |  |
| [getClass()](#getClass--) |  |
| [getColor()](#getColor--) | Gets the color of the structured document tag. |
| [getCustomNodeId()](#getCustomNodeId--) | Specifies custom node identifier. |
| [getDocument()](#getDocument--) | Gets the document to which this node belongs. |
| [getId()](#getId--) | Specifies a unique read-only persistent numerical Id for this structured document tag. |
| [getLastChild()](#getLastChild--) | Gets the last child in the stdContent range. |
| [getLevel()](#getLevel--) | Gets the level at which this structured document tag range start occurs in the document tree. |
| [getLockContentControl()](#getLockContentControl--) | When set to true, this property will prohibit a user from deleting this structured document tag. |
| [getLockContents()](#getLockContents--) | When set to true, this property will prohibit a user from editing the contents of this structured document tag. |
| [getNextSibling()](#getNextSibling--) | Gets the node immediately following this node. |
| [getNodeType()](#getNodeType--) |  |
| [getParentNode()](#getParentNode--) | Gets the immediate parent of this node. |
| [getPlaceholder()](#getPlaceholder--) | Gets the [BuildingBlock](../../com.aspose.words/buildingblock) containing placeholder text which should be displayed when this structured document tag run contents are empty, the associated mapped XML element is empty as specified via the [getXmlMapping()](../../com.aspose.words/structureddocumenttagrangestart\#getXmlMapping--) element or the [isShowingPlaceholderText()](../../com.aspose.words/structureddocumenttagrangestart\#isShowingPlaceholderText--) / [isShowingPlaceholderText(boolean)](../../com.aspose.words/structureddocumenttagrangestart\#isShowingPlaceholderText-boolean-) element is true. |
| [getPlaceholderName()](#getPlaceholderName--) | Gets or sets Name of the [BuildingBlock](../../com.aspose.words/buildingblock) containing placeholder text. |
| [getPreviousSibling()](#getPreviousSibling--) | Gets the node immediately preceding this node. |
| [getRange()](#getRange--) | Returns a **Range** object that represents the portion of a document that is contained in this node. |
| [getRangeEnd()](#getRangeEnd--) | Specifies end of range if the StructuredDocumentTag is a ranged structured document tag. |
| [getSdtType()](#getSdtType--) | Gets type of this structured document tag. |
| [getTag()](#getTag--) | Specifies a tag associated with the current structured document tag node. |
| [getText()](#getText--) | Gets the text of this node and of all its children. |
| [getTitle()](#getTitle--) | Specifies the friendly name associated with this structured document tag. |
| [getWordOpenXML()](#getWordOpenXML--) | Gets a string that represents the XML contained within the node in the [SaveFormat.FLAT\_OPC](../../com.aspose.words/saveformat\#FLAT-OPC) format. |
| [getXmlMapping()](#getXmlMapping--) | Gets an object that represents the mapping of this structured document tag range to XML data in a custom XML part of the current document. |
| [hashCode()](#hashCode--) |  |
| [isComposite()](#isComposite--) | Returns true if this node can contain other nodes. |
| [isRanged()](#isRanged--) |  |
| [isShowingPlaceholderText()](#isShowingPlaceholderText--) | Specifies whether the content of this structured document tag shall be interpreted to contain placeholder text (as opposed to regular text contents within the structured document tag). |
| [isShowingPlaceholderText(boolean value)](#isShowingPlaceholderText-boolean-) | Specifies whether the content of this structured document tag shall be interpreted to contain placeholder text (as opposed to regular text contents within the structured document tag). |
| [iterator()](#iterator--) | Provides support for the for each style iteration over the child nodes of this node. |
| [nextPreOrder(Node rootNode)](#nextPreOrder-com.aspose.words.Node-) | Gets next node according to the pre-order tree traversal algorithm. |
| [nodeTypeToString(int nodeType)](#nodeTypeToString-int-) |  |
| [notify()](#notify--) |  |
| [notifyAll()](#notifyAll--) |  |
| [previousPreOrder(Node rootNode)](#previousPreOrder-com.aspose.words.Node-) | Gets the previous node according to the pre-order tree traversal algorithm. |
| [remove()](#remove--) | Removes itself from the parent. |
| [removeAllChildren()](#removeAllChildren--) | Removes all the nodes between this range start node and the range end node. |
| [removeSelfOnly()](#removeSelfOnly--) | Removes this range start and appropriate range end nodes of the structured document tag, but keeps its content inside the document tree. |
| [setColor(Color value)](#setColor-java.awt.Color-) | Sets the color of the structured document tag. |
| [setCustomNodeId(int value)](#setCustomNodeId-int-) | Specifies custom node identifier. |
| [setLockContentControl(boolean value)](#setLockContentControl-boolean-) | When set to true, this property will prohibit a user from deleting this structured document tag. |
| [setLockContents(boolean value)](#setLockContents-boolean-) | When set to true, this property will prohibit a user from editing the contents of this structured document tag. |
| [setPlaceholderName(String value)](#setPlaceholderName-java.lang.String-) | Gets or sets Name of the [BuildingBlock](../../com.aspose.words/buildingblock) containing placeholder text. |
| [setTag(String value)](#setTag-java.lang.String-) | Specifies a tag associated with the current structured document tag node. |
| [setTitle(String value)](#setTitle-java.lang.String-) | Specifies the friendly name associated with this structured document tag. |
| [structuredDocumentTagNode()](#structuredDocumentTagNode--) |  |
| [toString()](#toString--) |  |
| [toString(SaveOptions saveOptions)](#toString-com.aspose.words.SaveOptions-) | Exports the content of the node into a string using the specified save options. |
| [toString(int saveFormat)](#toString-int-) |  |
| [wait()](#wait--) |  |
| [wait(long arg0)](#wait-long-) |  |
| [wait(long arg0, int arg1)](#wait-long-int-) |  |
### StructuredDocumentTagRangeStart(DocumentBase doc, int type) {#StructuredDocumentTagRangeStart-com.aspose.words.DocumentBase-int-}
```
public StructuredDocumentTagRangeStart(DocumentBase doc, int type)
```


Initializes a new instance of this class.

**Parameters:**
| Parameter | Type | Description |
| --- | --- | --- |
| doc | [DocumentBase](../../com.aspose.words/documentbase) |  |
| type | int |  |

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
| visitor | [DocumentVisitor](../../com.aspose.words/documentvisitor) |  |

**Returns:**
boolean
### appendChild(Node newChild) {#appendChild-com.aspose.words.Node-}
```
public Node appendChild(Node newChild)
```


Adds the specified node to the end of the stdContent range.

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
### getChildNodes() {#getChildNodes--}
```
public NodeCollection getChildNodes()
```


Gets all nodes between this range start node and the range end node.

**Returns:**
[NodeCollection](../../com.aspose.words/nodecollection) - All nodes between this range start node and the range end node.
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
### getColor() {#getColor--}
```
public Color getColor()
```


Gets the color of the structured document tag.

**Returns:**
java.awt.Color - The color of the structured document tag.
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
### getDocument() {#getDocument--}
```
public DocumentBase getDocument()
```


Gets the document to which this node belongs.

The node always belongs to a document even if it has just been created and not yet added to the tree, or if it has been removed from the tree.

**Returns:**
[DocumentBase](../../com.aspose.words/documentbase) - The document to which this node belongs.
### getId() {#getId--}
```
public int getId()
```


Specifies a unique read-only persistent numerical Id for this structured document tag.

Id attribute shall follow these rules:

 *  The document shall retain structured document tag ids only if the whole document is cloned [Document.deepClone()](../../com.aspose.words/document\#deepClone--).
 *  During [DocumentBase.importNode(com.aspose.words.Node, boolean)](../../com.aspose.words/documentbase\#importNode-com.aspose.words.Node--boolean-) Id shall be retained if import does not cause conflicts with other structured document tag Ids in the target document.
 *  If multiple structured document tag nodes specify the same decimal number value for the Id attribute, then the first structured document tag in the document shall maintain this original Id, and all subsequent structured document tag nodes shall have new identifiers assigned to them when the document is loaded.
 *  During standalone structured document tag **M:Aspose.Words.Markup.StructuredDocumentTag.Clone(System.Boolean,Aspose.Words.INodeCloningListener)** operation new unique ID will be generated for the cloned structured document tag node.
 *  If Id is not specified in the source document, then the structured document tag node shall have a new unique identifier assigned to it when the document is loaded.

**Returns:**
int - The corresponding  int  value.
### getLastChild() {#getLastChild--}
```
public Node getLastChild()
```


Gets the last child in the stdContent range. If there is no last child node, a null is returned.

**Returns:**
[Node](../../com.aspose.words/node) - The last child in the stdContent range.
### getLevel() {#getLevel--}
```
public int getLevel()
```


Gets the level at which this structured document tag range start occurs in the document tree.

**Returns:**
int - The level at which this structured document tag range start occurs in the document tree. The returned value is one of [MarkupLevel](../../com.aspose.words/markuplevel) constants.
### getLockContentControl() {#getLockContentControl--}
```
public boolean getLockContentControl()
```


When set to true, this property will prohibit a user from deleting this structured document tag.

**Returns:**
boolean - The corresponding  boolean  value.
### getLockContents() {#getLockContents--}
```
public boolean getLockContents()
```


When set to true, this property will prohibit a user from editing the contents of this structured document tag.

**Returns:**
boolean - The corresponding  boolean  value.
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


Gets the type of this node.

**Returns:**
int
### getParentNode() {#getParentNode--}
```
public CompositeNode getParentNode()
```


Gets the immediate parent of this node.

If a node has just been created and not yet added to the tree, or if it has been removed from the tree, the parent is null.

**Returns:**
[CompositeNode](../../com.aspose.words/compositenode) - The immediate parent of this node.
### getPlaceholder() {#getPlaceholder--}
```
public BuildingBlock getPlaceholder()
```


Gets the [BuildingBlock](../../com.aspose.words/buildingblock) containing placeholder text which should be displayed when this structured document tag run contents are empty, the associated mapped XML element is empty as specified via the [getXmlMapping()](../../com.aspose.words/structureddocumenttagrangestart\#getXmlMapping--) element or the [isShowingPlaceholderText()](../../com.aspose.words/structureddocumenttagrangestart\#isShowingPlaceholderText--) / [isShowingPlaceholderText(boolean)](../../com.aspose.words/structureddocumenttagrangestart\#isShowingPlaceholderText-boolean-) element is true. Can be null, meaning that the placeholder is not applicable for this structured document tag.

**Returns:**
[BuildingBlock](../../com.aspose.words/buildingblock) - The [BuildingBlock](../../com.aspose.words/buildingblock) containing placeholder text which should be displayed when this structured document tag run contents are empty, the associated mapped XML element is empty as specified via the [getXmlMapping()](../../com.aspose.words/structureddocumenttagrangestart\#getXmlMapping--) element or the [isShowingPlaceholderText()](../../com.aspose.words/structureddocumenttagrangestart\#isShowingPlaceholderText--) / [isShowingPlaceholderText(boolean)](../../com.aspose.words/structureddocumenttagrangestart\#isShowingPlaceholderText-boolean-) element is true.
### getPlaceholderName() {#getPlaceholderName--}
```
public String getPlaceholderName()
```


Gets or sets Name of the [BuildingBlock](../../com.aspose.words/buildingblock) containing placeholder text.

BuildingBlock with this name [BuildingBlock.getName()](../../com.aspose.words/buildingblock\#getName--) / [BuildingBlock.setName(java.lang.String)](../../com.aspose.words/buildingblock\#setName-java.lang.String-) has to be present in the [Document.getGlossaryDocument()](../../com.aspose.words/document\#getGlossaryDocument--) / [Document.setGlossaryDocument(com.aspose.words.GlossaryDocument)](../../com.aspose.words/document\#setGlossaryDocument-com.aspose.words.GlossaryDocument-) otherwise java.lang.IllegalStateException will occur.

**Returns:**
java.lang.String - The corresponding java.lang.String value.
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
### getRangeEnd() {#getRangeEnd--}
```
public StructuredDocumentTagRangeEnd getRangeEnd()
```


Specifies end of range if the StructuredDocumentTag is a ranged structured document tag. Otherwise returns null.

**Returns:**
[StructuredDocumentTagRangeEnd](../../com.aspose.words/structureddocumenttagrangeend) - The corresponding [StructuredDocumentTagRangeEnd](../../com.aspose.words/structureddocumenttagrangeend) value.
### getSdtType() {#getSdtType--}
```
public int getSdtType()
```


Gets type of this structured document tag.

**Returns:**
int - Type of this structured document tag. The returned value is one of [SdtType](../../com.aspose.words/sdttype) constants.
### getTag() {#getTag--}
```
public String getTag()
```


Specifies a tag associated with the current structured document tag node. Can not be null. A tag is an arbitrary string which applications can associate with structured document tag in order to identify it without providing a visible friendly name.

**Returns:**
java.lang.String - The corresponding java.lang.String value.
### getText() {#getText--}
```
public String getText()
```


Gets the text of this node and of all its children.

The returned string includes all control and special characters as described in [ControlChar](../../com.aspose.words/controlchar).

**Returns:**
java.lang.String
### getTitle() {#getTitle--}
```
public String getTitle()
```


Specifies the friendly name associated with this structured document tag. Can not be null.

**Returns:**
java.lang.String - The corresponding java.lang.String value.
### getWordOpenXML() {#getWordOpenXML--}
```
public String getWordOpenXML()
```


Gets a string that represents the XML contained within the node in the [SaveFormat.FLAT\_OPC](../../com.aspose.words/saveformat\#FLAT-OPC) format.

**Returns:**
java.lang.String - A string that represents the XML contained within the node in the [SaveFormat.FLAT\_OPC](../../com.aspose.words/saveformat\#FLAT-OPC) format.
### getXmlMapping() {#getXmlMapping--}
```
public XmlMapping getXmlMapping()
```


Gets an object that represents the mapping of this structured document tag range to XML data in a custom XML part of the current document. You can use the [XmlMapping.setMapping(com.aspose.words.CustomXmlPart, java.lang.String, java.lang.String)](../../com.aspose.words/xmlmapping\#setMapping-com.aspose.words.CustomXmlPart--java.lang.String--java.lang.String-) method of this object to map a structured document tag range to XML data.

**Returns:**
[XmlMapping](../../com.aspose.words/xmlmapping) - An object that represents the mapping of this structured document tag range to XML data in a custom XML part of the current document.
### hashCode() {#hashCode--}
```
public native int hashCode()
```




**Returns:**
int
### isComposite() {#isComposite--}
```
public boolean isComposite()
```


Returns true if this node can contain other nodes. (31110,6)

**Returns:**
boolean - True if this node can contain other nodes.
### isRanged() {#isRanged--}
```
public boolean isRanged()
```


Returns true if this instance is a ranged structured document tag.

**Returns:**
boolean
### isShowingPlaceholderText() {#isShowingPlaceholderText--}
```
public boolean isShowingPlaceholderText()
```


Specifies whether the content of this structured document tag shall be interpreted to contain placeholder text (as opposed to regular text contents within the structured document tag).

if set to true, this state shall be resumed (showing placeholder text) upon opening this document.

**Returns:**
boolean - The corresponding  boolean  value.
### isShowingPlaceholderText(boolean value) {#isShowingPlaceholderText-boolean-}
```
public void isShowingPlaceholderText(boolean value)
```


Specifies whether the content of this structured document tag shall be interpreted to contain placeholder text (as opposed to regular text contents within the structured document tag).

if set to true, this state shall be resumed (showing placeholder text) upon opening this document.

**Parameters:**
| Parameter | Type | Description |
| --- | --- | --- |
| value | boolean | The corresponding  boolean  value. |

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


Removes all the nodes between this range start node and the range end node.

### removeSelfOnly() {#removeSelfOnly--}
```
public void removeSelfOnly()
```


Removes this range start and appropriate range end nodes of the structured document tag, but keeps its content inside the document tree.

### setColor(Color value) {#setColor-java.awt.Color-}
```
public void setColor(Color value)
```


Sets the color of the structured document tag.

**Parameters:**
| Parameter | Type | Description |
| --- | --- | --- |
| value | java.awt.Color | The color of the structured document tag. |

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

### setLockContentControl(boolean value) {#setLockContentControl-boolean-}
```
public void setLockContentControl(boolean value)
```


When set to true, this property will prohibit a user from deleting this structured document tag.

**Parameters:**
| Parameter | Type | Description |
| --- | --- | --- |
| value | boolean | The corresponding  boolean  value. |

### setLockContents(boolean value) {#setLockContents-boolean-}
```
public void setLockContents(boolean value)
```


When set to true, this property will prohibit a user from editing the contents of this structured document tag.

**Parameters:**
| Parameter | Type | Description |
| --- | --- | --- |
| value | boolean | The corresponding  boolean  value. |

### setPlaceholderName(String value) {#setPlaceholderName-java.lang.String-}
```
public void setPlaceholderName(String value)
```


Gets or sets Name of the [BuildingBlock](../../com.aspose.words/buildingblock) containing placeholder text.

BuildingBlock with this name [BuildingBlock.getName()](../../com.aspose.words/buildingblock\#getName--) / [BuildingBlock.setName(java.lang.String)](../../com.aspose.words/buildingblock\#setName-java.lang.String-) has to be present in the [Document.getGlossaryDocument()](../../com.aspose.words/document\#getGlossaryDocument--) / [Document.setGlossaryDocument(com.aspose.words.GlossaryDocument)](../../com.aspose.words/document\#setGlossaryDocument-com.aspose.words.GlossaryDocument-) otherwise java.lang.IllegalStateException will occur.

**Parameters:**
| Parameter | Type | Description |
| --- | --- | --- |
| value | java.lang.String | The corresponding java.lang.String value. |

### setTag(String value) {#setTag-java.lang.String-}
```
public void setTag(String value)
```


Specifies a tag associated with the current structured document tag node. Can not be null. A tag is an arbitrary string which applications can associate with structured document tag in order to identify it without providing a visible friendly name.

**Parameters:**
| Parameter | Type | Description |
| --- | --- | --- |
| value | java.lang.String | The corresponding java.lang.String value. |

### setTitle(String value) {#setTitle-java.lang.String-}
```
public void setTitle(String value)
```


Specifies the friendly name associated with this structured document tag. Can not be null.

**Parameters:**
| Parameter | Type | Description |
| --- | --- | --- |
| value | java.lang.String | The corresponding java.lang.String value. |

### structuredDocumentTagNode() {#structuredDocumentTagNode--}
```
public Node structuredDocumentTagNode()
```


Returns Node object that implements this interface.

**Returns:**
[Node](../../com.aspose.words/node)
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

