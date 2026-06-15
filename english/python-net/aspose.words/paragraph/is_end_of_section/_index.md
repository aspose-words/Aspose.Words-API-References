---
title: Paragraph.is_end_of_section property
linktitle: is_end_of_section property
articleTitle: is_end_of_section property
second_title: Aspose.Words for Python
description: "Paragraph.is_end_of_section property. True if this paragraph is the last paragraph in the [Body](../../body/) (main text story) of a [Section](../../section/); false otherwise."
type: docs
weight: 80
url: /python-net/aspose.words/paragraph/is_end_of_section/
---

## Paragraph.is_end_of_section property

True if this paragraph is the last paragraph in the [Body](../../body/) (main text story) of a [Section](../../section/); false otherwise.



```python
@property
def is_end_of_section(self) -> bool:
    ...

```

### Examples

Shows how to insert the contents of one document to a bookmark in another document (InsertDocument).

```python
@staticmethod
def insert_document(insertion_destination, doc_to_insert):
    if insertion_destination.node_type == aw.NodeType.PARAGRAPH or insertion_destination.node_type == aw.NodeType.TABLE:
        destination_parent = insertion_destination.parent_node
        importer = aw.NodeImporter(src_doc=doc_to_insert, dst_doc=insertion_destination.document, import_format_mode=aw.ImportFormatMode.KEEP_SOURCE_FORMATTING)
        # Loop through all block-level nodes in the section's body,
        # then clone and insert every node that is not the last empty paragraph of a section.
        for src_section in filter(lambda a: a is not None, map(lambda b: system_helper.linq.Enumerable.of_type(lambda x: x.as_section(), b), list(doc_to_insert.sections))):
            for src_node in src_section.body:
                if src_node.node_type == aw.NodeType.PARAGRAPH:
                    para = src_node.as_paragraph()
                    if para.is_end_of_section and (not para.has_child_nodes):
                        continue
                new_node = importer.import_node(src_node, True)
                destination_parent.insert_after(new_node, insertion_destination)
                insertion_destination = new_node
    else:
        raise Exception()
```

### See Also

* module [aspose.words](../../)
* class [Paragraph](../)

