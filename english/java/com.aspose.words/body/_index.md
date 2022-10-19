---
title: Body
second_title: Aspose.Words for Java API Reference
description: Represents a container for the main text of a section.
type: docs
weight: 30
url: /java/com.aspose.words/body/
---

**Inheritance:**
java.lang.Object, [com.aspose.words.Node](../../com.aspose.words/node), [com.aspose.words.CompositeNode](../../com.aspose.words/compositenode), [com.aspose.words.Story](../../com.aspose.words/story)
```
public class Body extends Story
```

Represents a container for the main text of a section.

To learn more, visit the **Aspose.Words Document Object Model (DOM)** documentation article.

**Body** can contain **Paragraph** and **Table** child nodes.

**Body** is a section-level node and can only be a child of **Section**. There can only be one **Body** in a **Section**.

A minimal valid **Body** needs to contain at least one **Paragraph**.
## Constructors

| Constructor | Description |
| --- | --- |
| [Body(DocumentBase doc)](#Body-com.aspose.words.DocumentBase-) | Initializes a new instance of the **Body** class. |
## Methods

| Method | Description |
| --- | --- |
| [getNodeType()](#getNodeType--) | Returns **NodeType.Body**. |
| [getParentSection()](#getParentSection--) | Gets the parent section of this story. |
| [accept(DocumentVisitor visitor)](#accept-com.aspose.words.DocumentVisitor-) | Accepts a visitor. |
| [ensureMinimum()](#ensureMinimum--) | If the last child is not a paragraph, creates and appends one empty paragraph. |
### Body(DocumentBase doc) {#Body-com.aspose.words.DocumentBase-}
```
public Body(DocumentBase doc)
```


Initializes a new instance of the **Body** class.

When **Body** is created, it belongs to the specified document, but is not yet part of the document and **ParentNode** is null.

To append **Body** to a **Section** use Section.InsertAfter or Section.InsertBefore.

**Parameters:**
| Parameter | Type | Description |
| --- | --- | --- |
| doc | [DocumentBase](../../com.aspose.words/documentbase) | The owner document. |

### getNodeType() {#getNodeType--}
```
public int getNodeType()
```


Returns **NodeType.Body**.

**Returns:**
int - **NodeType.Body**. The returned value is one of [NodeType](../../com.aspose.words/nodetype) constants.
### getParentSection() {#getParentSection--}
```
public Section getParentSection()
```


Gets the parent section of this story.

**ParentSection** is equivalent to  (Section)ParentNode .

**Returns:**
[Section](../../com.aspose.words/section) - The parent section of this story.
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
boolean - True if all nodes were visited; false if DocumentVisitor stopped the operation before visiting all nodes. Calls DocumentVisitor.VisitBodyStart, then calls Accept for all child nodes of the section and calls DocumentVisitor.VisitBodyEnd at the end.
### ensureMinimum() {#ensureMinimum--}
```
public void ensureMinimum()
```


If the last child is not a paragraph, creates and appends one empty paragraph.

