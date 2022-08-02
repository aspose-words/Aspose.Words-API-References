---
title: visit_smart_tag_end method
second_title: Aspose.Words for Python via .NET API Reference
description: "Called when enumeration of a smart tag has ended."
type: docs
weight: 410
url: /python-net/aspose.words/documentvisitor/visit_smart_tag_end/
---

## visit_smart_tag_end(smart_tag) {#smarttag}

Called when enumeration of a smart tag has ended.


```python
def visit_smart_tag_end(self, smart_tag: aspose.words.markup.SmartTag):
    ...
```

| Parameter | Type | Description |
| --- | --- | --- |
| smart_tag | [SmartTag](../../../aspose.words.markup/smarttag/) |  |

### Returns

A [VisitorAction](../../visitoraction/) value that specifies how to continue the enumeration.


### Examples

Shows how to print the node structure of every smart tag in a document.

```python
def test_smart_tag_to_text(self):

    doc = aw.Document(MY_DIR + "Smart tags.doc")
    visitor = ExDocumentVisitor.SmartTagStructurePrinter()

    # When we get a composite node to accept a document visitor, the visitor visits the accepting node,
    # and then traverses all the node's children in a depth-first manner.
    # The visitor can read and modify each visited node.
    doc.accept(visitor)

    print(visitor.get_text())

class SmartTagStructurePrinter(aw.DocumentVisitor):
    """Traverses a node's non-binary tree of child nodes.
    Creates a map in the form of a string of all encountered SmartTag nodes and their children."""

    def __init__(self):

        aw.DocumentVisitor.__init__(self)

        self.builder = io.StringIO()
        self.visitor_is_inside_smart_tag = False
        self.doc_traversal_depth = 0

    def get_text(self) -> str:
        """Gets the plain text of the document that was accumulated by the visitor."""

        return self.builder.getvalue()

    def visit_run(self, run: aw.Run) -> aw.VisitorAction:
        """Called when a Run node is encountered in the document."""

        if self.visitor_is_inside_smart_tag:
            self._indent_and_append_line("[Run] \"" + run.get_text() + "\"")

        return aw.VisitorAction.CONTINUE

    def visit_smart_tag_start(self, smart_tag: aw.SmartTag) -> aw.VisitorAction:
        """Called when a SmartTag node is encountered in the document."""

        self._indent_and_append_line("[SmartTag start] Name: " + smart_tag.element)
        self.doc_traversal_depth += 1
        self.visitor_is_inside_smart_tag = True

        return aw.VisitorAction.CONTINUE

    def visit_smart_tag_end(self, smart_tag: aw.SmartTag) -> aw.VisitorAction:
        """Called after all the child nodes of a SmartTag node have been visited."""

        self.doc_traversal_depth -= 1
        self._indent_and_append_line("[SmartTag end]")
        self.visitor_is_inside_smart_tag = False

        return aw.VisitorAction.CONTINUE

    def _indent_and_append_line(self, text: str):
        """Append a line to the StringBuilder and indent it depending on how deep the visitor is into the document tree."""

        for i in range(self.doc_traversal_depth):
            self.builder.write("|  ")

        self.builder.write(text + "\n")
```

### See Also

* module [aspose.words](../../)
* class [DocumentVisitor](../)

