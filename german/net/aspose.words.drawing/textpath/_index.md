---
title: TextPath
second_title: Aspose.Words für .NET-API-Referenz
description: Definiert den Text und die Formatierung des Textpfads eines WordArtObjekts.
type: docs
weight: 1200
url: /de/net/aspose.words.drawing/textpath/
---
## TextPath class

Definiert den Text und die Formatierung des Textpfads (eines WordArt-Objekts).

```csharp
public class TextPath
```

## Eigenschaften

| Name | Beschreibung |
| --- | --- |
| [Bold](../../aspose.words.drawing/textpath/bold/) { get; set; } | Wahr, wenn die Schriftart fett formatiert ist. |
| [FitPath](../../aspose.words.drawing/textpath/fitpath/) { get; set; } | Definiert, ob der Text zum Pfad einer Form passt. |
| [FitShape](../../aspose.words.drawing/textpath/fitshape/) { get; set; } | Definiert, ob der Text in den Begrenzungsrahmen einer Form passt. |
| [FontFamily](../../aspose.words.drawing/textpath/fontfamily/) { get; set; } | Definiert die Familie der Textpfad-Schriftart. |
| [Italic](../../aspose.words.drawing/textpath/italic/) { get; set; } | Wahr, wenn die Schriftart kursiv formatiert ist. |
| [Kerning](../../aspose.words.drawing/textpath/kerning/) { get; set; } | Legt fest, ob Kerning aktiviert ist. |
| [On](../../aspose.words.drawing/textpath/on/) { get; set; } | Legt fest, ob der Text angezeigt wird. |
| [ReverseRows](../../aspose.words.drawing/textpath/reverserows/) { get; set; } | Bestimmt, ob die Layoutreihenfolge der Zeilen umgekehrt wird. |
| [RotateLetters](../../aspose.words.drawing/textpath/rotateletters/) { get; set; } | Legt fest, ob die Buchstaben des Textes gedreht werden. |
| [SameLetterHeights](../../aspose.words.drawing/textpath/sameletterheights/) { get; set; } | Legt fest, ob alle Buchstaben unabhängig vom Anfangsbuchstaben gleich hoch sind. |
| [Shadow](../../aspose.words.drawing/textpath/shadow/) { get; set; } | Definiert, ob ein Schatten auf den Text eines Textpfades angewendet wird. |
| [Size](../../aspose.words.drawing/textpath/size/) { get; set; } | Definiert die Schriftgröße in Punkt. |
| [SmallCaps](../../aspose.words.drawing/textpath/smallcaps/) { get; set; } | Wahr, wenn die Schriftart als kleine Großbuchstaben formatiert ist. |
| [Spacing](../../aspose.words.drawing/textpath/spacing/) { get; set; } | Definiert den Abstand für Text. 1 bedeutet 100 %. |
| [StrikeThrough](../../aspose.words.drawing/textpath/strikethrough/) { get; set; } | True, wenn die Schriftart als durchgestrichener Text formatiert ist. |
| [Text](../../aspose.words.drawing/textpath/text/) { get; set; } | Definiert den Text des Textpfades. |
| [TextPathAlignment](../../aspose.words.drawing/textpath/textpathalignment/) { get; set; } | Definiert die Ausrichtung von Text. |
| [Trim](../../aspose.words.drawing/textpath/trim/) { get; set; } | Legt fest, ob zusätzlicher Leerraum über und unter dem Text entfernt wird. |
| [Underline](../../aspose.words.drawing/textpath/underline/) { get; set; } | Wahr, wenn die Schriftart unterstrichen ist. |
| [XScale](../../aspose.words.drawing/textpath/xscale/) { get; set; } | Legt fest, ob anstelle des Formpfads ein gerader Textpfad verwendet wird. |

### Bemerkungen

Verwenden Sie die[`TextPath`](../shape/textpath/) -Eigenschaft, um auf die WordArt-Eigenschaften einer Form zuzugreifen. Sie erstellen keine Instanzen der`TextPath` Klasse direkt.

### Beispiele

Zeigt, wie Sie mit WordArt arbeiten.

```csharp
{
    Document doc = new Document();

    // Fügen Sie ein WordArt-Objekt ein, um Text in einer Form anzuzeigen, die wir mit der Maus in Microsoft Word in der Größe ändern und verschieben können.
    // Geben Sie einen "ShapeType" als Argument an, um eine Form für die WordArt festzulegen.
    Shape shape = AppendWordArt(doc, "Hello World! This text is bold, and italic.", 
        "Arial", 480, 24, Color.White, Color.Black, ShapeType.TextPlainText);

    // Wenden Sie die Formatierungseinstellungen "Fett" und "Kursiv" mithilfe der entsprechenden Eigenschaften auf den Text an.
    shape.TextPath.Bold = true;
    shape.TextPath.Italic = true;

    // Unten sind verschiedene andere Eigenschaften im Zusammenhang mit der Textformatierung aufgeführt.
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

    // Verwenden Sie die Eigenschaft "On", um den Text anzuzeigen/auszublenden.
    shape = AppendWordArt(doc, "On set to \"true\"", "Calibri", 150, 24, Color.Yellow, Color.Red, ShapeType.TextPlainText);
    shape.TextPath.On = true;

    shape = AppendWordArt(doc, "On set to \"false\"", "Calibri", 150, 24, Color.Yellow, Color.Purple, ShapeType.TextPlainText);
    shape.TextPath.On = false;

    // Verwenden Sie die Eigenschaft "Kerning", um den Kerning-Abstand zwischen bestimmten Zeichen zu aktivieren/deaktivieren.
    shape = AppendWordArt(doc, "Kerning: VAV", "Times New Roman", 90, 24, Color.Orange, Color.Red, ShapeType.TextPlainText);
    shape.TextPath.Kerning = true;

    shape = AppendWordArt(doc, "No kerning: VAV", "Times New Roman", 100, 24, Color.Orange, Color.Red, ShapeType.TextPlainText);
    shape.TextPath.Kerning = false;

    // Verwenden Sie die Eigenschaft "Spacing", um den benutzerdefinierten Abstand zwischen Zeichen auf einer Skala von 0,0 (keine) bis 1,0 (Standard) festzulegen.
    shape = AppendWordArt(doc, "Spacing set to 0.1", "Calibri", 120, 24, Color.BlueViolet, Color.Blue, ShapeType.TextCascadeDown);
    shape.TextPath.Spacing = 0.1;

    // Setzen Sie die Eigenschaft "RotateLetters" auf "true", um jedes Zeichen um 90 Grad gegen den Uhrzeigersinn zu drehen.
    shape = AppendWordArt(doc, "RotateLetters", "Calibri", 200, 36, Color.GreenYellow, Color.Green, ShapeType.TextWave);
    shape.TextPath.RotateLetters = true;

    // Setzen Sie die Eigenschaft "SameLetterHeights" auf "true", um die x-Höhe jedes Zeichens gleich der Kappenhöhe zu erhalten.
    shape = AppendWordArt(doc, "Same character height for lower and UPPER case", "Calibri", 300, 24, Color.DeepSkyBlue, Color.DodgerBlue, ShapeType.TextSlantUp);
    shape.TextPath.SameLetterHeights = true;

    // Standardmäßig wird die Textgröße immer an die Größe der umgebenden Form angepasst, wobei die Textgrößeneinstellung überschrieben wird.
    shape = AppendWordArt(doc, "FitShape on", "Calibri", 160, 24, Color.LightBlue, Color.Blue, ShapeType.TextPlainText);
    Assert.True(shape.TextPath.FitShape);
    shape.TextPath.Size = 24.0;

    // Wenn wir die Eigenschaft "FitShape:" auf "false" setzen, behält der Text die Größe
    // die die Eigenschaft "Größe" unabhängig von der Größe der Form angibt.
    // Verwenden Sie die Eigenschaft "TextPathAlignment", um den Text auch an einer Seite der Form auszurichten.
    shape = AppendWordArt(doc, "FitShape off", "Calibri", 160, 24, Color.LightBlue, Color.Blue, ShapeType.TextPlainText);
    shape.TextPath.FitShape = false;
    shape.TextPath.Size = 24.0;
    shape.TextPath.TextPathAlignment = TextPathAlignment.Right;

    doc.Save(ArtifactsDir + "Shape.InsertTextPaths.docx");

/// <summary>
/// Einen neuen Absatz mit einer WordArt-Form darin einfügen.
/// </summary>
private static Shape AppendWordArt(Document doc, string text, string textFontFamily, double shapeWidth, double shapeHeight, Color wordArtFill, Color line, ShapeType wordArtShapeType)
{
    // Erstellen Sie eine Inline-Form, die als Container für unsere WordArt dient.
    // Die Form kann nur dann eine gültige WordArt-Form sein, wenn wir ihr einen von WordArt bezeichneten ShapeType zuweisen.
    // Diese Typen haben "WordArt-Objekt" in der Beschreibung,
    // und die Namen ihrer Enumerator-Konstanten beginnen alle mit "Text".
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

### Siehe auch

* namensraum [Aspose.Words.Drawing](../../aspose.words.drawing/)
* Montage [Aspose.Words](../../)

<!-- DO NOT EDIT: generated by xmldocmd for Aspose.Words.dll -->
