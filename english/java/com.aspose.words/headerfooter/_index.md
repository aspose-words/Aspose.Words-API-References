---
title: HeaderFooter
second_title: Aspose.Words for Java API Reference
description: Represents a container for the header or footer text of a section.
type: docs
weight: 315
url: /java/com.aspose.words/headerfooter/
---

**Inheritance:**
java.lang.Object, [com.aspose.words.Node](../../com.aspose.words/node), [com.aspose.words.CompositeNode](../../com.aspose.words/compositenode), [com.aspose.words.Story](../../com.aspose.words/story)
```
public class HeaderFooter extends Story
```

Represents a container for the header or footer text of a section.

To learn more, visit the **Working with Headers and Footers** documentation article.

**HeaderFooter** can contain **Paragraph** and **Table** child nodes.

**HeaderFooter** is a section-level node and can only be a child of **Section**. There can only be one **HeaderFooter** or each [getHeaderFooterType()](../../com.aspose.words/headerfooter\#getHeaderFooterType--) in a **Section**.

If **Section** does not have a **HeaderFooter** of a specific type or the **HeaderFooter** has no child nodes, this header/footer is considered linked to the header/footer of the same type of the previous section in Microsoft Word.

When **HeaderFooter** contains at least one **Paragraph**, it is no longer considered linked to previous in Microsoft Word.
## Constructors

| Constructor | Description |
| --- | --- |
| [HeaderFooter(DocumentBase doc, int headerFooterType)](#HeaderFooter-com.aspose.words.DocumentBase-int-) | Initializes a new instance of this class. |
## Methods

| Method | Description |
| --- | --- |
| [getNodeType()](#getNodeType--) | Returns **NodeType.HeaderFooter**. |
| [getParentSection()](#getParentSection--) | Gets the parent section of this story. |
| [getHeaderFooterType()](#getHeaderFooterType--) | Gets the type of this header/footer. |
| [isHeader()](#isHeader--) | True if this **HeaderFooter** object is a header. |
| [isLinkedToPrevious()](#isLinkedToPrevious--) | True if this header or footer is linked to the corresponding header or footer in the previous section. |
| [isLinkedToPrevious(boolean value)](#isLinkedToPrevious-boolean-) | True if this header or footer is linked to the corresponding header or footer in the previous section. |
| [accept(DocumentVisitor visitor)](#accept-com.aspose.words.DocumentVisitor-) | Accepts a visitor. |
### HeaderFooter(DocumentBase doc, int headerFooterType) {#HeaderFooter-com.aspose.words.DocumentBase-int-}
```
public HeaderFooter(DocumentBase doc, int headerFooterType)
```


Initializes a new instance of this class.

**Parameters:**
| Parameter | Type | Description |
| --- | --- | --- |
| doc | [DocumentBase](../../com.aspose.words/documentbase) |  |
| headerFooterType | int |  |

### getNodeType() {#getNodeType--}
```
public int getNodeType()
```


Returns **NodeType.HeaderFooter**.

**Returns:**
int - **NodeType.HeaderFooter**. The returned value is one of [NodeType](../../com.aspose.words/nodetype) constants.
### getParentSection() {#getParentSection--}
```
public Section getParentSection()
```


Gets the parent section of this story.

**ParentSection** is equivalent to  (Section)ParentNode .

**Returns:**
[Section](../../com.aspose.words/section) - The parent section of this story.
### getHeaderFooterType() {#getHeaderFooterType--}
```
public int getHeaderFooterType()
```


Gets the type of this header/footer.

**Returns:**
int - The type of this header/footer. The returned value is one of [HeaderFooterType](../../com.aspose.words/headerfootertype) constants.
### isHeader() {#isHeader--}
```
public boolean isHeader()
```


True if this **HeaderFooter** object is a header.

**Returns:**
boolean - The corresponding  boolean  value.
### isLinkedToPrevious() {#isLinkedToPrevious--}
```
public boolean isLinkedToPrevious()
```


True if this header or footer is linked to the corresponding header or footer in the previous section.

Default is true.

Note, when your link a header or footer, its contents is cleared.

**Returns:**
boolean - The corresponding  boolean  value.
### isLinkedToPrevious(boolean value) {#isLinkedToPrevious-boolean-}
```
public void isLinkedToPrevious(boolean value)
```


True if this header or footer is linked to the corresponding header or footer in the previous section.

Default is true.

Note, when your link a header or footer, its contents is cleared.

**Parameters:**
| Parameter | Type | Description |
| --- | --- | --- |
| value | boolean | The corresponding  boolean  value. |

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
boolean - True if all nodes were visited; false if DocumentVisitor stopped the operation before visiting all nodes. Calls DocumentVisitor.VisitHeaderFooterStart, then calls Accept for all child nodes of the section and calls DocumentVisitor.VisitHeaderFooterEnd at the end.
