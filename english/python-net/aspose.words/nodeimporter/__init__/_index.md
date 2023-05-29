---
title: NodeImporter constructor
linktitle: NodeImporter constructor
articleTitle: NodeImporter constructor
second_title: Aspose.Words for Python
description: "aspose.words.NodeImporter constructor"
type: docs
weight: 10
url: /python-net/aspose.words/nodeimporter/__init__/
---

## NodeImporter(src_doc, dst_doc, import_format_mode) {#documentbase_documentbase_importformatmode}

Initializes a new instance of the [NodeImporter](../) class.



```python
def __init__(self, src_doc: aspose.words.DocumentBase, dst_doc: aspose.words.DocumentBase, import_format_mode: aspose.words.ImportFormatMode):
    ...
```

| Parameter | Type | Description |
| --- | --- | --- |
| src_doc | [DocumentBase](../../documentbase/) |  |
| dst_doc | [DocumentBase](../../documentbase/) |  |
| import_format_mode | [ImportFormatMode](../../importformatmode/) |  |

## NodeImporter(src_doc, dst_doc, import_format_mode, import_format_options) {#documentbase_documentbase_importformatmode_importformatoptions}

Initializes a new instance of the [NodeImporter](../) class.



```python
def __init__(self, src_doc: aspose.words.DocumentBase, dst_doc: aspose.words.DocumentBase, import_format_mode: aspose.words.ImportFormatMode, import_format_options: aspose.words.ImportFormatOptions):
    ...
```

| Parameter | Type | Description |
| --- | --- | --- |
| src_doc | [DocumentBase](../../documentbase/) |  |
| dst_doc | [DocumentBase](../../documentbase/) |  |
| import_format_mode | [ImportFormatMode](../../importformatmode/) |  |
| import_format_options | [ImportFormatOptions](../../importformatoptions/) |  |

## Examples

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

Shows how resolve a clash when importing documents that have lists with the same list definition identifier.

```python
src_doc = aw.Document(MY_DIR + "List with the same definition identifier - source.docx")
dst_doc = aw.Document(MY_DIR + "List with the same definition identifier - destination.docx")

# Set the "keep_source_numbering" property to "True" to apply a different list definition ID
# to identical styles as Aspose.Words imports them into destination documents.
import_format_options = aw.ImportFormatOptions()
import_format_options.keep_source_numbering = True

dst_doc.append_document(src_doc, aw.ImportFormatMode.USE_DESTINATION_STYLES, import_format_options)
dst_doc.update_list_labels()
```

Shows how to resolve list numbering clashes in source and destination documents.

```python
# Open a document with a custom list numbering scheme, and then clone it.
# Since both have the same numbering format, the formats will clash if we import one document into the other.
src_doc = aw.Document(MY_DIR + "Custom list numbering.docx")
dst_doc = src_doc.clone()

# When we import the document's clone into the original and then append it,
# then the two lists with the same list format will join.
# If we set the "keep_source_numbering" flag to "False", then the list from the document clone
# that we append to the original will carry on the numbering of the list we append it to.
# This will effectively merge the two lists into one.
# If we set the "keep_source_numbering" flag to "True", then the document clone
# list will preserve its original numbering, making the two lists appear as separate lists.
import_format_options = aw.ImportFormatOptions()
import_format_options.keep_source_numbering = keep_source_numbering

importer = aw.NodeImporter(src_doc, dst_doc, aw.ImportFormatMode.KEEP_DIFFERENT_STYLES, import_format_options)
for paragraph in src_doc.first_section.body.paragraphs:
    paragraph = paragraph.as_paragraph()
    imported_node = importer.import_node(paragraph, True)
    dst_doc.first_section.body.append_child(imported_node)

dst_doc.update_list_labels()

if keep_source_numbering:
    self.assertEqual(
        "6. Item 1\r\n" +
        "7. Item 2 \r\n" +
        "8. Item 3\r\n" +
        "9. Item 4\r\n" +
        "6. Item 1\r\n" +
        "7. Item 2 \r\n" +
        "8. Item 3\r\n" +
        "9. Item 4", dst_doc.first_section.body.to_string(aw.SaveFormat.TEXT).strip())
else:
    self.assertEqual(
        "6. Item 1\r\n" +
        "7. Item 2 \r\n" +
        "8. Item 3\r\n" +
        "9. Item 4\r\n" +
        "10. Item 1\r\n" +
        "11. Item 2 \r\n" +
        "12. Item 3\r\n" +
        "13. Item 4", dst_doc.first_section.body.to_string(aw.SaveFormat.TEXT).strip())
```

## See Also

* module [aspose.words](../../)
* class [NodeImporter](../)

