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
| [getChildNodes(int nodeType, boolean isDeep)](#getChildNodes-int-boolean-) |  |
| [isRanged()](#isRanged--) |  |
| [structuredDocumentTagNode()](#structuredDocumentTagNode--) |  |
| [getNodeType()](#getNodeType--) |  |
| [getChildNodes()](#getChildNodes--) | Gets all nodes between this range start node and the range end node. |
| [getLastChild()](#getLastChild--) | Gets the last child in the stdContent range. |
| [getLevel()](#getLevel--) | Gets the level at which this structured document tag range start occurs in the document tree. |
| [getSdtType()](#getSdtType--) | Gets type of this structured document tag. |
| [getColor()](#getColor--) | Gets the color of the structured document tag. |
| [setColor(Color value)](#setColor-java.awt.Color-) | Sets the color of the structured document tag. |
| [getId()](#getId--) | Specifies a unique read-only persistent numerical Id for this structured document tag. |
| [getLockContentControl()](#getLockContentControl--) | When set to true, this property will prohibit a user from deleting this structured document tag. |
| [setLockContentControl(boolean value)](#setLockContentControl-boolean-) | When set to true, this property will prohibit a user from deleting this structured document tag. |
| [getLockContents()](#getLockContents--) | When set to true, this property will prohibit a user from editing the contents of this structured document tag. |
| [setLockContents(boolean value)](#setLockContents-boolean-) | When set to true, this property will prohibit a user from editing the contents of this structured document tag. |
| [isShowingPlaceholderText()](#isShowingPlaceholderText--) | Specifies whether the content of this structured document tag shall be interpreted to contain placeholder text (as opposed to regular text contents within the structured document tag). |
| [isShowingPlaceholderText(boolean value)](#isShowingPlaceholderText-boolean-) | Specifies whether the content of this structured document tag shall be interpreted to contain placeholder text (as opposed to regular text contents within the structured document tag). |
| [getPlaceholder()](#getPlaceholder--) | Gets the [BuildingBlock](../../com.aspose.words/buildingblock) containing placeholder text which should be displayed when this structured document tag run contents are empty, the associated mapped XML element is empty as specified via the [getXmlMapping()](../../com.aspose.words/structureddocumenttagrangestart\#getXmlMapping--) element or the [isShowingPlaceholderText()](../../com.aspose.words/structureddocumenttagrangestart\#isShowingPlaceholderText--) / [isShowingPlaceholderText(boolean)](../../com.aspose.words/structureddocumenttagrangestart\#isShowingPlaceholderText-boolean-) element is true. |
| [getPlaceholderName()](#getPlaceholderName--) | Gets or sets Name of the [BuildingBlock](../../com.aspose.words/buildingblock) containing placeholder text. |
| [setPlaceholderName(String value)](#setPlaceholderName-java.lang.String-) | Gets or sets Name of the [BuildingBlock](../../com.aspose.words/buildingblock) containing placeholder text. |
| [getTag()](#getTag--) | Specifies a tag associated with the current structured document tag node. |
| [setTag(String value)](#setTag-java.lang.String-) | Specifies a tag associated with the current structured document tag node. |
| [getTitle()](#getTitle--) | Specifies the friendly name associated with this structured document tag. |
| [setTitle(String value)](#setTitle-java.lang.String-) | Specifies the friendly name associated with this structured document tag. |
| [getWordOpenXML()](#getWordOpenXML--) | Gets a string that represents the XML contained within the node in the [SaveFormat.FLAT\_OPC](../../com.aspose.words/saveformat\#FLAT-OPC) format. |
| [getXmlMapping()](#getXmlMapping--) | Gets an object that represents the mapping of this structured document tag range to XML data in a custom XML part of the current document. |
| [accept(DocumentVisitor visitor)](#accept-com.aspose.words.DocumentVisitor-) |  |
| [getRangeEnd()](#getRangeEnd--) | Specifies end of range if the StructuredDocumentTag is a ranged structured document tag. |
| [iterator()](#iterator--) | Provides support for the for each style iteration over the child nodes of this node. |
| [appendChild(Node newChild)](#appendChild-com.aspose.words.Node-) | Adds the specified node to the end of the stdContent range. |
| [removeAllChildren()](#removeAllChildren--) | Removes all the nodes between this range start node and the range end node. |
| [removeSelfOnly()](#removeSelfOnly--) | Removes this range start and appropriate range end nodes of the structured document tag, but keeps its content inside the document tree. |
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
### isRanged() {#isRanged--}
```
public boolean isRanged()
```


Returns true if this instance is a ranged structured document tag.

**Returns:**
boolean
### structuredDocumentTagNode() {#structuredDocumentTagNode--}
```
public Node structuredDocumentTagNode()
```


Returns Node object that implements this interface.

**Returns:**
[Node](../../com.aspose.words/node)
### getNodeType() {#getNodeType--}
```
public int getNodeType()
```


Gets the type of this node.

**Returns:**
int
### getChildNodes() {#getChildNodes--}
```
public NodeCollection getChildNodes()
```


Gets all nodes between this range start node and the range end node.

**Returns:**
[NodeCollection](../../com.aspose.words/nodecollection) - All nodes between this range start node and the range end node.
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
### getSdtType() {#getSdtType--}
```
public int getSdtType()
```


Gets type of this structured document tag.

**Returns:**
int - Type of this structured document tag. The returned value is one of [SdtType](../../com.aspose.words/sdttype) constants.
### getColor() {#getColor--}
```
public Color getColor()
```


Gets the color of the structured document tag.

**Returns:**
java.awt.Color - The color of the structured document tag.
### setColor(Color value) {#setColor-java.awt.Color-}
```
public void setColor(Color value)
```


Sets the color of the structured document tag.

**Parameters:**
| Parameter | Type | Description |
| --- | --- | --- |
| value | java.awt.Color | The color of the structured document tag. |

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
### getLockContentControl() {#getLockContentControl--}
```
public boolean getLockContentControl()
```


When set to true, this property will prohibit a user from deleting this structured document tag.

**Returns:**
boolean - The corresponding  boolean  value.
### setLockContentControl(boolean value) {#setLockContentControl-boolean-}
```
public void setLockContentControl(boolean value)
```


When set to true, this property will prohibit a user from deleting this structured document tag.

**Parameters:**
| Parameter | Type | Description |
| --- | --- | --- |
| value | boolean | The corresponding  boolean  value. |

### getLockContents() {#getLockContents--}
```
public boolean getLockContents()
```


When set to true, this property will prohibit a user from editing the contents of this structured document tag.

**Returns:**
boolean - The corresponding  boolean  value.
### setLockContents(boolean value) {#setLockContents-boolean-}
```
public void setLockContents(boolean value)
```


When set to true, this property will prohibit a user from editing the contents of this structured document tag.

**Parameters:**
| Parameter | Type | Description |
| --- | --- | --- |
| value | boolean | The corresponding  boolean  value. |

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

### getTag() {#getTag--}
```
public String getTag()
```


Specifies a tag associated with the current structured document tag node. Can not be null. A tag is an arbitrary string which applications can associate with structured document tag in order to identify it without providing a visible friendly name.

**Returns:**
java.lang.String - The corresponding java.lang.String value.
### setTag(String value) {#setTag-java.lang.String-}
```
public void setTag(String value)
```


Specifies a tag associated with the current structured document tag node. Can not be null. A tag is an arbitrary string which applications can associate with structured document tag in order to identify it without providing a visible friendly name.

**Parameters:**
| Parameter | Type | Description |
| --- | --- | --- |
| value | java.lang.String | The corresponding java.lang.String value. |

### getTitle() {#getTitle--}
```
public String getTitle()
```


Specifies the friendly name associated with this structured document tag. Can not be null.

**Returns:**
java.lang.String - The corresponding java.lang.String value.
### setTitle(String value) {#setTitle-java.lang.String-}
```
public void setTitle(String value)
```


Specifies the friendly name associated with this structured document tag. Can not be null.

**Parameters:**
| Parameter | Type | Description |
| --- | --- | --- |
| value | java.lang.String | The corresponding java.lang.String value. |

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
### getRangeEnd() {#getRangeEnd--}
```
public StructuredDocumentTagRangeEnd getRangeEnd()
```


Specifies end of range if the StructuredDocumentTag is a ranged structured document tag. Otherwise returns null.

**Returns:**
[StructuredDocumentTagRangeEnd](../../com.aspose.words/structureddocumenttagrangeend) - The corresponding [StructuredDocumentTagRangeEnd](../../com.aspose.words/structureddocumenttagrangeend) value.
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


Adds the specified node to the end of the stdContent range.

**Parameters:**
| Parameter | Type | Description |
| --- | --- | --- |
| newChild | [Node](../../com.aspose.words/node) | The node to add. |

**Returns:**
[Node](../../com.aspose.words/node) - The node added.
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

