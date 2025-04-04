---
title: DocumentVisitor.visitRowStart method
linktitle: visitRowStart method
articleTitle: visitRowStart method
second_title: Aspose.Words for Node.js
description: "DocumentVisitor.visitRowStart method. Called when enumeration of a table row has started."
type: docs
weight: 350
url: /nodejs-net/aspose.words/documentvisitor/visitRowStart/
---

## visitRowStart(row) {#row}

Called when enumeration of a table row has started.


```js
visitRowStart(row: Aspose.Words.Tables.Row)
```

| Parameter | Type | Description |
| --- | --- | --- |
| row | [Row](../../../aspose.words.tables/row/) | The object that is being visited. |

### Returns

A [VisitorAction](../../visitoraction/) value that specifies how to continue the enumeration.


### Examples

Shows how to print the node structure of every table in a document.

```js
test('TableToText', () => {
  let doc = new aw.Document(base.myDir + "DocumentVisitor-compatible features.docx");
  let visitor = new TableStructurePrinter();

  // When we get a composite node to accept a document visitor, the visitor visits the accepting node,
  // and then traverses all the node's children in a depth-first manner.
  // The visitor can read and modify each visited node.
  doc.accept(visitor);

  console.log(visitor.getText());
});


  /// <summary>
  /// Traverses a node's non-binary tree of child nodes.
  /// Creates a map in the form of a string of all encountered Table nodes and their children.
  /// </summary>
public class TableStructurePrinter : DocumentVisitor
{
  public TableStructurePrinter()
  {
    mVisitedTables = new StringBuilder();
    mVisitorIsInsideTable = false;
  }

  public string GetText()
  {
    return mVisitedTables.toString();
  }

    /// <summary>
    /// Called when a Run node is encountered in the document.
    /// Runs that are not within tables are not recorded.
    /// </summary>
  public override VisitorAction VisitRun(Run run)
  {
    if (mVisitorIsInsideTable) IndentAndAppendLine("[Run] \"" + run.getText() + "\"");

    return aw.VisitorAction.Continue;
  }

    /// <summary>
    /// Called when a Table is encountered in the document.
    /// </summary>
  public override VisitorAction VisitTableStart(Table table)
  {
    int rows = 0;
    int columns = 0;

    if (table.rows.count > 0)
    {
      rows = table.rows.count;
      columns = table.firstRow.count;
    }

    IndentAndAppendLine("[Table start] Size: " + rows + "x" + columns);
    mDocTraversalDepth++;
    mVisitorIsInsideTable = true;

    return aw.VisitorAction.Continue;
  }

    /// <summary>
    /// Called after all the child nodes of a Table node have been visited.
    /// </summary>
  public override VisitorAction VisitTableEnd(Table table)
  {
    mDocTraversalDepth--;
    IndentAndAppendLine("[Table end]");
    mVisitorIsInsideTable = false;

    return aw.VisitorAction.Continue;
  }

    /// <summary>
    /// Called when a Row node is encountered in the document.
    /// </summary>
  public override VisitorAction VisitRowStart(Row row)
  {
    string rowContents = row.getText().TrimEnd(new []{ '\u0007', ' ' }).Replace("\u0007", ", ");
    int rowWidth = row.indexOf(row.lastCell) + 1;
    int rowIndex = row.parentTable.indexOf(row);
    string rowStatusInTable = row.isFirstRow && row.isLastRow ? "only" : row.isFirstRow ? "first" : row.isLastRow ? "last" : "";
    if (rowStatusInTable != "")
    {
      rowStatusInTable = `, the ${rowStatusInTable} row in this table,`;
    }

    IndentAndAppendLine(`[Row start] Row #${++rowIndex}${rowStatusInTable} width ${rowWidth}, \"${rowContents}\"`);
    mDocTraversalDepth++;

    return aw.VisitorAction.Continue;
  }

    /// <summary>
    /// Called after all the child nodes of a Row node have been visited.
    /// </summary>
  public override VisitorAction VisitRowEnd(Row row)
  {
    mDocTraversalDepth--;
    IndentAndAppendLine("[Row end]");

    return aw.VisitorAction.Continue;
  }

    /// <summary>
    /// Called when a Cell node is encountered in the document.
    /// </summary>
  public override VisitorAction VisitCellStart(Cell cell)
  {
    let row = cell.parentRow;
    let table = row.parentTable;
    string cellStatusInRow = cell.isFirstCell && cell.isLastCell ? "only" : cell.isFirstCell ? "first" : cell.isLastCell ? "last" : "";
    if (cellStatusInRow != "")
    {
      cellStatusInRow = `, the ${cellStatusInRow} cell in this row`;
    }

    IndentAndAppendLine(`[Cell start] Row ${table.indexOf(row) + 1}, Col ${row.indexOf(cell) + 1}${cellStatusInRow}`);
    mDocTraversalDepth++;

    return aw.VisitorAction.Continue;
  }

    /// <summary>
    /// Called after all the child nodes of a Cell node have been visited.
    /// </summary>
  public override VisitorAction VisitCellEnd(Cell cell)
  {
    mDocTraversalDepth--;
    IndentAndAppendLine("[Cell end]");
    return aw.VisitorAction.Continue;
  }

    /// <summary>
    /// Append a line to the StringBuilder, and indent it depending on how deep the visitor is
    /// into the current table's tree of child nodes.
    /// </summary>
    /// <param name="text"></param>
  private void IndentAndAppendLine(string text)
  {
    for (let i = 0; i < mDocTraversalDepth; i++)
    {
      mVisitedTables.append("|  ");
    }

    mVisitedTables.AppendLine(text);
  }

  private bool mVisitorIsInsideTable;
  private int mDocTraversalDepth;
  private readonly StringBuilder mVisitedTables;
}
```

### See Also

* module [Aspose.Words](../../)
* class [DocumentVisitor](../)

