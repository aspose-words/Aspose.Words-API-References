---
title: is_end_of_section property
second_title: Aspose.Words for Python via .NET API Reference
description: "True if this paragraph is the last paragraph in the [Body](../../body/) (main text story) of a [Section](../../section/); false otherwise."
type: docs
weight: 80
url: /python-net/aspose.words/paragraph/is_end_of_section/
---

## Paragraph.is_end_of_section property

True if this paragraph is the last paragraph in the [Body](../../body/) (main text story) of a [Section](../../section/); false otherwise.



### Examples

Shows how to insert the contents of one document to a bookmark in another document.

```python
def test_insert_at_bookmark(self):

    doc = aw.Document()
    builder = aw.DocumentBuilder(doc)

    builder.start_bookmark("InsertionPoint")
    builder.write("We will insert a document here: ")
    builder.end_bookmark("InsertionPoint")

    doc_to_insert = aw.Document()
    builder = aw.DocumentBuilder(doc_to_insert)

    builder.write("Hello world!")

    doc_to_insert.save(ARTIFACTS_DIR + "NodeImporter.insert_at_bookmark.docx")

    bookmark = doc.range.bookmarks.get_by_name("InsertionPoint")
    ExNodeImporter.insert_document(bookmark.bookmark_start.parent_node, doc_to_insert)

    self.assertEqual("We will insert a document here: " +
                     "\rHello world!", doc.get_text().strip())

@staticmethod
def insert_document(insertion_destination: aw.Node, doc_to_insert: aw.Document):
    """Inserts the contents of a document after the specified node."""

    if insertion_destination.node_type == aw.NodeType.PARAGRAPH or insertion_destination.node_type == aw.NodeType.TABLE:

        destination_parent = insertion_destination.parent_node

        importer = aw.NodeImporter(doc_to_insert, insertion_destination.document, aw.ImportFormatMode.KEEP_SOURCE_FORMATTING)

        # Loop through all block-level nodes in the section's body,
        # then clone and insert every node that is not the last empty paragraph of a section.
        for src_section in doc_to_insert.sections:
            src_section = src_section.as_section()
            for src_node in src_section.body:
                if src_node.node_type == aw.NodeType.PARAGRAPH:
                    para = src_node.as_paragraph()
                    if para.is_end_of_section and not para.has_child_nodes:
                        continue

                new_node = importer.import_node(src_node, True)

                destination_parent.insert_after(new_node, insertion_destination)
                insertion_destination = new_node
    else:
        raise Exception("The destination node should be either a paragraph or table.")
```

### See Also

* module [aspose.words](../../)
* class [Paragraph](../)

