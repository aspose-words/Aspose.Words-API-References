---
title: Document.RenderToSize
linktitle: RenderToSize
second_title: Aspose.Words for .NET API Reference
description: Document method. Renders a document page into a Graphics object to a specified size in C#.
type: docs
weight: 690
url: /net/aspose.words/document/rendertosize/
---
## Document.RenderToSize method

Renders a document page into a Graphics object to a specified size.

```csharp
public float RenderToSize(int pageIndex, Graphics graphics, float x, float y, float width, 
    float height)
```

| Parameter | Type | Description |
| --- | --- | --- |
| pageIndex | Int32 | The 0-based page index. |
| graphics | Graphics | The object where to render to. |
| x | Single | The X coordinate (in world units) of the top left corner of the rendered page. |
| y | Single | The Y coordinate (in world units) of the top left corner of the rendered page. |
| width | Single | The maximum width (in world units) that can be occupied by the rendered page. |
| height | Single | The maximum height (in world units) that can be occupied by the rendered page. |

### Return Value

The scale that was automatically calculated for the rendered page to fit the specified size.

## Examples

Shows how to render the document as a bitmap at a specified location and size (.NetStandard 2.0).

```csharp
Document doc = new Document(MyDir + "Rendering.docx");

using (SKBitmap bitmap = new SKBitmap(700, 700))
{
    using (SKCanvas canvas = new SKCanvas(bitmap))
    {
        // Apply a scaling factor of 70% to the page that we will render using this canvas.
        canvas.Scale(70);

        // Offset the page 0.5" from the top and left edges of the page.
        canvas.Translate(0.5f, 0.5f);

        // Rotate the rendered page by 10 degrees.
        canvas.RotateDegrees(10);

        // Create and draw a rectangle.
        SKRect rect = new SKRect(0f, 0f, 3f, 3f);
        canvas.DrawRect(rect, new SKPaint
        {
            Color = SKColors.Black,
            Style = SKPaintStyle.Stroke,
            StrokeWidth = 3f / 72f
        });

        // Render the first page of the document to the same size as the above rectangle.
        // The rectangle will frame this page.
        float returnedScale = doc.RenderToSize(0, canvas, 0f, 0f, 3f, 3f);

        Console.WriteLine("The image was rendered at {0:P0} zoom.", returnedScale);

        // Reset the matrix, and then apply a new set of scaling and translations.
        canvas.ResetMatrix();
        canvas.Scale(5);
        canvas.Translate(10, 10);

        // Create another rectangle.
        rect = new SKRect(0, 0, 50, 100);
        rect.Offset(90, 10);
        canvas.DrawRect(rect, new SKPaint
        {
            Color = SKColors.Black,
            Style = SKPaintStyle.Stroke,
            StrokeWidth = 1
        });

        // Render the first page within the newly created rectangle once again.
        doc.RenderToSize(0, canvas, 90, 10, 50, 100);

        using (SKFileWStream fs = new SKFileWStream(ArtifactsDir + "Rendering.RenderToSizeNetStandard2.png"))
        {
            bitmap.PeekPixels().Encode(fs, SKEncodedImageFormat.Png, 100);
        }
    }
}
```

Shows how to render a document to a bitmap at a specified location and size.

```csharp
Document doc = new Document(MyDir + "Rendering.docx");

using (Bitmap bmp = new Bitmap(700, 700))
{
    using (Graphics gr = Graphics.FromImage(bmp))
    {
        gr.TextRenderingHint = TextRenderingHint.AntiAliasGridFit;

        // Set the "PageUnit" property to "GraphicsUnit.Inch" to use inches as the
        // measurement unit for any transformations and dimensions that we will define.
        gr.PageUnit = GraphicsUnit.Inch;

        // Offset the output 0.5" from the edge.
        gr.TranslateTransform(0.5f, 0.5f);

        // Rotate the output by 10 degrees.
        gr.RotateTransform(10);

        // Draw a 3"x3" rectangle.
        gr.DrawRectangle(new Pen(Color.Black, 3f / 72f), 0f, 0f, 3f, 3f);

        // Draw the first page of our document with the same dimensions and transformation as the rectangle.
        // The rectangle will frame the first page.
        float returnedScale = doc.RenderToSize(0, gr, 0f, 0f, 3f, 3f);

        // This is the scaling factor that the RenderToSize method applied to the first page to fit the specified size.
        Assert.AreEqual(0.2566f, returnedScale, 0.0001f);

        // Set the "PageUnit" property to "GraphicsUnit.Millimeter" to use millimeters as the
        // measurement unit for any transformations and dimensions that we will define.
        gr.PageUnit = GraphicsUnit.Millimeter;

        // Reset the transformations that we used from the previous rendering.
        gr.ResetTransform();

        // Apply another set of transformations. 
        gr.TranslateTransform(10, 10);
        gr.ScaleTransform(0.5f, 0.5f);
        gr.PageScale = 2f;

        // Create another rectangle and use it to frame another page from the document.
        gr.DrawRectangle(new Pen(Color.Black, 1), 90, 10, 50, 100);
        doc.RenderToSize(1, gr, 90, 10, 50, 100);

        bmp.Save(ArtifactsDir + "Rendering.RenderToSize.png");
    }
}
```

### See Also

* class [Document](../)
* namespace [Aspose.Words](../../document/)
* assembly [Aspose.Words](../../../)
