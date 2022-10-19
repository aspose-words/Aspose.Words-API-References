---
title: SubDocument
second_title: Aspose.Words for Java API Reference
description: Represents a SubDocument - which is a reference to an externally stored document.
type: docs
weight: 540
url: /java/com.aspose.words/subdocument/
---

**Inheritance:**
java.lang.Object, [com.aspose.words.Node](../../com.aspose.words/node)
```
public class SubDocument extends Node
```

Represents a **SubDocument** \- which is a reference to an externally stored document.

To learn more, visit the **Aspose.Words Document Object Model (DOM)** documentation article.

In this version of Aspose.Words, [SubDocument](../../com.aspose.words/subdocument) nodes do not provide public methods and properties to create or modify a subdocument. In this version you are not able to instantiate SubDocument nodes or modify existing except deleting them.

[SubDocument](../../com.aspose.words/subdocument) can only be a child of [Paragraph](../../com.aspose.words/paragraph).
## Methods

| Method | Description |
| --- | --- |
| [getNodeType()](#getNodeType--) | Returns **NodeType.SubDocument** |
| [accept(DocumentVisitor visitor)](#accept-com.aspose.words.DocumentVisitor-) | Accepts a visitor. |
### getNodeType() {#getNodeType--}
```
public int getNodeType()
```


Returns **NodeType.SubDocument**

**Returns:**
int - **NodeType.SubDocument** The returned value is one of [NodeType](../../com.aspose.words/nodetype) constants.
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
