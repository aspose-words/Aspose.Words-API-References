---
title: ShapeBase class
second_title: Aspose.Words for Python via .NET API Reference
description: "Base class for objects in the drawing layer, such as an AutoShape, freeform, OLE object, ActiveX control, or picture."
type: docs
weight: 310
url: /python-net/aspose.words.drawing/shapebase/
---

## ShapeBase class

Base class for objects in the drawing layer, such as an AutoShape, freeform, OLE object, ActiveX control, or picture.


This is an abstract class. The two derived classes that you can instantiate
are [Shape](../shape/) and [GroupShape](../groupshape/).

A shape is a node in the document tree.

If the shape is a child of a [Paragraph](../../aspose.words/paragraph/) object, then the shape is said to be "top-level".
Top-level shapes are measured and positioned in points.

A shape can also occur as a child of a [GroupShape](../groupshape/) object when several shapes
are grouped. Child shapes of a group shape are positioned in the coordinate space and units
defined by the [ShapeBase.coord_size](./coord_size/) and [ShapeBase.coord_origin](./coord_origin/) properties of the parent
group shape.

A shape can be positioned inline with text or floating. The positioning method is controlled
using the [ShapeBase.wrap_type](./wrap_type/) property.

When a shape is floating, it is positioned relative to something (e.g the current paragraph,
the margin or the page). The relative positioning of the shape is specified using the
[ShapeBase.relative_horizontal_position](./relative_horizontal_position/) and [ShapeBase.relative_vertical_position](./relative_vertical_position/) properties.

A floating shape be positioned explicitly using the [ShapeBase.left](./left/) and [ShapeBase.top](./top/)
properties or aligned relative to some other object using the [ShapeBase.horizontal_alignment](./horizontal_alignment/)
and [ShapeBase.vertical_alignment](./vertical_alignment/) properties.




**Inheritance:** [ShapeBase](./) → [CompositeNode](../../aspose.words/compositenode/) → [Node](../../aspose.words/node/)

### Properties

| Name | Description |
| --- | --- |
| [allow_overlap](./allow_overlap/) | Gets or sets a value that specifies whether this shape can overlap other shapes. |
| [alternative_text](./alternative_text/) | Defines alternative text to be displayed instead of a graphic. |
| [anchor_locked](./anchor_locked/) | Specifies whether the shape's anchor is locked. |
| [aspect_ratio_locked](./aspect_ratio_locked/) | Specifies whether the shape's aspect ratio is locked. |
| [behind_text](./behind_text/) | Specifies whether the shape is below or above text. |
| [bottom](./bottom/) | Gets the position of the bottom edge of the containing block of the shape. |
| [bounds](./bounds/) | Gets or sets the location and size of the containing block of the shape. |
| [bounds_in_points](./bounds_in_points/) | Gets the location and size of the containing block of the shape in points, relative to the anchor of the topmost shape. |
| [bounds_with_effects](./bounds_with_effects/) | Gets final extent that this shape object has after applying drawing effects. Value is measured in points. |
| [can_have_image](./can_have_image/) | Returns true if the shape type allows the shape to have an image. |
| [child_nodes](../../aspose.words/compositenode/child_nodes/) | Gets all immediate child nodes of this node.<br>(Inherited from [CompositeNode](../../aspose.words/compositenode/)) |
| [coord_origin](./coord_origin/) | The coordinates at the top-left corner of the containing block of this shape. |
| [coord_size](./coord_size/) | The width and height of the coordinate space inside the containing block of this shape. |
| [count](../../aspose.words/compositenode/count/) | Gets the number of immediate children of this node.<br>(Inherited from [CompositeNode](../../aspose.words/compositenode/)) |
| [custom_node_id](../../aspose.words/node/custom_node_id/) | Specifies custom node identifier.<br>(Inherited from [Node](../../aspose.words/node/)) |
| [distance_bottom](./distance_bottom/) | Returns or sets the distance (in points) between the document text and the bottom edge of the shape. |
| [distance_left](./distance_left/) | Returns or sets the distance (in points) between the document text and the left edge of the shape. |
| [distance_right](./distance_right/) | Returns or sets the distance (in points) between the document text and the right edge of the shape. |
| [distance_top](./distance_top/) | Returns or sets the distance (in points) between the document text and the top edge of the shape. |
| [document](../../aspose.words/node/document/) | Gets the document to which this node belongs.<br>(Inherited from [Node](../../aspose.words/node/)) |
| [fill](./fill/) | Gets fill formatting for the shape. |
| [first_child](../../aspose.words/compositenode/first_child/) | Gets the first child of the node.<br>(Inherited from [CompositeNode](../../aspose.words/compositenode/)) |
| [flip_orientation](./flip_orientation/) | Switches the orientation of a shape. |
| [font](./font/) | Provides access to the font formatting of this object. |
| [has_child_nodes](../../aspose.words/compositenode/has_child_nodes/) | Returns true if this node has any child nodes.<br>(Inherited from [CompositeNode](../../aspose.words/compositenode/)) |
| [height](./height/) | Gets or sets the height of the containing block of the shape. |
| [horizontal_alignment](./horizontal_alignment/) | Specifies how the shape is positioned horizontally. |
| [href](./href/) | Gets or sets the full hyperlink address for a shape. |
| [is_composite](../../aspose.words/node/is_composite/) | Returns true if this node can contain other nodes.<br>(Inherited from [Node](../../aspose.words/node/)) |
| [is_decorative](./is_decorative/) | Gets or sets the flag that specifies whether the shape is decorative in the document. |
| [is_delete_revision](./is_delete_revision/) | Returns true if this object was deleted in Microsoft Word while change tracking was enabled. |
| [is_group](./is_group/) | Returns true if this is a group shape. |
| [is_horizontal_rule](./is_horizontal_rule/) | Returns true if this shape is a horizontal rule. |
| [is_image](./is_image/) | Returns true if this shape is an image shape. |
| [is_inline](./is_inline/) | A quick way to determine if this shape is positioned inline with text. |
| [is_insert_revision](./is_insert_revision/) | Returns true if this object was inserted in Microsoft Word while change tracking was enabled. |
| [is_layout_in_cell](./is_layout_in_cell/) | Gets or sets a flag indicating whether the shape is displayed inside a table or outside of it. |
| [is_move_from_revision](./is_move_from_revision/) | Returns **true** if this object was moved (deleted) in Microsoft Word while change tracking was enabled. |
| [is_move_to_revision](./is_move_to_revision/) | Returns **true** if this object was moved (inserted) in Microsoft Word while change tracking was enabled. |
| [is_signature_line](./is_signature_line/) | Indicates that shape is a SignatureLine. |
| [is_top_level](./is_top_level/) | Returns true if this shape is not a child of a group shape. |
| [is_word_art](./is_word_art/) | Returns true if this shape is a WordArt object. |
| [last_child](../../aspose.words/compositenode/last_child/) | Gets the last child of the node.<br>(Inherited from [CompositeNode](../../aspose.words/compositenode/)) |
| [left](./left/) | Gets or sets the position of the left edge of the containing block of the shape. |
| [markup_language](./markup_language/) | Gets MarkupLanguage used for this graphic object. |
| [name](./name/) | Gets or sets the optional shape name. |
| [next_sibling](../../aspose.words/node/next_sibling/) | Gets the node immediately following this node.<br>(Inherited from [Node](../../aspose.words/node/)) |
| [node_type](../../aspose.words/node/node_type/) | Gets the type of this node.<br>(Inherited from [Node](../../aspose.words/node/)) |
| [parent_node](../../aspose.words/node/parent_node/) | Gets the immediate parent of this node.<br>(Inherited from [Node](../../aspose.words/node/)) |
| [parent_paragraph](./parent_paragraph/) | Returns the immediate parent paragraph. |
| [previous_sibling](../../aspose.words/node/previous_sibling/) | Gets the node immediately preceding this node.<br>(Inherited from [Node](../../aspose.words/node/)) |
| [range](../../aspose.words/node/range/) | Returns a **Range** object that represents the portion of a document that is contained in this node.<br>(Inherited from [Node](../../aspose.words/node/)) |
| [relative_horizontal_position](./relative_horizontal_position/) | Specifies relative to what the shape is positioned horizontally. |
| [relative_vertical_position](./relative_vertical_position/) | Specifies relative to what the shape is positioned vertically. |
| [right](./right/) | Gets the position of the right edge of the containing block of the shape. |
| [rotation](./rotation/) | Defines the angle (in degrees) that a shape is rotated. Positive value corresponds to clockwise rotation angle. |
| [screen_tip](./screen_tip/) | Defines the text displayed when the mouse pointer moves over the shape. |
| [shadow_format](./shadow_format/) | Gets shadow formatting for the shape. |
| [shape_type](./shape_type/) | Gets the shape type. |
| [size_in_points](./size_in_points/) | Gets the size of the shape in points. |
| [target](./target/) | Gets or sets the target frame for the shape hyperlink. |
| [title](./title/) | Gets or sets the title (caption) of the current shape object. |
| [top](./top/) | Gets or sets the position of the top edge of the containing block of the shape. |
| [vertical_alignment](./vertical_alignment/) | Specifies how the shape is positioned vertically. |
| [width](./width/) | Gets or sets the width of the containing block of the shape. |
| [wrap_side](./wrap_side/) | Specifies how the text is wrapped around the shape. |
| [wrap_type](./wrap_type/) | Defines whether the shape is inline or floating. For floating shapes defines the wrapping mode for text around the shape. |
| [z_order](./z_order/) | Determines the display order of overlapping shapes. |

### Methods

| Name | Description |
| --- | --- |
|[ accept(visitor)](../../aspose.words/node/accept/#documentvisitor) | Accepts a visitor.<br>(Inherited from [Node](../../aspose.words/node/)) |
|[ adjust_with_effects(source)](./adjust_with_effects/#rectanglef) | Adds to the source rectangle values of the effect extent and returns the final rectangle. |
|[ append_child(new_child)](../../aspose.words/compositenode/append_child/#node) | Adds the specified node to the end of the list of child nodes for this node.<br>(Inherited from [CompositeNode](../../aspose.words/compositenode/)) |
|[ clone(is_clone_children)](../../aspose.words/node/clone/#bool) | Creates a duplicate of the node.<br>(Inherited from [Node](../../aspose.words/node/)) |
|[ fetch_inherited_shape_attr(key)](./fetch_inherited_shape_attr/#int) | Reserved for system use. IShapeAttrSource. |
|[ fetch_shape_attr(key)](./fetch_shape_attr/#int) | Reserved for system use. IShapeAttrSource. |
|[ get_ancestor(ancestor_type)](../../aspose.words/node/get_ancestor/#nodetype) | Gets the first ancestor of the specified [NodeType](../../aspose.words/nodetype/).<br>(Inherited from [Node](../../aspose.words/node/)) |
|[ get_child(node_type, index, is_deep)](../../aspose.words/compositenode/get_child/#nodetype_int_bool) | Returns an Nth child node that matches the specified type.<br>(Inherited from [CompositeNode](../../aspose.words/compositenode/)) |
|[ get_child_nodes(node_type, is_deep)](../../aspose.words/compositenode/get_child_nodes/#nodetype_bool) | Returns a live collection of child nodes that match the specified type.<br>(Inherited from [CompositeNode](../../aspose.words/compositenode/)) |
|[ get_direct_shape_attr(key)](./get_direct_shape_attr/#int) | Reserved for system use. IShapeAttrSource. |
|[ get_shape_renderer()](./get_shape_renderer/#default) | Creates and returns an object that can be used to render this shape into an image. |
|[ get_text()](../../aspose.words/node/get_text/#default) | Gets the text of this node and of all its children.<br>(Inherited from [Node](../../aspose.words/node/)) |
|[ index_of(child)](../../aspose.words/compositenode/index_of/#node) | Returns the index of the specified child node in the child node array.<br>(Inherited from [CompositeNode](../../aspose.words/compositenode/)) |
|[ insert_after(new_child, ref_child)](../../aspose.words/compositenode/insert_after/#node_node) | Inserts the specified node immediately after the specified reference node.<br>(Inherited from [CompositeNode](../../aspose.words/compositenode/)) |
|[ insert_before(new_child, ref_child)](../../aspose.words/compositenode/insert_before/#node_node) | Inserts the specified node immediately before the specified reference node.<br>(Inherited from [CompositeNode](../../aspose.words/compositenode/)) |
|[ local_to_parent(value)](./local_to_parent/#pointf) | Converts a value from the local coordinate space into the coordinate space of the parent shape. |
|[ next_pre_order(root_node)](../../aspose.words/node/next_pre_order/#node) | Gets next node according to the pre-order tree traversal algorithm.<br>(Inherited from [Node](../../aspose.words/node/)) |
|[ node_type_to_string(node_type)](../../aspose.words/node/node_type_to_string/#nodetype) | A utility method that converts a node type enum value into a user friendly string.<br>(Inherited from [Node](../../aspose.words/node/)) |
|[ prepend_child(new_child)](../../aspose.words/compositenode/prepend_child/#node) | Adds the specified node to the beginning of the list of child nodes for this node.<br>(Inherited from [CompositeNode](../../aspose.words/compositenode/)) |
|[ previous_pre_order(root_node)](../../aspose.words/node/previous_pre_order/#node) | Gets the previous node according to the pre-order tree traversal algorithm.<br>(Inherited from [Node](../../aspose.words/node/)) |
|[ remove()](../../aspose.words/node/remove/#default) | Removes itself from the parent.<br>(Inherited from [Node](../../aspose.words/node/)) |
|[ remove_all_children()](../../aspose.words/compositenode/remove_all_children/#default) | Removes all the child nodes of the current node.<br>(Inherited from [CompositeNode](../../aspose.words/compositenode/)) |
|[ remove_child(old_child)](../../aspose.words/compositenode/remove_child/#node) | Removes the specified child node.<br>(Inherited from [CompositeNode](../../aspose.words/compositenode/)) |
|[ remove_shape_attr(key)](./remove_shape_attr/#int) | Reserved for system use. IShapeAttrSource. |
|[ remove_smart_tags()](../../aspose.words/compositenode/remove_smart_tags/#default) | Removes all [SmartTag](../../aspose.words.markup/smarttag/) descendant nodes of the current node.<br>(Inherited from [CompositeNode](../../aspose.words/compositenode/)) |
|[ select_nodes(xpath)](../../aspose.words/compositenode/select_nodes/#str) | Selects a list of nodes matching the XPath expression.<br>(Inherited from [CompositeNode](../../aspose.words/compositenode/)) |
|[ select_single_node(xpath)](../../aspose.words/compositenode/select_single_node/#str) | Selects the first Node that matches the XPath expression.<br>(Inherited from [CompositeNode](../../aspose.words/compositenode/)) |
|[ set_shape_attr(key, value)](./set_shape_attr/#int_object) | Reserved for system use. IShapeAttrSource. |
|[ to_string(save_format)](../../aspose.words/node/to_string/#saveformat) | Exports the content of the node into a string in the specified format.<br>(Inherited from [Node](../../aspose.words/node/)) |
|[ to_string(save_options)](../../aspose.words/node/to_string/#saveoptions) | Exports the content of the node into a string using the specified save options.<br>(Inherited from [Node](../../aspose.words/node/)) |

### Examples

Shows how to insert a floating image to the center of a page.

```python
doc = aw.Document()
builder = aw.DocumentBuilder(doc)

# Insert a floating image that will appear behind the overlapping text and align it to the page's center.
shape = builder.insert_image(IMAGE_DIR + "Logo.jpg")
shape.wrap_type = aw.drawing.WrapType.NONE
shape.behind_text = True
shape.relative_horizontal_position = aw.drawing.RelativeHorizontalPosition.PAGE
shape.relative_vertical_position = aw.drawing.RelativeVerticalPosition.PAGE
shape.horizontal_alignment = aw.drawing.HorizontalAlignment.CENTER
shape.vertical_alignment = aw.drawing.VerticalAlignment.CENTER

doc.save(ARTIFACTS_DIR + "Image.create_floating_page_center.docx")
```

### See Also

* module [aspose.words.drawing](../)
* class [CompositeNode](../../aspose.words/compositenode/)
* class [Shape](../shape/)
* class [GroupShape](../groupshape/)

