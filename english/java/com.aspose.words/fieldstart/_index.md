---
title: FieldStart
second_title: Aspose.Words for Java API Reference
description: Represents a start of a Word field in a document.
type: docs
weight: 245
url: /java/com.aspose.words/fieldstart/
---

**Inheritance:**
java.lang.Object, [com.aspose.words.Node](../../com.aspose.words/node), [com.aspose.words.Inline](../../com.aspose.words/inline), [com.aspose.words.SpecialChar](../../com.aspose.words/specialchar), [com.aspose.words.FieldChar](../../com.aspose.words/fieldchar)
```
public class FieldStart extends FieldChar
```

Represents a start of a Word field in a document.

To learn more, visit the **Working with Fields** documentation article.

[FieldStart](../../com.aspose.words/fieldstart) is an inline-level node and represented by the [ControlChar.FIELD\_START\_CHAR](../../com.aspose.words/controlchar\#FIELD-START-CHAR) control character in the document.

[FieldStart](../../com.aspose.words/fieldstart) can only be a child of [Paragraph](../../com.aspose.words/paragraph).

A complete field in a Microsoft Word document is a complex structure consisting of a field start character, field code, field separator character, field result and field end character. Some fields only have field start, field code and field end.

To easily insert a new field into a document, use the [DocumentBuilder.insertField(java.lang.String)](../../com.aspose.words/documentbuilder\#insertField-java.lang.String-) method.
## Methods

| Method | Description |
| --- | --- |
| [getNodeType()](#getNodeType--) | Returns [NodeType.FIELD\_START](../../com.aspose.words/nodetype\#FIELD-START). |
| [accept(DocumentVisitor visitor)](#accept-com.aspose.words.DocumentVisitor-) | Accepts a visitor. |
| [getFieldData()](#getFieldData--) | Gets custom field data which is associated with the field. |
### getNodeType() {#getNodeType--}
```
public int getNodeType()
```


Returns [NodeType.FIELD\_START](../../com.aspose.words/nodetype\#FIELD-START).

**Returns:**
int - \{[NodeType.FIELD\_START](../../com.aspose.words/nodetype\#FIELD-START). The returned value is one of [NodeType](../../com.aspose.words/nodetype) constants.
### accept(DocumentVisitor visitor) {#accept-com.aspose.words.DocumentVisitor-}
```
public boolean accept(DocumentVisitor visitor)
```


Accepts a visitor.

Calls [DocumentVisitor.visitFieldStart(com.aspose.words.FieldStart)](../../com.aspose.words/documentvisitor\#visitFieldStart-com.aspose.words.FieldStart-).

For more info see the Visitor design pattern.

**Parameters:**
| Parameter | Type | Description |
| --- | --- | --- |
| visitor | [DocumentVisitor](../../com.aspose.words/documentvisitor) | The visitor that will visit the node. |

**Returns:**
boolean - **False** if the visitor requested the enumeration to stop.
### getFieldData() {#getFieldData--}
```
public byte[] getFieldData()
```


Gets custom field data which is associated with the field.

**Returns:**
byte[] - Custom field data which is associated with the field.
