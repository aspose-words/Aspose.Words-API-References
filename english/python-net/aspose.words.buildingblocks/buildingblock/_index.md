---
title: BuildingBlock class
second_title: Aspose.Words for Python via .NET API Reference
description: "Represents a glossary document entry such as a Building Block, AutoText or an AutoCorrect entry"
type: docs
weight: 10
url: /python-net/aspose.words.buildingblocks/buildingblock/
---

## BuildingBlock class

Represents a glossary document entry such as a Building Block, AutoText or an AutoCorrect entry.
To learn more, visit the [Aspose.Words Document Object Model (DOM)](https://docs.aspose.com/words/net/aspose-words-document-object-model/) documentation article.




[BuildingBlock](./) can contain only [Section](../../aspose.words/section/) nodes.

[BuildingBlock](./) can only be a child of [GlossaryDocument](../glossarydocument/).

You can create new building blocks and insert them into a glossary document.
You can modify or delete existing building blocks. You can copy or move building blocks
between documents. You can insert content of a building block into a document.

Corresponds to the **docPart**, **docPartPr** and **docPartBody** elements in OOXML.




**Inheritance:** [BuildingBlock](./) → [CompositeNode](../../aspose.words/compositenode/) → [Node](../../aspose.words/node/)

### Constructors
| Name | Description |
| --- | --- |
| [BuildingBlock(glossary_doc)](./__init__/#glossarydocument) | Initializes a new instance of this class. |

### Properties

| Name | Description |
| --- | --- |
| [behavior](./behavior/) | Specifies the behavior that shall be applied when the contents of the building block is inserted into the main document. |
| [category](./category/) | Specifies the second-level categorization for the building block. |
| [child_nodes](../../aspose.words/compositenode/child_nodes/) | Gets all immediate child nodes of this node.<br>(Inherited from [CompositeNode](../../aspose.words/compositenode/)) |
| [count](../../aspose.words/compositenode/count/) | Gets the number of immediate children of this node.<br>(Inherited from [CompositeNode](../../aspose.words/compositenode/)) |
| [custom_node_id](../../aspose.words/node/custom_node_id/) | Specifies custom node identifier.<br>(Inherited from [Node](../../aspose.words/node/)) |
| [description](./description/) | Gets or sets the description associated with this building block. |
| [document](../../aspose.words/node/document/) | Gets the document to which this node belongs.<br>(Inherited from [Node](../../aspose.words/node/)) |
| [first_child](../../aspose.words/compositenode/first_child/) | Gets the first child of the node.<br>(Inherited from [CompositeNode](../../aspose.words/compositenode/)) |
| [first_section](./first_section/) | Gets the first section in the building block. |
| [gallery](./gallery/) | Specifies the first-level categorization for the building block for the purposes of  classification or user interface sorting. |
| [guid](./guid/) | Gets or sets an identifier (a 128-bit GUID) that uniquely identifies this building block. |
| [has_child_nodes](../../aspose.words/compositenode/has_child_nodes/) | Returns ``True`` if this node has any child nodes.<br>(Inherited from [CompositeNode](../../aspose.words/compositenode/)) |
| [is_composite](../../aspose.words/node/is_composite/) | Returns ``True`` if this node can contain other nodes.<br>(Inherited from [Node](../../aspose.words/node/)) |
| [last_child](../../aspose.words/compositenode/last_child/) | Gets the last child of the node.<br>(Inherited from [CompositeNode](../../aspose.words/compositenode/)) |
| [last_section](./last_section/) | Gets the last section in the building block. |
| [name](./name/) | Gets or sets the name of this building block. |
| [next_sibling](../../aspose.words/node/next_sibling/) | Gets the node immediately following this node.<br>(Inherited from [Node](../../aspose.words/node/)) |
| [node_type](./node_type/) | Returns the [NodeType.BUILDING_BLOCK](../../aspose.words/nodetype/#BUILDING_BLOCK) value. |
| [parent_node](../../aspose.words/node/parent_node/) | Gets the immediate parent of this node.<br>(Inherited from [Node](../../aspose.words/node/)) |
| [previous_sibling](../../aspose.words/node/previous_sibling/) | Gets the node immediately preceding this node.<br>(Inherited from [Node](../../aspose.words/node/)) |
| [range](../../aspose.words/node/range/) | Returns a [Range](../../aspose.words/range/) object that represents the portion of a document that is contained in this node.<br>(Inherited from [Node](../../aspose.words/node/)) |
| [sections](./sections/) | Returns a collection that represents all sections in the building block. |
| [type](./type/) | Specifies the building block type. |

### Methods

| Name | Description |
| --- | --- |
|[ accept(visitor)](./accept/#documentvisitor) | Accepts a visitor. |
|[ append_child(new_child)](../../aspose.words/compositenode/append_child/#node) | Adds the specified node to the end of the list of child nodes for this node.<br>(Inherited from [CompositeNode](../../aspose.words/compositenode/)) |
|[ clone(is_clone_children)](../../aspose.words/node/clone/#bool) | Creates a duplicate of the node.<br>(Inherited from [Node](../../aspose.words/node/)) |
|[ get_ancestor(ancestor_type)](../../aspose.words/node/get_ancestor/#unknown) | Gets the first ancestor of the specified object type.<br>(Inherited from [Node](../../aspose.words/node/)) |
|[ get_ancestor(ancestor_type)](../../aspose.words/node/get_ancestor/#nodetype) | Gets the first ancestor of the specified [NodeType](../../aspose.words/nodetype/).<br>(Inherited from [Node](../../aspose.words/node/)) |
|[ get_child(node_type, index, is_deep)](../../aspose.words/compositenode/get_child/#nodetype_int_bool) | Returns an Nth child node that matches the specified type.<br>(Inherited from [CompositeNode](../../aspose.words/compositenode/)) |
|[ get_child_nodes(node_type, is_deep)](../../aspose.words/compositenode/get_child_nodes/#nodetype_bool) | Returns a live collection of child nodes that match the specified type.<br>(Inherited from [CompositeNode](../../aspose.words/compositenode/)) |
|[ get_text()](../../aspose.words/node/get_text/#default) | Gets the text of this node and of all its children.<br>(Inherited from [Node](../../aspose.words/node/)) |
|[ index_of(child)](../../aspose.words/compositenode/index_of/#node) | Returns the index of the specified child node in the child node array.<br>(Inherited from [CompositeNode](../../aspose.words/compositenode/)) |
|[ insert_after(new_child, ref_child)](../../aspose.words/compositenode/insert_after/#node_node) | Inserts the specified node immediately after the specified reference node.<br>(Inherited from [CompositeNode](../../aspose.words/compositenode/)) |
|[ insert_before(new_child, ref_child)](../../aspose.words/compositenode/insert_before/#node_node) | Inserts the specified node immediately before the specified reference node.<br>(Inherited from [CompositeNode](../../aspose.words/compositenode/)) |
|[ next_pre_order(root_node)](../../aspose.words/node/next_pre_order/#node) | Gets next node according to the pre-order tree traversal algorithm.<br>(Inherited from [Node](../../aspose.words/node/)) |
|[ node_type_to_string(node_type)](../../aspose.words/node/node_type_to_string/#nodetype) | A utility method that converts a node type enum value into a user friendly string.<br>(Inherited from [Node](../../aspose.words/node/)) |
|[ prepend_child(new_child)](../../aspose.words/compositenode/prepend_child/#node) | Adds the specified node to the beginning of the list of child nodes for this node.<br>(Inherited from [CompositeNode](../../aspose.words/compositenode/)) |
|[ previous_pre_order(root_node)](../../aspose.words/node/previous_pre_order/#node) | Gets the previous node according to the pre-order tree traversal algorithm.<br>(Inherited from [Node](../../aspose.words/node/)) |
|[ remove()](../../aspose.words/node/remove/#default) | Removes itself from the parent.<br>(Inherited from [Node](../../aspose.words/node/)) |
|[ remove_all_children()](../../aspose.words/compositenode/remove_all_children/#default) | Removes all the child nodes of the current node.<br>(Inherited from [CompositeNode](../../aspose.words/compositenode/)) |
|[ remove_child(old_child)](../../aspose.words/compositenode/remove_child/#node) | Removes the specified child node.<br>(Inherited from [CompositeNode](../../aspose.words/compositenode/)) |
|[ remove_smart_tags()](../../aspose.words/compositenode/remove_smart_tags/#default) | Removes all [SmartTag](../../aspose.words.markup/smarttag/) descendant nodes of the current node.<br>(Inherited from [CompositeNode](../../aspose.words/compositenode/)) |
|[ select_nodes(xpath)](../../aspose.words/compositenode/select_nodes/#str) | Selects a list of nodes matching the XPath expression.<br>(Inherited from [CompositeNode](../../aspose.words/compositenode/)) |
|[ select_single_node(xpath)](../../aspose.words/compositenode/select_single_node/#str) | Selects the first [Node](../../aspose.words/node/) that matches the XPath expression.<br>(Inherited from [CompositeNode](../../aspose.words/compositenode/)) |
|[ to_string(save_format)](../../aspose.words/node/to_string/#saveformat) | Exports the content of the node into a string in the specified format.<br>(Inherited from [Node](../../aspose.words/node/)) |
|[ to_string(save_options)](../../aspose.words/node/to_string/#saveoptions) | Exports the content of the node into a string using the specified save options.<br>(Inherited from [Node](../../aspose.words/node/)) |

### See Also

* module [aspose.words.buildingblocks](../)
* class [CompositeNode](../../aspose.words/compositenode/)
* class [GlossaryDocument](../glossarydocument/)

