---
title: StructuredDocumentTagRangeStart.placeholder_name property
linktitle: placeholder_name property
articleTitle: placeholder_name property
second_title: Aspose.Words for Python
description: "StructuredDocumentTagRangeStart.placeholder_name property. Gets or sets Name of the [BuildingBlock](../../../aspose.words.buildingblocks/buildingblock/) containing placeholder text."
type: docs
weight: 120
url: /python-net/aspose.words.markup/structureddocumenttagrangestart/placeholder_name/
---

## StructuredDocumentTagRangeStart.placeholder_name property

Gets or sets Name of the [BuildingBlock](../../../aspose.words.buildingblocks/buildingblock/) containing placeholder text.




```python
@property
def placeholder_name(self) -> str:
    ...

@placeholder_name.setter
def placeholder_name(self, value: str):
    ...

```

### Exceptions

| exception | condition |
| --- | --- |
| RuntimeError (Proxy error(InvalidOperationException)) | Throw if BuildingBlock with this name [BuildingBlock.name](../../../aspose.words.buildingblocks/buildingblock/name/) is not present in [Document.glossary_document](../../../aspose.words/document/glossary_document/). |

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

