---
title: accept method
second_title: Aspose.Words for Python via .NET API Reference
description: "Accepts a visitor."
type: docs
weight: 60
url: /python-net/aspose.words.math/officemath/accept/
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

Enumerates over this node and all of its children. Each node calls a corresponding method on [DocumentVisitor](../../../aspose.words/documentvisitor/).

For more info see the Visitor design pattern.




Calls [DocumentVisitor.visit_office_math_start()](../../../aspose.words/documentvisitor/visit_office_math_start/#officemath), then calls [Node.accept()](../../../aspose.words/node/accept/#documentvisitor) for all
child nodes of the Office Math and calls [DocumentVisitor.visit_office_math_end()](../../../aspose.words/documentvisitor/visit_office_math_end/#officemath) at the end.



### Returns

True if all nodes were visited; false if [DocumentVisitor](../../../aspose.words/documentvisitor/) stopped the operation before visiting all nodes.


### Examples

Shows how to print the node structure of every office math node in a document.

```python
def test_office_math_to_text(self):

    doc = aw.Document(MY_DIR + "DocumentVisitor-compatible features.docx")
    visitor = ExDocumentVisitor.OfficeMathStructurePrinter()

    # When we get a composite node to accept a document visitor, the visitor visits the accepting node,
    # and then traverses all the node's children in a depth-first manner.
    # The visitor can read and modify each visited node.
    doc.accept(visitor)

    print(visitor.get_text())

class OfficeMathStructurePrinter(aw.DocumentVisitor):
    """Traverses a node's non-binary tree of child nodes.
    Creates a map in the form of a string of all encountered OfficeMath nodes and their children."""

    def __init__(self):

        aw.DocumentVisitor.__init__(self)

        self.builder = io.StringIO()
        self.visitor_is_inside_office_math = False
        self.doc_traversal_depth = 0

    def get_text(self) -> str:
        """Gets the plain text of the document that was accumulated by the visitor."""

        return self.builder.getvalue()

    def visit_run(self, run: aw.Run) -> aw.VisitorAction:
        """Called when a Run node is encountered in the document."""

        if self.visitor_is_inside_office_math:
            self._indent_and_append_line("[Run] \"" + run.get_text() + "\"")

        return aw.VisitorAction.CONTINUE

    def visit_office_math_start(self, office_math: aw.OfficeMath) -> aw.VisitorAction:
        """Called when an OfficeMath node is encountered in the document."""

        self._indent_and_append_line("[OfficeMath start] Math object type: " + office_math.math_object_type)
        self.doc_traversal_depth += 1
        self.visitor_is_inside_office_math = True

        return aw.VisitorAction.CONTINUE

    def visit_office_math_end(self, office_math: aw.OfficeMath) -> aw.VisitorAction:
        """Called after all the child nodes of an OfficeMath node have been visited."""

        self.doc_traversal_depth -= 1
        self._indent_and_append_line("[OfficeMath end]")
        self.visitor_is_inside_office_math = False

        return aw.VisitorAction.CONTINUE

    def _indent_and_append_line(self, text: str):
        """Append a line to the StringBuilder and indent it depending on how deep the visitor is into the document tree."""

        for i in range(self.doc_traversal_depth):
            self.builder.write("|  ")

        self.builder.write(text + "\n")
```

### See Also

* module [aspose.words.math](../../)
* class [OfficeMath](../)

