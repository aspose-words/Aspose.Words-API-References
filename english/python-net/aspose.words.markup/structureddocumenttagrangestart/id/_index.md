---
title: StructuredDocumentTagRangeStart.id property
linktitle: id property
articleTitle: id property
second_title: Aspose.Words for Python
description: "StructuredDocumentTagRangeStart.id property. Specifies a unique read-only persistent numerical Id for this structured document tag."
type: docs
weight: 40
url: /python-net/aspose.words.markup/structureddocumenttagrangestart/id/
---

## StructuredDocumentTagRangeStart.id property

Specifies a unique read-only persistent numerical Id for this structured document tag.




```python
@property
def id(self) -> int:
    ...

```

### Remarks

Id attribute shall follow these rules:

* The document shall retain structured document tag ids only if the whole document
  is cloned [Document.clone()](../../../aspose.words/document/clone/#bool).
  
* During [DocumentBase.import_node()](../../../aspose.words/documentbase/import_node/#node_bool)
  Id shall be retained if import does not cause conflicts with other structured document tag Ids in
  the target document.
  
* If multiple structured document tag nodes specify the same decimal number value for the Id attribute,
  then the first structured document tag in the document shall maintain this original Id,
  and all subsequent structured document tag nodes shall have new identifiers assigned to them when the document is loaded.
  
* During standalone structured document tag Aspose.Words.Markup.StructuredDocumentTag.Clone(System.Boolean,Aspose.Words.INodeCloningListener) operation new unique ID will be
  generated for the cloned structured document tag node.
  
* If Id is not specified in the source document, then the structured document tag node shall have a new unique identifier assigned
  to it when the document is loaded.
  





### Examples

Shows how to get the properties of multi-section structured document tags.

```python
doc = aw.Document(file_name=MY_DIR + 'Multi-section structured document tags.docx')
range_start_tag = doc.get_child_nodes(aw.NodeType.STRUCTURED_DOCUMENT_TAG_RANGE_START, True)[0].as_structured_document_tag_range_start()
range_end_tag = doc.get_child_nodes(aw.NodeType.STRUCTURED_DOCUMENT_TAG_RANGE_END, True)[0].as_structured_document_tag_range_end()
print('StructuredDocumentTagRangeStart values:')
print(f'\t|Id: {range_start_tag.id}')
print(f'\t|Title: {range_start_tag.title}')
print(f'\t|PlaceholderName: {range_start_tag.placeholder_name}')
print(f'\t|IsShowingPlaceholderText: {range_start_tag.is_showing_placeholder_text}')
print(f'\t|LockContentControl: {range_start_tag.lock_content_control}')
print(f'\t|LockContents: {range_start_tag.lock_contents}')
print(f'\t|Level: {range_start_tag.level}')
print(f'\t|NodeType: {range_start_tag.node_type}')
print(f'\t|RangeEnd: {range_start_tag.range_end}')
print(f'\t|Color: {range_start_tag.color.to_argb()}')
print(f'\t|SdtType: {range_start_tag.sdt_type}')
print(f'\t|FlatOpcContent: {range_start_tag.word_open_xml}')
print(f'\t|Tag: {range_start_tag.tag}\n')
print('StructuredDocumentTagRangeEnd values:')
print(f'\t|Id: {range_end_tag.id}')
print(f'\t|NodeType: {range_end_tag.node_type}')
```

### See Also

* module [aspose.words.markup](../../)
* class [StructuredDocumentTagRangeStart](../)

