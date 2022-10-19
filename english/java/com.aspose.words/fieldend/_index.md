---
title: FieldEnd
second_title: Aspose.Words for Java API Reference
description: Represents an end of a Word field in a document.
type: docs
weight: 186
url: /java/com.aspose.words/fieldend/
---

**Inheritance:**
java.lang.Object, [com.aspose.words.Node](../../com.aspose.words/node), [com.aspose.words.Inline](../../com.aspose.words/inline), [com.aspose.words.SpecialChar](../../com.aspose.words/specialchar), [com.aspose.words.FieldChar](../../com.aspose.words/fieldchar)
```
public class FieldEnd extends FieldChar
```

Represents an end of a Word field in a document.

To learn more, visit the **Working with Fields** documentation article.

[FieldEnd](../../com.aspose.words/fieldend) is an inline-level node and represented by the [ControlChar.FIELD\_END\_CHAR](../../com.aspose.words/controlchar\#FIELD-END-CHAR) control character in the document.

[FieldEnd](../../com.aspose.words/fieldend) can only be a child of [Paragraph](../../com.aspose.words/paragraph).

A complete field in a Microsoft Word document is a complex structure consisting of a field start character, field code, field separator character, field result and field end character. Some fields only have field start, field code and field end.

To easily insert a new field into a document, use the [DocumentBuilder.insertField(java.lang.String)](../../com.aspose.words/documentbuilder\#insertField-java.lang.String-) method.
## Methods

| Method | Description |
| --- | --- |
| [getNodeType()](#getNodeType--) | Returns [NodeType.FIELD\_END](../../com.aspose.words/nodetype\#FIELD-END). |
| [hasSeparator()](#hasSeparator--) | Returns **true** if this field has a separator. |
| [accept(DocumentVisitor visitor)](#accept-com.aspose.words.DocumentVisitor-) | Accepts a visitor. |
### getNodeType() {#getNodeType--}
```
public int getNodeType()
```


Returns [NodeType.FIELD\_END](../../com.aspose.words/nodetype\#FIELD-END).

**Returns:**
int - \{[NodeType.FIELD\_END](../../com.aspose.words/nodetype\#FIELD-END). The returned value is one of [NodeType](../../com.aspose.words/nodetype) constants.
### hasSeparator() {#hasSeparator--}
```
public boolean hasSeparator()
```


Returns **true** if this field has a separator.

**Returns:**
boolean - **true** if this field has a separator.
### accept(DocumentVisitor visitor) {#accept-com.aspose.words.DocumentVisitor-}
```
public boolean accept(DocumentVisitor visitor)
```


Accepts a visitor.

Calls [DocumentVisitor.visitFieldEnd(com.aspose.words.FieldEnd)](../../com.aspose.words/documentvisitor\#visitFieldEnd-com.aspose.words.FieldEnd-).

For more info see the Visitor design pattern.

**Parameters:**
| Parameter | Type | Description |
| --- | --- | --- |
| visitor | [DocumentVisitor](../../com.aspose.words/documentvisitor) | The visitor that will visit the node. |

**Returns:**
boolean - **False** if the visitor requested the enumeration to stop.
