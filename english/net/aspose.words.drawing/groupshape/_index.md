---
title: GroupShape Class
linktitle: GroupShape
articleTitle: GroupShape
second_title: Aspose.Words for .NET
description: Aspose.Words.Drawing.GroupShape class. Represents a group of shapes in a document in C#.
type: docs
weight: 1020
url: /net/aspose.words.drawing/groupshape/
---
## GroupShape class

Represents a group of shapes in a document.

To learn more, visit the [How to Add Group Shape into a Word Document](https://docs.aspose.com/words/net/how-to-add-group-shape-into-a-word-document/) documentation article.

```csharp
public class GroupShape : ShapeBase
```

## Constructors

| Name | Description |
| --- | --- |
| [GroupShape](groupshape/)(*[DocumentBase](../../aspose.words/documentbase/)*) | Creates a new group shape. |

## Properties

| Name | Description |
| --- | --- |
| [AllowOverlap](../../aspose.words.drawing/shapebase/allowoverlap/) { get; set; } | Gets or sets a value that specifies whether this shape can overlap other shapes. |
| [AlternativeText](../../aspose.words.drawing/shapebase/alternativetext/) { get; set; } | Defines alternative text to be displayed instead of a graphic. |
| [AnchorLocked](../../aspose.words.drawing/shapebase/anchorlocked/) { get; set; } | Specifies whether the shape's anchor is locked. |
| [AspectRatioLocked](../../aspose.words.drawing/shapebase/aspectratiolocked/) { get; set; } | Specifies whether the shape's aspect ratio is locked. |
| [BehindText](../../aspose.words.drawing/shapebase/behindtext/) { get; set; } | Specifies whether the shape is below or above text. |
| [Bottom](../../aspose.words.drawing/shapebase/bottom/) { get; } | Gets the position of the bottom edge of the containing block of the shape. |
| [Bounds](../../aspose.words.drawing/shapebase/bounds/) { get; set; } | Gets or sets the location and size of the containing block of the shape. |
| [BoundsInPoints](../../aspose.words.drawing/shapebase/boundsinpoints/) { get; } | Gets the location and size of the containing block of the shape in points, relative to the anchor of the topmost shape. |
| [BoundsWithEffects](../../aspose.words.drawing/shapebase/boundswitheffects/) { get; } | Gets final extent that this shape object has after applying drawing effects. Value is measured in points. |
| [CanHaveImage](../../aspose.words.drawing/shapebase/canhaveimage/) { get; } | Returns `true` if the shape type allows the shape to have an image. |
| [CoordOrigin](../../aspose.words.drawing/shapebase/coordorigin/) { get; set; } | The coordinates at the top-left corner of the containing block of this shape. |
| [CoordSize](../../aspose.words.drawing/shapebase/coordsize/) { get; set; } | The width and height of the coordinate space inside the containing block of this shape. |
| [Count](../../aspose.words/compositenode/count/) { get; } | Gets the number of immediate children of this node. |
| [CustomNodeId](../../aspose.words/node/customnodeid/) { get; set; } | Specifies custom node identifier. |
| [DistanceBottom](../../aspose.words.drawing/shapebase/distancebottom/) { get; set; } | Returns or sets the distance (in points) between the document text and the bottom edge of the shape. |
| [DistanceLeft](../../aspose.words.drawing/shapebase/distanceleft/) { get; set; } | Returns or sets the distance (in points) between the document text and the left edge of the shape. |
| [DistanceRight](../../aspose.words.drawing/shapebase/distanceright/) { get; set; } | Returns or sets the distance (in points) between the document text and the right edge of the shape. |
| [DistanceTop](../../aspose.words.drawing/shapebase/distancetop/) { get; set; } | Returns or sets the distance (in points) between the document text and the top edge of the shape. |
| virtual [Document](../../aspose.words/node/document/) { get; } | Gets the document to which this node belongs. |
| [Fill](../../aspose.words.drawing/shapebase/fill/) { get; } | Gets fill formatting for the shape. |
| [FirstChild](../../aspose.words/compositenode/firstchild/) { get; } | Gets the first child of the node. |
| [FlipOrientation](../../aspose.words.drawing/shapebase/fliporientation/) { get; set; } | Switches the orientation of a shape. |
| [Font](../../aspose.words.drawing/shapebase/font/) { get; } | Provides access to the font formatting of this object. |
| [HasChildNodes](../../aspose.words/compositenode/haschildnodes/) { get; } | Returns `true` if this node has any child nodes. |
| [Height](../../aspose.words.drawing/shapebase/height/) { get; set; } | Gets or sets the height of the containing block of the shape. |
| [HeightRelative](../../aspose.words.drawing/shapebase/heightrelative/) { get; set; } | Gets or sets the value that represents the percentage of shape's relative height. |
| [HorizontalAlignment](../../aspose.words.drawing/shapebase/horizontalalignment/) { get; set; } | Specifies how the shape is positioned horizontally. |
| [HRef](../../aspose.words.drawing/shapebase/href/) { get; set; } | Gets or sets the full hyperlink address for a shape. |
| override [IsComposite](../../aspose.words/compositenode/iscomposite/) { get; } | Returns `true` as this node can have child nodes. |
| [IsDecorative](../../aspose.words.drawing/shapebase/isdecorative/) { get; set; } | Gets or sets the flag that specifies whether the shape is decorative in the document. |
| [IsDeleteRevision](../../aspose.words.drawing/shapebase/isdeleterevision/) { get; } | Returns true if this object was deleted in Microsoft Word while change tracking was enabled. |
| [IsGroup](../../aspose.words.drawing/shapebase/isgroup/) { get; } | Returns `true` if this is a group shape. |
| [IsHorizontalRule](../../aspose.words.drawing/shapebase/ishorizontalrule/) { get; } | Returns `true` if this shape is a horizontal rule. |
| [IsImage](../../aspose.words.drawing/shapebase/isimage/) { get; } | Returns `true` if this shape is an image shape. |
| [IsInline](../../aspose.words.drawing/shapebase/isinline/) { get; } | A quick way to determine if this shape is positioned inline with text. |
| [IsInsertRevision](../../aspose.words.drawing/shapebase/isinsertrevision/) { get; } | Returns true if this object was inserted in Microsoft Word while change tracking was enabled. |
| [IsLayoutInCell](../../aspose.words.drawing/shapebase/islayoutincell/) { get; set; } | Gets or sets a flag indicating whether the shape is displayed inside a table or outside of it. |
| [IsMoveFromRevision](../../aspose.words.drawing/shapebase/ismovefromrevision/) { get; } | Returns `true` if this object was moved (deleted) in Microsoft Word while change tracking was enabled. |
| [IsMoveToRevision](../../aspose.words.drawing/shapebase/ismovetorevision/) { get; } | Returns `true` if this object was moved (inserted) in Microsoft Word while change tracking was enabled. |
| [IsSignatureLine](../../aspose.words.drawing/shapebase/issignatureline/) { get; } | Indicates that shape is a [`SignatureLine`](../signatureline/). |
| [IsTopLevel](../../aspose.words.drawing/shapebase/istoplevel/) { get; } | Returns `true` if this shape is not a child of a group shape. |
| [IsWordArt](../../aspose.words.drawing/shapebase/iswordart/) { get; } | Returns `true` if this shape is a WordArt object. |
| [LastChild](../../aspose.words/compositenode/lastchild/) { get; } | Gets the last child of the node. |
| [Left](../../aspose.words.drawing/shapebase/left/) { get; set; } | Gets or sets the position of the left edge of the containing block of the shape. |
| [LeftRelative](../../aspose.words.drawing/shapebase/leftrelative/) { get; set; } | Gets or sets the value that represents shape's relative left position in percent. |
| [MarkupLanguage](../../aspose.words.drawing/shapebase/markuplanguage/) { get; } | Gets MarkupLanguage used for this graphic object. |
| [Name](../../aspose.words.drawing/shapebase/name/) { get; set; } | Gets or sets the optional shape name. |
| [NextSibling](../../aspose.words/node/nextsibling/) { get; } | Gets the node immediately following this node. |
| override [NodeType](../../aspose.words.drawing/groupshape/nodetype/) { get; } | Returns GroupShape. |
| [ParentNode](../../aspose.words/node/parentnode/) { get; } | Gets the immediate parent of this node. |
| [ParentParagraph](../../aspose.words.drawing/shapebase/parentparagraph/) { get; } | Returns the immediate parent paragraph. |
| [PreviousSibling](../../aspose.words/node/previoussibling/) { get; } | Gets the node immediately preceding this node. |
| [Range](../../aspose.words/node/range/) { get; } | Returns a [`Range`](../../aspose.words/range/) object that represents the portion of a document that is contained in this node. |
| [RelativeHorizontalPosition](../../aspose.words.drawing/shapebase/relativehorizontalposition/) { get; set; } | Specifies relative to what the shape is positioned horizontally. |
| [RelativeHorizontalSize](../../aspose.words.drawing/shapebase/relativehorizontalsize/) { get; set; } | Gets or sets the value of shape's relative size in horizontal direction. |
| [RelativeVerticalPosition](../../aspose.words.drawing/shapebase/relativeverticalposition/) { get; set; } | Specifies relative to what the shape is positioned vertically. |
| [RelativeVerticalSize](../../aspose.words.drawing/shapebase/relativeverticalsize/) { get; set; } | Gets or sets the value of shape's relative size in vertical direction. |
| [Right](../../aspose.words.drawing/shapebase/right/) { get; } | Gets the position of the right edge of the containing block of the shape. |
| [Rotation](../../aspose.words.drawing/shapebase/rotation/) { get; set; } | Defines the angle (in degrees) that a shape is rotated. Positive value corresponds to clockwise rotation angle. |
| [ScreenTip](../../aspose.words.drawing/shapebase/screentip/) { get; set; } | Defines the text displayed when the mouse pointer moves over the shape. |
| [ShadowFormat](../../aspose.words.drawing/shapebase/shadowformat/) { get; } | Gets shadow formatting for the shape. |
| [ShapeType](../../aspose.words.drawing/shapebase/shapetype/) { get; } | Gets the shape type. |
| [SizeInPoints](../../aspose.words.drawing/shapebase/sizeinpoints/) { get; } | Gets the size of the shape in points. |
| [Target](../../aspose.words.drawing/shapebase/target/) { get; set; } | Gets or sets the target frame for the shape hyperlink. |
| [Title](../../aspose.words.drawing/shapebase/title/) { get; set; } | Gets or sets the title (caption) of the current shape object. |
| [Top](../../aspose.words.drawing/shapebase/top/) { get; set; } | Gets or sets the position of the top edge of the containing block of the shape. |
| [TopRelative](../../aspose.words.drawing/shapebase/toprelative/) { get; set; } | Gets or sets the value that represents shape's relative top position in percent. |
| [VerticalAlignment](../../aspose.words.drawing/shapebase/verticalalignment/) { get; set; } | Specifies how the shape is positioned vertically. |
| [Width](../../aspose.words.drawing/shapebase/width/) { get; set; } | Gets or sets the width of the containing block of the shape. |
| [WidthRelative](../../aspose.words.drawing/shapebase/widthrelative/) { get; set; } | Gets or sets the value that represents the percentage of shape's relative width. |
| [WrapSide](../../aspose.words.drawing/shapebase/wrapside/) { get; set; } | Specifies how the text is wrapped around the shape. |
| [WrapType](../../aspose.words.drawing/shapebase/wraptype/) { get; set; } | Defines whether the shape is inline or floating. For floating shapes defines the wrapping mode for text around the shape. |
| [ZOrder](../../aspose.words.drawing/shapebase/zorder/) { get; set; } | Determines the display order of overlapping shapes. |

## Methods

| Name | Description |
| --- | --- |
| override [Accept](../../aspose.words.drawing/groupshape/accept/)(*[DocumentVisitor](../../aspose.words/documentvisitor/)*) | Accepts a visitor. |
| [AdjustWithEffects](../../aspose.words.drawing/shapebase/adjustwitheffects/)(*RectangleF*) | Adds to the source rectangle values of the effect extent and returns the final rectangle. |
| [AppendChild](../../aspose.words/compositenode/appendchild/)(*[Node](../../aspose.words/node/)*) | Adds the specified node to the end of the list of child nodes for this node. |
| [Clone](../../aspose.words/node/clone/)(*bool*) | Creates a duplicate of the node. |
| [CreateNavigator](../../aspose.words/compositenode/createnavigator/)() | Creates navigator which can be used to traverse and read nodes. |
| [FetchInheritedShapeAttr](../../aspose.words.drawing/shapebase/fetchinheritedshapeattr/)(*int*) | Reserved for system use. IShapeAttrSource. |
| [FetchShapeAttr](../../aspose.words.drawing/shapebase/fetchshapeattr/)(*int*) | Reserved for system use. IShapeAttrSource. |
| [GetAncestor](../../aspose.words/node/getancestor/)(*[NodeType](../../aspose.words/nodetype/)*) | Gets the first ancestor of the specified [`NodeType`](../../aspose.words/nodetype/). |
| [GetAncestor](../../aspose.words/node/getancestor/)(*Type*) | Gets the first ancestor of the specified object type. |
| [GetChild](../../aspose.words/compositenode/getchild/)(*[NodeType](../../aspose.words/nodetype/), int, bool*) | Returns an Nth child node that matches the specified type. |
| [GetChildNodes](../../aspose.words/compositenode/getchildnodes/)(*[NodeType](../../aspose.words/nodetype/), bool*) | Returns a live collection of child nodes that match the specified type. |
| [GetDirectShapeAttr](../../aspose.words.drawing/shapebase/getdirectshapeattr/)(*int*) | Reserved for system use. IShapeAttrSource. |
| [GetEnumerator](../../aspose.words/compositenode/getenumerator/)() | Provides support for the for each style iteration over the child nodes of this node. |
| [GetShapeRenderer](../../aspose.words.drawing/shapebase/getshaperenderer/)() | Creates and returns an object that can be used to render this shape into an image. |
| override [GetText](../../aspose.words/compositenode/gettext/)() | Gets the text of this node and of all its children. |
| [IndexOf](../../aspose.words/compositenode/indexof/)(*[Node](../../aspose.words/node/)*) | Returns the index of the specified child node in the child node array. |
| [InsertAfter](../../aspose.words/compositenode/insertafter/)(*[Node](../../aspose.words/node/), [Node](../../aspose.words/node/)*) | Inserts the specified node immediately after the specified reference node. |
| [InsertBefore](../../aspose.words/compositenode/insertbefore/)(*[Node](../../aspose.words/node/), [Node](../../aspose.words/node/)*) | Inserts the specified node immediately before the specified reference node. |
| [LocalToParent](../../aspose.words.drawing/shapebase/localtoparent/)(*PointF*) | Converts a value from the local coordinate space into the coordinate space of the parent shape. |
| [NextPreOrder](../../aspose.words/node/nextpreorder/)(*[Node](../../aspose.words/node/)*) | Gets next node according to the pre-order tree traversal algorithm. |
| [PrependChild](../../aspose.words/compositenode/prependchild/)(*[Node](../../aspose.words/node/)*) | Adds the specified node to the beginning of the list of child nodes for this node. |
| [PreviousPreOrder](../../aspose.words/node/previouspreorder/)(*[Node](../../aspose.words/node/)*) | Gets the previous node according to the pre-order tree traversal algorithm. |
| [Remove](../../aspose.words/node/remove/)() | Removes itself from the parent. |
| [RemoveAllChildren](../../aspose.words/compositenode/removeallchildren/)() | Removes all the child nodes of the current node. |
| [RemoveChild](../../aspose.words/compositenode/removechild/)(*[Node](../../aspose.words/node/)*) | Removes the specified child node. |
| [RemoveShapeAttr](../../aspose.words.drawing/shapebase/removeshapeattr/)(*int*) | Reserved for system use. IShapeAttrSource. |
| [RemoveSmartTags](../../aspose.words/compositenode/removesmarttags/)() | Removes all [`SmartTag`](../../aspose.words.markup/smarttag/) descendant nodes of the current node. |
| [SelectNodes](../../aspose.words/compositenode/selectnodes/)(*string*) | Selects a list of nodes matching the XPath expression. |
| [SelectSingleNode](../../aspose.words/compositenode/selectsinglenode/)(*string*) | Selects the first [`Node`](../../aspose.words/node/) that matches the XPath expression. |
| [SetShapeAttr](../../aspose.words.drawing/shapebase/setshapeattr/)(*int, object*) | Reserved for system use. IShapeAttrSource. |
| [ToString](../../aspose.words/node/tostring/)(*[SaveFormat](../../aspose.words/saveformat/)*) | Exports the content of the node into a string in the specified format. |
| [ToString](../../aspose.words/node/tostring/)(*[SaveOptions](../../aspose.words.saving/saveoptions/)*) | Exports the content of the node into a string using the specified save options. |

## Remarks

A `GroupShape` is a composite node and can have [`Shape`](../shape/) and `GroupShape` nodes as children.

Each `GroupShape` defines a new coordinate system for its child shapes. The coordinate system is defined using the [`CoordSize`](../shapebase/coordsize/) and [`CoordOrigin`](../shapebase/coordorigin/) properties.

## Examples

Shows how to create a group of shapes, and print its contents using a document visitor.

```csharp
public void GroupOfShapes()
{
    Document doc = new Document();
    DocumentBuilder builder = new DocumentBuilder(doc);

    // If you need to create "NonPrimitive" shapes, such as SingleCornerSnipped, TopCornersSnipped, DiagonalCornersSnipped,
    // TopCornersOneRoundedOneSnipped, SingleCornerRounded, TopCornersRounded, DiagonalCornersRounded
    // please use DocumentBuilder.InsertShape methods.
    Shape balloon = new Shape(doc, ShapeType.Balloon)
    {
        Width = 200, 
        Height = 200,
        Stroke = { Color = Color.Red }
    };

    Shape cube = new Shape(doc, ShapeType.Cube)
    {
        Width = 100, 
        Height = 100,
        Stroke = { Color = Color.Blue }
    };

    GroupShape group = new GroupShape(doc);
    group.AppendChild(balloon);
    group.AppendChild(cube);

    Assert.True(group.IsGroup);

    builder.InsertNode(group);

    ShapeGroupPrinter printer = new ShapeGroupPrinter();
    group.Accept(printer);

    Console.WriteLine(printer.GetText());
}

/// <summary>
/// Prints the contents of a visited shape group to the console.
/// </summary>
public class ShapeGroupPrinter : DocumentVisitor
{
    public ShapeGroupPrinter()
    {
        mBuilder = new StringBuilder();
    }

    public string GetText()
    {
        return mBuilder.ToString();
    }

    public override VisitorAction VisitGroupShapeStart(GroupShape groupShape)
    {
        mBuilder.AppendLine("Shape group started:");
        return VisitorAction.Continue;
    }

    public override VisitorAction VisitGroupShapeEnd(GroupShape groupShape)
    {
        mBuilder.AppendLine("End of shape group");
        return VisitorAction.Continue;
    }

    public override VisitorAction VisitShapeStart(Shape shape)
    {
        mBuilder.AppendLine("\tShape - " + shape.ShapeType + ":");
        mBuilder.AppendLine("\t\tWidth: " + shape.Width);
        mBuilder.AppendLine("\t\tHeight: " + shape.Height);
        mBuilder.AppendLine("\t\tStroke color: " + shape.Stroke.Color);
        mBuilder.AppendLine("\t\tFill color: " + shape.Fill.ForeColor);
        return VisitorAction.Continue;
    }

    public override VisitorAction VisitShapeEnd(Shape shape)
    {
        mBuilder.AppendLine("\tEnd of shape");
        return VisitorAction.Continue;
    }

    private readonly StringBuilder mBuilder;
}
```

### See Also

* class [ShapeBase](../shapebase/)
* namespace [Aspose.Words.Drawing](../../aspose.words.drawing/)
* assembly [Aspose.Words](../../)
