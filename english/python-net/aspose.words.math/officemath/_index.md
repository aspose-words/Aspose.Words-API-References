---
title: OfficeMath class
linktitle: OfficeMath class
articleTitle: OfficeMath class
second_title: Aspose.Words for Python
description: "aspose.words.math.OfficeMath class. Represents an Office Math object such as function, equation, matrix or alike"
type: docs
weight: 20
url: /python-net/aspose.words.math/officemath/
---

## OfficeMath class

Represents an Office Math object such as function, equation, matrix or alike. Can contain child elements
including runs of mathematical text, bookmarks, comments, other [OfficeMath](./) instances and some other nodes.
To learn more, visit the [Working with OfficeMath](https://docs.aspose.com/words/python-net/working-with-officemath/) documentation article.




### Remarks

In this version of Aspose.Words, [OfficeMath](./) nodes do not provide public methods
and properties to create or modify a [OfficeMath](./) object. In this version you are not able to instantiate
[aspose.words.math](../) nodes or modify existing except deleting them.

[OfficeMath](./) can only be a child of [Paragraph](../../aspose.words/paragraph/).




**Inheritance:** [OfficeMath](./) → [CompositeNode](../../aspose.words/compositenode/) → [Node](../../aspose.words/node/)

### Properties

| Name | Description |
| --- | --- |
| [count](../../aspose.words/compositenode/count/) | Gets the number of immediate children of this node.<br>(Inherited from [CompositeNode](../../aspose.words/compositenode/)) |
| [custom_node_id](../../aspose.words/node/custom_node_id/) | Specifies custom node identifier.<br>(Inherited from [Node](../../aspose.words/node/)) |
| [display_type](./display_type/) | Gets/sets Office Math display format type which represents whether an equation is displayed inline with the text or displayed on its own line. |
| [document](../../aspose.words/node/document/) | Gets the document to which this node belongs.<br>(Inherited from [Node](../../aspose.words/node/)) |
| [first_child](../../aspose.words/compositenode/first_child/) | Gets the first child of the node.<br>(Inherited from [CompositeNode](../../aspose.words/compositenode/)) |
| [has_child_nodes](../../aspose.words/compositenode/has_child_nodes/) | Returns ``True`` if this node has any child nodes.<br>(Inherited from [CompositeNode](../../aspose.words/compositenode/)) |
| [is_composite](../../aspose.words/node/is_composite/) | Returns ``True`` if this node can contain other nodes.<br>(Inherited from [Node](../../aspose.words/node/)) |
| [justification](./justification/) | Gets/sets Office Math justification. |
| [last_child](../../aspose.words/compositenode/last_child/) | Gets the last child of the node.<br>(Inherited from [CompositeNode](../../aspose.words/compositenode/)) |
| [math_object_type](./math_object_type/) | Gets type [OfficeMath.math_object_type](./math_object_type/) of this Office Math object. |
| [next_sibling](../../aspose.words/node/next_sibling/) | Gets the node immediately following this node.<br>(Inherited from [Node](../../aspose.words/node/)) |
| [node_type](./node_type/) | Returns [NodeType.OFFICE_MATH](../../aspose.words/nodetype/#OFFICE_MATH). |
| [parent_node](../../aspose.words/node/parent_node/) | Gets the immediate parent of this node.<br>(Inherited from [Node](../../aspose.words/node/)) |
| [parent_paragraph](./parent_paragraph/) | Retrieves the parent [Paragraph](../../aspose.words/paragraph/) of this node. |
| [previous_sibling](../../aspose.words/node/previous_sibling/) | Gets the node immediately preceding this node.<br>(Inherited from [Node](../../aspose.words/node/)) |
| [range](../../aspose.words/node/range/) | Returns a [Range](../../aspose.words/range/) object that represents the portion of a document that is contained in this node.<br>(Inherited from [Node](../../aspose.words/node/)) |

### Methods

| Name | Description |
| --- | --- |
|[ accept(visitor)](./accept/#documentvisitor) | Accepts a visitor. |
|[ accept_end(visitor)](./accept_end/#documentvisitor) | Accepts a visitor for visiting the end of the office math. |
|[ accept_start(visitor)](./accept_start/#documentvisitor) | Accepts a visitor for visiting the start of the office math. |
|[ append_child(new_child)](../../aspose.words/compositenode/append_child/#node) | Adds the specified node to the end of the list of child nodes for this node.<br>(Inherited from [CompositeNode](../../aspose.words/compositenode/)) |
|[ clone(is_clone_children)](../../aspose.words/node/clone/#bool) | Creates a duplicate of the node.<br>(Inherited from [Node](../../aspose.words/node/)) |
|[ get_ancestor(ancestor_type)](../../aspose.words/node/get_ancestor/#object) | Gets the first ancestor of the specified object type.<br>(Inherited from [Node](../../aspose.words/node/)) |
|[ get_ancestor(ancestor_type)](../../aspose.words/node/get_ancestor/#nodetype) | Gets the first ancestor of the specified [NodeType](../../aspose.words/nodetype/).<br>(Inherited from [Node](../../aspose.words/node/)) |
|[ get_child(node_type, index, is_deep)](../../aspose.words/compositenode/get_child/#nodetype_int_bool) | Returns an Nth child node that matches the specified type.<br>(Inherited from [CompositeNode](../../aspose.words/compositenode/)) |
|[ get_child_nodes(node_type, is_deep)](../../aspose.words/compositenode/get_child_nodes/#nodetype_bool) | Returns a live collection of child nodes that match the specified type.<br>(Inherited from [CompositeNode](../../aspose.words/compositenode/)) |
|[ get_math_renderer()](./get_math_renderer/#default) | Creates and returns an object that can be used to render this equation into an image. |
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

### Examples

Shows how to set office math display formatting.

```python
doc = aw.Document(MY_DIR + "Office math.docx")

office_math = doc.get_child(aw.NodeType.OFFICE_MATH, 0, True).as_office_math()

# OfficeMath nodes that are children of other OfficeMath nodes are always inline.
# The node we are working with is the base node to change its location and display type.
self.assertEqual(aw.math.MathObjectType.O_MATH_PARA, office_math.math_object_type)
self.assertEqual(aw.NodeType.OFFICE_MATH, office_math.node_type)
self.assertEqual(office_math.parent_node, office_math.parent_paragraph)

# Change the location and display type of the OfficeMath node.
office_math.display_type = aw.math.OfficeMathDisplayType.DISPLAY
office_math.justification = aw.math.OfficeMathJustification.LEFT

doc.save(ARTIFACTS_DIR + "Shape.office_math.docx")
```

### See Also

* module [aspose.words.math](../)
* class [CompositeNode](../../aspose.words/compositenode/)

