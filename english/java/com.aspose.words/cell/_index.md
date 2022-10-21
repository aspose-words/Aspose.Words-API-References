---
title: Cell
second_title: Aspose.Words for Java API Reference
description: Represents a table cell.
type: docs
weight: 48
url: /java/com.aspose.words/cell/
---

**Inheritance:**
java.lang.Object, [com.aspose.words.Node](../../com.aspose.words/node), [com.aspose.words.CompositeNode](../../com.aspose.words/compositenode)
```
public class Cell extends CompositeNode
```

Represents a table cell.

To learn more, visit the **Working with Tables** documentation article.

**Cell** can only be a child of a **Row**.

**Cell** can contain block-level nodes **Paragraph** and **Table**.

A minimal valid cell needs to have at least one **Paragraph**.
## Constructors

| Constructor | Description |
| --- | --- |
| [Cell(DocumentBase doc)](#Cell-com.aspose.words.DocumentBase-) | Initializes a new instance of the **Cell** class. |
## Methods

| Method | Description |
| --- | --- |
| [getNodeType()](#getNodeType--) | Returns **NodeType.Cell**. |
| [getParentRow()](#getParentRow--) | Returns the parent row of the cell. |
| [getFirstParagraph()](#getFirstParagraph--) | Gets the first paragraph among the immediate children. |
| [getLastParagraph()](#getLastParagraph--) | Gets the last paragraph among the immediate children. |
| [isFirstCell()](#isFirstCell--) | True if this is the first cell inside a row; false otherwise. |
| [isLastCell()](#isLastCell--) | True if this is the last cell inside a row; false otherwise. |
| [getCellFormat()](#getCellFormat--) | Provides access to the formatting properties of the cell. |
| [getParagraphs()](#getParagraphs--) | Gets a collection of paragraphs that are immediate children of the cell. |
| [getTables()](#getTables--) | Gets a collection of tables that are immediate children of the cell. |
| [accept(DocumentVisitor visitor)](#accept-com.aspose.words.DocumentVisitor-) | Accepts a visitor. |
| [ensureMinimum()](#ensureMinimum--) | If the last child is not a paragraph, creates and appends one empty paragraph. |
| [getDirectCellAttr(int key)](#getDirectCellAttr-int-) |  |
| [fetchCellAttr(int key)](#fetchCellAttr-int-) |  |
| [fetchInheritedCellAttr(int key)](#fetchInheritedCellAttr-int-) |  |
| [setCellAttr(int key, Object value)](#setCellAttr-int-java.lang.Object-) |  |
| [clearCellAttrs()](#clearCellAttrs--) |  |
| [removeMoveRevisions()](#removeMoveRevisions--) |  |
### Cell(DocumentBase doc) {#Cell-com.aspose.words.DocumentBase-}
```
public Cell(DocumentBase doc)
```


Initializes a new instance of the **Cell** class.

When **Cell** is created, it belongs to the specified document, but is not yet part of the document and **ParentNode** is null.

To append **Cell** to the document use InsertAfter or InsertBefore on the row where you want the cell inserted.

**Parameters:**
| Parameter | Type | Description |
| --- | --- | --- |
| doc | [DocumentBase](../../com.aspose.words/documentbase) | The owner document. |

### getNodeType() {#getNodeType--}
```
public int getNodeType()
```


Returns **NodeType.Cell**.

**Returns:**
int - **NodeType.Cell**. The returned value is one of [NodeType](../../com.aspose.words/nodetype) constants.
### getParentRow() {#getParentRow--}
```
public Row getParentRow()
```


Returns the parent row of the cell. Equivalent to  (Row)FirstNonMarkupParentNode .

**Returns:**
[Row](../../com.aspose.words/row) - The parent row of the cell.
### getFirstParagraph() {#getFirstParagraph--}
```
public Paragraph getFirstParagraph()
```


Gets the first paragraph among the immediate children.

**Returns:**
[Paragraph](../../com.aspose.words/paragraph) - The first paragraph among the immediate children.
### getLastParagraph() {#getLastParagraph--}
```
public Paragraph getLastParagraph()
```


Gets the last paragraph among the immediate children.

**Returns:**
[Paragraph](../../com.aspose.words/paragraph) - The last paragraph among the immediate children.
### isFirstCell() {#isFirstCell--}
```
public boolean isFirstCell()
```


True if this is the first cell inside a row; false otherwise.

**Returns:**
boolean - The corresponding  boolean  value.
### isLastCell() {#isLastCell--}
```
public boolean isLastCell()
```


True if this is the last cell inside a row; false otherwise.

**Returns:**
boolean - The corresponding  boolean  value.
### getCellFormat() {#getCellFormat--}
```
public CellFormat getCellFormat()
```


Provides access to the formatting properties of the cell.

**Returns:**
[CellFormat](../../com.aspose.words/cellformat) - The corresponding [CellFormat](../../com.aspose.words/cellformat) value.
### getParagraphs() {#getParagraphs--}
```
public ParagraphCollection getParagraphs()
```


Gets a collection of paragraphs that are immediate children of the cell.

**Returns:**
[ParagraphCollection](../../com.aspose.words/paragraphcollection) - A collection of paragraphs that are immediate children of the cell.
### getTables() {#getTables--}
```
public TableCollection getTables()
```


Gets a collection of tables that are immediate children of the cell.

**Returns:**
[TableCollection](../../com.aspose.words/tablecollection) - A collection of tables that are immediate children of the cell.
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
boolean - True if all nodes were visited; false if DocumentVisitor stopped the operation before visiting all nodes. Calls DocumentVisitor.VisitCellStart, then calls Accept for all child nodes of the section and calls DocumentVisitor.VisitCellEnd at the end.
### ensureMinimum() {#ensureMinimum--}
```
public void ensureMinimum()
```


If the last child is not a paragraph, creates and appends one empty paragraph.

### getDirectCellAttr(int key) {#getDirectCellAttr-int-}
```
public Object getDirectCellAttr(int key)
```




**Parameters:**
| Parameter | Type | Description |
| --- | --- | --- |
| key | int |  |

**Returns:**
java.lang.Object
### fetchCellAttr(int key) {#fetchCellAttr-int-}
```
public Object fetchCellAttr(int key)
```




**Parameters:**
| Parameter | Type | Description |
| --- | --- | --- |
| key | int |  |

**Returns:**
java.lang.Object
### fetchInheritedCellAttr(int key) {#fetchInheritedCellAttr-int-}
```
public Object fetchInheritedCellAttr(int key)
```




**Parameters:**
| Parameter | Type | Description |
| --- | --- | --- |
| key | int |  |

**Returns:**
java.lang.Object
### setCellAttr(int key, Object value) {#setCellAttr-int-java.lang.Object-}
```
public void setCellAttr(int key, Object value)
```




**Parameters:**
| Parameter | Type | Description |
| --- | --- | --- |
| key | int |  |
| value | java.lang.Object |  |

### clearCellAttrs() {#clearCellAttrs--}
```
public void clearCellAttrs()
```




### removeMoveRevisions() {#removeMoveRevisions--}
```
public void removeMoveRevisions()
```




