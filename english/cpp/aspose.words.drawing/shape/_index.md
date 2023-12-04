---
title: Aspose::Words::Drawing::Shape class
linktitle: Shape
second_title: Aspose.Words for C++ API Reference
description: 'Aspose::Words::Drawing::Shape class. Represents an object in the drawing layer, such as an AutoShape, textbox, freeform, OLE object, ActiveX control, or picture. To learn more, visit the  documentation article in C++.'
type: docs
weight: 11000
url: /cpp/aspose.words.drawing/shape/
---
## Shape class


Represents an object in the drawing layer, such as an AutoShape, textbox, freeform, OLE object, ActiveX control, or picture. To learn more, visit the [Working with Shapes](https://docs.aspose.com/words/cpp/working-with-shapes/) documentation article.

```cpp
class Shape : public Aspose::Words::Drawing::ShapeBase,
              public Aspose::Words::Drawing::Core::ITextBox,
              public Aspose::Words::Drawing::Core::IStrokable
```

## Methods

| Method | Description |
| --- | --- |
| [Accept](./accept/)(System::SharedPtr\<Aspose::Words::DocumentVisitor\>) override | Accepts a visitor. |
| [AcceptEnd](./acceptend/)(System::SharedPtr\<Aspose::Words::DocumentVisitor\>) override |  |
| [AcceptStart](./acceptstart/)(System::SharedPtr\<Aspose::Words::DocumentVisitor\>) override |  |
| [AdjustWithEffects](../shapebase/adjustwitheffects/)(System::Drawing::RectangleF) | Adds to the source rectangle values of the effect extent and returns the final rectangle. |
| [AppendChild](../../aspose.words/compositenode/appendchild/)(T) |  |
| [Clone](../../aspose.words/node/clone/)(bool) | Creates a duplicate of the node. |
| [get_AllowOverlap](../shapebase/get_allowoverlap/)() | Gets or sets a value that specifies whether this shape can overlap other shapes. |
| [get_AlternativeText](../shapebase/get_alternativetext/)() | Defines alternative text to be displayed instead of a graphic. |
| [get_AnchorLocked](../shapebase/get_anchorlocked/)() | Specifies whether the shape's anchor is locked. |
| [get_AspectRatioLocked](../shapebase/get_aspectratiolocked/)() | Specifies whether the shape's aspect ratio is locked. |
| [get_BehindText](../shapebase/get_behindtext/)() | Specifies whether the shape is below or above text. |
| [get_Bottom](../shapebase/get_bottom/)() | Gets the position of the bottom edge of the containing block of the shape. |
| [get_Bounds](../shapebase/get_bounds/)() | Gets or sets the location and size of the containing block of the shape. |
| [get_BoundsInPoints](../shapebase/get_boundsinpoints/)() | Gets the location and size of the containing block of the shape in points, relative to the anchor of the topmost shape. |
| [get_BoundsWithEffects](../shapebase/get_boundswitheffects/)() | Gets final extent that this shape object has after applying drawing effects. Value is measured in points. |
| [get_CanHaveImage](../shapebase/get_canhaveimage/)() | Returns **true** if the shape type allows the shape to have an image. |
| [get_Chart](./get_chart/)() | Provides access to the chart properties if this shape has a [Chart](../../aspose.words.drawing.charts/chart/). |
| [get_CoordOrigin](../shapebase/get_coordorigin/)() | The coordinates at the top-left corner of the containing block of this shape. |
| [get_CoordSize](../shapebase/get_coordsize/)() | The width and height of the coordinate space inside the containing block of this shape. |
| [get_Count](../../aspose.words/compositenode/get_count/)() | Gets the number of immediate children of this node. |
| [get_CustomNodeId](../../aspose.words/node/get_customnodeid/)() const | Specifies custom node identifier. |
| [get_DistanceBottom](../shapebase/get_distancebottom/)() | Returns or sets the distance (in points) between the document text and the bottom edge of the shape. |
| [get_DistanceLeft](../shapebase/get_distanceleft/)() | Returns or sets the distance (in points) between the document text and the left edge of the shape. |
| [get_DistanceRight](../shapebase/get_distanceright/)() | Returns or sets the distance (in points) between the document text and the right edge of the shape. |
| [get_DistanceTop](../shapebase/get_distancetop/)() | Returns or sets the distance (in points) between the document text and the top edge of the shape. |
| virtual [get_Document](../../aspose.words/node/get_document/)() const | Gets the document to which this node belongs. |
| [get_ExtrusionEnabled](./get_extrusionenabled/)() | Returns **true** if an extrusion effect is enabled. |
| [get_Fill](../shapebase/get_fill/)() | Gets fill formatting for the shape. |
| [get_FillColor](./get_fillcolor/)() | Defines the brush color that fills the closed path of the shape. |
| [get_Filled](./get_filled/)() | Determines whether the closed path of the shape will be filled. |
| [get_FirstChild](../../aspose.words/compositenode/get_firstchild/)() const | Gets the first child of the node. |
| [get_FirstParagraph](./get_firstparagraph/)() | Gets the first paragraph in the shape. |
| [get_FlipOrientation](../shapebase/get_fliporientation/)() | Switches the orientation of a shape. |
| [get_Font](../shapebase/get_font/)() | Provides access to the font formatting of this object. |
| [get_HasChart](./get_haschart/)() | Returns **true** if this [Shape](./) has a [Chart](../../aspose.words.drawing.charts/chart/). |
| [get_HasChildNodes](../../aspose.words/compositenode/get_haschildnodes/)() | Returns **true** if this node has any child nodes. |
| [get_HasImage](./get_hasimage/)() | Returns **true** if the shape has image bytes or links an image. |
| [get_HasSmartArt](./get_hassmartart/)() | Returns **true** if this [Shape](./) has a SmartArt object. |
| [get_Height](../shapebase/get_height/)() | Gets or sets the height of the containing block of the shape. |
| [get_HeightRelative](../shapebase/get_heightrelative/)() | Gets the value that represents the percentage of shape's relative height. |
| [get_HorizontalAlignment](../shapebase/get_horizontalalignment/)() | Specifies how the shape is positioned horizontally. |
| [get_HorizontalRuleFormat](./get_horizontalruleformat/)() | Provides access to the properties of the horizontal rule shape. For a shape that is not a horizontal rule, returns **null**. |
| [get_HRef](../shapebase/get_href/)() | Gets or sets the full hyperlink address for a shape. |
| [get_ImageData](./get_imagedata/)() | Provides access to the image of the shape. Returns **null** if the shape cannot have an image. |
| [get_IsComposite](../../aspose.words/compositenode/get_iscomposite/)() override | Returns **true** as this node can have child nodes. |
| [get_IsDecorative](../shapebase/get_isdecorative/)() | Gets or sets the flag that specifies whether the shape is decorative in the document. |
| [get_IsDeleteRevision](../shapebase/get_isdeleterevision/)() | Returns true if this object was deleted in Microsoft Word while change tracking was enabled. |
| [get_IsGroup](../shapebase/get_isgroup/)() | Returns **true** if this is a group shape. |
| [get_IsHorizontalRule](../shapebase/get_ishorizontalrule/)() | Returns **true** if this shape is a horizontal rule. |
| [get_IsImage](../shapebase/get_isimage/)() | Returns **true** if this shape is an image shape. |
| [get_IsInline](../shapebase/get_isinline/)() | A quick way to determine if this shape is positioned inline with text. |
| [get_IsInsertRevision](../shapebase/get_isinsertrevision/)() | Returns true if this object was inserted in Microsoft Word while change tracking was enabled. |
| [get_IsLayoutInCell](../shapebase/get_islayoutincell/)() | Gets or sets a flag indicating whether the shape is displayed inside a table or outside of it. |
| [get_IsMoveFromRevision](../shapebase/get_ismovefromrevision/)() | Returns **true** if this object was moved (deleted) in Microsoft Word while change tracking was enabled. |
| [get_IsMoveToRevision](../shapebase/get_ismovetorevision/)() | Returns **true** if this object was moved (inserted) in Microsoft Word while change tracking was enabled. |
| [get_IsSignatureLine](../shapebase/get_issignatureline/)() | Indicates that shape is a [SignatureLine](../signatureline/). |
| [get_IsTopLevel](../shapebase/get_istoplevel/)() | Returns **true** if this shape is not a child of a group shape. |
| [get_IsWordArt](../shapebase/get_iswordart/)() | Returns **true** if this shape is a WordArt object. |
| [get_LastChild](../../aspose.words/compositenode/get_lastchild/)() const | Gets the last child of the node. |
| [get_LastParagraph](./get_lastparagraph/)() | Gets the last paragraph in the shape. |
| [get_Left](../shapebase/get_left/)() | Gets or sets the position of the left edge of the containing block of the shape. |
| [get_LeftRelative](../shapebase/get_leftrelative/)() | Gets the value that represents shape's relative left position in percent. |
| [get_MarkupLanguage](../shapebase/get_markuplanguage/)() const | Gets MarkupLanguage used for this graphic object. |
| [get_Name](../shapebase/get_name/)() | Gets or sets the optional shape name. |
| [get_NextNode](../../aspose.words/node/get_nextnode/)() const |  |
| [get_NextSibling](../../aspose.words/node/get_nextsibling/)() | Gets the node immediately following this node. |
| [get_NodeType](./get_nodetype/)() const override | Returns [Shape](../../aspose.words/nodetype/). |
| [get_OleFormat](./get_oleformat/)() | Provides access to the OLE data of a shape. For a shape that is not an OLE object or ActiveX control, returns **null**. |
| [get_ParentNode](../../aspose.words/node/get_parentnode/)() | Gets the immediate parent of this node. |
| [get_ParentParagraph](../shapebase/get_parentparagraph/)() | Returns the immediate parent paragraph. |
| [get_PreviousSibling](../../aspose.words/node/get_previoussibling/)() | Gets the node immediately preceding this node. |
| [get_PrevNode](../../aspose.words/node/get_prevnode/)() const |  |
| [get_Range](../../aspose.words/node/get_range/)() | Returns a [Range](../../aspose.words/range/) object that represents the portion of a document that is contained in this node. |
| [get_RelativeHorizontalPosition](../shapebase/get_relativehorizontalposition/)() | Specifies relative to what the shape is positioned horizontally. |
| [get_RelativeHorizontalSize](../shapebase/get_relativehorizontalsize/)() | Gets or sets the value of shape's relative size in horizontal direction. |
| [get_RelativeVerticalPosition](../shapebase/get_relativeverticalposition/)() | Specifies relative to what the shape is positioned vertically. |
| [get_RelativeVerticalSize](../shapebase/get_relativeverticalsize/)() | Gets or sets the value of shape's relative size in vertical direction. |
| [get_Right](../shapebase/get_right/)() | Gets the position of the right edge of the containing block of the shape. |
| [get_Rotation](../shapebase/get_rotation/)() | Defines the angle (in degrees) that a shape is rotated. Positive value corresponds to clockwise rotation angle. |
| [get_ScreenTip](../shapebase/get_screentip/)() | Defines the text displayed when the mouse pointer moves over the shape. |
| [get_ShadowEnabled](./get_shadowenabled/)() | Returns **true** if a shadow effect is enabled. |
| [get_ShadowFormat](../shapebase/get_shadowformat/)() | Gets shadow formatting for the shape. |
| [get_ShapeType](../shapebase/get_shapetype/)() | Gets the shape type. |
| [get_SignatureLine](./get_signatureline/)() | Gets [SignatureLine](../signatureline/) object if the shape is a signature line. Returns **null** otherwise. |
| [get_SizeInPoints](../shapebase/get_sizeinpoints/)() | Gets the size of the shape in points. |
| [get_StoryType](./get_storytype/)() | Returns [Textbox](../../aspose.words/storytype/). |
| [get_Stroke](./get_stroke/)() | Defines a stroke for a shape. |
| [get_StrokeColor](./get_strokecolor/)() | Defines the color of a stroke. |
| [get_Stroked](./get_stroked/)() | Defines whether the path will be stroked. |
| [get_StrokeWeight](./get_strokeweight/)() | Defines the brush thickness that strokes the path of a shape in points. |
| [get_Target](../shapebase/get_target/)() | Gets or sets the target frame for the shape hyperlink. |
| [get_TextBox](./get_textbox/)() | Defines attributes that specify how text is displayed in a shape. |
| [get_TextPath](./get_textpath/)() | Defines the text of the text path (of a WordArt object). |
| [get_Title](../shapebase/get_title/)() | Gets or sets the title (caption) of the current shape object. |
| [get_Top](../shapebase/get_top/)() | Gets or sets the position of the top edge of the containing block of the shape. |
| [get_TopRelative](../shapebase/get_toprelative/)() | Gets the value that represents shape's relative top position in percent. |
| [get_VerticalAlignment](../shapebase/get_verticalalignment/)() | Specifies how the shape is positioned vertically. |
| [get_Width](../shapebase/get_width/)() | Gets or sets the width of the containing block of the shape. |
| [get_WidthRelative](../shapebase/get_widthrelative/)() | Gets the value that represents the percentage of shape's relative width. |
| [get_WrapSide](../shapebase/get_wrapside/)() | Specifies how the text is wrapped around the shape. |
| [get_WrapType](../shapebase/get_wraptype/)() | Defines whether the shape is inline or floating. For floating shapes defines the wrapping mode for text around the shape. |
| [get_ZOrder](../shapebase/get_zorder/)() | Determines the display order of overlapping shapes. |
| [GetAncestor](../../aspose.words/node/getancestor/)(Aspose::Words::NodeType) | Gets the first ancestor of the specified [NodeType](../../aspose.words/nodetype/). |
| [GetAncestorOf](../../aspose.words/node/getancestorof/)() |  |
| [GetChild](../../aspose.words/compositenode/getchild/)(Aspose::Words::NodeType, int32_t, bool) | Returns an Nth child node that matches the specified type. |
| [GetChildNodes](../../aspose.words/compositenode/getchildnodes/)(Aspose::Words::NodeType, bool) | Returns a live collection of child nodes that match the specified type. |
| [GetEnumerator](../../aspose.words/compositenode/getenumerator/)() override | Provides support for the for each style iteration over the child nodes of this node. |
| [GetShapeRenderer](../shapebase/getshaperenderer/)() | Creates and returns an object that can be used to render this shape into an image. |
| [GetText](../../aspose.words/compositenode/gettext/)() override | Gets the text of this node and of all its children. |
| [GetType](./gettype/)() const override |  |
| [IndexOf](../../aspose.words/compositenode/indexof/)(const System::SharedPtr\<Aspose::Words::Node\>\&) | Returns the index of the specified child node in the child node array. |
| [InsertAfter](../../aspose.words/compositenode/insertafter/)(T, const System::SharedPtr\<Aspose::Words::Node\>\&) |  |
| [InsertBefore](../../aspose.words/compositenode/insertbefore/)(T, const System::SharedPtr\<Aspose::Words::Node\>\&) |  |
| [Is](./is/)(const System::TypeInfo\&) const override |  |
| [IsAncestorNode](../../aspose.words/node/isancestornode/)(const System::SharedPtr\<Aspose::Words::Node\>\&) |  |
| [LocalToParent](../shapebase/localtoparent/)(System::Drawing::PointF) | Converts a value from the local coordinate space into the coordinate space of the parent shape. |
| [NextPreOrder](../../aspose.words/node/nextpreorder/)(const System::SharedPtr\<Aspose::Words::Node\>\&) | Gets next node according to the pre-order tree traversal algorithm. |
| static [NodeTypeToString](../../aspose.words/node/nodetypetostring/)(Aspose::Words::NodeType) | A utility method that converts a node type enum value into a user friendly string. |
| [PrependChild](../../aspose.words/compositenode/prependchild/)(T) |  |
| [PreviousPreOrder](../../aspose.words/node/previouspreorder/)(const System::SharedPtr\<Aspose::Words::Node\>\&) | Gets the previous node according to the pre-order tree traversal algorithm. |
| [Remove](../../aspose.words/node/remove/)() | Removes itself from the parent. |
| [RemoveAllChildren](../../aspose.words/compositenode/removeallchildren/)() | Removes all the child nodes of the current node. |
| [RemoveChild](../../aspose.words/compositenode/removechild/)(T) |  |
| [RemoveSmartTags](../../aspose.words/compositenode/removesmarttags/)() | Removes all [SmartTag](../../aspose.words.markup/smarttag/) descendant nodes of the current node. |
| [SelectNodes](../../aspose.words/compositenode/selectnodes/)(const System::String\&) | Selects a list of nodes matching the XPath expression. |
| [SelectSingleNode](../../aspose.words/compositenode/selectsinglenode/)(const System::String\&) | Selects the first [Node](../../aspose.words/node/) that matches the XPath expression. |
| [set_AllowOverlap](../shapebase/set_allowoverlap/)(bool) | Setter for [Aspose::Words::Drawing::ShapeBase::get_AllowOverlap](../shapebase/get_allowoverlap/). |
| [set_AlternativeText](../shapebase/set_alternativetext/)(const System::String\&) | Defines alternative text to be displayed instead of a graphic. |
| [set_AnchorLocked](../shapebase/set_anchorlocked/)(bool) | Setter for [Aspose::Words::Drawing::ShapeBase::get_AnchorLocked](../shapebase/get_anchorlocked/). |
| [set_AspectRatioLocked](../shapebase/set_aspectratiolocked/)(bool) | Setter for [Aspose::Words::Drawing::ShapeBase::get_AspectRatioLocked](../shapebase/get_aspectratiolocked/). |
| [set_BehindText](../shapebase/set_behindtext/)(bool) | Setter for [Aspose::Words::Drawing::ShapeBase::get_BehindText](../shapebase/get_behindtext/). |
| [set_Bounds](../shapebase/set_bounds/)(System::Drawing::RectangleF) | Setter for [Aspose::Words::Drawing::ShapeBase::get_Bounds](../shapebase/get_bounds/). |
| [set_CoordOrigin](../shapebase/set_coordorigin/)(System::Drawing::Point) | Setter for [Aspose::Words::Drawing::ShapeBase::get_CoordOrigin](../shapebase/get_coordorigin/). |
| [set_CoordSize](../shapebase/set_coordsize/)(System::Drawing::Size) | Setter for [Aspose::Words::Drawing::ShapeBase::get_CoordSize](../shapebase/get_coordsize/). |
| [set_CustomNodeId](../../aspose.words/node/set_customnodeid/)(int32_t) | Setter for [Aspose::Words::Node::get_CustomNodeId](../../aspose.words/node/get_customnodeid/). |
| [set_DistanceBottom](../shapebase/set_distancebottom/)(double) | Setter for [Aspose::Words::Drawing::ShapeBase::get_DistanceBottom](../shapebase/get_distancebottom/). |
| [set_DistanceLeft](../shapebase/set_distanceleft/)(double) | Setter for [Aspose::Words::Drawing::ShapeBase::get_DistanceLeft](../shapebase/get_distanceleft/). |
| [set_DistanceRight](../shapebase/set_distanceright/)(double) | Setter for [Aspose::Words::Drawing::ShapeBase::get_DistanceRight](../shapebase/get_distanceright/). |
| [set_DistanceTop](../shapebase/set_distancetop/)(double) | Setter for [Aspose::Words::Drawing::ShapeBase::get_DistanceTop](../shapebase/get_distancetop/). |
| [set_FillColor](./set_fillcolor/)(System::Drawing::Color) | Setter for [Aspose::Words::Drawing::Shape::get_FillColor](./get_fillcolor/). |
| [set_Filled](./set_filled/)(bool) | Setter for [Aspose::Words::Drawing::Shape::get_Filled](./get_filled/). |
| [set_FlipOrientation](../shapebase/set_fliporientation/)(Aspose::Words::Drawing::FlipOrientation) | Setter for [Aspose::Words::Drawing::ShapeBase::get_FlipOrientation](../shapebase/get_fliporientation/). |
| [set_Height](../shapebase/set_height/)(double) | Setter for [Aspose::Words::Drawing::ShapeBase::get_Height](../shapebase/get_height/). |
| [set_HeightRelative](../shapebase/set_heightrelative/)(float) | Sets the value that represents the percentage of shape's relative height. |
| [set_HorizontalAlignment](../shapebase/set_horizontalalignment/)(Aspose::Words::Drawing::HorizontalAlignment) | Setter for [Aspose::Words::Drawing::ShapeBase::get_HorizontalAlignment](../shapebase/get_horizontalalignment/). |
| [set_HRef](../shapebase/set_href/)(const System::String\&) | Setter for [Aspose::Words::Drawing::ShapeBase::get_HRef](../shapebase/get_href/). |
| [set_IsDecorative](../shapebase/set_isdecorative/)(bool) | Setter for [Aspose::Words::Drawing::ShapeBase::get_IsDecorative](../shapebase/get_isdecorative/). |
| [set_IsLayoutInCell](../shapebase/set_islayoutincell/)(bool) | Setter for [Aspose::Words::Drawing::ShapeBase::get_IsLayoutInCell](../shapebase/get_islayoutincell/). |
| [set_Left](../shapebase/set_left/)(double) | Setter for [Aspose::Words::Drawing::ShapeBase::get_Left](../shapebase/get_left/). |
| [set_LeftRelative](../shapebase/set_leftrelative/)(float) | Sets the value that represents shape's relative left position in percent. |
| [set_Name](../shapebase/set_name/)(const System::String\&) | Setter for [Aspose::Words::Drawing::ShapeBase::get_Name](../shapebase/get_name/). |
| [set_NextNode](../../aspose.words/node/set_nextnode/)(const System::SharedPtr\<Aspose::Words::Node\>\&) |  |
| [set_PrevNode](../../aspose.words/node/set_prevnode/)(const System::SharedPtr\<Aspose::Words::Node\>\&) |  |
| [set_RelativeHorizontalPosition](../shapebase/set_relativehorizontalposition/)(Aspose::Words::Drawing::RelativeHorizontalPosition) | Setter for [Aspose::Words::Drawing::ShapeBase::get_RelativeHorizontalPosition](../shapebase/get_relativehorizontalposition/). |
| [set_RelativeHorizontalSize](../shapebase/set_relativehorizontalsize/)(Aspose::Words::Drawing::RelativeHorizontalSize) | Setter for [Aspose::Words::Drawing::ShapeBase::get_RelativeHorizontalSize](../shapebase/get_relativehorizontalsize/). |
| [set_RelativeVerticalPosition](../shapebase/set_relativeverticalposition/)(Aspose::Words::Drawing::RelativeVerticalPosition) | Setter for [Aspose::Words::Drawing::ShapeBase::get_RelativeVerticalPosition](../shapebase/get_relativeverticalposition/). |
| [set_RelativeVerticalSize](../shapebase/set_relativeverticalsize/)(Aspose::Words::Drawing::RelativeVerticalSize) | Setter for [Aspose::Words::Drawing::ShapeBase::get_RelativeVerticalSize](../shapebase/get_relativeverticalsize/). |
| [set_Rotation](../shapebase/set_rotation/)(double) | Setter for [Aspose::Words::Drawing::ShapeBase::get_Rotation](../shapebase/get_rotation/). |
| [set_ScreenTip](../shapebase/set_screentip/)(const System::String\&) | Setter for [Aspose::Words::Drawing::ShapeBase::get_ScreenTip](../shapebase/get_screentip/). |
| [set_StrokeColor](./set_strokecolor/)(System::Drawing::Color) | Setter for [Aspose::Words::Drawing::Shape::get_StrokeColor](./get_strokecolor/). |
| [set_Stroked](./set_stroked/)(bool) | Setter for [Aspose::Words::Drawing::Shape::get_Stroked](./get_stroked/). |
| [set_StrokeWeight](./set_strokeweight/)(double) | Setter for [Aspose::Words::Drawing::Shape::get_StrokeWeight](./get_strokeweight/). |
| [set_Target](../shapebase/set_target/)(const System::String\&) | Setter for [Aspose::Words::Drawing::ShapeBase::get_Target](../shapebase/get_target/). |
| [set_Title](../shapebase/set_title/)(const System::String\&) | Setter for [Aspose::Words::Drawing::ShapeBase::get_Title](../shapebase/get_title/). |
| [set_Top](../shapebase/set_top/)(double) | Setter for [Aspose::Words::Drawing::ShapeBase::get_Top](../shapebase/get_top/). |
| [set_TopRelative](../shapebase/set_toprelative/)(float) | Sets the value that represents shape's relative top position in percent. |
| [set_VerticalAlignment](../shapebase/set_verticalalignment/)(Aspose::Words::Drawing::VerticalAlignment) | Setter for [Aspose::Words::Drawing::ShapeBase::get_VerticalAlignment](../shapebase/get_verticalalignment/). |
| [set_Width](../shapebase/set_width/)(double) | Setter for [Aspose::Words::Drawing::ShapeBase::get_Width](../shapebase/get_width/). |
| [set_WidthRelative](../shapebase/set_widthrelative/)(float) | Sets the value that represents the percentage of shape's relative width. |
| [set_WrapSide](../shapebase/set_wrapside/)(Aspose::Words::Drawing::WrapSide) | Setter for [Aspose::Words::Drawing::ShapeBase::get_WrapSide](../shapebase/get_wrapside/). |
| [set_WrapType](../shapebase/set_wraptype/)(Aspose::Words::Drawing::WrapType) | Setter for [Aspose::Words::Drawing::ShapeBase::get_WrapType](../shapebase/get_wraptype/). |
| [set_ZOrder](../shapebase/set_zorder/)(int32_t) | Setter for [Aspose::Words::Drawing::ShapeBase::get_ZOrder](../shapebase/get_zorder/). |
| [SetParent](../../aspose.words/node/setparent/)(const System::SharedPtr\<Aspose::Words::Node\>\&) |  |
| [SetTemplateWeakPtr](../../aspose.words/compositenode/settemplateweakptr/)(uint32_t) override |  |
| [Shape](./shape/)(const System::SharedPtr\<Aspose::Words::DocumentBase\>\&, Aspose::Words::Drawing::ShapeType) | Creates a new shape object. |
| [ToString](../../aspose.words/node/tostring/)(Aspose::Words::SaveFormat) | Exports the content of the node into a string in the specified format. |
| [ToString](../../aspose.words/node/tostring/)(const System::SharedPtr\<Aspose::Words::Saving::SaveOptions\>\&) | Exports the content of the node into a string using the specified save options. |
| static [Type](./type/)() |  |
| [UpdateSmartArtDrawing](./updatesmartartdrawing/)() | Updates SmartArt pre-rendered drawing by using [Aspose.Words](../../aspose.words/)'s SmartArt cold rendering engine. |
## Remarks


Using the [Shape](./) class you can create or modify shapes in a Microsoft Word document.

An important property of a shape is its [ShapeType](../shapebase/get_shapetype/). Shapes of different types can have different capabilities in a Word document. For example, only image and OLE shapes can have images inside them. Most of the shapes can have text, but not all.

Shapes that can have text, can contain [Paragraph](../../aspose.words/paragraph/) and [Table](../../aspose.words.tables/table/) nodes as children.

## Examples



Shows how to extract images from a document, and save them to the local file system as individual files. 
```cpp
auto doc = MakeObject<Document>(MyDir + u"Images.docx");

// Get the collection of shapes from the document,
// and save the image data of every shape with an image as a file to the local file system.
SharedPtr<NodeCollection> shapes = doc->GetChildNodes(NodeType::Shape, true);

ASSERT_EQ(9, shapes->LINQ_Count([](SharedPtr<Node> s) { return (System::ExplicitCast<Shape>(s))->get_HasImage(); }));

int imageIndex = 0;
for (const auto& shape : System::IterateOver(shapes->LINQ_OfType<SharedPtr<Shape>>()))
{
    if (shape->get_HasImage())
    {
        // The image data of shapes may contain images of many possible image formats.
        // We can determine a file extension for each image automatically, based on its format.
        String imageFileName =
            String::Format(u"File.ExtractImages.{0}{1}", imageIndex, FileFormatUtil::ImageTypeToExtension(shape->get_ImageData()->get_ImageType()));
        shape->get_ImageData()->Save(ArtifactsDir + imageFileName);
        imageIndex++;
    }
}
```


Shows how to insert a floating image to the center of a page. 
```cpp
auto doc = MakeObject<Document>();
auto builder = MakeObject<DocumentBuilder>(doc);

// Insert a floating image that will appear behind the overlapping text and align it to the page's center.
SharedPtr<Shape> shape = builder->InsertImage(ImageDir + u"Logo.jpg");
shape->set_WrapType(WrapType::None);
shape->set_BehindText(true);
shape->set_RelativeHorizontalPosition(RelativeHorizontalPosition::Page);
shape->set_RelativeVerticalPosition(RelativeVerticalPosition::Page);
shape->set_HorizontalAlignment(HorizontalAlignment::Center);
shape->set_VerticalAlignment(VerticalAlignment::Center);

doc->Save(ArtifactsDir + u"Image.CreateFloatingPageCenter.docx");
```


Shows how to delete all shapes from a document. 
```cpp
auto doc = MakeObject<Document>();
auto builder = MakeObject<DocumentBuilder>(doc);

// Insert two shapes along with a group shape with another shape inside it.
builder->InsertShape(ShapeType::Rectangle, 400, 200);
builder->InsertShape(ShapeType::Star, 300, 300);

auto group = MakeObject<GroupShape>(doc);
group->set_Bounds(System::Drawing::RectangleF(100.0f, 50.0f, 200.0f, 100.0f));
group->set_CoordOrigin(System::Drawing::Point(-1000, -500));

auto subShape = MakeObject<Shape>(doc, ShapeType::Cube);
subShape->set_Width(500);
subShape->set_Height(700);
subShape->set_Left(0);
subShape->set_Top(0);

group->AppendChild(subShape);
builder->InsertNode(group);

ASSERT_EQ(3, doc->GetChildNodes(NodeType::Shape, true)->get_Count());
ASSERT_EQ(1, doc->GetChildNodes(NodeType::GroupShape, true)->get_Count());

// Remove all Shape nodes from the document.
SharedPtr<NodeCollection> shapes = doc->GetChildNodes(NodeType::Shape, true);
shapes->Clear();

// All shapes are gone, but the group shape is still in the document.
ASSERT_EQ(1, doc->GetChildNodes(NodeType::GroupShape, true)->get_Count());
ASSERT_EQ(0, doc->GetChildNodes(NodeType::Shape, true)->get_Count());

// Remove all group shapes separately.
SharedPtr<NodeCollection> groupShapes = doc->GetChildNodes(NodeType::GroupShape, true);
groupShapes->Clear();

ASSERT_EQ(0, doc->GetChildNodes(NodeType::GroupShape, true)->get_Count());
ASSERT_EQ(0, doc->GetChildNodes(NodeType::Shape, true)->get_Count());
```

## See Also

* Class [ShapeBase](../shapebase/)
* Namespace [Aspose::Words::Drawing](../)
* Library [Aspose.Words for C++](../../)
