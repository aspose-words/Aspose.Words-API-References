---
title: IReplacingCallback.replacing method
linktitle: replacing method
articleTitle: replacing method
second_title: Aspose.Words for Python
description: "IReplacingCallback.replacing method. A user defined method that is called during a replace operation for each match found just before a replace is made."
type: docs
weight: 10
url: /python-net/aspose.words.replacing/ireplacingcallback/replacing/
---

## replacing(args) {#replacingargs}

A user defined method that is called during a replace operation for each match found just before a replace is made.


```python
def replacing(self, args: aspose.words.replacing.ReplacingArgs):
    ...
```

| Parameter | Type | Description |
| --- | --- | --- |
| args | [ReplacingArgs](../../replacingargs/) |  |

### Returns

A [ReplaceAction](../../replaceaction/) value that specifies the action to be taken for the current match.



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

Shows how to replace all occurrences of a regular expression pattern with another string, while tracking all such replacements (TextFindAndReplacementLogger).

```python
class TextFindAndReplacementLogger(aw.replacing.IReplacingCallback):

    def __init__(self):
        self.m_log = []

    def replacing(self, args):
        m_log.append(f'"{args.match.value}" converted to "{args.replacement}" {args.match_offset} characters into a {args.match_node.node_type} node.')
        args.replacement = f'(Old value:"{args.match.value}") {args.replacement}'
        return aw.Replacing.ReplaceAction.REPLACE

    def get_log(self):
        return str.join('', self.m_log)
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
* class [IReplacingCallback](../)

