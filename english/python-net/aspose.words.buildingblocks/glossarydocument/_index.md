---
title: GlossaryDocument class
linktitle: GlossaryDocument class
articleTitle: GlossaryDocument class
second_title: Aspose.Words for Python
description: "aspose.words.buildingblocks.GlossaryDocument class. Represents the root element for a glossary document within a Word document"
type: docs
weight: 60
url: /python-net/aspose.words.buildingblocks/glossarydocument/
---

## GlossaryDocument class

Represents the root element for a glossary document within a Word document.
A glossary document is a storage for AutoText, AutoCorrect entries and Building Blocks.
To learn more, visit the [Aspose.Words Document Object Model (DOM)](https://docs.aspose.com/words/python-net/aspose-words-document-object-model/) documentation article.




### Remarks

Some documents, usually templates, can contain AutoText, AutoCorrect entries
and/or Building Blocks (also known as *glossary document entries*, *document parts*
or *building blocks*).

To access building blocks, you need to load a document into a [Document](../../aspose.words/document/)
object. Building blocks will be available via the [Document.glossary_document](../../aspose.words/document/glossary_document/) property.

[GlossaryDocument](./) can contain any number of [BuildingBlock](../buildingblock/) objects.
Each [BuildingBlock](../buildingblock/) represents one document part.

Corresponds to the **glossaryDocument** and **docParts** elements in OOXML.




**Inheritance:** [GlossaryDocument](./) → [DocumentBase](../../aspose.words/documentbase/) → [CompositeNode](../../aspose.words/compositenode/) → [Node](../../aspose.words/node/)

### Constructors
| Name | Description |
| --- | --- |
| [GlossaryDocument()](./__init__/#default) | The default constructor. |

### Properties

| Name | Description |
| --- | --- |
| [background_shape](../../aspose.words/documentbase/background_shape/) | Gets or sets the background shape of the document. Can be ``None``.<br>(Inherited from [DocumentBase](../../aspose.words/documentbase/)) |
| [building_blocks](./building_blocks/) | Returns a typed collection that represents all building blocks in the glossary document. |
| [count](../../aspose.words/compositenode/count/) | Gets the number of immediate children of this node.<br>(Inherited from [CompositeNode](../../aspose.words/compositenode/)) |
| [custom_node_id](../../aspose.words/node/custom_node_id/) | Specifies custom node identifier.<br>(Inherited from [Node](../../aspose.words/node/)) |
| [document](../../aspose.words/node/document/) | Gets the document to which this node belongs.<br>(Inherited from [Node](../../aspose.words/node/)) |
| [first_building_block](./first_building_block/) | Gets the first building block in the glossary document. |
| [first_child](../../aspose.words/compositenode/first_child/) | Gets the first child of the node.<br>(Inherited from [CompositeNode](../../aspose.words/compositenode/)) |
| [font_infos](../../aspose.words/documentbase/font_infos/) | Provides access to properties of fonts used in this document.<br>(Inherited from [DocumentBase](../../aspose.words/documentbase/)) |
| [has_child_nodes](../../aspose.words/compositenode/has_child_nodes/) | Returns ``True`` if this node has any child nodes.<br>(Inherited from [CompositeNode](../../aspose.words/compositenode/)) |
| [is_composite](../../aspose.words/node/is_composite/) | Returns ``True`` if this node can contain other nodes.<br>(Inherited from [Node](../../aspose.words/node/)) |
| [last_building_block](./last_building_block/) | Gets the last building block in the glossary document. |
| [last_child](../../aspose.words/compositenode/last_child/) | Gets the last child of the node.<br>(Inherited from [CompositeNode](../../aspose.words/compositenode/)) |
| [lists](../../aspose.words/documentbase/lists/) | Provides access to the list formatting used in the document.<br>(Inherited from [DocumentBase](../../aspose.words/documentbase/)) |
| [next_sibling](../../aspose.words/node/next_sibling/) | Gets the node immediately following this node.<br>(Inherited from [Node](../../aspose.words/node/)) |
| [node_changing_callback](../../aspose.words/documentbase/node_changing_callback/) | Called when a node is inserted or removed in the document.<br>(Inherited from [DocumentBase](../../aspose.words/documentbase/)) |
| [node_type](./node_type/) | Returns the [NodeType.GLOSSARY_DOCUMENT](../../aspose.words/nodetype/#GLOSSARY_DOCUMENT) value. |
| [page_color](../../aspose.words/documentbase/page_color/) | Gets or sets the page color of the document. This property is a simpler version of [DocumentBase.background_shape](../../aspose.words/documentbase/background_shape/).<br>(Inherited from [DocumentBase](../../aspose.words/documentbase/)) |
| [parent_node](../../aspose.words/node/parent_node/) | Gets the immediate parent of this node.<br>(Inherited from [Node](../../aspose.words/node/)) |
| [previous_sibling](../../aspose.words/node/previous_sibling/) | Gets the node immediately preceding this node.<br>(Inherited from [Node](../../aspose.words/node/)) |
| [range](../../aspose.words/node/range/) | Returns a [Range](../../aspose.words/range/) object that represents the portion of a document that is contained in this node.<br>(Inherited from [Node](../../aspose.words/node/)) |
| [resource_loading_callback](../../aspose.words/documentbase/resource_loading_callback/) | Allows to control how external resources are loaded.<br>(Inherited from [DocumentBase](../../aspose.words/documentbase/)) |
| [styles](../../aspose.words/documentbase/styles/) | Returns a collection of styles defined in the document.<br>(Inherited from [DocumentBase](../../aspose.words/documentbase/)) |
| [warning_callback](../../aspose.words/documentbase/warning_callback/) | Called during various document processing procedures when an issue is detected that might result in data or formatting fidelity loss.<br>(Inherited from [DocumentBase](../../aspose.words/documentbase/)) |

### Methods

| Name | Description |
| --- | --- |
|[ accept(visitor)](./accept/#documentvisitor) | Accepts a visitor. |
|[ accept_end(visitor)](../../aspose.words/compositenode/accept_end/#documentvisitor) | When implemented in a derived class, calls the VisitXXXEnd method of the specified document visitor.<br>(Inherited from [CompositeNode](../../aspose.words/compositenode/)) |
|[ accept_start(visitor)](../../aspose.words/compositenode/accept_start/#documentvisitor) | When implemented in a derived class, calls the VisitXXXStart method of the specified document visitor.<br>(Inherited from [CompositeNode](../../aspose.words/compositenode/)) |
|[ append_child(new_child)](../../aspose.words/compositenode/append_child/#node) | Adds the specified node to the end of the list of child nodes for this node.<br>(Inherited from [CompositeNode](../../aspose.words/compositenode/)) |
|[ clone(is_clone_children)](../../aspose.words/node/clone/#bool) | Creates a duplicate of the node.<br>(Inherited from [Node](../../aspose.words/node/)) |
|[ get_ancestor(ancestor_type)](../../aspose.words/node/get_ancestor/#object) | Gets the first ancestor of the specified object type.<br>(Inherited from [Node](../../aspose.words/node/)) |
|[ get_ancestor(ancestor_type)](../../aspose.words/node/get_ancestor/#nodetype) | Gets the first ancestor of the specified [NodeType](../../aspose.words/nodetype/).<br>(Inherited from [Node](../../aspose.words/node/)) |
|[ get_building_block(gallery, category, name)](./get_building_block/#buildingblockgallery_str_str) | Finds a building block using the specified gallery, category and name. |
|[ get_child(node_type, index, is_deep)](../../aspose.words/compositenode/get_child/#nodetype_int_bool) | Returns an Nth child node that matches the specified type.<br>(Inherited from [CompositeNode](../../aspose.words/compositenode/)) |
|[ get_child_nodes(node_type, is_deep)](../../aspose.words/compositenode/get_child_nodes/#nodetype_bool) | Returns a live collection of child nodes that match the specified type.<br>(Inherited from [CompositeNode](../../aspose.words/compositenode/)) |
|[ get_text()](../../aspose.words/node/get_text/#default) | Gets the text of this node and of all its children.<br>(Inherited from [Node](../../aspose.words/node/)) |
|[ import_node(src_node, is_import_children)](../../aspose.words/documentbase/import_node/#node_bool) | Imports a node from another document to the current document.<br>(Inherited from [DocumentBase](../../aspose.words/documentbase/)) |
|[ import_node(src_node, is_import_children, import_format_mode)](../../aspose.words/documentbase/import_node/#node_bool_importformatmode) | Imports a node from another document to the current document with an option to control formatting.<br>(Inherited from [DocumentBase](../../aspose.words/documentbase/)) |
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
* class [DocumentBase](../../aspose.words/documentbase/)
* class [Document](../../aspose.words/document/)
* property [Document.glossary_document](../../aspose.words/document/glossary_document/)
* class [BuildingBlock](../buildingblock/)

