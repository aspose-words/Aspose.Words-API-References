---
title: accept method
second_title: Aspose.Words for Python via .NET API Reference
description: "Accepts a visitor."
type: docs
weight: 70
url: /python-net/aspose.words/headerfooter/accept/
---

## accept(visitor) {#documentvisitor}

Accepts a visitor.


```python
def accept(self, visitor: aspose.words.DocumentVisitor):
    ...
```

| Parameter | Type | Description |
| --- | --- | --- |
| visitor | [DocumentVisitor](../../documentvisitor/) |  |

Enumerates over this node and all of its children. Each node calls a corresponding method on [DocumentVisitor](../../documentvisitor/).

For more info see the Visitor design pattern.




Calls [DocumentVisitor.visit_header_footer_start()](../../documentvisitor/visit_header_footer_start/#headerfooter), then calls [Node.accept()](../../node/accept/#documentvisitor) for all child nodes of the section
and calls [DocumentVisitor.visit_header_footer_end()](../../documentvisitor/visit_header_footer_end/#headerfooter) at the end.



### Returns

True if all nodes were visited; false if [DocumentVisitor](../../documentvisitor/) stopped the operation before visiting all nodes.


### Examples

Shows how to print the node structure of every header and footer in a document.

```python
def test_header_footer_to_text(self):

    doc = aw.Document(MY_DIR + "DocumentVisitor-compatible features.docx")
    visitor = ExDocumentVisitor.HeaderFooterStructurePrinter()

    # When we get a composite node to accept a document visitor, the visitor visits the accepting node,
    # and then traverses all the node's children in a depth-first manner.
    # The visitor can read and modify each visited node.
    doc.accept(visitor)

    print(visitor.get_text())

    # An alternative way of accessing a document's header/footers section-by-section is by accessing the collection.
    header_footers = doc.first_section.headers_footers.to_array()
    self.assertEqual(3, len(header_footers))

class HeaderFooterStructurePrinter(aw.DocumentVisitor):
    """Traverses a node's non-binary tree of child nodes.
    Creates a map in the form of a string of all encountered HeaderFooter nodes and their children."""

    def __init__(self):

        aw.DocumentVisitor.__init__(self)

        self.builder = io.StringIO()
        self.visitor_is_inside_header_footer = False
        self.doc_traversal_depth = 0

    def get_text(self):

        return self.builder.getvalue()

    def visit_run(self, run: aw.Run) -> aw.VisitorAction:
        """Called when a Run node is encountered in the document."""

        if self.visitor_is_inside_header_footer:
            self._indent_and_append_line("[Run] \"" + run.get_text() + "\"")

        return aw.VisitorAction.CONTINUE

    def visit_header_footer_start(self, header_footer: aw.HeaderFooter) -> aw.VisitorAction:
        """Called when a HeaderFooter node is encountered in the document."""

        self._indent_and_append_line("[HeaderFooter start] HeaderFooterType: " + header_footer.header_footer_type)
        self.doc_traversal_depth += 1
        self.visitor_is_inside_header_footer = True

        return aw.VisitorAction.CONTINUE

    def visit_header_footer_end(self, header_footer: aw.HeaderFooter) -> aw.VisitorAction:
        """Called after all the child nodes of a HeaderFooter node have been visited."""

        self.doc_traversal_depth -= 1
        self._indent_and_append_line("[HeaderFooter end]")
        self.visitor_is_inside_header_footer = False

        return aw.VisitorAction.CONTINUE

    def _indent_and_append_line(self, text: str):
        """Append a line to the output, and indent it depending on how deep the visitor is into the document tree."""

        for i in range(self.doc_traversal_depth):
            self.builder.write("|  ")

        self.builder.write(text + "\n")
```

### See Also

* module [aspose.words](../../)
* class [HeaderFooter](../)

