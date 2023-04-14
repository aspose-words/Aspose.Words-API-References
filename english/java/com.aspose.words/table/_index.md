---
title: Table
linktitle: Table
second_title: Aspose.Words for Java API Reference
description: Represents a table in a Word document in Java.
type: docs
weight: 557
url: /java/com.aspose.words/table/
---

**Inheritance:**
java.lang.Object, [com.aspose.words.Node](../../com.aspose.words/node/), [com.aspose.words.CompositeNode](../../com.aspose.words/compositenode/)
```
public class Table extends CompositeNode
```

Represents a table in a Word document.

To learn more, visit the [ Working with Tables ][Working with Tables] documentation article.

 **Remarks:** 

[Table](../../com.aspose.words/table/) is a block-level node and can be a child of classes derived from [Story](../../com.aspose.words/story/) or [InlineStory](../../com.aspose.words/inlinestory/).

[Table](../../com.aspose.words/table/) can contain one or more [Row](../../com.aspose.words/row/) nodes.

A minimal valid table needs to have at least one [Row](../../com.aspose.words/row/).

 **Examples:** 

Shows how to create a table.

```

 Document doc = new Document();
 Table table = new Table(doc);
 doc.getFirstSection().getBody().appendChild(table);

 // Tables contain rows, which contain cells, which may have paragraphs
 // with typical elements such as runs, shapes, and even other tables.
 // Calling the "EnsureMinimum" method on a table will ensure that
 // the table has at least one row, cell, and paragraph.
 Row firstRow = new Row(doc);
 table.appendChild(firstRow);

 Cell firstCell = new Cell(doc);
 firstRow.appendChild(firstCell);

 Paragraph paragraph = new Paragraph(doc);
 firstCell.appendChild(paragraph);

 // Add text to the first call in the first row of the table.
 Run run = new Run(doc, "Hello world!");
 paragraph.appendChild(run);

 doc.save(getArtifactsDir() + "Table.CreateTable.docx");
 
```

Shows how to iterate through all tables in the document and print the contents of each cell.

```

 Document doc = new Document(getMyDir() + "Tables.docx");
 TableCollection tables = doc.getFirstSection().getBody().getTables();

 Assert.assertEquals(2, tables.toArray().length);

 for (int i = 0; i < tables.getCount(); i++) {
     System.out.println(MessageFormat.format("Start of Table {0}", i));

     RowCollection rows = tables.get(i).getRows();

     for (int j = 0; j < rows.getCount(); j++) {
         System.out.println(MessageFormat.format("\tStart of Row {0}", j));

         CellCollection cells = rows.get(j).getCells();

         for (int k = 0; k < cells.getCount(); k++) {
             String cellText = cells.get(k).toString(SaveFormat.TEXT).trim();
             System.out.println(MessageFormat.format("\t\tContents of Cell:{0} = \"{1}\"", k, cellText));
         }

         System.out.println(MessageFormat.format("\tEnd of Row {0}", j));
     }

     System.out.println(MessageFormat.format("End of Table {0}\n", i));
 }
 
```

Shows how to build a nested table without using a document builder.

```

 public void createNestedTable() throws Exception {
     Document doc = new Document();

     // Create the outer table with three rows and four columns, and then add it to the document.
     Table outerTable = createTable(doc, 3, 4, "Outer Table");
     doc.getFirstSection().getBody().appendChild(outerTable);

     // Create another table with two rows and two columns and then insert it into the first table's first cell.
     Table innerTable = createTable(doc, 2, 2, "Inner Table");
     outerTable.getFirstRow().getFirstCell().appendChild(innerTable);

     doc.save(getArtifactsDir() + "Table.CreateNestedTable.docx");
 }

 // Creates a new table in the document with the given dimensions and text in each cell.
 private Table createTable(final Document doc, final int rowCount, final int cellCount, final String cellText) throws Exception {
     Table table = new Table(doc);

     for (int rowId = 1; rowId <= rowCount; rowId++) {
         Row row = new Row(doc);
         table.appendChild(row);

         for (int cellId = 1; cellId <= cellCount; cellId++) {
             Cell cell = new Cell(doc);
             cell.appendChild(new Paragraph(doc));
             cell.getFirstParagraph().appendChild(new Run(doc, cellText));

             row.appendChild(cell);
         }
     }

     // You can use the "Title" and "Description" properties to add a title and description respectively to your table.
     // The table must have at least one row before we can use these properties.
     // These properties are meaningful for ISO / IEC 29500 compliant .docx documents (see the OoxmlCompliance class).
     // If we save the document to pre-ISO/IEC 29500 formats, Microsoft Word ignores these properties.
     table.setTitle("Aspose table title");
     table.setDescription("Aspose table description");

     return table;
 }
 
```

Shows how to build a formatted 2x2 table.

```

 Document doc = new Document();
 DocumentBuilder builder = new DocumentBuilder(doc);

 Table table = builder.startTable();
 builder.insertCell();
 builder.getCellFormat().setVerticalAlignment(CellVerticalAlignment.CENTER);
 builder.write("Row 1, cell 1.");
 builder.insertCell();
 builder.write("Row 1, cell 2.");
 builder.endRow();

 // While building the table, the document builder will apply its current RowFormat/CellFormat property values
 // to the current row/cell that its cursor is in and any new rows/cells as it creates them.
 Assert.assertEquals(CellVerticalAlignment.CENTER, table.getRows().get(0).getCells().get(0).getCellFormat().getVerticalAlignment());
 Assert.assertEquals(CellVerticalAlignment.CENTER, table.getRows().get(0).getCells().get(1).getCellFormat().getVerticalAlignment());

 builder.insertCell();
 builder.getRowFormat().setHeight(100.0);
 builder.getRowFormat().setHeightRule(HeightRule.EXACTLY);
 builder.getCellFormat().setOrientation(TextOrientation.UPWARD);
 builder.write("Row 2, cell 1.");
 builder.insertCell();
 builder.getCellFormat().setOrientation(TextOrientation.DOWNWARD);
 builder.write("Row 2, cell 2.");
 builder.endRow();
 builder.endTable();

 // Previously added rows and cells are not retroactively affected by changes to the builder's formatting.
 Assert.assertEquals(0.0, table.getRows().get(0).getRowFormat().getHeight());
 Assert.assertEquals(HeightRule.AUTO, table.getRows().get(0).getRowFormat().getHeightRule());
 Assert.assertEquals(100.0, table.getRows().get(1).getRowFormat().getHeight());
 Assert.assertEquals(HeightRule.EXACTLY, table.getRows().get(1).getRowFormat().getHeightRule());
 Assert.assertEquals(TextOrientation.UPWARD, table.getRows().get(1).getCells().get(0).getCellFormat().getOrientation());
 Assert.assertEquals(TextOrientation.DOWNWARD, table.getRows().get(1).getCells().get(1).getCellFormat().getOrientation());

 doc.save(getArtifactsDir() + "DocumentBuilder.BuildTable.docx");
 
```


[Working with Tables]: https://docs.aspose.com/words/java/working-with-tables/
## Constructors

| Constructor | Description |
| --- | --- |
| [Table(DocumentBase doc)](#Table-com.aspose.words.DocumentBase) | Initializes a new instance of the [Table](../../com.aspose.words/table/) class. |
## Methods

| Method | Description |
| --- | --- |
| [accept(DocumentVisitor visitor)](#accept-com.aspose.words.DocumentVisitor) | Accepts a visitor. |
| [appendChild(Node newChild)](#appendChild-com.aspose.words.Node) | Adds the specified node to the end of the list of child nodes for this node. |
| [autoFit(int behavior)](#autoFit-int) |  |
| [clearBorders()](#clearBorders) | Removes all table and cell borders on this table. |
| [clearShading()](#clearShading) | Removes all shading on the table. |
| [convertToHorizontallyMergedCells()](#convertToHorizontallyMergedCells) | Converts cells horizontally merged by width to cells merged by [CellFormat.getHorizontalMerge()](../../com.aspose.words/cellformat/\#getHorizontalMerge) / [CellFormat.setHorizontalMerge(int)](../../com.aspose.words/cellformat/\#setHorizontalMerge-int). |
| [dd()](#dd) |  |
| [deepClone(boolean isCloneChildren)](#deepClone-boolean) | Creates a duplicate of the node. |
| [ensureMinimum()](#ensureMinimum) | If the table has no rows, creates and appends one [Row](../../com.aspose.words/row/). |
| [equals(Object arg0)](#equals-java.lang.Object) |  |
| [getAbsoluteHorizontalDistance()](#getAbsoluteHorizontalDistance) | Gets absolute horizontal floating table position specified by the table properties, in points. |
| [getAbsoluteVerticalDistance()](#getAbsoluteVerticalDistance) | Gets absolute vertical floating table position specified by the table properties, in points. |
| [getAlignment()](#getAlignment) | Specifies how an inline table is aligned in the document. |
| [getAllowAutoFit()](#getAllowAutoFit) | Allows Microsoft Word and Aspose.Words to automatically resize cells in a table to fit their contents. |
| [getAllowCellSpacing()](#getAllowCellSpacing) | Gets the "Allow spacing between cells" option. |
| [getAllowOverlap()](#getAllowOverlap) | Gets whether a floating table shall allow other floating objects in the document to overlap its extents when displayed. |
| [getAncestor(int ancestorType)](#getAncestor-int) |  |
| [getAncestor(Class ancestorType)](#getAncestor-java.lang.Class) | Gets the first ancestor of the specified object type. |
| [getBidi()](#getBidi) | Gets whether this is a right-to-left table. |
| [getBottomPadding()](#getBottomPadding) | Gets the amount of space (in points) to add below the contents of cells. |
| [getCellSpacing()](#getCellSpacing) | Gets the amount of space (in points) between the cells. |
| [getChild(int nodeType, int index, boolean isDeep)](#getChild-int-int-boolean) |  |
| [getChildNodes()](#getChildNodes) | Gets all immediate child nodes of this node. |
| [getChildNodes(int nodeType, boolean isDeep)](#getChildNodes-int-boolean) |  |
| [getClass()](#getClass) |  |
| [getContainer()](#getContainer) |  |
| [getCount()](#getCount) | Gets the number of immediate children of this node. |
| [getCurrentNode()](#getCurrentNode) |  |
| [getCustomNodeId()](#getCustomNodeId) | Specifies custom node identifier. |
| [getDescription()](#getDescription) | Gets description of this table. |
| [getDistanceBottom()](#getDistanceBottom) | Gets distance between table bottom and the surrounding text, in points. |
| [getDistanceLeft()](#getDistanceLeft) | Gets distance between table left and the surrounding text, in points. |
| [getDistanceRight()](#getDistanceRight) | Gets distance between table right and the surrounding text, in points. |
| [getDistanceTop()](#getDistanceTop) | Gets distance between table top and the surrounding text, in points. |
| [getDocument()](#getDocument) | Gets the document to which this node belongs. |
| [getFirstChild()](#getFirstChild) | Gets the first child of the node. |
| [getFirstRow()](#getFirstRow) | Returns the first [Row](../../com.aspose.words/row/) node in the table. |
| [getHorizontalAnchor()](#getHorizontalAnchor) | Gets the base object from which the horizontal positioning of floating table should be calculated. |
| [getLastChild()](#getLastChild) | Gets the last child of the node. |
| [getLastRow()](#getLastRow) | Returns the last [Row](../../com.aspose.words/row/) node in the table. |
| [getLeftIndent()](#getLeftIndent) | Gets the value that represents the left indent of the table. |
| [getLeftPadding()](#getLeftPadding) | Gets the amount of space (in points) to add to the left of the contents of cells. |
| [getNextMatchingNode(Node curNode)](#getNextMatchingNode-com.aspose.words.Node) |  |
| [getNextSibling()](#getNextSibling) | Gets the node immediately following this node. |
| [getNodeType()](#getNodeType) | Returns [NodeType.TABLE](../../com.aspose.words/nodetype/\#TABLE). |
| [getParentNode()](#getParentNode) | Gets the immediate parent of this node. |
| [getPreferredWidth()](#getPreferredWidth) | Gets the table preferred width. |
| [getPreviousSibling()](#getPreviousSibling) | Gets the node immediately preceding this node. |
| [getRange()](#getRange) | Returns a [Range](../../com.aspose.words/range/) object that represents the portion of a document that is contained in this node. |
| [getRelativeHorizontalAlignment()](#getRelativeHorizontalAlignment) | Gets floating table relative horizontal alignment. |
| [getRelativeVerticalAlignment()](#getRelativeVerticalAlignment) | Gets floating table relative vertical alignment. |
| [getRightPadding()](#getRightPadding) | Gets the amount of space (in points) to add to the right of the contents of cells. |
| [getRows()](#getRows) | Provides typed access to the rows of the table. |
| [getStyle()](#getStyle) | Gets the table style applied to this table. |
| [getStyleIdentifier()](#getStyleIdentifier) | Gets the locale independent style identifier of the table style applied to this table. |
| [getStyleName()](#getStyleName) | Gets the name of the table style applied to this table. |
| [getStyleOptions()](#getStyleOptions) | Gets bit flags that specify how a table style is applied to this table. |
| [getText()](#getText) | Gets the text of this node and of all its children. |
| [getTextWrapping()](#getTextWrapping) | Gets [getTextWrapping()](../../com.aspose.words/table/\#getTextWrapping) / [setTextWrapping(int)](../../com.aspose.words/table/\#setTextWrapping-int) for table. |
| [getTitle()](#getTitle) | Gets title of this table. |
| [getTopPadding()](#getTopPadding) | Gets the amount of space (in points) to add above the contents of cells. |
| [getVerticalAnchor()](#getVerticalAnchor) | Gets the base object from which the vertical positioning of floating table should be calculated. |
| [hasChildNodes()](#hasChildNodes) | Returns  true  if this node has any child nodes. |
| [hashCode()](#hashCode) |  |
| [indexOf(Node child)](#indexOf-com.aspose.words.Node) | Returns the index of the specified child node in the child node array. |
| [insertAfter(Node newChild, Node refChild)](#insertAfter-com.aspose.words.Node-com.aspose.words.Node) | Inserts the specified node immediately after the specified reference node. |
| [insertBefore(Node newChild, Node refChild)](#insertBefore-com.aspose.words.Node-com.aspose.words.Node) | Inserts the specified node immediately before the specified reference node. |
| [isComposite()](#isComposite) | Returns  true  as this node can have child nodes. |
| [iterator()](#iterator) | Provides support for the for each style iteration over the child nodes of this node. |
| [nextPreOrder(Node rootNode)](#nextPreOrder-com.aspose.words.Node) | Gets next node according to the pre-order tree traversal algorithm. |
| [nodeTypeToString(int nodeType)](#nodeTypeToString-int) |  |
| [notify()](#notify) |  |
| [notifyAll()](#notifyAll) |  |
| [prependChild(Node newChild)](#prependChild-com.aspose.words.Node) | Adds the specified node to the beginning of the list of child nodes for this node. |
| [previousPreOrder(Node rootNode)](#previousPreOrder-com.aspose.words.Node) | Gets the previous node according to the pre-order tree traversal algorithm. |
| [remove()](#remove) | Removes itself from the parent. |
| [removeAllChildren()](#removeAllChildren) | Removes all the child nodes of the current node. |
| [removeChild(Node oldChild)](#removeChild-com.aspose.words.Node) | Removes the specified child node. |
| [removeSmartTags()](#removeSmartTags) | Removes all [SmartTag](../../com.aspose.words/smarttag/) descendant nodes of the current node. |
| [selectNodes(String xpath)](#selectNodes-java.lang.String) | Selects a list of nodes matching the XPath expression. |
| [selectSingleNode(String xpath)](#selectSingleNode-java.lang.String) | Selects the first [Node](../../com.aspose.words/node/) that matches the XPath expression. |
| [setAbsoluteHorizontalDistance(double value)](#setAbsoluteHorizontalDistance-double) | Sets absolute horizontal floating table position specified by the table properties, in points. |
| [setAbsoluteVerticalDistance(double value)](#setAbsoluteVerticalDistance-double) | Sets absolute vertical floating table position specified by the table properties, in points. |
| [setAlignment(int value)](#setAlignment-int) | Specifies how an inline table is aligned in the document. |
| [setAllowAutoFit(boolean value)](#setAllowAutoFit-boolean) | Allows Microsoft Word and Aspose.Words to automatically resize cells in a table to fit their contents. |
| [setAllowCellSpacing(boolean value)](#setAllowCellSpacing-boolean) | Sets the "Allow spacing between cells" option. |
| [setBidi(boolean value)](#setBidi-boolean) | Sets whether this is a right-to-left table. |
| [setBorder(int borderType, int lineStyle, double lineWidth, Color color, boolean isOverrideCellBorders)](#setBorder-int-int-double-java.awt.Color-boolean) |  |
| [setBorders(int lineStyle, double lineWidth, Color color)](#setBorders-int-double-java.awt.Color) |  |
| [setBottomPadding(double value)](#setBottomPadding-double) | Sets the amount of space (in points) to add below the contents of cells. |
| [setCellSpacing(double value)](#setCellSpacing-double) | Sets the amount of space (in points) between the cells. |
| [setCustomNodeId(int value)](#setCustomNodeId-int) | Specifies custom node identifier. |
| [setDescription(String value)](#setDescription-java.lang.String) | Sets description of this table. |
| [setDistanceBottom(double value)](#setDistanceBottom-double) | Sets distance between table bottom and the surrounding text, in points. |
| [setDistanceLeft(double value)](#setDistanceLeft-double) | Sets distance between table left and the surrounding text, in points. |
| [setDistanceRight(double value)](#setDistanceRight-double) | Sets distance between table right and the surrounding text, in points. |
| [setDistanceTop(double value)](#setDistanceTop-double) | Sets distance between table top and the surrounding text, in points. |
| [setHorizontalAnchor(int value)](#setHorizontalAnchor-int) | Gets the base object from which the horizontal positioning of floating table should be calculated. |
| [setLeftIndent(double value)](#setLeftIndent-double) | Sets the value that represents the left indent of the table. |
| [setLeftPadding(double value)](#setLeftPadding-double) | Sets the amount of space (in points) to add to the left of the contents of cells. |
| [setPreferredWidth(PreferredWidth value)](#setPreferredWidth-com.aspose.words.PreferredWidth) | Sets the table preferred width. |
| [setRelativeHorizontalAlignment(int value)](#setRelativeHorizontalAlignment-int) | Sets floating table relative horizontal alignment. |
| [setRelativeVerticalAlignment(int value)](#setRelativeVerticalAlignment-int) | Sets floating table relative vertical alignment. |
| [setRightPadding(double value)](#setRightPadding-double) | Sets the amount of space (in points) to add to the right of the contents of cells. |
| [setShading(int texture, Color foregroundColor, Color backgroundColor)](#setShading-int-java.awt.Color-java.awt.Color) |  |
| [setStyle(Style value)](#setStyle-com.aspose.words.Style) | Sets the table style applied to this table. |
| [setStyleIdentifier(int value)](#setStyleIdentifier-int) | Sets the locale independent style identifier of the table style applied to this table. |
| [setStyleName(String value)](#setStyleName-java.lang.String) | Sets the name of the table style applied to this table. |
| [setStyleOptions(int value)](#setStyleOptions-int) | Sets bit flags that specify how a table style is applied to this table. |
| [setTextWrapping(int value)](#setTextWrapping-int) | Sets [getTextWrapping()](../../com.aspose.words/table/\#getTextWrapping) / [setTextWrapping(int)](../../com.aspose.words/table/\#setTextWrapping-int) for table. |
| [setTitle(String value)](#setTitle-java.lang.String) | Sets title of this table. |
| [setTopPadding(double value)](#setTopPadding-double) | Sets the amount of space (in points) to add above the contents of cells. |
| [setVerticalAnchor(int value)](#setVerticalAnchor-int) | Gets the base object from which the vertical positioning of floating table should be calculated. |
| [toString()](#toString) |  |
| [toString(SaveOptions saveOptions)](#toString-com.aspose.words.SaveOptions) | Exports the content of the node into a string using the specified save options. |
| [toString(int saveFormat)](#toString-int) |  |
| [wait()](#wait) |  |
| [wait(long arg0)](#wait-long) |  |
| [wait(long arg0, int arg1)](#wait-long-int) |  |
### Table(DocumentBase doc) {#Table-com.aspose.words.DocumentBase}
```
public Table(DocumentBase doc)
```


Initializes a new instance of the [Table](../../com.aspose.words/table/) class.

 **Remarks:** 

When [Table](../../com.aspose.words/table/) is created, it belongs to the specified document, but is not yet part of the document and [Node.getParentNode()](../../com.aspose.words/node/\#getParentNode) is  null .

To append [Table](../../com.aspose.words/table/) to the document use [CompositeNode.insertAfter(com.aspose.words.Node, com.aspose.words.Node)](../../com.aspose.words/compositenode/\#insertAfter-com.aspose.words.Node--com.aspose.words.Node) or [CompositeNode.insertBefore(com.aspose.words.Node, com.aspose.words.Node)](../../com.aspose.words/compositenode/\#insertBefore-com.aspose.words.Node--com.aspose.words.Node) on the story where you want the table inserted.

**Parameters:**
| Parameter | Type | Description |
| --- | --- | --- |
| doc | [DocumentBase](../../com.aspose.words/documentbase/) | The owner document.

 **Examples:** 

Shows how to create a table.

```

 Document doc = new Document();
 Table table = new Table(doc);
 doc.getFirstSection().getBody().appendChild(table);

 // Tables contain rows, which contain cells, which may have paragraphs
 // with typical elements such as runs, shapes, and even other tables.
 // Calling the "EnsureMinimum" method on a table will ensure that
 // the table has at least one row, cell, and paragraph.
 Row firstRow = new Row(doc);
 table.appendChild(firstRow);

 Cell firstCell = new Cell(doc);
 firstRow.appendChild(firstCell);

 Paragraph paragraph = new Paragraph(doc);
 firstCell.appendChild(paragraph);

 // Add text to the first call in the first row of the table.
 Run run = new Run(doc, "Hello world!");
 paragraph.appendChild(run);

 doc.save(getArtifactsDir() + "Table.CreateTable.docx");
 
```

Shows how to build a nested table without using a document builder.

```

 public void createNestedTable() throws Exception {
     Document doc = new Document();

     // Create the outer table with three rows and four columns, and then add it to the document.
     Table outerTable = createTable(doc, 3, 4, "Outer Table");
     doc.getFirstSection().getBody().appendChild(outerTable);

     // Create another table with two rows and two columns and then insert it into the first table's first cell.
     Table innerTable = createTable(doc, 2, 2, "Inner Table");
     outerTable.getFirstRow().getFirstCell().appendChild(innerTable);

     doc.save(getArtifactsDir() + "Table.CreateNestedTable.docx");
 }

 // Creates a new table in the document with the given dimensions and text in each cell.
 private Table createTable(final Document doc, final int rowCount, final int cellCount, final String cellText) throws Exception {
     Table table = new Table(doc);

     for (int rowId = 1; rowId <= rowCount; rowId++) {
         Row row = new Row(doc);
         table.appendChild(row);

         for (int cellId = 1; cellId <= cellCount; cellId++) {
             Cell cell = new Cell(doc);
             cell.appendChild(new Paragraph(doc));
             cell.getFirstParagraph().appendChild(new Run(doc, cellText));

             row.appendChild(cell);
         }
     }

     // You can use the "Title" and "Description" properties to add a title and description respectively to your table.
     // The table must have at least one row before we can use these properties.
     // These properties are meaningful for ISO / IEC 29500 compliant .docx documents (see the OoxmlCompliance class).
     // If we save the document to pre-ISO/IEC 29500 formats, Microsoft Word ignores these properties.
     table.setTitle("Aspose table title");
     table.setDescription("Aspose table description");

     return table;
 }
 
``` |

### accept(DocumentVisitor visitor) {#accept-com.aspose.words.DocumentVisitor}
```
public boolean accept(DocumentVisitor visitor)
```


Accepts a visitor.

 **Remarks:** 

Enumerates over this node and all of its children. Each node calls a corresponding method on [DocumentVisitor](../../com.aspose.words/documentvisitor/).

For more info see the Visitor design pattern.

**Parameters:**
| Parameter | Type | Description |
| --- | --- | --- |
| visitor | [DocumentVisitor](../../com.aspose.words/documentvisitor/) | The visitor that will visit the nodes. |

**Returns:**
boolean - True if all nodes were visited; false if [DocumentVisitor](../../com.aspose.words/documentvisitor/) stopped the operation before visiting all nodes.

 **Remarks:** 

Calls [DocumentVisitor.visitTableStart(com.aspose.words.Table)](../../com.aspose.words/documentvisitor/\#visitTableStart-com.aspose.words.Table), then calls [Node.accept(com.aspose.words.DocumentVisitor)](../../com.aspose.words/node/\#accept-com.aspose.words.DocumentVisitor) for all child nodes of the section and calls [DocumentVisitor.visitTableEnd(com.aspose.words.Table)](../../com.aspose.words/documentvisitor/\#visitTableEnd-com.aspose.words.Table) at the end.

 **Examples:** 

Shows how to use a DocumentVisitor implementation to remove all hidden content from a document.

```

 public void removeHiddenContentFromDocument() throws Exception {
     Document doc = new Document(getMyDir() + "Hidden content.docx");
     RemoveHiddenContentVisitor hiddenContentRemover = new RemoveHiddenContentVisitor();

     // Below are three types of fields which can accept a document visitor,
     // which will allow it to visit the accepting node, and then traverse its child nodes in a depth-first manner.
     // 1 -  Paragraph node:
     Paragraph para = (Paragraph) doc.getChild(NodeType.PARAGRAPH, 4, true);
     para.accept(hiddenContentRemover);

     // 2 -  Table node:
     Table table = doc.getFirstSection().getBody().getTables().get(0);
     table.accept(hiddenContentRemover);

     // 3 -  Document node:
     doc.accept(hiddenContentRemover);

     doc.save(getArtifactsDir() + "Font.RemoveHiddenContentFromDocument.docx");
 }

 /// 
 /// Removes all visited nodes marked as "hidden content".
 /// 
 public static class RemoveHiddenContentVisitor extends DocumentVisitor {
     /// 
     /// Called when a FieldStart node is encountered in the document.
     /// 
     public int visitFieldStart(FieldStart fieldStart) {
         if (fieldStart.getFont().getHidden())
             fieldStart.remove();

         return VisitorAction.CONTINUE;
     }

     /// 
     /// Called when a FieldEnd node is encountered in the document.
     /// 
     public int visitFieldEnd(FieldEnd fieldEnd) {
         if (fieldEnd.getFont().getHidden())
             fieldEnd.remove();

         return VisitorAction.CONTINUE;
     }

     /// 
     /// Called when a FieldSeparator node is encountered in the document.
     /// 
     public int visitFieldSeparator(FieldSeparator fieldSeparator) {
         if (fieldSeparator.getFont().getHidden())
             fieldSeparator.remove();

         return VisitorAction.CONTINUE;
     }

     /// 
     /// Called when a Run node is encountered in the document.
     /// 
     public int visitRun(Run run) {
         if (run.getFont().getHidden())
             run.remove();

         return VisitorAction.CONTINUE;
     }

     /// 
     /// Called when a Paragraph node is encountered in the document.
     /// 
     public int visitParagraphStart(Paragraph paragraph) {
         if (paragraph.getParagraphBreakFont().getHidden())
             paragraph.remove();

         return VisitorAction.CONTINUE;
     }

     /// 
     /// Called when a FormField is encountered in the document.
     /// 
     public int visitFormField(FormField formField) {
         if (formField.getFont().getHidden())
             formField.remove();

         return VisitorAction.CONTINUE;
     }

     /// 
     /// Called when a GroupShape is encountered in the document.
     /// 
     public int visitGroupShapeStart(GroupShape groupShape) {
         if (groupShape.getFont().getHidden())
             groupShape.remove();

         return VisitorAction.CONTINUE;
     }

     /// 
     /// Called when a Shape is encountered in the document.
     /// 
     public int visitShapeStart(Shape shape) {
         if (shape.getFont().getHidden())
             shape.remove();

         return VisitorAction.CONTINUE;
     }

     /// 
     /// Called when a Comment is encountered in the document.
     /// 
     public int visitCommentStart(Comment comment) {
         if (comment.getFont().getHidden())
             comment.remove();

         return VisitorAction.CONTINUE;
     }

     /// 
     /// Called when a Footnote is encountered in the document.
     /// 
     public int visitFootnoteStart(Footnote footnote) {
         if (footnote.getFont().getHidden())
             footnote.remove();

         return VisitorAction.CONTINUE;
     }

     /// 
     /// Called when a SpecialCharacter is encountered in the document.
     /// 
     public int visitSpecialChar(SpecialChar specialChar) {
         if (specialChar.getFont().getHidden())
             specialChar.remove();

         return VisitorAction.CONTINUE;
     }

     /// 
     /// Called when visiting of a Table node is ended in the document.
     /// 
     public int visitTableEnd(Table table) {
         // The content inside table cells may have the hidden content flag, but the tables themselves cannot.
         // If this table had nothing but hidden content, this visitor would have removed all of it,
         // and there would be no child nodes left.
         // Thus, we can also treat the table itself as hidden content and remove it.
         // Tables which are empty but do not have hidden content will have cells with empty paragraphs inside,
         // which this visitor will not remove.
         if (!table.hasChildNodes())
             table.remove();

         return VisitorAction.CONTINUE;
     }

     /// 
     /// Called when visiting of a Cell node is ended in the document.
     /// 
     public int visitCellEnd(Cell cell) {
         if (!cell.hasChildNodes() && cell.getParentNode() != null)
             cell.remove();

         return VisitorAction.CONTINUE;
     }

     /// 
     /// Called when visiting of a Row node is ended in the document.
     /// 
     public int visitRowEnd(Row row) {
         if (!row.hasChildNodes() && row.getParentNode() != null)
             row.remove();

         return VisitorAction.CONTINUE;
     }
 }
 
```
### appendChild(Node newChild) {#appendChild-com.aspose.words.Node}
```
public Node appendChild(Node newChild)
```


Adds the specified node to the end of the list of child nodes for this node.

 **Remarks:** 

If the  newChild  is already in the tree, it is first removed.

If the node being inserted was created from another document, you should use **M:Aspose.Words.DocumentBase.ImportNode(Aspose.Words.Node,System.Boolean,Aspose.Words.ImportFormatMode)** to import the node to the current document. The imported node can then be inserted into the current document.

**Parameters:**
| Parameter | Type | Description |
| --- | --- | --- |
| newChild | [Node](../../com.aspose.words/node/) | The node to add. |

**Returns:**
[Node](../../com.aspose.words/node/) - The node added.

 **Examples:** 

Shows how to construct an Aspose.Words document by hand.

```

 Document doc = new Document();

 // A blank document contains one section, one body and one paragraph.
 // Call the "RemoveAllChildren" method to remove all those nodes,
 // and end up with a document node with no children.
 doc.removeAllChildren();

 // This document now has no composite child nodes that we can add content to.
 // If we wish to edit it, we will need to repopulate its node collection.
 // First, create a new section, and then append it as a child to the root document node.
 Section section = new Section(doc);
 doc.appendChild(section);

 // Set some page setup properties for the section.
 section.getPageSetup().setSectionStart(SectionStart.NEW_PAGE);
 section.getPageSetup().setPaperSize(PaperSize.LETTER);

 // A section needs a body, which will contain and display all its contents
 // on the page between the section's header and footer.
 Body body = new Body(doc);
 section.appendChild(body);

 // Create a paragraph, set some formatting properties, and then append it as a child to the body.
 Paragraph para = new Paragraph(doc);

 para.getParagraphFormat().setStyleName("Heading 1");
 para.getParagraphFormat().setAlignment(ParagraphAlignment.CENTER);

 body.appendChild(para);

 // Finally, add some content to do the document. Create a run,
 // set its appearance and contents, and then append it as a child to the paragraph.
 Run run = new Run(doc);
 run.setText("Hello World!");
 run.getFont().setColor(Color.RED);
 para.appendChild(run);

 Assert.assertEquals("Hello World!", doc.getText().trim());

 doc.save(getArtifactsDir() + "Section.CreateManually.docx");
 
```
### autoFit(int behavior) {#autoFit-int}
```
public void autoFit(int behavior)
```




**Parameters:**
| Parameter | Type | Description |
| --- | --- | --- |
| behavior | int |  |

### clearBorders() {#clearBorders}
```
public void clearBorders()
```


Removes all table and cell borders on this table.

 **Examples:** 

Shows how to apply an outline border to a table.

```

 Document doc = new Document(getMyDir() + "Tables.docx");
 Table table = doc.getFirstSection().getBody().getTables().get(0);

 // Align the table to the center of the page.
 table.setAlignment(TableAlignment.CENTER);

 // Clear any existing borders and shading from the table.
 table.clearBorders();
 table.clearShading();

 // Add green borders to the outline of the table.
 table.setBorder(BorderType.LEFT, LineStyle.SINGLE, 1.5, Color.GREEN, true);
 table.setBorder(BorderType.RIGHT, LineStyle.SINGLE, 1.5, Color.GREEN, true);
 table.setBorder(BorderType.TOP, LineStyle.SINGLE, 1.5, Color.GREEN, true);
 table.setBorder(BorderType.BOTTOM, LineStyle.SINGLE, 1.5, Color.GREEN, true);

 // Fill the cells with a light green solid color.
 table.setShading(TextureIndex.TEXTURE_SOLID, Color.GREEN, Color.GREEN);

 doc.save(getArtifactsDir() + "Table.SetOutlineBorders.docx");
 
```

Shows how to remove all borders from a table.

```

 Document doc = new Document();
 DocumentBuilder builder = new DocumentBuilder(doc);

 Table table = builder.startTable();
 builder.insertCell();
 builder.write("Hello world!");
 builder.endTable();

 // Modify the color and thickness of the top border.
 Border topBorder = table.getFirstRow().getRowFormat().getBorders().getByBorderType(BorderType.TOP);
 table.setBorder(BorderType.TOP, LineStyle.DOUBLE, 1.5, Color.RED, true);

 Assert.assertEquals(1.5d, topBorder.getLineWidth());
 Assert.assertEquals(Color.RED.getRGB(), topBorder.getColor().getRGB());
 Assert.assertEquals(LineStyle.DOUBLE, topBorder.getLineStyle());

 // Clear the borders of all cells in the table, and then save the document.
 table.clearBorders();

 Border finalTopBorder = topBorder;
 doc.save(getArtifactsDir() + "Table.ClearBorders.docx");

 // Verify the values of the table's properties after re-opening the document.
 doc = new Document(getArtifactsDir() + "Table.ClearBorders.docx");
 table = doc.getFirstSection().getBody().getTables().get(0);
 topBorder = table.getFirstRow().getRowFormat().getBorders().getByBorderType(BorderType.TOP);

 Assert.assertEquals(0.0d, topBorder.getLineWidth());
 Assert.assertEquals(0, topBorder.getColor().getRGB());
 Assert.assertEquals(LineStyle.NONE, topBorder.getLineStyle());
 
```

### clearShading() {#clearShading}
```
public void clearShading()
```


Removes all shading on the table.

 **Examples:** 

Shows how to apply an outline border to a table.

```

 Document doc = new Document(getMyDir() + "Tables.docx");
 Table table = doc.getFirstSection().getBody().getTables().get(0);

 // Align the table to the center of the page.
 table.setAlignment(TableAlignment.CENTER);

 // Clear any existing borders and shading from the table.
 table.clearBorders();
 table.clearShading();

 // Add green borders to the outline of the table.
 table.setBorder(BorderType.LEFT, LineStyle.SINGLE, 1.5, Color.GREEN, true);
 table.setBorder(BorderType.RIGHT, LineStyle.SINGLE, 1.5, Color.GREEN, true);
 table.setBorder(BorderType.TOP, LineStyle.SINGLE, 1.5, Color.GREEN, true);
 table.setBorder(BorderType.BOTTOM, LineStyle.SINGLE, 1.5, Color.GREEN, true);

 // Fill the cells with a light green solid color.
 table.setShading(TextureIndex.TEXTURE_SOLID, Color.GREEN, Color.GREEN);

 doc.save(getArtifactsDir() + "Table.SetOutlineBorders.docx");
 
```

### convertToHorizontallyMergedCells() {#convertToHorizontallyMergedCells}
```
public void convertToHorizontallyMergedCells()
```


Converts cells horizontally merged by width to cells merged by [CellFormat.getHorizontalMerge()](../../com.aspose.words/cellformat/\#getHorizontalMerge) / [CellFormat.setHorizontalMerge(int)](../../com.aspose.words/cellformat/\#setHorizontalMerge-int).

 **Remarks:** 

Table cells can be horizontally merged either using merge flags [CellFormat.getHorizontalMerge()](../../com.aspose.words/cellformat/\#getHorizontalMerge) / [CellFormat.setHorizontalMerge(int)](../../com.aspose.words/cellformat/\#setHorizontalMerge-int) or using cell width [CellFormat.getWidth()](../../com.aspose.words/cellformat/\#getWidth) / [CellFormat.setWidth(double)](../../com.aspose.words/cellformat/\#setWidth-double).

When table cell is merged by width property [CellFormat.getHorizontalMerge()](../../com.aspose.words/cellformat/\#getHorizontalMerge) / [CellFormat.setHorizontalMerge(int)](../../com.aspose.words/cellformat/\#setHorizontalMerge-int) is meaningless but sometimes having merge flags is more convenient way.

Use this method to transforms table cells horizontally merged by width to cells merged by merge flags.

 **Examples:** 

Shows how to convert cells horizontally merged by width to cells merged by CellFormat.HorizontalMerge.

```

 Document doc = new Document(getMyDir() + "Table with merged cells.docx");

 // Microsoft Word does not write merge flags anymore, defining merged cells by width instead.
 // Aspose.Words by default define only 5 cells in a row, and none of them have the horizontal merge flag,
 // even though there were 7 cells in the row before the horizontal merging took place.
 Table table = doc.getFirstSection().getBody().getTables().get(0);
 Row row = table.getRows().get(0);

 Assert.assertEquals(5, row.getCells().getCount());
 Assert.assertTrue(IterableUtils.matchesAll(row.getCells(), s -> s.getCellFormat().getHorizontalMerge() == CellMerge.NONE));

 // Use the "ConvertToHorizontallyMergedCells" method to convert cells horizontally merged
 // by its width to the cell horizontally merged by flags.
 // Now, we have 7 cells, and some of them have horizontal merge values.
 table.convertToHorizontallyMergedCells();
 row = table.getRows().get(0);

 Assert.assertEquals(7, row.getCells().getCount());

 Assert.assertEquals(CellMerge.NONE, row.getCells().get(0).getCellFormat().getHorizontalMerge());
 Assert.assertEquals(CellMerge.FIRST, row.getCells().get(1).getCellFormat().getHorizontalMerge());
 Assert.assertEquals(CellMerge.PREVIOUS, row.getCells().get(2).getCellFormat().getHorizontalMerge());
 Assert.assertEquals(CellMerge.NONE, row.getCells().get(3).getCellFormat().getHorizontalMerge());
 Assert.assertEquals(CellMerge.FIRST, row.getCells().get(4).getCellFormat().getHorizontalMerge());
 Assert.assertEquals(CellMerge.PREVIOUS, row.getCells().get(5).getCellFormat().getHorizontalMerge());
 Assert.assertEquals(CellMerge.NONE, row.getCells().get(6).getCellFormat().getHorizontalMerge());
 
```

### dd() {#dd}
```
public void dd()
```




### deepClone(boolean isCloneChildren) {#deepClone-boolean}
```
public Node deepClone(boolean isCloneChildren)
```


Creates a duplicate of the node.

 **Remarks:** 

This method serves as a copy constructor for nodes. The cloned node has no parent, but belongs to the same document as the original node.

This method always performs a deep copy of the node. The  isCloneChildren  parameter specifies whether to perform copy all child nodes as well.

**Parameters:**
| Parameter | Type | Description |
| --- | --- | --- |
| isCloneChildren | boolean | True to recursively clone the subtree under the specified node; false to clone only the node itself. |

**Returns:**
[Node](../../com.aspose.words/node/) - The cloned node.

 **Examples:** 

Shows how to clone a composite node.

```

 Document doc = new Document();
 Paragraph para = doc.getFirstSection().getBody().getFirstParagraph();
 para.appendChild(new Run(doc, "Hello world!"));

 // Below are two ways of cloning a composite node.
 // 1 -  Create a clone of a node, and create a clone of each of its child nodes as well.
 Node cloneWithChildren = para.deepClone(true);

 Assert.assertTrue(((CompositeNode) cloneWithChildren).hasChildNodes());
 Assert.assertEquals("Hello world!", cloneWithChildren.getText().trim());

 // 2 -  Create a clone of a node just by itself without any children.
 Node cloneWithoutChildren = para.deepClone(false);

 Assert.assertFalse(((CompositeNode) cloneWithoutChildren).hasChildNodes());
 Assert.assertEquals("", cloneWithoutChildren.getText().trim());
 
```
### ensureMinimum() {#ensureMinimum}
```
public void ensureMinimum()
```


If the table has no rows, creates and appends one [Row](../../com.aspose.words/row/).

 **Examples:** 

Shows how to ensure that a table node contains the nodes we need to add content.

```

 Document doc = new Document();
 Table table = new Table(doc);
 doc.getFirstSection().getBody().appendChild(table);

 // Tables contain rows, which contain cells, which may contain paragraphs
 // with typical elements such as runs, shapes, and even other tables.
 // Our new table has none of these nodes, and we cannot add contents to it until it does.
 Assert.assertEquals(0, table.getChildNodes(NodeType.ANY, true).getCount());

 // Calling the "EnsureMinimum" method on a table will ensure that
 // the table has at least one row and one cell with an empty paragraph.
 table.ensureMinimum();
 table.getFirstRow().getFirstCell().getFirstParagraph().appendChild(new Run(doc, "Hello world!"));
 
```

### equals(Object arg0) {#equals-java.lang.Object}
```
public boolean equals(Object arg0)
```




**Parameters:**
| Parameter | Type | Description |
| --- | --- | --- |
| arg0 | java.lang.Object |  |

**Returns:**
boolean
### getAbsoluteHorizontalDistance() {#getAbsoluteHorizontalDistance}
```
public double getAbsoluteHorizontalDistance()
```


Gets absolute horizontal floating table position specified by the table properties, in points. Default value is 0.

 **Examples:** 

Shows how set the location of floating tables.

```

 Document doc = new Document();
 DocumentBuilder builder = new DocumentBuilder(doc);

 Table table = builder.startTable();
 builder.insertCell();
 builder.write("Table 1, cell 1");
 builder.endTable();
 table.setPreferredWidth(PreferredWidth.fromPoints(300.0));

 // Set the table's location to a place on the page, such as, in this case, the bottom right corner.
 table.setRelativeVerticalAlignment(VerticalAlignment.BOTTOM);
 table.setRelativeHorizontalAlignment(HorizontalAlignment.RIGHT);

 table = builder.startTable();
 builder.insertCell();
 builder.write("Table 2, cell 1");
 builder.endTable();
 table.setPreferredWidth(PreferredWidth.fromPoints(300.0));

 // We can also set a horizontal and vertical offset in points from the paragraph's location where we inserted the table.
 table.setAbsoluteVerticalDistance(50.0);
 table.setAbsoluteHorizontalDistance(100.0);

 doc.save(getArtifactsDir() + "Table.ChangeFloatingTableProperties.docx");
 
```

**Returns:**
double - Absolute horizontal floating table position specified by the table properties, in points.
### getAbsoluteVerticalDistance() {#getAbsoluteVerticalDistance}
```
public double getAbsoluteVerticalDistance()
```


Gets absolute vertical floating table position specified by the table properties, in points. Default value is 0.

 **Examples:** 

Shows how set the location of floating tables.

```

 Document doc = new Document();
 DocumentBuilder builder = new DocumentBuilder(doc);

 Table table = builder.startTable();
 builder.insertCell();
 builder.write("Table 1, cell 1");
 builder.endTable();
 table.setPreferredWidth(PreferredWidth.fromPoints(300.0));

 // Set the table's location to a place on the page, such as, in this case, the bottom right corner.
 table.setRelativeVerticalAlignment(VerticalAlignment.BOTTOM);
 table.setRelativeHorizontalAlignment(HorizontalAlignment.RIGHT);

 table = builder.startTable();
 builder.insertCell();
 builder.write("Table 2, cell 1");
 builder.endTable();
 table.setPreferredWidth(PreferredWidth.fromPoints(300.0));

 // We can also set a horizontal and vertical offset in points from the paragraph's location where we inserted the table.
 table.setAbsoluteVerticalDistance(50.0);
 table.setAbsoluteHorizontalDistance(100.0);

 doc.save(getArtifactsDir() + "Table.ChangeFloatingTableProperties.docx");
 
```

**Returns:**
double - Absolute vertical floating table position specified by the table properties, in points.
### getAlignment() {#getAlignment}
```
public int getAlignment()
```


Specifies how an inline table is aligned in the document.

 **Remarks:** 

The default value is [TableAlignment.LEFT](../../com.aspose.words/tablealignment/\#LEFT).

 **Examples:** 

Shows how to apply an outline border to a table.

```

 Document doc = new Document(getMyDir() + "Tables.docx");
 Table table = doc.getFirstSection().getBody().getTables().get(0);

 // Align the table to the center of the page.
 table.setAlignment(TableAlignment.CENTER);

 // Clear any existing borders and shading from the table.
 table.clearBorders();
 table.clearShading();

 // Add green borders to the outline of the table.
 table.setBorder(BorderType.LEFT, LineStyle.SINGLE, 1.5, Color.GREEN, true);
 table.setBorder(BorderType.RIGHT, LineStyle.SINGLE, 1.5, Color.GREEN, true);
 table.setBorder(BorderType.TOP, LineStyle.SINGLE, 1.5, Color.GREEN, true);
 table.setBorder(BorderType.BOTTOM, LineStyle.SINGLE, 1.5, Color.GREEN, true);

 // Fill the cells with a light green solid color.
 table.setShading(TextureIndex.TEXTURE_SOLID, Color.GREEN, Color.GREEN);

 doc.save(getArtifactsDir() + "Table.SetOutlineBorders.docx");
 
```

**Returns:**
int - The corresponding  int  value. The returned value is one of [TableAlignment](../../com.aspose.words/tablealignment/) constants.
### getAllowAutoFit() {#getAllowAutoFit}
```
public boolean getAllowAutoFit()
```


Allows Microsoft Word and Aspose.Words to automatically resize cells in a table to fit their contents.

 **Remarks:** 

The default value is  true .

 **Examples:** 

Shows how to enable/disable automatic table cell resizing.

```

 Document doc = new Document();
 DocumentBuilder builder = new DocumentBuilder(doc);

 Table table = builder.startTable();
 builder.insertCell();
 builder.getCellFormat().setPreferredWidth(PreferredWidth.fromPoints(100.0));
 builder.write("Lorem ipsum dolor sit amet, consectetur adipiscing elit, " +
         "sed do eiusmod tempor incididunt ut labore et dolore magna aliqua.");

 builder.insertCell();
 builder.getCellFormat().setPreferredWidth(PreferredWidth.AUTO);
 builder.write("Lorem ipsum dolor sit amet, consectetur adipiscing elit, " +
         "sed do eiusmod tempor incididunt ut labore et dolore magna aliqua.");
 builder.endRow();
 builder.endTable();

 // Set the "AllowAutoFit" property to "false" to get the table to maintain the dimensions
 // of all its rows and cells, and truncate contents if they get too large to fit.
 // Set the "AllowAutoFit" property to "true" to allow the table to change its cells' width and height
 // to accommodate their contents.
 table.setAllowAutoFit(allowAutoFit);

 doc.save(getArtifactsDir() + "Table.AllowAutoFitOnTable.html");
 
```

**M:Aspose.Words.Tables.Table.AutoFit(Aspose.Words.Tables.AutoFitBehavior)**

**Returns:**
boolean - The corresponding  boolean  value.
### getAllowCellSpacing() {#getAllowCellSpacing}
```
public boolean getAllowCellSpacing()
```


Gets the "Allow spacing between cells" option.

 **Examples:** 

Shows how to enable spacing between individual cells in a table.

```

 Document doc = new Document();
 DocumentBuilder builder = new DocumentBuilder(doc);

 Table table = builder.startTable();
 builder.insertCell();
 builder.write("Animal");
 builder.insertCell();
 builder.write("Class");
 builder.endRow();
 builder.insertCell();
 builder.write("Dog");
 builder.insertCell();
 builder.write("Mammal");
 builder.endTable();

 table.setCellSpacing(3.0);

 // Set the "AllowCellSpacing" property to "true" to enable spacing between cells
 // with a magnitude equal to the value of the "CellSpacing" property, in points.
 // Set the "AllowCellSpacing" property to "false" to disable cell spacing
 // and ignore the value of the "CellSpacing" property.
 table.setAllowCellSpacing(allowCellSpacing);

 doc.save(getArtifactsDir() + "Table.AllowCellSpacing.html");

 // Adjusting the "CellSpacing" property will automatically enable cell spacing.
 table.setCellSpacing(5.0);

 Assert.assertTrue(table.getAllowCellSpacing());
 
```

**Returns:**
boolean - The "Allow spacing between cells" option.
### getAllowOverlap() {#getAllowOverlap}
```
public boolean getAllowOverlap()
```


Gets whether a floating table shall allow other floating objects in the document to overlap its extents when displayed. Default value is  true .

 **Examples:** 

Shows how to work with floating tables properties.

```

 Document doc = new Document(getMyDir() + "Table wrapped by text.docx");

 Table table = doc.getFirstSection().getBody().getTables().get(0);

 if (table.getTextWrapping() == TextWrapping.AROUND) {
     Assert.assertEquals(RelativeHorizontalPosition.MARGIN, table.getHorizontalAnchor());
     Assert.assertEquals(RelativeVerticalPosition.PARAGRAPH, table.getVerticalAnchor());
     Assert.assertEquals(false, table.getAllowOverlap());

     // Only Margin, Page, Column available in RelativeHorizontalPosition for HorizontalAnchor setter.
     // The ArgumentException will be thrown for any other values.
     table.setHorizontalAnchor(RelativeHorizontalPosition.COLUMN);

     // Only Margin, Page, Paragraph available in RelativeVerticalPosition for VerticalAnchor setter.
     // The ArgumentException will be thrown for any other values.
     table.setVerticalAnchor(RelativeVerticalPosition.PAGE);
 }
 
```

**Returns:**
boolean - Whether a floating table shall allow other floating objects in the document to overlap its extents when displayed.
### getAncestor(int ancestorType) {#getAncestor-int}
```
public CompositeNode getAncestor(int ancestorType)
```




**Parameters:**
| Parameter | Type | Description |
| --- | --- | --- |
| ancestorType | int |  |

**Returns:**
[CompositeNode](../../com.aspose.words/compositenode/)
### getAncestor(Class ancestorType) {#getAncestor-java.lang.Class}
```
public CompositeNode getAncestor(Class ancestorType)
```


Gets the first ancestor of the specified object type.

**Parameters:**
| Parameter | Type | Description |
| --- | --- | --- |
| ancestorType | java.lang.Class | The object type of the ancestor to retrieve. |

**Returns:**
[CompositeNode](../../com.aspose.words/compositenode/) - The ancestor of the specified type or  null  if no ancestor of this type was found.

 **Remarks:** 

The ancestor type matches if it is equal to  ancestorType  or derived from  ancestorType .

 **Examples:** 

Shows how to find out if a tables are nested.

```

 public void calculateDepthOfNestedTables() throws Exception {
     Document doc = new Document(getMyDir() + "Nested tables.docx");
     NodeCollection tables = doc.getChildNodes(NodeType.TABLE, true);
     for (int i = 0; i < tables.getCount(); i++) {
         Table table = (Table) tables.get(i);

         // Find out if any cells in the table have other tables as children.
         int count = getChildTableCount(table);
         System.out.print(MessageFormat.format("Table #{0} has {1} tables directly within its cells", i, count));

         // Find out if the table is nested inside another table, and, if so, at what depth.
         int tableDepth = getNestedDepthOfTable(table);

         if (tableDepth > 0)
             System.out.println(MessageFormat.format("Table #{0} is nested inside another table at depth of {1}", i, tableDepth));
         else
             System.out.println(MessageFormat.format("Table #{0} is a non nested table (is not a child of another table)", i));
     }
 }

 // Calculates what level a table is nested inside other tables.
 //
 // Returns An integer containing the level the table is nested at.
 // 0 = Table is not nested inside any other table
 // 1 = Table is nested within one parent table
 // 2 = Table is nested within two parent tables etc..
 private static int getNestedDepthOfTable(final Table table) {
     int depth = 0;
     Node parent = table.getAncestor(table.getNodeType());

     while (parent != null) {
         depth++;
         parent = parent.getAncestor(Table.class);
     }

     return depth;
 }

 // Determines if a table contains any immediate child table within its cells.
 // Does not recursively traverse through those tables to check for further tables.
 //
 // Returns true if at least one child cell contains a table.
 // Returns false if no cells in the table contains a table.
 private static int getChildTableCount(final Table table) {
     int childTableCount = 0;

     for (Row row : table.getRows()) {
         for (Cell cell : row.getCells()) {
             TableCollection childTables = cell.getTables();

             if (childTables.getCount() > 0) childTableCount++;
         }
     }

     return childTableCount;
 }
 
```
### getBidi() {#getBidi}
```
public boolean getBidi()
```


Gets whether this is a right-to-left table.

 **Remarks:** 

When  true , the cells in this row are laid out right to left.

The default value is  false .

 **Examples:** 

Shows how to create custom style settings for the table.

```

 Document doc = new Document();
 DocumentBuilder builder = new DocumentBuilder(doc);

 Table table = builder.startTable();
 builder.insertCell();
 builder.write("Name");
 builder.insertCell();
 builder.write("\u0645\u0631\u062d\u0628\u064b\u0627");
 builder.endRow();
 builder.insertCell();
 builder.insertCell();
 builder.endTable();

 TableStyle tableStyle = (TableStyle) doc.getStyles().add(StyleType.TABLE, "MyTableStyle1");
 tableStyle.setAllowBreakAcrossPages(true);
 tableStyle.setBidi(true);
 tableStyle.setCellSpacing(5.0);
 tableStyle.setBottomPadding(20.0);
 tableStyle.setLeftPadding(5.0);
 tableStyle.setRightPadding(10.0);
 tableStyle.setTopPadding(20.0);
 tableStyle.getShading().setBackgroundPatternColor(Color.WHITE);
 tableStyle.getBorders().setColor(Color.BLACK);
 tableStyle.getBorders().setLineStyle(LineStyle.DOT_DASH);
 tableStyle.setVerticalAlignment(CellVerticalAlignment.CENTER);

 table.setStyle(tableStyle);

 // Setting the style properties of a table may affect the properties of the table itself.
 Assert.assertTrue(table.getBidi());
 Assert.assertEquals(5.0d, table.getCellSpacing());
 Assert.assertEquals("MyTableStyle1", table.getStyleName());

 doc.save(getArtifactsDir() + "Table.TableStyleCreation.docx");
 
```

**Returns:**
boolean - Whether this is a right-to-left table.
### getBottomPadding() {#getBottomPadding}
```
public double getBottomPadding()
```


Gets the amount of space (in points) to add below the contents of cells.

 **Examples:** 

Shows how to configure content padding in a table.

```

 Document doc = new Document();
 DocumentBuilder builder = new DocumentBuilder(doc);

 Table table = builder.startTable();
 builder.insertCell();
 builder.write("Row 1, cell 1.");
 builder.insertCell();
 builder.write("Row 1, cell 2.");
 builder.endTable();

 // For every cell in the table, set the distance between its contents and each of its borders.
 // This table will maintain the minimum padding distance by wrapping text.
 table.setLeftPadding(30.0);
 table.setRightPadding(60.0);
 table.setTopPadding(10.0);
 table.setBottomPadding(90.0);
 table.setPreferredWidth(PreferredWidth.fromPoints(250.0));

 doc.save(getArtifactsDir() + "DocumentBuilder.SetRowFormatting.docx");
 
```

**Returns:**
double - The amount of space (in points) to add below the contents of cells.
### getCellSpacing() {#getCellSpacing}
```
public double getCellSpacing()
```


Gets the amount of space (in points) between the cells.

 **Examples:** 

Shows how to enable spacing between individual cells in a table.

```

 Document doc = new Document();
 DocumentBuilder builder = new DocumentBuilder(doc);

 Table table = builder.startTable();
 builder.insertCell();
 builder.write("Animal");
 builder.insertCell();
 builder.write("Class");
 builder.endRow();
 builder.insertCell();
 builder.write("Dog");
 builder.insertCell();
 builder.write("Mammal");
 builder.endTable();

 table.setCellSpacing(3.0);

 // Set the "AllowCellSpacing" property to "true" to enable spacing between cells
 // with a magnitude equal to the value of the "CellSpacing" property, in points.
 // Set the "AllowCellSpacing" property to "false" to disable cell spacing
 // and ignore the value of the "CellSpacing" property.
 table.setAllowCellSpacing(allowCellSpacing);

 doc.save(getArtifactsDir() + "Table.AllowCellSpacing.html");

 // Adjusting the "CellSpacing" property will automatically enable cell spacing.
 table.setCellSpacing(5.0);

 Assert.assertTrue(table.getAllowCellSpacing());
 
```

Shows how to create custom style settings for the table.

```

 Document doc = new Document();
 DocumentBuilder builder = new DocumentBuilder(doc);

 Table table = builder.startTable();
 builder.insertCell();
 builder.write("Name");
 builder.insertCell();
 builder.write("\u0645\u0631\u062d\u0628\u064b\u0627");
 builder.endRow();
 builder.insertCell();
 builder.insertCell();
 builder.endTable();

 TableStyle tableStyle = (TableStyle) doc.getStyles().add(StyleType.TABLE, "MyTableStyle1");
 tableStyle.setAllowBreakAcrossPages(true);
 tableStyle.setBidi(true);
 tableStyle.setCellSpacing(5.0);
 tableStyle.setBottomPadding(20.0);
 tableStyle.setLeftPadding(5.0);
 tableStyle.setRightPadding(10.0);
 tableStyle.setTopPadding(20.0);
 tableStyle.getShading().setBackgroundPatternColor(Color.WHITE);
 tableStyle.getBorders().setColor(Color.BLACK);
 tableStyle.getBorders().setLineStyle(LineStyle.DOT_DASH);
 tableStyle.setVerticalAlignment(CellVerticalAlignment.CENTER);

 table.setStyle(tableStyle);

 // Setting the style properties of a table may affect the properties of the table itself.
 Assert.assertTrue(table.getBidi());
 Assert.assertEquals(5.0d, table.getCellSpacing());
 Assert.assertEquals("MyTableStyle1", table.getStyleName());

 doc.save(getArtifactsDir() + "Table.TableStyleCreation.docx");
 
```

**Returns:**
double - The amount of space (in points) between the cells.
### getChild(int nodeType, int index, boolean isDeep) {#getChild-int-int-boolean}
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
[Node](../../com.aspose.words/node/)
### getChildNodes() {#getChildNodes}
```
public NodeCollection getChildNodes()
```


Gets all immediate child nodes of this node.

 **Remarks:** 

Note, [getChildNodes()](../../com.aspose.words/compositenode/\#getChildNodes) is equivalent to calling **M:Aspose.Words.CompositeNode.GetChildNodes(Aspose.Words.NodeType,System.Boolean)** with arguments ( [NodeType.ANY](../../com.aspose.words/nodetype/\#ANY),  false ) and creates and returns a new collection every time it is accessed.

If there are no child nodes, this property returns an empty collection.

 **Examples:** 

Shows how to traverse through a composite node's collection of child nodes.

```

 Document doc = new Document();

 // Add two runs and one shape as child nodes to the first paragraph of this document.
 Paragraph paragraph = (Paragraph) doc.getChild(NodeType.PARAGRAPH, 0, true);
 paragraph.appendChild(new Run(doc, "Hello world! "));

 Shape shape = new Shape(doc, ShapeType.RECTANGLE);
 shape.setWidth(200.0);
 shape.setHeight(200.0);
 // Note that the 'CustomNodeId' is not saved to an output file and exists only during the node lifetime.
 shape.setCustomNodeId(100);
 shape.setWrapType(WrapType.INLINE);
 paragraph.appendChild(shape);

 paragraph.appendChild(new Run(doc, "Hello again!"));

 // Iterate through the paragraph's collection of immediate children,
 // and print any runs or shapes that we find within.
 NodeCollection children = paragraph.getChildNodes();

 Assert.assertEquals(3, paragraph.getChildNodes().getCount());

 for (Node child : (Iterable) children)
     switch (child.getNodeType()) {
         case NodeType.RUN:
             System.out.println("Run contents:");
             System.out.println("\t\"{child.GetText().Trim()}\"");
             break;
         case NodeType.SHAPE:
             Shape childShape = (Shape) child;
             System.out.println("Shape:");
             System.out.println("\t{childShape.ShapeType}, {childShape.Width}x{childShape.Height}");
             break;
     }
 
```

**Returns:**
[NodeCollection](../../com.aspose.words/nodecollection/) - All immediate child nodes of this node.
### getChildNodes(int nodeType, boolean isDeep) {#getChildNodes-int-boolean}
```
public NodeCollection getChildNodes(int nodeType, boolean isDeep)
```




**Parameters:**
| Parameter | Type | Description |
| --- | --- | --- |
| nodeType | int |  |
| isDeep | boolean |  |

**Returns:**
[NodeCollection](../../com.aspose.words/nodecollection/)
### getClass() {#getClass}
```
public final native Class<?> getClass()
```




**Returns:**
java.lang.Class<?>
### getContainer() {#getContainer}
```
public CompositeNode getContainer()
```




**Returns:**
[CompositeNode](../../com.aspose.words/compositenode/)
### getCount() {#getCount}
```
public int getCount()
```


Gets the number of immediate children of this node.

 **Examples:** 

Shows how to add, update and delete child nodes in a CompositeNode's collection of children.

```

 Document doc = new Document();

 // An empty document, by default, has one paragraph.
 Assert.assertEquals(1, doc.getFirstSection().getBody().getParagraphs().getCount());

 // Composite nodes such as our paragraph can contain other composite and inline nodes as children.
 Paragraph paragraph = doc.getFirstSection().getBody().getFirstParagraph();
 Run paragraphText = new Run(doc, "Initial text. ");
 paragraph.appendChild(paragraphText);

 // Create three more run nodes.
 Run run1 = new Run(doc, "Run 1. ");
 Run run2 = new Run(doc, "Run 2. ");
 Run run3 = new Run(doc, "Run 3. ");

 // The document body will not display these runs until we insert them into a composite node
 // that itself is a part of the document's node tree, as we did with the first run.
 // We can determine where the text contents of nodes that we insert
 // appears in the document by specifying an insertion location relative to another node in the paragraph.
 Assert.assertEquals("Initial text.", paragraph.getText().trim());

 // Insert the second run into the paragraph in front of the initial run.
 paragraph.insertBefore(run2, paragraphText);

 Assert.assertEquals("Run 2. Initial text.", paragraph.getText().trim());

 // Insert the third run after the initial run.
 paragraph.insertAfter(run3, paragraphText);

 Assert.assertEquals("Run 2. Initial text. Run 3.", paragraph.getText().trim());

 // Insert the first run to the start of the paragraph's child nodes collection.
 paragraph.prependChild(run1);

 Assert.assertEquals("Run 1. Run 2. Initial text. Run 3.", paragraph.getText().trim());
 Assert.assertEquals(4, paragraph.getChildNodes(NodeType.ANY, true).getCount());

 // We can modify the contents of the run by editing and deleting existing child nodes.
 ((Run) paragraph.getChildNodes(NodeType.RUN, true).get(1)).setText("Updated run 2. ");
 paragraph.getChildNodes(NodeType.RUN, true).remove(paragraphText);

 Assert.assertEquals("Run 1. Updated run 2. Run 3.", paragraph.getText().trim());
 Assert.assertEquals(3, paragraph.getChildNodes(NodeType.ANY, true).getCount());
 
```

**Returns:**
int - The number of immediate children of this node.
### getCurrentNode() {#getCurrentNode}
```
public Node getCurrentNode()
```




**Returns:**
[Node](../../com.aspose.words/node/)
### getCustomNodeId() {#getCustomNodeId}
```
public int getCustomNodeId()
```


Specifies custom node identifier.

 **Remarks:** 

Default is zero.

This identifier can be set and used arbitrarily. For example, as a key to get external data.

Important note, specified value is not saved to an output file and exists only during the node lifetime.

 **Examples:** 

Shows how to traverse through a composite node's collection of child nodes.

```

 Document doc = new Document();

 // Add two runs and one shape as child nodes to the first paragraph of this document.
 Paragraph paragraph = (Paragraph) doc.getChild(NodeType.PARAGRAPH, 0, true);
 paragraph.appendChild(new Run(doc, "Hello world! "));

 Shape shape = new Shape(doc, ShapeType.RECTANGLE);
 shape.setWidth(200.0);
 shape.setHeight(200.0);
 // Note that the 'CustomNodeId' is not saved to an output file and exists only during the node lifetime.
 shape.setCustomNodeId(100);
 shape.setWrapType(WrapType.INLINE);
 paragraph.appendChild(shape);

 paragraph.appendChild(new Run(doc, "Hello again!"));

 // Iterate through the paragraph's collection of immediate children,
 // and print any runs or shapes that we find within.
 NodeCollection children = paragraph.getChildNodes();

 Assert.assertEquals(3, paragraph.getChildNodes().getCount());

 for (Node child : (Iterable) children)
     switch (child.getNodeType()) {
         case NodeType.RUN:
             System.out.println("Run contents:");
             System.out.println("\t\"{child.GetText().Trim()}\"");
             break;
         case NodeType.SHAPE:
             Shape childShape = (Shape) child;
             System.out.println("Shape:");
             System.out.println("\t{childShape.ShapeType}, {childShape.Width}x{childShape.Height}");
             break;
     }
 
```

**Returns:**
int - The corresponding  int  value.
### getDescription() {#getDescription}
```
public String getDescription()
```


Gets description of this table. It provides an alternative text representation of the information contained in the table.

 **Remarks:** 

The default value is an empty string.

This property is meaningful for ISO/IEC 29500 compliant DOCX documents ( [OoxmlCompliance](../../com.aspose.words/ooxmlcompliance/)). When saved to pre-ISO/IEC 29500 formats, the property is ignored.

 **Examples:** 

Shows how to build a nested table without using a document builder.

```

 public void createNestedTable() throws Exception {
     Document doc = new Document();

     // Create the outer table with three rows and four columns, and then add it to the document.
     Table outerTable = createTable(doc, 3, 4, "Outer Table");
     doc.getFirstSection().getBody().appendChild(outerTable);

     // Create another table with two rows and two columns and then insert it into the first table's first cell.
     Table innerTable = createTable(doc, 2, 2, "Inner Table");
     outerTable.getFirstRow().getFirstCell().appendChild(innerTable);

     doc.save(getArtifactsDir() + "Table.CreateNestedTable.docx");
 }

 // Creates a new table in the document with the given dimensions and text in each cell.
 private Table createTable(final Document doc, final int rowCount, final int cellCount, final String cellText) throws Exception {
     Table table = new Table(doc);

     for (int rowId = 1; rowId <= rowCount; rowId++) {
         Row row = new Row(doc);
         table.appendChild(row);

         for (int cellId = 1; cellId <= cellCount; cellId++) {
             Cell cell = new Cell(doc);
             cell.appendChild(new Paragraph(doc));
             cell.getFirstParagraph().appendChild(new Run(doc, cellText));

             row.appendChild(cell);
         }
     }

     // You can use the "Title" and "Description" properties to add a title and description respectively to your table.
     // The table must have at least one row before we can use these properties.
     // These properties are meaningful for ISO / IEC 29500 compliant .docx documents (see the OoxmlCompliance class).
     // If we save the document to pre-ISO/IEC 29500 formats, Microsoft Word ignores these properties.
     table.setTitle("Aspose table title");
     table.setDescription("Aspose table description");

     return table;
 }
 
```

**Returns:**
java.lang.String - Description of this table.
### getDistanceBottom() {#getDistanceBottom}
```
public double getDistanceBottom()
```


Gets distance between table bottom and the surrounding text, in points.

 **Examples:** 

Shows the minimum distance operations between table boundaries and text.

```

 Document doc = new Document(getMyDir() + "Table wrapped by text.docx");

 Table table = (Table) doc.getChild(NodeType.TABLE, 0, true);

 Assert.assertEquals(table.getDistanceTop(), 25.9d);
 Assert.assertEquals(table.getDistanceBottom(), 25.9d);
 Assert.assertEquals(table.getDistanceLeft(), 17.3d);
 Assert.assertEquals(table.getDistanceRight(), 17.3d);
 
```

**Returns:**
double - Distance between table bottom and the surrounding text, in points.
### getDistanceLeft() {#getDistanceLeft}
```
public double getDistanceLeft()
```


Gets distance between table left and the surrounding text, in points.

 **Examples:** 

Shows the minimum distance operations between table boundaries and text.

```

 Document doc = new Document(getMyDir() + "Table wrapped by text.docx");

 Table table = (Table) doc.getChild(NodeType.TABLE, 0, true);

 Assert.assertEquals(table.getDistanceTop(), 25.9d);
 Assert.assertEquals(table.getDistanceBottom(), 25.9d);
 Assert.assertEquals(table.getDistanceLeft(), 17.3d);
 Assert.assertEquals(table.getDistanceRight(), 17.3d);
 
```

**Returns:**
double - Distance between table left and the surrounding text, in points.
### getDistanceRight() {#getDistanceRight}
```
public double getDistanceRight()
```


Gets distance between table right and the surrounding text, in points.

 **Examples:** 

Shows the minimum distance operations between table boundaries and text.

```

 Document doc = new Document(getMyDir() + "Table wrapped by text.docx");

 Table table = (Table) doc.getChild(NodeType.TABLE, 0, true);

 Assert.assertEquals(table.getDistanceTop(), 25.9d);
 Assert.assertEquals(table.getDistanceBottom(), 25.9d);
 Assert.assertEquals(table.getDistanceLeft(), 17.3d);
 Assert.assertEquals(table.getDistanceRight(), 17.3d);
 
```

**Returns:**
double - Distance between table right and the surrounding text, in points.
### getDistanceTop() {#getDistanceTop}
```
public double getDistanceTop()
```


Gets distance between table top and the surrounding text, in points.

 **Examples:** 

Shows the minimum distance operations between table boundaries and text.

```

 Document doc = new Document(getMyDir() + "Table wrapped by text.docx");

 Table table = (Table) doc.getChild(NodeType.TABLE, 0, true);

 Assert.assertEquals(table.getDistanceTop(), 25.9d);
 Assert.assertEquals(table.getDistanceBottom(), 25.9d);
 Assert.assertEquals(table.getDistanceLeft(), 17.3d);
 Assert.assertEquals(table.getDistanceRight(), 17.3d);
 
```

**Returns:**
double - Distance between table top and the surrounding text, in points.
### getDocument() {#getDocument}
```
public DocumentBase getDocument()
```


Gets the document to which this node belongs.

 **Remarks:** 

The node always belongs to a document even if it has just been created and not yet added to the tree, or if it has been removed from the tree.

 **Examples:** 

Shows how to create a node and set its owning document.

```

 Document doc = new Document();
 Paragraph para = new Paragraph(doc);
 para.appendChild(new Run(doc, "Hello world!"));

 // We have not yet appended this paragraph as a child to any composite node.
 Assert.assertNull(para.getParentNode());

 // If a node is an appropriate child node type of another composite node,
 // we can attach it as a child only if both nodes have the same owner document.
 // The owner document is the document we passed to the node's constructor.
 // We have not attached this paragraph to the document, so the document does not contain its text.
 Assert.assertEquals(para.getDocument(), doc);
 Assert.assertEquals("", doc.getText().trim());

 // Since the document owns this paragraph, we can apply one of its styles to the paragraph's contents.
 para.getParagraphFormat().setStyleName("Heading 1");

 // Add this node to the document, and then verify its contents.
 doc.getFirstSection().getBody().appendChild(para);

 Assert.assertEquals(doc.getFirstSection().getBody(), para.getParentNode());
 Assert.assertEquals("Hello world!", doc.getText().trim());
 
```

**Returns:**
[DocumentBase](../../com.aspose.words/documentbase/) - The document to which this node belongs.
### getFirstChild() {#getFirstChild}
```
public Node getFirstChild()
```


Gets the first child of the node.

 **Remarks:** 

If there is no first child node, a  null  is returned.

 **Examples:** 

Shows how to use a node's NextSibling property to enumerate through its immediate children.

```

 Document doc = new Document(getMyDir() + "Paragraphs.docx");

 for (Node node = doc.getFirstSection().getBody().getFirstChild(); node != null; node = node.getNextSibling()) {
     System.out.println(Node.nodeTypeToString(node.getNodeType()));
 }
 
```

Shows how to traverse a composite node's tree of child nodes.

```

 public void recurseChildren() throws Exception {
     Document doc = new Document(getMyDir() + "Paragraphs.docx");

     // Any node that can contain child nodes, such as the document itself, is composite.
     Assert.assertTrue(doc.isComposite());

     // Invoke the recursive function that will go through and print all the child nodes of a composite node.
     traverseAllNodes(doc, 0);
 }

 /// 
 /// Recursively traverses a node tree while printing the type of each node
 /// with an indent depending on depth as well as the contents of all inline nodes.
 /// 
 public void traverseAllNodes(CompositeNode parentNode, int depth) {
     for (Node childNode = parentNode.getFirstChild(); childNode != null; childNode = childNode.getNextSibling()) {
         System.out.println(MessageFormat.format("{0}{1}", String.format("    ", depth), Node.nodeTypeToString(childNode.getNodeType())));

         // Recurse into the node if it is a composite node. Otherwise, print its contents if it is an inline node.
         if (childNode.isComposite()) {
             System.out.println();
             traverseAllNodes((CompositeNode) childNode, depth + 1);
         } else if (childNode instanceof Inline) {
             System.out.println(" - \"{childNode.GetText().Trim()}\"");
         } else {
             System.out.println();
         }
     }
 }
 
```

**Returns:**
[Node](../../com.aspose.words/node/) - The first child of the node.
### getFirstRow() {#getFirstRow}
```
public Row getFirstRow()
```


Returns the first [Row](../../com.aspose.words/row/) node in the table.

 **Examples:** 

Shows how to remove the first and last rows of all tables in a document.

```

 Document doc = new Document(getMyDir() + "Tables.docx");

 TableCollection tables = doc.getFirstSection().getBody().getTables();

 Assert.assertEquals(5, tables.get(0).getRows().getCount());
 Assert.assertEquals(4, tables.get(1).getRows().getCount());

 for (Table table : tables) {
     if (table.getFirstRow() != null) {
         table.getFirstRow().remove();
     }

     if (table.getLastRow() != null) {
         table.getLastRow().remove();
     }
 }

 Assert.assertEquals(3, tables.get(0).getRows().getCount());
 Assert.assertEquals(2, tables.get(1).getRows().getCount());
 
```

Shows how to combine the rows from two tables into one.

```

 Document doc = new Document(getMyDir() + "Tables.docx");

 // Below are two ways of getting a table from a document.
 // 1 -  From the "Tables" collection of a Body node:
 Table firstTable = doc.getFirstSection().getBody().getTables().get(0);

 // 2 -  Using the "GetChild" method:
 Table secondTable = (Table) doc.getChild(NodeType.TABLE, 1, true);

 // Append all rows from the current table to the next.
 while (secondTable.hasChildNodes())
     firstTable.getRows().add(secondTable.getFirstRow());

 // Remove the empty table container.
 secondTable.remove();

 doc.save(getArtifactsDir() + "Table.CombineTables.docx");
 
```

**Returns:**
[Row](../../com.aspose.words/row/) - The first [Row](../../com.aspose.words/row/) node in the table.
### getHorizontalAnchor() {#getHorizontalAnchor}
```
public int getHorizontalAnchor()
```


Gets the base object from which the horizontal positioning of floating table should be calculated. Default value is [RelativeHorizontalPosition.COLUMN](../../com.aspose.words/relativehorizontalposition/\#COLUMN).

 **Examples:** 

Shows how to work with floating tables properties.

```

 Document doc = new Document(getMyDir() + "Table wrapped by text.docx");

 Table table = doc.getFirstSection().getBody().getTables().get(0);

 if (table.getTextWrapping() == TextWrapping.AROUND) {
     Assert.assertEquals(RelativeHorizontalPosition.MARGIN, table.getHorizontalAnchor());
     Assert.assertEquals(RelativeVerticalPosition.PARAGRAPH, table.getVerticalAnchor());
     Assert.assertEquals(false, table.getAllowOverlap());

     // Only Margin, Page, Column available in RelativeHorizontalPosition for HorizontalAnchor setter.
     // The ArgumentException will be thrown for any other values.
     table.setHorizontalAnchor(RelativeHorizontalPosition.COLUMN);

     // Only Margin, Page, Paragraph available in RelativeVerticalPosition for VerticalAnchor setter.
     // The ArgumentException will be thrown for any other values.
     table.setVerticalAnchor(RelativeVerticalPosition.PAGE);
 }
 
```

**Returns:**
int - The base object from which the horizontal positioning of floating table should be calculated. The returned value is one of [RelativeHorizontalPosition](../../com.aspose.words/relativehorizontalposition/) constants.
### getLastChild() {#getLastChild}
```
public Node getLastChild()
```


Gets the last child of the node.

 **Remarks:** 

If there is no last child node, a  null  is returned.

 **Examples:** 

Shows how to use of methods of Node and CompositeNode to remove a section before the last section in the document.

```

 Document doc = new Document();
 DocumentBuilder builder = new DocumentBuilder(doc);

 builder.writeln("Section 1 text.");
 builder.insertBreak(BreakType.SECTION_BREAK_CONTINUOUS);
 builder.writeln("Section 2 text.");

 // Both sections are siblings of each other.
 Section lastSection = (Section) doc.getLastChild();
 Section firstSection = (Section) lastSection.getPreviousSibling();

 // Remove a section based on its sibling relationship with another section.
 if (lastSection.getPreviousSibling() != null)
     doc.removeChild(firstSection);

 // The section we removed was the first one, leaving the document with only the second.
 Assert.assertEquals("Section 2 text.", doc.getText().trim());
 
```

**Returns:**
[Node](../../com.aspose.words/node/) - The last child of the node.
### getLastRow() {#getLastRow}
```
public Row getLastRow()
```


Returns the last [Row](../../com.aspose.words/row/) node in the table.

 **Examples:** 

Shows how to remove the first and last rows of all tables in a document.

```

 Document doc = new Document(getMyDir() + "Tables.docx");

 TableCollection tables = doc.getFirstSection().getBody().getTables();

 Assert.assertEquals(5, tables.get(0).getRows().getCount());
 Assert.assertEquals(4, tables.get(1).getRows().getCount());

 for (Table table : tables) {
     if (table.getFirstRow() != null) {
         table.getFirstRow().remove();
     }

     if (table.getLastRow() != null) {
         table.getLastRow().remove();
     }
 }

 Assert.assertEquals(3, tables.get(0).getRows().getCount());
 Assert.assertEquals(2, tables.get(1).getRows().getCount());
 
```

**Returns:**
[Row](../../com.aspose.words/row/) - The last [Row](../../com.aspose.words/row/) node in the table.
### getLeftIndent() {#getLeftIndent}
```
public double getLeftIndent()
```


Gets the value that represents the left indent of the table.

 **Examples:** 

Shows how to create a formatted table using DocumentBuilder.

```

 Document doc = new Document();
 DocumentBuilder builder = new DocumentBuilder(doc);

 Table table = builder.startTable();
 builder.insertCell();
 table.setLeftIndent(20.0);

 // Set some formatting options for text and table appearance.
 builder.getRowFormat().setHeight(40.0);
 builder.getRowFormat().setHeightRule(HeightRule.AT_LEAST);
 builder.getCellFormat().getShading().setBackgroundPatternColor(new Color((198), (217), (241)));

 builder.getParagraphFormat().setAlignment(ParagraphAlignment.CENTER);
 builder.getFont().setSize(16.0);
 builder.getFont().setName("Arial");
 builder.getFont().setBold(true);

 // Configuring the formatting options in a document builder will apply them
 // to the current cell/row its cursor is in,
 // as well as any new cells and rows created using that builder.
 builder.write("Header Row,\n Cell 1");
 builder.insertCell();
 builder.write("Header Row,\n Cell 2");
 builder.insertCell();
 builder.write("Header Row,\n Cell 3");
 builder.endRow();

 // Reconfigure the builder's formatting objects for new rows and cells that we are about to make.
 // The builder will not apply these to the first row already created so that it will stand out as a header row.
 builder.getCellFormat().getShading().setBackgroundPatternColor(Color.WHITE);
 builder.getCellFormat().setVerticalAlignment(CellVerticalAlignment.CENTER);
 builder.getRowFormat().setHeight(30.0);
 builder.getRowFormat().setHeightRule(HeightRule.AUTO);
 builder.insertCell();
 builder.getFont().setSize(12.0);
 builder.getFont().setBold(false);

 builder.write("Row 1, Cell 1.");
 builder.insertCell();
 builder.write("Row 1, Cell 2.");
 builder.insertCell();
 builder.write("Row 1, Cell 3.");
 builder.endRow();
 builder.insertCell();
 builder.write("Row 2, Cell 1.");
 builder.insertCell();
 builder.write("Row 2, Cell 2.");
 builder.insertCell();
 builder.write("Row 2, Cell 3.");
 builder.endRow();
 builder.endTable();

 doc.save(getArtifactsDir() + "DocumentBuilder.CreateFormattedTable.docx");
 
```

**Returns:**
double - The value that represents the left indent of the table.
### getLeftPadding() {#getLeftPadding}
```
public double getLeftPadding()
```


Gets the amount of space (in points) to add to the left of the contents of cells.

 **Examples:** 

Shows how to configure content padding in a table.

```

 Document doc = new Document();
 DocumentBuilder builder = new DocumentBuilder(doc);

 Table table = builder.startTable();
 builder.insertCell();
 builder.write("Row 1, cell 1.");
 builder.insertCell();
 builder.write("Row 1, cell 2.");
 builder.endTable();

 // For every cell in the table, set the distance between its contents and each of its borders.
 // This table will maintain the minimum padding distance by wrapping text.
 table.setLeftPadding(30.0);
 table.setRightPadding(60.0);
 table.setTopPadding(10.0);
 table.setBottomPadding(90.0);
 table.setPreferredWidth(PreferredWidth.fromPoints(250.0));

 doc.save(getArtifactsDir() + "DocumentBuilder.SetRowFormatting.docx");
 
```

**Returns:**
double - The amount of space (in points) to add to the left of the contents of cells.
### getNextMatchingNode(Node curNode) {#getNextMatchingNode-com.aspose.words.Node}
```
public Node getNextMatchingNode(Node curNode)
```




**Parameters:**
| Parameter | Type | Description |
| --- | --- | --- |
| curNode | [Node](../../com.aspose.words/node/) |  |

**Returns:**
[Node](../../com.aspose.words/node/)
### getNextSibling() {#getNextSibling}
```
public Node getNextSibling()
```


Gets the node immediately following this node.

 **Remarks:** 

If there is no next node, a  null  is returned.

 **Examples:** 

Shows how to use a node's NextSibling property to enumerate through its immediate children.

```

 Document doc = new Document(getMyDir() + "Paragraphs.docx");

 for (Node node = doc.getFirstSection().getBody().getFirstChild(); node != null; node = node.getNextSibling()) {
     System.out.println(Node.nodeTypeToString(node.getNodeType()));
 }
 
```

Shows how to traverse a composite node's tree of child nodes.

```

 public void recurseChildren() throws Exception {
     Document doc = new Document(getMyDir() + "Paragraphs.docx");

     // Any node that can contain child nodes, such as the document itself, is composite.
     Assert.assertTrue(doc.isComposite());

     // Invoke the recursive function that will go through and print all the child nodes of a composite node.
     traverseAllNodes(doc, 0);
 }

 /// 
 /// Recursively traverses a node tree while printing the type of each node
 /// with an indent depending on depth as well as the contents of all inline nodes.
 /// 
 public void traverseAllNodes(CompositeNode parentNode, int depth) {
     for (Node childNode = parentNode.getFirstChild(); childNode != null; childNode = childNode.getNextSibling()) {
         System.out.println(MessageFormat.format("{0}{1}", String.format("    ", depth), Node.nodeTypeToString(childNode.getNodeType())));

         // Recurse into the node if it is a composite node. Otherwise, print its contents if it is an inline node.
         if (childNode.isComposite()) {
             System.out.println();
             traverseAllNodes((CompositeNode) childNode, depth + 1);
         } else if (childNode instanceof Inline) {
             System.out.println(" - \"{childNode.GetText().Trim()}\"");
         } else {
             System.out.println();
         }
     }
 }
 
```

**Returns:**
[Node](../../com.aspose.words/node/) - The node immediately following this node.
### getNodeType() {#getNodeType}
```
public int getNodeType()
```


Returns [NodeType.TABLE](../../com.aspose.words/nodetype/\#TABLE).

 **Examples:** 

Shows how to traverse a composite node's tree of child nodes.

```

 public void recurseChildren() throws Exception {
     Document doc = new Document(getMyDir() + "Paragraphs.docx");

     // Any node that can contain child nodes, such as the document itself, is composite.
     Assert.assertTrue(doc.isComposite());

     // Invoke the recursive function that will go through and print all the child nodes of a composite node.
     traverseAllNodes(doc, 0);
 }

 /// 
 /// Recursively traverses a node tree while printing the type of each node
 /// with an indent depending on depth as well as the contents of all inline nodes.
 /// 
 public void traverseAllNodes(CompositeNode parentNode, int depth) {
     for (Node childNode = parentNode.getFirstChild(); childNode != null; childNode = childNode.getNextSibling()) {
         System.out.println(MessageFormat.format("{0}{1}", String.format("    ", depth), Node.nodeTypeToString(childNode.getNodeType())));

         // Recurse into the node if it is a composite node. Otherwise, print its contents if it is an inline node.
         if (childNode.isComposite()) {
             System.out.println();
             traverseAllNodes((CompositeNode) childNode, depth + 1);
         } else if (childNode instanceof Inline) {
             System.out.println(" - \"{childNode.GetText().Trim()}\"");
         } else {
             System.out.println();
         }
     }
 }
 
```

Shows how to find out if a tables are nested.

```

 public void calculateDepthOfNestedTables() throws Exception {
     Document doc = new Document(getMyDir() + "Nested tables.docx");
     NodeCollection tables = doc.getChildNodes(NodeType.TABLE, true);
     for (int i = 0; i < tables.getCount(); i++) {
         Table table = (Table) tables.get(i);

         // Find out if any cells in the table have other tables as children.
         int count = getChildTableCount(table);
         System.out.print(MessageFormat.format("Table #{0} has {1} tables directly within its cells", i, count));

         // Find out if the table is nested inside another table, and, if so, at what depth.
         int tableDepth = getNestedDepthOfTable(table);

         if (tableDepth > 0)
             System.out.println(MessageFormat.format("Table #{0} is nested inside another table at depth of {1}", i, tableDepth));
         else
             System.out.println(MessageFormat.format("Table #{0} is a non nested table (is not a child of another table)", i));
     }
 }

 // Calculates what level a table is nested inside other tables.
 //
 // Returns An integer containing the level the table is nested at.
 // 0 = Table is not nested inside any other table
 // 1 = Table is nested within one parent table
 // 2 = Table is nested within two parent tables etc..
 private static int getNestedDepthOfTable(final Table table) {
     int depth = 0;
     Node parent = table.getAncestor(table.getNodeType());

     while (parent != null) {
         depth++;
         parent = parent.getAncestor(Table.class);
     }

     return depth;
 }

 // Determines if a table contains any immediate child table within its cells.
 // Does not recursively traverse through those tables to check for further tables.
 //
 // Returns true if at least one child cell contains a table.
 // Returns false if no cells in the table contains a table.
 private static int getChildTableCount(final Table table) {
     int childTableCount = 0;

     for (Row row : table.getRows()) {
         for (Cell cell : row.getCells()) {
             TableCollection childTables = cell.getTables();

             if (childTables.getCount() > 0) childTableCount++;
         }
     }

     return childTableCount;
 }
 
```

**Returns:**
int - [NodeType.TABLE](../../com.aspose.words/nodetype/\#TABLE). The returned value is one of [NodeType](../../com.aspose.words/nodetype/) constants.
### getParentNode() {#getParentNode}
```
public CompositeNode getParentNode()
```


Gets the immediate parent of this node.

 **Remarks:** 

If a node has just been created and not yet added to the tree, or if it has been removed from the tree, the parent is  null .

 **Examples:** 

Shows how to access a node's parent node.

```

 Document doc = new Document();
 Paragraph para = doc.getFirstSection().getBody().getFirstParagraph();

 // Append a child Run node to the document's first paragraph.
 Run run = new Run(doc, "Hello world!");
 para.appendChild(run);

 // The paragraph is the parent node of the run node. We can trace this lineage
 // all the way to the document node, which is the root of the document's node tree.
 Assert.assertEquals(para, run.getParentNode());
 Assert.assertEquals(doc.getFirstSection().getBody(), para.getParentNode());
 Assert.assertEquals(doc.getFirstSection(), doc.getFirstSection().getBody().getParentNode());
 Assert.assertEquals(doc, doc.getFirstSection().getParentNode());
 
```

Shows how to create a node and set its owning document.

```

 Document doc = new Document();
 Paragraph para = new Paragraph(doc);
 para.appendChild(new Run(doc, "Hello world!"));

 // We have not yet appended this paragraph as a child to any composite node.
 Assert.assertNull(para.getParentNode());

 // If a node is an appropriate child node type of another composite node,
 // we can attach it as a child only if both nodes have the same owner document.
 // The owner document is the document we passed to the node's constructor.
 // We have not attached this paragraph to the document, so the document does not contain its text.
 Assert.assertEquals(para.getDocument(), doc);
 Assert.assertEquals("", doc.getText().trim());

 // Since the document owns this paragraph, we can apply one of its styles to the paragraph's contents.
 para.getParagraphFormat().setStyleName("Heading 1");

 // Add this node to the document, and then verify its contents.
 doc.getFirstSection().getBody().appendChild(para);

 Assert.assertEquals(doc.getFirstSection().getBody(), para.getParentNode());
 Assert.assertEquals("Hello world!", doc.getText().trim());
 
```

**Returns:**
[CompositeNode](../../com.aspose.words/compositenode/) - The immediate parent of this node.
### getPreferredWidth() {#getPreferredWidth}
```
public PreferredWidth getPreferredWidth()
```


Gets the table preferred width.

 **Remarks:** 

The default value is [PreferredWidth.AUTO](../../com.aspose.words/preferredwidth/\#AUTO).

 **Examples:** 

Shows how to set a table to auto fit to 50% of the width of the page.

```

 Document doc = new Document();
 DocumentBuilder builder = new DocumentBuilder(doc);

 Table table = builder.startTable();
 builder.insertCell();
 builder.write("Cell #1");
 builder.insertCell();
 builder.write("Cell #2");
 builder.insertCell();
 builder.write("Cell #3");

 table.setPreferredWidth(PreferredWidth.fromPercent(50.0));

 doc.save(getArtifactsDir() + "DocumentBuilder.InsertTableWithPreferredWidth.docx");
 
```

**Returns:**
[PreferredWidth](../../com.aspose.words/preferredwidth/) - The table preferred width.
### getPreviousSibling() {#getPreviousSibling}
```
public Node getPreviousSibling()
```


Gets the node immediately preceding this node.

 **Remarks:** 

If there is no preceding node, a  null  is returned.

 **Examples:** 

Shows how to use of methods of Node and CompositeNode to remove a section before the last section in the document.

```

 Document doc = new Document();
 DocumentBuilder builder = new DocumentBuilder(doc);

 builder.writeln("Section 1 text.");
 builder.insertBreak(BreakType.SECTION_BREAK_CONTINUOUS);
 builder.writeln("Section 2 text.");

 // Both sections are siblings of each other.
 Section lastSection = (Section) doc.getLastChild();
 Section firstSection = (Section) lastSection.getPreviousSibling();

 // Remove a section based on its sibling relationship with another section.
 if (lastSection.getPreviousSibling() != null)
     doc.removeChild(firstSection);

 // The section we removed was the first one, leaving the document with only the second.
 Assert.assertEquals("Section 2 text.", doc.getText().trim());
 
```

**Returns:**
[Node](../../com.aspose.words/node/) - The node immediately preceding this node.
### getRange() {#getRange}
```
public Range getRange()
```


Returns a [Range](../../com.aspose.words/range/) object that represents the portion of a document that is contained in this node.

 **Examples:** 

Shows how to delete all the nodes from a range.

```

 Document doc = new Document();
 DocumentBuilder builder = new DocumentBuilder(doc);

 // Add text to the first section in the document, and then add another section.
 builder.write("Section 1. ");
 builder.insertBreak(BreakType.SECTION_BREAK_CONTINUOUS);
 builder.write("Section 2.");

 Assert.assertEquals("Section 1. \fSection 2.", doc.getText().trim());

 // Remove the first section entirely by removing all the nodes
 // within its range, including the section itself.
 doc.getSections().get(0).getRange().delete();

 Assert.assertEquals(1, doc.getSections().getCount());
 Assert.assertEquals("Section 2.", doc.getText().trim());
 
```

**Returns:**
[Range](../../com.aspose.words/range/) - A [Range](../../com.aspose.words/range/) object that represents the portion of a document that is contained in this node.
### getRelativeHorizontalAlignment() {#getRelativeHorizontalAlignment}
```
public int getRelativeHorizontalAlignment()
```


Gets floating table relative horizontal alignment.

 **Examples:** 

Shows how set the location of floating tables.

```

 Document doc = new Document();
 DocumentBuilder builder = new DocumentBuilder(doc);

 Table table = builder.startTable();
 builder.insertCell();
 builder.write("Table 1, cell 1");
 builder.endTable();
 table.setPreferredWidth(PreferredWidth.fromPoints(300.0));

 // Set the table's location to a place on the page, such as, in this case, the bottom right corner.
 table.setRelativeVerticalAlignment(VerticalAlignment.BOTTOM);
 table.setRelativeHorizontalAlignment(HorizontalAlignment.RIGHT);

 table = builder.startTable();
 builder.insertCell();
 builder.write("Table 2, cell 1");
 builder.endTable();
 table.setPreferredWidth(PreferredWidth.fromPoints(300.0));

 // We can also set a horizontal and vertical offset in points from the paragraph's location where we inserted the table.
 table.setAbsoluteVerticalDistance(50.0);
 table.setAbsoluteHorizontalDistance(100.0);

 doc.save(getArtifactsDir() + "Table.ChangeFloatingTableProperties.docx");
 
```

**Returns:**
int - Floating table relative horizontal alignment. The returned value is one of [HorizontalAlignment](../../com.aspose.words/horizontalalignment/) constants.
### getRelativeVerticalAlignment() {#getRelativeVerticalAlignment}
```
public int getRelativeVerticalAlignment()
```


Gets floating table relative vertical alignment.

 **Examples:** 

Shows how set the location of floating tables.

```

 Document doc = new Document();
 DocumentBuilder builder = new DocumentBuilder(doc);

 Table table = builder.startTable();
 builder.insertCell();
 builder.write("Table 1, cell 1");
 builder.endTable();
 table.setPreferredWidth(PreferredWidth.fromPoints(300.0));

 // Set the table's location to a place on the page, such as, in this case, the bottom right corner.
 table.setRelativeVerticalAlignment(VerticalAlignment.BOTTOM);
 table.setRelativeHorizontalAlignment(HorizontalAlignment.RIGHT);

 table = builder.startTable();
 builder.insertCell();
 builder.write("Table 2, cell 1");
 builder.endTable();
 table.setPreferredWidth(PreferredWidth.fromPoints(300.0));

 // We can also set a horizontal and vertical offset in points from the paragraph's location where we inserted the table.
 table.setAbsoluteVerticalDistance(50.0);
 table.setAbsoluteHorizontalDistance(100.0);

 doc.save(getArtifactsDir() + "Table.ChangeFloatingTableProperties.docx");
 
```

**Returns:**
int - Floating table relative vertical alignment. The returned value is one of [VerticalAlignment](../../com.aspose.words/verticalalignment/) constants.
### getRightPadding() {#getRightPadding}
```
public double getRightPadding()
```


Gets the amount of space (in points) to add to the right of the contents of cells.

 **Examples:** 

Shows how to configure content padding in a table.

```

 Document doc = new Document();
 DocumentBuilder builder = new DocumentBuilder(doc);

 Table table = builder.startTable();
 builder.insertCell();
 builder.write("Row 1, cell 1.");
 builder.insertCell();
 builder.write("Row 1, cell 2.");
 builder.endTable();

 // For every cell in the table, set the distance between its contents and each of its borders.
 // This table will maintain the minimum padding distance by wrapping text.
 table.setLeftPadding(30.0);
 table.setRightPadding(60.0);
 table.setTopPadding(10.0);
 table.setBottomPadding(90.0);
 table.setPreferredWidth(PreferredWidth.fromPoints(250.0));

 doc.save(getArtifactsDir() + "DocumentBuilder.SetRowFormatting.docx");
 
```

**Returns:**
double - The amount of space (in points) to add to the right of the contents of cells.
### getRows() {#getRows}
```
public RowCollection getRows()
```


Provides typed access to the rows of the table.

 **Examples:** 

Shows how to combine the rows from two tables into one.

```

 Document doc = new Document(getMyDir() + "Tables.docx");

 // Below are two ways of getting a table from a document.
 // 1 -  From the "Tables" collection of a Body node:
 Table firstTable = doc.getFirstSection().getBody().getTables().get(0);

 // 2 -  Using the "GetChild" method:
 Table secondTable = (Table) doc.getChild(NodeType.TABLE, 1, true);

 // Append all rows from the current table to the next.
 while (secondTable.hasChildNodes())
     firstTable.getRows().add(secondTable.getFirstRow());

 // Remove the empty table container.
 secondTable.remove();

 doc.save(getArtifactsDir() + "Table.CombineTables.docx");
 
```

Shows how to iterate through all tables in the document and print the contents of each cell.

```

 Document doc = new Document(getMyDir() + "Tables.docx");
 TableCollection tables = doc.getFirstSection().getBody().getTables();

 Assert.assertEquals(2, tables.toArray().length);

 for (int i = 0; i < tables.getCount(); i++) {
     System.out.println(MessageFormat.format("Start of Table {0}", i));

     RowCollection rows = tables.get(i).getRows();

     for (int j = 0; j < rows.getCount(); j++) {
         System.out.println(MessageFormat.format("\tStart of Row {0}", j));

         CellCollection cells = rows.get(j).getCells();

         for (int k = 0; k < cells.getCount(); k++) {
             String cellText = cells.get(k).toString(SaveFormat.TEXT).trim();
             System.out.println(MessageFormat.format("\t\tContents of Cell:{0} = \"{1}\"", k, cellText));
         }

         System.out.println(MessageFormat.format("\tEnd of Row {0}", j));
     }

     System.out.println(MessageFormat.format("End of Table {0}\n", i));
 }
 
```

**Returns:**
[RowCollection](../../com.aspose.words/rowcollection/) - The corresponding [RowCollection](../../com.aspose.words/rowcollection/) value.
### getStyle() {#getStyle}
```
public Style getStyle()
```


Gets the table style applied to this table.

 **Examples:** 

Shows how to create custom style settings for the table.

```

 Document doc = new Document();
 DocumentBuilder builder = new DocumentBuilder(doc);

 Table table = builder.startTable();
 builder.insertCell();
 builder.write("Name");
 builder.insertCell();
 builder.write("\u0645\u0631\u062d\u0628\u064b\u0627");
 builder.endRow();
 builder.insertCell();
 builder.insertCell();
 builder.endTable();

 TableStyle tableStyle = (TableStyle) doc.getStyles().add(StyleType.TABLE, "MyTableStyle1");
 tableStyle.setAllowBreakAcrossPages(true);
 tableStyle.setBidi(true);
 tableStyle.setCellSpacing(5.0);
 tableStyle.setBottomPadding(20.0);
 tableStyle.setLeftPadding(5.0);
 tableStyle.setRightPadding(10.0);
 tableStyle.setTopPadding(20.0);
 tableStyle.getShading().setBackgroundPatternColor(Color.WHITE);
 tableStyle.getBorders().setColor(Color.BLACK);
 tableStyle.getBorders().setLineStyle(LineStyle.DOT_DASH);
 tableStyle.setVerticalAlignment(CellVerticalAlignment.CENTER);

 table.setStyle(tableStyle);

 // Setting the style properties of a table may affect the properties of the table itself.
 Assert.assertTrue(table.getBidi());
 Assert.assertEquals(5.0d, table.getCellSpacing());
 Assert.assertEquals("MyTableStyle1", table.getStyleName());

 doc.save(getArtifactsDir() + "Table.TableStyleCreation.docx");
 
```

**Returns:**
[Style](../../com.aspose.words/style/) - The table style applied to this table.
### getStyleIdentifier() {#getStyleIdentifier}
```
public int getStyleIdentifier()
```


Gets the locale independent style identifier of the table style applied to this table.

 **Examples:** 

Shows how to build a new table while applying a style.

```

 Document doc = new Document();
 DocumentBuilder builder = new DocumentBuilder(doc);
 Table table = builder.startTable();

 // We must insert at least one row before setting any table formatting.
 builder.insertCell();

 // Set the table style used based on the style identifier.
 // Note that not all table styles are available when saving to .doc format.
 table.setStyleIdentifier(StyleIdentifier.MEDIUM_SHADING_1_ACCENT_1);

 // Partially apply the style to features of the table based on predicates, then build the table.
 table.setStyleOptions(TableStyleOptions.FIRST_COLUMN | TableStyleOptions.ROW_BANDS | TableStyleOptions.FIRST_ROW);
 table.autoFit(AutoFitBehavior.AUTO_FIT_TO_CONTENTS);

 builder.writeln("Item");
 builder.getCellFormat().setRightPadding(40.0);
 builder.insertCell();
 builder.writeln("Quantity (kg)");
 builder.endRow();

 builder.insertCell();
 builder.writeln("Apples");
 builder.insertCell();
 builder.writeln("20");
 builder.endRow();

 builder.insertCell();
 builder.writeln("Bananas");
 builder.insertCell();
 builder.writeln("40");
 builder.endRow();

 builder.insertCell();
 builder.writeln("Carrots");
 builder.insertCell();
 builder.writeln("50");
 builder.endRow();

 doc.save(getArtifactsDir() + "DocumentBuilder.InsertTableWithStyle.docx");
 
```

**Returns:**
int - The locale independent style identifier of the table style applied to this table. The returned value is one of [StyleIdentifier](../../com.aspose.words/styleidentifier/) constants.
### getStyleName() {#getStyleName}
```
public String getStyleName()
```


Gets the name of the table style applied to this table.

 **Examples:** 

Shows how to create custom style settings for the table.

```

 Document doc = new Document();
 DocumentBuilder builder = new DocumentBuilder(doc);

 Table table = builder.startTable();
 builder.insertCell();
 builder.write("Name");
 builder.insertCell();
 builder.write("\u0645\u0631\u062d\u0628\u064b\u0627");
 builder.endRow();
 builder.insertCell();
 builder.insertCell();
 builder.endTable();

 TableStyle tableStyle = (TableStyle) doc.getStyles().add(StyleType.TABLE, "MyTableStyle1");
 tableStyle.setAllowBreakAcrossPages(true);
 tableStyle.setBidi(true);
 tableStyle.setCellSpacing(5.0);
 tableStyle.setBottomPadding(20.0);
 tableStyle.setLeftPadding(5.0);
 tableStyle.setRightPadding(10.0);
 tableStyle.setTopPadding(20.0);
 tableStyle.getShading().setBackgroundPatternColor(Color.WHITE);
 tableStyle.getBorders().setColor(Color.BLACK);
 tableStyle.getBorders().setLineStyle(LineStyle.DOT_DASH);
 tableStyle.setVerticalAlignment(CellVerticalAlignment.CENTER);

 table.setStyle(tableStyle);

 // Setting the style properties of a table may affect the properties of the table itself.
 Assert.assertTrue(table.getBidi());
 Assert.assertEquals(5.0d, table.getCellSpacing());
 Assert.assertEquals("MyTableStyle1", table.getStyleName());

 doc.save(getArtifactsDir() + "Table.TableStyleCreation.docx");
 
```

**Returns:**
java.lang.String - The name of the table style applied to this table.
### getStyleOptions() {#getStyleOptions}
```
public int getStyleOptions()
```


Gets bit flags that specify how a table style is applied to this table.

 **Examples:** 

Shows how to build a new table while applying a style.

```

 Document doc = new Document();
 DocumentBuilder builder = new DocumentBuilder(doc);
 Table table = builder.startTable();

 // We must insert at least one row before setting any table formatting.
 builder.insertCell();

 // Set the table style used based on the style identifier.
 // Note that not all table styles are available when saving to .doc format.
 table.setStyleIdentifier(StyleIdentifier.MEDIUM_SHADING_1_ACCENT_1);

 // Partially apply the style to features of the table based on predicates, then build the table.
 table.setStyleOptions(TableStyleOptions.FIRST_COLUMN | TableStyleOptions.ROW_BANDS | TableStyleOptions.FIRST_ROW);
 table.autoFit(AutoFitBehavior.AUTO_FIT_TO_CONTENTS);

 builder.writeln("Item");
 builder.getCellFormat().setRightPadding(40.0);
 builder.insertCell();
 builder.writeln("Quantity (kg)");
 builder.endRow();

 builder.insertCell();
 builder.writeln("Apples");
 builder.insertCell();
 builder.writeln("20");
 builder.endRow();

 builder.insertCell();
 builder.writeln("Bananas");
 builder.insertCell();
 builder.writeln("40");
 builder.endRow();

 builder.insertCell();
 builder.writeln("Carrots");
 builder.insertCell();
 builder.writeln("50");
 builder.endRow();

 doc.save(getArtifactsDir() + "DocumentBuilder.InsertTableWithStyle.docx");
 
```

**Returns:**
int - Bit flags that specify how a table style is applied to this table. The returned value is a bitwise combination of [TableStyleOptions](../../com.aspose.words/tablestyleoptions/) constants.
### getText() {#getText}
```
public String getText()
```


Gets the text of this node and of all its children.

 **Remarks:** 

The returned string includes all control and special characters as described in [ControlChar](../../com.aspose.words/controlchar/).

 **Examples:** 

Shows the difference between calling the GetText and ToString methods on a node.

```

 Document doc = new Document();

 DocumentBuilder builder = new DocumentBuilder(doc);
 builder.insertField("MERGEFIELD Field");

 // GetText will retrieve the visible text as well as field codes and special characters.
 Assert.assertEquals("MERGEFIELD Field«Field»\f", doc.getText());

 // ToString will give us the document's appearance if saved to a passed save format.
 Assert.assertEquals("«Field»\r\n", doc.toString(SaveFormat.TEXT));
 
```

Shows how to output all paragraphs in a document that are list items.

```

 Document doc = new Document();
 DocumentBuilder builder = new DocumentBuilder(doc);

 builder.getListFormat().applyNumberDefault();
 builder.writeln("Numbered list item 1");
 builder.writeln("Numbered list item 2");
 builder.writeln("Numbered list item 3");
 builder.getListFormat().removeNumbers();

 builder.getListFormat().applyBulletDefault();
 builder.writeln("Bulleted list item 1");
 builder.writeln("Bulleted list item 2");
 builder.writeln("Bulleted list item 3");
 builder.getListFormat().removeNumbers();

 NodeCollection paras = doc.getChildNodes(NodeType.PARAGRAPH, true);
 for (Paragraph para : (Iterable) paras) {
     if (para.getListFormat().isListItem()) {
         System.out.println(java.text.MessageFormat.format("*** A paragraph belongs to list {0}", para.getListFormat().getList().getListId()));
         System.out.println(para.getText());
     }
 }
 
```

**Returns:**
java.lang.String
### getTextWrapping() {#getTextWrapping}
```
public int getTextWrapping()
```


Gets [getTextWrapping()](../../com.aspose.words/table/\#getTextWrapping) / [setTextWrapping(int)](../../com.aspose.words/table/\#setTextWrapping-int) for table.

 **Examples:** 

Shows how to work with table text wrapping.

```

 Document doc = new Document();
 DocumentBuilder builder = new DocumentBuilder(doc);

 Table table = builder.startTable();
 builder.insertCell();
 builder.write("Cell 1");
 builder.insertCell();
 builder.write("Cell 2");
 builder.endTable();
 table.setPreferredWidth(PreferredWidth.fromPoints(300.0));

 builder.getFont().setSize(16.0);
 builder.writeln("Lorem ipsum dolor sit amet, consectetur adipiscing elit, sed do eiusmod tempor incididunt ut labore et dolore magna aliqua.");

 // Set the "TextWrapping" property to "TextWrapping.Around" to get the table to wrap text around it,
 // and push it down into the paragraph below by setting the position.
 table.setTextWrapping(TextWrapping.AROUND);
 table.setAbsoluteHorizontalDistance(100.0);
 table.setAbsoluteVerticalDistance(20.0);

 doc.save(getArtifactsDir() + "Table.WrapText.docx");
 
```

**Returns:**
int - [getTextWrapping()](../../com.aspose.words/table/\#getTextWrapping) / [setTextWrapping(int)](../../com.aspose.words/table/\#setTextWrapping-int) for table. The returned value is one of [TextWrapping](../../com.aspose.words/textwrapping/) constants.
### getTitle() {#getTitle}
```
public String getTitle()
```


Gets title of this table. It provides an alternative text representation of the information contained in the table.

 **Remarks:** 

The default value is an empty string.

This property is meaningful for ISO/IEC 29500 compliant DOCX documents ( [OoxmlCompliance](../../com.aspose.words/ooxmlcompliance/)). When saved to pre-ISO/IEC 29500 formats, the property is ignored.

 **Examples:** 

Shows how to build a nested table without using a document builder.

```

 public void createNestedTable() throws Exception {
     Document doc = new Document();

     // Create the outer table with three rows and four columns, and then add it to the document.
     Table outerTable = createTable(doc, 3, 4, "Outer Table");
     doc.getFirstSection().getBody().appendChild(outerTable);

     // Create another table with two rows and two columns and then insert it into the first table's first cell.
     Table innerTable = createTable(doc, 2, 2, "Inner Table");
     outerTable.getFirstRow().getFirstCell().appendChild(innerTable);

     doc.save(getArtifactsDir() + "Table.CreateNestedTable.docx");
 }

 // Creates a new table in the document with the given dimensions and text in each cell.
 private Table createTable(final Document doc, final int rowCount, final int cellCount, final String cellText) throws Exception {
     Table table = new Table(doc);

     for (int rowId = 1; rowId <= rowCount; rowId++) {
         Row row = new Row(doc);
         table.appendChild(row);

         for (int cellId = 1; cellId <= cellCount; cellId++) {
             Cell cell = new Cell(doc);
             cell.appendChild(new Paragraph(doc));
             cell.getFirstParagraph().appendChild(new Run(doc, cellText));

             row.appendChild(cell);
         }
     }

     // You can use the "Title" and "Description" properties to add a title and description respectively to your table.
     // The table must have at least one row before we can use these properties.
     // These properties are meaningful for ISO / IEC 29500 compliant .docx documents (see the OoxmlCompliance class).
     // If we save the document to pre-ISO/IEC 29500 formats, Microsoft Word ignores these properties.
     table.setTitle("Aspose table title");
     table.setDescription("Aspose table description");

     return table;
 }
 
```

**Returns:**
java.lang.String - Title of this table.
### getTopPadding() {#getTopPadding}
```
public double getTopPadding()
```


Gets the amount of space (in points) to add above the contents of cells.

 **Examples:** 

Shows how to configure content padding in a table.

```

 Document doc = new Document();
 DocumentBuilder builder = new DocumentBuilder(doc);

 Table table = builder.startTable();
 builder.insertCell();
 builder.write("Row 1, cell 1.");
 builder.insertCell();
 builder.write("Row 1, cell 2.");
 builder.endTable();

 // For every cell in the table, set the distance between its contents and each of its borders.
 // This table will maintain the minimum padding distance by wrapping text.
 table.setLeftPadding(30.0);
 table.setRightPadding(60.0);
 table.setTopPadding(10.0);
 table.setBottomPadding(90.0);
 table.setPreferredWidth(PreferredWidth.fromPoints(250.0));

 doc.save(getArtifactsDir() + "DocumentBuilder.SetRowFormatting.docx");
 
```

**Returns:**
double - The amount of space (in points) to add above the contents of cells.
### getVerticalAnchor() {#getVerticalAnchor}
```
public int getVerticalAnchor()
```


Gets the base object from which the vertical positioning of floating table should be calculated. Default value is [RelativeVerticalPosition.MARGIN](../../com.aspose.words/relativeverticalposition/\#MARGIN).

 **Examples:** 

Shows how to work with floating tables properties.

```

 Document doc = new Document(getMyDir() + "Table wrapped by text.docx");

 Table table = doc.getFirstSection().getBody().getTables().get(0);

 if (table.getTextWrapping() == TextWrapping.AROUND) {
     Assert.assertEquals(RelativeHorizontalPosition.MARGIN, table.getHorizontalAnchor());
     Assert.assertEquals(RelativeVerticalPosition.PARAGRAPH, table.getVerticalAnchor());
     Assert.assertEquals(false, table.getAllowOverlap());

     // Only Margin, Page, Column available in RelativeHorizontalPosition for HorizontalAnchor setter.
     // The ArgumentException will be thrown for any other values.
     table.setHorizontalAnchor(RelativeHorizontalPosition.COLUMN);

     // Only Margin, Page, Paragraph available in RelativeVerticalPosition for VerticalAnchor setter.
     // The ArgumentException will be thrown for any other values.
     table.setVerticalAnchor(RelativeVerticalPosition.PAGE);
 }
 
```

**Returns:**
int - The base object from which the vertical positioning of floating table should be calculated. The returned value is one of [RelativeVerticalPosition](../../com.aspose.words/relativeverticalposition/) constants.
### hasChildNodes() {#hasChildNodes}
```
public boolean hasChildNodes()
```


Returns  true  if this node has any child nodes.

 **Examples:** 

Shows how to combine the rows from two tables into one.

```

 Document doc = new Document(getMyDir() + "Tables.docx");

 // Below are two ways of getting a table from a document.
 // 1 -  From the "Tables" collection of a Body node:
 Table firstTable = doc.getFirstSection().getBody().getTables().get(0);

 // 2 -  Using the "GetChild" method:
 Table secondTable = (Table) doc.getChild(NodeType.TABLE, 1, true);

 // Append all rows from the current table to the next.
 while (secondTable.hasChildNodes())
     firstTable.getRows().add(secondTable.getFirstRow());

 // Remove the empty table container.
 secondTable.remove();

 doc.save(getArtifactsDir() + "Table.CombineTables.docx");
 
```

**Returns:**
boolean -  true  if this node has any child nodes.
### hashCode() {#hashCode}
```
public native int hashCode()
```




**Returns:**
int
### indexOf(Node child) {#indexOf-com.aspose.words.Node}
```
public int indexOf(Node child)
```


Returns the index of the specified child node in the child node array.

 **Remarks:** 

Returns -1 if the node is not found in the child nodes.

 **Examples:** 

Shows how to get the index of a given child node from its parent.

```

 Document doc = new Document(getMyDir() + "Rendering.docx");

 Body body = doc.getFirstSection().getBody();

 // Retrieve the index of the last paragraph in the body of the first section.
 Assert.assertEquals(24, body.getChildNodes().indexOf(body.getLastParagraph()));
 
```

**Parameters:**
| Parameter | Type | Description |
| --- | --- | --- |
| child | [Node](../../com.aspose.words/node/) |  |

**Returns:**
int
### insertAfter(Node newChild, Node refChild) {#insertAfter-com.aspose.words.Node-com.aspose.words.Node}
```
public Node insertAfter(Node newChild, Node refChild)
```


Inserts the specified node immediately after the specified reference node.

 **Remarks:** 

If  refChild  is  null , inserts  newChild  at the beginning of the list of child nodes.

 **Remarks:** 

If the  newChild  is already in the tree, it is first removed.

If the node being inserted was created from another document, you should use **M:Aspose.Words.DocumentBase.ImportNode(Aspose.Words.Node,System.Boolean,Aspose.Words.ImportFormatMode)** to import the node to the current document. The imported node can then be inserted into the current document.

**Parameters:**
| Parameter | Type | Description |
| --- | --- | --- |
| newChild | [Node](../../com.aspose.words/node/) | The [Node](../../com.aspose.words/node/) to insert. |
| refChild | [Node](../../com.aspose.words/node/) | The [Node](../../com.aspose.words/node/) that is the reference node. The  newChild  is placed after the  refChild . |

**Returns:**
[Node](../../com.aspose.words/node/) - The inserted node.

 **Examples:** 

Shows how to replace all textbox shapes with image shapes.

```

 Document doc = new Document(getMyDir() + "Textboxes in drawing canvas.docx");

 List shapeList = Arrays.stream(doc.getChildNodes(NodeType.SHAPE, true).toArray())
         .filter(Shape.class::isInstance)
         .map(Shape.class::cast)
         .collect(Collectors.toList());

 Assert.assertEquals(3, IterableUtils.countMatches(shapeList, s -> s.getShapeType() == ShapeType.TEXT_BOX));
 Assert.assertEquals(1, IterableUtils.countMatches(shapeList, s -> s.getShapeType() == ShapeType.IMAGE));

 for (Shape shape : shapeList) {
     if (((shape.getShapeType()) == (ShapeType.TEXT_BOX))) {
         Shape replacementShape = new Shape(doc, ShapeType.IMAGE);
         replacementShape.getImageData().setImage(getImageDir() + "Logo.jpg");
         replacementShape.setLeft(shape.getLeft());
         replacementShape.setTop(shape.getTop());
         replacementShape.setWidth(shape.getWidth());
         replacementShape.setHeight(shape.getHeight());
         replacementShape.setRelativeHorizontalPosition(shape.getRelativeHorizontalPosition());
         replacementShape.setRelativeVerticalPosition(shape.getRelativeVerticalPosition());
         replacementShape.setHorizontalAlignment(shape.getHorizontalAlignment());
         replacementShape.setVerticalAlignment(shape.getVerticalAlignment());
         replacementShape.setWrapType(shape.getWrapType());
         replacementShape.setWrapSide(shape.getWrapSide());

         shape.getParentNode().insertAfter(replacementShape, shape);
         shape.remove();
     }
 }

 shapeList = Arrays.stream(doc.getChildNodes(NodeType.SHAPE, true).toArray())
         .filter(Shape.class::isInstance)
         .map(Shape.class::cast)
         .collect(Collectors.toList());

 Assert.assertEquals(0, IterableUtils.countMatches(shapeList, s -> s.getShapeType() == ShapeType.TEXT_BOX));
 Assert.assertEquals(4, IterableUtils.countMatches(shapeList, s -> s.getShapeType() == ShapeType.IMAGE));

 doc.save(getArtifactsDir() + "Shape.ReplaceTextboxesWithImages.docx");
 
```

Shows how to add, update and delete child nodes in a CompositeNode's collection of children.

```

 Document doc = new Document();

 // An empty document, by default, has one paragraph.
 Assert.assertEquals(1, doc.getFirstSection().getBody().getParagraphs().getCount());

 // Composite nodes such as our paragraph can contain other composite and inline nodes as children.
 Paragraph paragraph = doc.getFirstSection().getBody().getFirstParagraph();
 Run paragraphText = new Run(doc, "Initial text. ");
 paragraph.appendChild(paragraphText);

 // Create three more run nodes.
 Run run1 = new Run(doc, "Run 1. ");
 Run run2 = new Run(doc, "Run 2. ");
 Run run3 = new Run(doc, "Run 3. ");

 // The document body will not display these runs until we insert them into a composite node
 // that itself is a part of the document's node tree, as we did with the first run.
 // We can determine where the text contents of nodes that we insert
 // appears in the document by specifying an insertion location relative to another node in the paragraph.
 Assert.assertEquals("Initial text.", paragraph.getText().trim());

 // Insert the second run into the paragraph in front of the initial run.
 paragraph.insertBefore(run2, paragraphText);

 Assert.assertEquals("Run 2. Initial text.", paragraph.getText().trim());

 // Insert the third run after the initial run.
 paragraph.insertAfter(run3, paragraphText);

 Assert.assertEquals("Run 2. Initial text. Run 3.", paragraph.getText().trim());

 // Insert the first run to the start of the paragraph's child nodes collection.
 paragraph.prependChild(run1);

 Assert.assertEquals("Run 1. Run 2. Initial text. Run 3.", paragraph.getText().trim());
 Assert.assertEquals(4, paragraph.getChildNodes(NodeType.ANY, true).getCount());

 // We can modify the contents of the run by editing and deleting existing child nodes.
 ((Run) paragraph.getChildNodes(NodeType.RUN, true).get(1)).setText("Updated run 2. ");
 paragraph.getChildNodes(NodeType.RUN, true).remove(paragraphText);

 Assert.assertEquals("Run 1. Updated run 2. Run 3.", paragraph.getText().trim());
 Assert.assertEquals(3, paragraph.getChildNodes(NodeType.ANY, true).getCount());
 
```
### insertBefore(Node newChild, Node refChild) {#insertBefore-com.aspose.words.Node-com.aspose.words.Node}
```
public Node insertBefore(Node newChild, Node refChild)
```


Inserts the specified node immediately before the specified reference node.

 **Remarks:** 

If  refChild  is  null , inserts  newChild  at the end of the list of child nodes.

 **Remarks:** 

If the  newChild  is already in the tree, it is first removed.

If the node being inserted was created from another document, you should use **M:Aspose.Words.DocumentBase.ImportNode(Aspose.Words.Node,System.Boolean,Aspose.Words.ImportFormatMode)** to import the node to the current document. The imported node can then be inserted into the current document.

**Parameters:**
| Parameter | Type | Description |
| --- | --- | --- |
| newChild | [Node](../../com.aspose.words/node/) | The [Node](../../com.aspose.words/node/) to insert. |
| refChild | [Node](../../com.aspose.words/node/) | The [Node](../../com.aspose.words/node/) that is the reference node. The  newChild  is placed before this node. |

**Returns:**
[Node](../../com.aspose.words/node/) - The inserted node.

 **Examples:** 

Shows how to add, update and delete child nodes in a CompositeNode's collection of children.

```

 Document doc = new Document();

 // An empty document, by default, has one paragraph.
 Assert.assertEquals(1, doc.getFirstSection().getBody().getParagraphs().getCount());

 // Composite nodes such as our paragraph can contain other composite and inline nodes as children.
 Paragraph paragraph = doc.getFirstSection().getBody().getFirstParagraph();
 Run paragraphText = new Run(doc, "Initial text. ");
 paragraph.appendChild(paragraphText);

 // Create three more run nodes.
 Run run1 = new Run(doc, "Run 1. ");
 Run run2 = new Run(doc, "Run 2. ");
 Run run3 = new Run(doc, "Run 3. ");

 // The document body will not display these runs until we insert them into a composite node
 // that itself is a part of the document's node tree, as we did with the first run.
 // We can determine where the text contents of nodes that we insert
 // appears in the document by specifying an insertion location relative to another node in the paragraph.
 Assert.assertEquals("Initial text.", paragraph.getText().trim());

 // Insert the second run into the paragraph in front of the initial run.
 paragraph.insertBefore(run2, paragraphText);

 Assert.assertEquals("Run 2. Initial text.", paragraph.getText().trim());

 // Insert the third run after the initial run.
 paragraph.insertAfter(run3, paragraphText);

 Assert.assertEquals("Run 2. Initial text. Run 3.", paragraph.getText().trim());

 // Insert the first run to the start of the paragraph's child nodes collection.
 paragraph.prependChild(run1);

 Assert.assertEquals("Run 1. Run 2. Initial text. Run 3.", paragraph.getText().trim());
 Assert.assertEquals(4, paragraph.getChildNodes(NodeType.ANY, true).getCount());

 // We can modify the contents of the run by editing and deleting existing child nodes.
 ((Run) paragraph.getChildNodes(NodeType.RUN, true).get(1)).setText("Updated run 2. ");
 paragraph.getChildNodes(NodeType.RUN, true).remove(paragraphText);

 Assert.assertEquals("Run 1. Updated run 2. Run 3.", paragraph.getText().trim());
 Assert.assertEquals(3, paragraph.getChildNodes(NodeType.ANY, true).getCount());
 
```
### isComposite() {#isComposite}
```
public boolean isComposite()
```


Returns  true  as this node can have child nodes.

 **Examples:** 

Shows how to traverse a composite node's tree of child nodes.

```

 public void recurseChildren() throws Exception {
     Document doc = new Document(getMyDir() + "Paragraphs.docx");

     // Any node that can contain child nodes, such as the document itself, is composite.
     Assert.assertTrue(doc.isComposite());

     // Invoke the recursive function that will go through and print all the child nodes of a composite node.
     traverseAllNodes(doc, 0);
 }

 /// 
 /// Recursively traverses a node tree while printing the type of each node
 /// with an indent depending on depth as well as the contents of all inline nodes.
 /// 
 public void traverseAllNodes(CompositeNode parentNode, int depth) {
     for (Node childNode = parentNode.getFirstChild(); childNode != null; childNode = childNode.getNextSibling()) {
         System.out.println(MessageFormat.format("{0}{1}", String.format("    ", depth), Node.nodeTypeToString(childNode.getNodeType())));

         // Recurse into the node if it is a composite node. Otherwise, print its contents if it is an inline node.
         if (childNode.isComposite()) {
             System.out.println();
             traverseAllNodes((CompositeNode) childNode, depth + 1);
         } else if (childNode instanceof Inline) {
             System.out.println(" - \"{childNode.GetText().Trim()}\"");
         } else {
             System.out.println();
         }
     }
 }
 
```

**Returns:**
boolean -  true  as this node can have child nodes.
### iterator() {#iterator}
```
public Iterator iterator()
```


Provides support for the for each style iteration over the child nodes of this node.

 **Examples:** 

Shows how to traverse through a composite node's collection of child nodes.

```

 Document doc = new Document();

 // Add two runs and one shape as child nodes to the first paragraph of this document.
 Paragraph paragraph = (Paragraph) doc.getChild(NodeType.PARAGRAPH, 0, true);
 paragraph.appendChild(new Run(doc, "Hello world! "));

 Shape shape = new Shape(doc, ShapeType.RECTANGLE);
 shape.setWidth(200.0);
 shape.setHeight(200.0);
 // Note that the 'CustomNodeId' is not saved to an output file and exists only during the node lifetime.
 shape.setCustomNodeId(100);
 shape.setWrapType(WrapType.INLINE);
 paragraph.appendChild(shape);

 paragraph.appendChild(new Run(doc, "Hello again!"));

 // Iterate through the paragraph's collection of immediate children,
 // and print any runs or shapes that we find within.
 NodeCollection children = paragraph.getChildNodes();

 Assert.assertEquals(3, paragraph.getChildNodes().getCount());

 for (Node child : (Iterable) children)
     switch (child.getNodeType()) {
         case NodeType.RUN:
             System.out.println("Run contents:");
             System.out.println("\t\"{child.GetText().Trim()}\"");
             break;
         case NodeType.SHAPE:
             Shape childShape = (Shape) child;
             System.out.println("Shape:");
             System.out.println("\t{childShape.ShapeType}, {childShape.Width}x{childShape.Height}");
             break;
     }
 
```

**Returns:**
java.util.Iterator
### nextPreOrder(Node rootNode) {#nextPreOrder-com.aspose.words.Node}
```
public Node nextPreOrder(Node rootNode)
```


Gets next node according to the pre-order tree traversal algorithm.

**Parameters:**
| Parameter | Type | Description |
| --- | --- | --- |
| rootNode | [Node](../../com.aspose.words/node/) | The top node (limit) of traversal. |

**Returns:**
[Node](../../com.aspose.words/node/) - Next node in pre-order order. Null if reached the  rootNode .

 **Examples:** 

Shows how to traverse the document's node tree using the pre-order traversal algorithm, and delete any encountered shape with an image.

```

 Document doc = new Document(getMyDir() + "Images.docx");
 ArrayList shapes = (ArrayList) IterableUtils.toList(doc.getChildNodes(NodeType.SHAPE, true));

 Assert.assertEquals(9, IterableUtils.countMatches(shapes, s -> {
     try {
         return s.hasImage();
     } catch (Exception e) {
         e.printStackTrace();
     }
     return false;
 }));

 Node curNode = doc;
 while (curNode != null) {
     Node nextNode = curNode.nextPreOrder(doc);

     if (curNode.previousPreOrder(doc) != null && nextNode != null)
         Assert.assertEquals(curNode, nextNode.previousPreOrder(doc));

     if (curNode.getNodeType() == NodeType.SHAPE && ((Shape) curNode).hasImage())
         curNode.remove();

     curNode = nextNode;
 }

 shapes = (ArrayList) IterableUtils.toList(doc.getChildNodes(NodeType.SHAPE, true));

 Assert.assertEquals(0, IterableUtils.countMatches(shapes, s -> {
     try {
         return s.hasImage();
     } catch (Exception e) {
         e.printStackTrace();
     }
     return false;
 }));
 
```
### nodeTypeToString(int nodeType) {#nodeTypeToString-int}
```
public static String nodeTypeToString(int nodeType)
```




**Parameters:**
| Parameter | Type | Description |
| --- | --- | --- |
| nodeType | int |  |

**Returns:**
java.lang.String
### notify() {#notify}
```
public final native void notify()
```




### notifyAll() {#notifyAll}
```
public final native void notifyAll()
```




### prependChild(Node newChild) {#prependChild-com.aspose.words.Node}
```
public Node prependChild(Node newChild)
```


Adds the specified node to the beginning of the list of child nodes for this node.

 **Remarks:** 

If the  newChild  is already in the tree, it is first removed.

If the node being inserted was created from another document, you should use **M:Aspose.Words.DocumentBase.ImportNode(Aspose.Words.Node,System.Boolean,Aspose.Words.ImportFormatMode)** to import the node to the current document. The imported node can then be inserted into the current document.

**Parameters:**
| Parameter | Type | Description |
| --- | --- | --- |
| newChild | [Node](../../com.aspose.words/node/) | The node to add. |

**Returns:**
[Node](../../com.aspose.words/node/) - The node added.

 **Examples:** 

Shows how to add, update and delete child nodes in a CompositeNode's collection of children.

```

 Document doc = new Document();

 // An empty document, by default, has one paragraph.
 Assert.assertEquals(1, doc.getFirstSection().getBody().getParagraphs().getCount());

 // Composite nodes such as our paragraph can contain other composite and inline nodes as children.
 Paragraph paragraph = doc.getFirstSection().getBody().getFirstParagraph();
 Run paragraphText = new Run(doc, "Initial text. ");
 paragraph.appendChild(paragraphText);

 // Create three more run nodes.
 Run run1 = new Run(doc, "Run 1. ");
 Run run2 = new Run(doc, "Run 2. ");
 Run run3 = new Run(doc, "Run 3. ");

 // The document body will not display these runs until we insert them into a composite node
 // that itself is a part of the document's node tree, as we did with the first run.
 // We can determine where the text contents of nodes that we insert
 // appears in the document by specifying an insertion location relative to another node in the paragraph.
 Assert.assertEquals("Initial text.", paragraph.getText().trim());

 // Insert the second run into the paragraph in front of the initial run.
 paragraph.insertBefore(run2, paragraphText);

 Assert.assertEquals("Run 2. Initial text.", paragraph.getText().trim());

 // Insert the third run after the initial run.
 paragraph.insertAfter(run3, paragraphText);

 Assert.assertEquals("Run 2. Initial text. Run 3.", paragraph.getText().trim());

 // Insert the first run to the start of the paragraph's child nodes collection.
 paragraph.prependChild(run1);

 Assert.assertEquals("Run 1. Run 2. Initial text. Run 3.", paragraph.getText().trim());
 Assert.assertEquals(4, paragraph.getChildNodes(NodeType.ANY, true).getCount());

 // We can modify the contents of the run by editing and deleting existing child nodes.
 ((Run) paragraph.getChildNodes(NodeType.RUN, true).get(1)).setText("Updated run 2. ");
 paragraph.getChildNodes(NodeType.RUN, true).remove(paragraphText);

 Assert.assertEquals("Run 1. Updated run 2. Run 3.", paragraph.getText().trim());
 Assert.assertEquals(3, paragraph.getChildNodes(NodeType.ANY, true).getCount());
 
```
### previousPreOrder(Node rootNode) {#previousPreOrder-com.aspose.words.Node}
```
public Node previousPreOrder(Node rootNode)
```


Gets the previous node according to the pre-order tree traversal algorithm.

**Parameters:**
| Parameter | Type | Description |
| --- | --- | --- |
| rootNode | [Node](../../com.aspose.words/node/) | The top node (limit) of traversal. |

**Returns:**
[Node](../../com.aspose.words/node/) - Previous node in pre-order order. Null if reached the  rootNode .

 **Examples:** 

Shows how to traverse the document's node tree using the pre-order traversal algorithm, and delete any encountered shape with an image.

```

 Document doc = new Document(getMyDir() + "Images.docx");
 ArrayList shapes = (ArrayList) IterableUtils.toList(doc.getChildNodes(NodeType.SHAPE, true));

 Assert.assertEquals(9, IterableUtils.countMatches(shapes, s -> {
     try {
         return s.hasImage();
     } catch (Exception e) {
         e.printStackTrace();
     }
     return false;
 }));

 Node curNode = doc;
 while (curNode != null) {
     Node nextNode = curNode.nextPreOrder(doc);

     if (curNode.previousPreOrder(doc) != null && nextNode != null)
         Assert.assertEquals(curNode, nextNode.previousPreOrder(doc));

     if (curNode.getNodeType() == NodeType.SHAPE && ((Shape) curNode).hasImage())
         curNode.remove();

     curNode = nextNode;
 }

 shapes = (ArrayList) IterableUtils.toList(doc.getChildNodes(NodeType.SHAPE, true));

 Assert.assertEquals(0, IterableUtils.countMatches(shapes, s -> {
     try {
         return s.hasImage();
     } catch (Exception e) {
         e.printStackTrace();
     }
     return false;
 }));
 
```
### remove() {#remove}
```
public void remove()
```


Removes itself from the parent.

 **Examples:** 

Shows how to remove all child nodes of a specific type from a composite node.

```

 Document doc = new Document(getMyDir() + "Tables.docx");

 Assert.assertEquals(2, doc.getChildNodes(NodeType.TABLE, true).getCount());

 Node curNode = doc.getFirstSection().getBody().getFirstChild();

 while (curNode != null) {
     // Save the next sibling node as a variable in case we want to move to it after deleting this node.
     Node nextNode = curNode.getNextSibling();

     // A section body can contain Paragraph and Table nodes.
     // If the node is a Table, remove it from the parent.
     if (curNode.getNodeType() == NodeType.TABLE) {
         curNode.remove();
     }

     curNode = nextNode;
 }

 Assert.assertEquals(0, doc.getChildNodes(NodeType.TABLE, true).getCount());
 
```

Shows how to delete all shapes with images from a document.

```

 Document doc = new Document(getMyDir() + "Images.docx");
 ArrayList shapes = (ArrayList) IterableUtils.toList(doc.getChildNodes(NodeType.SHAPE, true));

 Assert.assertEquals(9, IterableUtils.countMatches(shapes, s -> {
     try {
         return s.hasImage();
     } catch (Exception e) {
         e.printStackTrace();
     }
     return false;
 }));

 for (Shape shape : shapes)
     if (shape.hasImage())
         shape.remove();

 shapes = (ArrayList) IterableUtils.toList(doc.getChildNodes(NodeType.SHAPE, true));

 Assert.assertEquals(0, IterableUtils.countMatches(shapes, s -> {
     try {
         return s.hasImage();
     } catch (Exception e) {
         e.printStackTrace();
     }
     return false;
 }));
 
```

### removeAllChildren() {#removeAllChildren}
```
public void removeAllChildren()
```


Removes all the child nodes of the current node.

 **Examples:** 

Shows how to construct an Aspose.Words document by hand.

```

 Document doc = new Document();

 // A blank document contains one section, one body and one paragraph.
 // Call the "RemoveAllChildren" method to remove all those nodes,
 // and end up with a document node with no children.
 doc.removeAllChildren();

 // This document now has no composite child nodes that we can add content to.
 // If we wish to edit it, we will need to repopulate its node collection.
 // First, create a new section, and then append it as a child to the root document node.
 Section section = new Section(doc);
 doc.appendChild(section);

 // Set some page setup properties for the section.
 section.getPageSetup().setSectionStart(SectionStart.NEW_PAGE);
 section.getPageSetup().setPaperSize(PaperSize.LETTER);

 // A section needs a body, which will contain and display all its contents
 // on the page between the section's header and footer.
 Body body = new Body(doc);
 section.appendChild(body);

 // Create a paragraph, set some formatting properties, and then append it as a child to the body.
 Paragraph para = new Paragraph(doc);

 para.getParagraphFormat().setStyleName("Heading 1");
 para.getParagraphFormat().setAlignment(ParagraphAlignment.CENTER);

 body.appendChild(para);

 // Finally, add some content to do the document. Create a run,
 // set its appearance and contents, and then append it as a child to the paragraph.
 Run run = new Run(doc);
 run.setText("Hello World!");
 run.getFont().setColor(Color.RED);
 para.appendChild(run);

 Assert.assertEquals("Hello World!", doc.getText().trim());

 doc.save(getArtifactsDir() + "Section.CreateManually.docx");
 
```

### removeChild(Node oldChild) {#removeChild-com.aspose.words.Node}
```
public Node removeChild(Node oldChild)
```


Removes the specified child node.

 **Remarks:** 

The parent of  oldChild  is set to  null  after the node is removed.

**Parameters:**
| Parameter | Type | Description |
| --- | --- | --- |
| oldChild | [Node](../../com.aspose.words/node/) | The node to remove. |

**Returns:**
[Node](../../com.aspose.words/node/) - The removed node.

 **Examples:** 

Shows how to use of methods of Node and CompositeNode to remove a section before the last section in the document.

```

 Document doc = new Document();
 DocumentBuilder builder = new DocumentBuilder(doc);

 builder.writeln("Section 1 text.");
 builder.insertBreak(BreakType.SECTION_BREAK_CONTINUOUS);
 builder.writeln("Section 2 text.");

 // Both sections are siblings of each other.
 Section lastSection = (Section) doc.getLastChild();
 Section firstSection = (Section) lastSection.getPreviousSibling();

 // Remove a section based on its sibling relationship with another section.
 if (lastSection.getPreviousSibling() != null)
     doc.removeChild(firstSection);

 // The section we removed was the first one, leaving the document with only the second.
 Assert.assertEquals("Section 2 text.", doc.getText().trim());
 
```
### removeSmartTags() {#removeSmartTags}
```
public void removeSmartTags()
```


Removes all [SmartTag](../../com.aspose.words/smarttag/) descendant nodes of the current node.

 **Remarks:** 

This method does not remove the content of the smart tags.

 **Examples:** 

Removes all smart tags from descendant nodes of a composite node.

```

 Document doc = new Document(getMyDir() + "Smart tags.doc");

 Assert.assertEquals(8, doc.getChildNodes(NodeType.SMART_TAG, true).getCount());

 doc.removeSmartTags();

 Assert.assertEquals(0, doc.getChildNodes(NodeType.SMART_TAG, true).getCount());
 
```

Shows how to create smart tags.

```

 public void create() throws Exception {
     Document doc = new Document();

     // A smart tag appears in a document with Microsoft Word recognizes a part of its text as some form of data,
     // such as a name, date, or address, and converts it to a hyperlink that displays a purple dotted underline.
     SmartTag smartTag = new SmartTag(doc);

     // Smart tags are composite nodes that contain their recognized text in its entirety.
     // Add contents to this smart tag manually.
     smartTag.appendChild(new Run(doc, "May 29, 2019"));

     // Microsoft Word may recognize the above contents as being a date.
     // Smart tags use the "Element" property to reflect the type of data they contain.
     smartTag.setElement("date");

     // Some smart tag types process their contents further into custom XML properties.
     smartTag.getProperties().add(new CustomXmlProperty("Day", "", "29"));
     smartTag.getProperties().add(new CustomXmlProperty("Month", "", "5"));
     smartTag.getProperties().add(new CustomXmlProperty("Year", "", "2019"));

     // Set the smart tag's URI to the default value.
     smartTag.setUri("urn:schemas-microsoft-com:office:smarttags");

     doc.getFirstSection().getBody().getFirstParagraph().appendChild(smartTag);
     doc.getFirstSection().getBody().getFirstParagraph().appendChild(new Run(doc, " is a date. "));

     // Create another smart tag for a stock ticker.
     smartTag = new SmartTag(doc);
     smartTag.setElement("stockticker");
     smartTag.setUri("urn:schemas-microsoft-com:office:smarttags");

     smartTag.appendChild(new Run(doc, "MSFT"));

     doc.getFirstSection().getBody().getFirstParagraph().appendChild(smartTag);
     doc.getFirstSection().getBody().getFirstParagraph().appendChild(new Run(doc, " is a stock ticker."));

     // Print all the smart tags in our document using a document visitor.
     doc.accept(new SmartTagPrinter());

     // Older versions of Microsoft Word support smart tags.
     doc.save(getArtifactsDir() + "SmartTag.Create.doc");

     // Use the "RemoveSmartTags" method to remove all smart tags from a document.
     Assert.assertEquals(2, doc.getChildNodes(NodeType.SMART_TAG, true).getCount());

     doc.removeSmartTags();

     Assert.assertEquals(0, doc.getChildNodes(NodeType.SMART_TAG, true).getCount());
 }

 /// 
 /// Prints visited smart tags and their contents.
 /// 
 private static class SmartTagPrinter extends DocumentVisitor {
     /// 
     /// Called when a SmartTag node is encountered in the document.
     /// 
     public int visitSmartTagStart(SmartTag smartTag) {
         System.out.println("Smart tag type: {smartTag.Element}");
         return VisitorAction.CONTINUE;
     }

     /// 
     /// Called when the visiting of a SmartTag node is ended.
     /// 
     public int visitSmartTagEnd(SmartTag smartTag) {
         System.out.println("\tContents: \"{smartTag.ToString(SaveFormat.Text)}\"");

         if (smartTag.getProperties().getCount() == 0) {
             System.out.println("\tContains no properties");
         } else {
             System.out.println("\tProperties: ");
             String[] properties = new String[smartTag.getProperties().getCount()];
             int index = 0;

             for (CustomXmlProperty cxp : smartTag.getProperties())
                 properties[index++] = MessageFormat.format("\"{0}\" = \"{1}\"", cxp.getName(), cxp.getValue());

             System.out.println(StringUtils.join(properties, ", "));
         }

         return VisitorAction.CONTINUE;
     }
 }
 
```

### selectNodes(String xpath) {#selectNodes-java.lang.String}
```
public NodeList selectNodes(String xpath)
```


Selects a list of nodes matching the XPath expression.

 **Remarks:** 

Only expressions with element names are supported at the moment. Expressions that use attribute names are not supported.

**Parameters:**
| Parameter | Type | Description |
| --- | --- | --- |
| xpath | java.lang.String | The XPath expression. |

**Returns:**
[NodeList](../../com.aspose.words/nodelist/) - A list of nodes matching the XPath query.

 **Examples:** 

Shows how to use an XPath expression to test whether a node is inside a field.

```

 Document doc = new Document(getMyDir() + "Mail merge destination - Northwind employees.docx");

 // The NodeList that results from this XPath expression will contain all nodes we find inside a field.
 // However, FieldStart and FieldEnd nodes can be on the list if there are nested fields in the path.
 // Currently does not find rare fields in which the FieldCode or FieldResult spans across multiple paragraphs.
 NodeList resultList =
         doc.selectNodes("//FieldStart/following-sibling::node()[following-sibling::FieldEnd]");

 // Check if the specified run is one of the nodes that are inside the field.
 System.out.println("Contents of the first Run node that's part of a field: {resultList.First(n => n.NodeType == NodeType.Run).GetText().Trim()}");
 
```

Shows how to select certain nodes by using an XPath expression.

```

 Document doc = new Document(getMyDir() + "Tables.docx");

 // This expression will extract all paragraph nodes,
 // which are descendants of any table node in the document.
 NodeList nodeList = doc.selectNodes("//Table//Paragraph");

 // Iterate through the list with an enumerator and print the contents of every paragraph in each cell of the table.
 int index = 0;

 Iterator e = nodeList.iterator();
 while (e.hasNext()) {
     Node currentNode = e.next();
     System.out.println(MessageFormat.format("Table paragraph index {0}, contents: \"{1}\"", index++, currentNode.getText().trim()));
 }

 // This expression will select any paragraphs that are direct children of any Body node in the document.
 nodeList = doc.selectNodes("//Body/Paragraph");

 // We can treat the list as an array.
 Assert.assertEquals(nodeList.toArray().length, 4);

 // Use SelectSingleNode to select the first result of the same expression as above.
 Node node = doc.selectSingleNode("//Body/Paragraph");

 Assert.assertEquals(Paragraph.class, node.getClass());
 
```
### selectSingleNode(String xpath) {#selectSingleNode-java.lang.String}
```
public Node selectSingleNode(String xpath)
```


Selects the first [Node](../../com.aspose.words/node/) that matches the XPath expression.

 **Remarks:** 

Only expressions with element names are supported at the moment. Expressions that use attribute names are not supported.

**Parameters:**
| Parameter | Type | Description |
| --- | --- | --- |
| xpath | java.lang.String | The XPath expression. |

**Returns:**
[Node](../../com.aspose.words/node/) - The first [Node](../../com.aspose.words/node/) that matches the XPath query or  null  if no matching node is found.

 **Examples:** 

Shows how to select certain nodes by using an XPath expression.

```

 Document doc = new Document(getMyDir() + "Tables.docx");

 // This expression will extract all paragraph nodes,
 // which are descendants of any table node in the document.
 NodeList nodeList = doc.selectNodes("//Table//Paragraph");

 // Iterate through the list with an enumerator and print the contents of every paragraph in each cell of the table.
 int index = 0;

 Iterator e = nodeList.iterator();
 while (e.hasNext()) {
     Node currentNode = e.next();
     System.out.println(MessageFormat.format("Table paragraph index {0}, contents: \"{1}\"", index++, currentNode.getText().trim()));
 }

 // This expression will select any paragraphs that are direct children of any Body node in the document.
 nodeList = doc.selectNodes("//Body/Paragraph");

 // We can treat the list as an array.
 Assert.assertEquals(nodeList.toArray().length, 4);

 // Use SelectSingleNode to select the first result of the same expression as above.
 Node node = doc.selectSingleNode("//Body/Paragraph");

 Assert.assertEquals(Paragraph.class, node.getClass());
 
```
### setAbsoluteHorizontalDistance(double value) {#setAbsoluteHorizontalDistance-double}
```
public void setAbsoluteHorizontalDistance(double value)
```


Sets absolute horizontal floating table position specified by the table properties, in points. Default value is 0.

 **Examples:** 

Shows how set the location of floating tables.

```

 Document doc = new Document();
 DocumentBuilder builder = new DocumentBuilder(doc);

 Table table = builder.startTable();
 builder.insertCell();
 builder.write("Table 1, cell 1");
 builder.endTable();
 table.setPreferredWidth(PreferredWidth.fromPoints(300.0));

 // Set the table's location to a place on the page, such as, in this case, the bottom right corner.
 table.setRelativeVerticalAlignment(VerticalAlignment.BOTTOM);
 table.setRelativeHorizontalAlignment(HorizontalAlignment.RIGHT);

 table = builder.startTable();
 builder.insertCell();
 builder.write("Table 2, cell 1");
 builder.endTable();
 table.setPreferredWidth(PreferredWidth.fromPoints(300.0));

 // We can also set a horizontal and vertical offset in points from the paragraph's location where we inserted the table.
 table.setAbsoluteVerticalDistance(50.0);
 table.setAbsoluteHorizontalDistance(100.0);

 doc.save(getArtifactsDir() + "Table.ChangeFloatingTableProperties.docx");
 
```

**Parameters:**
| Parameter | Type | Description |
| --- | --- | --- |
| value | double | Absolute horizontal floating table position specified by the table properties, in points. |

### setAbsoluteVerticalDistance(double value) {#setAbsoluteVerticalDistance-double}
```
public void setAbsoluteVerticalDistance(double value)
```


Sets absolute vertical floating table position specified by the table properties, in points. Default value is 0.

 **Examples:** 

Shows how set the location of floating tables.

```

 Document doc = new Document();
 DocumentBuilder builder = new DocumentBuilder(doc);

 Table table = builder.startTable();
 builder.insertCell();
 builder.write("Table 1, cell 1");
 builder.endTable();
 table.setPreferredWidth(PreferredWidth.fromPoints(300.0));

 // Set the table's location to a place on the page, such as, in this case, the bottom right corner.
 table.setRelativeVerticalAlignment(VerticalAlignment.BOTTOM);
 table.setRelativeHorizontalAlignment(HorizontalAlignment.RIGHT);

 table = builder.startTable();
 builder.insertCell();
 builder.write("Table 2, cell 1");
 builder.endTable();
 table.setPreferredWidth(PreferredWidth.fromPoints(300.0));

 // We can also set a horizontal and vertical offset in points from the paragraph's location where we inserted the table.
 table.setAbsoluteVerticalDistance(50.0);
 table.setAbsoluteHorizontalDistance(100.0);

 doc.save(getArtifactsDir() + "Table.ChangeFloatingTableProperties.docx");
 
```

**Parameters:**
| Parameter | Type | Description |
| --- | --- | --- |
| value | double | Absolute vertical floating table position specified by the table properties, in points. |

### setAlignment(int value) {#setAlignment-int}
```
public void setAlignment(int value)
```


Specifies how an inline table is aligned in the document.

 **Remarks:** 

The default value is [TableAlignment.LEFT](../../com.aspose.words/tablealignment/\#LEFT).

 **Examples:** 

Shows how to apply an outline border to a table.

```

 Document doc = new Document(getMyDir() + "Tables.docx");
 Table table = doc.getFirstSection().getBody().getTables().get(0);

 // Align the table to the center of the page.
 table.setAlignment(TableAlignment.CENTER);

 // Clear any existing borders and shading from the table.
 table.clearBorders();
 table.clearShading();

 // Add green borders to the outline of the table.
 table.setBorder(BorderType.LEFT, LineStyle.SINGLE, 1.5, Color.GREEN, true);
 table.setBorder(BorderType.RIGHT, LineStyle.SINGLE, 1.5, Color.GREEN, true);
 table.setBorder(BorderType.TOP, LineStyle.SINGLE, 1.5, Color.GREEN, true);
 table.setBorder(BorderType.BOTTOM, LineStyle.SINGLE, 1.5, Color.GREEN, true);

 // Fill the cells with a light green solid color.
 table.setShading(TextureIndex.TEXTURE_SOLID, Color.GREEN, Color.GREEN);

 doc.save(getArtifactsDir() + "Table.SetOutlineBorders.docx");
 
```

**Parameters:**
| Parameter | Type | Description |
| --- | --- | --- |
| value | int | The corresponding  int  value. The value must be one of [TableAlignment](../../com.aspose.words/tablealignment/) constants. |

### setAllowAutoFit(boolean value) {#setAllowAutoFit-boolean}
```
public void setAllowAutoFit(boolean value)
```


Allows Microsoft Word and Aspose.Words to automatically resize cells in a table to fit their contents.

 **Remarks:** 

The default value is  true .

 **Examples:** 

Shows how to enable/disable automatic table cell resizing.

```

 Document doc = new Document();
 DocumentBuilder builder = new DocumentBuilder(doc);

 Table table = builder.startTable();
 builder.insertCell();
 builder.getCellFormat().setPreferredWidth(PreferredWidth.fromPoints(100.0));
 builder.write("Lorem ipsum dolor sit amet, consectetur adipiscing elit, " +
         "sed do eiusmod tempor incididunt ut labore et dolore magna aliqua.");

 builder.insertCell();
 builder.getCellFormat().setPreferredWidth(PreferredWidth.AUTO);
 builder.write("Lorem ipsum dolor sit amet, consectetur adipiscing elit, " +
         "sed do eiusmod tempor incididunt ut labore et dolore magna aliqua.");
 builder.endRow();
 builder.endTable();

 // Set the "AllowAutoFit" property to "false" to get the table to maintain the dimensions
 // of all its rows and cells, and truncate contents if they get too large to fit.
 // Set the "AllowAutoFit" property to "true" to allow the table to change its cells' width and height
 // to accommodate their contents.
 table.setAllowAutoFit(allowAutoFit);

 doc.save(getArtifactsDir() + "Table.AllowAutoFitOnTable.html");
 
```

**M:Aspose.Words.Tables.Table.AutoFit(Aspose.Words.Tables.AutoFitBehavior)**

**Parameters:**
| Parameter | Type | Description |
| --- | --- | --- |
| value | boolean | The corresponding  boolean  value. |

### setAllowCellSpacing(boolean value) {#setAllowCellSpacing-boolean}
```
public void setAllowCellSpacing(boolean value)
```


Sets the "Allow spacing between cells" option.

 **Examples:** 

Shows how to enable spacing between individual cells in a table.

```

 Document doc = new Document();
 DocumentBuilder builder = new DocumentBuilder(doc);

 Table table = builder.startTable();
 builder.insertCell();
 builder.write("Animal");
 builder.insertCell();
 builder.write("Class");
 builder.endRow();
 builder.insertCell();
 builder.write("Dog");
 builder.insertCell();
 builder.write("Mammal");
 builder.endTable();

 table.setCellSpacing(3.0);

 // Set the "AllowCellSpacing" property to "true" to enable spacing between cells
 // with a magnitude equal to the value of the "CellSpacing" property, in points.
 // Set the "AllowCellSpacing" property to "false" to disable cell spacing
 // and ignore the value of the "CellSpacing" property.
 table.setAllowCellSpacing(allowCellSpacing);

 doc.save(getArtifactsDir() + "Table.AllowCellSpacing.html");

 // Adjusting the "CellSpacing" property will automatically enable cell spacing.
 table.setCellSpacing(5.0);

 Assert.assertTrue(table.getAllowCellSpacing());
 
```

**Parameters:**
| Parameter | Type | Description |
| --- | --- | --- |
| value | boolean | The "Allow spacing between cells" option. |

### setBidi(boolean value) {#setBidi-boolean}
```
public void setBidi(boolean value)
```


Sets whether this is a right-to-left table.

 **Remarks:** 

When  true , the cells in this row are laid out right to left.

The default value is  false .

 **Examples:** 

Shows how to create custom style settings for the table.

```

 Document doc = new Document();
 DocumentBuilder builder = new DocumentBuilder(doc);

 Table table = builder.startTable();
 builder.insertCell();
 builder.write("Name");
 builder.insertCell();
 builder.write("\u0645\u0631\u062d\u0628\u064b\u0627");
 builder.endRow();
 builder.insertCell();
 builder.insertCell();
 builder.endTable();

 TableStyle tableStyle = (TableStyle) doc.getStyles().add(StyleType.TABLE, "MyTableStyle1");
 tableStyle.setAllowBreakAcrossPages(true);
 tableStyle.setBidi(true);
 tableStyle.setCellSpacing(5.0);
 tableStyle.setBottomPadding(20.0);
 tableStyle.setLeftPadding(5.0);
 tableStyle.setRightPadding(10.0);
 tableStyle.setTopPadding(20.0);
 tableStyle.getShading().setBackgroundPatternColor(Color.WHITE);
 tableStyle.getBorders().setColor(Color.BLACK);
 tableStyle.getBorders().setLineStyle(LineStyle.DOT_DASH);
 tableStyle.setVerticalAlignment(CellVerticalAlignment.CENTER);

 table.setStyle(tableStyle);

 // Setting the style properties of a table may affect the properties of the table itself.
 Assert.assertTrue(table.getBidi());
 Assert.assertEquals(5.0d, table.getCellSpacing());
 Assert.assertEquals("MyTableStyle1", table.getStyleName());

 doc.save(getArtifactsDir() + "Table.TableStyleCreation.docx");
 
```

**Parameters:**
| Parameter | Type | Description |
| --- | --- | --- |
| value | boolean | Whether this is a right-to-left table. |

### setBorder(int borderType, int lineStyle, double lineWidth, Color color, boolean isOverrideCellBorders) {#setBorder-int-int-double-java.awt.Color-boolean}
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

### setBorders(int lineStyle, double lineWidth, Color color) {#setBorders-int-double-java.awt.Color}
```
public void setBorders(int lineStyle, double lineWidth, Color color)
```




**Parameters:**
| Parameter | Type | Description |
| --- | --- | --- |
| lineStyle | int |  |
| lineWidth | double |  |
| color | java.awt.Color |  |

### setBottomPadding(double value) {#setBottomPadding-double}
```
public void setBottomPadding(double value)
```


Sets the amount of space (in points) to add below the contents of cells.

 **Examples:** 

Shows how to configure content padding in a table.

```

 Document doc = new Document();
 DocumentBuilder builder = new DocumentBuilder(doc);

 Table table = builder.startTable();
 builder.insertCell();
 builder.write("Row 1, cell 1.");
 builder.insertCell();
 builder.write("Row 1, cell 2.");
 builder.endTable();

 // For every cell in the table, set the distance between its contents and each of its borders.
 // This table will maintain the minimum padding distance by wrapping text.
 table.setLeftPadding(30.0);
 table.setRightPadding(60.0);
 table.setTopPadding(10.0);
 table.setBottomPadding(90.0);
 table.setPreferredWidth(PreferredWidth.fromPoints(250.0));

 doc.save(getArtifactsDir() + "DocumentBuilder.SetRowFormatting.docx");
 
```

**Parameters:**
| Parameter | Type | Description |
| --- | --- | --- |
| value | double | The amount of space (in points) to add below the contents of cells. |

### setCellSpacing(double value) {#setCellSpacing-double}
```
public void setCellSpacing(double value)
```


Sets the amount of space (in points) between the cells.

 **Examples:** 

Shows how to enable spacing between individual cells in a table.

```

 Document doc = new Document();
 DocumentBuilder builder = new DocumentBuilder(doc);

 Table table = builder.startTable();
 builder.insertCell();
 builder.write("Animal");
 builder.insertCell();
 builder.write("Class");
 builder.endRow();
 builder.insertCell();
 builder.write("Dog");
 builder.insertCell();
 builder.write("Mammal");
 builder.endTable();

 table.setCellSpacing(3.0);

 // Set the "AllowCellSpacing" property to "true" to enable spacing between cells
 // with a magnitude equal to the value of the "CellSpacing" property, in points.
 // Set the "AllowCellSpacing" property to "false" to disable cell spacing
 // and ignore the value of the "CellSpacing" property.
 table.setAllowCellSpacing(allowCellSpacing);

 doc.save(getArtifactsDir() + "Table.AllowCellSpacing.html");

 // Adjusting the "CellSpacing" property will automatically enable cell spacing.
 table.setCellSpacing(5.0);

 Assert.assertTrue(table.getAllowCellSpacing());
 
```

Shows how to create custom style settings for the table.

```

 Document doc = new Document();
 DocumentBuilder builder = new DocumentBuilder(doc);

 Table table = builder.startTable();
 builder.insertCell();
 builder.write("Name");
 builder.insertCell();
 builder.write("\u0645\u0631\u062d\u0628\u064b\u0627");
 builder.endRow();
 builder.insertCell();
 builder.insertCell();
 builder.endTable();

 TableStyle tableStyle = (TableStyle) doc.getStyles().add(StyleType.TABLE, "MyTableStyle1");
 tableStyle.setAllowBreakAcrossPages(true);
 tableStyle.setBidi(true);
 tableStyle.setCellSpacing(5.0);
 tableStyle.setBottomPadding(20.0);
 tableStyle.setLeftPadding(5.0);
 tableStyle.setRightPadding(10.0);
 tableStyle.setTopPadding(20.0);
 tableStyle.getShading().setBackgroundPatternColor(Color.WHITE);
 tableStyle.getBorders().setColor(Color.BLACK);
 tableStyle.getBorders().setLineStyle(LineStyle.DOT_DASH);
 tableStyle.setVerticalAlignment(CellVerticalAlignment.CENTER);

 table.setStyle(tableStyle);

 // Setting the style properties of a table may affect the properties of the table itself.
 Assert.assertTrue(table.getBidi());
 Assert.assertEquals(5.0d, table.getCellSpacing());
 Assert.assertEquals("MyTableStyle1", table.getStyleName());

 doc.save(getArtifactsDir() + "Table.TableStyleCreation.docx");
 
```

**Parameters:**
| Parameter | Type | Description |
| --- | --- | --- |
| value | double | The amount of space (in points) between the cells. |

### setCustomNodeId(int value) {#setCustomNodeId-int}
```
public void setCustomNodeId(int value)
```


Specifies custom node identifier.

 **Remarks:** 

Default is zero.

This identifier can be set and used arbitrarily. For example, as a key to get external data.

Important note, specified value is not saved to an output file and exists only during the node lifetime.

 **Examples:** 

Shows how to traverse through a composite node's collection of child nodes.

```

 Document doc = new Document();

 // Add two runs and one shape as child nodes to the first paragraph of this document.
 Paragraph paragraph = (Paragraph) doc.getChild(NodeType.PARAGRAPH, 0, true);
 paragraph.appendChild(new Run(doc, "Hello world! "));

 Shape shape = new Shape(doc, ShapeType.RECTANGLE);
 shape.setWidth(200.0);
 shape.setHeight(200.0);
 // Note that the 'CustomNodeId' is not saved to an output file and exists only during the node lifetime.
 shape.setCustomNodeId(100);
 shape.setWrapType(WrapType.INLINE);
 paragraph.appendChild(shape);

 paragraph.appendChild(new Run(doc, "Hello again!"));

 // Iterate through the paragraph's collection of immediate children,
 // and print any runs or shapes that we find within.
 NodeCollection children = paragraph.getChildNodes();

 Assert.assertEquals(3, paragraph.getChildNodes().getCount());

 for (Node child : (Iterable) children)
     switch (child.getNodeType()) {
         case NodeType.RUN:
             System.out.println("Run contents:");
             System.out.println("\t\"{child.GetText().Trim()}\"");
             break;
         case NodeType.SHAPE:
             Shape childShape = (Shape) child;
             System.out.println("Shape:");
             System.out.println("\t{childShape.ShapeType}, {childShape.Width}x{childShape.Height}");
             break;
     }
 
```

**Parameters:**
| Parameter | Type | Description |
| --- | --- | --- |
| value | int | The corresponding  int  value. |

### setDescription(String value) {#setDescription-java.lang.String}
```
public void setDescription(String value)
```


Sets description of this table. It provides an alternative text representation of the information contained in the table.

 **Remarks:** 

The default value is an empty string.

This property is meaningful for ISO/IEC 29500 compliant DOCX documents ( [OoxmlCompliance](../../com.aspose.words/ooxmlcompliance/)). When saved to pre-ISO/IEC 29500 formats, the property is ignored.

 **Examples:** 

Shows how to build a nested table without using a document builder.

```

 public void createNestedTable() throws Exception {
     Document doc = new Document();

     // Create the outer table with three rows and four columns, and then add it to the document.
     Table outerTable = createTable(doc, 3, 4, "Outer Table");
     doc.getFirstSection().getBody().appendChild(outerTable);

     // Create another table with two rows and two columns and then insert it into the first table's first cell.
     Table innerTable = createTable(doc, 2, 2, "Inner Table");
     outerTable.getFirstRow().getFirstCell().appendChild(innerTable);

     doc.save(getArtifactsDir() + "Table.CreateNestedTable.docx");
 }

 // Creates a new table in the document with the given dimensions and text in each cell.
 private Table createTable(final Document doc, final int rowCount, final int cellCount, final String cellText) throws Exception {
     Table table = new Table(doc);

     for (int rowId = 1; rowId <= rowCount; rowId++) {
         Row row = new Row(doc);
         table.appendChild(row);

         for (int cellId = 1; cellId <= cellCount; cellId++) {
             Cell cell = new Cell(doc);
             cell.appendChild(new Paragraph(doc));
             cell.getFirstParagraph().appendChild(new Run(doc, cellText));

             row.appendChild(cell);
         }
     }

     // You can use the "Title" and "Description" properties to add a title and description respectively to your table.
     // The table must have at least one row before we can use these properties.
     // These properties are meaningful for ISO / IEC 29500 compliant .docx documents (see the OoxmlCompliance class).
     // If we save the document to pre-ISO/IEC 29500 formats, Microsoft Word ignores these properties.
     table.setTitle("Aspose table title");
     table.setDescription("Aspose table description");

     return table;
 }
 
```

**Parameters:**
| Parameter | Type | Description |
| --- | --- | --- |
| value | java.lang.String | Description of this table. |

### setDistanceBottom(double value) {#setDistanceBottom-double}
```
public void setDistanceBottom(double value)
```


Sets distance between table bottom and the surrounding text, in points.

 **Examples:** 

Shows the minimum distance operations between table boundaries and text.

```

 Document doc = new Document(getMyDir() + "Table wrapped by text.docx");

 Table table = (Table) doc.getChild(NodeType.TABLE, 0, true);

 Assert.assertEquals(table.getDistanceTop(), 25.9d);
 Assert.assertEquals(table.getDistanceBottom(), 25.9d);
 Assert.assertEquals(table.getDistanceLeft(), 17.3d);
 Assert.assertEquals(table.getDistanceRight(), 17.3d);
 
```

**Parameters:**
| Parameter | Type | Description |
| --- | --- | --- |
| value | double | Distance between table bottom and the surrounding text, in points. |

### setDistanceLeft(double value) {#setDistanceLeft-double}
```
public void setDistanceLeft(double value)
```


Sets distance between table left and the surrounding text, in points.

 **Examples:** 

Shows the minimum distance operations between table boundaries and text.

```

 Document doc = new Document(getMyDir() + "Table wrapped by text.docx");

 Table table = (Table) doc.getChild(NodeType.TABLE, 0, true);

 Assert.assertEquals(table.getDistanceTop(), 25.9d);
 Assert.assertEquals(table.getDistanceBottom(), 25.9d);
 Assert.assertEquals(table.getDistanceLeft(), 17.3d);
 Assert.assertEquals(table.getDistanceRight(), 17.3d);
 
```

**Parameters:**
| Parameter | Type | Description |
| --- | --- | --- |
| value | double | Distance between table left and the surrounding text, in points. |

### setDistanceRight(double value) {#setDistanceRight-double}
```
public void setDistanceRight(double value)
```


Sets distance between table right and the surrounding text, in points.

 **Examples:** 

Shows the minimum distance operations between table boundaries and text.

```

 Document doc = new Document(getMyDir() + "Table wrapped by text.docx");

 Table table = (Table) doc.getChild(NodeType.TABLE, 0, true);

 Assert.assertEquals(table.getDistanceTop(), 25.9d);
 Assert.assertEquals(table.getDistanceBottom(), 25.9d);
 Assert.assertEquals(table.getDistanceLeft(), 17.3d);
 Assert.assertEquals(table.getDistanceRight(), 17.3d);
 
```

**Parameters:**
| Parameter | Type | Description |
| --- | --- | --- |
| value | double | Distance between table right and the surrounding text, in points. |

### setDistanceTop(double value) {#setDistanceTop-double}
```
public void setDistanceTop(double value)
```


Sets distance between table top and the surrounding text, in points.

 **Examples:** 

Shows the minimum distance operations between table boundaries and text.

```

 Document doc = new Document(getMyDir() + "Table wrapped by text.docx");

 Table table = (Table) doc.getChild(NodeType.TABLE, 0, true);

 Assert.assertEquals(table.getDistanceTop(), 25.9d);
 Assert.assertEquals(table.getDistanceBottom(), 25.9d);
 Assert.assertEquals(table.getDistanceLeft(), 17.3d);
 Assert.assertEquals(table.getDistanceRight(), 17.3d);
 
```

**Parameters:**
| Parameter | Type | Description |
| --- | --- | --- |
| value | double | Distance between table top and the surrounding text, in points. |

### setHorizontalAnchor(int value) {#setHorizontalAnchor-int}
```
public void setHorizontalAnchor(int value)
```


Gets the base object from which the horizontal positioning of floating table should be calculated. Default value is [RelativeHorizontalPosition.COLUMN](../../com.aspose.words/relativehorizontalposition/\#COLUMN).

 **Examples:** 

Shows how to work with floating tables properties.

```

 Document doc = new Document(getMyDir() + "Table wrapped by text.docx");

 Table table = doc.getFirstSection().getBody().getTables().get(0);

 if (table.getTextWrapping() == TextWrapping.AROUND) {
     Assert.assertEquals(RelativeHorizontalPosition.MARGIN, table.getHorizontalAnchor());
     Assert.assertEquals(RelativeVerticalPosition.PARAGRAPH, table.getVerticalAnchor());
     Assert.assertEquals(false, table.getAllowOverlap());

     // Only Margin, Page, Column available in RelativeHorizontalPosition for HorizontalAnchor setter.
     // The ArgumentException will be thrown for any other values.
     table.setHorizontalAnchor(RelativeHorizontalPosition.COLUMN);

     // Only Margin, Page, Paragraph available in RelativeVerticalPosition for VerticalAnchor setter.
     // The ArgumentException will be thrown for any other values.
     table.setVerticalAnchor(RelativeVerticalPosition.PAGE);
 }
 
```

**Parameters:**
| Parameter | Type | Description |
| --- | --- | --- |
| value | int | The base object from which the horizontal positioning of floating table should be calculated. The value must be one of [RelativeHorizontalPosition](../../com.aspose.words/relativehorizontalposition/) constants. |

### setLeftIndent(double value) {#setLeftIndent-double}
```
public void setLeftIndent(double value)
```


Sets the value that represents the left indent of the table.

 **Examples:** 

Shows how to create a formatted table using DocumentBuilder.

```

 Document doc = new Document();
 DocumentBuilder builder = new DocumentBuilder(doc);

 Table table = builder.startTable();
 builder.insertCell();
 table.setLeftIndent(20.0);

 // Set some formatting options for text and table appearance.
 builder.getRowFormat().setHeight(40.0);
 builder.getRowFormat().setHeightRule(HeightRule.AT_LEAST);
 builder.getCellFormat().getShading().setBackgroundPatternColor(new Color((198), (217), (241)));

 builder.getParagraphFormat().setAlignment(ParagraphAlignment.CENTER);
 builder.getFont().setSize(16.0);
 builder.getFont().setName("Arial");
 builder.getFont().setBold(true);

 // Configuring the formatting options in a document builder will apply them
 // to the current cell/row its cursor is in,
 // as well as any new cells and rows created using that builder.
 builder.write("Header Row,\n Cell 1");
 builder.insertCell();
 builder.write("Header Row,\n Cell 2");
 builder.insertCell();
 builder.write("Header Row,\n Cell 3");
 builder.endRow();

 // Reconfigure the builder's formatting objects for new rows and cells that we are about to make.
 // The builder will not apply these to the first row already created so that it will stand out as a header row.
 builder.getCellFormat().getShading().setBackgroundPatternColor(Color.WHITE);
 builder.getCellFormat().setVerticalAlignment(CellVerticalAlignment.CENTER);
 builder.getRowFormat().setHeight(30.0);
 builder.getRowFormat().setHeightRule(HeightRule.AUTO);
 builder.insertCell();
 builder.getFont().setSize(12.0);
 builder.getFont().setBold(false);

 builder.write("Row 1, Cell 1.");
 builder.insertCell();
 builder.write("Row 1, Cell 2.");
 builder.insertCell();
 builder.write("Row 1, Cell 3.");
 builder.endRow();
 builder.insertCell();
 builder.write("Row 2, Cell 1.");
 builder.insertCell();
 builder.write("Row 2, Cell 2.");
 builder.insertCell();
 builder.write("Row 2, Cell 3.");
 builder.endRow();
 builder.endTable();

 doc.save(getArtifactsDir() + "DocumentBuilder.CreateFormattedTable.docx");
 
```

**Parameters:**
| Parameter | Type | Description |
| --- | --- | --- |
| value | double | The value that represents the left indent of the table. |

### setLeftPadding(double value) {#setLeftPadding-double}
```
public void setLeftPadding(double value)
```


Sets the amount of space (in points) to add to the left of the contents of cells.

 **Examples:** 

Shows how to configure content padding in a table.

```

 Document doc = new Document();
 DocumentBuilder builder = new DocumentBuilder(doc);

 Table table = builder.startTable();
 builder.insertCell();
 builder.write("Row 1, cell 1.");
 builder.insertCell();
 builder.write("Row 1, cell 2.");
 builder.endTable();

 // For every cell in the table, set the distance between its contents and each of its borders.
 // This table will maintain the minimum padding distance by wrapping text.
 table.setLeftPadding(30.0);
 table.setRightPadding(60.0);
 table.setTopPadding(10.0);
 table.setBottomPadding(90.0);
 table.setPreferredWidth(PreferredWidth.fromPoints(250.0));

 doc.save(getArtifactsDir() + "DocumentBuilder.SetRowFormatting.docx");
 
```

**Parameters:**
| Parameter | Type | Description |
| --- | --- | --- |
| value | double | The amount of space (in points) to add to the left of the contents of cells. |

### setPreferredWidth(PreferredWidth value) {#setPreferredWidth-com.aspose.words.PreferredWidth}
```
public void setPreferredWidth(PreferredWidth value)
```


Sets the table preferred width.

 **Remarks:** 

The default value is [PreferredWidth.AUTO](../../com.aspose.words/preferredwidth/\#AUTO).

 **Examples:** 

Shows how to set a table to auto fit to 50% of the width of the page.

```

 Document doc = new Document();
 DocumentBuilder builder = new DocumentBuilder(doc);

 Table table = builder.startTable();
 builder.insertCell();
 builder.write("Cell #1");
 builder.insertCell();
 builder.write("Cell #2");
 builder.insertCell();
 builder.write("Cell #3");

 table.setPreferredWidth(PreferredWidth.fromPercent(50.0));

 doc.save(getArtifactsDir() + "DocumentBuilder.InsertTableWithPreferredWidth.docx");
 
```

**Parameters:**
| Parameter | Type | Description |
| --- | --- | --- |
| value | [PreferredWidth](../../com.aspose.words/preferredwidth/) | The table preferred width. |

### setRelativeHorizontalAlignment(int value) {#setRelativeHorizontalAlignment-int}
```
public void setRelativeHorizontalAlignment(int value)
```


Sets floating table relative horizontal alignment.

 **Examples:** 

Shows how set the location of floating tables.

```

 Document doc = new Document();
 DocumentBuilder builder = new DocumentBuilder(doc);

 Table table = builder.startTable();
 builder.insertCell();
 builder.write("Table 1, cell 1");
 builder.endTable();
 table.setPreferredWidth(PreferredWidth.fromPoints(300.0));

 // Set the table's location to a place on the page, such as, in this case, the bottom right corner.
 table.setRelativeVerticalAlignment(VerticalAlignment.BOTTOM);
 table.setRelativeHorizontalAlignment(HorizontalAlignment.RIGHT);

 table = builder.startTable();
 builder.insertCell();
 builder.write("Table 2, cell 1");
 builder.endTable();
 table.setPreferredWidth(PreferredWidth.fromPoints(300.0));

 // We can also set a horizontal and vertical offset in points from the paragraph's location where we inserted the table.
 table.setAbsoluteVerticalDistance(50.0);
 table.setAbsoluteHorizontalDistance(100.0);

 doc.save(getArtifactsDir() + "Table.ChangeFloatingTableProperties.docx");
 
```

**Parameters:**
| Parameter | Type | Description |
| --- | --- | --- |
| value | int | Floating table relative horizontal alignment. The value must be one of [HorizontalAlignment](../../com.aspose.words/horizontalalignment/) constants. |

### setRelativeVerticalAlignment(int value) {#setRelativeVerticalAlignment-int}
```
public void setRelativeVerticalAlignment(int value)
```


Sets floating table relative vertical alignment.

 **Examples:** 

Shows how set the location of floating tables.

```

 Document doc = new Document();
 DocumentBuilder builder = new DocumentBuilder(doc);

 Table table = builder.startTable();
 builder.insertCell();
 builder.write("Table 1, cell 1");
 builder.endTable();
 table.setPreferredWidth(PreferredWidth.fromPoints(300.0));

 // Set the table's location to a place on the page, such as, in this case, the bottom right corner.
 table.setRelativeVerticalAlignment(VerticalAlignment.BOTTOM);
 table.setRelativeHorizontalAlignment(HorizontalAlignment.RIGHT);

 table = builder.startTable();
 builder.insertCell();
 builder.write("Table 2, cell 1");
 builder.endTable();
 table.setPreferredWidth(PreferredWidth.fromPoints(300.0));

 // We can also set a horizontal and vertical offset in points from the paragraph's location where we inserted the table.
 table.setAbsoluteVerticalDistance(50.0);
 table.setAbsoluteHorizontalDistance(100.0);

 doc.save(getArtifactsDir() + "Table.ChangeFloatingTableProperties.docx");
 
```

**Parameters:**
| Parameter | Type | Description |
| --- | --- | --- |
| value | int | Floating table relative vertical alignment. The value must be one of [VerticalAlignment](../../com.aspose.words/verticalalignment/) constants. |

### setRightPadding(double value) {#setRightPadding-double}
```
public void setRightPadding(double value)
```


Sets the amount of space (in points) to add to the right of the contents of cells.

 **Examples:** 

Shows how to configure content padding in a table.

```

 Document doc = new Document();
 DocumentBuilder builder = new DocumentBuilder(doc);

 Table table = builder.startTable();
 builder.insertCell();
 builder.write("Row 1, cell 1.");
 builder.insertCell();
 builder.write("Row 1, cell 2.");
 builder.endTable();

 // For every cell in the table, set the distance between its contents and each of its borders.
 // This table will maintain the minimum padding distance by wrapping text.
 table.setLeftPadding(30.0);
 table.setRightPadding(60.0);
 table.setTopPadding(10.0);
 table.setBottomPadding(90.0);
 table.setPreferredWidth(PreferredWidth.fromPoints(250.0));

 doc.save(getArtifactsDir() + "DocumentBuilder.SetRowFormatting.docx");
 
```

**Parameters:**
| Parameter | Type | Description |
| --- | --- | --- |
| value | double | The amount of space (in points) to add to the right of the contents of cells. |

### setShading(int texture, Color foregroundColor, Color backgroundColor) {#setShading-int-java.awt.Color-java.awt.Color}
```
public void setShading(int texture, Color foregroundColor, Color backgroundColor)
```




**Parameters:**
| Parameter | Type | Description |
| --- | --- | --- |
| texture | int |  |
| foregroundColor | java.awt.Color |  |
| backgroundColor | java.awt.Color |  |

### setStyle(Style value) {#setStyle-com.aspose.words.Style}
```
public void setStyle(Style value)
```


Sets the table style applied to this table.

 **Examples:** 

Shows how to create custom style settings for the table.

```

 Document doc = new Document();
 DocumentBuilder builder = new DocumentBuilder(doc);

 Table table = builder.startTable();
 builder.insertCell();
 builder.write("Name");
 builder.insertCell();
 builder.write("\u0645\u0631\u062d\u0628\u064b\u0627");
 builder.endRow();
 builder.insertCell();
 builder.insertCell();
 builder.endTable();

 TableStyle tableStyle = (TableStyle) doc.getStyles().add(StyleType.TABLE, "MyTableStyle1");
 tableStyle.setAllowBreakAcrossPages(true);
 tableStyle.setBidi(true);
 tableStyle.setCellSpacing(5.0);
 tableStyle.setBottomPadding(20.0);
 tableStyle.setLeftPadding(5.0);
 tableStyle.setRightPadding(10.0);
 tableStyle.setTopPadding(20.0);
 tableStyle.getShading().setBackgroundPatternColor(Color.WHITE);
 tableStyle.getBorders().setColor(Color.BLACK);
 tableStyle.getBorders().setLineStyle(LineStyle.DOT_DASH);
 tableStyle.setVerticalAlignment(CellVerticalAlignment.CENTER);

 table.setStyle(tableStyle);

 // Setting the style properties of a table may affect the properties of the table itself.
 Assert.assertTrue(table.getBidi());
 Assert.assertEquals(5.0d, table.getCellSpacing());
 Assert.assertEquals("MyTableStyle1", table.getStyleName());

 doc.save(getArtifactsDir() + "Table.TableStyleCreation.docx");
 
```

**Parameters:**
| Parameter | Type | Description |
| --- | --- | --- |
| value | [Style](../../com.aspose.words/style/) | The table style applied to this table. |

### setStyleIdentifier(int value) {#setStyleIdentifier-int}
```
public void setStyleIdentifier(int value)
```


Sets the locale independent style identifier of the table style applied to this table.

 **Examples:** 

Shows how to build a new table while applying a style.

```

 Document doc = new Document();
 DocumentBuilder builder = new DocumentBuilder(doc);
 Table table = builder.startTable();

 // We must insert at least one row before setting any table formatting.
 builder.insertCell();

 // Set the table style used based on the style identifier.
 // Note that not all table styles are available when saving to .doc format.
 table.setStyleIdentifier(StyleIdentifier.MEDIUM_SHADING_1_ACCENT_1);

 // Partially apply the style to features of the table based on predicates, then build the table.
 table.setStyleOptions(TableStyleOptions.FIRST_COLUMN | TableStyleOptions.ROW_BANDS | TableStyleOptions.FIRST_ROW);
 table.autoFit(AutoFitBehavior.AUTO_FIT_TO_CONTENTS);

 builder.writeln("Item");
 builder.getCellFormat().setRightPadding(40.0);
 builder.insertCell();
 builder.writeln("Quantity (kg)");
 builder.endRow();

 builder.insertCell();
 builder.writeln("Apples");
 builder.insertCell();
 builder.writeln("20");
 builder.endRow();

 builder.insertCell();
 builder.writeln("Bananas");
 builder.insertCell();
 builder.writeln("40");
 builder.endRow();

 builder.insertCell();
 builder.writeln("Carrots");
 builder.insertCell();
 builder.writeln("50");
 builder.endRow();

 doc.save(getArtifactsDir() + "DocumentBuilder.InsertTableWithStyle.docx");
 
```

**Parameters:**
| Parameter | Type | Description |
| --- | --- | --- |
| value | int | The locale independent style identifier of the table style applied to this table. The value must be one of [StyleIdentifier](../../com.aspose.words/styleidentifier/) constants. |

### setStyleName(String value) {#setStyleName-java.lang.String}
```
public void setStyleName(String value)
```


Sets the name of the table style applied to this table.

 **Examples:** 

Shows how to create custom style settings for the table.

```

 Document doc = new Document();
 DocumentBuilder builder = new DocumentBuilder(doc);

 Table table = builder.startTable();
 builder.insertCell();
 builder.write("Name");
 builder.insertCell();
 builder.write("\u0645\u0631\u062d\u0628\u064b\u0627");
 builder.endRow();
 builder.insertCell();
 builder.insertCell();
 builder.endTable();

 TableStyle tableStyle = (TableStyle) doc.getStyles().add(StyleType.TABLE, "MyTableStyle1");
 tableStyle.setAllowBreakAcrossPages(true);
 tableStyle.setBidi(true);
 tableStyle.setCellSpacing(5.0);
 tableStyle.setBottomPadding(20.0);
 tableStyle.setLeftPadding(5.0);
 tableStyle.setRightPadding(10.0);
 tableStyle.setTopPadding(20.0);
 tableStyle.getShading().setBackgroundPatternColor(Color.WHITE);
 tableStyle.getBorders().setColor(Color.BLACK);
 tableStyle.getBorders().setLineStyle(LineStyle.DOT_DASH);
 tableStyle.setVerticalAlignment(CellVerticalAlignment.CENTER);

 table.setStyle(tableStyle);

 // Setting the style properties of a table may affect the properties of the table itself.
 Assert.assertTrue(table.getBidi());
 Assert.assertEquals(5.0d, table.getCellSpacing());
 Assert.assertEquals("MyTableStyle1", table.getStyleName());

 doc.save(getArtifactsDir() + "Table.TableStyleCreation.docx");
 
```

**Parameters:**
| Parameter | Type | Description |
| --- | --- | --- |
| value | java.lang.String | The name of the table style applied to this table. |

### setStyleOptions(int value) {#setStyleOptions-int}
```
public void setStyleOptions(int value)
```


Sets bit flags that specify how a table style is applied to this table.

 **Examples:** 

Shows how to build a new table while applying a style.

```

 Document doc = new Document();
 DocumentBuilder builder = new DocumentBuilder(doc);
 Table table = builder.startTable();

 // We must insert at least one row before setting any table formatting.
 builder.insertCell();

 // Set the table style used based on the style identifier.
 // Note that not all table styles are available when saving to .doc format.
 table.setStyleIdentifier(StyleIdentifier.MEDIUM_SHADING_1_ACCENT_1);

 // Partially apply the style to features of the table based on predicates, then build the table.
 table.setStyleOptions(TableStyleOptions.FIRST_COLUMN | TableStyleOptions.ROW_BANDS | TableStyleOptions.FIRST_ROW);
 table.autoFit(AutoFitBehavior.AUTO_FIT_TO_CONTENTS);

 builder.writeln("Item");
 builder.getCellFormat().setRightPadding(40.0);
 builder.insertCell();
 builder.writeln("Quantity (kg)");
 builder.endRow();

 builder.insertCell();
 builder.writeln("Apples");
 builder.insertCell();
 builder.writeln("20");
 builder.endRow();

 builder.insertCell();
 builder.writeln("Bananas");
 builder.insertCell();
 builder.writeln("40");
 builder.endRow();

 builder.insertCell();
 builder.writeln("Carrots");
 builder.insertCell();
 builder.writeln("50");
 builder.endRow();

 doc.save(getArtifactsDir() + "DocumentBuilder.InsertTableWithStyle.docx");
 
```

**Parameters:**
| Parameter | Type | Description |
| --- | --- | --- |
| value | int | Bit flags that specify how a table style is applied to this table. The value must be a bitwise combination of [TableStyleOptions](../../com.aspose.words/tablestyleoptions/) constants. |

### setTextWrapping(int value) {#setTextWrapping-int}
```
public void setTextWrapping(int value)
```


Sets [getTextWrapping()](../../com.aspose.words/table/\#getTextWrapping) / [setTextWrapping(int)](../../com.aspose.words/table/\#setTextWrapping-int) for table.

 **Examples:** 

Shows how to work with table text wrapping.

```

 Document doc = new Document();
 DocumentBuilder builder = new DocumentBuilder(doc);

 Table table = builder.startTable();
 builder.insertCell();
 builder.write("Cell 1");
 builder.insertCell();
 builder.write("Cell 2");
 builder.endTable();
 table.setPreferredWidth(PreferredWidth.fromPoints(300.0));

 builder.getFont().setSize(16.0);
 builder.writeln("Lorem ipsum dolor sit amet, consectetur adipiscing elit, sed do eiusmod tempor incididunt ut labore et dolore magna aliqua.");

 // Set the "TextWrapping" property to "TextWrapping.Around" to get the table to wrap text around it,
 // and push it down into the paragraph below by setting the position.
 table.setTextWrapping(TextWrapping.AROUND);
 table.setAbsoluteHorizontalDistance(100.0);
 table.setAbsoluteVerticalDistance(20.0);

 doc.save(getArtifactsDir() + "Table.WrapText.docx");
 
```

**Parameters:**
| Parameter | Type | Description |
| --- | --- | --- |
| value | int | [getTextWrapping()](../../com.aspose.words/table/\#getTextWrapping) / [setTextWrapping(int)](../../com.aspose.words/table/\#setTextWrapping-int) for table. The value must be one of [TextWrapping](../../com.aspose.words/textwrapping/) constants. |

### setTitle(String value) {#setTitle-java.lang.String}
```
public void setTitle(String value)
```


Sets title of this table. It provides an alternative text representation of the information contained in the table.

 **Remarks:** 

The default value is an empty string.

This property is meaningful for ISO/IEC 29500 compliant DOCX documents ( [OoxmlCompliance](../../com.aspose.words/ooxmlcompliance/)). When saved to pre-ISO/IEC 29500 formats, the property is ignored.

 **Examples:** 

Shows how to build a nested table without using a document builder.

```

 public void createNestedTable() throws Exception {
     Document doc = new Document();

     // Create the outer table with three rows and four columns, and then add it to the document.
     Table outerTable = createTable(doc, 3, 4, "Outer Table");
     doc.getFirstSection().getBody().appendChild(outerTable);

     // Create another table with two rows and two columns and then insert it into the first table's first cell.
     Table innerTable = createTable(doc, 2, 2, "Inner Table");
     outerTable.getFirstRow().getFirstCell().appendChild(innerTable);

     doc.save(getArtifactsDir() + "Table.CreateNestedTable.docx");
 }

 // Creates a new table in the document with the given dimensions and text in each cell.
 private Table createTable(final Document doc, final int rowCount, final int cellCount, final String cellText) throws Exception {
     Table table = new Table(doc);

     for (int rowId = 1; rowId <= rowCount; rowId++) {
         Row row = new Row(doc);
         table.appendChild(row);

         for (int cellId = 1; cellId <= cellCount; cellId++) {
             Cell cell = new Cell(doc);
             cell.appendChild(new Paragraph(doc));
             cell.getFirstParagraph().appendChild(new Run(doc, cellText));

             row.appendChild(cell);
         }
     }

     // You can use the "Title" and "Description" properties to add a title and description respectively to your table.
     // The table must have at least one row before we can use these properties.
     // These properties are meaningful for ISO / IEC 29500 compliant .docx documents (see the OoxmlCompliance class).
     // If we save the document to pre-ISO/IEC 29500 formats, Microsoft Word ignores these properties.
     table.setTitle("Aspose table title");
     table.setDescription("Aspose table description");

     return table;
 }
 
```

**Parameters:**
| Parameter | Type | Description |
| --- | --- | --- |
| value | java.lang.String | Title of this table. |

### setTopPadding(double value) {#setTopPadding-double}
```
public void setTopPadding(double value)
```


Sets the amount of space (in points) to add above the contents of cells.

 **Examples:** 

Shows how to configure content padding in a table.

```

 Document doc = new Document();
 DocumentBuilder builder = new DocumentBuilder(doc);

 Table table = builder.startTable();
 builder.insertCell();
 builder.write("Row 1, cell 1.");
 builder.insertCell();
 builder.write("Row 1, cell 2.");
 builder.endTable();

 // For every cell in the table, set the distance between its contents and each of its borders.
 // This table will maintain the minimum padding distance by wrapping text.
 table.setLeftPadding(30.0);
 table.setRightPadding(60.0);
 table.setTopPadding(10.0);
 table.setBottomPadding(90.0);
 table.setPreferredWidth(PreferredWidth.fromPoints(250.0));

 doc.save(getArtifactsDir() + "DocumentBuilder.SetRowFormatting.docx");
 
```

**Parameters:**
| Parameter | Type | Description |
| --- | --- | --- |
| value | double | The amount of space (in points) to add above the contents of cells. |

### setVerticalAnchor(int value) {#setVerticalAnchor-int}
```
public void setVerticalAnchor(int value)
```


Gets the base object from which the vertical positioning of floating table should be calculated. Default value is [RelativeVerticalPosition.MARGIN](../../com.aspose.words/relativeverticalposition/\#MARGIN).

 **Examples:** 

Shows how to work with floating tables properties.

```

 Document doc = new Document(getMyDir() + "Table wrapped by text.docx");

 Table table = doc.getFirstSection().getBody().getTables().get(0);

 if (table.getTextWrapping() == TextWrapping.AROUND) {
     Assert.assertEquals(RelativeHorizontalPosition.MARGIN, table.getHorizontalAnchor());
     Assert.assertEquals(RelativeVerticalPosition.PARAGRAPH, table.getVerticalAnchor());
     Assert.assertEquals(false, table.getAllowOverlap());

     // Only Margin, Page, Column available in RelativeHorizontalPosition for HorizontalAnchor setter.
     // The ArgumentException will be thrown for any other values.
     table.setHorizontalAnchor(RelativeHorizontalPosition.COLUMN);

     // Only Margin, Page, Paragraph available in RelativeVerticalPosition for VerticalAnchor setter.
     // The ArgumentException will be thrown for any other values.
     table.setVerticalAnchor(RelativeVerticalPosition.PAGE);
 }
 
```

**Parameters:**
| Parameter | Type | Description |
| --- | --- | --- |
| value | int | The base object from which the vertical positioning of floating table should be calculated. The value must be one of [RelativeVerticalPosition](../../com.aspose.words/relativeverticalposition/) constants. |

### toString() {#toString}
```
public String toString()
```




**Returns:**
java.lang.String
### toString(SaveOptions saveOptions) {#toString-com.aspose.words.SaveOptions}
```
public String toString(SaveOptions saveOptions)
```


Exports the content of the node into a string using the specified save options.

**Parameters:**
| Parameter | Type | Description |
| --- | --- | --- |
| saveOptions | [SaveOptions](../../com.aspose.words/saveoptions/) | Specifies the options that control how the node is saved. |

**Returns:**
java.lang.String - The content of the node in the specified format.

 **Examples:** 

Exports the content of a node to String in HTML format.

```

 Document doc = new Document(getMyDir() + "Document.docx");

 Node node = doc.getLastSection().getBody().getLastParagraph();

 // When we call the ToString method using the html SaveFormat overload,
 // it converts the node's contents to their raw html representation.
 Assert.assertEquals(" " +
         "Hello World!" +
         "", node.toString(SaveFormat.HTML));

 // We can also modify the result of this conversion using a SaveOptions object.
 HtmlSaveOptions saveOptions = new HtmlSaveOptions();
 saveOptions.setExportRelativeFontSize(true);

 Assert.assertEquals(" " +
         "Hello World!" +
         "", node.toString(saveOptions));
 
```
### toString(int saveFormat) {#toString-int}
```
public String toString(int saveFormat)
```




**Parameters:**
| Parameter | Type | Description |
| --- | --- | --- |
| saveFormat | int |  |

**Returns:**
java.lang.String
### wait() {#wait}
```
public final void wait()
```




### wait(long arg0) {#wait-long}
```
public final native void wait(long arg0)
```




**Parameters:**
| Parameter | Type | Description |
| --- | --- | --- |
| arg0 | long |  |

### wait(long arg0, int arg1) {#wait-long-int}
```
public final void wait(long arg0, int arg1)
```




**Parameters:**
| Parameter | Type | Description |
| --- | --- | --- |
| arg0 | long |  |
| arg1 | int |  |

