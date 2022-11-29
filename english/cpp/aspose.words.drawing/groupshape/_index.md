---
title: GroupShape
second_title: Aspose.Words for C++ API Reference
description: Represents a group of shapes in a document.
type: docs
weight: 40
url: /cpp/aspose.words.drawing/groupshape/
---
## GroupShape class


Represents a group of shapes in a document.

```cpp
class GroupShape : public Aspose::Words::Drawing::ShapeBase
```

## Methods

| Method | Description |
| --- | --- |
| [Accept](./accept/)(System::SharedPtr\<Aspose::Words::DocumentVisitor\>) override | Accepts a visitor. |
| [AdjustWithEffects](../shapebase/adjustwitheffects/)(System::Drawing::RectangleF) | Adds to the source rectangle values of the effect extent and returns the final rectangle. |
| [AppendChild](../../aspose.words/compositenode/appendchild/)(const System::SharedPtr\<Aspose::Words::Node\>\&) | Adds the specified node to the end of the list of child nodes for this node. |
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
| [get_CanHaveImage](../shapebase/get_canhaveimage/)() | Returns true if the shape type allows the shape to have an image. |
| [get_ChildNodes](../../aspose.words/compositenode/get_childnodes/)() | Gets all immediate child nodes of this node. |
| [get_CoordOrigin](../shapebase/get_coordorigin/)() | The coordinates at the top-left corner of the containing block of this shape. |
| [get_CoordSize](../shapebase/get_coordsize/)() | The width and height of the coordinate space inside the containing block of this shape. |
| [get_Count](../../aspose.words/compositenode/get_count/)() | Gets the number of immediate children of this node. |
| [get_CustomNodeId](../../aspose.words/node/get_customnodeid/)() const | Specifies custom node identifier. |
| [get_DistanceBottom](../shapebase/get_distancebottom/)() | Returns or sets the distance (in points) between the document text and the bottom edge of the shape. |
| [get_DistanceLeft](../shapebase/get_distanceleft/)() | Returns or sets the distance (in points) between the document text and the left edge of the shape. |
| [get_DistanceRight](../shapebase/get_distanceright/)() | Returns or sets the distance (in points) between the document text and the right edge of the shape. |
| [get_DistanceTop](../shapebase/get_distancetop/)() | Returns or sets the distance (in points) between the document text and the top edge of the shape. |
| virtual [get_Document](../../aspose.words/node/get_document/)() const | Gets the document to which this node belongs. |
| [get_Fill](../shapebase/get_fill/)() | Gets fill formatting for the shape. |
| [get_FirstChild](../../aspose.words/compositenode/get_firstchild/)() const | Gets the first child of the node. |
| [get_FlipOrientation](../shapebase/get_fliporientation/)() | Switches the orientation of a shape. |
| [get_Font](../shapebase/get_font/)() | Provides access to the font formatting of this object. |
| [get_HasChildNodes](../../aspose.words/compositenode/get_haschildnodes/)() | Returns true if this node has any child nodes. |
| [get_Height](../shapebase/get_height/)() | Gets or sets the height of the containing block of the shape. |
| [get_HorizontalAlignment](../shapebase/get_horizontalalignment/)() | Specifies how the shape is positioned horizontally. |
| [get_HRef](../shapebase/get_href/)() | Gets or sets the full hyperlink address for a shape. |
| [get_IsComposite](../../aspose.words/compositenode/get_iscomposite/)() override | Returns true as this node can have child nodes. |
| [get_IsDecorative](../shapebase/get_isdecorative/)() | Gets or sets the flag that specifies whether the shape is decorative in the document. |
| [get_IsDeleteRevision](../shapebase/get_isdeleterevision/)() | Returns true if this object was deleted in Microsoft Word while change tracking was enabled. |
| [get_IsGroup](../shapebase/get_isgroup/)() | Returns true if this is a group shape. |
| [get_IsHorizontalRule](../shapebase/get_ishorizontalrule/)() | Returns true if this shape is a horizontal rule. |
| [get_IsImage](../shapebase/get_isimage/)() | Returns true if this shape is an image shape. |
| [get_IsInline](../shapebase/get_isinline/)() | A quick way to determine if this shape is positioned inline with text. |
| [get_IsInsertRevision](../shapebase/get_isinsertrevision/)() | Returns true if this object was inserted in Microsoft Word while change tracking was enabled. |
| [get_IsLayoutInCell](../shapebase/get_islayoutincell/)() | Gets or sets a flag indicating whether the shape is displayed inside a table or outside of it. |
| [get_IsMoveFromRevision](../shapebase/get_ismovefromrevision/)() | Returns **true** if this object was moved (deleted) in Microsoft Word while change tracking was enabled. |
| [get_IsMoveToRevision](../shapebase/get_ismovetorevision/)() | Returns **true** if this object was moved (inserted) in Microsoft Word while change tracking was enabled. |
| [get_IsSignatureLine](../shapebase/get_issignatureline/)() | Indicates that shape is a [SignatureLine](../signatureline/). |
| [get_IsTopLevel](../shapebase/get_istoplevel/)() | Returns true if this shape is not a child of a group shape. |
| [get_IsWordArt](../shapebase/get_iswordart/)() | Returns true if this shape is a WordArt object. |
| [get_LastChild](../../aspose.words/compositenode/get_lastchild/)() const | Gets the last child of the node. |
| [get_Left](../shapebase/get_left/)() | Gets or sets the position of the left edge of the containing block of the shape. |
| [get_MarkupLanguage](../shapebase/get_markuplanguage/)() const | Gets MarkupLanguage used for this graphic object. |
| [get_Name](../shapebase/get_name/)() | Gets or sets the optional shape name. |
| [get_NextSibling](../../aspose.words/node/get_nextsibling/)() | Gets the node immediately following this node. |
| [get_NodeType](./get_nodetype/)() const override | Returns [GroupShape](../../aspose.words/nodetype/). |
| [get_ParentNode](../../aspose.words/node/get_parentnode/)() | Gets the immediate parent of this node. |
| [get_ParentParagraph](../shapebase/get_parentparagraph/)() | Returns the immediate parent paragraph. |
| [get_PreviousSibling](../../aspose.words/node/get_previoussibling/)() | Gets the node immediately preceding this node. |
| [get_Range](../../aspose.words/node/get_range/)() | Returns a **Range** object that represents the portion of a document that is contained in this node. |
| [get_RelativeHorizontalPosition](../shapebase/get_relativehorizontalposition/)() | Specifies relative to what the shape is positioned horizontally. |
| [get_RelativeVerticalPosition](../shapebase/get_relativeverticalposition/)() | Specifies relative to what the shape is positioned vertically. |
| [get_Right](../shapebase/get_right/)() | Gets the position of the right edge of the containing block of the shape. |
| [get_Rotation](../shapebase/get_rotation/)() | Defines the angle (in degrees) that a shape is rotated. Positive value corresponds to clockwise rotation angle. |
| [get_ScreenTip](../shapebase/get_screentip/)() | Defines the text displayed when the mouse pointer moves over the shape. |
| [get_ShadowFormat](../shapebase/get_shadowformat/)() | Gets shadow formatting for the shape. |
| [get_ShapeType](../shapebase/get_shapetype/)() | Gets the shape type. |
| [get_SizeInPoints](../shapebase/get_sizeinpoints/)() | Gets the size of the shape in points. |
| [get_Target](../shapebase/get_target/)() | Gets or sets the target frame for the shape hyperlink. |
| [get_Title](../shapebase/get_title/)() | Gets or sets the title (caption) of the current shape object. |
| [get_Top](../shapebase/get_top/)() | Gets or sets the position of the top edge of the containing block of the shape. |
| [get_VerticalAlignment](../shapebase/get_verticalalignment/)() | Specifies how the shape is positioned vertically. |
| [get_Width](../shapebase/get_width/)() | Gets or sets the width of the containing block of the shape. |
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
| [GroupShape](./groupshape/)(const System::SharedPtr\<Aspose::Words::DocumentBase\>\&) | Creates a new group shape. |
| [IndexOf](../../aspose.words/compositenode/indexof/)(const System::SharedPtr\<Aspose::Words::Node\>\&) | Returns the index of the specified child node in the child node array. |
| [InsertAfter](../../aspose.words/compositenode/insertafter/)(const System::SharedPtr\<Aspose::Words::Node\>\&, const System::SharedPtr\<Aspose::Words::Node\>\&) | Inserts the specified node immediately after the specified reference node. |
| [InsertBefore](../../aspose.words/compositenode/insertbefore/)(const System::SharedPtr\<Aspose::Words::Node\>\&, const System::SharedPtr\<Aspose::Words::Node\>\&) | Inserts the specified node immediately before the specified reference node. |
| [LocalToParent](../shapebase/localtoparent/)(System::Drawing::PointF) | Converts a value from the local coordinate space into the coordinate space of the parent shape. |
| [NextPreOrder](../../aspose.words/node/nextpreorder/)(const System::SharedPtr\<Aspose::Words::Node\>\&) | Gets next node according to the pre-order tree traversal algorithm. |
| static [NodeTypeToString](../../aspose.words/node/nodetypetostring/)(Aspose::Words::NodeType) | A utility method that converts a node type enum value into a user friendly string. |
| [PrependChild](../../aspose.words/compositenode/prependchild/)(const System::SharedPtr\<Aspose::Words::Node\>\&) | Adds the specified node to the beginning of the list of child nodes for this node. |
| [PreviousPreOrder](../../aspose.words/node/previouspreorder/)(const System::SharedPtr\<Aspose::Words::Node\>\&) | Gets the previous node according to the pre-order tree traversal algorithm. |
| [Remove](../../aspose.words/node/remove/)() | Removes itself from the parent. |
| [RemoveAllChildren](../../aspose.words/compositenode/removeallchildren/)() | Removes all the child nodes of the current node. |
| [RemoveChild](../../aspose.words/compositenode/removechild/)(const System::SharedPtr\<Aspose::Words::Node\>\&) | Removes the specified child node. |
| [RemoveSmartTags](../../aspose.words/compositenode/removesmarttags/)() | Removes all [SmartTag](../../aspose.words.markup/smarttag/) descendant nodes of the current node. |
| [SelectNodes](../../aspose.words/compositenode/selectnodes/)(const System::String\&) | Selects a list of nodes matching the XPath expression. |
| [SelectSingleNode](../../aspose.words/compositenode/selectsinglenode/)(const System::String\&) | Selects the first [Node](../../aspose.words/node/) that matches the XPath expression. |
| [set_AllowOverlap](../shapebase/set_allowoverlap/)(bool) | Setter for [Aspose::Words::Drawing::ShapeBase::get_AllowOverlap](../shapebase/get_allowoverlap/). |
| [set_AlternativeText](../shapebase/set_alternativetext/)(const System::String\&) | Setter for [Aspose::Words::Drawing::ShapeBase::get_AlternativeText](../shapebase/get_alternativetext/). |
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
| [set_FlipOrientation](../shapebase/set_fliporientation/)(Aspose::Words::Drawing::FlipOrientation) | Setter for [Aspose::Words::Drawing::ShapeBase::get_FlipOrientation](../shapebase/get_fliporientation/). |
| [set_Height](../shapebase/set_height/)(double) | Setter for [Aspose::Words::Drawing::ShapeBase::get_Height](../shapebase/get_height/). |
| [set_HorizontalAlignment](../shapebase/set_horizontalalignment/)(Aspose::Words::Drawing::HorizontalAlignment) | Setter for [Aspose::Words::Drawing::ShapeBase::get_HorizontalAlignment](../shapebase/get_horizontalalignment/). |
| [set_HRef](../shapebase/set_href/)(const System::String\&) | Setter for [Aspose::Words::Drawing::ShapeBase::get_HRef](../shapebase/get_href/). |
| [set_IsDecorative](../shapebase/set_isdecorative/)(bool) | Setter for [Aspose::Words::Drawing::ShapeBase::get_IsDecorative](../shapebase/get_isdecorative/). |
| [set_IsLayoutInCell](../shapebase/set_islayoutincell/)(bool) | Setter for [Aspose::Words::Drawing::ShapeBase::get_IsLayoutInCell](../shapebase/get_islayoutincell/). |
| [set_Left](../shapebase/set_left/)(double) | Setter for [Aspose::Words::Drawing::ShapeBase::get_Left](../shapebase/get_left/). |
| [set_Name](../shapebase/set_name/)(const System::String\&) | Setter for [Aspose::Words::Drawing::ShapeBase::get_Name](../shapebase/get_name/). |
| [set_RelativeHorizontalPosition](../shapebase/set_relativehorizontalposition/)(Aspose::Words::Drawing::RelativeHorizontalPosition) | Setter for [Aspose::Words::Drawing::ShapeBase::get_RelativeHorizontalPosition](../shapebase/get_relativehorizontalposition/). |
| [set_RelativeVerticalPosition](../shapebase/set_relativeverticalposition/)(Aspose::Words::Drawing::RelativeVerticalPosition) | Setter for [Aspose::Words::Drawing::ShapeBase::get_RelativeVerticalPosition](../shapebase/get_relativeverticalposition/). |
| [set_Rotation](../shapebase/set_rotation/)(double) | Setter for [Aspose::Words::Drawing::ShapeBase::get_Rotation](../shapebase/get_rotation/). |
| [set_ScreenTip](../shapebase/set_screentip/)(const System::String\&) | Setter for [Aspose::Words::Drawing::ShapeBase::get_ScreenTip](../shapebase/get_screentip/). |
| [set_Target](../shapebase/set_target/)(const System::String\&) | Setter for [Aspose::Words::Drawing::ShapeBase::get_Target](../shapebase/get_target/). |
| [set_Title](../shapebase/set_title/)(const System::String\&) | Setter for [Aspose::Words::Drawing::ShapeBase::get_Title](../shapebase/get_title/). |
| [set_Top](../shapebase/set_top/)(double) | Setter for [Aspose::Words::Drawing::ShapeBase::get_Top](../shapebase/get_top/). |
| [set_VerticalAlignment](../shapebase/set_verticalalignment/)(Aspose::Words::Drawing::VerticalAlignment) | Setter for [Aspose::Words::Drawing::ShapeBase::get_VerticalAlignment](../shapebase/get_verticalalignment/). |
| [set_Width](../shapebase/set_width/)(double) | Setter for [Aspose::Words::Drawing::ShapeBase::get_Width](../shapebase/get_width/). |
| [set_WrapSide](../shapebase/set_wrapside/)(Aspose::Words::Drawing::WrapSide) | Setter for [Aspose::Words::Drawing::ShapeBase::get_WrapSide](../shapebase/get_wrapside/). |
| [set_WrapType](../shapebase/set_wraptype/)(Aspose::Words::Drawing::WrapType) | Setter for [Aspose::Words::Drawing::ShapeBase::get_WrapType](../shapebase/get_wraptype/). |
| [set_ZOrder](../shapebase/set_zorder/)(int32_t) | Setter for [Aspose::Words::Drawing::ShapeBase::get_ZOrder](../shapebase/get_zorder/). |
| [SetTemplateWeakPtr](../../aspose.words/compositenode/settemplateweakptr/)(uint32_t) override |  |
| [ToString](../../aspose.words/node/tostring/)(Aspose::Words::SaveFormat) | Exports the content of the node into a string in the specified format. |
| [ToString](../../aspose.words/node/tostring/)(const System::SharedPtr\<Aspose::Words::Saving::SaveOptions\>\&) | Exports the content of the node into a string using the specified save options. |
## Remarks


A [GroupShape](./) is a composite node and can have [Shape](../shape/) and [GroupShape](./) nodes as children.

Each [GroupShape](./) defines a new coordinate system for its child shapes. The coordinate system is defined using the [CoordSize](../shapebase/get_coordsize/) and [CoordOrigin](../shapebase/get_coordorigin/) properties.

## Examples



Shows how to create a group of shapes, and print its contents using a document visitor. 
```cpp
void GroupOfShapes()
{
    auto doc = MakeObject<Document>();
    auto builder = MakeObject<DocumentBuilder>(doc);

    // If you need to create "NonPrimitive" shapes, such as SingleCornerSnipped, TopCornersSnipped, DiagonalCornersSnipped,
    // TopCornersOneRoundedOneSnipped, SingleCornerRounded, TopCornersRounded, DiagonalCornersRounded
    // please use DocumentBuilder.InsertShape methods.
    auto balloon = MakeObject<Shape>(doc, ShapeType::Balloon);
    balloon->set_Width(200);
    balloon->set_Height(200);
    balloon->get_Stroke()->set_Color(System::Drawing::Color::get_Red());

    auto cube = MakeObject<Shape>(doc, ShapeType::Cube);
    cube->set_Width(100);
    cube->set_Height(100);
    cube->get_Stroke()->set_Color(System::Drawing::Color::get_Blue());

    auto group = MakeObject<GroupShape>(doc);
    group->AppendChild(balloon);
    group->AppendChild(cube);

    ASSERT_TRUE(group->get_IsGroup());

    builder->InsertNode(group);

    auto printer = MakeObject<ExDrawing::ShapeGroupPrinter>();
    group->Accept(printer);

    std::cout << printer->GetText() << std::endl;
}

class ShapeGroupPrinter : public DocumentVisitor
{
public:
    ShapeGroupPrinter()
    {
        mBuilder = MakeObject<System::Text::StringBuilder>();
    }

    String GetText()
    {
        return mBuilder->ToString();
    }

    VisitorAction VisitGroupShapeStart(SharedPtr<GroupShape> groupShape) override
    {
        mBuilder->AppendLine(u"Shape group started:");
        return VisitorAction::Continue;
    }

    VisitorAction VisitGroupShapeEnd(SharedPtr<GroupShape> groupShape) override
    {
        mBuilder->AppendLine(u"End of shape group");
        return VisitorAction::Continue;
    }

    VisitorAction VisitShapeStart(SharedPtr<Shape> shape) override
    {
        mBuilder->AppendLine(String(u"\tShape - ") + System::ObjectExt::ToString(shape->get_ShapeType()) + u":");
        mBuilder->AppendLine(String(u"\t\tWidth: ") + shape->get_Width());
        mBuilder->AppendLine(String(u"\t\tHeight: ") + shape->get_Height());
        mBuilder->AppendLine(String(u"\t\tStroke color: ") + shape->get_Stroke()->get_Color());
        mBuilder->AppendLine(String(u"\t\tFill color: ") + shape->get_Fill()->get_ForeColor());
        return VisitorAction::Continue;
    }

    VisitorAction VisitShapeEnd(SharedPtr<Shape> shape) override
    {
        mBuilder->AppendLine(u"\tEnd of shape");
        return VisitorAction::Continue;
    }

private:
    SharedPtr<System::Text::StringBuilder> mBuilder;
};
```

## See Also

* Class [ShapeBase](../shapebase/)
* Namespace [Aspose::Words::Drawing](../)
* Library [Aspose.Words](../../)
