---
title: StructuredDocumentTag
second_title: Aspose.Words for Java API Reference
description: Represents a structured document tag SDT or content control in a document.
type: docs
weight: 532
url: /java/com.aspose.words/structureddocumenttag/
---

**Inheritance:**
java.lang.Object, [com.aspose.words.Node](../../com.aspose.words/node), [com.aspose.words.CompositeNode](../../com.aspose.words/compositenode)

**All Implemented Interfaces:**
[com.aspose.words.IStructuredDocumentTag](../../com.aspose.words/istructureddocumenttag)
```
public class StructuredDocumentTag extends CompositeNode implements IStructuredDocumentTag
```

Represents a structured document tag (SDT or content control) in a document.

To learn more, visit the **Structured Document Tags or Content Control** documentation article.

Structured document tags (SDTs) allow to embed customer-defined semantics as well as its behavior and appearance into a document.

In this version Aspose.Words provides a number of public methods and properties to manipulate the behavior and content of [StructuredDocumentTag](../../com.aspose.words/structureddocumenttag). Mapping of SDT nodes to custom XML packages within a document can be performed with using the [getXmlMapping()](../../com.aspose.words/structureddocumenttag\#getXmlMapping--) property.

[StructuredDocumentTag](../../com.aspose.words/structureddocumenttag) can occur in a document in the following places:

 *  Block-level - Among paragraphs and tables, as a child of a [Body](../../com.aspose.words/body), [HeaderFooter](../../com.aspose.words/headerfooter), [Comment](../../com.aspose.words/comment), [Footnote](../../com.aspose.words/footnote) or a [Shape](../../com.aspose.words/shape) node.
 *  Row-level - Among rows in a table, as a child of a [Table](../../com.aspose.words/table) node.
 *  Cell-level - Among cells in a table row, as a child of a [Row](../../com.aspose.words/row) node.
 *  Inline-level - Among inline content inside, as a child of a [Paragraph](../../com.aspose.words/paragraph).
 *  Nested inside another [StructuredDocumentTag](../../com.aspose.words/structureddocumenttag).
## Constructors

| Constructor | Description |
| --- | --- |
| [StructuredDocumentTag(DocumentBase doc, int type, int level)](#StructuredDocumentTag-com.aspose.words.DocumentBase-int-int-) | Initializes a new instance of this class. |
## Methods

| Method | Description |
| --- | --- |
| [setCheckedSymbol(int characterCode, String fontName)](#setCheckedSymbol-int-java.lang.String-) | Sets the symbol used to represent the checked state of a check box content control. |
| [setUncheckedSymbol(int characterCode, String fontName)](#setUncheckedSymbol-int-java.lang.String-) | Sets the symbol used to represent the unchecked state of a check box content control. |
| [removeSelfOnly()](#removeSelfOnly--) | Removes just this SDT node itself, but keeps the content of it inside the document tree. |
| [accept(DocumentVisitor visitor)](#accept-com.aspose.words.DocumentVisitor-) | Accepts a visitor. |
| [clear()](#clear--) | Clears contents of this structured document tag and displays a placeholder if it is defined. |
| [isRanged()](#isRanged--) |  |
| [structuredDocumentTagNode()](#structuredDocumentTagNode--) |  |
| [getNodeType()](#getNodeType--) | Returns **NodeType.StructuredDocumentTag**. |
| [getPlaceholder()](#getPlaceholder--) | Gets the [BuildingBlock](../../com.aspose.words/buildingblock) containing placeholder text which should be displayed when this SDT run contents are empty, the associated mapped XML element is empty as specified via the [getXmlMapping()](../../com.aspose.words/structureddocumenttag\#getXmlMapping--) element or the [isShowingPlaceholderText()](../../com.aspose.words/structureddocumenttag\#isShowingPlaceholderText--) / [isShowingPlaceholderText(boolean)](../../com.aspose.words/structureddocumenttag\#isShowingPlaceholderText-boolean-) element is true. |
| [getPlaceholderName()](#getPlaceholderName--) | Gets or sets Name of the [BuildingBlock](../../com.aspose.words/buildingblock) containing placeholder text. |
| [setPlaceholderName(String value)](#setPlaceholderName-java.lang.String-) | Gets or sets Name of the [BuildingBlock](../../com.aspose.words/buildingblock) containing placeholder text. |
| [getLevel()](#getLevel--) | Gets the level at which this **SDT** occurs in the document tree. |
| [getSdtType()](#getSdtType--) | Gets type of this **Structured document tag**. |
| [getId()](#getId--) | Specifies a unique read-only persistent numerical Id for this **SDT**. |
| [getLockContentControl()](#getLockContentControl--) | When set to true, this property will prohibit a user from deleting this **SDT**. |
| [setLockContentControl(boolean value)](#setLockContentControl-boolean-) | When set to true, this property will prohibit a user from deleting this **SDT**. |
| [getLockContents()](#getLockContents--) | When set to true, this property will prohibit a user from editing the contents of this **SDT**. |
| [setLockContents(boolean value)](#setLockContents-boolean-) | When set to true, this property will prohibit a user from editing the contents of this **SDT**. |
| [isShowingPlaceholderText()](#isShowingPlaceholderText--) | Specifies whether the content of this **SDT** shall be interpreted to contain placeholder text (as opposed to regular text contents within the SDT). |
| [isShowingPlaceholderText(boolean value)](#isShowingPlaceholderText-boolean-) | Specifies whether the content of this **SDT** shall be interpreted to contain placeholder text (as opposed to regular text contents within the SDT). |
| [getTag()](#getTag--) | Specifies a tag associated with the current SDT node. |
| [setTag(String value)](#setTag-java.lang.String-) | Specifies a tag associated with the current SDT node. |
| [getContentsFont()](#getContentsFont--) | Font formatting that will be applied to text entered into **SDT**. |
| [getEndCharacterFont()](#getEndCharacterFont--) | Font formatting that will be applied to the last character of text entered into **SDT**. |
| [isTemporary()](#isTemporary--) | Specifies whether this **SDT** shall be removed from the WordProcessingML document when its contents are modified. |
| [isTemporary(boolean value)](#isTemporary-boolean-) | Specifies whether this **SDT** shall be removed from the WordProcessingML document when its contents are modified. |
| [getTitle()](#getTitle--) | Specifies the friendly name associated with this **SDT**. |
| [setTitle(String value)](#setTitle-java.lang.String-) | Specifies the friendly name associated with this **SDT**. |
| [getListItems()](#getListItems--) | Gets [SdtListItemCollection](../../com.aspose.words/sdtlistitemcollection) associated with this **SDT**. |
| [getChecked()](#getChecked--) | Gets/Sets current state of the Checkbox **SDT**. |
| [setChecked(boolean value)](#setChecked-boolean-) | Gets/Sets current state of the Checkbox **SDT**. |
| [getAppearance()](#getAppearance--) | Gets/sets the appearance of a structured document tag. |
| [setAppearance(int value)](#setAppearance-int-) | Gets/sets the appearance of a structured document tag. |
| [getDateDisplayLocale()](#getDateDisplayLocale--) | Allows to set/get the language format for the date displayed in this **SDT**. |
| [setDateDisplayLocale(int value)](#setDateDisplayLocale-int-) | Allows to set/get the language format for the date displayed in this **SDT**. |
| [getDateDisplayFormat()](#getDateDisplayFormat--) | String that represents the format in which dates are displayed. |
| [setDateDisplayFormat(String value)](#setDateDisplayFormat-java.lang.String-) | String that represents the format in which dates are displayed. |
| [getFullDate()](#getFullDate--) | Specifies the full date and time last entered into this **SDT**. |
| [setFullDate(Date value)](#setFullDate-java.util.Date-) | Specifies the full date and time last entered into this **SDT**. |
| [getDateStorageFormat()](#getDateStorageFormat--) | Gets/sets format in which the date for a date SDT is stored when the **SDT** is bound to an XML node in the document's data store. |
| [setDateStorageFormat(int value)](#setDateStorageFormat-int-) | Gets/sets format in which the date for a date SDT is stored when the **SDT** is bound to an XML node in the document's data store. |
| [getCalendarType()](#getCalendarType--) | Specifies the type of calendar for this **SDT**. |
| [setCalendarType(int value)](#setCalendarType-int-) | Specifies the type of calendar for this **SDT**. |
| [getBuildingBlockGallery()](#getBuildingBlockGallery--) | Specifies type of building block for this **SDT**. |
| [setBuildingBlockGallery(String value)](#setBuildingBlockGallery-java.lang.String-) | Specifies type of building block for this **SDT**. |
| [getBuildingBlockCategory()](#getBuildingBlockCategory--) | Specifies category of building block for this **SDT** node. |
| [setBuildingBlockCategory(String value)](#setBuildingBlockCategory-java.lang.String-) | Specifies category of building block for this **SDT** node. |
| [getMultiline()](#getMultiline--) | Specifies whether this **SDT** allows multiple lines of text. |
| [setMultiline(boolean value)](#setMultiline-boolean-) | Specifies whether this **SDT** allows multiple lines of text. |
| [getColor()](#getColor--) | Gets the color of the structured document tag. |
| [setColor(Color value)](#setColor-java.awt.Color-) | Sets the color of the structured document tag. |
| [getStyle()](#getStyle--) | Gets the Style of the structured document tag. |
| [setStyle(Style value)](#setStyle-com.aspose.words.Style-) | Sets the Style of the structured document tag. |
| [getStyleName()](#getStyleName--) | Gets the name of the style applied to the structured document tag. |
| [setStyleName(String value)](#setStyleName-java.lang.String-) | Sets the name of the style applied to the structured document tag. |
| [getXmlMapping()](#getXmlMapping--) | Gets an object that represents the mapping of this structured document tag to XML data in a custom XML part of the current document. |
| [getWordOpenXML()](#getWordOpenXML--) | Gets a string that represents the XML contained within the node in the [SaveFormat.FLAT\_OPC](../../com.aspose.words/saveformat\#FLAT-OPC) format. |
| [getLevel_IMarkupNode()](#getLevel-IMarkupNode--) |  |
| [removeMoveRevisions()](#removeMoveRevisions--) |  |
| [getDirectRunAttr(int key)](#getDirectRunAttr-int-) |  |
| [fetchInheritedRunAttr(int key)](#fetchInheritedRunAttr-int-) |  |
| [setRunAttr(int key, Object value)](#setRunAttr-int-java.lang.Object-) |  |
| [removeRunAttr(int key)](#removeRunAttr-int-) |  |
| [clearRunAttrs()](#clearRunAttrs--) |  |
### StructuredDocumentTag(DocumentBase doc, int type, int level) {#StructuredDocumentTag-com.aspose.words.DocumentBase-int-int-}
```
public StructuredDocumentTag(DocumentBase doc, int type, int level)
```


Initializes a new instance of this class.

**Parameters:**
| Parameter | Type | Description |
| --- | --- | --- |
| doc | [DocumentBase](../../com.aspose.words/documentbase) |  |
| type | int |  |
| level | int |  |

### setCheckedSymbol(int characterCode, String fontName) {#setCheckedSymbol-int-java.lang.String-}
```
public void setCheckedSymbol(int characterCode, String fontName)
```


Sets the symbol used to represent the checked state of a check box content control.

**Parameters:**
| Parameter | Type | Description |
| --- | --- | --- |
| characterCode | int | The character code for the specified symbol. |
| fontName | java.lang.String | The name of the font that contains the symbol.

Accessing this method will only work for [SdtType.CHECKBOX](../../com.aspose.words/sdttype\#CHECKBOX) SDT types.

For all other SDT types exception will occur. |

### setUncheckedSymbol(int characterCode, String fontName) {#setUncheckedSymbol-int-java.lang.String-}
```
public void setUncheckedSymbol(int characterCode, String fontName)
```


Sets the symbol used to represent the unchecked state of a check box content control.

**Parameters:**
| Parameter | Type | Description |
| --- | --- | --- |
| characterCode | int | The character code for the specified symbol. |
| fontName | java.lang.String | The name of the font that contains the symbol.

Accessing this method will only work for [SdtType.CHECKBOX](../../com.aspose.words/sdttype\#CHECKBOX) SDT types.

For all other SDT types exception will occur. |

### removeSelfOnly() {#removeSelfOnly--}
```
public void removeSelfOnly()
```


Removes just this SDT node itself, but keeps the content of it inside the document tree.

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
boolean - True if all nodes were visited; false if DocumentVisitor stopped the operation before visiting all nodes. Calls [DocumentVisitor.visitStructuredDocumentTagStart(com.aspose.words.StructuredDocumentTag)](../../com.aspose.words/documentvisitor\#visitStructuredDocumentTagStart-com.aspose.words.StructuredDocumentTag-), then calls [Node.accept(com.aspose.words.DocumentVisitor)](../../com.aspose.words/node\#accept-com.aspose.words.DocumentVisitor-) for all child nodes of the smart tag and calls [DocumentVisitor.visitStructuredDocumentTagEnd(com.aspose.words.StructuredDocumentTag)](../../com.aspose.words/documentvisitor\#visitStructuredDocumentTagEnd-com.aspose.words.StructuredDocumentTag-) at the end.
### clear() {#clear--}
```
public void clear()
```


Clears contents of this structured document tag and displays a placeholder if it is defined.

It is not possible to clear contents of a structured document tag if it has revisions.

If this structured document tag is mapped to custom XML (with using the [getXmlMapping()](../../com.aspose.words/structureddocumenttag\#getXmlMapping--) property), the referenced XML node is cleared.

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


Returns **NodeType.StructuredDocumentTag**.

**Returns:**
int - **NodeType.StructuredDocumentTag**. The returned value is one of [NodeType](../../com.aspose.words/nodetype) constants.
### getPlaceholder() {#getPlaceholder--}
```
public BuildingBlock getPlaceholder()
```


Gets the [BuildingBlock](../../com.aspose.words/buildingblock) containing placeholder text which should be displayed when this SDT run contents are empty, the associated mapped XML element is empty as specified via the [getXmlMapping()](../../com.aspose.words/structureddocumenttag\#getXmlMapping--) element or the [isShowingPlaceholderText()](../../com.aspose.words/structureddocumenttag\#isShowingPlaceholderText--) / [isShowingPlaceholderText(boolean)](../../com.aspose.words/structureddocumenttag\#isShowingPlaceholderText-boolean-) element is true. Can be null, meaning that the placeholder is not applicable for this Sdt.

**Returns:**
[BuildingBlock](../../com.aspose.words/buildingblock) - The [BuildingBlock](../../com.aspose.words/buildingblock) containing placeholder text which should be displayed when this SDT run contents are empty, the associated mapped XML element is empty as specified via the [getXmlMapping()](../../com.aspose.words/structureddocumenttag\#getXmlMapping--) element or the [isShowingPlaceholderText()](../../com.aspose.words/structureddocumenttag\#isShowingPlaceholderText--) / [isShowingPlaceholderText(boolean)](../../com.aspose.words/structureddocumenttag\#isShowingPlaceholderText-boolean-) element is true.
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

### getLevel() {#getLevel--}
```
public int getLevel()
```


Gets the level at which this **SDT** occurs in the document tree.

**Returns:**
int - The level at which this **SDT** occurs in the document tree. The returned value is one of [MarkupLevel](../../com.aspose.words/markuplevel) constants.
### getSdtType() {#getSdtType--}
```
public int getSdtType()
```


Gets type of this **Structured document tag**.

**Returns:**
int - Type of this **Structured document tag**. The returned value is one of [SdtType](../../com.aspose.words/sdttype) constants.
### getId() {#getId--}
```
public int getId()
```


Specifies a unique read-only persistent numerical Id for this **SDT**.

Id attribute shall follow these rules:

 *  The document shall retain SDT ids only if the whole document is cloned [Document.deepClone()](../../com.aspose.words/document\#deepClone--).
 *  During [DocumentBase.importNode(com.aspose.words.Node, boolean)](../../com.aspose.words/documentbase\#importNode-com.aspose.words.Node--boolean-) Id shall be retained if import does not cause conflicts with other SDT Ids in the target document.
 *  If multiple SDT nodes specify the same decimal number value for the Id attribute, then the first SDT in the document shall maintain this original Id, and all subsequent SDT nodes shall have new identifiers assigned to them when the document is loaded.
 *  During standalone SDT **M:Aspose.Words.Markup.StructuredDocumentTag.Clone(System.Boolean,Aspose.Words.INodeCloningListener)** operation new unique ID will be generated for the cloned SDT node.
 *  If Id is not specified in the source document, then the SDT node shall have a new unique identifier assigned to it when the document is loaded.

**Returns:**
int - The corresponding  int  value.
### getLockContentControl() {#getLockContentControl--}
```
public boolean getLockContentControl()
```


When set to true, this property will prohibit a user from deleting this **SDT**.

**Returns:**
boolean - The corresponding  boolean  value.
### setLockContentControl(boolean value) {#setLockContentControl-boolean-}
```
public void setLockContentControl(boolean value)
```


When set to true, this property will prohibit a user from deleting this **SDT**.

**Parameters:**
| Parameter | Type | Description |
| --- | --- | --- |
| value | boolean | The corresponding  boolean  value. |

### getLockContents() {#getLockContents--}
```
public boolean getLockContents()
```


When set to true, this property will prohibit a user from editing the contents of this **SDT**.

**Returns:**
boolean - The corresponding  boolean  value.
### setLockContents(boolean value) {#setLockContents-boolean-}
```
public void setLockContents(boolean value)
```


When set to true, this property will prohibit a user from editing the contents of this **SDT**.

**Parameters:**
| Parameter | Type | Description |
| --- | --- | --- |
| value | boolean | The corresponding  boolean  value. |

### isShowingPlaceholderText() {#isShowingPlaceholderText--}
```
public boolean isShowingPlaceholderText()
```


Specifies whether the content of this **SDT** shall be interpreted to contain placeholder text (as opposed to regular text contents within the SDT).

if set to true, this state shall be resumed (showing placeholder text) upon opening this document.

**Returns:**
boolean - The corresponding  boolean  value.
### isShowingPlaceholderText(boolean value) {#isShowingPlaceholderText-boolean-}
```
public void isShowingPlaceholderText(boolean value)
```


Specifies whether the content of this **SDT** shall be interpreted to contain placeholder text (as opposed to regular text contents within the SDT).

if set to true, this state shall be resumed (showing placeholder text) upon opening this document.

**Parameters:**
| Parameter | Type | Description |
| --- | --- | --- |
| value | boolean | The corresponding  boolean  value. |

### getTag() {#getTag--}
```
public String getTag()
```


Specifies a tag associated with the current SDT node. Can not be null. A tag is an arbitrary string which applications can associate with SDT in order to identify it without providing a visible friendly name.

**Returns:**
java.lang.String - The corresponding java.lang.String value.
### setTag(String value) {#setTag-java.lang.String-}
```
public void setTag(String value)
```


Specifies a tag associated with the current SDT node. Can not be null. A tag is an arbitrary string which applications can associate with SDT in order to identify it without providing a visible friendly name.

**Parameters:**
| Parameter | Type | Description |
| --- | --- | --- |
| value | java.lang.String | The corresponding java.lang.String value. |

### getContentsFont() {#getContentsFont--}
```
public Font getContentsFont()
```


Font formatting that will be applied to text entered into **SDT**.

**Returns:**
[Font](../../com.aspose.words/font) - The corresponding [Font](../../com.aspose.words/font) value.
### getEndCharacterFont() {#getEndCharacterFont--}
```
public Font getEndCharacterFont()
```


Font formatting that will be applied to the last character of text entered into **SDT**.

**Returns:**
[Font](../../com.aspose.words/font) - The corresponding [Font](../../com.aspose.words/font) value.
### isTemporary() {#isTemporary--}
```
public boolean isTemporary()
```


Specifies whether this **SDT** shall be removed from the WordProcessingML document when its contents are modified.

**Returns:**
boolean - The corresponding  boolean  value.
### isTemporary(boolean value) {#isTemporary-boolean-}
```
public void isTemporary(boolean value)
```


Specifies whether this **SDT** shall be removed from the WordProcessingML document when its contents are modified.

**Parameters:**
| Parameter | Type | Description |
| --- | --- | --- |
| value | boolean | The corresponding  boolean  value. |

### getTitle() {#getTitle--}
```
public String getTitle()
```


Specifies the friendly name associated with this **SDT**. Can not be null.

**Returns:**
java.lang.String - The corresponding java.lang.String value.
### setTitle(String value) {#setTitle-java.lang.String-}
```
public void setTitle(String value)
```


Specifies the friendly name associated with this **SDT**. Can not be null.

**Parameters:**
| Parameter | Type | Description |
| --- | --- | --- |
| value | java.lang.String | The corresponding java.lang.String value. |

### getListItems() {#getListItems--}
```
public SdtListItemCollection getListItems()
```


Gets [SdtListItemCollection](../../com.aspose.words/sdtlistitemcollection) associated with this **SDT**.

Accessing this property will only work for [SdtType.COMBO\_BOX](../../com.aspose.words/sdttype\#COMBO-BOX) or [SdtType.DROP\_DOWN\_LIST](../../com.aspose.words/sdttype\#DROP-DOWN-LIST) SDT types.

For all other SDT types exception will occur.

**Returns:**
[SdtListItemCollection](../../com.aspose.words/sdtlistitemcollection) - \{[SdtListItemCollection](../../com.aspose.words/sdtlistitemcollection) associated with this **SDT**.
### getChecked() {#getChecked--}
```
public boolean getChecked()
```


Gets/Sets current state of the Checkbox **SDT**. Default value for this property is false.

Accessing this property will only work for [SdtType.CHECKBOX](../../com.aspose.words/sdttype\#CHECKBOX) SDT types.

For all other SDT types exception will occur.

**Returns:**
boolean - The corresponding  boolean  value.
### setChecked(boolean value) {#setChecked-boolean-}
```
public void setChecked(boolean value)
```


Gets/Sets current state of the Checkbox **SDT**. Default value for this property is false.

Accessing this property will only work for [SdtType.CHECKBOX](../../com.aspose.words/sdttype\#CHECKBOX) SDT types.

For all other SDT types exception will occur.

**Parameters:**
| Parameter | Type | Description |
| --- | --- | --- |
| value | boolean | The corresponding  boolean  value. |

### getAppearance() {#getAppearance--}
```
public int getAppearance()
```


Gets/sets the appearance of a structured document tag.

**Returns:**
int - The corresponding  int  value. The returned value is one of [SdtAppearance](../../com.aspose.words/sdtappearance) constants.
### setAppearance(int value) {#setAppearance-int-}
```
public void setAppearance(int value)
```


Gets/sets the appearance of a structured document tag.

**Parameters:**
| Parameter | Type | Description |
| --- | --- | --- |
| value | int | The corresponding  int  value. The value must be one of [SdtAppearance](../../com.aspose.words/sdtappearance) constants. |

### getDateDisplayLocale() {#getDateDisplayLocale--}
```
public int getDateDisplayLocale()
```


Allows to set/get the language format for the date displayed in this **SDT**.

Accessing this property will only work for [SdtType.DATE](../../com.aspose.words/sdttype\#DATE) SDT type.

For all other SDT types exception will occur.

**Returns:**
int - The corresponding  int  value.
### setDateDisplayLocale(int value) {#setDateDisplayLocale-int-}
```
public void setDateDisplayLocale(int value)
```


Allows to set/get the language format for the date displayed in this **SDT**.

Accessing this property will only work for [SdtType.DATE](../../com.aspose.words/sdttype\#DATE) SDT type.

For all other SDT types exception will occur.

**Parameters:**
| Parameter | Type | Description |
| --- | --- | --- |
| value | int | The corresponding  int  value. |

### getDateDisplayFormat() {#getDateDisplayFormat--}
```
public String getDateDisplayFormat()
```


String that represents the format in which dates are displayed. Can not be null. The dates for English (U.S.) is "mm/dd/yyyy"

Accessing this property will only work for [SdtType.DATE](../../com.aspose.words/sdttype\#DATE) SDT type.

For all other SDT types exception will occur.

**Returns:**
java.lang.String - The corresponding java.lang.String value.
### setDateDisplayFormat(String value) {#setDateDisplayFormat-java.lang.String-}
```
public void setDateDisplayFormat(String value)
```


String that represents the format in which dates are displayed. Can not be null. The dates for English (U.S.) is "mm/dd/yyyy"

Accessing this property will only work for [SdtType.DATE](../../com.aspose.words/sdttype\#DATE) SDT type.

For all other SDT types exception will occur.

**Parameters:**
| Parameter | Type | Description |
| --- | --- | --- |
| value | java.lang.String | The corresponding java.lang.String value. |

### getFullDate() {#getFullDate--}
```
public Date getFullDate()
```


Specifies the full date and time last entered into this **SDT**.

Accessing this property will only work for [SdtType.DATE](../../com.aspose.words/sdttype\#DATE) SDT type.

For all other SDT types exception will occur.

**Returns:**
java.util.Date - The corresponding java.util.Date value.
### setFullDate(Date value) {#setFullDate-java.util.Date-}
```
public void setFullDate(Date value)
```


Specifies the full date and time last entered into this **SDT**.

Accessing this property will only work for [SdtType.DATE](../../com.aspose.words/sdttype\#DATE) SDT type.

For all other SDT types exception will occur.

**Parameters:**
| Parameter | Type | Description |
| --- | --- | --- |
| value | java.util.Date | The corresponding java.util.Date value. |

### getDateStorageFormat() {#getDateStorageFormat--}
```
public int getDateStorageFormat()
```


Gets/sets format in which the date for a date SDT is stored when the **SDT** is bound to an XML node in the document's data store. Default value is [SdtDateStorageFormat.DATE\_TIME](../../com.aspose.words/sdtdatestorageformat\#DATE-TIME)

Accessing this property will only work for [SdtType.DATE](../../com.aspose.words/sdttype\#DATE) SDT type.

For all other SDT types exception will occur.

**Returns:**
int - The corresponding  int  value. The returned value is one of [SdtDateStorageFormat](../../com.aspose.words/sdtdatestorageformat) constants.
### setDateStorageFormat(int value) {#setDateStorageFormat-int-}
```
public void setDateStorageFormat(int value)
```


Gets/sets format in which the date for a date SDT is stored when the **SDT** is bound to an XML node in the document's data store. Default value is [SdtDateStorageFormat.DATE\_TIME](../../com.aspose.words/sdtdatestorageformat\#DATE-TIME)

Accessing this property will only work for [SdtType.DATE](../../com.aspose.words/sdttype\#DATE) SDT type.

For all other SDT types exception will occur.

**Parameters:**
| Parameter | Type | Description |
| --- | --- | --- |
| value | int | The corresponding  int  value. The value must be one of [SdtDateStorageFormat](../../com.aspose.words/sdtdatestorageformat) constants. |

### getCalendarType() {#getCalendarType--}
```
public int getCalendarType()
```


Specifies the type of calendar for this **SDT**. Default is [SdtCalendarType.DEFAULT](../../com.aspose.words/sdtcalendartype\#DEFAULT)

Accessing this property will only work for [SdtType.DATE](../../com.aspose.words/sdttype\#DATE) SDT type.

For all other SDT types exception will occur.

**Returns:**
int - The corresponding  int  value. The returned value is one of [SdtCalendarType](../../com.aspose.words/sdtcalendartype) constants.
### setCalendarType(int value) {#setCalendarType-int-}
```
public void setCalendarType(int value)
```


Specifies the type of calendar for this **SDT**. Default is [SdtCalendarType.DEFAULT](../../com.aspose.words/sdtcalendartype\#DEFAULT)

Accessing this property will only work for [SdtType.DATE](../../com.aspose.words/sdttype\#DATE) SDT type.

For all other SDT types exception will occur.

**Parameters:**
| Parameter | Type | Description |
| --- | --- | --- |
| value | int | The corresponding  int  value. The value must be one of [SdtCalendarType](../../com.aspose.words/sdtcalendartype) constants. |

### getBuildingBlockGallery() {#getBuildingBlockGallery--}
```
public String getBuildingBlockGallery()
```


Specifies type of building block for this **SDT**. Can not be null.

Accessing this property will only work for [SdtType.BUILDING\_BLOCK\_GALLERY](../../com.aspose.words/sdttype\#BUILDING-BLOCK-GALLERY) and [SdtType.DOC\_PART\_OBJ](../../com.aspose.words/sdttype\#DOC-PART-OBJ) SDT types. It is read-only for **SDT** of the document part type.

For all other SDT types exception will occur.

**Returns:**
java.lang.String - The corresponding java.lang.String value.
### setBuildingBlockGallery(String value) {#setBuildingBlockGallery-java.lang.String-}
```
public void setBuildingBlockGallery(String value)
```


Specifies type of building block for this **SDT**. Can not be null.

Accessing this property will only work for [SdtType.BUILDING\_BLOCK\_GALLERY](../../com.aspose.words/sdttype\#BUILDING-BLOCK-GALLERY) and [SdtType.DOC\_PART\_OBJ](../../com.aspose.words/sdttype\#DOC-PART-OBJ) SDT types. It is read-only for **SDT** of the document part type.

For all other SDT types exception will occur.

**Parameters:**
| Parameter | Type | Description |
| --- | --- | --- |
| value | java.lang.String | The corresponding java.lang.String value. |

### getBuildingBlockCategory() {#getBuildingBlockCategory--}
```
public String getBuildingBlockCategory()
```


Specifies category of building block for this **SDT** node. Can not be null.

Accessing this property will only work for [SdtType.BUILDING\_BLOCK\_GALLERY](../../com.aspose.words/sdttype\#BUILDING-BLOCK-GALLERY) and [SdtType.DOC\_PART\_OBJ](../../com.aspose.words/sdttype\#DOC-PART-OBJ) SDT types. It is read-only for **SDT** of the document part type.

For all other SDT types exception will occur.

**Returns:**
java.lang.String - The corresponding java.lang.String value.
### setBuildingBlockCategory(String value) {#setBuildingBlockCategory-java.lang.String-}
```
public void setBuildingBlockCategory(String value)
```


Specifies category of building block for this **SDT** node. Can not be null.

Accessing this property will only work for [SdtType.BUILDING\_BLOCK\_GALLERY](../../com.aspose.words/sdttype\#BUILDING-BLOCK-GALLERY) and [SdtType.DOC\_PART\_OBJ](../../com.aspose.words/sdttype\#DOC-PART-OBJ) SDT types. It is read-only for **SDT** of the document part type.

For all other SDT types exception will occur.

**Parameters:**
| Parameter | Type | Description |
| --- | --- | --- |
| value | java.lang.String | The corresponding java.lang.String value. |

### getMultiline() {#getMultiline--}
```
public boolean getMultiline()
```


Specifies whether this **SDT** allows multiple lines of text.

Accessing this property will only work for [SdtType.RICH\_TEXT](../../com.aspose.words/sdttype\#RICH-TEXT) and [SdtType.PLAIN\_TEXT](../../com.aspose.words/sdttype\#PLAIN-TEXT) SDT type.

For all other SDT types exception will occur.

**Returns:**
boolean - The corresponding  boolean  value.
### setMultiline(boolean value) {#setMultiline-boolean-}
```
public void setMultiline(boolean value)
```


Specifies whether this **SDT** allows multiple lines of text.

Accessing this property will only work for [SdtType.RICH\_TEXT](../../com.aspose.words/sdttype\#RICH-TEXT) and [SdtType.PLAIN\_TEXT](../../com.aspose.words/sdttype\#PLAIN-TEXT) SDT type.

For all other SDT types exception will occur.

**Parameters:**
| Parameter | Type | Description |
| --- | --- | --- |
| value | boolean | The corresponding  boolean  value. |

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

### getStyle() {#getStyle--}
```
public Style getStyle()
```


Gets the Style of the structured document tag. Only [StyleType.CHARACTER](../../com.aspose.words/styletype\#CHARACTER) style or [StyleType.PARAGRAPH](../../com.aspose.words/styletype\#PARAGRAPH) style with linked character style can be set.

**Returns:**
[Style](../../com.aspose.words/style) - The Style of the structured document tag.
### setStyle(Style value) {#setStyle-com.aspose.words.Style-}
```
public void setStyle(Style value)
```


Sets the Style of the structured document tag. Only [StyleType.CHARACTER](../../com.aspose.words/styletype\#CHARACTER) style or [StyleType.PARAGRAPH](../../com.aspose.words/styletype\#PARAGRAPH) style with linked character style can be set.

**Parameters:**
| Parameter | Type | Description |
| --- | --- | --- |
| value | [Style](../../com.aspose.words/style) | The Style of the structured document tag. |

### getStyleName() {#getStyleName--}
```
public String getStyleName()
```


Gets the name of the style applied to the structured document tag.

**Returns:**
java.lang.String - The name of the style applied to the structured document tag.
### setStyleName(String value) {#setStyleName-java.lang.String-}
```
public void setStyleName(String value)
```


Sets the name of the style applied to the structured document tag.

**Parameters:**
| Parameter | Type | Description |
| --- | --- | --- |
| value | java.lang.String | The name of the style applied to the structured document tag. |

### getXmlMapping() {#getXmlMapping--}
```
public XmlMapping getXmlMapping()
```


Gets an object that represents the mapping of this structured document tag to XML data in a custom XML part of the current document. You can use the [XmlMapping.setMapping(com.aspose.words.CustomXmlPart, java.lang.String, java.lang.String)](../../com.aspose.words/xmlmapping\#setMapping-com.aspose.words.CustomXmlPart--java.lang.String--java.lang.String-) method of this object to map a structured document tag to XML data.

**Returns:**
[XmlMapping](../../com.aspose.words/xmlmapping) - An object that represents the mapping of this structured document tag to XML data in a custom XML part of the current document.
### getWordOpenXML() {#getWordOpenXML--}
```
public String getWordOpenXML()
```


Gets a string that represents the XML contained within the node in the [SaveFormat.FLAT\_OPC](../../com.aspose.words/saveformat\#FLAT-OPC) format.

**Returns:**
java.lang.String - A string that represents the XML contained within the node in the [SaveFormat.FLAT\_OPC](../../com.aspose.words/saveformat\#FLAT-OPC) format.
### getLevel_IMarkupNode() {#getLevel-IMarkupNode--}
```
public int getLevel_IMarkupNode()
```




**Returns:**
int
### removeMoveRevisions() {#removeMoveRevisions--}
```
public void removeMoveRevisions()
```




### getDirectRunAttr(int key) {#getDirectRunAttr-int-}
```
public Object getDirectRunAttr(int key)
```




**Parameters:**
| Parameter | Type | Description |
| --- | --- | --- |
| key | int |  |

**Returns:**
java.lang.Object
### fetchInheritedRunAttr(int key) {#fetchInheritedRunAttr-int-}
```
public Object fetchInheritedRunAttr(int key)
```




**Parameters:**
| Parameter | Type | Description |
| --- | --- | --- |
| key | int |  |

**Returns:**
java.lang.Object
### setRunAttr(int key, Object value) {#setRunAttr-int-java.lang.Object-}
```
public void setRunAttr(int key, Object value)
```




**Parameters:**
| Parameter | Type | Description |
| --- | --- | --- |
| key | int |  |
| value | java.lang.Object |  |

### removeRunAttr(int key) {#removeRunAttr-int-}
```
public void removeRunAttr(int key)
```




**Parameters:**
| Parameter | Type | Description |
| --- | --- | --- |
| key | int |  |

### clearRunAttrs() {#clearRunAttrs--}
```
public void clearRunAttrs()
```




