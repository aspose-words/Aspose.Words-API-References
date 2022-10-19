---
title: EditableRangeStart
second_title: Aspose.Words for Java API Reference
description: Represents a start of an editable range in a Word document.
type: docs
weight: 138
url: /java/com.aspose.words/editablerangestart/
---

**Inheritance:**
java.lang.Object, [com.aspose.words.Node](../../com.aspose.words/node)
```
public class EditableRangeStart extends Node
```

Represents a start of an editable range in a Word document.

To learn more, visit the **Aspose.Words Document Object Model (DOM)** documentation article.

A complete editable range in a Word document consists of a [EditableRangeStart](../../com.aspose.words/editablerangestart) and a matching [EditableRangeEnd](../../com.aspose.words/editablerangeend) with the same Id.

[EditableRangeStart](../../com.aspose.words/editablerangestart) and [EditableRangeEnd](../../com.aspose.words/editablerangeend) are just markers inside a document that specify where the editable range starts and ends.

Use the [getEditableRange()](../../com.aspose.words/editablerangestart\#getEditableRange--) class as a "facade" to work with an editable range as a single object.

Currently editable ranges are supported only at the inline-level, that is inside [Paragraph](../../com.aspose.words/paragraph), but editable range start and editable range end can be in different paragraphs.
## Methods

| Method | Description |
| --- | --- |
| [accept(DocumentVisitor visitor)](#accept-com.aspose.words.DocumentVisitor-) | Accepts a visitor. |
| [getId()](#getId--) | Specifies the identifier of the editable range. |
| [setId(int value)](#setId-int-) | Specifies the identifier of the editable range. |
| [getEditableRange()](#getEditableRange--) | Gets the facade object that encapsulates this editable range start and end. |
| [getNodeType()](#getNodeType--) | Returns [NodeType.EDITABLE\_RANGE\_START](../../com.aspose.words/nodetype\#EDITABLE-RANGE-START). |
| [getDisplacedByCustomXml()](#getDisplacedByCustomXml--) |  |
| [setDisplacedByCustomXml(int value)](#setDisplacedByCustomXml-int-) |  |
| [getIdInternal()](#getIdInternal--) |  |
| [setIdInternal(int value)](#setIdInternal-int-) |  |
| [getParentIdInternal()](#getParentIdInternal--) |  |
| [setParentIdInternal(int value)](#setParentIdInternal-int-) |  |
### accept(DocumentVisitor visitor) {#accept-com.aspose.words.DocumentVisitor-}
```
public boolean accept(DocumentVisitor visitor)
```


Accepts a visitor.

Calls [DocumentVisitor.visitEditableRangeStart(com.aspose.words.EditableRangeStart)](../../com.aspose.words/documentvisitor\#visitEditableRangeStart-com.aspose.words.EditableRangeStart-).

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

### getEditableRange() {#getEditableRange--}
```
public EditableRange getEditableRange()
```


Gets the facade object that encapsulates this editable range start and end.

**Returns:**
[EditableRange](../../com.aspose.words/editablerange) - The facade object that encapsulates this editable range start and end.
### getNodeType() {#getNodeType--}
```
public int getNodeType()
```


Returns [NodeType.EDITABLE\_RANGE\_START](../../com.aspose.words/nodetype\#EDITABLE-RANGE-START).

**Returns:**
int - \{[NodeType.EDITABLE\_RANGE\_START](../../com.aspose.words/nodetype\#EDITABLE-RANGE-START). The returned value is one of [NodeType](../../com.aspose.words/nodetype) constants.
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

