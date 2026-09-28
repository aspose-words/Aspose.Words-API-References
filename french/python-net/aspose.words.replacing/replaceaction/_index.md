---
title: ReplaceAction enumeration
linktitle: ReplaceAction enumeration
articleTitle: ReplaceAction enumeration
second_title: Aspose.Words for Python
description: "aspose.words.replacing.ReplaceAction enumeration. Allows the user to specify what happens to the current match during a replace operation."
type: docs
weight: 40
url: /fr/python-net/aspose.words.replacing/replaceaction/
---

## ReplaceAction enumeration

Allows the user to specify what happens to the current match during a replace operation.


### Members

| Name | Description |
| --- | --- |
| REPLACE | Replace the current match. |
| SKIP | Skip the current match. |
| STOP | Terminate the replace operation. |

### Examples

Shows how to insert an entire document's contents as a replacement of a match in a find-and-replace operation (InsertDocumentAtReplaceHandler).

```python
def _insert_document(insertion_destination, doc_to_insert):
    if insertion_destination.node_type == aw.NodeType.PARAGRAPH or insertion_destination.node_type == aw.NodeType.TABLE:
        dst_story = insertion_destination.parent_node
        importer = aw.NodeImporter(src_doc=doc_to_insert, dst_doc=insertion_destination.document, import_format_mode=aw.ImportFormatMode.KEEP_SOURCE_FORMATTING)
        for src_section in filter(lambda a: a is not None, map(lambda b: system_helper.linq.Enumerable.of_type(lambda x: x.as_section(), b), list(doc_to_insert.sections))):
            for src_node in src_section.body:
                # Ignorer le nœud s'il s'agit du dernier paragraphe vide d'une section.
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
        # Insérer un document après le paragraphe contenant le texte correspondant.
        para = args.match_node.parent_node.as_paragraph()
        ExRange._insert_document(para, sub_doc)
        # Supprimer le paragraphe contenant le texte correspondant.
        para.remove()
        return aw.replacing.ReplaceAction.SKIP
```

### See Also

* module [aspose.words.replacing](../)
* class [IReplacingCallback](../ireplacingcallback/)
* class [Range](../../aspose.words/range/)
* method [Range.replace()](../../aspose.words/range/replace/#str_str_findreplaceoptions)

