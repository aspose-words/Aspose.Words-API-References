---
title: StructuredDocumentTag class
second_title: Aspose.Words for Python via .NET API Reference
description: "Represents a structured document tag (SDT or content control) in a document"
type: docs
weight: 170
url: /python-net/aspose.words.markup/structureddocumenttag/
---

## StructuredDocumentTag class

Represents a structured document tag (SDT or content control) in a document.
To learn more, visit the [Structured Document Tags or Content Control](https://docs.aspose.com/words/python-net/working-with-content-control-sdt/) documentation article.




Structured document tags (SDTs) allow to embed customer-defined semantics as well as its
behavior and appearance into a document.

In this version Aspose.Words provides a number of public methods and properties to
manipulate the behavior and content of [StructuredDocumentTag](./).
Mapping of SDT nodes to custom XML packages within a document can be performed with using
the [StructuredDocumentTag.xml_mapping](./xml_mapping/) property.

[StructuredDocumentTag](./) can occur in a document in the following places:


* Block-level - Among paragraphs and tables, as a child of a [Body](../../aspose.words/body/), [HeaderFooter](../../aspose.words/headerfooter/),
  [Comment](../../aspose.words/comment/), [Footnote](../../aspose.words.notes/footnote/) or a [Shape](../../aspose.words.drawing/shape/) node.
  
* Row-level - Among rows in a table, as a child of a [Table](../../aspose.words.tables/table/) node.
  
* Cell-level - Among cells in a table row, as a child of a [Row](../../aspose.words.tables/row/) node.
  
* Inline-level - Among inline content inside, as a child of a [Paragraph](../../aspose.words/paragraph/).
  
* Nested inside another [StructuredDocumentTag](./).
  



**Inheritance:** [StructuredDocumentTag](./) → [CompositeNode](../../aspose.words/compositenode/) → [Node](../../aspose.words/node/)

**Interfaces:** [IStructuredDocumentTag](../istructureddocumenttag/)

### Constructors
| Name | Description |
| --- | --- |
| [StructuredDocumentTag(doc, type, level)](./__init__/#documentbase_sdttype_markuplevel) | Initializes a new instance of the **Structured document tag** class. |

### Properties

| Name | Description |
| --- | --- |
| [appearance](./appearance/) | Gets/sets the appearance of a structured document tag. |
| [building_block_category](./building_block_category/) | Specifies category of building block for this **SDT** node. Can not be ``None``. |
| [building_block_gallery](./building_block_gallery/) | Specifies type of building block for this **SDT**. Can not be ``None``. |
| [calendar_type](./calendar_type/) | Specifies the type of calendar for this **SDT**. Default is [SdtCalendarType.DEFAULT](../sdtcalendartype/#DEFAULT) |
| [checked](./checked/) | Gets/Sets current state of the Checkbox **SDT**. Default value for this property is ``False``. |
| [child_nodes](../../aspose.words/compositenode/child_nodes/) | Gets all immediate child nodes of this node.<br>(Inherited from [CompositeNode](../../aspose.words/compositenode/)) |
| [color](./color/) | Gets or sets the color of the structured document tag. |
| [contents_font](./contents_font/) | Font formatting that will be applied to text entered into **SDT**. |
| [count](../../aspose.words/compositenode/count/) | Gets the number of immediate children of this node.<br>(Inherited from [CompositeNode](../../aspose.words/compositenode/)) |
| [custom_node_id](../../aspose.words/node/custom_node_id/) | Specifies custom node identifier.<br>(Inherited from [Node](../../aspose.words/node/)) |
| [date_display_format](./date_display_format/) | String that represents the format in which dates are displayed. Can not be ``None``. |
| [date_display_locale](./date_display_locale/) | Allows to set/get the language format for the date displayed in this **SDT**. |
| [date_storage_format](./date_storage_format/) | Gets/sets format in which the date for a date SDT is stored when the **SDT** is bound to an XML node in the document's data store. Default value is [SdtDateStorageFormat.DATE_TIME](../sdtdatestorageformat/#DATE_TIME) |
| [document](../../aspose.words/node/document/) | Gets the document to which this node belongs.<br>(Inherited from [Node](../../aspose.words/node/)) |
| [end_character_font](./end_character_font/) | Font formatting that will be applied to the last character of text entered into **SDT**. |
| [first_child](../../aspose.words/compositenode/first_child/) | Gets the first child of the node.<br>(Inherited from [CompositeNode](../../aspose.words/compositenode/)) |
| [full_date](./full_date/) | Specifies the full date and time last entered into this **SDT**. |
| [has_child_nodes](../../aspose.words/compositenode/has_child_nodes/) | Returns ``True`` if this node has any child nodes.<br>(Inherited from [CompositeNode](../../aspose.words/compositenode/)) |
| [id](./id/) | Specifies a unique read-only persistent numerical Id for this **SDT**. |
| [is_composite](../../aspose.words/node/is_composite/) | Returns ``True`` if this node can contain other nodes.<br>(Inherited from [Node](../../aspose.words/node/)) |
| [is_showing_placeholder_text](./is_showing_placeholder_text/) | Specifies whether the content of this **SDT** shall be interpreted to contain placeholder text (as opposed to regular text contents within the SDT). |
| [is_temporary](./is_temporary/) | Specifies whether this **SDT** shall be removed from the WordProcessingML document when its contents are modified. |
| [last_child](../../aspose.words/compositenode/last_child/) | Gets the last child of the node.<br>(Inherited from [CompositeNode](../../aspose.words/compositenode/)) |
| [level](./level/) | Gets the level at which this **SDT** occurs in the document tree. |
| [list_items](./list_items/) | Gets [SdtListItemCollection](../sdtlistitemcollection/) associated with this **SDT**. |
| [lock_content_control](./lock_content_control/) | When set to ``True``, this property will prohibit a user from deleting this **SDT**. |
| [lock_contents](./lock_contents/) | When set to ``True``, this property will prohibit a user from editing the contents of this **SDT**. |
| [multiline](./multiline/) | Specifies whether this **SDT** allows multiple lines of text. |
| [next_sibling](../../aspose.words/node/next_sibling/) | Gets the node immediately following this node.<br>(Inherited from [Node](../../aspose.words/node/)) |
| [node_type](./node_type/) | Returns [NodeType.STRUCTURED_DOCUMENT_TAG](../../aspose.words/nodetype/#STRUCTURED_DOCUMENT_TAG). |
| [parent_node](../../aspose.words/node/parent_node/) | Gets the immediate parent of this node.<br>(Inherited from [Node](../../aspose.words/node/)) |
| [placeholder](./placeholder/) | Gets the [BuildingBlock](../../aspose.words.buildingblocks/buildingblock/) containing placeholder text which should be displayed when this SDT run contents are empty, the associated mapped XML element is empty as specified via the [StructuredDocumentTag.xml_mapping](./xml_mapping/) element or the [StructuredDocumentTag.is_showing_placeholder_text](./is_showing_placeholder_text/) element is ``True``. |
| [placeholder_name](./placeholder_name/) | Gets or sets Name of the [BuildingBlock](../../aspose.words.buildingblocks/buildingblock/) containing placeholder text. |
| [previous_sibling](../../aspose.words/node/previous_sibling/) | Gets the node immediately preceding this node.<br>(Inherited from [Node](../../aspose.words/node/)) |
| [range](../../aspose.words/node/range/) | Returns a [Range](../../aspose.words/range/) object that represents the portion of a document that is contained in this node.<br>(Inherited from [Node](../../aspose.words/node/)) |
| [sdt_type](./sdt_type/) | Gets type of this **Structured document tag**. |
| [style](./style/) | Gets or sets the Style of the structured document tag. |
| [style_name](./style_name/) | Gets or sets the name of the style applied to the structured document tag. |
| [tag](./tag/) | Specifies a tag associated with the current SDT node. Can not be ``None``. |
| [title](./title/) | Specifies the friendly name associated with this **SDT**. Can not be ``None``. |
| [word_open_xml](./word_open_xml/) | Gets a string that represents the XML contained within the node in the [SaveFormat.FLAT_OPC](../../aspose.words/saveformat/#FLAT_OPC) format. |
| [xml_mapping](./xml_mapping/) | Gets an object that represents the mapping of this structured document tag to XML data in a custom XML part of the current document. |

### Methods

| Name | Description |
| --- | --- |
|[ accept(visitor)](./accept/#documentvisitor) | Accepts a visitor. |
|[ append_child(new_child)](../../aspose.words/compositenode/append_child/#node) | Adds the specified node to the end of the list of child nodes for this node.<br>(Inherited from [CompositeNode](../../aspose.words/compositenode/)) |
|[ clear()](./clear/#default) | Clears contents of this structured document tag and displays a placeholder if it is defined. |
|[ clone(is_clone_children)](../../aspose.words/node/clone/#bool) | Creates a duplicate of the node.<br>(Inherited from [Node](../../aspose.words/node/)) |
|[ get_ancestor(ancestor_type)](../../aspose.words/node/get_ancestor/#unknown) | Gets the first ancestor of the specified object type.<br>(Inherited from [Node](../../aspose.words/node/)) |
|[ get_ancestor(ancestor_type)](../../aspose.words/node/get_ancestor/#nodetype) | Gets the first ancestor of the specified [NodeType](../../aspose.words/nodetype/).<br>(Inherited from [Node](../../aspose.words/node/)) |
|[ get_child(node_type, index, is_deep)](../../aspose.words/compositenode/get_child/#nodetype_int_bool) | Returns an Nth child node that matches the specified type.<br>(Inherited from [CompositeNode](../../aspose.words/compositenode/)) |
|[ get_child_nodes(node_type, is_deep)](../../aspose.words/compositenode/get_child_nodes/#nodetype_bool) | Returns a live collection of child nodes that match the specified type.<br>(Inherited from [CompositeNode](../../aspose.words/compositenode/)) |
|[ get_text()](../../aspose.words/node/get_text/#default) | Gets the text of this node and of all its children.<br>(Inherited from [Node](../../aspose.words/node/)) |
|[ index_of(child)](../../aspose.words/compositenode/index_of/#node) | Returns the index of the specified child node in the child node array.<br>(Inherited from [CompositeNode](../../aspose.words/compositenode/)) |
|[ insert_after(new_child, ref_child)](../../aspose.words/compositenode/insert_after/#node_node) | Inserts the specified node immediately after the specified reference node.<br>(Inherited from [CompositeNode](../../aspose.words/compositenode/)) |
|[ insert_before(new_child, ref_child)](../../aspose.words/compositenode/insert_before/#node_node) | Inserts the specified node immediately before the specified reference node.<br>(Inherited from [CompositeNode](../../aspose.words/compositenode/)) |
|[ is_ranged()](../istructureddocumenttag/is_ranged/#default) | Returns true if this instance is a ranged structured document tag.<br>(Inherited from [IStructuredDocumentTag](../istructureddocumenttag/)) |
|[ next_pre_order(root_node)](../../aspose.words/node/next_pre_order/#node) | Gets next node according to the pre-order tree traversal algorithm.<br>(Inherited from [Node](../../aspose.words/node/)) |
|[ node_type_to_string(node_type)](../../aspose.words/node/node_type_to_string/#nodetype) | A utility method that converts a node type enum value into a user friendly string.<br>(Inherited from [Node](../../aspose.words/node/)) |
|[ prepend_child(new_child)](../../aspose.words/compositenode/prepend_child/#node) | Adds the specified node to the beginning of the list of child nodes for this node.<br>(Inherited from [CompositeNode](../../aspose.words/compositenode/)) |
|[ previous_pre_order(root_node)](../../aspose.words/node/previous_pre_order/#node) | Gets the previous node according to the pre-order tree traversal algorithm.<br>(Inherited from [Node](../../aspose.words/node/)) |
|[ remove()](../../aspose.words/node/remove/#default) | Removes itself from the parent.<br>(Inherited from [Node](../../aspose.words/node/)) |
|[ remove_all_children()](../../aspose.words/compositenode/remove_all_children/#default) | Removes all the child nodes of the current node.<br>(Inherited from [CompositeNode](../../aspose.words/compositenode/)) |
|[ remove_child(old_child)](../../aspose.words/compositenode/remove_child/#node) | Removes the specified child node.<br>(Inherited from [CompositeNode](../../aspose.words/compositenode/)) |
|[ remove_self_only()](./remove_self_only/#default) | Removes just this SDT node itself, but keeps the content of it inside the document tree. |
|[ remove_smart_tags()](../../aspose.words/compositenode/remove_smart_tags/#default) | Removes all [SmartTag](../smarttag/) descendant nodes of the current node.<br>(Inherited from [CompositeNode](../../aspose.words/compositenode/)) |
|[ select_nodes(xpath)](../../aspose.words/compositenode/select_nodes/#str) | Selects a list of nodes matching the XPath expression.<br>(Inherited from [CompositeNode](../../aspose.words/compositenode/)) |
|[ select_single_node(xpath)](../../aspose.words/compositenode/select_single_node/#str) | Selects the first [Node](../../aspose.words/node/) that matches the XPath expression.<br>(Inherited from [CompositeNode](../../aspose.words/compositenode/)) |
|[ set_checked_symbol(character_code, font_name)](./set_checked_symbol/#int_str) | Sets the symbol used to represent the checked state of a check box content control. |
|[ set_unchecked_symbol(character_code, font_name)](./set_unchecked_symbol/#int_str) | Sets the symbol used to represent the unchecked state of a check box content control. |
|[ structured_document_tag_node()](../istructureddocumenttag/structured_document_tag_node/#default) | Returns Node object that implements this interface.<br>(Inherited from [IStructuredDocumentTag](../istructureddocumenttag/)) |
|[ to_string(save_format)](../../aspose.words/node/to_string/#saveformat) | Exports the content of the node into a string in the specified format.<br>(Inherited from [Node](../../aspose.words/node/)) |
|[ to_string(save_options)](../../aspose.words/node/to_string/#saveoptions) | Exports the content of the node into a string using the specified save options.<br>(Inherited from [Node](../../aspose.words/node/)) |

### Examples

Shows how to work with styles for content control elements.

```python
doc = aw.Document()
builder = aw.DocumentBuilder(doc)

# Below are two ways to apply a style from the document to a structured document tag.
# 1 -  Apply a style object from the document's style collection:
quote_style = doc.styles.get_by_style_identifier(aw.StyleIdentifier.QUOTE)
sdt_plain_text = aw.markup.StructuredDocumentTag(doc, aw.markup.SdtType.PLAIN_TEXT, aw.markup.MarkupLevel.INLINE)
sdt_plain_text.style = quote_style

# 2 -  Reference a style in the document by name:
sdt_rich_text = aw.markup.StructuredDocumentTag(doc, aw.markup.SdtType.RICH_TEXT, aw.markup.MarkupLevel.INLINE)
sdt_rich_text.style_name = "Quote"

builder.insert_node(sdt_plain_text)
builder.insert_node(sdt_rich_text)

self.assertEqual(aw.NodeType.STRUCTURED_DOCUMENT_TAG, sdt_plain_text.node_type)

tags = doc.get_child_nodes(aw.NodeType.STRUCTURED_DOCUMENT_TAG, True)

for node in tags:
    sdt = node.as_structured_document_tag()

    self.assertEqual(aw.StyleIdentifier.QUOTE, sdt.style.style_identifier)
    self.assertEqual("Quote", sdt.style_name)
```

### See Also

* module [aspose.words.markup](../)
* class [CompositeNode](../../aspose.words/compositenode/)
* class [IStructuredDocumentTag](../istructureddocumenttag/)

