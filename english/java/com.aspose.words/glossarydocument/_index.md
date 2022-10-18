---
title: GlossaryDocument
second_title: Aspose.Words for Java API Reference
description: Represents the root element for a glossary document within a Word document.
type: docs
weight: 306
url: /java/com.aspose.words/glossarydocument/
---

**Inheritance:**
java.lang.Object, [com.aspose.words.Node](../../com.aspose.words/node), [com.aspose.words.CompositeNode](../../com.aspose.words/compositenode), [com.aspose.words.DocumentBase](../../com.aspose.words/documentbase)
```
public class GlossaryDocument extends DocumentBase
```

Represents the root element for a glossary document within a Word document. A glossary document is a storage for AutoText, AutoCorrect entries and Building Blocks.

To learn more, visit the **Aspose.Words Document Object Model (DOM)** documentation article.

Some documents, usually templates, can contain AutoText, AutoCorrect entries and/or Building Blocks (also known as *glossary document entries*, *document parts* or *building blocks*).

To access building blocks, you need to load a document into a [Document](../../com.aspose.words/document) object. Building blocks will be available via the [Document.getGlossaryDocument()](../../com.aspose.words/document\#getGlossaryDocument--) / [Document.setGlossaryDocument(com.aspose.words.GlossaryDocument)](../../com.aspose.words/document\#setGlossaryDocument-com.aspose.words.GlossaryDocument-) property.

[GlossaryDocument](../../com.aspose.words/glossarydocument) can contain any number of [BuildingBlock](../../com.aspose.words/buildingblock) objects. Each [BuildingBlock](../../com.aspose.words/buildingblock) represents one document part.

Corresponds to the **glossaryDocument** and **docParts** elements in OOXML.
## Methods

| Method | Description |
| --- | --- |
| [getNodeType()](#getNodeType--) | Returns the [NodeType.GLOSSARY\_DOCUMENT](../../com.aspose.words/nodetype\#GLOSSARY-DOCUMENT) value. |
| [getBuildingBlocks()](#getBuildingBlocks--) | Returns a typed collection that represents all building blocks in the glossary document. |
| [getFirstBuildingBlock()](#getFirstBuildingBlock--) | Gets the first building block in the glossary document. |
| [getLastBuildingBlock()](#getLastBuildingBlock--) | Gets the last building block in the glossary document. |
| [accept(DocumentVisitor visitor)](#accept-com.aspose.words.DocumentVisitor-) | Accepts a visitor. |
| [getBuildingBlock(int gallery, String category, String name)](#getBuildingBlock-int-java.lang.String-java.lang.String-) |  |
### getNodeType() {#getNodeType--}
```
public int getNodeType()
```


Returns the [NodeType.GLOSSARY\_DOCUMENT](../../com.aspose.words/nodetype\#GLOSSARY-DOCUMENT) value.

**Returns:**
int - The [NodeType.GLOSSARY\_DOCUMENT](../../com.aspose.words/nodetype\#GLOSSARY-DOCUMENT) value. The returned value is one of [NodeType](../../com.aspose.words/nodetype) constants.
### getBuildingBlocks() {#getBuildingBlocks--}
```
public BuildingBlockCollection getBuildingBlocks()
```


Returns a typed collection that represents all building blocks in the glossary document.

**Returns:**
[BuildingBlockCollection](../../com.aspose.words/buildingblockcollection) - A typed collection that represents all building blocks in the glossary document.
### getFirstBuildingBlock() {#getFirstBuildingBlock--}
```
public BuildingBlock getFirstBuildingBlock()
```


Gets the first building block in the glossary document. Returns  null  if there are no building blocks available.

**Returns:**
[BuildingBlock](../../com.aspose.words/buildingblock) - The first building block in the glossary document.
### getLastBuildingBlock() {#getLastBuildingBlock--}
```
public BuildingBlock getLastBuildingBlock()
```


Gets the last building block in the glossary document. Returns  null  if there are no building blocks available.

**Returns:**
[BuildingBlock](../../com.aspose.words/buildingblock) - The last building block in the glossary document.
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

Calls [DocumentVisitor.visitGlossaryDocumentStart(com.aspose.words.GlossaryDocument)](../../com.aspose.words/documentvisitor\#visitGlossaryDocumentStart-com.aspose.words.GlossaryDocument-), then calls [Node.accept(com.aspose.words.DocumentVisitor)](../../com.aspose.words/node\#accept-com.aspose.words.DocumentVisitor-) for all child nodes of this node and then calls [DocumentVisitor.visitGlossaryDocumentEnd(com.aspose.words.GlossaryDocument)](../../com.aspose.words/documentvisitor\#visitGlossaryDocumentEnd-com.aspose.words.GlossaryDocument-) at the end.

Note: A glossary document node and its children are not visited when you execute a Visitor over a [Document](../../com.aspose.words/document). If you want to execute a Visitor over a glossary document, you need to call [accept(com.aspose.words.DocumentVisitor)](../../com.aspose.words/glossarydocument\#accept-com.aspose.words.DocumentVisitor-).
### getBuildingBlock(int gallery, String category, String name) {#getBuildingBlock-int-java.lang.String-java.lang.String-}
```
public BuildingBlock getBuildingBlock(int gallery, String category, String name)
```




**Parameters:**
| Parameter | Type | Description |
| --- | --- | --- |
| gallery | int |  |
| category | java.lang.String |  |
| name | java.lang.String |  |

**Returns:**
[BuildingBlock](../../com.aspose.words/buildingblock)
