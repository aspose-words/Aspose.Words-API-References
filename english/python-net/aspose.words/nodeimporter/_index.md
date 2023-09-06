﻿---
title: NodeImporter class
linktitle: NodeImporter class
articleTitle: NodeImporter class
second_title: Aspose.Words for Python
description: "aspose.words.NodeImporter class. Allows to efficiently perform repeated import of nodes from one document to another"
type: docs
weight: 750
url: /python-net/aspose.words/nodeimporter/
---

## NodeImporter class

Allows to efficiently perform repeated import of nodes from one document to another.
To learn more, visit the [Aspose.Words Document Object Model (DOM)](https://docs.aspose.com/words/python-net/aspose-words-document-object-model/) documentation article.




Aspose.Words provides functionality for easy copying and moving fragments
between Microsoft Word documents. This is known as "importing nodes".
Before you can insert a fragment from one document into another, you need to "import" it.
Importing creates a deep clone of the original node, ready to be inserted into the
destination document.

The simplest way to import a node is to use the [DocumentBase.import_node()](../documentbase/import_node/#node_bool) method
provided by the [DocumentBase](../documentbase/) object.

However, when you need to import nodes from one document to another multiple times,
it is better to use the [NodeImporter](./) class. The [NodeImporter](./)
class allows to minimize the number of styles and lists created in the destination document.

Copying or moving fragments from one Microsoft Word document to another presents a number
of technical challenges for Aspose.Words. In a Word document, styles and list formatting
are stored centrally, separately from the text of the document. The paragraphs
and runs of text merely reference the styles by internal unique identifiers.

The challenges arise from the fact that styles and lists are different in different documents.
For example, to copy a paragraph formatted with the Heading 1 style from one document to another,
a number of things must be taken into account: decide whether to copy the Heading 1 style from
the source document to the destination document, clone the paragraph, update the cloned
paragraph so it refers to the correct Heading 1 style in the destination document.
If the style had to be copied, all the styles that it references (based on style
and next paragraph style) should be analyzed and possibly copied too and so on.
Similar issues exist when copying bulleted or numbered paragraphs because Microsoft Word
stores list definitions separately from text.

The [NodeImporter](./) class is like a context, that holds the "translation tables"
during the import. It correctly translates between styles and lists in the source and
destination documents.




### Constructors
| Name | Description |
| --- | --- |
| [NodeImporter(src_doc, dst_doc, import_format_mode)](./__init__/#documentbase_documentbase_importformatmode) | Initializes a new instance of the [NodeImporter](./) class. |
| [NodeImporter(src_doc, dst_doc, import_format_mode, import_format_options)](./__init__/#documentbase_documentbase_importformatmode_importformatoptions) | Initializes a new instance of the [NodeImporter](./) class. |

### Methods

| Name | Description |
| --- | --- |
|[ import_node(src_node, is_import_children)](./import_node/#node_bool) | Imports a node from one document into another. |

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

* module [aspose.words](../)
* class [Document](../document/)
* method [DocumentBase.import_node()](../documentbase/import_node/#node_bool)

