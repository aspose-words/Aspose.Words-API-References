---
title: DocumentVisitor.visit_paragraph_end method
linktitle: visit_paragraph_end method
articleTitle: visit_paragraph_end method
second_title: Aspose.Words for Python
description: "DocumentVisitor.visit_paragraph_end method. Called when enumeration of a paragraph has ended."
type: docs
weight: 320
url: /python-net/aspose.words/documentvisitor/visit_paragraph_end/
---

## visit_paragraph_end(paragraph) {#paragraph}

Called when enumeration of a paragraph has ended.


```python
def visit_paragraph_end(self, paragraph: aspose.words.Paragraph):
    ...
```

| Parameter | Type | Description |
| --- | --- | --- |
| paragraph | [Paragraph](../../paragraph/) |  |

### Returns

A [VisitorAction](../../visitoraction/) value that specifies how to continue the enumeration.


### Examples

Shows how to use a document visitor to print a document's node structure.

```python
def test_doc_structure_to_text(self):

    doc = aw.Document(MY_DIR + "DocumentVisitor-compatible features.docx")
    visitor = ExDocumentVisitor.DocStructurePrinter()

    # When we get a composite node to accept a document visitor, the visitor visits the accepting node,
    # and then traverses all the node's children in a depth-first manner.
    # The visitor can read and modify each visited node.
    doc.accept(visitor)

    print(visitor.get_text())

class DocStructurePrinter(aw.DocumentVisitor):
    """Traverses a node's tree of child nodes.
    Creates a map of this tree in the form of a string."""

    def __init__(self):

        aw.DocumentVisitor.__init__(self)

        self.accepting_node_child_tree = io.StringIO()
        self.doc_traversal_depth = 0

    def get_text(self):

        return self.accepting_node_child_tree.getvalue()

    def visit_document_start(self, doc: aw.Document) -> aw.VisitorAction:
        """Called when a Document node is encountered."""

        child_node_count = doc.get_child_nodes(aw.NodeType.ANY, True).count

        self._indent_and_append_line("[Document start] Child nodes: " + child_node_count)
        self.doc_traversal_depth += 1

        # Allow the visitor to continue visiting other nodes.
        return aw.VisitorAction.CONTINUE

    def visit_document_end(self, doc: aw.Document) -> aw.VisitorAction:
        """Called after all the child nodes of a Document node have been visited."""

        self.doc_traversal_depth -= 1
        self._indent_and_append_line("[Document end]")

        return aw.VisitorAction.CONTINUE

    def visit_section_start(self, section: aw.Section) -> aw.VisitorAction:
        """Called when a Section node is encountered in the document."""

        # Get the index of our section within the document.
        doc_sections = section.document.get_child_nodes(aw.NodeType.SECTION, False)
        section_index = doc_sections.index_of(section)

        self._indent_and_append_line("[Section start] Section index: " + section_index)
        self.doc_traversal_depth += 1

        return aw.VisitorAction.CONTINUE

    def visit_section_end(self, section: aw.Section) -> aw.VisitorAction:
        """Called after all the child nodes of a Section node have been visited."""

        self.doc_traversal_depth -= 1
        self._indent_and_append_line("[Section end]")

        return aw.VisitorAction.CONTINUE

    def visit_body_start(self, body: aw.Body) -> aw.VisitorAction:
        """Called when a Body node is encountered in the document."""

        paragraph_count = body.paragraphs.count
        self._indent_and_append_line("[Body start] Paragraphs: " + paragraph_count)
        self.doc_traversal_depth += 1

        return aw.VisitorAction.CONTINUE

    def visit_body_end(self, body: aw.Body) -> aw.VisitorAction:
        """Called after all the child nodes of a Body node have been visited."""

        self.doc_traversal_depth -= 1
        self._indent_and_append_line("[Body end]")

        return aw.VisitorAction.CONTINUE

    def visit_paragraph_start(self, paragraph: aw.Paragraph) -> aw.VisitorAction:
        """Called when a Paragraph node is encountered in the document."""

        self._indent_and_append_line("[Paragraph start]")
        self.doc_traversal_depth += 1

        return aw.VisitorAction.CONTINUE

    def visit_paragraph_end(self, paragraph: aw.Paragraph) -> aw.VisitorAction:
        """Called after all the child nodes of a Paragraph node have been visited."""

        self.doc_traversal_depth -= 1
        self._indent_and_append_line("[Paragraph end]")

        return aw.VisitorAction.CONTINUE

    def visit_run(self, run: aw.Run) -> aw.VisitorAction:
        """Called when a Run node is encountered in the document."""

        self._indent_and_append_line("[Run] \"" + run.get_text() + "\"")

        return aw.VisitorAction.CONTINUE

    def visit_sub_document(self, sub_document: aw.SubDocument) -> aw.VisitorAction:
        """Called when a SubDocument node is encountered in the document."""

        self._indent_and_append_line("[SubDocument]")

        return aw.VisitorAction.CONTINUE

    def _indent_and_append_line(self, text: str):
        """Append a line to the StringBuilder and indent it depending on how deep the visitor is into the document tree."""

        for i in range(self.doc_traversal_depth):
            self.accepting_node_child_tree.write("|  ")

        self.accepting_node_child_tree.write(text + "\n")
```

### See Also

* module [aspose.words](../../)
* class [DocumentVisitor](../)

