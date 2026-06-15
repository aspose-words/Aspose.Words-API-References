---
title: ReplacingArgs class
linktitle: ReplacingArgs class
articleTitle: ReplacingArgs class
second_title: Aspose.Words for Python
description: "aspose.words.replacing.ReplacingArgs class. Provides data for a custom replace operation"
type: docs
weight: 60
url: /python-net/aspose.words.replacing/replacingargs/
---

## ReplacingArgs class

Provides data for a custom replace operation.
To learn more, visit the [Find and Replace](https://docs.aspose.com/words/python-net/find-and-replace/) documentation article.




### Properties

| Name | Description |
| --- | --- |
| [group_index](./group_index/) | Identifies, by index, a captured group in the Aspose.Words.Replacing.ReplacingArgs.Match that is to be replaced with the [ReplacingArgs.replacement](./replacement/) string. |
| [group_name](./group_name/) | Identifies, by name, a captured group in the Aspose.Words.Replacing.ReplacingArgs.Match that is to be replaced with the [ReplacingArgs.replacement](./replacement/) string. |
| [match_end_node](./match_end_node/) | Gets the node that contains the end of the match. |
| [match_node](./match_node/) | Gets the node that contains the beginning of the match. |
| [match_offset](./match_offset/) | Gets the zero-based starting position of the match from the start of the node that contains the beginning of the match. |
| [replacement](./replacement/) | Gets or sets the replacement string. |

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

* module [aspose.words.replacing](../)
* class [IReplacingCallback](../ireplacingcallback/)
* class [Range](../../aspose.words/range/)
* method [Range.replace()](../../aspose.words/range/replace/#str_str_findreplaceoptions)

