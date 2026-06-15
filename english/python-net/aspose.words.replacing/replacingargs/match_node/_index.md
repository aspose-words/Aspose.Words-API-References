---
title: ReplacingArgs.match_node property
linktitle: match_node property
articleTitle: match_node property
second_title: Aspose.Words for Python
description: "ReplacingArgs.match_node property. Gets the node that contains the beginning of the match."
type: docs
weight: 40
url: /python-net/aspose.words.replacing/replacingargs/match_node/
---

## ReplacingArgs.match_node property

Gets the node that contains the beginning of the match.


```python
@property
def match_node(self) -> aspose.words.Node:
    ...

```

### Examples

Shows how to insert an entire document's contents as a replacement of a match in a find-and-replace operation (InsertDocumentAtReplaceHandler).

```python
def _insert_document(insertion_destination, doc_to_insert):
    if insertion_destination.node_type == aw.NodeType.PARAGRAPH or insertion_destination.node_type == aw.NodeType.TABLE:
        dst_story = insertion_destination.parent_node
        importer = aw.NodeImporter(src_doc=doc_to_insert, dst_doc=insertion_destination.document, import_format_mode=aw.ImportFormatMode.KEEP_SOURCE_FORMATTING)
        for src_section in filter(lambda a: a is not None, map(lambda b: system_helper.linq.Enumerable.of_type(lambda x: x.as_section(), b), list(doc_to_insert.sections))):
            for src_node in src_section.body:
                # Skip the node if it is the last empty paragraph in a section.
                if src_node.node_type == aw.NodeType.PARAGRAPH:
                    para = src_node.as_paragraph()
                    if para.is_end_of_section and (not para.has_child_nodes):
                        continue
                new_node = importer.import_node(src_node, True)
                dst_story.insert_after(new_node, insertion_destination)
                insertion_destination = new_node
    else:
        raise Exception()
```

Shows how to insert an entire document's contents as a replacement of a match in a find-and-replace operation (InsertDocumentAtReplaceHandler).

```python
class InsertDocumentAtReplaceHandler(aw.replacing.IReplacingCallback):

    def replacing(self, args):
        sub_doc = aw.Document(file_name=MY_DIR + 'Document.docx')
        # Insert a document after the paragraph containing the matched text.
        para = args.match_node.parent_node.as_paragraph()
        ExRange._insert_document(para, sub_doc)
        # Remove the paragraph with the matched text.
        para.remove()
        return aw.replacing.ReplaceAction.SKIP
```

### See Also

* module [aspose.words.replacing](../../)
* class [ReplacingArgs](../)

