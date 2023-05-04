---
title: DocumentBase.BackgroundShape
linktitle: BackgroundShape
articleTitle: BackgroundShape
second_title: Aspose.Words for .NET
description: DocumentBase BackgroundShape property. Gets or sets the background shape of the document. Can be null in C#.
type: docs
weight: 10
url: /net/aspose.words/documentbase/backgroundshape/
---
## DocumentBase.BackgroundShape property

Gets or sets the background shape of the document. Can be `null`.

```csharp
public Shape BackgroundShape { get; set; }
```

## Remarks

Microsoft Word allows only a shape that has its [`ShapeType`](../../../aspose.words.drawing/shapebase/shapetype/) property equal to Rectangle to be used as a background shape for a document.

Microsoft Word supports only the fill properties of a background shape. All other properties are ignored.

Setting this property to a non-null value will also set the [`DisplayBackgroundShape`](../../../aspose.words.settings/viewoptions/displaybackgroundshape/) to `true`.

## Examples

Shows how to set a background shape for every page of a document.

```csharp
Document doc = new Document();

Assert.IsNull(doc.BackgroundShape);

// The only shape type that we can use as a background is a rectangle.
Shape shapeRectangle = new Shape(doc, ShapeType.Rectangle);

// There are two ways of using this shape as a page background.
// 1 -  A flat color:
shapeRectangle.FillColor = System.Drawing.Color.LightBlue;
doc.BackgroundShape = shapeRectangle;

doc.Save(ArtifactsDir + "DocumentBase.BackgroundShape.FlatColor.docx");

// 2 -  An image:
shapeRectangle = new Shape(doc, ShapeType.Rectangle);
shapeRectangle.ImageData.SetImage(ImageDir + "Transparent background logo.png");

// Adjust the image's appearance to make it more suitable as a watermark.
shapeRectangle.ImageData.Contrast = 0.2;
shapeRectangle.ImageData.Brightness = 0.7;

doc.BackgroundShape = shapeRectangle;

Assert.IsTrue(doc.BackgroundShape.HasImage);

Aspose.Words.Saving.PdfSaveOptions saveOptions = new Aspose.Words.Saving.PdfSaveOptions
{
    CacheBackgroundGraphics = false
};

// Microsoft Word does not support shapes with images as backgrounds,
// but we can still see these backgrounds in other save formats such as .pdf.
doc.Save(ArtifactsDir + "DocumentBase.BackgroundShape.Image.pdf", saveOptions);
```

### See Also

* class [Shape](../../../aspose.words.drawing/shape/)
* class [DocumentBase](../)
* namespace [Aspose.Words](../../documentbase/)
* assembly [Aspose.Words](../../../)
