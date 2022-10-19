---
title: EditableRangeEnd
second_title: Aspose.Words for Java API Reference
description: Represents an end of an editable range in a Word document.
type: docs
weight: 137
url: /java/com.aspose.words/editablerangeend/
---

**Inheritance:**
java.lang.Object, [com.aspose.words.Node](../../com.aspose.words/node)
```
public class EditableRangeEnd extends Node
```

Represents an end of an editable range in a Word document.

To learn more, visit the **Aspose.Words Document Object Model (DOM)** documentation article.

A complete editable range in a Word document consists of a [getEditableRangeStart()](../../com.aspose.words/editablerangeend\#getEditableRangeStart--) and a matching [EditableRangeEnd](../../com.aspose.words/editablerangeend) with the same Id.

[getEditableRangeStart()](../../com.aspose.words/editablerangeend\#getEditableRangeStart--) and [EditableRangeEnd](../../com.aspose.words/editablerangeend) are just markers inside a document that specify where the editable range starts and ends.

Use the [EditableRange](../../com.aspose.words/editablerange) class as a "facade" to work with an editable range as a single object.

Currently editable ranges are supported only at the inline-level, that is inside [Paragraph](../../com.aspose.words/paragraph), but editable range start and editable range end can be in different paragraphs.
## Methods

| Method | Description |
| --- | --- |
| [getEditableRangeStart()](#getEditableRangeStart--) | Corresponding EditableRangeStart, received by ID. |
| [accept(DocumentVisitor visitor)](#accept-com.aspose.words.DocumentVisitor-) | Accepts a visitor. |
| [getId()](#getId--) | Specifies the identifier of the editable range. |
| [setId(int value)](#setId-int-) | Specifies the identifier of the editable range. |
| [getNodeType()](#getNodeType--) | Returns [NodeType.EDITABLE\_RANGE\_END](../../com.aspose.words/nodetype\#EDITABLE-RANGE-END). |
| [getDisplacedByCustomXml()](#getDisplacedByCustomXml--) |  |
| [setDisplacedByCustomXml(int value)](#setDisplacedByCustomXml-int-) |  |
| [getIdInternal()](#getIdInternal--) |  |
| [setIdInternal(int value)](#setIdInternal-int-) |  |
| [getParentIdInternal()](#getParentIdInternal--) |  |
| [setParentIdInternal(int value)](#setParentIdInternal-int-) |  |
### getEditableRangeStart() {#getEditableRangeStart--}
```
public EditableRangeStart getEditableRangeStart()
```


Corresponding EditableRangeStart, received by ID.

**Returns:**
[EditableRangeStart](../../com.aspose.words/editablerangestart) - The corresponding [EditableRangeStart](../../com.aspose.words/editablerangestart) value.
### accept(DocumentVisitor visitor) {#accept-com.aspose.words.DocumentVisitor-}
```
public boolean accept(DocumentVisitor visitor)
```


Accepts a visitor.

Calls [DocumentVisitor.visitEditableRangeEnd(com.aspose.words.EditableRangeEnd)](../../com.aspose.words/documentvisitor\#visitEditableRangeEnd-com.aspose.words.EditableRangeEnd-).

For more info see the Visitor design pattern.

**Parameters:**
| Parameter | Type | Description |
| --- | --- | --- |
| visitor | [DocumentVisitor](../../com.aspose.words/documentvisitor) | The visitor that will visit the node. |

**Returns:**
boolean - False if the visitor requested the enumeration to stop.
### getId() {#getId--}
```
public int getId()
```


Specifies the identifier of the editable range.

**Returns:**
int - The corresponding  int  value.
### setId(int value) {#setId-int-}
```
public void setId(int value)
```


Specifies the identifier of the editable range.

**Parameters:**
| Parameter | Type | Description |
| --- | --- | --- |
| value | int | The corresponding  int  value. |

### getNodeType() {#getNodeType--}
```
public int getNodeType()
```


Returns [NodeType.EDITABLE\_RANGE\_END](../../com.aspose.words/nodetype\#EDITABLE-RANGE-END).

**Returns:**
int - \{[NodeType.EDITABLE\_RANGE\_END](../../com.aspose.words/nodetype\#EDITABLE-RANGE-END). The returned value is one of [NodeType](../../com.aspose.words/nodetype) constants.
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

