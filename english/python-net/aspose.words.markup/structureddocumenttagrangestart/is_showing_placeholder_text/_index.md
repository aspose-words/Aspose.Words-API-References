---
title: is_showing_placeholder_text property
second_title: Aspose.Words for Python via .NET API Reference
description: "Specifies whether the content of this structured document tag shall be interpreted to contain placeholder text (as opposed to regular text contents within the structured document tag)."
type: docs
weight: 50
url: /python-net/aspose.words.markup/structureddocumenttagrangestart/is_showing_placeholder_text/
---

## StructuredDocumentTagRangeStart.is_showing_placeholder_text property

Specifies whether the content of this structured document tag shall be interpreted to contain
placeholder text (as opposed to regular text contents within the structured document tag).

if set to true, this state shall be resumed (showing placeholder text) upon opening this document.




### Examples

Shows how to get the properties of multi-section structured document tags.

```python
doc = aw.Document(MY_DIR + "Multi-section structured document tags.docx")

range_start_tag = doc.get_child_nodes(aw.NodeType.STRUCTURED_DOCUMENT_TAG_RANGE_START, True)[0].as_structured_document_tag_range_start()
range_end_tag = doc.get_child_nodes(aw.NodeType.STRUCTURED_DOCUMENT_TAG_RANGE_END, True)[0].as_structured_document_tag_range_end()


print("StructuredDocumentTagRangeStart values:")
print(f"\t|id: {range_start_tag.id}")
print(f"\t|title: {range_start_tag.title}")
print(f"\t|placeholder_name: {range_start_tag.placeholder_name}")
print(f"\t|is_showing_placeholder_text: {range_start_tag.is_showing_placeholder_text}")
print(f"\t|lock_content_control: {range_start_tag.lock_content_control}")
print(f"\t|lock_contents: {range_start_tag.lock_contents}")
print(f"\t|level: {range_start_tag.level}")
print(f"\t|node_type: {range_start_tag.node_type}")
print(f"\t|range_end: {range_start_tag.range_end}")
print(f"\t|color: {range_start_tag.color.to_argb()}")
print(f"\t|sdt_type: {range_start_tag.sdt_type}")
print(f"\t|tag: {range_start_tag.tag}\n")

print("StructuredDocumentTagRangeEnd values:")
print(f"\t|id: {range_end_tag.id}")
print(f"\t|node_type: {range_end_tag.node_type}")
```

### See Also

* module [aspose.words.markup](../../)
* class [StructuredDocumentTagRangeStart](../)

