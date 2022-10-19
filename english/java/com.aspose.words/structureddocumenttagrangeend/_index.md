---
title: StructuredDocumentTagRangeEnd
second_title: Aspose.Words for Java API Reference
description: Represents an end of ranged structured document tag which accepts multi-sections content.
type: docs
weight: 534
url: /java/com.aspose.words/structureddocumenttagrangeend/
---

**Inheritance:**
java.lang.Object, [com.aspose.words.Node](../../com.aspose.words/node)
```
public class StructuredDocumentTagRangeEnd extends Node
```

Represents an end of **ranged** structured document tag which accepts multi-sections content. See also [StructuredDocumentTagRangeStart](../../com.aspose.words/structureddocumenttagrangestart) node.

To learn more, visit the **Structured Document Tags or Content Control** documentation article.

Can be immediate child of [Body](../../com.aspose.words/body) node **only**.
## Constructors

| Constructor | Description |
| --- | --- |
| [StructuredDocumentTagRangeEnd(DocumentBase doc, int id)](#StructuredDocumentTagRangeEnd-com.aspose.words.DocumentBase-int-) | Initializes a new instance of the **Structured document tag range end** class. |
## Methods

| Method | Description |
| --- | --- |
| [getNodeType()](#getNodeType--) |  |
| [accept(DocumentVisitor visitor)](#accept-com.aspose.words.DocumentVisitor-) |  |
| [getId()](#getId--) | Specifies a unique read-only persistent numerical Id for this **StructuredDocumentTagRange** node. |
### StructuredDocumentTagRangeEnd(DocumentBase doc, int id) {#StructuredDocumentTagRangeEnd-com.aspose.words.DocumentBase-int-}
```
public StructuredDocumentTagRangeEnd(DocumentBase doc, int id)
```


Initializes a new instance of the **Structured document tag range end** class.

**Parameters:**
| Parameter | Type | Description |
| --- | --- | --- |
| doc | [DocumentBase](../../com.aspose.words/documentbase) | The owner document. |
| id | int | Identifier of the corresponding structured document tag range start. |

### getNodeType() {#getNodeType--}
```
public int getNodeType()
```


Gets the type of this node.

**Returns:**
int
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
### getId() {#getId--}
```
public int getId()
```


Specifies a unique read-only persistent numerical Id for this **StructuredDocumentTagRange** node. Corresponding [StructuredDocumentTagRangeStart](../../com.aspose.words/structureddocumenttagrangestart) node has the same [StructuredDocumentTagRangeStart.getId()](../../com.aspose.words/structureddocumenttagrangestart\#getId--).

**Returns:**
int - The corresponding  int  value.
