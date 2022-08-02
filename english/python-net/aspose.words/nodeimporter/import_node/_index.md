---
title: import_node method
second_title: Aspose.Words for Python via .NET API Reference
description: "Imports a node from one document into another."
type: docs
weight: 20
url: /python-net/aspose.words/nodeimporter/import_node/
---

## import_node(src_node, is_import_children) {#node_bool}

Imports a node from one document into another.




```python
def import_node(self, src_node: aspose.words.Node, is_import_children: bool):
    ...
```

| Parameter | Type | Description |
| --- | --- | --- |
| src_node | [Node](../../node/) |  |
| is_import_children | bool |  |

Importing a node creates a copy of the source node belonging to the importing document. 
The returned node has no parent. The source node is not altered or removed from the original document.

Before a node from another document can be inserted into this document, it must be imported.
During import, document-specific properties such as references to styles and lists are translated
from the original to the importing document. After the node was imported, it can be inserted
into the appropriate place in the document using [CompositeNode.insert_before()](../../compositenode/insert_before/#node_node) or 
[CompositeNode.insert_after()](../../compositenode/insert_after/#node_node).

If the source node already belongs to the destination document, then simply a deep clone
of the source node is created.




### Returns

The cloned, imported node. The node belongs to the destination document, but has no parent.


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
* class [NodeImporter](../)

