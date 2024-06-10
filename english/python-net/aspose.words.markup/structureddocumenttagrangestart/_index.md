---
title: StructuredDocumentTagRangeStart class
linktitle: StructuredDocumentTagRangeStart class
articleTitle: StructuredDocumentTagRangeStart class
second_title: Aspose.Words for Python
description: "aspose.words.markup.StructuredDocumentTagRangeStart class. Represents a start of ranged structured document tag which accepts multi-sections content"
type: docs
weight: 200
url: /python-net/aspose.words.markup/structureddocumenttagrangestart/
---

## StructuredDocumentTagRangeStart class

Represents a start of **ranged** structured document tag which accepts multi-sections content.
See also [StructuredDocumentTagRangeEnd](../structureddocumenttagrangeend/).
To learn more, visit the [Structured Document Tags or Content Control](https://docs.aspose.com/words/python-net/working-with-content-control-sdt/) documentation article.




### Remarks

Can be immediate child of [Body](../../aspose.words/body/) node **only**.



**Inheritance:** [StructuredDocumentTagRangeStart](./) → [Node](../../aspose.words/node/)

**Interfaces:** [IStructuredDocumentTag](../istructureddocumenttag/)

### Constructors
| Name | Description |
| --- | --- |
| [StructuredDocumentTagRangeStart(doc, type)](./__init__/#documentbase_sdttype) | Initializes a new instance of the **Structured document tag range start** class. |

### Properties

| Name | Description |
| --- | --- |
| [appearance](./appearance/) | Gets or sets the appearance of the structured document tag. |
| [color](./color/) | Gets or sets the color of the structured document tag. |
| [custom_node_id](../../aspose.words/node/custom_node_id/) | Specifies custom node identifier.<br>(Inherited from [Node](../../aspose.words/node/)) |
| [document](../../aspose.words/node/document/) | Gets the document to which this node belongs.<br>(Inherited from [Node](../../aspose.words/node/)) |
| [id](./id/) | Specifies a unique read-only persistent numerical Id for this structured document tag. |
| [is_composite](../../aspose.words/node/is_composite/) | Returns ``True`` if this node can contain other nodes.<br>(Inherited from [Node](../../aspose.words/node/)) |
| [is_multi_section](../istructureddocumenttag/is_multi_section/) | Returns true if this instance is a ranged (multi-section) structured document tag.<br>(Inherited from [IStructuredDocumentTag](../istructureddocumenttag/)) |
| [is_showing_placeholder_text](./is_showing_placeholder_text/) | Specifies whether the content of this structured document tag shall be interpreted to contain placeholder text (as opposed to regular text contents within the structured document tag). |
| [last_child](./last_child/) | Gets the last child in the stdContent range. |
| [level](./level/) | Gets the level at which this structured document tag range start occurs in the document tree. |
| [lock_content_control](./lock_content_control/) | When set to ``True``, this property will prohibit a user from deleting this structured document tag. |
| [lock_contents](./lock_contents/) | When set to ``True``, this property will prohibit a user from editing the contents of this structured document tag. |
| [next_sibling](../../aspose.words/node/next_sibling/) | Gets the node immediately following this node.<br>(Inherited from [Node](../../aspose.words/node/)) |
| [node](../istructureddocumenttag/node/) | Returns Node object that implements this interface.<br>(Inherited from [IStructuredDocumentTag](../istructureddocumenttag/)) |
| [node_type](./node_type/) | Returns [NodeType.STRUCTURED_DOCUMENT_TAG_RANGE_START](../../aspose.words/nodetype/#STRUCTURED_DOCUMENT_TAG_RANGE_START). |
| [parent_node](../../aspose.words/node/parent_node/) | Gets the immediate parent of this node.<br>(Inherited from [Node](../../aspose.words/node/)) |
| [placeholder](./placeholder/) | Gets the [BuildingBlock](../../aspose.words.buildingblocks/buildingblock/) containing placeholder text which should be displayed when this structured document tag run contents are empty, the associated mapped XML element is empty as specified via the [StructuredDocumentTagRangeStart.xml_mapping](./xml_mapping/) element or the [StructuredDocumentTagRangeStart.is_showing_placeholder_text](./is_showing_placeholder_text/) element is ``True``. |
| [placeholder_name](./placeholder_name/) | Gets or sets Name of the [BuildingBlock](../../aspose.words.buildingblocks/buildingblock/) containing placeholder text. |
| [previous_sibling](../../aspose.words/node/previous_sibling/) | Gets the node immediately preceding this node.<br>(Inherited from [Node](../../aspose.words/node/)) |
| [range](../../aspose.words/node/range/) | Returns a [Range](../../aspose.words/range/) object that represents the portion of a document that is contained in this node.<br>(Inherited from [Node](../../aspose.words/node/)) |
| [range_end](./range_end/) | Specifies end of range if the [StructuredDocumentTag](../structureddocumenttag/) is a ranged structured document tag. Otherwise returns ``None``. |
| [sdt_type](./sdt_type/) | Gets type of this structured document tag. |
| [tag](./tag/) | Specifies a tag associated with the current structured document tag node. Can not be ``None``. |
| [title](./title/) | Specifies the friendly name associated with this structured document tag. Can not be ``None``. |
| [word_open_xml](./word_open_xml/) | Gets a string that represents the XML contained within the node in the [SaveFormat.FLAT_OPC](../../aspose.words/saveformat/#FLAT_OPC) format. |
| [word_open_xml_minimal](./word_open_xml_minimal/) | Gets a string that represents the XML contained within the node in the [SaveFormat.FLAT_OPC](../../aspose.words/saveformat/#FLAT_OPC) format. |
| [xml_mapping](./xml_mapping/) | Gets an object that represents the mapping of this structured document tag range to XML data in a custom XML part of the current document. |

### Methods

| Name | Description |
| --- | --- |
|[ accept(visitor)](./accept/#documentvisitor) | Accepts a visitor. |
|[ append_child(new_child)](./append_child/#node) | Adds the specified node to the end of the stdContent range. |
|[ clone(is_clone_children)](../../aspose.words/node/clone/#bool) | Creates a duplicate of the node.<br>(Inherited from [Node](../../aspose.words/node/)) |
|[ get_ancestor(ancestor_type)](../../aspose.words/node/get_ancestor/#object) | Gets the first ancestor of the specified object type.<br>(Inherited from [Node](../../aspose.words/node/)) |
|[ get_ancestor(ancestor_type)](../../aspose.words/node/get_ancestor/#nodetype) | Gets the first ancestor of the specified [NodeType](../../aspose.words/nodetype/).<br>(Inherited from [Node](../../aspose.words/node/)) |
|[ get_child_nodes(node_type, is_deep)](./get_child_nodes/#nodetype_bool) | Returns a live collection of child nodes that match the specified types. |
|[ get_text()](../../aspose.words/node/get_text/#default) | Gets the text of this node and of all its children.<br>(Inherited from [Node](../../aspose.words/node/)) |
|[ is_ranged()](../istructureddocumenttag/is_ranged/#default) | Returns true if this instance is a ranged structured document tag.<br>(Inherited from [IStructuredDocumentTag](../istructureddocumenttag/)) |
|[ next_pre_order(root_node)](../../aspose.words/node/next_pre_order/#node) | Gets next node according to the pre-order tree traversal algorithm.<br>(Inherited from [Node](../../aspose.words/node/)) |
|[ node_type_to_string(node_type)](../../aspose.words/node/node_type_to_string/#nodetype) | A utility method that converts a node type enum value into a user friendly string.<br>(Inherited from [Node](../../aspose.words/node/)) |
|[ previous_pre_order(root_node)](../../aspose.words/node/previous_pre_order/#node) | Gets the previous node according to the pre-order tree traversal algorithm.<br>(Inherited from [Node](../../aspose.words/node/)) |
|[ remove()](../../aspose.words/node/remove/#default) | Removes itself from the parent.<br>(Inherited from [Node](../../aspose.words/node/)) |
|[ remove_all_children()](./remove_all_children/#default) | Removes all the nodes between this range start node and the range end node. |
|[ remove_self_only()](./remove_self_only/#default) | Removes this range start and appropriate range end nodes of the structured document tag, but keeps its content inside the document tree. |
|[ structured_document_tag_node()](../istructureddocumenttag/structured_document_tag_node/#default) | Returns Node object that implements this interface.<br>(Inherited from [IStructuredDocumentTag](../istructureddocumenttag/)) |
|[ to_string(save_format)](../../aspose.words/node/to_string/#saveformat) | Exports the content of the node into a string in the specified format.<br>(Inherited from [Node](../../aspose.words/node/)) |
|[ to_string(save_options)](../../aspose.words/node/to_string/#saveoptions) | Exports the content of the node into a string using the specified save options.<br>(Inherited from [Node](../../aspose.words/node/)) |

### Examples

Shows how to get the properties of multi-section structured document tags.

```python
doc = aw.Document(MY_DIR + 'Multi-section structured document tags.docx')
range_start_tag = doc.get_child_nodes(aw.NodeType.STRUCTURED_DOCUMENT_TAG_RANGE_START, True)[0].as_structured_document_tag_range_start()
range_end_tag = doc.get_child_nodes(aw.NodeType.STRUCTURED_DOCUMENT_TAG_RANGE_END, True)[0].as_structured_document_tag_range_end()
print('StructuredDocumentTagRangeStart values:')
print(f'\t|id: {range_start_tag.id}')
print(f'\t|title: {range_start_tag.title}')
print(f'\t|placeholder_name: {range_start_tag.placeholder_name}')
print(f'\t|is_showing_placeholder_text: {range_start_tag.is_showing_placeholder_text}')
print(f'\t|lock_content_control: {range_start_tag.lock_content_control}')
print(f'\t|lock_contents: {range_start_tag.lock_contents}')
print(f'\t|level: {range_start_tag.level}')
print(f'\t|node_type: {range_start_tag.node_type}')
print(f'\t|range_end: {range_start_tag.range_end}')
print(f'\t|color: {range_start_tag.color.to_argb()}')
print(f'\t|sdt_type: {range_start_tag.sdt_type}')
print(f'\t|flat_opc_content: {range_start_tag.word_open_xml}')
print(f'\t|tag: {range_start_tag.tag}\n')
print('StructuredDocumentTagRangeEnd values:')
print(f'\t|id: {range_end_tag.id}')
print(f'\t|node_type: {range_end_tag.node_type}')
```

### See Also

* module [aspose.words.markup](../)
* class [Node](../../aspose.words/node/)
* class [IStructuredDocumentTag](../istructureddocumenttag/)

