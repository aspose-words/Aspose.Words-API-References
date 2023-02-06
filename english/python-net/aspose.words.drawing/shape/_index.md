---
title: Shape class
second_title: Aspose.Words for Python via .NET API Reference
description: "Represents an object in the drawing layer, such as an AutoShape, textbox, freeform, OLE object, ActiveX control, or picture"
type: docs
weight: 300
url: /python-net/aspose.words.drawing/shape/
---

## Shape class

Represents an object in the drawing layer, such as an AutoShape, textbox, freeform, OLE object, ActiveX control, or picture.
To learn more, visit the [Working with Shapes](https://docs.aspose.com/words/python-net/working-with-shapes/) documentation article.




Using the [Shape](./) class you can create or modify shapes in a Microsoft Word document.

An important property of a shape is its [ShapeBase.shape_type](../shapebase/shape_type/). Shapes of different
types can have different capabilities in a Word document. For example, only image and OLE shapes
can have images inside them. Most of the shapes can have text, but not all.

Shapes that can have text, can contain [Paragraph](../../aspose.words/paragraph/) and
[Table](../../aspose.words.tables/table/) nodes as children.




**Inheritance:** [Shape](./) → [ShapeBase](../shapebase/) → [CompositeNode](../../aspose.words/compositenode/) → [Node](../../aspose.words/node/)

### Constructors
| Name | Description |
| --- | --- |
| [Shape(doc, shape_type)](./__init__/#documentbase_shapetype) | Creates a new shape object. |

### Properties

| Name | Description |
| --- | --- |
| [allow_overlap](../shapebase/allow_overlap/) | Gets or sets a value that specifies whether this shape can overlap other shapes.<br>(Inherited from [ShapeBase](../shapebase/)) |
| [alternative_text](../shapebase/alternative_text/) | Defines alternative text to be displayed instead of a graphic.<br>(Inherited from [ShapeBase](../shapebase/)) |
| [anchor_locked](../shapebase/anchor_locked/) | Specifies whether the shape's anchor is locked.<br>(Inherited from [ShapeBase](../shapebase/)) |
| [aspect_ratio_locked](../shapebase/aspect_ratio_locked/) | Specifies whether the shape's aspect ratio is locked.<br>(Inherited from [ShapeBase](../shapebase/)) |
| [behind_text](../shapebase/behind_text/) | Specifies whether the shape is below or above text.<br>(Inherited from [ShapeBase](../shapebase/)) |
| [bottom](../shapebase/bottom/) | Gets the position of the bottom edge of the containing block of the shape.<br>(Inherited from [ShapeBase](../shapebase/)) |
| [bounds](../shapebase/bounds/) | Gets or sets the location and size of the containing block of the shape.<br>(Inherited from [ShapeBase](../shapebase/)) |
| [bounds_in_points](../shapebase/bounds_in_points/) | Gets the location and size of the containing block of the shape in points, relative to the anchor of the topmost shape.<br>(Inherited from [ShapeBase](../shapebase/)) |
| [bounds_with_effects](../shapebase/bounds_with_effects/) | Gets final extent that this shape object has after applying drawing effects. Value is measured in points.<br>(Inherited from [ShapeBase](../shapebase/)) |
| [can_have_image](../shapebase/can_have_image/) | Returns ``True`` if the shape type allows the shape to have an image.<br>(Inherited from [ShapeBase](../shapebase/)) |
| [chart](./chart/) | Provides access to the chart properties if this shape has a [Chart](../../aspose.words.drawing.charts/chart/). |
| [child_nodes](../../aspose.words/compositenode/child_nodes/) | Gets all immediate child nodes of this node.<br>(Inherited from [CompositeNode](../../aspose.words/compositenode/)) |
| [coord_origin](../shapebase/coord_origin/) | The coordinates at the top-left corner of the containing block of this shape.<br>(Inherited from [ShapeBase](../shapebase/)) |
| [coord_size](../shapebase/coord_size/) | The width and height of the coordinate space inside the containing block of this shape.<br>(Inherited from [ShapeBase](../shapebase/)) |
| [count](../../aspose.words/compositenode/count/) | Gets the number of immediate children of this node.<br>(Inherited from [CompositeNode](../../aspose.words/compositenode/)) |
| [custom_node_id](../../aspose.words/node/custom_node_id/) | Specifies custom node identifier.<br>(Inherited from [Node](../../aspose.words/node/)) |
| [distance_bottom](../shapebase/distance_bottom/) | Returns or sets the distance (in points) between the document text and the bottom edge of the shape.<br>(Inherited from [ShapeBase](../shapebase/)) |
| [distance_left](../shapebase/distance_left/) | Returns or sets the distance (in points) between the document text and the left edge of the shape.<br>(Inherited from [ShapeBase](../shapebase/)) |
| [distance_right](../shapebase/distance_right/) | Returns or sets the distance (in points) between the document text and the right edge of the shape.<br>(Inherited from [ShapeBase](../shapebase/)) |
| [distance_top](../shapebase/distance_top/) | Returns or sets the distance (in points) between the document text and the top edge of the shape.<br>(Inherited from [ShapeBase](../shapebase/)) |
| [document](../../aspose.words/node/document/) | Gets the document to which this node belongs.<br>(Inherited from [Node](../../aspose.words/node/)) |
| [extrusion_enabled](./extrusion_enabled/) | Returns ``True`` if an extrusion effect is enabled. |
| [fill](../shapebase/fill/) | Gets fill formatting for the shape.<br>(Inherited from [ShapeBase](../shapebase/)) |
| [fill_color](./fill_color/) | Defines the brush color that fills the closed path of the shape. |
| [filled](./filled/) | Determines whether the closed path of the shape will be filled. |
| [first_child](../../aspose.words/compositenode/first_child/) | Gets the first child of the node.<br>(Inherited from [CompositeNode](../../aspose.words/compositenode/)) |
| [first_paragraph](./first_paragraph/) | Gets the first paragraph in the shape. |
| [flip_orientation](../shapebase/flip_orientation/) | Switches the orientation of a shape.<br>(Inherited from [ShapeBase](../shapebase/)) |
| [font](../shapebase/font/) | Provides access to the font formatting of this object.<br>(Inherited from [ShapeBase](../shapebase/)) |
| [has_chart](./has_chart/) | Returns ``True`` if this [Shape](./) has a [Chart](../../aspose.words.drawing.charts/chart/). |
| [has_child_nodes](../../aspose.words/compositenode/has_child_nodes/) | Returns ``True`` if this node has any child nodes.<br>(Inherited from [CompositeNode](../../aspose.words/compositenode/)) |
| [has_image](./has_image/) | Returns ``True`` if the shape has image bytes or links an image. |
| [has_smart_art](./has_smart_art/) | Returns ``True`` if this [Shape](./) has a SmartArt object. |
| [height](../shapebase/height/) | Gets or sets the height of the containing block of the shape.<br>(Inherited from [ShapeBase](../shapebase/)) |
| [horizontal_alignment](../shapebase/horizontal_alignment/) | Specifies how the shape is positioned horizontally.<br>(Inherited from [ShapeBase](../shapebase/)) |
| [horizontal_rule_format](./horizontal_rule_format/) | Provides access to the properties of the horizontal rule shape. For a shape that is not a horizontal rule, returns ``None``. |
| [href](../shapebase/href/) | Gets or sets the full hyperlink address for a shape.<br>(Inherited from [ShapeBase](../shapebase/)) |
| [image_data](./image_data/) | Provides access to the image of the shape. Returns ``None`` if the shape cannot have an image. |
| [is_composite](../../aspose.words/node/is_composite/) | Returns ``True`` if this node can contain other nodes.<br>(Inherited from [Node](../../aspose.words/node/)) |
| [is_decorative](../shapebase/is_decorative/) | Gets or sets the flag that specifies whether the shape is decorative in the document.<br>(Inherited from [ShapeBase](../shapebase/)) |
| [is_delete_revision](../shapebase/is_delete_revision/) | Returns true if this object was deleted in Microsoft Word while change tracking was enabled.<br>(Inherited from [ShapeBase](../shapebase/)) |
| [is_group](../shapebase/is_group/) | Returns ``True`` if this is a group shape.<br>(Inherited from [ShapeBase](../shapebase/)) |
| [is_horizontal_rule](../shapebase/is_horizontal_rule/) | Returns ``True`` if this shape is a horizontal rule.<br>(Inherited from [ShapeBase](../shapebase/)) |
| [is_image](../shapebase/is_image/) | Returns ``True`` if this shape is an image shape.<br>(Inherited from [ShapeBase](../shapebase/)) |
| [is_inline](../shapebase/is_inline/) | A quick way to determine if this shape is positioned inline with text.<br>(Inherited from [ShapeBase](../shapebase/)) |
| [is_insert_revision](../shapebase/is_insert_revision/) | Returns true if this object was inserted in Microsoft Word while change tracking was enabled.<br>(Inherited from [ShapeBase](../shapebase/)) |
| [is_layout_in_cell](../shapebase/is_layout_in_cell/) | Gets or sets a flag indicating whether the shape is displayed inside a table or outside of it.<br>(Inherited from [ShapeBase](../shapebase/)) |
| [is_move_from_revision](../shapebase/is_move_from_revision/) | Returns ``True`` if this object was moved (deleted) in Microsoft Word while change tracking was enabled.<br>(Inherited from [ShapeBase](../shapebase/)) |
| [is_move_to_revision](../shapebase/is_move_to_revision/) | Returns ``True`` if this object was moved (inserted) in Microsoft Word while change tracking was enabled.<br>(Inherited from [ShapeBase](../shapebase/)) |
| [is_signature_line](../shapebase/is_signature_line/) | Indicates that shape is a [SignatureLine](../signatureline/).<br>(Inherited from [ShapeBase](../shapebase/)) |
| [is_top_level](../shapebase/is_top_level/) | Returns ``True`` if this shape is not a child of a group shape.<br>(Inherited from [ShapeBase](../shapebase/)) |
| [is_word_art](../shapebase/is_word_art/) | Returns ``True`` if this shape is a WordArt object.<br>(Inherited from [ShapeBase](../shapebase/)) |
| [last_child](../../aspose.words/compositenode/last_child/) | Gets the last child of the node.<br>(Inherited from [CompositeNode](../../aspose.words/compositenode/)) |
| [last_paragraph](./last_paragraph/) | Gets the last paragraph in the shape. |
| [left](../shapebase/left/) | Gets or sets the position of the left edge of the containing block of the shape.<br>(Inherited from [ShapeBase](../shapebase/)) |
| [markup_language](../shapebase/markup_language/) | Gets MarkupLanguage used for this graphic object.<br>(Inherited from [ShapeBase](../shapebase/)) |
| [name](../shapebase/name/) | Gets or sets the optional shape name.<br>(Inherited from [ShapeBase](../shapebase/)) |
| [next_sibling](../../aspose.words/node/next_sibling/) | Gets the node immediately following this node.<br>(Inherited from [Node](../../aspose.words/node/)) |
| [node_type](./node_type/) | Returns [NodeType.SHAPE](../../aspose.words/nodetype/#SHAPE). |
| [ole_format](./ole_format/) | Provides access to the OLE data of a shape. For a shape that is not an OLE object or ActiveX control, returns ``None``. |
| [parent_node](../../aspose.words/node/parent_node/) | Gets the immediate parent of this node.<br>(Inherited from [Node](../../aspose.words/node/)) |
| [parent_paragraph](../shapebase/parent_paragraph/) | Returns the immediate parent paragraph.<br>(Inherited from [ShapeBase](../shapebase/)) |
| [previous_sibling](../../aspose.words/node/previous_sibling/) | Gets the node immediately preceding this node.<br>(Inherited from [Node](../../aspose.words/node/)) |
| [range](../../aspose.words/node/range/) | Returns a [Range](../../aspose.words/range/) object that represents the portion of a document that is contained in this node.<br>(Inherited from [Node](../../aspose.words/node/)) |
| [relative_horizontal_position](../shapebase/relative_horizontal_position/) | Specifies relative to what the shape is positioned horizontally.<br>(Inherited from [ShapeBase](../shapebase/)) |
| [relative_vertical_position](../shapebase/relative_vertical_position/) | Specifies relative to what the shape is positioned vertically.<br>(Inherited from [ShapeBase](../shapebase/)) |
| [right](../shapebase/right/) | Gets the position of the right edge of the containing block of the shape.<br>(Inherited from [ShapeBase](../shapebase/)) |
| [rotation](../shapebase/rotation/) | Defines the angle (in degrees) that a shape is rotated. Positive value corresponds to clockwise rotation angle.<br>(Inherited from [ShapeBase](../shapebase/)) |
| [screen_tip](../shapebase/screen_tip/) | Defines the text displayed when the mouse pointer moves over the shape.<br>(Inherited from [ShapeBase](../shapebase/)) |
| [shadow_enabled](./shadow_enabled/) | Returns ``True`` if a shadow effect is enabled. |
| [shadow_format](../shapebase/shadow_format/) | Gets shadow formatting for the shape.<br>(Inherited from [ShapeBase](../shapebase/)) |
| [shape_type](../shapebase/shape_type/) | Gets the shape type.<br>(Inherited from [ShapeBase](../shapebase/)) |
| [signature_line](./signature_line/) | Gets [SignatureLine](../signatureline/) object if the shape is a signature line. Returns ``None`` otherwise. |
| [size_in_points](../shapebase/size_in_points/) | Gets the size of the shape in points.<br>(Inherited from [ShapeBase](../shapebase/)) |
| [story_type](./story_type/) | Returns [StoryType.TEXTBOX](../../aspose.words/storytype/#TEXTBOX). |
| [stroke](./stroke/) | Defines a stroke for a shape. |
| [stroke_color](./stroke_color/) | Defines the color of a stroke. |
| [stroke_weight](./stroke_weight/) | Defines the brush thickness that strokes the path of a shape in points. |
| [stroked](./stroked/) | Defines whether the path will be stroked. |
| [target](../shapebase/target/) | Gets or sets the target frame for the shape hyperlink.<br>(Inherited from [ShapeBase](../shapebase/)) |
| [text_box](./text_box/) | Defines attributes that specify how text is displayed in a shape. |
| [text_path](./text_path/) | Defines the text of the text path (of a WordArt object). |
| [title](../shapebase/title/) | Gets or sets the title (caption) of the current shape object.<br>(Inherited from [ShapeBase](../shapebase/)) |
| [top](../shapebase/top/) | Gets or sets the position of the top edge of the containing block of the shape.<br>(Inherited from [ShapeBase](../shapebase/)) |
| [vertical_alignment](../shapebase/vertical_alignment/) | Specifies how the shape is positioned vertically.<br>(Inherited from [ShapeBase](../shapebase/)) |
| [width](../shapebase/width/) | Gets or sets the width of the containing block of the shape.<br>(Inherited from [ShapeBase](../shapebase/)) |
| [wrap_side](../shapebase/wrap_side/) | Specifies how the text is wrapped around the shape.<br>(Inherited from [ShapeBase](../shapebase/)) |
| [wrap_type](../shapebase/wrap_type/) | Defines whether the shape is inline or floating. For floating shapes defines the wrapping mode for text around the shape.<br>(Inherited from [ShapeBase](../shapebase/)) |
| [z_order](../shapebase/z_order/) | Determines the display order of overlapping shapes.<br>(Inherited from [ShapeBase](../shapebase/)) |

### Methods

| Name | Description |
| --- | --- |
|[ accept(visitor)](./accept/#documentvisitor) | Accepts a visitor. |
|[ adjust_with_effects(source)](../shapebase/adjust_with_effects/#rectanglef) | Adds to the source rectangle values of the effect extent and returns the final rectangle.<br>(Inherited from [ShapeBase](../shapebase/)) |
|[ append_child(new_child)](../../aspose.words/compositenode/append_child/#node) | Adds the specified node to the end of the list of child nodes for this node.<br>(Inherited from [CompositeNode](../../aspose.words/compositenode/)) |
|[ clone(is_clone_children)](../../aspose.words/node/clone/#bool) | Creates a duplicate of the node.<br>(Inherited from [Node](../../aspose.words/node/)) |
|[ fetch_inherited_shape_attr(key)](../shapebase/fetch_inherited_shape_attr/#int) | Reserved for system use. IShapeAttrSource.<br>(Inherited from [ShapeBase](../shapebase/)) |
|[ fetch_shape_attr(key)](../shapebase/fetch_shape_attr/#int) | Reserved for system use. IShapeAttrSource.<br>(Inherited from [ShapeBase](../shapebase/)) |
|[ get_ancestor(ancestor_type)](../../aspose.words/node/get_ancestor/#unknown) | Gets the first ancestor of the specified object type.<br>(Inherited from [Node](../../aspose.words/node/)) |
|[ get_ancestor(ancestor_type)](../../aspose.words/node/get_ancestor/#nodetype) | Gets the first ancestor of the specified [NodeType](../../aspose.words/nodetype/).<br>(Inherited from [Node](../../aspose.words/node/)) |
|[ get_child(node_type, index, is_deep)](../../aspose.words/compositenode/get_child/#nodetype_int_bool) | Returns an Nth child node that matches the specified type.<br>(Inherited from [CompositeNode](../../aspose.words/compositenode/)) |
|[ get_child_nodes(node_type, is_deep)](../../aspose.words/compositenode/get_child_nodes/#nodetype_bool) | Returns a live collection of child nodes that match the specified type.<br>(Inherited from [CompositeNode](../../aspose.words/compositenode/)) |
|[ get_direct_shape_attr(key)](../shapebase/get_direct_shape_attr/#int) | Reserved for system use. IShapeAttrSource.<br>(Inherited from [ShapeBase](../shapebase/)) |
|[ get_shape_renderer()](../shapebase/get_shape_renderer/#default) | Creates and returns an object that can be used to render this shape into an image.<br>(Inherited from [ShapeBase](../shapebase/)) |
|[ get_text()](../../aspose.words/node/get_text/#default) | Gets the text of this node and of all its children.<br>(Inherited from [Node](../../aspose.words/node/)) |
|[ index_of(child)](../../aspose.words/compositenode/index_of/#node) | Returns the index of the specified child node in the child node array.<br>(Inherited from [CompositeNode](../../aspose.words/compositenode/)) |
|[ insert_after(new_child, ref_child)](../../aspose.words/compositenode/insert_after/#node_node) | Inserts the specified node immediately after the specified reference node.<br>(Inherited from [CompositeNode](../../aspose.words/compositenode/)) |
|[ insert_before(new_child, ref_child)](../../aspose.words/compositenode/insert_before/#node_node) | Inserts the specified node immediately before the specified reference node.<br>(Inherited from [CompositeNode](../../aspose.words/compositenode/)) |
|[ local_to_parent(value)](../shapebase/local_to_parent/#pointf) | Converts a value from the local coordinate space into the coordinate space of the parent shape.<br>(Inherited from [ShapeBase](../shapebase/)) |
|[ next_pre_order(root_node)](../../aspose.words/node/next_pre_order/#node) | Gets next node according to the pre-order tree traversal algorithm.<br>(Inherited from [Node](../../aspose.words/node/)) |
|[ node_type_to_string(node_type)](../../aspose.words/node/node_type_to_string/#nodetype) | A utility method that converts a node type enum value into a user friendly string.<br>(Inherited from [Node](../../aspose.words/node/)) |
|[ prepend_child(new_child)](../../aspose.words/compositenode/prepend_child/#node) | Adds the specified node to the beginning of the list of child nodes for this node.<br>(Inherited from [CompositeNode](../../aspose.words/compositenode/)) |
|[ previous_pre_order(root_node)](../../aspose.words/node/previous_pre_order/#node) | Gets the previous node according to the pre-order tree traversal algorithm.<br>(Inherited from [Node](../../aspose.words/node/)) |
|[ remove()](../../aspose.words/node/remove/#default) | Removes itself from the parent.<br>(Inherited from [Node](../../aspose.words/node/)) |
|[ remove_all_children()](../../aspose.words/compositenode/remove_all_children/#default) | Removes all the child nodes of the current node.<br>(Inherited from [CompositeNode](../../aspose.words/compositenode/)) |
|[ remove_child(old_child)](../../aspose.words/compositenode/remove_child/#node) | Removes the specified child node.<br>(Inherited from [CompositeNode](../../aspose.words/compositenode/)) |
|[ remove_shape_attr(key)](../shapebase/remove_shape_attr/#int) | Reserved for system use. IShapeAttrSource.<br>(Inherited from [ShapeBase](../shapebase/)) |
|[ remove_smart_tags()](../../aspose.words/compositenode/remove_smart_tags/#default) | Removes all [SmartTag](../../aspose.words.markup/smarttag/) descendant nodes of the current node.<br>(Inherited from [CompositeNode](../../aspose.words/compositenode/)) |
|[ select_nodes(xpath)](../../aspose.words/compositenode/select_nodes/#str) | Selects a list of nodes matching the XPath expression.<br>(Inherited from [CompositeNode](../../aspose.words/compositenode/)) |
|[ select_single_node(xpath)](../../aspose.words/compositenode/select_single_node/#str) | Selects the first [Node](../../aspose.words/node/) that matches the XPath expression.<br>(Inherited from [CompositeNode](../../aspose.words/compositenode/)) |
|[ set_shape_attr(key, value)](../shapebase/set_shape_attr/#int_object) | Reserved for system use. IShapeAttrSource.<br>(Inherited from [ShapeBase](../shapebase/)) |
|[ to_string(save_format)](../../aspose.words/node/to_string/#saveformat) | Exports the content of the node into a string in the specified format.<br>(Inherited from [Node](../../aspose.words/node/)) |
|[ to_string(save_options)](../../aspose.words/node/to_string/#saveoptions) | Exports the content of the node into a string using the specified save options.<br>(Inherited from [Node](../../aspose.words/node/)) |
|[ update_smart_art_drawing()](./update_smart_art_drawing/#default) | Updates SmartArt pre-rendered drawing by using Aspose.Words's SmartArt cold rendering engine. |

### Examples

Shows how to extract images from a document, and save them to the local file system as individual files.

```python
doc = aw.Document(MY_DIR + "Images.docx")

# Get the collection of shapes from the document,
# and save the image data of every shape with an image as a file to the local file system.
shapes = doc.get_child_nodes(aw.NodeType.SHAPE, True)

self.assertEqual(9, len([s for s in shapes if s.as_shape().has_image]))

image_index = 0
for shape in shapes:
    shape = shape.as_shape()

    if shape.has_image:

        # The image data of shapes may contain images of many possible image formats.
        # We can determine a file extension for each image automatically, based on its format.
        image_file_name = f"File.extract_images.{image_index}{aw.FileFormatUtil.image_type_to_extension(shape.image_data.image_type)}"
        shape.image_data.save(ARTIFACTS_DIR + image_file_name)
        image_index += 1
```

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

Shows how to delete all shapes from a document.

```python
doc = aw.Document()
builder = aw.DocumentBuilder(doc)

# Insert two shapes along with a group shape with another shape inside it.
builder.insert_shape(aw.drawing.ShapeType.RECTANGLE, 400, 200)
builder.insert_shape(aw.drawing.ShapeType.STAR, 300, 300)

group = aw.drawing.GroupShape(doc)
group.bounds = drawing.RectangleF(100, 50, 200, 100)
group.coord_origin = drawing.Point(-1000, -500)

sub_shape = aw.drawing.Shape(doc, aw.drawing.ShapeType.CUBE)
sub_shape.width = 500
sub_shape.height = 700
sub_shape.left = 0
sub_shape.top = 0

group.append_child(sub_shape)
builder.insert_node(group)

self.assertEqual(3, doc.get_child_nodes(aw.NodeType.SHAPE, True).count)
self.assertEqual(1, doc.get_child_nodes(aw.NodeType.GROUP_SHAPE, True).count)

# Remove all Shape nodes from the document.
shapes = doc.get_child_nodes(aw.NodeType.SHAPE, True)
shapes.clear()

# All shapes are gone, but the group shape is still in the document.
self.assertEqual(1, doc.get_child_nodes(aw.NodeType.GROUP_SHAPE, True).count)
self.assertEqual(0, doc.get_child_nodes(aw.NodeType.SHAPE, True).count)

# Remove all group shapes separately.
group_shapes = doc.get_child_nodes(aw.NodeType.GROUP_SHAPE, True)
group_shapes.clear()

self.assertEqual(0, doc.get_child_nodes(aw.NodeType.GROUP_SHAPE, True).count)
self.assertEqual(0, doc.get_child_nodes(aw.NodeType.SHAPE, True).count)
```

### See Also

* module [aspose.words.drawing](../)
* class [ShapeBase](../shapebase/)
* class [GroupShape](../groupshape/)

