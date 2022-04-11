---
title: Shape
second_title: Aspose.Words for .NET API Reference
description: 
type: docs
weight: 1070
url: /net/aspose.words.drawing/shape/
---
## Shape class

Represents an object in the drawing layer, such as an AutoShape, textbox, freeform, OLE object, ActiveX control, or picture.

```csharp
public sealed class Shape : ShapeBase
```

## Public Members

| Name | Description |
| --- | --- |
| [Shape](shape)(…) | Creates a new shape object. |
| [Chart](chart) { get; } | Provides access to the chart properties if this shape has a Chart. |
| [ExtrusionEnabled](extrusionenabled) { get; } | Returns true if an extrusion effect is enabled. |
| [FillColor](fillcolor) { get; set; } | Defines the brush color that fills the closed path of the shape. |
| [Filled](filled) { get; set; } | Determines whether the closed path of the shape will be filled. |
| [FirstParagraph](firstparagraph) { get; } | Gets the first paragraph in the shape. |
| [HasChart](haschart) { get; } | Returns true if this Shape has a [`Chart`](./chart). |
| [HasImage](hasimage) { get; } | Returns true if the shape has image bytes or links an image. |
| [HasSmartArt](hassmartart) { get; } | Returns true if this Shape has a SmartArt object. |
| [HorizontalRuleFormat](horizontalruleformat) { get; } | Provides access to the properties of the horizontal rule shape. For a shape that is not a horizontal rule, returns null. |
| [ImageData](imagedata) { get; } | Provides access to the image of the shape. Returns null if the shape cannot have an image. |
| [LastParagraph](lastparagraph) { get; } | Gets the last paragraph in the shape. |
| override [NodeType](nodetype) { get; } | Returns Shape. |
| [OleFormat](oleformat) { get; } | Provides access to the OLE data of a shape. For a shape that is not an OLE object or ActiveX control, returns null. |
| [ShadowEnabled](shadowenabled) { get; } | Returns true if a shadow effect is enabled. |
| [SignatureLine](signatureline) { get; } | Gets [`SignatureLine`](./signatureline) object if the shape is a signature line. Returns null otherwise. |
| [StoryType](storytype) { get; } | Returns Textbox. |
| [Stroke](stroke) { get; } | Defines a stroke for a shape. |
| [StrokeColor](strokecolor) { get; set; } | Defines the color of a stroke. |
| [Stroked](stroked) { get; set; } | Defines whether the path will be stroked. |
| [StrokeWeight](strokeweight) { get; set; } | Defines the brush thickness that strokes the path of a shape in points. |
| [TextBox](textbox) { get; } | Defines attributes that specify how text is displayed in a shape. |
| [TextPath](textpath) { get; } | Defines the text of the text path (of a WordArt object). |
| override [Accept](accept)(…) | Accepts a visitor. |
| [UpdateSmartArtDrawing](updatesmartartdrawing)() | Updates SmartArt pre-rendered drawing by using Aspose.Words's SmartArt cold rendering engine. |

### Remarks

Using the [`Shape`](../shape) class you can create or modify shapes in a Microsoft Word document.An important property of a shape is its [`ShapeType`](../shapebase/shapetype). Shapes of different types can have different capabilities in a Word document. For example, only image and OLE shapes can have images inside them. Most of the shapes can have text, but not all.Shapes that can have text, can contain [`Paragraph`](../../aspose.words/paragraph) and [`Table`](../../aspose.words.tables/table) nodes as children.

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

* class [ShapeBase](../shapebase)
* namespace [Aspose.Words.Drawing](../../aspose.words.drawing)
* assembly [Aspose.Words](../../)

<!-- DO NOT EDIT: generated by xmldocmd for Aspose.Words.dll -->
