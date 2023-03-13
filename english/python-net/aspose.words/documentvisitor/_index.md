﻿---
title: DocumentVisitor class
second_title: Aspose.Words for Python via .NET API Reference
description: "Base class for custom document visitors"
type: docs
weight: 310
url: /python-net/aspose.words/documentvisitor/
---

## DocumentVisitor class

Base class for custom document visitors.
To learn more, visit the [Aspose.Words Document Object Model (DOM)](https://docs.aspose.com/words/python-net/aspose-words-document-object-model/) documentation article.




With [DocumentVisitor](./) you can define and execute custom operations
that require enumeration over the document tree.

For example, Aspose.Words uses [DocumentVisitor](./) internally for saving [Document](../document/)
in various formats and for other operations like finding fields or bookmarks over
a fragment of a document.

To use [DocumentVisitor](./):


1. Create a class derived from [DocumentVisitor](./).
   
1. Override and provide implementations for some or all of the VisitXXX methods
   to perform some custom operations.
   
1. Call [Node.accept()](../node/accept/#documentvisitor) on the [Node](../node/) that
   you want to start the enumeration from.
   
[DocumentVisitor](./) provides default implementations for all of the VisitXXX methods 
to make it easier to create new document visitors as only the methods required for the particular
visitor need to be overridden. It is not necessary to override all of the visitor methods.

For more information see the Visitor design pattern.




### Methods

| Name | Description |
| --- | --- |
|[ visit_absolute_position_tab(tab)](./visit_absolute_position_tab/#absolutepositiontab) | Called when a [AbsolutePositionTab](../absolutepositiontab/) node is encountered in the document. |
|[ visit_body_end(body)](./visit_body_end/#body) | Called when enumeration of the main text story in a section has ended. |
|[ visit_body_start(body)](./visit_body_start/#body) | Called when enumeration of the main text story in a section has started. |
|[ visit_bookmark_end(bookmark_end)](./visit_bookmark_end/#bookmarkend) | Called when an end of a bookmark is encountered in the document. |
|[ visit_bookmark_start(bookmark_start)](./visit_bookmark_start/#bookmarkstart) | Called when a start of a bookmark is encountered in the document. |
|[ visit_building_block_end(block)](./visit_building_block_end/#buildingblock) | Called when enumeration of a building block has ended. |
|[ visit_building_block_start(block)](./visit_building_block_start/#buildingblock) | Called when enumeration of a building block has started. |
|[ visit_cell_end(cell)](./visit_cell_end/#cell) | Called when enumeration of a table cell has ended. |
|[ visit_cell_start(cell)](./visit_cell_start/#cell) | Called when enumeration of a table cell has started. |
|[ visit_comment_end(comment)](./visit_comment_end/#comment) | Called when enumeration of a comment text has ended. |
|[ visit_comment_range_end(comment_range_end)](./visit_comment_range_end/#commentrangeend) | Called when the end of a commented range of text is encountered. |
|[ visit_comment_range_start(comment_range_start)](./visit_comment_range_start/#commentrangestart) | Called when the start of a commented range of text is encountered. |
|[ visit_comment_start(comment)](./visit_comment_start/#comment) | Called when enumeration of a comment text has started. |
|[ visit_document_end(doc)](./visit_document_end/#document) | Called when enumeration of the document has finished. |
|[ visit_document_start(doc)](./visit_document_start/#document) | Called when enumeration of the document has started. |
|[ visit_editable_range_end(editable_range_end)](./visit_editable_range_end/#editablerangeend) | Called when an end of an editable range is encountered in the document. |
|[ visit_editable_range_start(editable_range_start)](./visit_editable_range_start/#editablerangestart) | Called when a start of an editable range is encountered in the document. |
|[ visit_field_end(field_end)](./visit_field_end/#fieldend) | Called when a field ends in the document. |
|[ visit_field_separator(field_separator)](./visit_field_separator/#fieldseparator) | Called when a field separator is encountered in the document. |
|[ visit_field_start(field_start)](./visit_field_start/#fieldstart) | Called when a field starts in the document. |
|[ visit_footnote_end(footnote)](./visit_footnote_end/#footnote) | Called when enumeration of a footnote or endnote text has ended. |
|[ visit_footnote_start(footnote)](./visit_footnote_start/#footnote) | Called when enumeration of a footnote or endnote text has started. |
|[ visit_form_field(form_field)](./visit_form_field/#formfield) | Called when a form field is encountered in the document. |
|[ visit_glossary_document_end(glossary)](./visit_glossary_document_end/#glossarydocument) | Called when enumeration of a glossary document has ended. |
|[ visit_glossary_document_start(glossary)](./visit_glossary_document_start/#glossarydocument) | Called when enumeration of a glossary document has started. |
|[ visit_group_shape_end(group_shape)](./visit_group_shape_end/#groupshape) | Called when enumeration of a group shape has ended. |
|[ visit_group_shape_start(group_shape)](./visit_group_shape_start/#groupshape) | Called when enumeration of a group shape has started. |
|[ visit_header_footer_end(header_footer)](./visit_header_footer_end/#headerfooter) | Called when enumeration of a header or footer in a section has ended. |
|[ visit_header_footer_start(header_footer)](./visit_header_footer_start/#headerfooter) | Called when enumeration of a header or footer in a section has started. |
|[ visit_office_math_end(office_math)](./visit_office_math_end/#officemath) | Called when enumeration of a Office Math object has ended. |
|[ visit_office_math_start(office_math)](./visit_office_math_start/#officemath) | Called when enumeration of a Office Math object has started. |
|[ visit_paragraph_end(paragraph)](./visit_paragraph_end/#paragraph) | Called when enumeration of a paragraph has ended. |
|[ visit_paragraph_start(paragraph)](./visit_paragraph_start/#paragraph) | Called when enumeration of a paragraph has started. |
|[ visit_row_end(row)](./visit_row_end/#row) | Called when enumeration of a table row has ended. |
|[ visit_row_start(row)](./visit_row_start/#row) | Called when enumeration of a table row has started. |
|[ visit_run(run)](./visit_run/#run) | Called when a run of text in the is encountered. |
|[ visit_section_end(section)](./visit_section_end/#section) | Called when enumeration of a section has ended. |
|[ visit_section_start(section)](./visit_section_start/#section) | Called when enumeration of a section has started. |
|[ visit_shape_end(shape)](./visit_shape_end/#shape) | Called when enumeration of a shape has ended. |
|[ visit_shape_start(shape)](./visit_shape_start/#shape) | Called when enumeration of a shape has started. |
|[ visit_smart_tag_end(smart_tag)](./visit_smart_tag_end/#smarttag) | Called when enumeration of a smart tag has ended. |
|[ visit_smart_tag_start(smart_tag)](./visit_smart_tag_start/#smarttag) | Called when enumeration of a smart tag has started. |
|[ visit_special_char(special_char)](./visit_special_char/#specialchar) | Called when a [SpecialChar](../specialchar/) node is encountered in the document. |
|[ visit_structured_document_tag_end(sdt)](./visit_structured_document_tag_end/#structureddocumenttag) | Called when enumeration of a structured document tag has ended. |
|[ visit_structured_document_tag_range_end(sdt_range_end)](./visit_structured_document_tag_range_end/#structureddocumenttagrangeend) | Called when a StructuredDocumentTagRangeEnd is encountered. |
|[ visit_structured_document_tag_range_start(sdt_range_start)](./visit_structured_document_tag_range_start/#structureddocumenttagrangestart) | Called when a StructuredDocumentTagRangeStart is encountered. |
|[ visit_structured_document_tag_start(sdt)](./visit_structured_document_tag_start/#structureddocumenttag) | Called when enumeration of a structured document tag has started. |
|[ visit_sub_document(sub_document)](./visit_sub_document/#subdocument) | Called when a sub-document is encountered. |
|[ visit_table_end(table)](./visit_table_end/#table) | Called when enumeration of a table has ended. |
|[ visit_table_start(table)](./visit_table_start/#table) | Called when enumeration of a table has started. |

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

* module [aspose.words](../)

