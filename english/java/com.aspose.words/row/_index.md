---
title: Row
second_title: Aspose.Words for Java API Reference
description: Represents a table row.
type: docs
weight: 492
url: /java/com.aspose.words/row/
---

**Inheritance:**
java.lang.Object, [com.aspose.words.Node](../../com.aspose.words/node), [com.aspose.words.CompositeNode](../../com.aspose.words/compositenode)
```
public class Row extends CompositeNode
```

Represents a table row.

To learn more, visit the **Working with Tables** documentation article.

**Row** can only be a child of a **Table**.

**Row** can contain one or more **Cell** nodes.

A minimal valid row needs to have at least one **Cell**.
## Constructors

| Constructor | Description |
| --- | --- |
| [Row(DocumentBase doc)](#Row-com.aspose.words.DocumentBase-) | Initializes a new instance of the **Row** class. |
## Methods

| Method | Description |
| --- | --- |
| [getNodeType()](#getNodeType--) | Returns **NodeType.Row**. |
| [getParentTable()](#getParentTable--) | Returns the immediate parent table of the row. |
| [isFirstRow()](#isFirstRow--) | True if this is the first row in a table; false otherwise. |
| [isLastRow()](#isLastRow--) | True if this is the last row in a table; false otherwise. |
| [getFirstCell()](#getFirstCell--) | Returns the first **Cell** in the row. |
| [getLastCell()](#getLastCell--) | Returns the last **Cell** in the row. |
| [getCells()](#getCells--) | Provides typed access to the **Cell** child nodes of the row. |
| [getRowFormat()](#getRowFormat--) | Provides access to the formatting properties of the row. |
| [accept(DocumentVisitor visitor)](#accept-com.aspose.words.DocumentVisitor-) | Accepts a visitor. |
| [getText()](#getText--) | Gets the text of all cells in this row including the end of row character. |
| [ensureMinimum()](#ensureMinimum--) | If the **Row** has no cells, creates and appends one **Cell**. |
| [getDirectRowAttr(int key)](#getDirectRowAttr-int-) |  |
| [fetchRowAttr(int key)](#fetchRowAttr-int-) |  |
| [fetchInheritedRowAttr(int key)](#fetchInheritedRowAttr-int-) |  |
| [setRowAttr(int key, Object value)](#setRowAttr-int-java.lang.Object-) |  |
| [clearRowAttrs()](#clearRowAttrs--) |  |
| [resetToDefaultAttrs()](#resetToDefaultAttrs--) |  |
| [removeMoveRevisions()](#removeMoveRevisions--) |  |
### Row(DocumentBase doc) {#Row-com.aspose.words.DocumentBase-}
```
public Row(DocumentBase doc)
```


Initializes a new instance of the **Row** class.

When **Row** is created, it belongs to the specified document, but is not yet part of the document and **ParentNode** is null.

To append **Row** to the document use InsertAfter or InsertBefore on the table where you want the row inserted.

**Parameters:**
| Parameter | Type | Description |
| --- | --- | --- |
| doc | [DocumentBase](../../com.aspose.words/documentbase) | The owner document. |

### getNodeType() {#getNodeType--}
```
public int getNodeType()
```


Returns **NodeType.Row**.

**Returns:**
int - **NodeType.Row**. The returned value is one of [NodeType](../../com.aspose.words/nodetype) constants.
### getParentTable() {#getParentTable--}
```
public Table getParentTable()
```


Returns the immediate parent table of the row. Equivalent to  (Table)FirstNonMarkupParentNode .

**Returns:**
[Table](../../com.aspose.words/table) - The immediate parent table of the row.
### isFirstRow() {#isFirstRow--}
```
public boolean isFirstRow()
```


True if this is the first row in a table; false otherwise.

**Returns:**
boolean - The corresponding  boolean  value.
### isLastRow() {#isLastRow--}
```
public boolean isLastRow()
```


True if this is the last row in a table; false otherwise.

**Returns:**
boolean - The corresponding  boolean  value.
### getFirstCell() {#getFirstCell--}
```
public Cell getFirstCell()
```


Returns the first **Cell** in the row.

**Returns:**
[Cell](../../com.aspose.words/cell) - The first **Cell** in the row.
### getLastCell() {#getLastCell--}
```
public Cell getLastCell()
```


Returns the last **Cell** in the row.

**Returns:**
[Cell](../../com.aspose.words/cell) - The last **Cell** in the row.
### getCells() {#getCells--}
```
public CellCollection getCells()
```


Provides typed access to the **Cell** child nodes of the row.

**Returns:**
[CellCollection](../../com.aspose.words/cellcollection) - The corresponding [CellCollection](../../com.aspose.words/cellcollection) value.
### getRowFormat() {#getRowFormat--}
```
public RowFormat getRowFormat()
```


Provides access to the formatting properties of the row.

**Returns:**
[RowFormat](../../com.aspose.words/rowformat) - The corresponding [RowFormat](../../com.aspose.words/rowformat) value.
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
boolean - True if all nodes were visited; false if DocumentVisitor stopped the operation before visiting all nodes. Calls DocumentVisitor.VisitRowStart, then calls Accept for all child nodes of the section and calls DocumentVisitor.VisitRowEnd at the end.
### getText() {#getText--}
```
public String getText()
```


Gets the text of all cells in this row including the end of row character.

Returns concatenated text of all child nodes with the end of row character [ControlChar.CELL](../../com.aspose.words/controlchar\#CELL) appended at the end.

The returned string includes all control and special characters as described in [ControlChar](../../com.aspose.words/controlchar).

**Returns:**
java.lang.String
### ensureMinimum() {#ensureMinimum--}
```
public void ensureMinimum()
```


If the **Row** has no cells, creates and appends one **Cell**.

### getDirectRowAttr(int key) {#getDirectRowAttr-int-}
```
public Object getDirectRowAttr(int key)
```




**Parameters:**
| Parameter | Type | Description |
| --- | --- | --- |
| key | int |  |

**Returns:**
java.lang.Object
### fetchRowAttr(int key) {#fetchRowAttr-int-}
```
public Object fetchRowAttr(int key)
```




**Parameters:**
| Parameter | Type | Description |
| --- | --- | --- |
| key | int |  |

**Returns:**
java.lang.Object
### fetchInheritedRowAttr(int key) {#fetchInheritedRowAttr-int-}
```
public Object fetchInheritedRowAttr(int key)
```




**Parameters:**
| Parameter | Type | Description |
| --- | --- | --- |
| key | int |  |

**Returns:**
java.lang.Object
### setRowAttr(int key, Object value) {#setRowAttr-int-java.lang.Object-}
```
public void setRowAttr(int key, Object value)
```




**Parameters:**
| Parameter | Type | Description |
| --- | --- | --- |
| key | int |  |
| value | java.lang.Object |  |

### clearRowAttrs() {#clearRowAttrs--}
```
public void clearRowAttrs()
```




### resetToDefaultAttrs() {#resetToDefaultAttrs--}
```
public void resetToDefaultAttrs()
```




### removeMoveRevisions() {#removeMoveRevisions--}
```
public void removeMoveRevisions()
```




