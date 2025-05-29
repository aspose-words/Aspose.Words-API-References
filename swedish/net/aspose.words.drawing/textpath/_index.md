---
title: TextPath Class
linktitle: TextPath
articleTitle: TextPath
second_title: Aspose.Words för .NET
description: Upptäck klassen Aspose.Words.Drawing.TextPath för att skapa snygga WordArt-bilder. Definiera enkelt text och formatering för att förbättra dina dokument.
type: docs
weight: 1760
url: /sv/net/aspose.words.drawing/textpath/
---
## TextPath class

Definierar texten och formateringen för textbanan (för ett WordArt-objekt).

För att lära dig mer, besök[Arbeta med former](https://docs.aspose.com/words/net/working-with-shapes/) dokumentationsartikel.

```csharp
public class TextPath
```

## Egenskaper

| namn | Beskrivning |
| --- | --- |
| [Bold](../../aspose.words.drawing/textpath/bold/) { get; set; } | Sant om teckensnittet är formaterat som fetstil. |
| [FitPath](../../aspose.words.drawing/textpath/fitpath/) { get; set; } | Definierar om texten passar in i en forms bana. |
| [FitShape](../../aspose.words.drawing/textpath/fitshape/) { get; set; } | Definierar om texten passar in i en forms avgränsningsram. |
| [FontFamily](../../aspose.words.drawing/textpath/fontfamily/) { get; set; } | Definierar familjen för textpath-teckensnittet. |
| [Italic](../../aspose.words.drawing/textpath/italic/) { get; set; } | Sant om teckensnittet är formaterat som kursiv stil. |
| [Kerning](../../aspose.words.drawing/textpath/kerning/) { get; set; } | Avgör om kerning är aktiverat. |
| [On](../../aspose.words.drawing/textpath/on/) { get; set; } | Definierar om texten visas. |
| [ReverseRows](../../aspose.words.drawing/textpath/reverserows/) { get; set; } | Avgör om layoutordningen för raderna är omvänd. |
| [RotateLetters](../../aspose.words.drawing/textpath/rotateletters/) { get; set; } | Avgör om bokstäverna i texten roteras. |
| [SameLetterHeights](../../aspose.words.drawing/textpath/sameletterheights/) { get; set; } | Avgör om alla bokstäver ska ha samma höjd oavsett skiftläge/gemensamma skiftlägen. |
| [Shadow](../../aspose.words.drawing/textpath/shadow/) { get; set; } | Definierar om en skugga appliceras på texten på en textbana. |
| [Size](../../aspose.words.drawing/textpath/size/) { get; set; } | Definierar teckenstorleken i punkter. |
| [SmallCaps](../../aspose.words.drawing/textpath/smallcaps/) { get; set; } | Sant om teckensnittet är formaterat som små versaler. |
| [Spacing](../../aspose.words.drawing/textpath/spacing/) { get; set; } | Definierar avståndet för text. 1 betyder 100%. |
| [StrikeThrough](../../aspose.words.drawing/textpath/strikethrough/) { get; set; } | Sant om teckensnittet är formaterat som genomstruken text. |
| [Text](../../aspose.words.drawing/textpath/text/) { get; set; } | Definierar texten för textbanan. |
| [TextPathAlignment](../../aspose.words.drawing/textpath/textpathalignment/) { get; set; } | Definierar textjusteringen. |
| [Trim](../../aspose.words.drawing/textpath/trim/) { get; set; } | Avgör om extra utrymme tas bort ovanför och under texten. |
| [Underline](../../aspose.words.drawing/textpath/underline/) { get; set; } | Sant om teckensnittet är understruket. |
| [XScale](../../aspose.words.drawing/textpath/xscale/) { get; set; } | Avgör om en rak textbana ska användas istället för formbanan. |

## Anmärkningar

Använd[`TextPath`](../shape/textpath/) egenskap för att komma åt WordArt-egenskaper för en form. Du skapar inte instanser av`TextPath` klass direkt.

## Exempel

Visar hur man arbetar med WordArt.

```csharp
public void InsertTextPaths()
{
    Document doc = new Document();

    // Infoga ett WordArt-objekt för att visa text i en form som vi kan ändra storlek på och flytta med hjälp av musen i Microsoft Word.
    // Ange en "ShapeType" som ett argument för att ange en form för WordArt-objektet.
    Shape shape = AppendWordArt(doc, "Hello World! This text is bold, and italic.",
        "Arial", 480, 24, Color.White, Color.Black, ShapeType.TextPlainText);

    // Använd formateringsinställningarna "Fet" och "Kursiv" på texten med hjälp av respektive egenskaper.
    shape.TextPath.Bold = true;
    shape.TextPath.Italic = true;

    // Nedan finns diverse andra textformateringsrelaterade egenskaper.
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

    // Använd egenskapen "Kerning" för att aktivera/avaktivera kerningavstånd mellan vissa tecken.
    shape = AppendWordArt(doc, "Kerning: VAV", "Times New Roman", 90, 24, Color.Orange, Color.Red, ShapeType.TextPlainText);
    shape.TextPath.Kerning = true;

    shape = AppendWordArt(doc, "No kerning: VAV", "Times New Roman", 100, 24, Color.Orange, Color.Red, ShapeType.TextPlainText);
    shape.TextPath.Kerning = false;

    // Använd egenskapen "Spacing" för att ställa in det anpassade avståndet mellan tecken på en skala från 0,0 (inget) till 1,0 (standard).
    shape = AppendWordArt(doc, "Spacing set to 0.1", "Calibri", 120, 24, Color.BlueViolet, Color.Blue, ShapeType.TextCascadeDown);
    shape.TextPath.Spacing = 0.1;

    // Sätt egenskapen "RotateLetters" till "true" för att rotera varje tecken 90 grader moturs.
    shape = AppendWordArt(doc, "RotateLetters", "Calibri", 200, 36, Color.GreenYellow, Color.Green, ShapeType.TextWave);
    shape.TextPath.RotateLetters = true;

    // Sätt egenskapen "SameLetterHeights" till "true" för att få x-höjden för varje tecken att vara lika med versalhöjden.
    shape = AppendWordArt(doc, "Same character height for lower and UPPER case", "Calibri", 300, 24, Color.DeepSkyBlue, Color.DodgerBlue, ShapeType.TextSlantUp);
    shape.TextPath.SameLetterHeights = true;

    // Som standard kommer textens storlek alltid att skalas för att passa den ingående formens storlek, vilket åsidosätter inställningen för textstorlek.
    shape = AppendWordArt(doc, "FitShape on", "Calibri", 160, 24, Color.LightBlue, Color.Blue, ShapeType.TextPlainText);
    Assert.True(shape.TextPath.FitShape);
    shape.TextPath.Size = 24.0;

    // Om vi ställer in egenskapen "FitShape:" till "false" kommer texten att behålla storleken
    // som egenskapen "Storlek" anger oavsett formens storlek.
    // Använd även egenskapen "TextPathAlignment" för att justera texten mot en sida av formen.
    shape = AppendWordArt(doc, "FitShape off", "Calibri", 160, 24, Color.LightBlue, Color.Blue, ShapeType.TextPlainText);
    shape.TextPath.FitShape = false;
    shape.TextPath.Size = 24.0;
    shape.TextPath.TextPathAlignment = TextPathAlignment.Right;

    doc.Save(ArtifactsDir + "Shape.InsertTextPaths.docx");
}

/// <summary>
/// Infoga ett nytt stycke med en WordArt-form inuti.
/// </summary>
private static Shape AppendWordArt(Document doc, string text, string textFontFamily, double shapeWidth, double shapeHeight, Color wordArtFill, Color line, ShapeType wordArtShapeType)
{
    // Skapa en inline-form som kommer att fungera som en behållare för vårt WordArt-objekt.
    // Formen kan bara vara en giltig WordArt-form om vi tilldelar den en WordArt-designerad formtyp.
    // Dessa typer kommer att ha "WordArt-objekt" i beskrivningen,
    // och deras namn på uppräknarkonstanter börjar alla med "Text".
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

* namnutrymme [Aspose.Words.Drawing](../../aspose.words.drawing/)
* hopsättning [Aspose.Words](../../)
