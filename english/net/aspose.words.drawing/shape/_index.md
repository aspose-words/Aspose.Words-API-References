---
title: Shape Class
linktitle: Shape
articleTitle: Shape
second_title: Aspose.Words for .NET
description: Aspose.Words.Drawing.Shape class. Represents an object in the drawing layer such as an AutoShape textbox freeform OLE object ActiveX control or picture in C#.
type: docs
weight: 1390
url: /net/aspose.words.drawing/shape/
---
## Shape class

Represents an object in the drawing layer, such as an AutoShape, textbox, freeform, OLE object, ActiveX control, or picture.

To learn more, visit the [Working with Shapes](https://docs.aspose.com/words/net/working-with-shapes/) documentation article.

```csharp
public sealed class Shape : ShapeBase
```

## Constructors

| Name | Description |
| --- | --- |
| [Shape](shape/)(*[DocumentBase](../../aspose.words/documentbase/), [ShapeType](../shapetype/)*) | Creates a new shape object. |

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
| [Chart](../../aspose.words.drawing/shape/chart/) { get; } | Provides access to the chart properties if this shape has a [`Chart`](../../aspose.words.drawing.charts/chart/). |
| [CoordOrigin](../../aspose.words.drawing/shapebase/coordorigin/) { get; set; } | The coordinates at the top-left corner of the containing block of this shape. |
| [CoordSize](../../aspose.words.drawing/shapebase/coordsize/) { get; set; } | The width and height of the coordinate space inside the containing block of this shape. |
| [Count](../../aspose.words/compositenode/count/) { get; } | Gets the number of immediate children of this node. |
| [CustomNodeId](../../aspose.words/node/customnodeid/) { get; set; } | Specifies custom node identifier. |
| [DistanceBottom](../../aspose.words.drawing/shapebase/distancebottom/) { get; set; } | Returns or sets the distance (in points) between the document text and the bottom edge of the shape. |
| [DistanceLeft](../../aspose.words.drawing/shapebase/distanceleft/) { get; set; } | Returns or sets the distance (in points) between the document text and the left edge of the shape. |
| [DistanceRight](../../aspose.words.drawing/shapebase/distanceright/) { get; set; } | Returns or sets the distance (in points) between the document text and the right edge of the shape. |
| [DistanceTop](../../aspose.words.drawing/shapebase/distancetop/) { get; set; } | Returns or sets the distance (in points) between the document text and the top edge of the shape. |
| virtual [Document](../../aspose.words/node/document/) { get; } | Gets the document to which this node belongs. |
| [ExtrusionEnabled](../../aspose.words.drawing/shape/extrusionenabled/) { get; } | Returns `true` if an extrusion effect is enabled. |
| [Fill](../../aspose.words.drawing/shapebase/fill/) { get; } | Gets fill formatting for the shape. |
| [FillColor](../../aspose.words.drawing/shape/fillcolor/) { get; set; } | Defines the brush color that fills the closed path of the shape. |
| [Filled](../../aspose.words.drawing/shape/filled/) { get; set; } | Determines whether the closed path of the shape will be filled. |
| [FirstChild](../../aspose.words/compositenode/firstchild/) { get; } | Gets the first child of the node. |
| [FirstParagraph](../../aspose.words.drawing/shape/firstparagraph/) { get; } | Gets the first paragraph in the shape. |
| [FlipOrientation](../../aspose.words.drawing/shapebase/fliporientation/) { get; set; } | Switches the orientation of a shape. |
| [Font](../../aspose.words.drawing/shapebase/font/) { get; } | Provides access to the font formatting of this object. |
| [Glow](../../aspose.words.drawing/shapebase/glow/) { get; } | Gets glow formatting for the shape. |
| [HasChart](../../aspose.words.drawing/shape/haschart/) { get; } | Returns `true` if this `Shape` has a [`Chart`](../../aspose.words.drawing.charts/chart/). |
| [HasChildNodes](../../aspose.words/compositenode/haschildnodes/) { get; } | Returns `true` if this node has any child nodes. |
| [HasImage](../../aspose.words.drawing/shape/hasimage/) { get; } | Returns `true` if the shape has image bytes or links an image. |
| [HasSmartArt](../../aspose.words.drawing/shape/hassmartart/) { get; } | Returns `true` if this `Shape` has a SmartArt object. |
| [Height](../../aspose.words.drawing/shapebase/height/) { get; set; } | Gets or sets the height of the containing block of the shape. |
| [HeightRelative](../../aspose.words.drawing/shapebase/heightrelative/) { get; set; } | Gets or sets the value that represents the percentage of shape's relative height. |
| [HorizontalAlignment](../../aspose.words.drawing/shapebase/horizontalalignment/) { get; set; } | Specifies how the shape is positioned horizontally. |
| [HorizontalRuleFormat](../../aspose.words.drawing/shape/horizontalruleformat/) { get; } | Provides access to the properties of the horizontal rule shape. For a shape that is not a horizontal rule, returns `null`. |
| [HRef](../../aspose.words.drawing/shapebase/href/) { get; set; } | Gets or sets the full hyperlink address for a shape. |
| [ImageData](../../aspose.words.drawing/shape/imagedata/) { get; } | Provides access to the image of the shape. Returns `null` if the shape cannot have an image. |
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
| [LastParagraph](../../aspose.words.drawing/shape/lastparagraph/) { get; } | Gets the last paragraph in the shape. |
| [Left](../../aspose.words.drawing/shapebase/left/) { get; set; } | Gets or sets the position of the left edge of the containing block of the shape. |
| [LeftRelative](../../aspose.words.drawing/shapebase/leftrelative/) { get; set; } | Gets or sets the value that represents shape's relative left position in percent. |
| [MarkupLanguage](../../aspose.words.drawing/shapebase/markuplanguage/) { get; } | Gets MarkupLanguage used for this graphic object. |
| [Name](../../aspose.words.drawing/shapebase/name/) { get; set; } | Gets or sets the optional shape name. |
| [NextSibling](../../aspose.words/node/nextsibling/) { get; } | Gets the node immediately following this node. |
| override [NodeType](../../aspose.words.drawing/shape/nodetype/) { get; } | Returns Shape. |
| [OleFormat](../../aspose.words.drawing/shape/oleformat/) { get; } | Provides access to the OLE data of a shape. For a shape that is not an OLE object or ActiveX control, returns `null`. |
| [ParentNode](../../aspose.words/node/parentnode/) { get; } | Gets the immediate parent of this node. |
| [ParentParagraph](../../aspose.words.drawing/shapebase/parentparagraph/) { get; } | Returns the immediate parent paragraph. |
| [PreviousSibling](../../aspose.words/node/previoussibling/) { get; } | Gets the node immediately preceding this node. |
| [Range](../../aspose.words/node/range/) { get; } | Returns a [`Range`](../../aspose.words/range/) object that represents the portion of a document that is contained in this node. |
| [Reflection](../../aspose.words.drawing/shapebase/reflection/) { get; } | Gets reflection formatting for the shape. |
| [RelativeHorizontalPosition](../../aspose.words.drawing/shapebase/relativehorizontalposition/) { get; set; } | Specifies relative to what the shape is positioned horizontally. |
| [RelativeHorizontalSize](../../aspose.words.drawing/shapebase/relativehorizontalsize/) { get; set; } | Gets or sets the value of shape's relative size in horizontal direction. |
| [RelativeVerticalPosition](../../aspose.words.drawing/shapebase/relativeverticalposition/) { get; set; } | Specifies relative to what the shape is positioned vertically. |
| [RelativeVerticalSize](../../aspose.words.drawing/shapebase/relativeverticalsize/) { get; set; } | Gets or sets the value of shape's relative size in vertical direction. |
| [Right](../../aspose.words.drawing/shapebase/right/) { get; } | Gets the position of the right edge of the containing block of the shape. |
| [Rotation](../../aspose.words.drawing/shapebase/rotation/) { get; set; } | Defines the angle (in degrees) that a shape is rotated. Positive value corresponds to clockwise rotation angle. |
| [ScreenTip](../../aspose.words.drawing/shapebase/screentip/) { get; set; } | Defines the text displayed when the mouse pointer moves over the shape. |
| [ShadowEnabled](../../aspose.words.drawing/shape/shadowenabled/) { get; } | Returns `true` if a shadow effect is enabled. |
| [ShadowFormat](../../aspose.words.drawing/shapebase/shadowformat/) { get; } | Gets shadow formatting for the shape. |
| [ShapeType](../../aspose.words.drawing/shapebase/shapetype/) { get; } | Gets the shape type. |
| [SignatureLine](../../aspose.words.drawing/shape/signatureline/) { get; } | Gets [`SignatureLine`](../signatureline/) object if the shape is a signature line. Returns `null` otherwise. |
| [SizeInPoints](../../aspose.words.drawing/shapebase/sizeinpoints/) { get; } | Gets the size of the shape in points. |
| [StoryType](../../aspose.words.drawing/shape/storytype/) { get; } | Returns Textbox. |
| [Stroke](../../aspose.words.drawing/shape/stroke/) { get; } | Defines a stroke for a shape. |
| [StrokeColor](../../aspose.words.drawing/shape/strokecolor/) { get; set; } | Defines the color of a stroke. |
| [Stroked](../../aspose.words.drawing/shape/stroked/) { get; set; } | Defines whether the path will be stroked. |
| [StrokeWeight](../../aspose.words.drawing/shape/strokeweight/) { get; set; } | Defines the brush thickness that strokes the path of a shape in points. |
| [Target](../../aspose.words.drawing/shapebase/target/) { get; set; } | Gets or sets the target frame for the shape hyperlink. |
| [TextBox](../../aspose.words.drawing/shape/textbox/) { get; } | Defines attributes that specify how text is displayed in a shape. |
| [TextPath](../../aspose.words.drawing/shape/textpath/) { get; } | Defines the text of the text path (of a WordArt object). |
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
| override [Accept](../../aspose.words.drawing/shape/accept/)(*[DocumentVisitor](../../aspose.words/documentvisitor/)*) | Accepts a visitor. |
| override [AcceptEnd](../../aspose.words.drawing/shape/acceptend/)(*[DocumentVisitor](../../aspose.words/documentvisitor/)*) | Accepts a visitor for visiting the end of the shape. |
| override [AcceptStart](../../aspose.words.drawing/shape/acceptstart/)(*[DocumentVisitor](../../aspose.words/documentvisitor/)*) | Accepts a visitor for visiting the start of the shape. |
| [AdjustWithEffects](../../aspose.words.drawing/shapebase/adjustwitheffects/)(*RectangleF*) | Adds to the source rectangle values of the effect extent and returns the final rectangle. |
| [AppendChild&lt;T&gt;](../../aspose.words/compositenode/appendchild/)(*T*) | Adds the specified node to the end of the list of child nodes for this node. |
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
| [InsertAfter&lt;T&gt;](../../aspose.words/compositenode/insertafter/)(*T, [Node](../../aspose.words/node/)*) | Inserts the specified node immediately after the specified reference node. |
| [InsertBefore&lt;T&gt;](../../aspose.words/compositenode/insertbefore/)(*T, [Node](../../aspose.words/node/)*) | Inserts the specified node immediately before the specified reference node. |
| [LocalToParent](../../aspose.words.drawing/shapebase/localtoparent/)(*PointF*) | Converts a value from the local coordinate space into the coordinate space of the parent shape. |
| [NextPreOrder](../../aspose.words/node/nextpreorder/)(*[Node](../../aspose.words/node/)*) | Gets next node according to the pre-order tree traversal algorithm. |
| [PrependChild&lt;T&gt;](../../aspose.words/compositenode/prependchild/)(*T*) | Adds the specified node to the beginning of the list of child nodes for this node. |
| [PreviousPreOrder](../../aspose.words/node/previouspreorder/)(*[Node](../../aspose.words/node/)*) | Gets the previous node according to the pre-order tree traversal algorithm. |
| [Remove](../../aspose.words/node/remove/)() | Removes itself from the parent. |
| [RemoveAllChildren](../../aspose.words/compositenode/removeallchildren/)() | Removes all the child nodes of the current node. |
| [RemoveChild&lt;T&gt;](../../aspose.words/compositenode/removechild/)(*T*) | Removes the specified child node. |
| [RemoveShapeAttr](../../aspose.words.drawing/shapebase/removeshapeattr/)(*int*) | Reserved for system use. IShapeAttrSource. |
| [RemoveSmartTags](../../aspose.words/compositenode/removesmarttags/)() | Removes all [`SmartTag`](../../aspose.words.markup/smarttag/) descendant nodes of the current node. |
| [SelectNodes](../../aspose.words/compositenode/selectnodes/)(*string*) | Selects a list of nodes matching the XPath expression. |
| [SelectSingleNode](../../aspose.words/compositenode/selectsinglenode/)(*string*) | Selects the first [`Node`](../../aspose.words/node/) that matches the XPath expression. |
| [SetShapeAttr](../../aspose.words.drawing/shapebase/setshapeattr/)(*int, object*) | Reserved for system use. IShapeAttrSource. |
| [ToString](../../aspose.words/node/tostring/)(*[SaveFormat](../../aspose.words/saveformat/)*) | Exports the content of the node into a string in the specified format. |
| [ToString](../../aspose.words/node/tostring/)(*[SaveOptions](../../aspose.words.saving/saveoptions/)*) | Exports the content of the node into a string using the specified save options. |
| [UpdateSmartArtDrawing](../../aspose.words.drawing/shape/updatesmartartdrawing/)() | Updates SmartArt pre-rendered drawing by using Aspose.Words's SmartArt cold rendering engine. |

## Remarks

Using the `Shape` class you can create or modify shapes in a Microsoft Word document.

An important property of a shape is its [`ShapeType`](../shapebase/shapetype/). Shapes of different types can have different capabilities in a Word document. For example, only image and OLE shapes can have images inside them. Most of the shapes can have text, but not all.

Shapes that can have text, can contain [`Paragraph`](../../aspose.words/paragraph/) and [`Table`](../../aspose.words.tables/table/) nodes as children.

## Examples

Shows how to insert a floating image to the center of a page.

```csharp
Document doc = new Document();
DocumentBuilder builder = new DocumentBuilder(doc);

// Insert a floating image that will appear behind the overlapping text and align it to the page's center.
Shape shape = builder.InsertImage(ImageDir + "Logo.jpg");
shape.WrapType = WrapType.None;
shape.BehindText = true;
shape.RelativeHorizontalPosition = RelativeHorizontalPosition.Page;
shape.RelativeVerticalPosition = RelativeVerticalPosition.Page;
shape.HorizontalAlignment = HorizontalAlignment.Center;
shape.VerticalAlignment = VerticalAlignment.Center;

doc.Save(ArtifactsDir + "Image.CreateFloatingPageCenter.docx");
```

Shows how to extract images from a document, and save them to the local file system as individual files.

```csharp
Document doc = new Document(MyDir + "Images.docx");

// Get the collection of shapes from the document,
// and save the image data of every shape with an image as a file to the local file system.
NodeCollection shapes = doc.GetChildNodes(NodeType.Shape, true);

Assert.AreEqual(9, shapes.Count(s => ((Shape)s).HasImage));

int imageIndex = 0;
foreach (Shape shape in shapes.OfType<Shape>())
{
    if (shape.HasImage)
    {
        // The image data of shapes may contain images of many possible image formats. 
        // We can determine a file extension for each image automatically, based on its format.
        string imageFileName =
            $"File.ExtractImages.{imageIndex}{FileFormatUtil.ImageTypeToExtension(shape.ImageData.ImageType)}";
        shape.ImageData.Save(ArtifactsDir + imageFileName);
        imageIndex++;
    }
}
```

Shows how to delete all shapes from a document.

```csharp
Document doc = new Document();
DocumentBuilder builder = new DocumentBuilder(doc);

// Insert two shapes along with a group shape with another shape inside it.
builder.InsertShape(ShapeType.Rectangle, 400, 200);
builder.InsertShape(ShapeType.Star, 300, 300);

GroupShape group = new GroupShape(doc);
group.Bounds = new RectangleF(100, 50, 200, 100);
group.CoordOrigin = new Point(-1000, -500);

Shape subShape = new Shape(doc, ShapeType.Cube);
subShape.Width = 500;
subShape.Height = 700;
subShape.Left = 0;
subShape.Top = 0;

group.AppendChild(subShape);
builder.InsertNode(group);

Assert.AreEqual(3, doc.GetChildNodes(NodeType.Shape, true).Count);
Assert.AreEqual(1, doc.GetChildNodes(NodeType.GroupShape, true).Count);

// Remove all Shape nodes from the document.
NodeCollection shapes = doc.GetChildNodes(NodeType.Shape, true);
shapes.Clear();

// All shapes are gone, but the group shape is still in the document.
Assert.AreEqual(1, doc.GetChildNodes(NodeType.GroupShape, true).Count);
Assert.AreEqual(0, doc.GetChildNodes(NodeType.Shape, true).Count);

// Remove all group shapes separately.
NodeCollection groupShapes = doc.GetChildNodes(NodeType.GroupShape, true);
groupShapes.Clear();

Assert.AreEqual(0, doc.GetChildNodes(NodeType.GroupShape, true).Count);
Assert.AreEqual(0, doc.GetChildNodes(NodeType.Shape, true).Count);
```

### See Also

* class [ShapeBase](../shapebase/)
* namespace [Aspose.Words.Drawing](../../aspose.words.drawing/)
* assembly [Aspose.Words](../../)
