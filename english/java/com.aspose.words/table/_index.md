---
title: Table
second_title: Aspose.Words for Java API Reference
description: Represents a table in a Word document.
type: docs
weight: 548
url: /java/com.aspose.words/table/
---

**Inheritance:**
java.lang.Object, [com.aspose.words.Node](../../com.aspose.words/node), [com.aspose.words.CompositeNode](../../com.aspose.words/compositenode)
```
public class Table extends CompositeNode
```

Represents a table in a Word document.

To learn more, visit the **Working with Tables** documentation article.

**Table** is a block-level node and can be a child of classes derived from **Story** or **InlineStory**.

**Table** can contain one or more **Row** nodes.

A minimal valid table needs to have at least one **Row**.
## Constructors

| Constructor | Description |
| --- | --- |
| [Table(DocumentBase doc)](#Table-com.aspose.words.DocumentBase-) | Initializes a new instance of the **Table** class. |
## Methods

| Method | Description |
| --- | --- |
| [accept(DocumentVisitor visitor)](#accept-com.aspose.words.DocumentVisitor-) | Accepts a visitor. |
| [appendChild(Node newChild)](#appendChild-com.aspose.words.Node-) | Adds the specified node to the end of the list of child nodes for this node. |
| [autoFit(int behavior)](#autoFit-int-) |  |
| [clearBorders()](#clearBorders--) | Removes all table and cell borders on this table. |
| [clearShading()](#clearShading--) | Removes all shading on the table. |
| [convertToHorizontallyMergedCells()](#convertToHorizontallyMergedCells--) | Converts cells horizontally merged by width to cells merged by [CellFormat.getHorizontalMerge()](../../com.aspose.words/cellformat\#getHorizontalMerge--) / [CellFormat.setHorizontalMerge(int)](../../com.aspose.words/cellformat\#setHorizontalMerge-int-). |
| [dd()](#dd--) |  |
| [deepClone(boolean isCloneChildren)](#deepClone-boolean-) | Creates a duplicate of the node. |
| [ensureMinimum()](#ensureMinimum--) | If the table has no rows, creates and appends one **Row**. |
| [equals(Object arg0)](#equals-java.lang.Object-) |  |
| [getAbsoluteHorizontalDistance()](#getAbsoluteHorizontalDistance--) | Gets absolute horizontal floating table position specified by the table properties, in points. |
| [getAbsoluteVerticalDistance()](#getAbsoluteVerticalDistance--) | Gets absolute vertical floating table position specified by the table properties, in points. |
| [getAlignment()](#getAlignment--) | Specifies how an inline table is aligned in the document. |
| [getAllowAutoFit()](#getAllowAutoFit--) | Allows Microsoft Word and Aspose.Words to automatically resize cells in a table to fit their contents. |
| [getAllowCellSpacing()](#getAllowCellSpacing--) | Gets the "Allow spacing between cells" option. |
| [getAllowOverlap()](#getAllowOverlap--) | Gets whether a floating table shall allow other floating objects in the document to overlap its extents when displayed. |
| [getAncestor(int ancestorType)](#getAncestor-int-) |  |
| [getAncestor(Class ancestorType)](#getAncestor-java.lang.Class-) | Gets the first ancestor of the specified object type. |
| [getBidi()](#getBidi--) | Gets whether this is a right-to-left table. |
| [getBottomPadding()](#getBottomPadding--) | Gets the amount of space (in points) to add below the contents of cells. |
| [getCellSpacing()](#getCellSpacing--) | Gets the amount of space (in points) between the cells. |
| [getChild(int nodeType, int index, boolean isDeep)](#getChild-int-int-boolean-) |  |
| [getChildNodes()](#getChildNodes--) | Gets all immediate child nodes of this node. |
| [getChildNodes(int nodeType, boolean isDeep)](#getChildNodes-int-boolean-) |  |
| [getClass()](#getClass--) |  |
| [getContainer()](#getContainer--) |  |
| [getCount()](#getCount--) | Gets the number of immediate children of this node. |
| [getCurrentNode()](#getCurrentNode--) |  |
| [getCustomNodeId()](#getCustomNodeId--) | Specifies custom node identifier. |
| [getDescription()](#getDescription--) | Gets description of this table. |
| [getDistanceBottom()](#getDistanceBottom--) | Gets distance between table bottom and the surrounding text, in points. |
| [getDistanceLeft()](#getDistanceLeft--) | Gets distance between table left and the surrounding text, in points. |
| [getDistanceRight()](#getDistanceRight--) | Gets distance between table right and the surrounding text, in points. |
| [getDistanceTop()](#getDistanceTop--) | Gets distance between table top and the surrounding text, in points. |
| [getDocument()](#getDocument--) | Gets the document to which this node belongs. |
| [getFirstChild()](#getFirstChild--) | Gets the first child of the node. |
| [getFirstRow()](#getFirstRow--) | Returns the first **Row** node in the table. |
| [getHorizontalAnchor()](#getHorizontalAnchor--) | Gets the base object from which the horizontal positioning of floating table should be calculated. |
| [getLastChild()](#getLastChild--) | Gets the last child of the node. |
| [getLastRow()](#getLastRow--) | Returns the last **Row** node in the table. |
| [getLeftIndent()](#getLeftIndent--) | Gets the value that represents the left indent of the table. |
| [getLeftPadding()](#getLeftPadding--) | Gets the amount of space (in points) to add to the left of the contents of cells. |
| [getNextMatchingNode(Node curNode)](#getNextMatchingNode-com.aspose.words.Node-) |  |
| [getNextSibling()](#getNextSibling--) | Gets the node immediately following this node. |
| [getNodeType()](#getNodeType--) | Returns **NodeType.Table**. |
| [getParentNode()](#getParentNode--) | Gets the immediate parent of this node. |
| [getPreferredWidth()](#getPreferredWidth--) | Gets the table preferred width. |
| [getPreviousSibling()](#getPreviousSibling--) | Gets the node immediately preceding this node. |
| [getRange()](#getRange--) | Returns a **Range** object that represents the portion of a document that is contained in this node. |
| [getRelativeHorizontalAlignment()](#getRelativeHorizontalAlignment--) | Gets floating table relative horizontal alignment. |
| [getRelativeVerticalAlignment()](#getRelativeVerticalAlignment--) | Gets floating table relative vertical alignment. |
| [getRightPadding()](#getRightPadding--) | Gets the amount of space (in points) to add to the right of the contents of cells. |
| [getRows()](#getRows--) | Provides typed access to the rows of the table. |
| [getStyle()](#getStyle--) | Gets the table style applied to this table. |
| [getStyleIdentifier()](#getStyleIdentifier--) | Gets the locale independent style identifier of the table style applied to this table. |
| [getStyleName()](#getStyleName--) | Gets the name of the table style applied to this table. |
| [getStyleOptions()](#getStyleOptions--) | Gets bit flags that specify how a table style is applied to this table. |
| [getText()](#getText--) | Gets the text of this node and of all its children. |
| [getTextWrapping()](#getTextWrapping--) | Gets [getTextWrapping()](../../com.aspose.words/table\#getTextWrapping--) / [setTextWrapping(int)](../../com.aspose.words/table\#setTextWrapping-int-) for table. |
| [getTitle()](#getTitle--) | Gets title of this table. |
| [getTopPadding()](#getTopPadding--) | Gets the amount of space (in points) to add above the contents of cells. |
| [getVerticalAnchor()](#getVerticalAnchor--) | Gets the base object from which the vertical positioning of floating table should be calculated. |
| [hasChildNodes()](#hasChildNodes--) | Returns true if this node has any child nodes. |
| [hashCode()](#hashCode--) |  |
| [indexOf(Node child)](#indexOf-com.aspose.words.Node-) | Returns the index of the specified child node in the child node array. |
| [insertAfter(Node newChild, Node refChild)](#insertAfter-com.aspose.words.Node-com.aspose.words.Node-) | Inserts the specified node immediately after the specified reference node. |
| [insertBefore(Node newChild, Node refChild)](#insertBefore-com.aspose.words.Node-com.aspose.words.Node-) | Inserts the specified node immediately before the specified reference node. |
| [isComposite()](#isComposite--) | Returns true as this node can have child nodes. |
| [iterator()](#iterator--) | Provides support for the for each style iteration over the child nodes of this node. |
| [nextPreOrder(Node rootNode)](#nextPreOrder-com.aspose.words.Node-) | Gets next node according to the pre-order tree traversal algorithm. |
| [nodeTypeToString(int nodeType)](#nodeTypeToString-int-) |  |
| [notify()](#notify--) |  |
| [notifyAll()](#notifyAll--) |  |
| [prependChild(Node newChild)](#prependChild-com.aspose.words.Node-) | Adds the specified node to the beginning of the list of child nodes for this node. |
| [previousPreOrder(Node rootNode)](#previousPreOrder-com.aspose.words.Node-) | Gets the previous node according to the pre-order tree traversal algorithm. |
| [remove()](#remove--) | Removes itself from the parent. |
| [removeAllChildren()](#removeAllChildren--) | Removes all the child nodes of the current node. |
| [removeChild(Node oldChild)](#removeChild-com.aspose.words.Node-) | Removes the specified child node. |
| [removeSmartTags()](#removeSmartTags--) | Removes all [SmartTag](../../com.aspose.words/smarttag) descendant nodes of the current node. |
| [selectNodes(String xpath)](#selectNodes-java.lang.String-) | Selects a list of nodes matching the XPath expression. |
| [selectSingleNode(String xpath)](#selectSingleNode-java.lang.String-) | Selects the first Node that matches the XPath expression. |
| [setAbsoluteHorizontalDistance(double value)](#setAbsoluteHorizontalDistance-double-) | Sets absolute horizontal floating table position specified by the table properties, in points. |
| [setAbsoluteVerticalDistance(double value)](#setAbsoluteVerticalDistance-double-) | Sets absolute vertical floating table position specified by the table properties, in points. |
| [setAlignment(int value)](#setAlignment-int-) | Specifies how an inline table is aligned in the document. |
| [setAllowAutoFit(boolean value)](#setAllowAutoFit-boolean-) | Allows Microsoft Word and Aspose.Words to automatically resize cells in a table to fit their contents. |
| [setAllowCellSpacing(boolean value)](#setAllowCellSpacing-boolean-) | Sets the "Allow spacing between cells" option. |
| [setBidi(boolean value)](#setBidi-boolean-) | Sets whether this is a right-to-left table. |
| [setBorder(int borderType, int lineStyle, double lineWidth, Color color, boolean isOverrideCellBorders)](#setBorder-int-int-double-java.awt.Color-boolean-) |  |
| [setBorders(int lineStyle, double lineWidth, Color color)](#setBorders-int-double-java.awt.Color-) |  |
| [setBottomPadding(double value)](#setBottomPadding-double-) | Sets the amount of space (in points) to add below the contents of cells. |
| [setCellSpacing(double value)](#setCellSpacing-double-) | Sets the amount of space (in points) between the cells. |
| [setCustomNodeId(int value)](#setCustomNodeId-int-) | Specifies custom node identifier. |
| [setDescription(String value)](#setDescription-java.lang.String-) | Sets description of this table. |
| [setHorizontalAnchor(int value)](#setHorizontalAnchor-int-) | Gets the base object from which the horizontal positioning of floating table should be calculated. |
| [setLeftIndent(double value)](#setLeftIndent-double-) | Sets the value that represents the left indent of the table. |
| [setLeftPadding(double value)](#setLeftPadding-double-) | Sets the amount of space (in points) to add to the left of the contents of cells. |
| [setPreferredWidth(PreferredWidth value)](#setPreferredWidth-com.aspose.words.PreferredWidth-) | Sets the table preferred width. |
| [setRelativeHorizontalAlignment(int value)](#setRelativeHorizontalAlignment-int-) | Sets floating table relative horizontal alignment. |
| [setRelativeVerticalAlignment(int value)](#setRelativeVerticalAlignment-int-) | Sets floating table relative vertical alignment. |
| [setRightPadding(double value)](#setRightPadding-double-) | Sets the amount of space (in points) to add to the right of the contents of cells. |
| [setShading(int texture, Color foregroundColor, Color backgroundColor)](#setShading-int-java.awt.Color-java.awt.Color-) |  |
| [setStyle(Style value)](#setStyle-com.aspose.words.Style-) | Sets the table style applied to this table. |
| [setStyleIdentifier(int value)](#setStyleIdentifier-int-) | Sets the locale independent style identifier of the table style applied to this table. |
| [setStyleName(String value)](#setStyleName-java.lang.String-) | Sets the name of the table style applied to this table. |
| [setStyleOptions(int value)](#setStyleOptions-int-) | Sets bit flags that specify how a table style is applied to this table. |
| [setTextWrapping(int value)](#setTextWrapping-int-) | Sets [getTextWrapping()](../../com.aspose.words/table\#getTextWrapping--) / [setTextWrapping(int)](../../com.aspose.words/table\#setTextWrapping-int-) for table. |
| [setTitle(String value)](#setTitle-java.lang.String-) | Sets title of this table. |
| [setTopPadding(double value)](#setTopPadding-double-) | Sets the amount of space (in points) to add above the contents of cells. |
| [setVerticalAnchor(int value)](#setVerticalAnchor-int-) | Gets the base object from which the vertical positioning of floating table should be calculated. |
| [toString()](#toString--) |  |
| [toString(SaveOptions saveOptions)](#toString-com.aspose.words.SaveOptions-) | Exports the content of the node into a string using the specified save options. |
| [toString(int saveFormat)](#toString-int-) |  |
| [wait()](#wait--) |  |
| [wait(long arg0)](#wait-long-) |  |
| [wait(long arg0, int arg1)](#wait-long-int-) |  |
### Table(DocumentBase doc) {#Table-com.aspose.words.DocumentBase-}
```
public Table(DocumentBase doc)
```


Initializes a new instance of the **Table** class.

When **Table** is created, it belongs to the specified document, but is not yet part of the document and **ParentNode** is null.

To append **Table** to the document use InsertAfter or InsertBefore on the story where you want the table inserted.

**Parameters:**
| Parameter | Type | Description |
| --- | --- | --- |
| doc | [DocumentBase](../../com.aspose.words/documentbase) | The owner document. |

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
boolean - True if all nodes were visited; false if DocumentVisitor stopped the operation before visiting all nodes. Calls DocumentVisitor.VisitTableStart, then calls Accept for all child nodes of the section and calls DocumentVisitor.VisitTableEnd at the end.
### appendChild(Node newChild) {#appendChild-com.aspose.words.Node-}
```
public Node appendChild(Node newChild)
```


Adds the specified node to the end of the list of child nodes for this node.

If the newChild is already in the tree, it is first removed.

If the node being inserted was created from another document, you should use **M:Aspose.Words.DocumentBase.ImportNode(Aspose.Words.Node,System.Boolean,Aspose.Words.ImportFormatMode)** to import the node to the current document. The imported node can then be inserted into the current document.

**Parameters:**
| Parameter | Type | Description |
| --- | --- | --- |
| newChild | [Node](../../com.aspose.words/node) | The node to add. |

**Returns:**
[Node](../../com.aspose.words/node) - The node added.
### autoFit(int behavior) {#autoFit-int-}
```
public void autoFit(int behavior)
```




**Parameters:**
| Parameter | Type | Description |
| --- | --- | --- |
| behavior | int |  |

### clearBorders() {#clearBorders--}
```
public void clearBorders()
```


Removes all table and cell borders on this table.

### clearShading() {#clearShading--}
```
public void clearShading()
```


Removes all shading on the table.

### convertToHorizontallyMergedCells() {#convertToHorizontallyMergedCells--}
```
public void convertToHorizontallyMergedCells()
```


Converts cells horizontally merged by width to cells merged by [CellFormat.getHorizontalMerge()](../../com.aspose.words/cellformat\#getHorizontalMerge--) / [CellFormat.setHorizontalMerge(int)](../../com.aspose.words/cellformat\#setHorizontalMerge-int-).

Table cells can be horizontally merged either using merge flags [CellFormat.getHorizontalMerge()](../../com.aspose.words/cellformat\#getHorizontalMerge--) / [CellFormat.setHorizontalMerge(int)](../../com.aspose.words/cellformat\#setHorizontalMerge-int-) or using cell width [CellFormat.getWidth()](../../com.aspose.words/cellformat\#getWidth--) / [CellFormat.setWidth(double)](../../com.aspose.words/cellformat\#setWidth-double-).

When table cell is merged by width property [CellFormat.getHorizontalMerge()](../../com.aspose.words/cellformat\#getHorizontalMerge--) / [CellFormat.setHorizontalMerge(int)](../../com.aspose.words/cellformat\#setHorizontalMerge-int-) is meaningless but sometimes having merge flags is more convenient way.

Use this method to transforms table cells horizontally merged by width to cells merged by merge flags.

### dd() {#dd--}
```
public void dd()
```




### deepClone(boolean isCloneChildren) {#deepClone-boolean-}
```
public Node deepClone(boolean isCloneChildren)
```


Creates a duplicate of the node.

This method serves as a copy constructor for nodes. The cloned node has no parent, but belongs to the same document as the original node.

This method always performs a deep copy of the node. The *isCloneChildren* parameter specifies whether to perform copy all child nodes as well.

**Parameters:**
| Parameter | Type | Description |
| --- | --- | --- |
| isCloneChildren | boolean | True to recursively clone the subtree under the specified node; false to clone only the node itself. |

**Returns:**
[Node](../../com.aspose.words/node) - The cloned node.
### ensureMinimum() {#ensureMinimum--}
```
public void ensureMinimum()
```


If the table has no rows, creates and appends one **Row**.

### equals(Object arg0) {#equals-java.lang.Object-}
```
public boolean equals(Object arg0)
```




**Parameters:**
| Parameter | Type | Description |
| --- | --- | --- |
| arg0 | java.lang.Object |  |

**Returns:**
boolean
### getAbsoluteHorizontalDistance() {#getAbsoluteHorizontalDistance--}
```
public double getAbsoluteHorizontalDistance()
```


Gets absolute horizontal floating table position specified by the table properties, in points. Default value is 0.

**Returns:**
double - Absolute horizontal floating table position specified by the table properties, in points.
### getAbsoluteVerticalDistance() {#getAbsoluteVerticalDistance--}
```
public double getAbsoluteVerticalDistance()
```


Gets absolute vertical floating table position specified by the table properties, in points. Default value is 0.

**Returns:**
double - Absolute vertical floating table position specified by the table properties, in points.
### getAlignment() {#getAlignment--}
```
public int getAlignment()
```


Specifies how an inline table is aligned in the document.

The default value is [TableAlignment.LEFT](../../com.aspose.words/tablealignment\#LEFT).

**Returns:**
int - The corresponding  int  value. The returned value is one of [TableAlignment](../../com.aspose.words/tablealignment) constants.
### getAllowAutoFit() {#getAllowAutoFit--}
```
public boolean getAllowAutoFit()
```


Allows Microsoft Word and Aspose.Words to automatically resize cells in a table to fit their contents.

The default value is  true .

**M:Aspose.Words.Tables.Table.AutoFit(Aspose.Words.Tables.AutoFitBehavior)**

**Returns:**
boolean - The corresponding  boolean  value.
### getAllowCellSpacing() {#getAllowCellSpacing--}
```
public boolean getAllowCellSpacing()
```


Gets the "Allow spacing between cells" option.

**Returns:**
boolean - The "Allow spacing between cells" option.
### getAllowOverlap() {#getAllowOverlap--}
```
public boolean getAllowOverlap()
```


Gets whether a floating table shall allow other floating objects in the document to overlap its extents when displayed. Default value is  true .

**Returns:**
boolean - Whether a floating table shall allow other floating objects in the document to overlap its extents when displayed.
### getAncestor(int ancestorType) {#getAncestor-int-}
```
public CompositeNode getAncestor(int ancestorType)
```




**Parameters:**
| Parameter | Type | Description |
| --- | --- | --- |
| ancestorType | int |  |

**Returns:**
[CompositeNode](../../com.aspose.words/compositenode)
### getAncestor(Class ancestorType) {#getAncestor-java.lang.Class-}
```
public CompositeNode getAncestor(Class ancestorType)
```


Gets the first ancestor of the specified object type.

**Parameters:**
| Parameter | Type | Description |
| --- | --- | --- |
| ancestorType | java.lang.Class | The object type of the ancestor to retrieve. |

**Returns:**
[CompositeNode](../../com.aspose.words/compositenode) - The ancestor of the specified type or null if no ancestor of this type was found.

The ancestor type matches if it is equal to ancestorType or derived from ancestorType.
### getBidi() {#getBidi--}
```
public boolean getBidi()
```


Gets whether this is a right-to-left table.

When  true , the cells in this row are laid out right to left.

The default value is  false .

**Returns:**
boolean - Whether this is a right-to-left table.
### getBottomPadding() {#getBottomPadding--}
```
public double getBottomPadding()
```


Gets the amount of space (in points) to add below the contents of cells.

**Returns:**
double - The amount of space (in points) to add below the contents of cells.
### getCellSpacing() {#getCellSpacing--}
```
public double getCellSpacing()
```


Gets the amount of space (in points) between the cells.

**Returns:**
double - The amount of space (in points) between the cells.
### getChild(int nodeType, int index, boolean isDeep) {#getChild-int-int-boolean-}
```
public Node getChild(int nodeType, int index, boolean isDeep)
```




**Parameters:**
| Parameter | Type | Description |
| --- | --- | --- |
| nodeType | int |  |
| index | int |  |
| isDeep | boolean |  |

**Returns:**
[Node](../../com.aspose.words/node)
### getChildNodes() {#getChildNodes--}
```
public NodeCollection getChildNodes()
```


Gets all immediate child nodes of this node.

Note, [getChildNodes()](../../com.aspose.words/compositenode\#getChildNodes--) is equivalent to calling  GetChildNodes(NodeType.Any, false)  and creates and returns a new collection every time it is accessed.

If there are no child nodes, this property returns an empty collection.

**Returns:**
[NodeCollection](../../com.aspose.words/nodecollection) - All immediate child nodes of this node.
### getChildNodes(int nodeType, boolean isDeep) {#getChildNodes-int-boolean-}
```
public NodeCollection getChildNodes(int nodeType, boolean isDeep)
```




**Parameters:**
| Parameter | Type | Description |
| --- | --- | --- |
| nodeType | int |  |
| isDeep | boolean |  |

**Returns:**
[NodeCollection](../../com.aspose.words/nodecollection)
### getClass() {#getClass--}
```
public final native Class<?> getClass()
```




**Returns:**
java.lang.Class<?>
### getContainer() {#getContainer--}
```
public CompositeNode getContainer()
```




**Returns:**
[CompositeNode](../../com.aspose.words/compositenode)
### getCount() {#getCount--}
```
public int getCount()
```


Gets the number of immediate children of this node.

**Returns:**
int - The number of immediate children of this node.
### getCurrentNode() {#getCurrentNode--}
```
public Node getCurrentNode()
```




**Returns:**
[Node](../../com.aspose.words/node)
### getCustomNodeId() {#getCustomNodeId--}
```
public int getCustomNodeId()
```


Specifies custom node identifier.

Default is zero.

This identifier can be set and used arbitrarily. For example, as a key to get external data.

Important note, specified value is not saved to an output file and exists only during the node lifetime.

**Returns:**
int - The corresponding  int  value.
### getDescription() {#getDescription--}
```
public String getDescription()
```


Gets description of this table. It provides an alternative text representation of the information contained in the table.

The default value is an empty string.

This property is meaningful for ISO/IEC 29500 compliant DOCX documents ( [OoxmlCompliance](../../com.aspose.words/ooxmlcompliance)). When saved to pre-ISO/IEC 29500 formats, the property is ignored.

**Returns:**
java.lang.String - Description of this table.
### getDistanceBottom() {#getDistanceBottom--}
```
public double getDistanceBottom()
```


Gets distance between table bottom and the surrounding text, in points.

**Returns:**
double - Distance between table bottom and the surrounding text, in points.
### getDistanceLeft() {#getDistanceLeft--}
```
public double getDistanceLeft()
```


Gets distance between table left and the surrounding text, in points.

**Returns:**
double - Distance between table left and the surrounding text, in points.
### getDistanceRight() {#getDistanceRight--}
```
public double getDistanceRight()
```


Gets distance between table right and the surrounding text, in points.

**Returns:**
double - Distance between table right and the surrounding text, in points.
### getDistanceTop() {#getDistanceTop--}
```
public double getDistanceTop()
```


Gets distance between table top and the surrounding text, in points.

**Returns:**
double - Distance between table top and the surrounding text, in points.
### getDocument() {#getDocument--}
```
public DocumentBase getDocument()
```


Gets the document to which this node belongs.

The node always belongs to a document even if it has just been created and not yet added to the tree, or if it has been removed from the tree.

**Returns:**
[DocumentBase](../../com.aspose.words/documentbase) - The document to which this node belongs.
### getFirstChild() {#getFirstChild--}
```
public Node getFirstChild()
```


Gets the first child of the node. If there is no first child node, a null is returned.

**Returns:**
[Node](../../com.aspose.words/node) - The first child of the node.
### getFirstRow() {#getFirstRow--}
```
public Row getFirstRow()
```


Returns the first **Row** node in the table.

**Returns:**
[Row](../../com.aspose.words/row) - The first **Row** node in the table.
### getHorizontalAnchor() {#getHorizontalAnchor--}
```
public int getHorizontalAnchor()
```


Gets the base object from which the horizontal positioning of floating table should be calculated. Default value is [RelativeHorizontalPosition.COLUMN](../../com.aspose.words/relativehorizontalposition\#COLUMN).

**Returns:**
int - The base object from which the horizontal positioning of floating table should be calculated. The returned value is one of [RelativeHorizontalPosition](../../com.aspose.words/relativehorizontalposition) constants.
### getLastChild() {#getLastChild--}
```
public Node getLastChild()
```


Gets the last child of the node. If there is no last child node, a null is returned.

**Returns:**
[Node](../../com.aspose.words/node) - The last child of the node.
### getLastRow() {#getLastRow--}
```
public Row getLastRow()
```


Returns the last **Row** node in the table.

**Returns:**
[Row](../../com.aspose.words/row) - The last **Row** node in the table.
### getLeftIndent() {#getLeftIndent--}
```
public double getLeftIndent()
```


Gets the value that represents the left indent of the table.

**Returns:**
double - The value that represents the left indent of the table.
### getLeftPadding() {#getLeftPadding--}
```
public double getLeftPadding()
```


Gets the amount of space (in points) to add to the left of the contents of cells.

**Returns:**
double - The amount of space (in points) to add to the left of the contents of cells.
### getNextMatchingNode(Node curNode) {#getNextMatchingNode-com.aspose.words.Node-}
```
public Node getNextMatchingNode(Node curNode)
```




**Parameters:**
| Parameter | Type | Description |
| --- | --- | --- |
| curNode | [Node](../../com.aspose.words/node) |  |

**Returns:**
[Node](../../com.aspose.words/node)
### getNextSibling() {#getNextSibling--}
```
public Node getNextSibling()
```


Gets the node immediately following this node. If there is no next node, a null is returned.

**Returns:**
[Node](../../com.aspose.words/node) - The node immediately following this node.
### getNodeType() {#getNodeType--}
```
public int getNodeType()
```


Returns **NodeType.Table**.

**Returns:**
int - **NodeType.Table**. The returned value is one of [NodeType](../../com.aspose.words/nodetype) constants.
### getParentNode() {#getParentNode--}
```
public CompositeNode getParentNode()
```


Gets the immediate parent of this node.

If a node has just been created and not yet added to the tree, or if it has been removed from the tree, the parent is null.

**Returns:**
[CompositeNode](../../com.aspose.words/compositenode) - The immediate parent of this node.
### getPreferredWidth() {#getPreferredWidth--}
```
public PreferredWidth getPreferredWidth()
```


Gets the table preferred width.

The default value is [PreferredWidth.AUTO](../../com.aspose.words/preferredwidth\#AUTO).

**Returns:**
[PreferredWidth](../../com.aspose.words/preferredwidth) - The table preferred width.
### getPreviousSibling() {#getPreviousSibling--}
```
public Node getPreviousSibling()
```


Gets the node immediately preceding this node. If there is no preceding node, a null is returned.

**Returns:**
[Node](../../com.aspose.words/node) - The node immediately preceding this node.
### getRange() {#getRange--}
```
public Range getRange()
```


Returns a **Range** object that represents the portion of a document that is contained in this node.

**Returns:**
[Range](../../com.aspose.words/range) - A **Range** object that represents the portion of a document that is contained in this node.
### getRelativeHorizontalAlignment() {#getRelativeHorizontalAlignment--}
```
public int getRelativeHorizontalAlignment()
```


Gets floating table relative horizontal alignment.

**Returns:**
int - Floating table relative horizontal alignment. The returned value is one of [HorizontalAlignment](../../com.aspose.words/horizontalalignment) constants.
### getRelativeVerticalAlignment() {#getRelativeVerticalAlignment--}
```
public int getRelativeVerticalAlignment()
```


Gets floating table relative vertical alignment.

**Returns:**
int - Floating table relative vertical alignment. The returned value is one of [VerticalAlignment](../../com.aspose.words/verticalalignment) constants.
### getRightPadding() {#getRightPadding--}
```
public double getRightPadding()
```


Gets the amount of space (in points) to add to the right of the contents of cells.

**Returns:**
double - The amount of space (in points) to add to the right of the contents of cells.
### getRows() {#getRows--}
```
public RowCollection getRows()
```


Provides typed access to the rows of the table.

**Returns:**
[RowCollection](../../com.aspose.words/rowcollection) - The corresponding [RowCollection](../../com.aspose.words/rowcollection) value.
### getStyle() {#getStyle--}
```
public Style getStyle()
```


Gets the table style applied to this table.

**Returns:**
[Style](../../com.aspose.words/style) - The table style applied to this table.
### getStyleIdentifier() {#getStyleIdentifier--}
```
public int getStyleIdentifier()
```


Gets the locale independent style identifier of the table style applied to this table.

**Returns:**
int - The locale independent style identifier of the table style applied to this table. The returned value is one of [StyleIdentifier](../../com.aspose.words/styleidentifier) constants.
### getStyleName() {#getStyleName--}
```
public String getStyleName()
```


Gets the name of the table style applied to this table.

**Returns:**
java.lang.String - The name of the table style applied to this table.
### getStyleOptions() {#getStyleOptions--}
```
public int getStyleOptions()
```


Gets bit flags that specify how a table style is applied to this table.

**Returns:**
int - Bit flags that specify how a table style is applied to this table. The returned value is a bitwise combination of [TableStyleOptions](../../com.aspose.words/tablestyleoptions) constants.
### getText() {#getText--}
```
public String getText()
```


Gets the text of this node and of all its children.

The returned string includes all control and special characters as described in [ControlChar](../../com.aspose.words/controlchar).

**Returns:**
java.lang.String
### getTextWrapping() {#getTextWrapping--}
```
public int getTextWrapping()
```


Gets [getTextWrapping()](../../com.aspose.words/table\#getTextWrapping--) / [setTextWrapping(int)](../../com.aspose.words/table\#setTextWrapping-int-) for table.

**Returns:**
int - \{[getTextWrapping()](../../com.aspose.words/table\#getTextWrapping--) / [setTextWrapping(int)](../../com.aspose.words/table\#setTextWrapping-int-) for table. The returned value is one of [TextWrapping](../../com.aspose.words/textwrapping) constants.
### getTitle() {#getTitle--}
```
public String getTitle()
```


Gets title of this table. It provides an alternative text representation of the information contained in the table.

The default value is an empty string.

This property is meaningful for ISO/IEC 29500 compliant DOCX documents ( [OoxmlCompliance](../../com.aspose.words/ooxmlcompliance)). When saved to pre-ISO/IEC 29500 formats, the property is ignored.

**Returns:**
java.lang.String - Title of this table.
### getTopPadding() {#getTopPadding--}
```
public double getTopPadding()
```


Gets the amount of space (in points) to add above the contents of cells.

**Returns:**
double - The amount of space (in points) to add above the contents of cells.
### getVerticalAnchor() {#getVerticalAnchor--}
```
public int getVerticalAnchor()
```


Gets the base object from which the vertical positioning of floating table should be calculated. Default value is [RelativeVerticalPosition.MARGIN](../../com.aspose.words/relativeverticalposition\#MARGIN).

**Returns:**
int - The base object from which the vertical positioning of floating table should be calculated. The returned value is one of [RelativeVerticalPosition](../../com.aspose.words/relativeverticalposition) constants.
### hasChildNodes() {#hasChildNodes--}
```
public boolean hasChildNodes()
```


Returns true if this node has any child nodes.

**Returns:**
boolean - True if this node has any child nodes.
### hashCode() {#hashCode--}
```
public native int hashCode()
```




**Returns:**
int
### indexOf(Node child) {#indexOf-com.aspose.words.Node-}
```
public int indexOf(Node child)
```


Returns the index of the specified child node in the child node array. Returns -1 if the node is not found in the child nodes.

**Parameters:**
| Parameter | Type | Description |
| --- | --- | --- |
| child | [Node](../../com.aspose.words/node) |  |

**Returns:**
int
### insertAfter(Node newChild, Node refChild) {#insertAfter-com.aspose.words.Node-com.aspose.words.Node-}
```
public Node insertAfter(Node newChild, Node refChild)
```


Inserts the specified node immediately after the specified reference node.

If refChild is null, inserts newChild at the beginning of the list of child nodes.

If the newChild is already in the tree, it is first removed.

If the node being inserted was created from another document, you should use **M:Aspose.Words.DocumentBase.ImportNode(Aspose.Words.Node,System.Boolean,Aspose.Words.ImportFormatMode)** to import the node to the current document. The imported node can then be inserted into the current document.

**Parameters:**
| Parameter | Type | Description |
| --- | --- | --- |
| newChild | [Node](../../com.aspose.words/node) | The Node to insert. |
| refChild | [Node](../../com.aspose.words/node) | The Node that is the reference node. The newNode is placed after the refNode. |

**Returns:**
[Node](../../com.aspose.words/node) - The inserted node.
### insertBefore(Node newChild, Node refChild) {#insertBefore-com.aspose.words.Node-com.aspose.words.Node-}
```
public Node insertBefore(Node newChild, Node refChild)
```


Inserts the specified node immediately before the specified reference node.

If refChild is null, inserts newChild at the end of the list of child nodes.

If the newChild is already in the tree, it is first removed.

If the node being inserted was created from another document, you should use **M:Aspose.Words.DocumentBase.ImportNode(Aspose.Words.Node,System.Boolean,Aspose.Words.ImportFormatMode)** to import the node to the current document. The imported node can then be inserted into the current document.

**Parameters:**
| Parameter | Type | Description |
| --- | --- | --- |
| newChild | [Node](../../com.aspose.words/node) | The Node to insert. |
| refChild | [Node](../../com.aspose.words/node) | The Node that is the reference node. The newChild is placed before this node. |

**Returns:**
[Node](../../com.aspose.words/node) - The inserted node.
### isComposite() {#isComposite--}
```
public boolean isComposite()
```


Returns true as this node can have child nodes.

**Returns:**
boolean - True as this node can have child nodes.
### iterator() {#iterator--}
```
public Iterator iterator()
```


Provides support for the for each style iteration over the child nodes of this node.

**Returns:**
java.util.Iterator
### nextPreOrder(Node rootNode) {#nextPreOrder-com.aspose.words.Node-}
```
public Node nextPreOrder(Node rootNode)
```


Gets next node according to the pre-order tree traversal algorithm.

**Parameters:**
| Parameter | Type | Description |
| --- | --- | --- |
| rootNode | [Node](../../com.aspose.words/node) | The top node (limit) of traversal. |

**Returns:**
[Node](../../com.aspose.words/node) - Next node in pre-order order. Null if reached the rootNode.
### nodeTypeToString(int nodeType) {#nodeTypeToString-int-}
```
public static String nodeTypeToString(int nodeType)
```




**Parameters:**
| Parameter | Type | Description |
| --- | --- | --- |
| nodeType | int |  |

**Returns:**
java.lang.String
### notify() {#notify--}
```
public final native void notify()
```




### notifyAll() {#notifyAll--}
```
public final native void notifyAll()
```




### prependChild(Node newChild) {#prependChild-com.aspose.words.Node-}
```
public Node prependChild(Node newChild)
```


Adds the specified node to the beginning of the list of child nodes for this node.

If the newChild is already in the tree, it is first removed.

If the node being inserted was created from another document, you should use **M:Aspose.Words.DocumentBase.ImportNode(Aspose.Words.Node,System.Boolean,Aspose.Words.ImportFormatMode)** to import the node to the current document. The imported node can then be inserted into the current document.

**Parameters:**
| Parameter | Type | Description |
| --- | --- | --- |
| newChild | [Node](../../com.aspose.words/node) | The node to add. |

**Returns:**
[Node](../../com.aspose.words/node) - The node added.
### previousPreOrder(Node rootNode) {#previousPreOrder-com.aspose.words.Node-}
```
public Node previousPreOrder(Node rootNode)
```


Gets the previous node according to the pre-order tree traversal algorithm.

**Parameters:**
| Parameter | Type | Description |
| --- | --- | --- |
| rootNode | [Node](../../com.aspose.words/node) | The top node (limit) of traversal. |

**Returns:**
[Node](../../com.aspose.words/node) - Previous node in pre-order order. Null if reached the rootNode.
### remove() {#remove--}
```
public void remove()
```


Removes itself from the parent.

### removeAllChildren() {#removeAllChildren--}
```
public void removeAllChildren()
```


Removes all the child nodes of the current node.

### removeChild(Node oldChild) {#removeChild-com.aspose.words.Node-}
```
public Node removeChild(Node oldChild)
```


Removes the specified child node.

The parent of oldChild is set to null after the node is removed.

**Parameters:**
| Parameter | Type | Description |
| --- | --- | --- |
| oldChild | [Node](../../com.aspose.words/node) | The node to remove. |

**Returns:**
[Node](../../com.aspose.words/node) - The removed node.
### removeSmartTags() {#removeSmartTags--}
```
public void removeSmartTags()
```


Removes all [SmartTag](../../com.aspose.words/smarttag) descendant nodes of the current node. This method does not remove the content of the smart tags.

### selectNodes(String xpath) {#selectNodes-java.lang.String-}
```
public NodeList selectNodes(String xpath)
```


Selects a list of nodes matching the XPath expression.

Only expressions with element names are supported at the moment. Expressions that use attribute names are not supported.

**Parameters:**
| Parameter | Type | Description |
| --- | --- | --- |
| xpath | java.lang.String | The XPath expression. |

**Returns:**
[NodeList](../../com.aspose.words/nodelist) - A list of nodes matching the XPath query.
### selectSingleNode(String xpath) {#selectSingleNode-java.lang.String-}
```
public Node selectSingleNode(String xpath)
```


Selects the first Node that matches the XPath expression.

Only expressions with element names are supported at the moment. Expressions that use attribute names are not supported.

**Parameters:**
| Parameter | Type | Description |
| --- | --- | --- |
| xpath | java.lang.String | The XPath expression. |

**Returns:**
[Node](../../com.aspose.words/node) - The first Node that matches the XPath query or null if no matching node is found.
### setAbsoluteHorizontalDistance(double value) {#setAbsoluteHorizontalDistance-double-}
```
public void setAbsoluteHorizontalDistance(double value)
```


Sets absolute horizontal floating table position specified by the table properties, in points. Default value is 0.

**Parameters:**
| Parameter | Type | Description |
| --- | --- | --- |
| value | double | Absolute horizontal floating table position specified by the table properties, in points. |

### setAbsoluteVerticalDistance(double value) {#setAbsoluteVerticalDistance-double-}
```
public void setAbsoluteVerticalDistance(double value)
```


Sets absolute vertical floating table position specified by the table properties, in points. Default value is 0.

**Parameters:**
| Parameter | Type | Description |
| --- | --- | --- |
| value | double | Absolute vertical floating table position specified by the table properties, in points. |

### setAlignment(int value) {#setAlignment-int-}
```
public void setAlignment(int value)
```


Specifies how an inline table is aligned in the document.

The default value is [TableAlignment.LEFT](../../com.aspose.words/tablealignment\#LEFT).

**Parameters:**
| Parameter | Type | Description |
| --- | --- | --- |
| value | int | The corresponding  int  value. The value must be one of [TableAlignment](../../com.aspose.words/tablealignment) constants. |

### setAllowAutoFit(boolean value) {#setAllowAutoFit-boolean-}
```
public void setAllowAutoFit(boolean value)
```


Allows Microsoft Word and Aspose.Words to automatically resize cells in a table to fit their contents.

The default value is  true .

**M:Aspose.Words.Tables.Table.AutoFit(Aspose.Words.Tables.AutoFitBehavior)**

**Parameters:**
| Parameter | Type | Description |
| --- | --- | --- |
| value | boolean | The corresponding  boolean  value. |

### setAllowCellSpacing(boolean value) {#setAllowCellSpacing-boolean-}
```
public void setAllowCellSpacing(boolean value)
```


Sets the "Allow spacing between cells" option.

**Parameters:**
| Parameter | Type | Description |
| --- | --- | --- |
| value | boolean | The "Allow spacing between cells" option. |

### setBidi(boolean value) {#setBidi-boolean-}
```
public void setBidi(boolean value)
```


Sets whether this is a right-to-left table.

When  true , the cells in this row are laid out right to left.

The default value is  false .

**Parameters:**
| Parameter | Type | Description |
| --- | --- | --- |
| value | boolean | Whether this is a right-to-left table. |

### setBorder(int borderType, int lineStyle, double lineWidth, Color color, boolean isOverrideCellBorders) {#setBorder-int-int-double-java.awt.Color-boolean-}
```
public void setBorder(int borderType, int lineStyle, double lineWidth, Color color, boolean isOverrideCellBorders)
```




**Parameters:**
| Parameter | Type | Description |
| --- | --- | --- |
| borderType | int |  |
| lineStyle | int |  |
| lineWidth | double |  |
| color | java.awt.Color |  |
| isOverrideCellBorders | boolean |  |

### setBorders(int lineStyle, double lineWidth, Color color) {#setBorders-int-double-java.awt.Color-}
```
public void setBorders(int lineStyle, double lineWidth, Color color)
```




**Parameters:**
| Parameter | Type | Description |
| --- | --- | --- |
| lineStyle | int |  |
| lineWidth | double |  |
| color | java.awt.Color |  |

### setBottomPadding(double value) {#setBottomPadding-double-}
```
public void setBottomPadding(double value)
```


Sets the amount of space (in points) to add below the contents of cells.

**Parameters:**
| Parameter | Type | Description |
| --- | --- | --- |
| value | double | The amount of space (in points) to add below the contents of cells. |

### setCellSpacing(double value) {#setCellSpacing-double-}
```
public void setCellSpacing(double value)
```


Sets the amount of space (in points) between the cells.

**Parameters:**
| Parameter | Type | Description |
| --- | --- | --- |
| value | double | The amount of space (in points) between the cells. |

### setCustomNodeId(int value) {#setCustomNodeId-int-}
```
public void setCustomNodeId(int value)
```


Specifies custom node identifier.

Default is zero.

This identifier can be set and used arbitrarily. For example, as a key to get external data.

Important note, specified value is not saved to an output file and exists only during the node lifetime.

**Parameters:**
| Parameter | Type | Description |
| --- | --- | --- |
| value | int | The corresponding  int  value. |

### setDescription(String value) {#setDescription-java.lang.String-}
```
public void setDescription(String value)
```


Sets description of this table. It provides an alternative text representation of the information contained in the table.

The default value is an empty string.

This property is meaningful for ISO/IEC 29500 compliant DOCX documents ( [OoxmlCompliance](../../com.aspose.words/ooxmlcompliance)). When saved to pre-ISO/IEC 29500 formats, the property is ignored.

**Parameters:**
| Parameter | Type | Description |
| --- | --- | --- |
| value | java.lang.String | Description of this table. |

### setHorizontalAnchor(int value) {#setHorizontalAnchor-int-}
```
public void setHorizontalAnchor(int value)
```


Gets the base object from which the horizontal positioning of floating table should be calculated. Default value is [RelativeHorizontalPosition.COLUMN](../../com.aspose.words/relativehorizontalposition\#COLUMN).

**Parameters:**
| Parameter | Type | Description |
| --- | --- | --- |
| value | int | The base object from which the horizontal positioning of floating table should be calculated. The value must be one of [RelativeHorizontalPosition](../../com.aspose.words/relativehorizontalposition) constants. |

### setLeftIndent(double value) {#setLeftIndent-double-}
```
public void setLeftIndent(double value)
```


Sets the value that represents the left indent of the table.

**Parameters:**
| Parameter | Type | Description |
| --- | --- | --- |
| value | double | The value that represents the left indent of the table. |

### setLeftPadding(double value) {#setLeftPadding-double-}
```
public void setLeftPadding(double value)
```


Sets the amount of space (in points) to add to the left of the contents of cells.

**Parameters:**
| Parameter | Type | Description |
| --- | --- | --- |
| value | double | The amount of space (in points) to add to the left of the contents of cells. |

### setPreferredWidth(PreferredWidth value) {#setPreferredWidth-com.aspose.words.PreferredWidth-}
```
public void setPreferredWidth(PreferredWidth value)
```


Sets the table preferred width.

The default value is [PreferredWidth.AUTO](../../com.aspose.words/preferredwidth\#AUTO).

**Parameters:**
| Parameter | Type | Description |
| --- | --- | --- |
| value | [PreferredWidth](../../com.aspose.words/preferredwidth) | The table preferred width. |

### setRelativeHorizontalAlignment(int value) {#setRelativeHorizontalAlignment-int-}
```
public void setRelativeHorizontalAlignment(int value)
```


Sets floating table relative horizontal alignment.

**Parameters:**
| Parameter | Type | Description |
| --- | --- | --- |
| value | int | Floating table relative horizontal alignment. The value must be one of [HorizontalAlignment](../../com.aspose.words/horizontalalignment) constants. |

### setRelativeVerticalAlignment(int value) {#setRelativeVerticalAlignment-int-}
```
public void setRelativeVerticalAlignment(int value)
```


Sets floating table relative vertical alignment.

**Parameters:**
| Parameter | Type | Description |
| --- | --- | --- |
| value | int | Floating table relative vertical alignment. The value must be one of [VerticalAlignment](../../com.aspose.words/verticalalignment) constants. |

### setRightPadding(double value) {#setRightPadding-double-}
```
public void setRightPadding(double value)
```


Sets the amount of space (in points) to add to the right of the contents of cells.

**Parameters:**
| Parameter | Type | Description |
| --- | --- | --- |
| value | double | The amount of space (in points) to add to the right of the contents of cells. |

### setShading(int texture, Color foregroundColor, Color backgroundColor) {#setShading-int-java.awt.Color-java.awt.Color-}
```
public void setShading(int texture, Color foregroundColor, Color backgroundColor)
```




**Parameters:**
| Parameter | Type | Description |
| --- | --- | --- |
| texture | int |  |
| foregroundColor | java.awt.Color |  |
| backgroundColor | java.awt.Color |  |

### setStyle(Style value) {#setStyle-com.aspose.words.Style-}
```
public void setStyle(Style value)
```


Sets the table style applied to this table.

**Parameters:**
| Parameter | Type | Description |
| --- | --- | --- |
| value | [Style](../../com.aspose.words/style) | The table style applied to this table. |

### setStyleIdentifier(int value) {#setStyleIdentifier-int-}
```
public void setStyleIdentifier(int value)
```


Sets the locale independent style identifier of the table style applied to this table.

**Parameters:**
| Parameter | Type | Description |
| --- | --- | --- |
| value | int | The locale independent style identifier of the table style applied to this table. The value must be one of [StyleIdentifier](../../com.aspose.words/styleidentifier) constants. |

### setStyleName(String value) {#setStyleName-java.lang.String-}
```
public void setStyleName(String value)
```


Sets the name of the table style applied to this table.

**Parameters:**
| Parameter | Type | Description |
| --- | --- | --- |
| value | java.lang.String | The name of the table style applied to this table. |

### setStyleOptions(int value) {#setStyleOptions-int-}
```
public void setStyleOptions(int value)
```


Sets bit flags that specify how a table style is applied to this table.

**Parameters:**
| Parameter | Type | Description |
| --- | --- | --- |
| value | int | Bit flags that specify how a table style is applied to this table. The value must be a bitwise combination of [TableStyleOptions](../../com.aspose.words/tablestyleoptions) constants. |

### setTextWrapping(int value) {#setTextWrapping-int-}
```
public void setTextWrapping(int value)
```


Sets [getTextWrapping()](../../com.aspose.words/table\#getTextWrapping--) / [setTextWrapping(int)](../../com.aspose.words/table\#setTextWrapping-int-) for table.

**Parameters:**
| Parameter | Type | Description |
| --- | --- | --- |
| value | int | \{[getTextWrapping()](../../com.aspose.words/table\#getTextWrapping--) / [setTextWrapping(int)](../../com.aspose.words/table\#setTextWrapping-int-) for table. The value must be one of [TextWrapping](../../com.aspose.words/textwrapping) constants. |

### setTitle(String value) {#setTitle-java.lang.String-}
```
public void setTitle(String value)
```


Sets title of this table. It provides an alternative text representation of the information contained in the table.

The default value is an empty string.

This property is meaningful for ISO/IEC 29500 compliant DOCX documents ( [OoxmlCompliance](../../com.aspose.words/ooxmlcompliance)). When saved to pre-ISO/IEC 29500 formats, the property is ignored.

**Parameters:**
| Parameter | Type | Description |
| --- | --- | --- |
| value | java.lang.String | Title of this table. |

### setTopPadding(double value) {#setTopPadding-double-}
```
public void setTopPadding(double value)
```


Sets the amount of space (in points) to add above the contents of cells.

**Parameters:**
| Parameter | Type | Description |
| --- | --- | --- |
| value | double | The amount of space (in points) to add above the contents of cells. |

### setVerticalAnchor(int value) {#setVerticalAnchor-int-}
```
public void setVerticalAnchor(int value)
```


Gets the base object from which the vertical positioning of floating table should be calculated. Default value is [RelativeVerticalPosition.MARGIN](../../com.aspose.words/relativeverticalposition\#MARGIN).

**Parameters:**
| Parameter | Type | Description |
| --- | --- | --- |
| value | int | The base object from which the vertical positioning of floating table should be calculated. The value must be one of [RelativeVerticalPosition](../../com.aspose.words/relativeverticalposition) constants. |

### toString() {#toString--}
```
public String toString()
```




**Returns:**
java.lang.String
### toString(SaveOptions saveOptions) {#toString-com.aspose.words.SaveOptions-}
```
public String toString(SaveOptions saveOptions)
```


Exports the content of the node into a string using the specified save options.

**Parameters:**
| Parameter | Type | Description |
| --- | --- | --- |
| saveOptions | [SaveOptions](../../com.aspose.words/saveoptions) | Specifies the options that control how the node is saved. |

**Returns:**
java.lang.String - The content of the node in the specified format.
### toString(int saveFormat) {#toString-int-}
```
public String toString(int saveFormat)
```




**Parameters:**
| Parameter | Type | Description |
| --- | --- | --- |
| saveFormat | int |  |

**Returns:**
java.lang.String
### wait() {#wait--}
```
public final void wait()
```




### wait(long arg0) {#wait-long-}
```
public final native void wait(long arg0)
```




**Parameters:**
| Parameter | Type | Description |
| --- | --- | --- |
| arg0 | long |  |

### wait(long arg0, int arg1) {#wait-long-int-}
```
public final void wait(long arg0, int arg1)
```




**Parameters:**
| Parameter | Type | Description |
| --- | --- | --- |
| arg0 | long |  |
| arg1 | int |  |

