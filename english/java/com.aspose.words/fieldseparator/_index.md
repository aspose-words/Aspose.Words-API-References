---
title: FieldSeparator
second_title: Aspose.Words for Java API Reference
description: Represents a Word field separator that separates the field code from the field result.
type: docs
weight: 240
url: /java/com.aspose.words/fieldseparator/
---

**Inheritance:**
java.lang.Object, [com.aspose.words.Node](../../com.aspose.words/node), [com.aspose.words.Inline](../../com.aspose.words/inline), [com.aspose.words.SpecialChar](../../com.aspose.words/specialchar), [com.aspose.words.FieldChar](../../com.aspose.words/fieldchar)
```
public class FieldSeparator extends FieldChar
```

Represents a Word field separator that separates the field code from the field result.

To learn more, visit the **Working with Fields** documentation article.

[FieldSeparator](../../com.aspose.words/fieldseparator) is an inline-level node and represented by the [ControlChar.FIELD\_SEPARATOR\_CHAR](../../com.aspose.words/controlchar\#FIELD-SEPARATOR-CHAR) control character in the document.

[FieldSeparator](../../com.aspose.words/fieldseparator) can only be a child of [Paragraph](../../com.aspose.words/paragraph).

A complete field in a Microsoft Word document is a complex structure consisting of a field start character, field code, field separator character, field result and field end character. Some fields only have field start, field code and field end.

To easily insert a new field into a document, use the [DocumentBuilder.insertField(java.lang.String)](../../com.aspose.words/documentbuilder\#insertField-java.lang.String-) method.
## Methods

| Method | Description |
| --- | --- |
| [getNodeType()](#getNodeType--) | Returns [NodeType.FIELD\_SEPARATOR](../../com.aspose.words/nodetype\#FIELD-SEPARATOR). |
| [accept(DocumentVisitor visitor)](#accept-com.aspose.words.DocumentVisitor-) | Accepts a visitor. |
### getNodeType() {#getNodeType--}
```
public int getNodeType()
```


Returns [NodeType.FIELD\_SEPARATOR](../../com.aspose.words/nodetype\#FIELD-SEPARATOR).

**Returns:**
int - \{[NodeType.FIELD\_SEPARATOR](../../com.aspose.words/nodetype\#FIELD-SEPARATOR). The returned value is one of [NodeType](../../com.aspose.words/nodetype) constants.
### accept(DocumentVisitor visitor) {#accept-com.aspose.words.DocumentVisitor-}
```
public boolean accept(DocumentVisitor visitor)
```


Accepts a visitor.

Calls [DocumentVisitor.visitFieldSeparator(com.aspose.words.FieldSeparator)](../../com.aspose.words/documentvisitor\#visitFieldSeparator-com.aspose.words.FieldSeparator-).

For more info see the Visitor design pattern.

**Parameters:**
| Parameter | Type | Description |
| --- | --- | --- |
| visitor | [DocumentVisitor](../../com.aspose.words/documentvisitor) | The visitor that will visit the node. |

**Returns:**
boolean - **False** if the visitor requested the enumeration to stop.
