---
title: TextPath.RotateLetters
linktitle: RotateLetters
articleTitle: RotateLetters
second_title: Aspose.Words for .NET
description: Discover the TextPath RotateLetters property to enhance your designs by controlling text rotation for a dynamic visual effect. Elevate your creativity!
type: docs
weight: 90
url: /net/aspose.words.drawing/textpath/rotateletters/
---
## TextPath.RotateLetters property

Determines whether the letters of the text are rotated.

```csharp
public bool RotateLetters { get; set; }
```

## Remarks

The default value is `false`.

## Examples

Shows how to work with WordArt.

```csharp
public void InsertTextPaths()
{
    Document doc = new Document();

    // Insert a WordArt object to display text in a shape that we can re-size and move by using the mouse in Microsoft Word.
    // Provide a "ShapeType" as an argument to set a shape for the WordArt.
    Shape shape = AppendWordArt(doc, "Hello World! This text is bold, and italic.",
        "Arial", 480, 24, Color.White, Color.Black, ShapeType.TextPlainText);

    // Apply the "Bold" and "Italic" formatting settings to the text using the respective properties.
    shape.TextPath.Bold = true;
    shape.TextPath.Italic = true;

    // Below are various other text formatting-related properties.
    Assert.That(shape.TextPath.Underline, Is.False);
    Assert.That(shape.TextPath.Shadow, Is.False);
    Assert.That(shape.TextPath.StrikeThrough, Is.False);
    Assert.That(shape.TextPath.ReverseRows, Is.False);
    Assert.That(shape.TextPath.XScale, Is.False);
    Assert.That(shape.TextPath.Trim, Is.False);
    Assert.That(shape.TextPath.SmallCaps, Is.False);

    Assert.That(shape.TextPath.Size, Is.EqualTo(36.0));
    Assert.That(shape.TextPath.Text, Is.EqualTo("Hello World! This text is bold, and italic."));
    Assert.That(shape.ShapeType, Is.EqualTo(ShapeType.TextPlainText));

    // Use the "On" property to show/hide the text.
    shape = AppendWordArt(doc, "On set to \"true\"", "Calibri", 150, 24, Color.Yellow, Color.Red, ShapeType.TextPlainText);
    shape.TextPath.On = true;

    shape = AppendWordArt(doc, "On set to \"false\"", "Calibri", 150, 24, Color.Yellow, Color.Purple, ShapeType.TextPlainText);
    shape.TextPath.On = false;

    // Use the "Kerning" property to enable/disable kerning spacing between certain characters.
    shape = AppendWordArt(doc, "Kerning: VAV", "Times New Roman", 90, 24, Color.Orange, Color.Red, ShapeType.TextPlainText);
    shape.TextPath.Kerning = true;

    shape = AppendWordArt(doc, "No kerning: VAV", "Times New Roman", 100, 24, Color.Orange, Color.Red, ShapeType.TextPlainText);
    shape.TextPath.Kerning = false;

    // Use the "Spacing" property to set the custom spacing between characters on a scale from 0.0 (none) to 1.0 (default).
    shape = AppendWordArt(doc, "Spacing set to 0.1", "Calibri", 120, 24, Color.BlueViolet, Color.Blue, ShapeType.TextCascadeDown);
    shape.TextPath.Spacing = 0.1;

    // Set the "RotateLetters" property to "true" to rotate each character 90 degrees counterclockwise.
    shape = AppendWordArt(doc, "RotateLetters", "Calibri", 200, 36, Color.GreenYellow, Color.Green, ShapeType.TextWave);
    shape.TextPath.RotateLetters = true;

    // Set the "SameLetterHeights" property to "true" to get the x-height of each character to equal the cap height.
    shape = AppendWordArt(doc, "Same character height for lower and UPPER case", "Calibri", 300, 24, Color.DeepSkyBlue, Color.DodgerBlue, ShapeType.TextSlantUp);
    shape.TextPath.SameLetterHeights = true;

    // By default, the text's size will always scale to fit the containing shape's size, overriding the text size setting.
    shape = AppendWordArt(doc, "FitShape on", "Calibri", 160, 24, Color.LightBlue, Color.Blue, ShapeType.TextPlainText);
    Assert.That(shape.TextPath.FitShape, Is.True);
    shape.TextPath.Size = 24.0;

    // If we set the "FitShape: property to "false", the text will keep the size
    // which the "Size" property specifies regardless of the size of the shape.
    // Use the "TextPathAlignment" property also to align the text to a side of the shape.
    shape = AppendWordArt(doc, "FitShape off", "Calibri", 160, 24, Color.LightBlue, Color.Blue, ShapeType.TextPlainText);
    shape.TextPath.FitShape = false;
    shape.TextPath.Size = 24.0;
    shape.TextPath.TextPathAlignment = TextPathAlignment.Right;

    doc.Save(ArtifactsDir + "Shape.InsertTextPaths.docx");
}

/// <summary>
/// Insert a new paragraph with a WordArt shape inside it.
/// </summary>
private static Shape AppendWordArt(Document doc, string text, string textFontFamily, double shapeWidth, double shapeHeight, Color wordArtFill, Color line, ShapeType wordArtShapeType)
{
    // Create an inline Shape, which will serve as a container for our WordArt.
    // The shape can only be a valid WordArt shape if we assign a WordArt-designated ShapeType to it.
    // These types will have "WordArt object" in the description,
    // and their enumerator constant names will all start with "Text".
    Shape shape = new Shape(doc, wordArtShapeType)
    {
        WrapType = WrapType.Inline,
        Width = shapeWidth,
        Height = shapeHeight,
        FillColor = wordArtFill,
        StrokeColor = line
    };

    shape.TextPath.Text = text;
    shape.TextPath.FontFamily = textFontFamily;

    Paragraph para = (Paragraph)doc.FirstSection.Body.AppendChild(new Paragraph(doc));
    para.AppendChild(shape);
    return shape;
}
```

### See Also

* class [TextPath](../)
* namespace [Aspose.Words.Drawing](../../../aspose.words.drawing/)
* assembly [Aspose.Words](../../../)
