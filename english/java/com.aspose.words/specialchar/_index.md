---
title: SpecialChar
second_title: Aspose.Words for Java API Reference
description: Base class for special characters in the document.
type: docs
weight: 527
url: /java/com.aspose.words/specialchar/
---

**Inheritance:**
java.lang.Object, [com.aspose.words.Node](../../com.aspose.words/node), [com.aspose.words.Inline](../../com.aspose.words/inline)
```
public class SpecialChar extends Inline
```

Base class for special characters in the document.

To learn more, visit the **Aspose.Words Document Object Model (DOM)** documentation article.

A Microsoft Word document can include a number of special characters that represent fields, form fields, shapes, OLE objects, footnotes etc. For the list of special characters see [ControlChar](../../com.aspose.words/controlchar).

**SpecialChar** is an inline-node and can only be a child of **Paragraph**.

**SpecialChar** char is used as a base class for more specific classes that represent special characters that Aspose.Words provides programmatic access for. The **SpecialChar** class is also used itself to represent special character for which Aspose.Words does not provide detailed programmatic access.
## Methods

| Method | Description |
| --- | --- |
| [getNodeType()](#getNodeType--) | Returns **NodeType.SpecialChar**. |
| [accept(DocumentVisitor visitor)](#accept-com.aspose.words.DocumentVisitor-) | Accepts a visitor. |
| [getText()](#getText--) | Gets the special character that this node represents. |
### getNodeType() {#getNodeType--}
```
public int getNodeType()
```


Returns **NodeType.SpecialChar**.

**Returns:**
int - **NodeType.SpecialChar**. The returned value is one of [NodeType](../../com.aspose.words/nodetype) constants.
### accept(DocumentVisitor visitor) {#accept-com.aspose.words.DocumentVisitor-}
```
public boolean accept(DocumentVisitor visitor)
```


Accepts a visitor.

Calls DocumentVisitor.VisitSpecialChar.

For more info see the Visitor design pattern.

**Parameters:**
| Parameter | Type | Description |
| --- | --- | --- |
| visitor | [DocumentVisitor](../../com.aspose.words/documentvisitor) | The visitor that will visit the node. |

**Returns:**
boolean - False if the visitor requested the enumeration to stop.
### getText() {#getText--}
```
public String getText()
```


Gets the special character that this node represents.

**Returns:**
java.lang.String - The string that contains the character that this node represents.
