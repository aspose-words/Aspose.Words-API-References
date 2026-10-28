---
title: Aspose::Words::Drawing::GroupShape class
linktitle: GroupShape
second_title: Aspose.Words for C++ API Reference
description: 'Aspose::Words::Drawing::GroupShape class. Represents a group of shapes in a document. To learn more, visit the How to Add Group Shape into a Word Document documentation article in C++.'
type: docs
weight: 4000
url: /cpp/aspose.words.drawing/groupshape/
---
## GroupShape class


Represents a group of shapes in a document. 
To learn more, visit the [How to Add Group Shape into a Word Document](https://docs.aspose.com/words/cpp/how-to-add-group-shape-into-a-word-document/) documentation article.

```cpp
class GroupShape : public ShapeBase
```

## Methods

| Method | Description |
| --- | --- |
| [Accept](./accept/)(System::SharedPtr\<Aspose::Words::DocumentVisitor\>) override | Accepts a visitor. |
| [AcceptEnd](./acceptend/)(System::SharedPtr\<Aspose::Words::DocumentVisitor\>) override | Accepts a visitor for visiting the end of the GroupShape. |
| [AcceptStart](./acceptstart/)(System::SharedPtr\<Aspose::Words::DocumentVisitor\>) override | Accepts a visitor for visiting the start of the GroupShape. |
| [GetType](./gettype/)() const override |  |
| [GroupShape](./groupshape/)(const System::SharedPtr\<Aspose::Words::DocumentBase\> \&) | Creates a new group shape. |
| [Is](./is/)(const System::TypeInfo \&) const override |  |
| static [Type](./type/)() |  |
| [get_NodeType](./get_nodetype/)() const override | Returns [GroupShape](../../aspose.words/nodetype/). |
| [AdjustWithEffects](../shapebase/adjustwitheffects/)(System::Drawing::RectangleF) | Adds to the source rectangle values of the effect extent and returns the final rectangle. |
| [GetShapeRenderer](../shapebase/getshaperenderer/)() | Creates and returns an object that can be used to render this shape into an image. |
| [GetType](../shapebase/gettype/)() const override |  |
| [Is](../shapebase/is/)(const System::TypeInfo \&) const override |  |
| [LocalToParent](../shapebase/localtoparent/)(System::Drawing::PointF) | Converts a value from the local coordinate space into the coordinate space of the parent shape. |
| static [Type](../shapebase/type/)() |  |
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
| [get_CoordOrigin](../shapebase/get_coordorigin/)() | The coordinates at the top-left corner of the containing block of this shape. |
| [get_CoordSize](../shapebase/get_coordsize/)() | The width and height of the coordinate space inside the containing block of this shape. |
| [get_DistanceBottom](../shapebase/get_distancebottom/)() | Returns or sets the distance (in points) between the document text and the bottom edge of the shape. |
| [get_DistanceLeft](../shapebase/get_distanceleft/)() | Returns or sets the distance (in points) between the document text and the left edge of the shape. |
| [get_DistanceRight](../shapebase/get_distanceright/)() | Returns or sets the distance (in points) between the document text and the right edge of the shape. |
| [get_DistanceTop](../shapebase/get_distancetop/)() | Returns or sets the distance (in points) between the document text and the top edge of the shape. |
| [get_Fill](../shapebase/get_fill/)() | Gets fill formatting for the shape. |
| [get_FlipOrientation](../shapebase/get_fliporientation/)() | Switches the orientation of a shape. |
| [get_Font](../shapebase/get_font/)() | Provides access to the font formatting of this object. |
| [get_Glow](../shapebase/get_glow/)() | Gets glow formatting for the shape. |
| [get_HRef](../shapebase/get_href/)() | Gets or sets the full hyperlink address for a shape. |
| [get_Height](../shapebase/get_height/)() | Gets or sets the height of the containing block of the shape. |
| [get_HeightRelative](../shapebase/get_heightrelative/)() | Gets or sets the value that represents the percentage of shape's relative height. |
| [get_Hidden](../shapebase/get_hidden/)() | Gets or sets a boolean value indicating whether the shape is visible. |
| [get_HorizontalAlignment](../shapebase/get_horizontalalignment/)() | Specifies how the shape is positioned horizontally. |
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
| [get_Left](../shapebase/get_left/)() | Gets or sets the position of the left edge of the containing block of the shape. |
| [get_LeftRelative](../shapebase/get_leftrelative/)() | Gets or sets the value that represents shape's relative left position in percent. |
| [get_MarkupLanguage](../shapebase/get_markuplanguage/)() const | Gets MarkupLanguage used for this graphic object. |
| [get_Name](../shapebase/get_name/)() | Gets or sets the optional shape name. |
| [get_ParentParagraph](../shapebase/get_parentparagraph/)() | Returns the immediate parent paragraph. |
| [get_Reflection](../shapebase/get_reflection/)() | Gets reflection formatting for the shape. |
| [get_RelativeHorizontalPosition](../shapebase/get_relativehorizontalposition/)() | Specifies relative to what the shape is positioned horizontally. |
| [get_RelativeHorizontalSize](../shapebase/get_relativehorizontalsize/)() | Gets or sets the value of shape's relative size in horizontal direction. |
| [get_RelativeVerticalPosition](../shapebase/get_relativeverticalposition/)() | Specifies relative to what the shape is positioned vertically. |
| [get_RelativeVerticalSize](../shapebase/get_relativeverticalsize/)() | Gets or sets the value of shape's relative size in vertical direction. |
| [get_Right](../shapebase/get_right/)() | Gets the position of the right edge of the containing block of the shape. |
| [get_Rotation](../shapebase/get_rotation/)() | Defines the angle (in degrees) that a shape is rotated. Positive value corresponds to clockwise rotation angle. |
| [get_ScreenTip](../shapebase/get_screentip/)() | Defines the text displayed when the mouse pointer moves over the shape. |
| [get_ShadowFormat](../shapebase/get_shadowformat/)() | Gets shadow formatting for the shape. |
| [get_ShapeType](../shapebase/get_shapetype/)() | Gets the shape type. |
| [get_SizeInPoints](../shapebase/get_sizeinpoints/)() | Gets the size of the shape in points. |
| [get_SoftEdge](../shapebase/get_softedge/)() | Gets soft edge formatting for the shape. |
| [get_Target](../shapebase/get_target/)() | Gets or sets the target frame for the shape hyperlink. |
| [get_Title](../shapebase/get_title/)() | Gets or sets the title (caption) of the current shape object. |
| [get_Top](../shapebase/get_top/)() | Gets or sets the position of the top edge of the containing block of the shape. |
| [get_TopRelative](../shapebase/get_toprelative/)() | Gets or sets the value that represents shape's relative top position in percent. |
| [get_VerticalAlignment](../shapebase/get_verticalalignment/)() | Specifies how the shape is positioned vertically. |
| [get_Width](../shapebase/get_width/)() | Gets or sets the width of the containing block of the shape. |
| [get_WidthRelative](../shapebase/get_widthrelative/)() | Gets or sets the value that represents the percentage of shape's relative width. |
| [get_WrapSide](../shapebase/get_wrapside/)() | Specifies how the text is wrapped around the shape. |
| [get_WrapType](../shapebase/get_wraptype/)() | Defines whether the shape is inline or floating. For floating shapes defines the wrapping mode for text around the shape. |
| [get_ZOrder](../shapebase/get_zorder/)() | Determines the display order of overlapping shapes. |
| [set_AllowOverlap](../shapebase/set_allowoverlap/)(bool) | Sets a value that specifies whether this shape can overlap other shapes. |
| [set_AlternativeText](../shapebase/set_alternativetext/)(const System::String \&) | Defines alternative text to be displayed instead of a graphic. |
| [set_AnchorLocked](../shapebase/set_anchorlocked/)(bool) | Specifies whether the shape's anchor is locked. |
| [set_AspectRatioLocked](../shapebase/set_aspectratiolocked/)(bool) | Specifies whether the shape's aspect ratio is locked. |
| [set_BehindText](../shapebase/set_behindtext/)(bool) | Specifies whether the shape is below or above text. |
| [set_Bounds](../shapebase/set_bounds/)(System::Drawing::RectangleF) | Sets the location and size of the containing block of the shape. |
| [set_CoordOrigin](../shapebase/set_coordorigin/)(System::Drawing::Point) | The coordinates at the top-left corner of the containing block of this shape. |
| [set_CoordSize](../shapebase/set_coordsize/)(System::Drawing::Size) | The width and height of the coordinate space inside the containing block of this shape. |
| [set_DistanceBottom](../shapebase/set_distancebottom/)(double) | Sets the distance (in points) between the document text and the bottom edge of the shape. |
| [set_DistanceLeft](../shapebase/set_distanceleft/)(double) | Sets the distance (in points) between the document text and the left edge of the shape. |
| [set_DistanceRight](../shapebase/set_distanceright/)(double) | Sets the distance (in points) between the document text and the right edge of the shape. |
| [set_DistanceTop](../shapebase/set_distancetop/)(double) | Sets the distance (in points) between the document text and the top edge of the shape. |
| [set_FlipOrientation](../shapebase/set_fliporientation/)(Aspose::Words::Drawing::FlipOrientation) | Switches the orientation of a shape. |
| [set_HRef](../shapebase/set_href/)(const System::String \&) | Sets the full hyperlink address for a shape. |
| [set_Height](../shapebase/set_height/)(double) | Sets the height of the containing block of the shape. |
| [set_HeightRelative](../shapebase/set_heightrelative/)(float) | Sets the value that represents the percentage of shape's relative height. |
| [set_Hidden](../shapebase/set_hidden/)(bool) | Sets a boolean value indicating whether the shape is visible. |
| [set_HorizontalAlignment](../shapebase/set_horizontalalignment/)(Aspose::Words::Drawing::HorizontalAlignment) | Specifies how the shape is positioned horizontally. |
| [set_IsDecorative](../shapebase/set_isdecorative/)(bool) | Sets the flag that specifies whether the shape is decorative in the document. |
| [set_IsLayoutInCell](../shapebase/set_islayoutincell/)(bool) | Sets a flag indicating whether the shape is displayed inside a table or outside of it. |
| [set_Left](../shapebase/set_left/)(double) | Sets the position of the left edge of the containing block of the shape. |
| [set_LeftRelative](../shapebase/set_leftrelative/)(float) | Sets the value that represents shape's relative left position in percent. |
| [set_Name](../shapebase/set_name/)(const System::String \&) | Sets the optional shape name. |
| [set_RelativeHorizontalPosition](../shapebase/set_relativehorizontalposition/)(Aspose::Words::Drawing::RelativeHorizontalPosition) | Specifies relative to what the shape is positioned horizontally. |
| [set_RelativeHorizontalSize](../shapebase/set_relativehorizontalsize/)(Aspose::Words::Drawing::RelativeHorizontalSize) | Sets the value of shape's relative size in horizontal direction. |
| [set_RelativeVerticalPosition](../shapebase/set_relativeverticalposition/)(Aspose::Words::Drawing::RelativeVerticalPosition) | Specifies relative to what the shape is positioned vertically. |
| [set_RelativeVerticalSize](../shapebase/set_relativeverticalsize/)(Aspose::Words::Drawing::RelativeVerticalSize) | Sets the value of shape's relative size in vertical direction. |
| [set_Rotation](../shapebase/set_rotation/)(double) | Defines the angle (in degrees) that a shape is rotated. Positive value corresponds to clockwise rotation angle. |
| [set_ScreenTip](../shapebase/set_screentip/)(const System::String \&) | Defines the text displayed when the mouse pointer moves over the shape. |
| [set_Target](../shapebase/set_target/)(const System::String \&) | Sets the target frame for the shape hyperlink. |
| [set_Title](../shapebase/set_title/)(const System::String \&) | Sets the title (caption) of the current shape object. |
| [set_Top](../shapebase/set_top/)(double) | Sets the position of the top edge of the containing block of the shape. |
| [set_TopRelative](../shapebase/set_toprelative/)(float) | Sets the value that represents shape's relative top position in percent. |
| [set_VerticalAlignment](../shapebase/set_verticalalignment/)(Aspose::Words::Drawing::VerticalAlignment) | Specifies how the shape is positioned vertically. |
| [set_Width](../shapebase/set_width/)(double) | Sets the width of the containing block of the shape. |
| [set_WidthRelative](../shapebase/set_widthrelative/)(float) | Sets the value that represents the percentage of shape's relative width. |
| [set_WrapSide](../shapebase/set_wrapside/)(Aspose::Words::Drawing::WrapSide) | Specifies how the text is wrapped around the shape. |
| [set_WrapType](../shapebase/set_wraptype/)(Aspose::Words::Drawing::WrapType) | Defines whether the shape is inline or floating. For floating shapes defines the wrapping mode for text around the shape. |
| [set_ZOrder](../shapebase/set_zorder/)(int32_t) | Determines the display order of overlapping shapes. |
| virtual [AcceptEnd](../../aspose.words/compositenode/acceptend/)(System::SharedPtr\<Aspose::Words::DocumentVisitor\>) | When implemented in a derived class, calls the VisitXXXEnd method of the specified document visitor. |
| virtual [AcceptStart](../../aspose.words/compositenode/acceptstart/)(System::SharedPtr\<Aspose::Words::DocumentVisitor\>) | When implemented in a derived class, calls the VisitXXXStart method of the specified document visitor. |
| [AppendChild](../../aspose.words/compositenode/appendchild/)(T) | Adds the specified node to the end of the list of child nodes for this node. |
| [GetChild](../../aspose.words/compositenode/getchild/)(Aspose::Words::NodeType, int32_t, bool) | Returns an Nth child node that matches the specified type. |
| [GetChildNodes](../../aspose.words/compositenode/getchildnodes/)(Aspose::Words::NodeType, bool) | Returns a live collection of child nodes that match the specified type. |
| [GetEnumerator](../../aspose.words/compositenode/getenumerator/)() override | Provides support for the for each style iteration over the child nodes of this node. |
| [GetText](../../aspose.words/compositenode/gettext/)() override | Gets the text of this node and of all its children. |
| [GetType](../../aspose.words/compositenode/gettype/)() const override |  |
| [IndexOf](../../aspose.words/compositenode/indexof/)(const System::SharedPtr\<Aspose::Words::Node\> \&) | Returns the index of the specified child node in the child node array. |
| [InsertAfter](../../aspose.words/compositenode/insertafter/)(T, const System::SharedPtr\<Aspose::Words::Node\> \&) | Inserts the specified node immediately after the specified reference node. |
| [InsertBefore](../../aspose.words/compositenode/insertbefore/)(T, const System::SharedPtr\<Aspose::Words::Node\> \&) | Inserts the specified node immediately before the specified reference node. |
| [Is](../../aspose.words/compositenode/is/)(const System::TypeInfo \&) const override |  |
| [PrependChild](../../aspose.words/compositenode/prependchild/)(T) | Adds the specified node to the beginning of the list of child nodes for this node. |
| [RemoveAllChildren](../../aspose.words/compositenode/removeallchildren/)() | Removes all the child nodes of the current node. |
| [RemoveChild](../../aspose.words/compositenode/removechild/)(T) | Removes the specified child node. |
| [RemoveSmartTags](../../aspose.words/compositenode/removesmarttags/)() | Removes all [SmartTag](../../aspose.words.markup/smarttag/) descendant nodes of the current node. |
| [SelectNodes](../../aspose.words/compositenode/selectnodes/)(const System::String \&) | Selects a list of nodes matching the XPath expression. |
| [SelectSingleNode](../../aspose.words/compositenode/selectsinglenode/)(const System::String \&) | Selects the first [Node](../../aspose.words/node/) that matches the XPath expression. |
| static [Type](../../aspose.words/compositenode/type/)() |  |
| [get_Count](../../aspose.words/compositenode/get_count/)() | Gets the number of immediate children of this node. |
| [get_FirstChild](../../aspose.words/compositenode/get_firstchild/)() const | Gets the first child of the node. |
| [get_HasChildNodes](../../aspose.words/compositenode/get_haschildnodes/)() | Returns **true** if this node has any child nodes. |
| [get_IsComposite](../../aspose.words/compositenode/get_iscomposite/)() override | Returns **true** as this node can have child nodes. |
| [get_LastChild](../../aspose.words/compositenode/get_lastchild/)() const | Gets the last child of the node. |
| virtual [Accept](../../aspose.words/node/accept/)(System::SharedPtr\<Aspose::Words::DocumentVisitor\>) | Accepts a visitor. |
| [Clone](../../aspose.words/node/clone/)(bool) | Creates a duplicate of the node. |
| [GetAncestor](../../aspose.words/node/getancestor/)(Aspose::Words::NodeType) | Gets the first ancestor of the specified [NodeType](../../aspose.words/nodetype/). |
| [GetAncestorOf](../../aspose.words/node/getancestorof/)() |  |
| virtual [GetText](../../aspose.words/node/gettext/)() | Gets the text of this node and of all its children. |
| [GetType](../../aspose.words/node/gettype/)() const override |  |
| [Is](../../aspose.words/node/is/)(const System::TypeInfo \&) const override |  |
| [IsAncestorNode](../../aspose.words/node/isancestornode/)(const System::SharedPtr\<Aspose::Words::Node\> \&) |  |
| [NextPreOrder](../../aspose.words/node/nextpreorder/)(const System::SharedPtr\<Aspose::Words::Node\> \&) | Gets next node according to the pre-order tree traversal algorithm. |
| static [NodeTypeToString](../../aspose.words/node/nodetypetostring/)(Aspose::Words::NodeType) | A utility method that converts a node type enum value into a user friendly string. |
| [PreviousPreOrder](../../aspose.words/node/previouspreorder/)(const System::SharedPtr\<Aspose::Words::Node\> \&) | Gets the previous node according to the pre-order tree traversal algorithm. |
| [Remove](../../aspose.words/node/remove/)() | Removes itself from the parent. |
| [SetParent](../../aspose.words/node/setparent/)(const System::SharedPtr\<Aspose::Words::Node\> \&) |  |
| [ToString](../../aspose.words/node/tostring/)(Aspose::Words::SaveFormat) | Exports the content of the node into a string in the specified format. |
| [ToString](../../aspose.words/node/tostring/)(const System::SharedPtr\<Aspose::Words::Saving::SaveOptions\> \&) | Exports the content of the node into a string using the specified save options. |
| static [Type](../../aspose.words/node/type/)() |  |
| [get_CustomNodeId](../../aspose.words/node/get_customnodeid/)() const | Specifies custom node identifier. |
| virtual [get_Document](../../aspose.words/node/get_document/)() const | Gets the document to which this node belongs. |
| virtual [get_IsComposite](../../aspose.words/node/get_iscomposite/)() | Returns **true** if this node can contain other nodes. |
| [get_NextNode](../../aspose.words/node/get_nextnode/)() const |  |
| [get_NextSibling](../../aspose.words/node/get_nextsibling/)() | Gets the node immediately following this node. |
| virtual [get_NodeType](../../aspose.words/node/get_nodetype/)() const | Gets the type of this node. |
| [get_ParentNode](../../aspose.words/node/get_parentnode/)() | Gets the immediate parent of this node. |
| [get_PrevNode](../../aspose.words/node/get_prevnode/)() const |  |
| [get_PreviousSibling](../../aspose.words/node/get_previoussibling/)() | Gets the node immediately preceding this node. |
| [get_Range](../../aspose.words/node/get_range/)() | Returns a [Range](../../aspose.words/range/) object that represents the portion of a document that is contained in this node. |
| [set_CustomNodeId](../../aspose.words/node/set_customnodeid/)(int32_t) | Specifies custom node identifier. |
| [set_NextNode](../../aspose.words/node/set_nextnode/)(const System::SharedPtr\<Aspose::Words::Node\> \&) |  |
| [set_PrevNode](../../aspose.words/node/set_prevnode/)(const System::SharedPtr\<Aspose::Words::Node\> \&) |  |
## Remarks


A [GroupShape](./) is a composite node and can have [Shape](../shape/) and [GroupShape](./) nodes as children.

Each [GroupShape](./) defines a new coordinate system for its child shapes. The coordinate system is defined using the [CoordSize](../shapebase/get_coordsize/) and [CoordOrigin](../shapebase/get_coordorigin/) properties.
## See Also

* Class [ShapeBase](../shapebase/)
* Namespace [Aspose::Words::Drawing](../)
* Library [Aspose.Words for C++](../../)
