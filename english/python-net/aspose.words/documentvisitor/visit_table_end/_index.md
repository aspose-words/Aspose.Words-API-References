---
title: visit_table_end method
second_title: Aspose.Words for Python via .NET API Reference
description: "Called when enumeration of a table has ended."
type: docs
weight: 490
url: /python-net/aspose.words/documentvisitor/visit_table_end/
---

## visit_table_end(table) {#table}

Called when enumeration of a table has ended.


```python
def visit_table_end(self, table: aspose.words.tables.Table):
    ...
```

| Parameter | Type | Description |
| --- | --- | --- |
| table | [Table](../../../aspose.words.tables/table/) |  |

### Returns

A [VisitorAction](../../visitoraction/) value that specifies how to continue the enumeration.


### Examples

Shows how to print the node structure of every table in a document.

```python
def test_table_to_text(self):

    doc = aw.Document(MY_DIR + "DocumentVisitor-compatible features.docx")
    visitor = ExDocumentVisitor.TableStructurePrinter()

    # When we get a composite node to accept a document visitor, the visitor visits the accepting node,
    # and then traverses all the node's children in a depth-first manner.
    # The visitor can read and modify each visited node.
    doc.accept(visitor)

    print(visitor.get_text())

class TableStructurePrinter(aw.DocumentVisitor):
    """Traverses a node's non-binary tree of child nodes.
    Creates a map in the form of a string of all encountered Table nodes and their children."""

    def __init__(self):

        aw.DocumentVisitor.__init__(self)

        self.visited_tables = io.StringIO()
        self.visitor_is_inside_table = False
        self.doc_traversal_depth = 0

    def get_text(self):

        return self.visited_tables.getvalue()

    def visit_run(self, run: aw.Run) -> aw.VisitorAction:
        """Called when a Run node is encountered in the document.
        Runs that are not within tables are not recorded."""

        if self.visitor_is_inside_table:
            self._indent_and_append_line("[Run] \"" + run.get_text() + "\"")

        return aw.VisitorAction.CONTINUE

    def visit_table_start(self, table: aw.Table) -> aw.VisitorAction:
        """Called when a Table is encountered in the document."""

        rows = 0
        columns = 0

        if table.rows.count > 0:
            rows = table.rows.count
            columns = table.first_row.count

        self._indent_and_append_line("[Table start] Size: " + rows + "x" + columns)
        self.doc_traversal_depth += 1
        self.visitor_is_inside_table = True

        return aw.VisitorAction.CONTINUE

    def visit_table_end(self, table: aw.Table) -> aw.VisitorAction:
        """Called after all the child nodes of a Table node have been visited."""

        self.doc_traversal_depth -= 1
        self._indent_and_append_line("[Table end]")
        self.visitor_is_inside_table = False

        return aw.VisitorAction.CONTINUE

    def visit_row_start(self, row: aw.Row) -> aw.VisitorAction:
        """Called when a Row node is encountered in the document."""

        row_contents = row.get_text().rstrip("\u0007 ").replace("\u0007", ", ")
        row_width = row.index_of(row.last_cell) + 1
        row_index = row.parent_table.index_of(row)
        if row.is_first_row and row.is_last_row:
            row_status_in_table = "only"
        elif row.is_first_row:
            row_status_in_table = "first"
        elif row.is_last_row:
            row_status_in_table = "last"
        else:
            row_status_in_table = ""

        if row_status_in_table != "":
            row_status_in_table = f", the {row_status_in_table} row in this table,"

        row_index += 1
        self._indent_and_append_line(f"[Row start] Row #{row_index}{row_status_in_table} width {row_width}, \"{row_contents}\"")
        self.doc_traversal_depth += 1

        return aw.VisitorAction.CONTINUE

    def visit_row_end(self, row: aw.Row) -> aw.VisitorAction:
        """Called after all the child nodes of a Row node have been visited."""

        self.doc_traversal_depth -= 1
        self._indent_and_append_line("[Row end]")

        return aw.VisitorAction.CONTINUE

    def visit_cell_start(self, cell: aw.Cell) -> aw.VisitorAction:
        """Called when a Cell node is encountered in the document."""

        row = cell.parent_row
        table = row.parent_table
        if cell.is_first_cell and cell.is_last_cell:
            cell_status_in_row = "only"
        elif cell.is_first_cell:
            cell_status_in_row = "first"
        elif cell.is_last_cell:
            cell_status_in_row = "last"
        else:
            cell_status_in_row = ""

        if cell_status_in_row != "":
            cell_status_in_row = f", the {cell_status_in_row} cell in this row"

        self._indent_and_append_line(f"[Cell start] Row {table.index_of(row) + 1}, Col {row.index_of(cell) + 1}{cell_status_in_row}")
        self.doc_traversal_depth += 1

        return aw.VisitorAction.CONTINUE

    def visit_cell_end(self, cell: aw.Cell) -> aw.VisitorAction:
        """Called after all the child nodes of a Cell node have been visited."""

        self.doc_traversal_depth -= 1
        self._indent_and_append_line("[Cell end]")
        return aw.VisitorAction.CONTINUE

    def _indent_and_append_line(self, text: str):
        """Append a line to the output, and indent it depending on how deep the visitor is
        into the current table's tree of child nodes."""

        for i in range(self.doc_traversal_depth):
            self.visited_tables.write("|  ")

        self.visited_tables.write(text + "\n")
```

### See Also

* module [aspose.words](../../)
* class [DocumentVisitor](../)

