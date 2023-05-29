---
title: DocumentVisitor.visit_comment_end method
linktitle: visit_comment_end method
articleTitle: visit_comment_end method
second_title: Aspose.Words for Python
description: "DocumentVisitor.visit_comment_end method. Called when enumeration of a comment text has ended."
type: docs
weight: 100
url: /python-net/aspose.words/documentvisitor/visit_comment_end/
---

## visit_comment_end(comment) {#comment}

Called when enumeration of a comment text has ended.


```python
def visit_comment_end(self, comment: aspose.words.Comment):
    ...
```

| Parameter | Type | Description |
| --- | --- | --- |
| comment | [Comment](../../comment/) |  |

### Returns

A [VisitorAction](../../visitoraction/) value that specifies how to continue the enumeration.


### Examples

Shows how to print the node structure of every comment and comment range in a document.

```python
def test_comments_to_text(self):

    doc = aw.Document(MY_DIR + "DocumentVisitor-compatible features.docx")
    visitor = ExDocumentVisitor.CommentStructurePrinter()

    # When we get a composite node to accept a document visitor, the visitor visits the accepting node,
    # and then traverses all the node's children in a depth-first manner.
    # The visitor can read and modify each visited node.
    doc.accept(visitor)

    print(visitor.get_text())

class CommentStructurePrinter(aw.DocumentVisitor):
    """Traverses a node's non-binary tree of child nodes.
    Creates a map in the form of a string of all encountered Comment/CommentRange nodes and their children."""

    def __init__(self):

        aw.DocumentVisitor.__init__(self)

        self.builder = io.StringIO()
        self.visitor_is_inside_comment = False
        self.doc_traversal_depth = 0

    def get_text(self):

        return self.builder.getvalue()

    def visit_run(self, run: aw.Run) -> aw.VisitorAction:
        """Called when a Run node is encountered in the document.
        A Run is only recorded if it is a child of a Comment or CommentRange node."""

        if self.visitor_is_inside_comment:
            self._indent_and_append_line("[Run] \"" + run.get_text() + "\"")

        return aw.VisitorAction.CONTINUE

    def visit_comment_range_start(self, comment_range_start: aw.CommentRangeStart) -> aw.VisitorAction:
        """Called when a CommentRangeStart node is encountered in the document."""

        self._indent_and_append_line("[Comment range start] ID: " + comment_range_start.id)
        self.doc_traversal_depth += 1
        self.visitor_is_inside_comment = True

        return aw.VisitorAction.CONTINUE

    def visit_comment_range_end(self, comment_range_end: aw.CommentRangeEnd) -> aw.VisitorAction:
        """Called when a CommentRangeEnd node is encountered in the document."""

        self.doc_traversal_depth -= 1
        self._indent_and_append_line("[Comment range end]")
        self.visitor_is_inside_comment = False

        return aw.VisitorAction.CONTINUE

    def visit_comment_start(self, comment: aw.Comment) -> aw.VisitorAction:
        """Called when a Comment node is encountered in the document."""

        self._indent_and_append_line(
            f"[Comment start] For comment range ID {comment.Id}, By {comment.Author} on {comment.DateTime}")
        self.doc_traversal_depth += 1
        self.visitor_is_inside_comment = True

        return aw.VisitorAction.CONTINUE

    def visit_comment_end(self, comment: aw.Comment) -> aw.VisitorAction:
        """Called after all the child nodes of a Comment node have been visited."""

        self.doc_traversal_depth -= 1
        self._indent_and_append_line("[Comment end]")
        self.visitor_is_inside_comment = False

        return aw.VisitorAction.CONTINUE

    def _indent_and_append_line(self, text: str):
        """Append a line to the output, and indent it depending on how deep the visitor is
        into a comment/comment range's tree of child nodes."""

        for i in range(self.doc_traversal_depth):
            self.builder.write("|  ")

        self.builder.write(text + "\n")
```

### See Also

* module [aspose.words](../../)
* class [DocumentVisitor](../)

