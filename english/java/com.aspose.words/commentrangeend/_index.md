---
title: CommentRangeEnd
second_title: Aspose.Words for Java API Reference
description: Denotes the end of a region of text that has a comment associated with it.
type: docs
weight: 79
url: /java/com.aspose.words/commentrangeend/
---

**Inheritance:**
java.lang.Object, [com.aspose.words.Node](../../com.aspose.words/node)
```
public class CommentRangeEnd extends Node
```

Denotes the end of a region of text that has a comment associated with it.

To learn more, visit the **Working with Comments** documentation article.

To create a comment anchored to a region of text, you need to create a [Comment](../../com.aspose.words/comment) and then create [CommentRangeStart](../../com.aspose.words/commentrangestart) and [CommentRangeEnd](../../com.aspose.words/commentrangeend) and set their identifiers to the same [Comment.getId()](../../com.aspose.words/comment\#getId--) value.

[CommentRangeEnd](../../com.aspose.words/commentrangeend) is an inline-level node and can only be a child of [Paragraph](../../com.aspose.words/paragraph).
## Constructors

| Constructor | Description |
| --- | --- |
| [CommentRangeEnd(DocumentBase doc, int id)](#CommentRangeEnd-com.aspose.words.DocumentBase-int-) | Initializes a new instance of this class. |
## Methods

| Method | Description |
| --- | --- |
| [getId()](#getId--) | Specifies the identifier of the comment to which this region is linked to. |
| [setId(int value)](#setId-int-) | Specifies the identifier of the comment to which this region is linked to. |
| [getDisplacedByCustomXml()](#getDisplacedByCustomXml--) |  |
| [setDisplacedByCustomXml(int value)](#setDisplacedByCustomXml-int-) |  |
| [getIdInternal()](#getIdInternal--) |  |
| [setIdInternal(int value)](#setIdInternal-int-) |  |
| [getParentIdInternal()](#getParentIdInternal--) |  |
| [setParentIdInternal(int value)](#setParentIdInternal-int-) |  |
| [getNodeType()](#getNodeType--) | Returns [NodeType.COMMENT\_RANGE\_END](../../com.aspose.words/nodetype\#COMMENT-RANGE-END). |
| [accept(DocumentVisitor visitor)](#accept-com.aspose.words.DocumentVisitor-) | Accepts a visitor. |
### CommentRangeEnd(DocumentBase doc, int id) {#CommentRangeEnd-com.aspose.words.DocumentBase-int-}
```
public CommentRangeEnd(DocumentBase doc, int id)
```


Initializes a new instance of this class.

When [CommentRangeEnd](../../com.aspose.words/commentrangeend) is created, it belongs to the specified document, but is not yet part of the document and [Node.getParentNode()](../../com.aspose.words/node\#getParentNode--) is null.

To append a [CommentRangeEnd](../../com.aspose.words/commentrangeend) to the document use InsertAfter or InsertBefore on the paragraph where you want the comment inserted.

**Parameters:**
| Parameter | Type | Description |
| --- | --- | --- |
| doc | [DocumentBase](../../com.aspose.words/documentbase) | The owner document. |
| id | int | The comment identifier to which this object is linked. |

### getId() {#getId--}
```
public int getId()
```


Specifies the identifier of the comment to which this region is linked to.

**Returns:**
int - The corresponding  int  value.
### setId(int value) {#setId-int-}
```
public void setId(int value)
```


Specifies the identifier of the comment to which this region is linked to.

**Parameters:**
| Parameter | Type | Description |
| --- | --- | --- |
| value | int | The corresponding  int  value. |

### getDisplacedByCustomXml() {#getDisplacedByCustomXml--}
```
public int getDisplacedByCustomXml()
```




**Returns:**
int
### setDisplacedByCustomXml(int value) {#setDisplacedByCustomXml-int-}
```
public void setDisplacedByCustomXml(int value)
```




**Parameters:**
| Parameter | Type | Description |
| --- | --- | --- |
| value | int |  |

### getIdInternal() {#getIdInternal--}
```
public int getIdInternal()
```




**Returns:**
int
### setIdInternal(int value) {#setIdInternal-int-}
```
public void setIdInternal(int value)
```




**Parameters:**
| Parameter | Type | Description |
| --- | --- | --- |
| value | int |  |

### getParentIdInternal() {#getParentIdInternal--}
```
public int getParentIdInternal()
```




**Returns:**
int
### setParentIdInternal(int value) {#setParentIdInternal-int-}
```
public void setParentIdInternal(int value)
```




**Parameters:**
| Parameter | Type | Description |
| --- | --- | --- |
| value | int |  |

### getNodeType() {#getNodeType--}
```
public int getNodeType()
```


Returns [NodeType.COMMENT\_RANGE\_END](../../com.aspose.words/nodetype\#COMMENT-RANGE-END).

**Returns:**
int - \{[NodeType.COMMENT\_RANGE\_END](../../com.aspose.words/nodetype\#COMMENT-RANGE-END). The returned value is one of [NodeType](../../com.aspose.words/nodetype) constants.
### accept(DocumentVisitor visitor) {#accept-com.aspose.words.DocumentVisitor-}
```
public boolean accept(DocumentVisitor visitor)
```


Accepts a visitor.

Calls [DocumentVisitor.visitCommentRangeEnd(com.aspose.words.CommentRangeEnd)](../../com.aspose.words/documentvisitor\#visitCommentRangeEnd-com.aspose.words.CommentRangeEnd-).

For more info see the Visitor design pattern.

**Parameters:**
| Parameter | Type | Description |
| --- | --- | --- |
| visitor | [DocumentVisitor](../../com.aspose.words/documentvisitor) | The visitor that will visit the node. |

**Returns:**
boolean - False if the visitor requested the enumeration to stop.