---
title: DocumentVisitor.visit_field_start method
linktitle: visit_field_start method
articleTitle: visit_field_start method
second_title: Aspose.Words for Python
description: "DocumentVisitor.visit_field_start method. Called when a field starts in the document."
type: docs
weight: 200
url: /python-net/aspose.words/documentvisitor/visit_field_start/
---

## visit_field_start(field_start) {#fieldstart}

Called when a field starts in the document.


```python
def visit_field_start(self, field_start: aspose.words.fields.FieldStart):
    ...
```

| Parameter | Type | Description |
| --- | --- | --- |
| field_start | [FieldStart](../../../aspose.words.fields/fieldstart/) |  |

A field in a Word document consists of a field code and field value.

For example, a field that displays a page number can be represented as follows:

[FieldStart]PAGE[FieldSeparator]98[FieldEnd]

The field separator separates field code from field value in the document. Note that some 
fields have only field code and do not have field separator and field value.

Fields can be nested.




### Returns

A [VisitorAction](../../visitoraction/) value that specifies how to continue the enumeration.


### Examples

Shows how to print the node structure of every field in a document.

```python
def test_field_to_text(self):

    doc = aw.Document(MY_DIR + "DocumentVisitor-compatible features.docx")
    visitor = ExDocumentVisitor.FieldStructurePrinter()

    # When we get a composite node to accept a document visitor, the visitor visits the accepting node,
    # and then traverses all the node's children in a depth-first manner.
    # The visitor can read and modify each visited node.
    doc.accept(visitor)

    print(visitor.get_text())

class FieldStructurePrinter(aw.DocumentVisitor):
    """Traverses a node's non-binary tree of child nodes.
    Creates a map in the form of a string of all encountered Field nodes and their children."""

    def __init__(self):

        aw.DocumentVisitor.__init__(self)

        self.builder = io.StringIO()
        self.visitor_is_inside_field = False
        self.doc_traversal_depth = 0

    def get_text(self):

        return self.builder.getvalue()

    def visit_run(self, run: aw.Run) -> aw.VisitorAction:
        """Called when a Run node is encountered in the document."""

        if self.visitor_is_inside_field:
            self._indent_and_append_line("[Run] \"" + run.get_text() + "\"")

        return aw.VisitorAction.CONTINUE

    def visit_field_start(self, field_start: aw.fields.FieldStart) -> aw.VisitorAction:
        """Called when a FieldStart node is encountered in the document."""

        self._indent_and_append_line("[Field start] FieldType: " + field_start.field_type)
        self.doc_traversal_depth += 1
        self.visitor_is_inside_field = True

        return aw.VisitorAction.CONTINUE

    def visit_field_end(self, field_end: aw.fields.FieldEnd) -> aw.VisitorAction:
        """Called when a FieldEnd node is encountered in the document."""

        self.doc_traversal_depth -= 1
        self._indent_and_append_line("[Field end]")
        self.visitor_is_inside_field = False

        return aw.VisitorAction.CONTINUE

    def visit_field_separator(self, field_separator: aw.fields.FieldSeparator) -> aw.VisitorAction:
        """Called when a FieldSeparator node is encountered in the document."""

        self._indent_and_append_line("[FieldSeparator]")

        return aw.VisitorAction.CONTINUE

    def _indent_and_append_line(self, text: str):
        """Append a line to the output, and indent it depending on how deep the visitor is
        into the field's tree of child nodes."""

        for i in range(self.doc_traversal_depth):
            self.builder.write("|  ")

        self.builder.write(text + "\n")
```

### See Also

* module [aspose.words](../../)
* class [DocumentVisitor](../)

