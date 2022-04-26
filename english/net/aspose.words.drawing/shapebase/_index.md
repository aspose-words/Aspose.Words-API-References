---
title: ShapeBase
second_title: Aspose.Words for .NET API Reference
description: 
type: docs
weight: 1060
url: /net/aspose.words.drawing/shapebase/
---
## ShapeBase class

Base class for objects in the drawing layer, such as an AutoShape, freeform, OLE object, ActiveX control, or picture.

```csharp
public abstract class ShapeBase : CompositeNode
```

## Properties

| Name | Description |
| --- | --- |
| [AllowOverlap](allowoverlap) { get; set; } | Gets or sets a value that specifies whether this shape can overlap other shapes. |
| [AlternativeText](alternativetext) { get; set; } | Defines alternative text to be displayed instead of a graphic. |
| [AnchorLocked](anchorlocked) { get; set; } | Specifies whether the shape's anchor is locked. |
| [AspectRatioLocked](aspectratiolocked) { get; set; } | Specifies whether the shape's aspect ratio is locked. |
| [BehindText](behindtext) { get; set; } | Specifies whether the shape is below or above text. |
| [Bottom](bottom) { get; } | Gets the position of the bottom edge of the containing block of the shape. |
| [Bounds](bounds) { get; set; } | Gets or sets the location and size of the containing block of the shape. |
| [BoundsInPoints](boundsinpoints) { get; } | Gets the location and size of the containing block of the shape in points, relative to the anchor of the topmost shape. |
| [BoundsWithEffects](boundswitheffects) { get; } | Gets final extent that this shape object has after applying drawing effects. Value is measured in points. |
| [CanHaveImage](canhaveimage) { get; } | Returns true if the shape type allows the shape to have an image. |
| [CoordOrigin](coordorigin) { get; set; } | The coordinates at the top-left corner of the containing block of this shape. |
| [CoordSize](coordsize) { get; set; } | The width and height of the coordinate space inside the containing block of this shape. |
| [DistanceBottom](distancebottom) { get; set; } | Returns or sets the distance (in points) between the document text and the bottom edge of the shape. |
| [DistanceLeft](distanceleft) { get; set; } | Returns or sets the distance (in points) between the document text and the left edge of the shape. |
| [DistanceRight](distanceright) { get; set; } | Returns or sets the distance (in points) between the document text and the right edge of the shape. |
| [DistanceTop](distancetop) { get; set; } | Returns or sets the distance (in points) between the document text and the top edge of the shape. |
| [Fill](fill) { get; } | Gets fill formatting for the shape. |
| [FlipOrientation](fliporientation) { get; set; } | Switches the orientation of a shape. |
| [Font](font) { get; } | Provides access to the font formatting of this object. |
| [Height](height) { get; set; } | Gets or sets the height of the containing block of the shape. |
| [HorizontalAlignment](horizontalalignment) { get; set; } | Specifies how the shape is positioned horizontally. |
| [HRef](href) { get; set; } | Gets or sets the full hyperlink address for a shape. |
| [IsDecorative](isdecorative) { get; set; } | Gets or sets the flag that specifies whether the shape is decorative in the document. |
| [IsDeleteRevision](isdeleterevision) { get; } | Returns true if this object was deleted in Microsoft Word while change tracking was enabled. |
| [IsGroup](isgroup) { get; } | Returns true if this is a group shape. |
| [IsHorizontalRule](ishorizontalrule) { get; } | Returns true if this shape is a horizontal rule. |
| [IsImage](isimage) { get; } | Returns true if this shape is an image shape. |
| [IsInline](isinline) { get; } | A quick way to determine if this shape is positioned inline with text. |
| [IsInsertRevision](isinsertrevision) { get; } | Returns true if this object was inserted in Microsoft Word while change tracking was enabled. |
| [IsLayoutInCell](islayoutincell) { get; set; } | Gets or sets a flag indicating whether the shape is displayed inside a table or outside of it. |
| [IsMoveFromRevision](ismovefromrevision) { get; } | Returns **true** if this object was moved (deleted) in Microsoft Word while change tracking was enabled. |
| [IsMoveToRevision](ismovetorevision) { get; } | Returns **true** if this object was moved (inserted) in Microsoft Word while change tracking was enabled. |
| [IsSignatureLine](issignatureline) { get; } | Indicates that shape is a SignatureLine. |
| [IsTopLevel](istoplevel) { get; } | Returns true if this shape is not a child of a group shape. |
| [IsWordArt](iswordart) { get; } | Returns true if this shape is a WordArt object. |
| [Left](left) { get; set; } | Gets or sets the position of the left edge of the containing block of the shape. |
| [MarkupLanguage](markuplanguage) { get; } | Gets MarkupLanguage used for this graphic object. |
| [Name](name) { get; set; } | Gets or sets the optional shape name. |
| [ParentParagraph](parentparagraph) { get; } | Returns the immediate parent paragraph. |
| [RelativeHorizontalPosition](relativehorizontalposition) { get; set; } | Specifies relative to what the shape is positioned horizontally. |
| [RelativeVerticalPosition](relativeverticalposition) { get; set; } | Specifies relative to what the shape is positioned vertically. |
| [Right](right) { get; } | Gets the position of the right edge of the containing block of the shape. |
| [Rotation](rotation) { get; set; } | Defines the angle (in degrees) that a shape is rotated. Positive value corresponds to clockwise rotation angle. |
| [ScreenTip](screentip) { get; set; } | Defines the text displayed when the mouse pointer moves over the shape. |
| [ShapeType](shapetype) { get; } | Gets the shape type. |
| [SizeInPoints](sizeinpoints) { get; } | Gets the size of the shape in points. |
| [Target](target) { get; set; } | Gets or sets the target frame for the shape hyperlink. |
| [Title](title) { get; set; } | Gets or sets the title (caption) of the current shape object. |
| [Top](top) { get; set; } | Gets or sets the position of the top edge of the containing block of the shape. |
| [VerticalAlignment](verticalalignment) { get; set; } | Specifies how the shape is positioned vertically. |
| [Width](width) { get; set; } | Gets or sets the width of the containing block of the shape. |
| [WrapSide](wrapside) { get; set; } | Specifies how the text is wrapped around the shape. |
| [WrapType](wraptype) { get; set; } | Defines whether the shape is inline or floating. For floating shapes defines the wrapping mode for text around the shape. |
| [ZOrder](zorder) { get; set; } | Determines the display order of overlapping shapes. |

## Methods

| Name | Description |
| --- | --- |
| [AdjustWithEffects](adjustwitheffects)(RectangleF) | Adds to the source rectangle values of the effect extent and returns the final rectangle. |
| [FetchInheritedShapeAttr](fetchinheritedshapeattr)(int) | Reserved for system use. IShapeAttrSource. |
| [FetchShapeAttr](fetchshapeattr)(int) | Reserved for system use. IShapeAttrSource. |
| [GetDirectShapeAttr](getdirectshapeattr)(int) | Reserved for system use. IShapeAttrSource. |
| [GetShapeRenderer](getshaperenderer)() | Creates and returns an object that can be used to render this shape into an image. |
| [LocalToParent](localtoparent)(PointF) | Converts a value from the local coordinate space into the coordinate space of the parent shape. |
| [RemoveShapeAttr](removeshapeattr)(int) | Reserved for system use. IShapeAttrSource. |
| [SetShapeAttr](setshapeattr)(int, object) | Reserved for system use. IShapeAttrSource. |

### Remarks

This is an abstract class. The two derived classes that you can instantiate are [`Shape`](../shape) and [`GroupShape`](../groupshape).

A shape is a node in the document tree.

If the shape is a child of a [`Paragraph`](../../aspose.words/paragraph) object, then the shape is said to be "top-level". Top-level shapes are measured and positioned in points.

A shape can also occur as a child of a [`GroupShape`](../groupshape) object when several shapes are grouped. Child shapes of a group shape are positioned in the coordinate space and units defined by the [`CoordSize`](./coordsize) and [`CoordOrigin`](./coordorigin) properties of the parent group shape.

A shape can be positioned inline with text or floating. The positioning method is controlled using the [`WrapType`](./wraptype) property.

When a shape is floating, it is positioned relative to something (e.g the current paragraph, the margin or the page). The relative positioning of the shape is specified using the [`RelativeHorizontalPosition`](./relativehorizontalposition) and [`RelativeVerticalPosition`](./relativeverticalposition) properties.

A floating shape be positioned explicitly using the [`Left`](./left) and [`Top`](./top) properties or aligned relative to some other object using the [`HorizontalAlignment`](./horizontalalignment) and [`VerticalAlignment`](./verticalalignment) properties.

### Examples

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

### See Also

* class [CompositeNode](../../aspose.words/compositenode)
* namespace [Aspose.Words.Drawing](../../aspose.words.drawing)
* assembly [Aspose.Words](../../)

<!-- DO NOT EDIT: generated by xmldocmd for Aspose.Words.dll -->
