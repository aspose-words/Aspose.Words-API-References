---
title: TextPath
second_title: Aspose.Words för .NET API Referens
description: Definierar texten och formateringen av textsökvägen för ett WordArt-objekt.
type: docs
weight: 1200
url: /sv/net/aspose.words.drawing/textpath/
---
## TextPath class

Definierar texten och formateringen av textsökvägen (för ett WordArt-objekt).

```csharp
public class TextPath
```

## Egenskaper

| namn | Beskrivning |
| --- | --- |
| [Bold](../../aspose.words.drawing/textpath/bold) { get; set; } | Sant om teckensnittet är formaterat med fet stil. |
| [FitPath](../../aspose.words.drawing/textpath/fitpath) { get; set; } | Definierar om texten passar vägen för en form. |
| [FitShape](../../aspose.words.drawing/textpath/fitshape) { get; set; } | Definierar om texten passar en forms begränsningsram. |
| [FontFamily](../../aspose.words.drawing/textpath/fontfamily) { get; set; } | Definierar familjen för textpath-teckensnittet. |
| [Italic](../../aspose.words.drawing/textpath/italic) { get; set; } | Sant om teckensnittet är formaterat som kursivt. |
| [Kerning](../../aspose.words.drawing/textpath/kerning) { get; set; } | Bestämmer om kerning är aktiverat. |
| [On](../../aspose.words.drawing/textpath/on) { get; set; } | Definierar om texten ska visas. |
| [ReverseRows](../../aspose.words.drawing/textpath/reverserows) { get; set; } | Bestämmer om layoutordningen för rader är omvänd. |
| [RotateLetters](../../aspose.words.drawing/textpath/rotateletters) { get; set; } | Bestämmer om bokstäverna i texten ska roteras. |
| [SameLetterHeights](../../aspose.words.drawing/textpath/sameletterheights) { get; set; } | Bestämmer om alla bokstäver ska ha samma höjd oavsett skiftläge. |
| [Shadow](../../aspose.words.drawing/textpath/shadow) { get; set; } | Definierar om en skugga appliceras på texten på en textväg. |
| [Size](../../aspose.words.drawing/textpath/size) { get; set; } | Definierar storleken på teckensnittet i punkter. |
| [SmallCaps](../../aspose.words.drawing/textpath/smallcaps) { get; set; } | Sant om teckensnittet är formaterat som små versaler. |
| [Spacing](../../aspose.words.drawing/textpath/spacing) { get; set; } | Definierar mängden mellanrum för text. 1 betyder 100%. |
| [StrikeThrough](../../aspose.words.drawing/textpath/strikethrough) { get; set; } | Sant om teckensnittet är formaterat som genomstruken text. |
| [Text](../../aspose.words.drawing/textpath/text) { get; set; } | Definierar texten i textvägen. |
| [TextPathAlignment](../../aspose.words.drawing/textpath/textpathalignment) { get; set; } | Definierar justeringen av text. |
| [Trim](../../aspose.words.drawing/textpath/trim) { get; set; } | Bestämmer om extra mellanslag ska tas bort ovanför och under texten. |
| [Underline](../../aspose.words.drawing/textpath/underline) { get; set; } | Sant om teckensnittet är understruket. |
| [XScale](../../aspose.words.drawing/textpath/xscale) { get; set; } | Bestämmer om en rak textbana kommer att användas istället för formbanan. |

### Anmärkningar

Använd[`TextPath`](../shape/textpath) egenskap för att komma åt WordArt-egenskaper för en shape. Du skapar inte instanser av[`TextPath`](../textpath) klass direkt.

### Exempel

Visar hur man arbetar med WordArt.

```csharp
{
    Document doc = new Document();

    // Infoga ett WordArt-objekt för att visa text i en form som vi kan ändra storlek på och flytta genom att använda musen i Microsoft Word.
    // Ange en "ShapeType" som ett argument för att ställa in en form för WordArt.
    Shape shape = AppendWordArt(doc, "Hello World! This text is bold, and italic.", 
        "Arial", 480, 24, Color.White, Color.Black, ShapeType.TextPlainText);

    // Använd formateringsinställningarna "Fet" och "Kursiv" på texten med respektive egenskaper.
    shape.TextPath.Bold = true;
    shape.TextPath.Italic = true;

    // Nedan finns olika andra textformateringsrelaterade egenskaper.
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

    // Använd egenskapen "På" för att visa/dölja texten.
    shape = AppendWordArt(doc, "On set to \"true\"", "Calibri", 150, 24, Color.Yellow, Color.Red, ShapeType.TextPlainText);
    shape.TextPath.On = true;

    shape = AppendWordArt(doc, "On set to \"false\"", "Calibri", 150, 24, Color.Yellow, Color.Purple, ShapeType.TextPlainText);
    shape.TextPath.On = false;

    // Använd egenskapen "Kerning" för att aktivera/inaktivera kerning-mellanrum mellan vissa tecken.
    shape = AppendWordArt(doc, "Kerning: VAV", "Times New Roman", 90, 24, Color.Orange, Color.Red, ShapeType.TextPlainText);
    shape.TextPath.Kerning = true;

    shape = AppendWordArt(doc, "No kerning: VAV", "Times New Roman", 100, 24, Color.Orange, Color.Red, ShapeType.TextPlainText);
    shape.TextPath.Kerning = false;

    // Använd egenskapen "Spacing" för att ställa in det anpassade avståndet mellan tecken på en skala från 0,0 (ingen) till 1,0 (standard).
    shape = AppendWordArt(doc, "Spacing set to 0.1", "Calibri", 120, 24, Color.BlueViolet, Color.Blue, ShapeType.TextCascadeDown);
    shape.TextPath.Spacing = 0.1;

    // Ställ in egenskapen "RotateLetters" till "true" för att rotera varje tecken 90 grader moturs.
    shape = AppendWordArt(doc, "RotateLetters", "Calibri", 200, 36, Color.GreenYellow, Color.Green, ShapeType.TextWave);
    shape.TextPath.RotateLetters = true;

    // Ställ in egenskapen "SameLetterHeights" till "true" för att få x-höjden för varje tecken att vara lika med caphöjden.
    shape = AppendWordArt(doc, "Same character height for lower and UPPER case", "Calibri", 300, 24, Color.DeepSkyBlue, Color.DodgerBlue, ShapeType.TextSlantUp);
    shape.TextPath.SameLetterHeights = true;

    // Som standard kommer textens storlek alltid att skalas för att passa den innehållande formens storlek, och åsidosätter inställningen för textstorlek.
    shape = AppendWordArt(doc, "FitShape on", "Calibri", 160, 24, Color.LightBlue, Color.Blue, ShapeType.TextPlainText);
    Assert.True(shape.TextPath.FitShape);
    shape.TextPath.Size = 24.0;

    // Om vi ställer in egenskapen "FitShape: till "false", kommer texten att behålla storleken
    // som egenskapen "Size" anger oavsett storleken på formen.
    // Använd egenskapen "TextPathAlignment" också för att justera texten mot en sida av formen.
    shape = AppendWordArt(doc, "FitShape off", "Calibri", 160, 24, Color.LightBlue, Color.Blue, ShapeType.TextPlainText);
    shape.TextPath.FitShape = false;
    shape.TextPath.Size = 24.0;
    shape.TextPath.TextPathAlignment = TextPathAlignment.Right;

    doc.Save(ArtifactsDir + "Shape.InsertTextPaths.docx");

/// <summary>
/// Infoga ett nytt stycke med en WordArt-form inuti.
/// </summary>
private static Shape AppendWordArt(Document doc, string text, string textFontFamily, double shapeWidth, double shapeHeight, Color wordArtFill, Color line, ShapeType wordArtShapeType)
{
    // Skapa en inline-form, som kommer att fungera som en behållare för vår WordArt.
    // Formen kan bara vara en giltig WordArt-form om vi tilldelar en WordArt-designad ShapeType till den.
    // Dessa typer kommer att ha "WordArt-objekt" i beskrivningen,
    // och deras uppräkningskonstantnamn börjar alla med "Text".
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

### Se även

* namnutrymme [Aspose.Words.Drawing](../../aspose.words.drawing)
* hopsättning [Aspose.Words](../../)

<!-- DO NOT EDIT: generated by xmldocmd for Aspose.Words.dll -->
