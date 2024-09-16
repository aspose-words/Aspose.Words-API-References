---
title: DocumentBase class
linktitle: DocumentBase class
articleTitle: DocumentBase class
second_title: Aspose.Words for Python
description: "aspose.words.DocumentBase class. Provides the abstract base class for a main document and a glossary document of a Word document"
type: docs
weight: 290
url: /python-net/aspose.words/documentbase/
---

## DocumentBase class

Provides the abstract base class for a main document and a glossary document of a Word document.
To learn more, visit the [Aspose.Words Document Object Model (DOM)](https://docs.aspose.com/words/python-net/aspose-words-document-object-model/) documentation article.




### Remarks

Aspose.Words represents a Word document as a tree of nodes. [DocumentBase](./) is a
root node of the tree that contains all other nodes of the document.

[DocumentBase](./) also stores document-wide information such as [DocumentBase.styles](./styles/) and
[DocumentBase.lists](./lists/) that the tree nodes might refer to.




**Inheritance:** [DocumentBase](./) → [CompositeNode](../compositenode/) → [Node](../node/)

### Properties

| Name | Description |
| --- | --- |
| [background_shape](./background_shape/) | Gets or sets the background shape of the document. Can be ``None``. |
| [count](../compositenode/count/) | Gets the number of immediate children of this node.<br>(Inherited from [CompositeNode](../compositenode/)) |
| [custom_node_id](../node/custom_node_id/) | Specifies custom node identifier.<br>(Inherited from [Node](../node/)) |
| [document](./document/) | Gets this instance. |
| [first_child](../compositenode/first_child/) | Gets the first child of the node.<br>(Inherited from [CompositeNode](../compositenode/)) |
| [font_infos](./font_infos/) | Provides access to properties of fonts used in this document. |
| [footnote_separators](./footnote_separators/) | Provides access to the footnote/endnote separators defined in the document. |
| [has_child_nodes](../compositenode/has_child_nodes/) | Returns ``True`` if this node has any child nodes.<br>(Inherited from [CompositeNode](../compositenode/)) |
| [is_composite](../node/is_composite/) | Returns ``True`` if this node can contain other nodes.<br>(Inherited from [Node](../node/)) |
| [last_child](../compositenode/last_child/) | Gets the last child of the node.<br>(Inherited from [CompositeNode](../compositenode/)) |
| [lists](./lists/) | Provides access to the list formatting used in the document. |
| [next_sibling](../node/next_sibling/) | Gets the node immediately following this node.<br>(Inherited from [Node](../node/)) |
| [node_changing_callback](./node_changing_callback/) | Called when a node is inserted or removed in the document. |
| [node_type](../node/node_type/) | Gets the type of this node.<br>(Inherited from [Node](../node/)) |
| [page_color](./page_color/) | Gets or sets the page color of the document. This property is a simpler version of [DocumentBase.background_shape](./background_shape/). |
| [parent_node](../node/parent_node/) | Gets the immediate parent of this node.<br>(Inherited from [Node](../node/)) |
| [previous_sibling](../node/previous_sibling/) | Gets the node immediately preceding this node.<br>(Inherited from [Node](../node/)) |
| [range](../node/range/) | Returns a [Range](../range/) object that represents the portion of a document that is contained in this node.<br>(Inherited from [Node](../node/)) |
| [resource_loading_callback](./resource_loading_callback/) | Allows to control how external resources are loaded. |
| [styles](./styles/) | Returns a collection of styles defined in the document. |
| [warning_callback](./warning_callback/) | Called during various document processing procedures when an issue is detected that might result in data or formatting fidelity loss. |

### Methods

| Name | Description |
| --- | --- |
|[ accept(visitor)](../node/accept/#documentvisitor) | Accepts a visitor.<br>(Inherited from [Node](../node/)) |
|[ accept_end(visitor)](../compositenode/accept_end/#documentvisitor) | When implemented in a derived class, calls the VisitXXXEnd method of the specified document visitor.<br>(Inherited from [CompositeNode](../compositenode/)) |
|[ accept_start(visitor)](../compositenode/accept_start/#documentvisitor) | When implemented in a derived class, calls the VisitXXXStart method of the specified document visitor.<br>(Inherited from [CompositeNode](../compositenode/)) |
|[ append_child(new_child)](../compositenode/append_child/#node) | Adds the specified node to the end of the list of child nodes for this node.<br>(Inherited from [CompositeNode](../compositenode/)) |
|[ clone(is_clone_children)](../node/clone/#bool) | Creates a duplicate of the node.<br>(Inherited from [Node](../node/)) |
|[ get_ancestor(ancestor_type)](../node/get_ancestor/#object) | Gets the first ancestor of the specified object type.<br>(Inherited from [Node](../node/)) |
|[ get_ancestor(ancestor_type)](../node/get_ancestor/#nodetype) | Gets the first ancestor of the specified [NodeType](../nodetype/).<br>(Inherited from [Node](../node/)) |
|[ get_child(node_type, index, is_deep)](../compositenode/get_child/#nodetype_int_bool) | Returns an Nth child node that matches the specified type.<br>(Inherited from [CompositeNode](../compositenode/)) |
|[ get_child_nodes(node_type, is_deep)](../compositenode/get_child_nodes/#nodetype_bool) | Returns a live collection of child nodes that match the specified type.<br>(Inherited from [CompositeNode](../compositenode/)) |
|[ get_text()](../node/get_text/#default) | Gets the text of this node and of all its children.<br>(Inherited from [Node](../node/)) |
|[ import_node(src_node, is_import_children)](./import_node/#node_bool) | Imports a node from another document to the current document. |
|[ import_node(src_node, is_import_children, import_format_mode)](./import_node/#node_bool_importformatmode) | Imports a node from another document to the current document with an option to control formatting. |
|[ index_of(child)](../compositenode/index_of/#node) | Returns the index of the specified child node in the child node array.<br>(Inherited from [CompositeNode](../compositenode/)) |
|[ insert_after(new_child, ref_child)](../compositenode/insert_after/#node_node) | Inserts the specified node immediately after the specified reference node.<br>(Inherited from [CompositeNode](../compositenode/)) |
|[ insert_before(new_child, ref_child)](../compositenode/insert_before/#node_node) | Inserts the specified node immediately before the specified reference node.<br>(Inherited from [CompositeNode](../compositenode/)) |
|[ next_pre_order(root_node)](../node/next_pre_order/#node) | Gets next node according to the pre-order tree traversal algorithm.<br>(Inherited from [Node](../node/)) |
|[ node_type_to_string(node_type)](../node/node_type_to_string/#nodetype) | A utility method that converts a node type enum value into a user friendly string.<br>(Inherited from [Node](../node/)) |
|[ prepend_child(new_child)](../compositenode/prepend_child/#node) | Adds the specified node to the beginning of the list of child nodes for this node.<br>(Inherited from [CompositeNode](../compositenode/)) |
|[ previous_pre_order(root_node)](../node/previous_pre_order/#node) | Gets the previous node according to the pre-order tree traversal algorithm.<br>(Inherited from [Node](../node/)) |
|[ remove()](../node/remove/#default) | Removes itself from the parent.<br>(Inherited from [Node](../node/)) |
|[ remove_all_children()](../compositenode/remove_all_children/#default) | Removes all the child nodes of the current node.<br>(Inherited from [CompositeNode](../compositenode/)) |
|[ remove_child(old_child)](../compositenode/remove_child/#node) | Removes the specified child node.<br>(Inherited from [CompositeNode](../compositenode/)) |
|[ remove_smart_tags()](../compositenode/remove_smart_tags/#default) | Removes all [SmartTag](../../aspose.words.markup/smarttag/) descendant nodes of the current node.<br>(Inherited from [CompositeNode](../compositenode/)) |
|[ select_nodes(xpath)](../compositenode/select_nodes/#str) | Selects a list of nodes matching the XPath expression.<br>(Inherited from [CompositeNode](../compositenode/)) |
|[ select_single_node(xpath)](../compositenode/select_single_node/#str) | Selects the first [Node](../node/) that matches the XPath expression.<br>(Inherited from [CompositeNode](../compositenode/)) |
|[ to_string(save_format)](../node/to_string/#saveformat) | Exports the content of the node into a string in the specified format.<br>(Inherited from [Node](../node/)) |
|[ to_string(save_options)](../node/to_string/#saveoptions) | Exports the content of the node into a string using the specified save options.<br>(Inherited from [Node](../node/)) |

### Examples

Shows how to initialize the subclasses of DocumentBase.

```python
doc = aw.Document()
self.assertIsInstance(doc, aw.DocumentBase)
glossary_doc = aw.buildingblocks.GlossaryDocument()
doc.glossary_document = glossary_doc
self.assertIsInstance(glossary_doc, aw.DocumentBase)
```

### See Also

* module [aspose.words](../)
* class [CompositeNode](../compositenode/)
* class [Document](../document/)
* class [DocumentBase](./)

