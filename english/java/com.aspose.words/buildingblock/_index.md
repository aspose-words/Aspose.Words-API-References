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
| [getNodeType()](#getNodeType--) | Returns the [NodeType.BUILDING\_BLOCK](../../com.aspose.words/nodetype\#BUILDING-BLOCK) value. |
| [accept(DocumentVisitor visitor)](#accept-com.aspose.words.DocumentVisitor-) | Accepts a visitor. |
| [getSections()](#getSections--) | Returns a collection that represents all sections in the building block. |
| [getFirstSection()](#getFirstSection--) | Gets the first section in the building block. |
| [getLastSection()](#getLastSection--) | Gets the last section in the building block. |
| [getName()](#getName--) | Gets the name of this building block. |
| [setName(String value)](#setName-java.lang.String-) | Sets the name of this building block. |
| [getGuid()](#getGuid--) | Gets an identifier (a 128-bit GUID) that uniquely identifies this building block. |
| [setGuid(UUID value)](#setGuid-java.util.UUID-) | Sets an identifier (a 128-bit GUID) that uniquely identifies this building block. |
| [getDescription()](#getDescription--) | Gets the description associated with this building block. |
| [setDescription(String value)](#setDescription-java.lang.String-) | Sets the description associated with this building block. |
| [getGallery()](#getGallery--) | Specifies the first-level categorization for the building block for the purposes of classification or user interface sorting. |
| [setGallery(int value)](#setGallery-int-) | Specifies the first-level categorization for the building block for the purposes of classification or user interface sorting. |
| [getCategory()](#getCategory--) | Specifies the second-level categorization for the building block. |
| [setCategory(String value)](#setCategory-java.lang.String-) | Specifies the second-level categorization for the building block. |
| [getBehavior()](#getBehavior--) | Specifies the behavior that shall be applied when the contents of the building block is inserted into the main document. |
| [setBehavior(int value)](#setBehavior-int-) | Specifies the behavior that shall be applied when the contents of the building block is inserted into the main document. |
| [getType()](#getType--) | Specifies the building block type. |
| [setType(int value)](#setType-int-) | Specifies the building block type. |
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

### getNodeType() {#getNodeType--}
```
public int getNodeType()
```


Returns the [NodeType.BUILDING\_BLOCK](../../com.aspose.words/nodetype\#BUILDING-BLOCK) value.

**Returns:**
int - The [NodeType.BUILDING\_BLOCK](../../com.aspose.words/nodetype\#BUILDING-BLOCK) value. The returned value is one of [NodeType](../../com.aspose.words/nodetype) constants.
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
### getSections() {#getSections--}
```
public SectionCollection getSections()
```


Returns a collection that represents all sections in the building block.

**Returns:**
[SectionCollection](../../com.aspose.words/sectioncollection) - A collection that represents all sections in the building block.
### getFirstSection() {#getFirstSection--}
```
public Section getFirstSection()
```


Gets the first section in the building block. Returns  null  if there are no sections.

**Returns:**
[Section](../../com.aspose.words/section) - The first section in the building block.
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

### getGuid() {#getGuid--}
```
public UUID getGuid()
```


Gets an identifier (a 128-bit GUID) that uniquely identifies this building block.

Can be used by an application to uniquely reference a building block regardless of different naming due to localization.

Corresponds to the **docPartPr.guid** element in OOXML.

**Returns:**
java.util.UUID - An identifier (a 128-bit GUID) that uniquely identifies this building block.
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

### getGallery() {#getGallery--}
```
public int getGallery()
```


Specifies the first-level categorization for the building block for the purposes of classification or user interface sorting.

Building blocks in Microsoft Word user interface are arranged into Galleries. Each [getGallery()](../../com.aspose.words/buildingblock\#getGallery--) / [setGallery(int)](../../com.aspose.words/buildingblock\#setGallery-int-) can have multiple Categories. Each block within a [getCategory()](../../com.aspose.words/buildingblock\#getCategory--) / [setCategory(java.lang.String)](../../com.aspose.words/buildingblock\#setCategory-java.lang.String-) has a [getName()](../../com.aspose.words/buildingblock\#getName--) / [setName(java.lang.String)](../../com.aspose.words/buildingblock\#setName-java.lang.String-).

Corresponds to the **docPartPr.category.gallery** element in OOXML.

**Returns:**
int - The corresponding  int  value. The returned value is one of [BuildingBlockGallery](../../com.aspose.words/buildingblockgallery) constants.
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

### getBehavior() {#getBehavior--}
```
public int getBehavior()
```


Specifies the behavior that shall be applied when the contents of the building block is inserted into the main document.

**Returns:**
int - The corresponding  int  value. The returned value is one of [BuildingBlockBehavior](../../com.aspose.words/buildingblockbehavior) constants.
### setBehavior(int value) {#setBehavior-int-}
```
public void setBehavior(int value)
```


Specifies the behavior that shall be applied when the contents of the building block is inserted into the main document.

**Parameters:**
| Parameter | Type | Description |
| --- | --- | --- |
| value | int | The corresponding  int  value. The value must be one of [BuildingBlockBehavior](../../com.aspose.words/buildingblockbehavior) constants. |

### getType() {#getType--}
```
public int getType()
```


Specifies the building block type.

The building block type can influence the visibility and behavior of the building block in Microsoft Word.

Corresponds to the **docPartPr.types** element in OOXML.

**Returns:**
int - The corresponding  int  value. The returned value is one of [BuildingBlockType](../../com.aspose.words/buildingblocktype) constants.
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

