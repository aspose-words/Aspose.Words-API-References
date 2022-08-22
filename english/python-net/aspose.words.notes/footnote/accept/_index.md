﻿---
title: accept method
second_title: Aspose.Words for Python via .NET API Reference
description: "Accepts a visitor."
type: docs
weight: 70
url: /python-net/aspose.words.notes/footnote/accept/
---

## accept(visitor) {#documentvisitor}

Accepts a visitor.


```python
def accept(self, visitor: aspose.words.DocumentVisitor):
    ...
```

| Parameter | Type | Description |
| --- | --- | --- |
| visitor | [DocumentVisitor](../../../aspose.words/documentvisitor/) |  |

Enumerates over this node and all of its children. Each node calls a corresponding method on DocumentVisitor.

For more info see the Visitor design pattern.




Calls DocumentVisitor.VisitFootnoteStart, then calls Accept for all child nodes of the footnote
and calls DocumentVisitor.VisitFootnoteEnd at the end.


### Returns

True if all nodes were visited; false if DocumentVisitor stopped the operation before visiting all nodes.


### Examples

Shows how to print the node structure of every footnote in a document.

```python
def test_footnote_to_text(self):

    doc = aw.Document(MY_DIR + "DocumentVisitor-compatible features.docx")
    visitor = ExDocumentVisitor.FootnoteStructurePrinter()

    # When we get a composite node to accept a document visitor, the visitor visits the accepting node,
    # and then traverses all the node's children in a depth-first manner.
    # The visitor can read and modify each visited node.
    doc.accept(visitor)

    print(visitor.get_text())

class FootnoteStructurePrinter(aw.DocumentVisitor):
    """Traverses a node's non-binary tree of child nodes.
    Creates a map in the form of a string of all encountered Footnote nodes and their children."""

    def __init__(self):

        aw.DocumentVisitor.__init__(self)

        self.builder = io.StringIO()
        self.visitor_is_inside_footnote = False
        self.doc_traversal_depth = 0

    def get_text(self) -> str:
        """Gets the plain text of the document that was accumulated by the visitor."""

        return self.builder.getvalue()

    def visit_footnote_start(self, footnote: aw.Footnote) -> aw.VisitorAction:
        """Called when a Footnote node is encountered in the document."""

        self._indent_and_append_line("[Footnote start] Type: " + footnote.footnote_type)
        self.doc_traversal_depth += 1
        self.visitor_is_inside_footnote = True

        return aw.VisitorAction.CONTINUE

    def visit_footnote_end(self, footnote: aw.Footnote) -> aw.VisitorAction:
        """Called after all the child nodes of a Footnote node have been visited."""

        self.doc_traversal_depth -= 1
        self._indent_and_append_line("[Footnote end]")
        self.visitor_is_inside_footnote = False

        return aw.VisitorAction.CONTINUE

    def visit_run(self, run: aw.Run) -> aw.VisitorAction:
        """Called when a Run node is encountered in the document."""

        if self.visitor_is_inside_footnote:
            self._indent_and_append_line("[Run] \"" + run.get_text() + "\"")

        return aw.VisitorAction.CONTINUE

    def _indent_and_append_line(self, text: str):
        """Append a line to the output and indent it depending on how deep the visitor is into the document tree."""

        for i in range(self.doc_traversal_depth):
            self.builder.write("|  ")

        self.builder.write(text + "\n")
```

### See Also

* module [aspose.words.notes](../../)
* class [Footnote](../)
