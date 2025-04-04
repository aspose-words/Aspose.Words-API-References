---
title: Table class
linktitle: Table class
articleTitle: Table class
second_title: Aspose.Words for Node.js
description: "Aspose.Words.Table class. Represents a table in a Word document"
type: docs
weight: 1340
url: /nodejs-net/aspose.words/table/
---

## Table class

Represents a table in a Word document.
To learn more, visit the [Working with Tables](https://docs.aspose.com/words/nodejs-net/working-with-tables/) documentation article.




### Remarks

[Table](./) is a block-level node and can be a child of classes derived from [Story](../story/) or
[InlineStory](../inlinestory/).

[Table](./) can contain one or more [Row](../../aspose.words.tables/row/) nodes.

A minimal valid table needs to have at least one [Row](../../aspose.words.tables/row/).




**Inheritance:** [Table](./) → [CompositeNode](../compositenode/) → [Node](../node/)

### Constructors
| Name | Description |
| --- | --- |
| [Table(doc)](./constructor/#documentbase) | Initializes a new instance of the [Table](./) class. |

### Properties

| Name | Description |
| --- | --- |
| [absoluteHorizontalDistance](./absoluteHorizontalDistance/) | Gets or sets absolute horizontal floating table position specified by the table properties, in points. Default value is 0. |
| [absoluteVerticalDistance](./absoluteVerticalDistance/) | Gets or sets absolute vertical floating table position specified by the table properties, in points. Default value is 0. |
| [alignment](./alignment/) | Specifies how an inline table is aligned in the document. |
| [allowAutoFit](./allowAutoFit/) | Allows Microsoft Word and Aspose.Words to automatically resize cells in a table to fit their contents. |
| [allowCellSpacing](./allowCellSpacing/) | Gets or sets the "Allow spacing between cells" option. |
| [allowOverlap](./allowOverlap/) | Gets whether a floating table shall allow other floating objects in the document to overlap its extents when displayed. Default value is ``true``. |
| [bidi](./bidi/) | Gets or sets whether this is a right-to-left table. |
| [bottomPadding](./bottomPadding/) | Gets or sets the amount of space (in points) to add below the contents of cells. |
| [cellSpacing](./cellSpacing/) | Gets or sets the amount of space (in points) between the cells. |
| [count](../compositenode/count/) | Gets the number of immediate children of this node.<br>(Inherited from [CompositeNode](../compositenode/)) |
| [customNodeId](../node/customNodeId/) | Specifies custom node identifier.<br>(Inherited from [Node](../node/)) |
| [description](./description/) | Gets or sets description of this table. It provides an alternative text representation of the information contained in the table. |
| [distanceBottom](./distanceBottom/) | Gets or sets distance between table bottom and the surrounding text, in points. |
| [distanceLeft](./distanceLeft/) | Gets or sets distance between table left and the surrounding text, in points. |
| [distanceRight](./distanceRight/) | Gets or sets distance between table right and the surrounding text, in points. |
| [distanceTop](./distanceTop/) | Gets or sets distance between table top and the surrounding text, in points. |
| [document](../node/document/) | Gets the document to which this node belongs.<br>(Inherited from [Node](../node/)) |
| [firstChild](../compositenode/firstChild/) | Gets the first child of the node.<br>(Inherited from [CompositeNode](../compositenode/)) |
| [firstRow](./firstRow/) | Returns the first [Row](../../aspose.words.tables/row/) node in the table. |
| [hasChildNodes](../compositenode/hasChildNodes/) | Returns ``true`` if this node has any child nodes.<br>(Inherited from [CompositeNode](../compositenode/)) |
| [horizontalAnchor](./horizontalAnchor/) | Gets the base object from which the horizontal positioning of floating table should be calculated. Default value is [RelativeHorizontalPosition.Column](../../aspose.words.drawing/relativehorizontalposition/#Column). |
| [isComposite](../node/isComposite/) | Returns ``true`` if this node can contain other nodes.<br>(Inherited from [Node](../node/)) |
| [lastChild](../compositenode/lastChild/) | Gets the last child of the node.<br>(Inherited from [CompositeNode](../compositenode/)) |
| [lastRow](./lastRow/) | Returns the last [Row](../../aspose.words.tables/row/) node in the table. |
| [leftIndent](./leftIndent/) | Gets or sets the value that represents the left indent of the table. |
| [leftPadding](./leftPadding/) | Gets or sets the amount of space (in points) to add to the left of the contents of cells. |
| [nextSibling](../node/nextSibling/) | Gets the node immediately following this node.<br>(Inherited from [Node](../node/)) |
| [nodeType](./nodeType/) | Returns [NodeType.Table](../nodetype/#Table). |
| [parentNode](../node/parentNode/) | Gets the immediate parent of this node.<br>(Inherited from [Node](../node/)) |
| [preferredWidth](./preferredWidth/) | Gets or sets the table preferred width. |
| [previousSibling](../node/previousSibling/) | Gets the node immediately preceding this node.<br>(Inherited from [Node](../node/)) |
| [range](../node/range/) | Returns a [Range](../range/) object that represents the portion of a document that is contained in this node.<br>(Inherited from [Node](../node/)) |
| [relativeHorizontalAlignment](./relativeHorizontalAlignment/) | Gets or sets floating table relative horizontal alignment. |
| [relativeVerticalAlignment](./relativeVerticalAlignment/) | Gets or sets floating table relative vertical alignment. |
| [rightPadding](./rightPadding/) | Gets or sets the amount of space (in points) to add to the right of the contents of cells. |
| [rows](./rows/) | Provides typed access to the rows of the table. |
| [style](./style/) | Gets or sets the table style applied to this table. |
| [styleIdentifier](./styleIdentifier/) | Gets or sets the locale independent style identifier of the table style applied to this table. |
| [styleName](./styleName/) | Gets or sets the name of the table style applied to this table. |
| [styleOptions](./styleOptions/) | Gets or sets bit flags that specify how a table style is applied to this table. |
| [textWrapping](./textWrapping/) | Gets or sets [Table.textWrapping](./textWrapping/) for table. |
| [title](./title/) | Gets or sets title of this table. It provides an alternative text representation of the information contained in the table. |
| [topPadding](./topPadding/) | Gets or sets the amount of space (in points) to add above the contents of cells. |
| [verticalAnchor](./verticalAnchor/) | Gets the base object from which the vertical positioning of floating table should be calculated. Default value is [RelativeVerticalPosition.Margin](../../aspose.words.drawing/relativeverticalposition/#Margin). |

### Methods

| Name | Description |
| --- | --- |
|[ accept(visitor)](./accept/#documentvisitor) | Accepts a visitor. |
|[ acceptEnd(visitor)](./acceptEnd/#documentvisitor) | Accepts a visitor for visiting the end of the table. |
|[ acceptStart(visitor)](./acceptStart/#documentvisitor) | Accepts a visitor for visiting the start of the table. |
|[ appendChild(newChild)](../compositenode/appendChild/#node) | Adds the specified node to the end of the list of child nodes for this node.<br>(Inherited from [CompositeNode](../compositenode/)) |
|[ asBody()](../node/asBody/#default) | Cast node to [Body](../body/).<br>(Inherited from [Node](../node/)) |
|[ asBookmarkEnd()](../node/asBookmarkEnd/#default) | Cast node to [BookmarkEnd](../bookmarkend/).<br>(Inherited from [Node](../node/)) |
|[ asBookmarkStart()](../node/asBookmarkStart/#default) | Cast node to [BookmarkStart](../bookmarkstart/).<br>(Inherited from [Node](../node/)) |
|[ asBuildingBlock()](../node/asBuildingBlock/#default) | Cast node to [BuildingBlock](../buildingblock/).<br>(Inherited from [Node](../node/)) |
|[ asCell()](../node/asCell/#default) | Cast node to [Cell](../../aspose.words.tables/cell/).<br>(Inherited from [Node](../node/)) |
|[ asComment()](../node/asComment/#default) | Cast node to [Comment](../comment/).<br>(Inherited from [Node](../node/)) |
|[ asCommentRangeEnd()](../node/asCommentRangeEnd/#default) | Cast node to [CommentRangeEnd](../commentrangeend/).<br>(Inherited from [Node](../node/)) |
|[ asCommentRangeStart()](../node/asCommentRangeStart/#default) | Cast node to [CommentRangeStart](../commentrangestart/).<br>(Inherited from [Node](../node/)) |
|[ asCompositeNode()](../node/asCompositeNode/#default) | Cast node to [CompositeNode](../compositenode/).<br>(Inherited from [Node](../node/)) |
|[ asDocument()](../node/asDocument/#default) | Cast node to [Node.document](../node/document/).<br>(Inherited from [Node](../node/)) |
|[ asEditableRangeEnd()](../node/asEditableRangeEnd/#default) | Cast node to [EditableRangeEnd](../editablerangeend/).<br>(Inherited from [Node](../node/)) |
|[ asEditableRangeStart()](../node/asEditableRangeStart/#default) | Cast node to [EditableRangeStart](../editablerangestart/).<br>(Inherited from [Node](../node/)) |
|[ asFieldEnd()](../node/asFieldEnd/#default) | Cast node to [FieldEnd](../../aspose.words.fields/fieldend/).<br>(Inherited from [Node](../node/)) |
|[ asFieldSeparator()](../node/asFieldSeparator/#default) | Cast node to [FieldSeparator](../../aspose.words.fields/fieldseparator/).<br>(Inherited from [Node](../node/)) |
|[ asFieldStart()](../node/asFieldStart/#default) | Cast node to [FieldStart](../../aspose.words.fields/fieldstart/).<br>(Inherited from [Node](../node/)) |
|[ asFootnote()](../node/asFootnote/#default) | Cast node to [Footnote](../../aspose.words.notes/footnote/).<br>(Inherited from [Node](../node/)) |
|[ asFormField()](../node/asFormField/#default) | Cast node to [FormField](../../aspose.words.fields/formfield/).<br>(Inherited from [Node](../node/)) |
|[ asGlossaryDocument()](../node/asGlossaryDocument/#default) | Cast node to [GlossaryDocument](../../aspose.words.buildingblocks/glossarydocument/).<br>(Inherited from [Node](../node/)) |
|[ asGroupShape()](../node/asGroupShape/#default) | Cast node to [GroupShape](../../aspose.words.drawing/groupshape/).<br>(Inherited from [Node](../node/)) |
|[ asHeaderFooter()](../node/asHeaderFooter/#default) | Cast node to [HeaderFooter](../headerfooter/).<br>(Inherited from [Node](../node/)) |
|[ asOfficeMath()](../node/asOfficeMath/#default) | Cast node to [OfficeMath](../../aspose.words.math/officemath/).<br>(Inherited from [Node](../node/)) |
|[ asParagraph()](../node/asParagraph/#default) | Cast node to [Paragraph](../paragraph/).<br>(Inherited from [Node](../node/)) |
|[ asRow()](../node/asRow/#default) | Cast node to [Row](../../aspose.words.tables/row/).<br>(Inherited from [Node](../node/)) |
|[ asRun()](../node/asRun/#default) | Cast node to [Run](../run/).<br>(Inherited from [Node](../node/)) |
|[ asSection()](../node/asSection/#default) | Cast node to [Section](../section/).<br>(Inherited from [Node](../node/)) |
|[ asShape()](../node/asShape/#default) | Cast node to [Shape](../../aspose.words.drawing/shape/).<br>(Inherited from [Node](../node/)) |
|[ asSmartTag()](../node/asSmartTag/#default) | Cast node to [SmartTag](../../aspose.words.markup/smarttag/).<br>(Inherited from [Node](../node/)) |
|[ asSpecialChar()](../node/asSpecialChar/#default) | Cast node to [SpecialChar](../specialchar/).<br>(Inherited from [Node](../node/)) |
|[ asStructuredDocumentTag()](../node/asStructuredDocumentTag/#default) | Cast node to [StructuredDocumentTag](../../aspose.words.markup/structureddocumenttag/).<br>(Inherited from [Node](../node/)) |
|[ asStructuredDocumentTagRangeEnd()](../node/asStructuredDocumentTagRangeEnd/#default) | Cast node to [StructuredDocumentTagRangeEnd](../../aspose.words.markup/structureddocumenttagrangeend/).<br>(Inherited from [Node](../node/)) |
|[ asStructuredDocumentTagRangeStart()](../node/asStructuredDocumentTagRangeStart/#default) | Cast node to [StructuredDocumentTagRangeStart](../../aspose.words.markup/structureddocumenttagrangestart/).<br>(Inherited from [Node](../node/)) |
|[ asSubDocument()](../node/asSubDocument/#default) | Cast node to [SubDocument](../subdocument/).<br>(Inherited from [Node](../node/)) |
|[ asTable()](../node/asTable/#default) | Cast node to [Table](./).<br>(Inherited from [Node](../node/)) |
|[ autoFit(behavior)](./autoFit/#autofitbehavior) | Resizes the table and cells according to the specified auto fit behavior. |
|[ clearBorders()](./clearBorders/#default) | Removes all table and cell borders on this table. |
|[ clearShading()](./clearShading/#default) | Removes all shading on the table. |
|[ clone(isCloneChildren)](../node/clone/#boolean) | Creates a duplicate of the node.<br>(Inherited from [Node](../node/)) |
|[ convertToHorizontallyMergedCells()](./convertToHorizontallyMergedCells/#default) | Converts cells horizontally merged by width to cells merged by [CellFormat.horizontalMerge](../../aspose.words.tables/cellformat/horizontalMerge/). |
|[ ensureMinimum()](./ensureMinimum/#default) | If the table has no rows, creates and appends one [Row](../../aspose.words.tables/row/). |
|[ getAncestor(ancestorType)](../node/getAncestor/#nodetype) | Gets the first ancestor of the specified [NodeType](../nodetype/).<br>(Inherited from [Node](../node/)) |
|[ getBuildingBlock(index, isDeep)](../compositenode/getBuildingBlock/#number_boolean) | <br>(Inherited from [CompositeNode](../compositenode/)) |
|[ getChild(nodeType, index, isDeep)](../compositenode/getChild/#nodetype_number_boolean) | Returns an Nth child node that matches the specified type.<br>(Inherited from [CompositeNode](../compositenode/)) |
|[ getChildNodes(nodeType, isDeep)](../compositenode/getChildNodes/#nodetype_boolean) | Returns a live collection of child nodes that match the specified type.<br>(Inherited from [CompositeNode](../compositenode/)) |
|[ getComment(index, isDeep)](../compositenode/getComment/#number_boolean) | <br>(Inherited from [CompositeNode](../compositenode/)) |
|[ getEditableRangeStart(index, isDeep)](../compositenode/getEditableRangeStart/#number_boolean) | <br>(Inherited from [CompositeNode](../compositenode/)) |
|[ getFootnote(index, isDeep)](../compositenode/getFootnote/#number_boolean) | <br>(Inherited from [CompositeNode](../compositenode/)) |
|[ getGroupShape(index, isDeep)](../compositenode/getGroupShape/#number_boolean) | <br>(Inherited from [CompositeNode](../compositenode/)) |
|[ getOfficeMath(index, isDeep)](../compositenode/getOfficeMath/#number_boolean) | <br>(Inherited from [CompositeNode](../compositenode/)) |
|[ getParagraph(index, isDeep)](../compositenode/getParagraph/#number_boolean) | <br>(Inherited from [CompositeNode](../compositenode/)) |
|[ getRun(index, isDeep)](../compositenode/getRun/#number_boolean) | <br>(Inherited from [CompositeNode](../compositenode/)) |
|[ getSdt(index, isDeep)](../compositenode/getSdt/#number_boolean) | <br>(Inherited from [CompositeNode](../compositenode/)) |
|[ getSdtRangeEnd(index, isDeep)](../compositenode/getSdtRangeEnd/#number_boolean) | <br>(Inherited from [CompositeNode](../compositenode/)) |
|[ getSdtRangeStart(index, isDeep)](../compositenode/getSdtRangeStart/#number_boolean) | <br>(Inherited from [CompositeNode](../compositenode/)) |
|[ getShape(index, isDeep)](../compositenode/getShape/#number_boolean) | <br>(Inherited from [CompositeNode](../compositenode/)) |
|[ getSmartTag(index, isDeep)](../compositenode/getSmartTag/#number_boolean) | <br>(Inherited from [CompositeNode](../compositenode/)) |
|[ getTable(index, isDeep)](../compositenode/getTable/#number_boolean) | <br>(Inherited from [CompositeNode](../compositenode/)) |
|[ getText()](../node/getText/#default) | Gets the text of this node and of all its children.<br>(Inherited from [Node](../node/)) |
|[ indexOf(child)](../compositenode/indexOf/#node) | Returns the index of the specified child node in the child node array.<br>(Inherited from [CompositeNode](../compositenode/)) |
|[ insertAfter(newChild, refChild)](../compositenode/insertAfter/#node_node) | Inserts the specified node immediately after the specified reference node.<br>(Inherited from [CompositeNode](../compositenode/)) |
|[ insertBefore(newChild, refChild)](../compositenode/insertBefore/#node_node) | Inserts the specified node immediately before the specified reference node.<br>(Inherited from [CompositeNode](../compositenode/)) |
|[ nextPreOrder(rootNode)](../node/nextPreOrder/#node) | Gets next node according to the pre-order tree traversal algorithm.<br>(Inherited from [Node](../node/)) |
|[ nodeTypeToString(nodeType)](../node/nodeTypeToString/#nodetype) | A utility method that converts a node type enum value into a user friendly string.<br>(Inherited from [Node](../node/)) |
|[ prependChild(newChild)](../compositenode/prependChild/#node) | Adds the specified node to the beginning of the list of child nodes for this node.<br>(Inherited from [CompositeNode](../compositenode/)) |
|[ previousPreOrder(rootNode)](../node/previousPreOrder/#node) | Gets the previous node according to the pre-order tree traversal algorithm.<br>(Inherited from [Node](../node/)) |
|[ referenceEquals(other)](../node/referenceEquals/#node) | <br>(Inherited from [Node](../node/)) |
|[ remove()](../node/remove/#default) | Removes itself from the parent.<br>(Inherited from [Node](../node/)) |
|[ removeAllChildren()](../compositenode/removeAllChildren/#default) | Removes all the child nodes of the current node.<br>(Inherited from [CompositeNode](../compositenode/)) |
|[ removeChild(oldChild)](../compositenode/removeChild/#node) | Removes the specified child node.<br>(Inherited from [CompositeNode](../compositenode/)) |
|[ removeSmartTags()](../compositenode/removeSmartTags/#default) | Removes all [SmartTag](../../aspose.words.markup/smarttag/) descendant nodes of the current node.<br>(Inherited from [CompositeNode](../compositenode/)) |
|[ selectNodes(xpath)](../compositenode/selectNodes/#string) | Selects a list of nodes matching the XPath expression.<br>(Inherited from [CompositeNode](../compositenode/)) |
|[ selectSingleNode(xpath)](../compositenode/selectSingleNode/#string) | Selects the first [Node](../node/) that matches the XPath expression.<br>(Inherited from [CompositeNode](../compositenode/)) |
|[ setBorder(borderType, lineStyle, lineWidth, color, isOverrideCellBorders)](./setBorder/#bordertype_linestyle_number_string_boolean) | Sets the specified table border to the specified line style, width and color. |
|[ setBorders(lineStyle, lineWidth, color)](./setBorders/#linestyle_number_string) | Sets all table borders to the specified line style, width and color. |
|[ setShading(texture, foregroundColor, backgroundColor)](./setShading/#textureindex_string_string) | Sets shading to the specified values on whole table. |
|[ toString(saveFormat)](../node/toString/#saveformat) | Exports the content of the node into a string in the specified format.<br>(Inherited from [Node](../node/)) |
|[ toString(saveOptions)](../node/toString/#saveoptions) | Exports the content of the node into a string using the specified save options.<br>(Inherited from [Node](../node/)) |

### Examples

Shows how to build a formatted 2x2 table.

```js
let doc = new aw.Document();
let builder = new aw.DocumentBuilder(doc);

let table = builder.startTable();
builder.insertCell();
builder.cellFormat.verticalAlignment = aw.Tables.CellVerticalAlignment.Center;
builder.write("Row 1, cell 1.");
builder.insertCell();
builder.write("Row 1, cell 2.");
builder.endRow();

// While building the table, the document builder will apply its current RowFormat/CellFormat property values
// to the current row/cell that its cursor is in and any new rows/cells as it creates them.
expect(table.rows.at(0).cells.at(0).cellFormat.verticalAlignment).toEqual(aw.Tables.CellVerticalAlignment.Center);
expect(table.rows.at(0).cells.at(1).cellFormat.verticalAlignment).toEqual(aw.Tables.CellVerticalAlignment.Center);

builder.insertCell();
builder.rowFormat.height = 100;
builder.rowFormat.heightRule = aw.HeightRule.Exactly;
builder.cellFormat.orientation = aw.TextOrientation.Upward;
builder.write("Row 2, cell 1.");
builder.insertCell();
builder.cellFormat.orientation = aw.TextOrientation.Downward;
builder.write("Row 2, cell 2.");
builder.endRow();
builder.endTable();

// Previously added rows and cells are not retroactively affected by changes to the builder's formatting.
expect(table.rows.at(0).rowFormat.height).toEqual(0);
expect(table.rows.at(0).rowFormat.heightRule).toEqual(aw.HeightRule.Auto);
expect(table.rows.at(1).rowFormat.height).toEqual(100);
expect(table.rows.at(1).rowFormat.heightRule).toEqual(aw.HeightRule.Exactly);
expect(table.rows.at(1).cells.at(0).cellFormat.orientation).toEqual(aw.TextOrientation.Upward);
expect(table.rows.at(1).cells.at(1).cellFormat.orientation).toEqual(aw.TextOrientation.Downward);

doc.save(base.artifactsDir + "DocumentBuilder.BuildTable.docx");
```

Shows how to create a table.

```js
let doc = new aw.Document();
let table = new aw.Tables.Table(doc);
doc.firstSection.body.appendChild(table);

// Tables contain rows, which contain cells, which may have paragraphs
// with typical elements such as runs, shapes, and even other tables.
// Calling the "EnsureMinimum" method on a table will ensure that
// the table has at least one row, cell, and paragraph.
let firstRow = new aw.Tables.Row(doc);
table.appendChild(firstRow);

let firstCell = new aw.Tables.Cell(doc);
firstRow.appendChild(firstCell);

let paragraph = new aw.Paragraph(doc);
firstCell.appendChild(paragraph);

// Add text to the first cell in the first row of the table.
let run = new aw.Run(doc, "Hello world!");
paragraph.appendChild(run);

doc.save(base.artifactsDir + "Table.CreateTable.docx");
```

Shows how to iterate through all tables in the document and print the contents of each cell.

```js
let doc = new aw.Document(base.myDir + "Tables.docx");
let tables = doc.firstSection.body.tables;

expect(tables.toArray().length).toEqual(2);

for (let i = 0; i < tables.count; i++)
{
  console.log(`Start of Table ${i}`);

  let rows = tables.at(i).rows;

  for (let j = 0; j < rows.count; j++)
  {
    console.log(`\tStart of Row ${j}`);

    let cells = rows.at(j).cells;

    for (let k = 0; k < cells.count; k++)
    {
      let cellText = cells.at(k).toString(aw.SaveFormat.Text).trim();
      console.log(`\t\tContents of Cell:${k} = \"${cellText}\"`);
    }

    console.log(`\tEnd of Row ${j}`);
  }

  console.log(`End of Table ${i}\n`);
}
```

Shows how to build a nested table without using a document builder.

```js
test('CreateNestedTable', () => {
  let doc = new aw.Document();

  // Create the outer table with three rows and four columns, and then add it to the document.
  let outerTable = createTable(doc, 3, 4, "Outer Table");
  doc.firstSection.body.appendChild(outerTable);

  // Create another table with two rows and two columns and then insert it into the first table's first cell.
  let innerTable = createTable(doc, 2, 2, "Inner Table");
  outerTable.firstRow.firstCell.appendChild(innerTable);

  doc.save(base.artifactsDir + "Table.CreateNestedTable.docx");
});


/// <summary>
/// Creates a new table in the document with the given dimensions and text in each cell.
/// </summary>
function createTable(doc, rowCount, cellCount, cellText)
{
  let table = new aw.Tables.Table(doc);

  for (let rowId = 1; rowId <= rowCount; rowId++)
  {
    let row = new aw.Tables.Row(doc);
    table.appendChild(row);

    for (let cellId = 1; cellId <= cellCount; cellId++)
    {
      let cell = new aw.Tables.Cell(doc);
      cell.appendChild(new aw.Paragraph(doc));
      cell.firstParagraph.appendChild(new aw.Run(doc, cellText));

      row.appendChild(cell);
    }
  }

  // You can use the "Title" and "Description" properties to add a title and description respectively to your table.
  // The table must have at least one row before we can use these properties.
  // These properties are meaningful for ISO / IEC 29500 compliant .docx documents (see the OoxmlCompliance class).
  // If we save the document to pre-ISO/IEC 29500 formats, Microsoft Word ignores these properties.
  table.title = "Aspose table title";
  table.description = "Aspose table description";

  return table;
}
```

### See Also

* module [Aspose.Words](../)
* class [CompositeNode](../compositenode/)

