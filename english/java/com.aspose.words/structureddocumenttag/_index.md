---
title: StructuredDocumentTag
linktitle: StructuredDocumentTag
second_title: Aspose.Words for Java API Reference
description: Represents a structured document tag SDT or content control in a document in Java.
type: docs
weight: 538
url: /java/com.aspose.words/structureddocumenttag/
---

**Inheritance:**
java.lang.Object, [com.aspose.words.Node](../../com.aspose.words/node/), [com.aspose.words.CompositeNode](../../com.aspose.words/compositenode/)

**All Implemented Interfaces:**
[com.aspose.words.IStructuredDocumentTag](../../com.aspose.words/istructureddocumenttag/)
```
public class StructuredDocumentTag extends CompositeNode implements IStructuredDocumentTag
```

Represents a structured document tag (SDT or content control) in a document.

To learn more, visit the [ Structured Document Tags or Content Control ][Structured Document Tags or Content Control] documentation article.

Structured document tags (SDTs) allow to embed customer-defined semantics as well as its behavior and appearance into a document.

In this version Aspose.Words provides a number of public methods and properties to manipulate the behavior and content of [StructuredDocumentTag](../../com.aspose.words/structureddocumenttag/). Mapping of SDT nodes to custom XML packages within a document can be performed with using the [getXmlMapping()](../../com.aspose.words/structureddocumenttag/\#getXmlMapping) property.

[StructuredDocumentTag](../../com.aspose.words/structureddocumenttag/) can occur in a document in the following places:

 *  Block-level - Among paragraphs and tables, as a child of a [Body](../../com.aspose.words/body/), [HeaderFooter](../../com.aspose.words/headerfooter/), [Comment](../../com.aspose.words/comment/), [Footnote](../../com.aspose.words/footnote/) or a [Shape](../../com.aspose.words/shape/) node.
 *  Row-level - Among rows in a table, as a child of a [Table](../../com.aspose.words/table/) node.
 *  Cell-level - Among cells in a table row, as a child of a [Row](../../com.aspose.words/row/) node.
 *  Inline-level - Among inline content inside, as a child of a [Paragraph](../../com.aspose.words/paragraph/).
 *  Nested inside another [StructuredDocumentTag](../../com.aspose.words/structureddocumenttag/).


[Structured Document Tags or Content Control]: https://docs.aspose.com/words/java/working-with-content-control-sdt/
## Constructors

| Constructor | Description |
| --- | --- |
| [StructuredDocumentTag(DocumentBase doc, int type, int level)](#StructuredDocumentTag-com.aspose.words.DocumentBase-int-int) | Initializes a new instance of this class. |
## Methods

| Method | Description |
| --- | --- |
| [accept(DocumentVisitor visitor)](#accept-com.aspose.words.DocumentVisitor) | Accepts a visitor. |
| [appendChild(Node newChild)](#appendChild-com.aspose.words.Node) | Adds the specified node to the end of the list of child nodes for this node. |
| [clear()](#clear) | Clears contents of this structured document tag and displays a placeholder if it is defined. |
| [clearRunAttrs()](#clearRunAttrs) |  |
| [dd()](#dd) |  |
| [deepClone(boolean isCloneChildren)](#deepClone-boolean) | Creates a duplicate of the node. |
| [equals(Object arg0)](#equals-java.lang.Object) |  |
| [fetchInheritedRunAttr(int key)](#fetchInheritedRunAttr-int) |  |
| [getAncestor(int ancestorType)](#getAncestor-int) |  |
| [getAncestor(Class ancestorType)](#getAncestor-java.lang.Class) | Gets the first ancestor of the specified object type. |
| [getAppearance()](#getAppearance) | Gets/sets the appearance of a structured document tag. |
| [getBuildingBlockCategory()](#getBuildingBlockCategory) | Specifies category of building block for this **SDT** node. |
| [getBuildingBlockGallery()](#getBuildingBlockGallery) | Specifies type of building block for this **SDT**. |
| [getCalendarType()](#getCalendarType) | Specifies the type of calendar for this **SDT**. |
| [getChecked()](#getChecked) | Gets/Sets current state of the Checkbox **SDT**. |
| [getChild(int nodeType, int index, boolean isDeep)](#getChild-int-int-boolean) |  |
| [getChildNodes()](#getChildNodes) | Gets all immediate child nodes of this node. |
| [getChildNodes(int nodeType, boolean isDeep)](#getChildNodes-int-boolean) |  |
| [getClass()](#getClass) |  |
| [getColor()](#getColor) | Gets the color of the structured document tag. |
| [getContainer()](#getContainer) |  |
| [getContentsFont()](#getContentsFont) | Font formatting that will be applied to text entered into **SDT**. |
| [getCount()](#getCount) | Gets the number of immediate children of this node. |
| [getCurrentNode()](#getCurrentNode) |  |
| [getCustomNodeId()](#getCustomNodeId) | Specifies custom node identifier. |
| [getDateDisplayFormat()](#getDateDisplayFormat) | String that represents the format in which dates are displayed. |
| [getDateDisplayLocale()](#getDateDisplayLocale) | Allows to set/get the language format for the date displayed in this **SDT**. |
| [getDateStorageFormat()](#getDateStorageFormat) | Gets/sets format in which the date for a date SDT is stored when the **SDT** is bound to an XML node in the document's data store. |
| [getDirectRunAttr(int key)](#getDirectRunAttr-int) |  |
| [getDirectRunAttr(int key, int revisionsView)](#getDirectRunAttr-int-int) |  |
| [getDocument()](#getDocument) | Gets the document to which this node belongs. |
| [getEndCharacterFont()](#getEndCharacterFont) | Font formatting that will be applied to the last character of text entered into **SDT**. |
| [getFirstChild()](#getFirstChild) | Gets the first child of the node. |
| [getFullDate()](#getFullDate) | Specifies the full date and time last entered into this **SDT**. |
| [getId()](#getId) | Specifies a unique read-only persistent numerical Id for this **SDT**. |
| [getLastChild()](#getLastChild) | Gets the last child of the node. |
| [getLevel()](#getLevel) | Gets the level at which this **SDT** occurs in the document tree. |
| [getLevel_IMarkupNode()](#getLevel-IMarkupNode) |  |
| [getListItems()](#getListItems) | Gets [SdtListItemCollection](../../com.aspose.words/sdtlistitemcollection/) associated with this **SDT**. |
| [getLockContentControl()](#getLockContentControl) | When set to  true , this property will prohibit a user from deleting this **SDT**. |
| [getLockContents()](#getLockContents) | When set to  true , this property will prohibit a user from editing the contents of this **SDT**. |
| [getMultiline()](#getMultiline) | Specifies whether this **SDT** allows multiple lines of text. |
| [getNextMatchingNode(Node curNode)](#getNextMatchingNode-com.aspose.words.Node) |  |
| [getNextSibling()](#getNextSibling) | Gets the node immediately following this node. |
| [getNodeType()](#getNodeType) | Returns [NodeType.STRUCTURED\_DOCUMENT\_TAG](../../com.aspose.words/nodetype/\#STRUCTURED-DOCUMENT-TAG). |
| [getParentNode()](#getParentNode) | Gets the immediate parent of this node. |
| [getPlaceholder()](#getPlaceholder) | Gets the [BuildingBlock](../../com.aspose.words/buildingblock/) containing placeholder text which should be displayed when this SDT run contents are empty, the associated mapped XML element is empty as specified via the [getXmlMapping()](../../com.aspose.words/structureddocumenttag/\#getXmlMapping) element or the [isShowingPlaceholderText()](../../com.aspose.words/structureddocumenttag/\#isShowingPlaceholderText) / [isShowingPlaceholderText(boolean)](../../com.aspose.words/structureddocumenttag/\#isShowingPlaceholderText-boolean) element is  true . |
| [getPlaceholderName()](#getPlaceholderName) | Gets or sets Name of the [BuildingBlock](../../com.aspose.words/buildingblock/) containing placeholder text. |
| [getPreviousSibling()](#getPreviousSibling) | Gets the node immediately preceding this node. |
| [getRange()](#getRange) | Returns a [Range](../../com.aspose.words/range/) object that represents the portion of a document that is contained in this node. |
| [getSdtType()](#getSdtType) | Gets type of this **Structured document tag**. |
| [getStyle()](#getStyle) | Gets the Style of the structured document tag. |
| [getStyleName()](#getStyleName) | Gets the name of the style applied to the structured document tag. |
| [getTag()](#getTag) | Specifies a tag associated with the current SDT node. |
| [getText()](#getText) | Gets the text of this node and of all its children. |
| [getTitle()](#getTitle) | Specifies the friendly name associated with this **SDT**. |
| [getWordOpenXML()](#getWordOpenXML) | Gets a string that represents the XML contained within the node in the [SaveFormat.FLAT\_OPC](../../com.aspose.words/saveformat/\#FLAT-OPC) format. |
| [getXmlMapping()](#getXmlMapping) | Gets an object that represents the mapping of this structured document tag to XML data in a custom XML part of the current document. |
| [hasChildNodes()](#hasChildNodes) | Returns  true  if this node has any child nodes. |
| [hashCode()](#hashCode) |  |
| [indexOf(Node child)](#indexOf-com.aspose.words.Node) | Returns the index of the specified child node in the child node array. |
| [insertAfter(Node newChild, Node refChild)](#insertAfter-com.aspose.words.Node-com.aspose.words.Node) | Inserts the specified node immediately after the specified reference node. |
| [insertBefore(Node newChild, Node refChild)](#insertBefore-com.aspose.words.Node-com.aspose.words.Node) | Inserts the specified node immediately before the specified reference node. |
| [isComposite()](#isComposite) | Returns  true  as this node can have child nodes. |
| [isRanged()](#isRanged) |  |
| [isShowingPlaceholderText()](#isShowingPlaceholderText) | Specifies whether the content of this **SDT** shall be interpreted to contain placeholder text (as opposed to regular text contents within the SDT). |
| [isShowingPlaceholderText(boolean value)](#isShowingPlaceholderText-boolean) | Specifies whether the content of this **SDT** shall be interpreted to contain placeholder text (as opposed to regular text contents within the SDT). |
| [isTemporary()](#isTemporary) | Specifies whether this **SDT** shall be removed from the WordProcessingML document when its contents are modified. |
| [isTemporary(boolean value)](#isTemporary-boolean) | Specifies whether this **SDT** shall be removed from the WordProcessingML document when its contents are modified. |
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
| [removeMoveRevisions()](#removeMoveRevisions) |  |
| [removeRunAttr(int key)](#removeRunAttr-int) |  |
| [removeSelfOnly()](#removeSelfOnly) | Removes just this SDT node itself, but keeps the content of it inside the document tree. |
| [removeSmartTags()](#removeSmartTags) | Removes all [SmartTag](../../com.aspose.words/smarttag/) descendant nodes of the current node. |
| [selectNodes(String xpath)](#selectNodes-java.lang.String) | Selects a list of nodes matching the XPath expression. |
| [selectSingleNode(String xpath)](#selectSingleNode-java.lang.String) | Selects the first [Node](../../com.aspose.words/node/) that matches the XPath expression. |
| [setAppearance(int value)](#setAppearance-int) | Gets/sets the appearance of a structured document tag. |
| [setBuildingBlockCategory(String value)](#setBuildingBlockCategory-java.lang.String) | Specifies category of building block for this **SDT** node. |
| [setBuildingBlockGallery(String value)](#setBuildingBlockGallery-java.lang.String) | Specifies type of building block for this **SDT**. |
| [setCalendarType(int value)](#setCalendarType-int) | Specifies the type of calendar for this **SDT**. |
| [setChecked(boolean value)](#setChecked-boolean) | Gets/Sets current state of the Checkbox **SDT**. |
| [setCheckedSymbol(int characterCode, String fontName)](#setCheckedSymbol-int-java.lang.String) | Sets the symbol used to represent the checked state of a check box content control. |
| [setColor(Color value)](#setColor-java.awt.Color) | Sets the color of the structured document tag. |
| [setCustomNodeId(int value)](#setCustomNodeId-int) | Specifies custom node identifier. |
| [setDateDisplayFormat(String value)](#setDateDisplayFormat-java.lang.String) | String that represents the format in which dates are displayed. |
| [setDateDisplayLocale(int value)](#setDateDisplayLocale-int) | Allows to set/get the language format for the date displayed in this **SDT**. |
| [setDateStorageFormat(int value)](#setDateStorageFormat-int) | Gets/sets format in which the date for a date SDT is stored when the **SDT** is bound to an XML node in the document's data store. |
| [setFullDate(Date value)](#setFullDate-java.util.Date) | Specifies the full date and time last entered into this **SDT**. |
| [setLockContentControl(boolean value)](#setLockContentControl-boolean) | When set to  true , this property will prohibit a user from deleting this **SDT**. |
| [setLockContents(boolean value)](#setLockContents-boolean) | When set to  true , this property will prohibit a user from editing the contents of this **SDT**. |
| [setMultiline(boolean value)](#setMultiline-boolean) | Specifies whether this **SDT** allows multiple lines of text. |
| [setPlaceholderName(String value)](#setPlaceholderName-java.lang.String) | Gets or sets Name of the [BuildingBlock](../../com.aspose.words/buildingblock/) containing placeholder text. |
| [setRunAttr(int key, Object value)](#setRunAttr-int-java.lang.Object) |  |
| [setStyle(Style value)](#setStyle-com.aspose.words.Style) | Sets the Style of the structured document tag. |
| [setStyleName(String value)](#setStyleName-java.lang.String) | Sets the name of the style applied to the structured document tag. |
| [setTag(String value)](#setTag-java.lang.String) | Specifies a tag associated with the current SDT node. |
| [setTitle(String value)](#setTitle-java.lang.String) | Specifies the friendly name associated with this **SDT**. |
| [setUncheckedSymbol(int characterCode, String fontName)](#setUncheckedSymbol-int-java.lang.String) | Sets the symbol used to represent the unchecked state of a check box content control. |
| [structuredDocumentTagNode()](#structuredDocumentTagNode) |  |
| [toString()](#toString) |  |
| [toString(SaveOptions saveOptions)](#toString-com.aspose.words.SaveOptions) | Exports the content of the node into a string using the specified save options. |
| [toString(int saveFormat)](#toString-int) |  |
| [wait()](#wait) |  |
| [wait(long arg0)](#wait-long) |  |
| [wait(long arg0, int arg1)](#wait-long-int) |  |
### StructuredDocumentTag(DocumentBase doc, int type, int level) {#StructuredDocumentTag-com.aspose.words.DocumentBase-int-int}
```
public StructuredDocumentTag(DocumentBase doc, int type, int level)
```


Initializes a new instance of this class.

**Parameters:**
| Parameter | Type | Description |
| --- | --- | --- |
| doc | [DocumentBase](../../com.aspose.words/documentbase/) |  |
| type | int |  |
| level | int |  |

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
boolean - True if all nodes were visited; false if [DocumentVisitor](../../com.aspose.words/documentvisitor/) stopped the operation before visiting all nodes. Calls [DocumentVisitor.visitStructuredDocumentTagStart(com.aspose.words.StructuredDocumentTag)](../../com.aspose.words/documentvisitor/\#visitStructuredDocumentTagStart-com.aspose.words.StructuredDocumentTag), then calls [Node.accept(com.aspose.words.DocumentVisitor)](../../com.aspose.words/node/\#accept-com.aspose.words.DocumentVisitor) for all child nodes of the smart tag and calls [DocumentVisitor.visitStructuredDocumentTagEnd(com.aspose.words.StructuredDocumentTag)](../../com.aspose.words/documentvisitor/\#visitStructuredDocumentTagEnd-com.aspose.words.StructuredDocumentTag) at the end.
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
### clear() {#clear}
```
public void clear()
```


Clears contents of this structured document tag and displays a placeholder if it is defined.

It is not possible to clear contents of a structured document tag if it has revisions.

If this structured document tag is mapped to custom XML (with using the [getXmlMapping()](../../com.aspose.words/structureddocumenttag/\#getXmlMapping) property), the referenced XML node is cleared.

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
### fetchInheritedRunAttr(int key) {#fetchInheritedRunAttr-int}
```
public Object fetchInheritedRunAttr(int key)
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
### getAppearance() {#getAppearance}
```
public int getAppearance()
```


Gets/sets the appearance of a structured document tag.

**Returns:**
int - The corresponding  int  value. The returned value is one of [SdtAppearance](../../com.aspose.words/sdtappearance/) constants.
### getBuildingBlockCategory() {#getBuildingBlockCategory}
```
public String getBuildingBlockCategory()
```


Specifies category of building block for this **SDT** node. Can not be  null .

Accessing this property will only work for [SdtType.BUILDING\_BLOCK\_GALLERY](../../com.aspose.words/sdttype/\#BUILDING-BLOCK-GALLERY) and [SdtType.DOC\_PART\_OBJ](../../com.aspose.words/sdttype/\#DOC-PART-OBJ) SDT types. It is read-only for **SDT** of the document part type.

For all other SDT types exception will occur.

**Returns:**
java.lang.String - The corresponding java.lang.String value.
### getBuildingBlockGallery() {#getBuildingBlockGallery}
```
public String getBuildingBlockGallery()
```


Specifies type of building block for this **SDT**. Can not be  null .

Accessing this property will only work for [SdtType.BUILDING\_BLOCK\_GALLERY](../../com.aspose.words/sdttype/\#BUILDING-BLOCK-GALLERY) and [SdtType.DOC\_PART\_OBJ](../../com.aspose.words/sdttype/\#DOC-PART-OBJ) SDT types. It is read-only for **SDT** of the document part type.

For all other SDT types exception will occur.

**Returns:**
java.lang.String - The corresponding java.lang.String value.
### getCalendarType() {#getCalendarType}
```
public int getCalendarType()
```


Specifies the type of calendar for this **SDT**. Default is [SdtCalendarType.DEFAULT](../../com.aspose.words/sdtcalendartype/\#DEFAULT)

Accessing this property will only work for [SdtType.DATE](../../com.aspose.words/sdttype/\#DATE) SDT type.

For all other SDT types exception will occur.

**Returns:**
int - The corresponding  int  value. The returned value is one of [SdtCalendarType](../../com.aspose.words/sdtcalendartype/) constants.
### getChecked() {#getChecked}
```
public boolean getChecked()
```


Gets/Sets current state of the Checkbox **SDT**. Default value for this property is  false .

Accessing this property will only work for [SdtType.CHECKBOX](../../com.aspose.words/sdttype/\#CHECKBOX) SDT types.

For all other SDT types exception will occur.

**Returns:**
boolean - The corresponding  boolean  value.
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
### getColor() {#getColor}
```
public Color getColor()
```


Gets the color of the structured document tag.

**Returns:**
java.awt.Color - The color of the structured document tag.
### getContainer() {#getContainer}
```
public CompositeNode getContainer()
```




**Returns:**
[CompositeNode](../../com.aspose.words/compositenode/)
### getContentsFont() {#getContentsFont}
```
public Font getContentsFont()
```


Font formatting that will be applied to text entered into **SDT**.

**Returns:**
[Font](../../com.aspose.words/font/) - The corresponding [Font](../../com.aspose.words/font/) value.
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
### getDateDisplayFormat() {#getDateDisplayFormat}
```
public String getDateDisplayFormat()
```


String that represents the format in which dates are displayed. Can not be  null . The dates for English (U.S.) is "mm/dd/yyyy"

Accessing this property will only work for [SdtType.DATE](../../com.aspose.words/sdttype/\#DATE) SDT type.

For all other SDT types exception will occur.

**Returns:**
java.lang.String - The corresponding java.lang.String value.
### getDateDisplayLocale() {#getDateDisplayLocale}
```
public int getDateDisplayLocale()
```


Allows to set/get the language format for the date displayed in this **SDT**.

Accessing this property will only work for [SdtType.DATE](../../com.aspose.words/sdttype/\#DATE) SDT type.

For all other SDT types exception will occur.

**Returns:**
int - The corresponding  int  value.
### getDateStorageFormat() {#getDateStorageFormat}
```
public int getDateStorageFormat()
```


Gets/sets format in which the date for a date SDT is stored when the **SDT** is bound to an XML node in the document's data store. Default value is [SdtDateStorageFormat.DATE\_TIME](../../com.aspose.words/sdtdatestorageformat/\#DATE-TIME)

Accessing this property will only work for [SdtType.DATE](../../com.aspose.words/sdttype/\#DATE) SDT type.

For all other SDT types exception will occur.

**Returns:**
int - The corresponding  int  value. The returned value is one of [SdtDateStorageFormat](../../com.aspose.words/sdtdatestorageformat/) constants.
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
### getEndCharacterFont() {#getEndCharacterFont}
```
public Font getEndCharacterFont()
```


Font formatting that will be applied to the last character of text entered into **SDT**.

**Returns:**
[Font](../../com.aspose.words/font/) - The corresponding [Font](../../com.aspose.words/font/) value.
### getFirstChild() {#getFirstChild}
```
public Node getFirstChild()
```


Gets the first child of the node. If there is no first child node, a  null  is returned.

**Returns:**
[Node](../../com.aspose.words/node/) - The first child of the node.
### getFullDate() {#getFullDate}
```
public Date getFullDate()
```


Specifies the full date and time last entered into this **SDT**.

Accessing this property will only work for [SdtType.DATE](../../com.aspose.words/sdttype/\#DATE) SDT type.

For all other SDT types exception will occur.

**Returns:**
java.util.Date - The corresponding java.util.Date value.
### getId() {#getId}
```
public int getId()
```


Specifies a unique read-only persistent numerical Id for this **SDT**.

Id attribute shall follow these rules:

 *  The document shall retain SDT ids only if the whole document is cloned [Document.deepClone()](../../com.aspose.words/document/\#deepClone).
 *  During [DocumentBase.importNode(com.aspose.words.Node, boolean)](../../com.aspose.words/documentbase/\#importNode-com.aspose.words.Node--boolean) Id shall be retained if import does not cause conflicts with other SDT Ids in the target document.
 *  If multiple SDT nodes specify the same decimal number value for the Id attribute, then the first SDT in the document shall maintain this original Id, and all subsequent SDT nodes shall have new identifiers assigned to them when the document is loaded.
 *  During standalone SDT **M:Aspose.Words.Markup.StructuredDocumentTag.Clone(System.Boolean,Aspose.Words.INodeCloningListener)** operation new unique ID will be generated for the cloned SDT node.
 *  If Id is not specified in the source document, then the SDT node shall have a new unique identifier assigned to it when the document is loaded.

**Returns:**
int - The corresponding  int  value.
### getLastChild() {#getLastChild}
```
public Node getLastChild()
```


Gets the last child of the node. If there is no last child node, a  null  is returned.

**Returns:**
[Node](../../com.aspose.words/node/) - The last child of the node.
### getLevel() {#getLevel}
```
public int getLevel()
```


Gets the level at which this **SDT** occurs in the document tree.

**Returns:**
int - The level at which this **SDT** occurs in the document tree. The returned value is one of [MarkupLevel](../../com.aspose.words/markuplevel/) constants.
### getLevel_IMarkupNode() {#getLevel-IMarkupNode}
```
public int getLevel_IMarkupNode()
```




**Returns:**
int
### getListItems() {#getListItems}
```
public SdtListItemCollection getListItems()
```


Gets [SdtListItemCollection](../../com.aspose.words/sdtlistitemcollection/) associated with this **SDT**.

Accessing this property will only work for [SdtType.COMBO\_BOX](../../com.aspose.words/sdttype/\#COMBO-BOX) or [SdtType.DROP\_DOWN\_LIST](../../com.aspose.words/sdttype/\#DROP-DOWN-LIST) SDT types.

For all other SDT types exception will occur.

**Returns:**
[SdtListItemCollection](../../com.aspose.words/sdtlistitemcollection/) - \{[SdtListItemCollection](../../com.aspose.words/sdtlistitemcollection/) associated with this **SDT**.
### getLockContentControl() {#getLockContentControl}
```
public boolean getLockContentControl()
```


When set to  true , this property will prohibit a user from deleting this **SDT**.

**Returns:**
boolean - The corresponding  boolean  value.
### getLockContents() {#getLockContents}
```
public boolean getLockContents()
```


When set to  true , this property will prohibit a user from editing the contents of this **SDT**.

**Returns:**
boolean - The corresponding  boolean  value.
### getMultiline() {#getMultiline}
```
public boolean getMultiline()
```


Specifies whether this **SDT** allows multiple lines of text.

Accessing this property will only work for [SdtType.RICH\_TEXT](../../com.aspose.words/sdttype/\#RICH-TEXT) and [SdtType.PLAIN\_TEXT](../../com.aspose.words/sdttype/\#PLAIN-TEXT) SDT type.

For all other SDT types exception will occur.

**Returns:**
boolean - The corresponding  boolean  value.
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


Returns [NodeType.STRUCTURED\_DOCUMENT\_TAG](../../com.aspose.words/nodetype/\#STRUCTURED-DOCUMENT-TAG).

**Returns:**
int - \{[NodeType.STRUCTURED\_DOCUMENT\_TAG](../../com.aspose.words/nodetype/\#STRUCTURED-DOCUMENT-TAG). The returned value is one of [NodeType](../../com.aspose.words/nodetype/) constants.
### getParentNode() {#getParentNode}
```
public CompositeNode getParentNode()
```


Gets the immediate parent of this node.

If a node has just been created and not yet added to the tree, or if it has been removed from the tree, the parent is  null .

**Returns:**
[CompositeNode](../../com.aspose.words/compositenode/) - The immediate parent of this node.
### getPlaceholder() {#getPlaceholder}
```
public BuildingBlock getPlaceholder()
```


Gets the [BuildingBlock](../../com.aspose.words/buildingblock/) containing placeholder text which should be displayed when this SDT run contents are empty, the associated mapped XML element is empty as specified via the [getXmlMapping()](../../com.aspose.words/structureddocumenttag/\#getXmlMapping) element or the [isShowingPlaceholderText()](../../com.aspose.words/structureddocumenttag/\#isShowingPlaceholderText) / [isShowingPlaceholderText(boolean)](../../com.aspose.words/structureddocumenttag/\#isShowingPlaceholderText-boolean) element is  true . Can be  null , meaning that the placeholder is not applicable for this Sdt.

**Returns:**
[BuildingBlock](../../com.aspose.words/buildingblock/) - The [BuildingBlock](../../com.aspose.words/buildingblock/) containing placeholder text which should be displayed when this SDT run contents are empty, the associated mapped XML element is empty as specified via the [getXmlMapping()](../../com.aspose.words/structureddocumenttag/\#getXmlMapping) element or the [isShowingPlaceholderText()](../../com.aspose.words/structureddocumenttag/\#isShowingPlaceholderText) / [isShowingPlaceholderText(boolean)](../../com.aspose.words/structureddocumenttag/\#isShowingPlaceholderText-boolean) element is  true .
### getPlaceholderName() {#getPlaceholderName}
```
public String getPlaceholderName()
```


Gets or sets Name of the [BuildingBlock](../../com.aspose.words/buildingblock/) containing placeholder text.

[BuildingBlock](../../com.aspose.words/buildingblock/) with this name [BuildingBlock.getName()](../../com.aspose.words/buildingblock/\#getName) / [BuildingBlock.setName(java.lang.String)](../../com.aspose.words/buildingblock/\#setName-java.lang.String) has to be present in the [Document.getGlossaryDocument()](../../com.aspose.words/document/\#getGlossaryDocument) / [Document.setGlossaryDocument(com.aspose.words.GlossaryDocument)](../../com.aspose.words/document/\#setGlossaryDocument-com.aspose.words.GlossaryDocument) otherwise java.lang.IllegalStateException will occur.

**Returns:**
java.lang.String - The corresponding java.lang.String value.
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
### getSdtType() {#getSdtType}
```
public int getSdtType()
```


Gets type of this **Structured document tag**.

**Returns:**
int - Type of this **Structured document tag**. The returned value is one of [SdtType](../../com.aspose.words/sdttype/) constants.
### getStyle() {#getStyle}
```
public Style getStyle()
```


Gets the Style of the structured document tag. Only [StyleType.CHARACTER](../../com.aspose.words/styletype/\#CHARACTER) style or [StyleType.PARAGRAPH](../../com.aspose.words/styletype/\#PARAGRAPH) style with linked character style can be set.

**Returns:**
[Style](../../com.aspose.words/style/) - The Style of the structured document tag.
### getStyleName() {#getStyleName}
```
public String getStyleName()
```


Gets the name of the style applied to the structured document tag.

**Returns:**
java.lang.String - The name of the style applied to the structured document tag.
### getTag() {#getTag}
```
public String getTag()
```


Specifies a tag associated with the current SDT node. Can not be  null . A tag is an arbitrary string which applications can associate with SDT in order to identify it without providing a visible friendly name.

**Returns:**
java.lang.String - The corresponding java.lang.String value.
### getText() {#getText}
```
public String getText()
```


Gets the text of this node and of all its children.

The returned string includes all control and special characters as described in [ControlChar](../../com.aspose.words/controlchar/).

**Returns:**
java.lang.String
### getTitle() {#getTitle}
```
public String getTitle()
```


Specifies the friendly name associated with this **SDT**. Can not be  null .

**Returns:**
java.lang.String - The corresponding java.lang.String value.
### getWordOpenXML() {#getWordOpenXML}
```
public String getWordOpenXML()
```


Gets a string that represents the XML contained within the node in the [SaveFormat.FLAT\_OPC](../../com.aspose.words/saveformat/\#FLAT-OPC) format.

**Returns:**
java.lang.String - A string that represents the XML contained within the node in the [SaveFormat.FLAT\_OPC](../../com.aspose.words/saveformat/\#FLAT-OPC) format.
### getXmlMapping() {#getXmlMapping}
```
public XmlMapping getXmlMapping()
```


Gets an object that represents the mapping of this structured document tag to XML data in a custom XML part of the current document. You can use the [XmlMapping.setMapping(com.aspose.words.CustomXmlPart, java.lang.String, java.lang.String)](../../com.aspose.words/xmlmapping/\#setMapping-com.aspose.words.CustomXmlPart--java.lang.String--java.lang.String) method of this object to map a structured document tag to XML data.

**Returns:**
[XmlMapping](../../com.aspose.words/xmlmapping/) - An object that represents the mapping of this structured document tag to XML data in a custom XML part of the current document.
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
### isRanged() {#isRanged}
```
public boolean isRanged()
```


Returns true if this instance is a ranged structured document tag.

**Returns:**
boolean
### isShowingPlaceholderText() {#isShowingPlaceholderText}
```
public boolean isShowingPlaceholderText()
```


Specifies whether the content of this **SDT** shall be interpreted to contain placeholder text (as opposed to regular text contents within the SDT).

if set to  true , this state shall be resumed (showing placeholder text) upon opening this document.

**Returns:**
boolean - The corresponding  boolean  value.
### isShowingPlaceholderText(boolean value) {#isShowingPlaceholderText-boolean}
```
public void isShowingPlaceholderText(boolean value)
```


Specifies whether the content of this **SDT** shall be interpreted to contain placeholder text (as opposed to regular text contents within the SDT).

if set to  true , this state shall be resumed (showing placeholder text) upon opening this document.

**Parameters:**
| Parameter | Type | Description |
| --- | --- | --- |
| value | boolean | The corresponding  boolean  value. |

### isTemporary() {#isTemporary}
```
public boolean isTemporary()
```


Specifies whether this **SDT** shall be removed from the WordProcessingML document when its contents are modified.

**Returns:**
boolean - The corresponding  boolean  value.
### isTemporary(boolean value) {#isTemporary-boolean}
```
public void isTemporary(boolean value)
```


Specifies whether this **SDT** shall be removed from the WordProcessingML document when its contents are modified.

**Parameters:**
| Parameter | Type | Description |
| --- | --- | --- |
| value | boolean | The corresponding  boolean  value. |

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




### removeRunAttr(int key) {#removeRunAttr-int}
```
public void removeRunAttr(int key)
```




**Parameters:**
| Parameter | Type | Description |
| --- | --- | --- |
| key | int |  |

### removeSelfOnly() {#removeSelfOnly}
```
public void removeSelfOnly()
```


Removes just this SDT node itself, but keeps the content of it inside the document tree.

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
### setAppearance(int value) {#setAppearance-int}
```
public void setAppearance(int value)
```


Gets/sets the appearance of a structured document tag.

**Parameters:**
| Parameter | Type | Description |
| --- | --- | --- |
| value | int | The corresponding  int  value. The value must be one of [SdtAppearance](../../com.aspose.words/sdtappearance/) constants. |

### setBuildingBlockCategory(String value) {#setBuildingBlockCategory-java.lang.String}
```
public void setBuildingBlockCategory(String value)
```


Specifies category of building block for this **SDT** node. Can not be  null .

Accessing this property will only work for [SdtType.BUILDING\_BLOCK\_GALLERY](../../com.aspose.words/sdttype/\#BUILDING-BLOCK-GALLERY) and [SdtType.DOC\_PART\_OBJ](../../com.aspose.words/sdttype/\#DOC-PART-OBJ) SDT types. It is read-only for **SDT** of the document part type.

For all other SDT types exception will occur.

**Parameters:**
| Parameter | Type | Description |
| --- | --- | --- |
| value | java.lang.String | The corresponding java.lang.String value. |

### setBuildingBlockGallery(String value) {#setBuildingBlockGallery-java.lang.String}
```
public void setBuildingBlockGallery(String value)
```


Specifies type of building block for this **SDT**. Can not be  null .

Accessing this property will only work for [SdtType.BUILDING\_BLOCK\_GALLERY](../../com.aspose.words/sdttype/\#BUILDING-BLOCK-GALLERY) and [SdtType.DOC\_PART\_OBJ](../../com.aspose.words/sdttype/\#DOC-PART-OBJ) SDT types. It is read-only for **SDT** of the document part type.

For all other SDT types exception will occur.

**Parameters:**
| Parameter | Type | Description |
| --- | --- | --- |
| value | java.lang.String | The corresponding java.lang.String value. |

### setCalendarType(int value) {#setCalendarType-int}
```
public void setCalendarType(int value)
```


Specifies the type of calendar for this **SDT**. Default is [SdtCalendarType.DEFAULT](../../com.aspose.words/sdtcalendartype/\#DEFAULT)

Accessing this property will only work for [SdtType.DATE](../../com.aspose.words/sdttype/\#DATE) SDT type.

For all other SDT types exception will occur.

**Parameters:**
| Parameter | Type | Description |
| --- | --- | --- |
| value | int | The corresponding  int  value. The value must be one of [SdtCalendarType](../../com.aspose.words/sdtcalendartype/) constants. |

### setChecked(boolean value) {#setChecked-boolean}
```
public void setChecked(boolean value)
```


Gets/Sets current state of the Checkbox **SDT**. Default value for this property is  false .

Accessing this property will only work for [SdtType.CHECKBOX](../../com.aspose.words/sdttype/\#CHECKBOX) SDT types.

For all other SDT types exception will occur.

**Parameters:**
| Parameter | Type | Description |
| --- | --- | --- |
| value | boolean | The corresponding  boolean  value. |

### setCheckedSymbol(int characterCode, String fontName) {#setCheckedSymbol-int-java.lang.String}
```
public void setCheckedSymbol(int characterCode, String fontName)
```


Sets the symbol used to represent the checked state of a check box content control.

**Parameters:**
| Parameter | Type | Description |
| --- | --- | --- |
| characterCode | int | The character code for the specified symbol. |
| fontName | java.lang.String | The name of the font that contains the symbol.

Accessing this method will only work for [SdtType.CHECKBOX](../../com.aspose.words/sdttype/\#CHECKBOX) SDT types.

For all other SDT types exception will occur. |

### setColor(Color value) {#setColor-java.awt.Color}
```
public void setColor(Color value)
```


Sets the color of the structured document tag.

**Parameters:**
| Parameter | Type | Description |
| --- | --- | --- |
| value | java.awt.Color | The color of the structured document tag. |

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

### setDateDisplayFormat(String value) {#setDateDisplayFormat-java.lang.String}
```
public void setDateDisplayFormat(String value)
```


String that represents the format in which dates are displayed. Can not be  null . The dates for English (U.S.) is "mm/dd/yyyy"

Accessing this property will only work for [SdtType.DATE](../../com.aspose.words/sdttype/\#DATE) SDT type.

For all other SDT types exception will occur.

**Parameters:**
| Parameter | Type | Description |
| --- | --- | --- |
| value | java.lang.String | The corresponding java.lang.String value. |

### setDateDisplayLocale(int value) {#setDateDisplayLocale-int}
```
public void setDateDisplayLocale(int value)
```


Allows to set/get the language format for the date displayed in this **SDT**.

Accessing this property will only work for [SdtType.DATE](../../com.aspose.words/sdttype/\#DATE) SDT type.

For all other SDT types exception will occur.

**Parameters:**
| Parameter | Type | Description |
| --- | --- | --- |
| value | int | The corresponding  int  value. |

### setDateStorageFormat(int value) {#setDateStorageFormat-int}
```
public void setDateStorageFormat(int value)
```


Gets/sets format in which the date for a date SDT is stored when the **SDT** is bound to an XML node in the document's data store. Default value is [SdtDateStorageFormat.DATE\_TIME](../../com.aspose.words/sdtdatestorageformat/\#DATE-TIME)

Accessing this property will only work for [SdtType.DATE](../../com.aspose.words/sdttype/\#DATE) SDT type.

For all other SDT types exception will occur.

**Parameters:**
| Parameter | Type | Description |
| --- | --- | --- |
| value | int | The corresponding  int  value. The value must be one of [SdtDateStorageFormat](../../com.aspose.words/sdtdatestorageformat/) constants. |

### setFullDate(Date value) {#setFullDate-java.util.Date}
```
public void setFullDate(Date value)
```


Specifies the full date and time last entered into this **SDT**.

Accessing this property will only work for [SdtType.DATE](../../com.aspose.words/sdttype/\#DATE) SDT type.

For all other SDT types exception will occur.

**Parameters:**
| Parameter | Type | Description |
| --- | --- | --- |
| value | java.util.Date | The corresponding java.util.Date value. |

### setLockContentControl(boolean value) {#setLockContentControl-boolean}
```
public void setLockContentControl(boolean value)
```


When set to  true , this property will prohibit a user from deleting this **SDT**.

**Parameters:**
| Parameter | Type | Description |
| --- | --- | --- |
| value | boolean | The corresponding  boolean  value. |

### setLockContents(boolean value) {#setLockContents-boolean}
```
public void setLockContents(boolean value)
```


When set to  true , this property will prohibit a user from editing the contents of this **SDT**.

**Parameters:**
| Parameter | Type | Description |
| --- | --- | --- |
| value | boolean | The corresponding  boolean  value. |

### setMultiline(boolean value) {#setMultiline-boolean}
```
public void setMultiline(boolean value)
```


Specifies whether this **SDT** allows multiple lines of text.

Accessing this property will only work for [SdtType.RICH\_TEXT](../../com.aspose.words/sdttype/\#RICH-TEXT) and [SdtType.PLAIN\_TEXT](../../com.aspose.words/sdttype/\#PLAIN-TEXT) SDT type.

For all other SDT types exception will occur.

**Parameters:**
| Parameter | Type | Description |
| --- | --- | --- |
| value | boolean | The corresponding  boolean  value. |

### setPlaceholderName(String value) {#setPlaceholderName-java.lang.String}
```
public void setPlaceholderName(String value)
```


Gets or sets Name of the [BuildingBlock](../../com.aspose.words/buildingblock/) containing placeholder text.

[BuildingBlock](../../com.aspose.words/buildingblock/) with this name [BuildingBlock.getName()](../../com.aspose.words/buildingblock/\#getName) / [BuildingBlock.setName(java.lang.String)](../../com.aspose.words/buildingblock/\#setName-java.lang.String) has to be present in the [Document.getGlossaryDocument()](../../com.aspose.words/document/\#getGlossaryDocument) / [Document.setGlossaryDocument(com.aspose.words.GlossaryDocument)](../../com.aspose.words/document/\#setGlossaryDocument-com.aspose.words.GlossaryDocument) otherwise java.lang.IllegalStateException will occur.

**Parameters:**
| Parameter | Type | Description |
| --- | --- | --- |
| value | java.lang.String | The corresponding java.lang.String value. |

### setRunAttr(int key, Object value) {#setRunAttr-int-java.lang.Object}
```
public void setRunAttr(int key, Object value)
```




**Parameters:**
| Parameter | Type | Description |
| --- | --- | --- |
| key | int |  |
| value | java.lang.Object |  |

### setStyle(Style value) {#setStyle-com.aspose.words.Style}
```
public void setStyle(Style value)
```


Sets the Style of the structured document tag. Only [StyleType.CHARACTER](../../com.aspose.words/styletype/\#CHARACTER) style or [StyleType.PARAGRAPH](../../com.aspose.words/styletype/\#PARAGRAPH) style with linked character style can be set.

**Parameters:**
| Parameter | Type | Description |
| --- | --- | --- |
| value | [Style](../../com.aspose.words/style/) | The Style of the structured document tag. |

### setStyleName(String value) {#setStyleName-java.lang.String}
```
public void setStyleName(String value)
```


Sets the name of the style applied to the structured document tag.

**Parameters:**
| Parameter | Type | Description |
| --- | --- | --- |
| value | java.lang.String | The name of the style applied to the structured document tag. |

### setTag(String value) {#setTag-java.lang.String}
```
public void setTag(String value)
```


Specifies a tag associated with the current SDT node. Can not be  null . A tag is an arbitrary string which applications can associate with SDT in order to identify it without providing a visible friendly name.

**Parameters:**
| Parameter | Type | Description |
| --- | --- | --- |
| value | java.lang.String | The corresponding java.lang.String value. |

### setTitle(String value) {#setTitle-java.lang.String}
```
public void setTitle(String value)
```


Specifies the friendly name associated with this **SDT**. Can not be  null .

**Parameters:**
| Parameter | Type | Description |
| --- | --- | --- |
| value | java.lang.String | The corresponding java.lang.String value. |

### setUncheckedSymbol(int characterCode, String fontName) {#setUncheckedSymbol-int-java.lang.String}
```
public void setUncheckedSymbol(int characterCode, String fontName)
```


Sets the symbol used to represent the unchecked state of a check box content control.

**Parameters:**
| Parameter | Type | Description |
| --- | --- | --- |
| characterCode | int | The character code for the specified symbol. |
| fontName | java.lang.String | The name of the font that contains the symbol.

Accessing this method will only work for [SdtType.CHECKBOX](../../com.aspose.words/sdttype/\#CHECKBOX) SDT types.

For all other SDT types exception will occur. |

### structuredDocumentTagNode() {#structuredDocumentTagNode}
```
public Node structuredDocumentTagNode()
```


Returns Node object that implements this interface.

**Returns:**
[Node](../../com.aspose.words/node/)
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

