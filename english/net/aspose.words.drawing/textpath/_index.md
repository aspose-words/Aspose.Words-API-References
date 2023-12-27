---
title: TextPath Class
linktitle: TextPath
articleTitle: TextPath
second_title: Aspose.Words for .NET
description: Aspose.Words.Drawing.TextPath class. Defines the text and formatting of the text path of a WordArt object in C#.
type: docs
weight: 1430
url: /net/aspose.words.drawing/textpath/
---
## TextPath class

Defines the text and formatting of the text path (of a WordArt object).

To learn more, visit the [Working with Shapes](https://docs.aspose.com/words/net/working-with-shapes/) documentation article.

```csharp
public class TextPath
```

## Properties

| Name | Description |
| --- | --- |
| [Bold](../../aspose.words.drawing/textpath/bold/) { get; set; } | True if the font is formatted as bold. |
| [FitPath](../../aspose.words.drawing/textpath/fitpath/) { get; set; } | Defines whether the text fits the path of a shape. |
| [FitShape](../../aspose.words.drawing/textpath/fitshape/) { get; set; } | Defines whether the text fits bounding box of a shape. |
| [FontFamily](../../aspose.words.drawing/textpath/fontfamily/) { get; set; } | Defines the family of the textpath font. |
| [Italic](../../aspose.words.drawing/textpath/italic/) { get; set; } | True if the font is formatted as italic. |
| [Kerning](../../aspose.words.drawing/textpath/kerning/) { get; set; } | Determines whether kerning is turned on. |
| [On](../../aspose.words.drawing/textpath/on/) { get; set; } | Defines whether the text is displayed. |
| [ReverseRows](../../aspose.words.drawing/textpath/reverserows/) { get; set; } | Determines whether the layout order of rows is reversed. |
| [RotateLetters](../../aspose.words.drawing/textpath/rotateletters/) { get; set; } | Determines whether the letters of the text are rotated. |
| [SameLetterHeights](../../aspose.words.drawing/textpath/sameletterheights/) { get; set; } | Determines whether all letters will be the same height regardless of initial case. |
| [Shadow](../../aspose.words.drawing/textpath/shadow/) { get; set; } | Defines whether a shadow is applied to the text on a text path. |
| [Size](../../aspose.words.drawing/textpath/size/) { get; set; } | Defines the size of the font in points. |
| [SmallCaps](../../aspose.words.drawing/textpath/smallcaps/) { get; set; } | True if the font is formatted as small capital letters. |
| [Spacing](../../aspose.words.drawing/textpath/spacing/) { get; set; } | Defines the amount of spacing for text. 1 means 100%. |
| [StrikeThrough](../../aspose.words.drawing/textpath/strikethrough/) { get; set; } | True if the font is formatted as strikethrough text. |
| [Text](../../aspose.words.drawing/textpath/text/) { get; set; } | Defines the text of the text path. |
| [TextPathAlignment](../../aspose.words.drawing/textpath/textpathalignment/) { get; set; } | Defines the alignment of text. |
| [Trim](../../aspose.words.drawing/textpath/trim/) { get; set; } | Determines whether extra space is removed above and below the text. |
| [Underline](../../aspose.words.drawing/textpath/underline/) { get; set; } | True if the font is underlined. |
| [XScale](../../aspose.words.drawing/textpath/xscale/) { get; set; } | Determines whether a straight textpath will be used instead of the shape path. |

## Remarks

Use the [`TextPath`](../shape/textpath/) property to access WordArt properties of a shape. You do not create instances of the `TextPath` class directly.

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
    Assert.False(shape.TextPath.Underline);
    Assert.False(shape.TextPath.Shadow);
    Assert.False(shape.TextPath.StrikeThrough);
    Assert.False(shape.TextPath.ReverseRows);
    Assert.False(shape.TextPath.XScale);
    Assert.False(shape.TextPath.Trim);
    Assert.False(shape.TextPath.SmallCaps);

    Assert.AreEqual(36.0, shape.TextPath.Size);
    Assert.AreEqual("Hello World! This text is bold, and italic.", shape.TextPath.Text);
    Assert.AreEqual(ShapeType.TextPlainText, shape.ShapeType);

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
    Assert.True(shape.TextPath.FitShape);
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

* namespace [Aspose.Words.Drawing](../../aspose.words.drawing/)
* assembly [Aspose.Words](../../)
