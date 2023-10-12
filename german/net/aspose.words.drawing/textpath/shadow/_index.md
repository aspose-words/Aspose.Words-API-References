---
title: TextPath.Shadow
second_title: Aspose.Words für .NET-API-Referenz
description: TextPath eigendom. Definiert ob ein Schatten auf den Text auf einem Textpfad angewendet wird.
type: docs
weight: 110
url: /de/net/aspose.words.drawing/textpath/shadow/
---
## TextPath.Shadow property

Definiert, ob ein Schatten auf den Text auf einem Textpfad angewendet wird.

```csharp
public bool Shadow { get; set; }
```

### Bemerkungen

Der Standardwert ist`FALSCH`.

### Beispiele

Zeigt, wie man mit WordArt arbeitet.

```csharp
public void InsertTextPaths()
{
    Document doc = new Document();

    // Ein WordArt-Objekt einfügen, um Text in einer Form anzuzeigen, deren Größe wir ändern und mit der Maus in Microsoft Word verschieben können.
    // Geben Sie einen „ShapeType“ als Argument an, um eine Form für das WordArt festzulegen.
    Shape shape = AppendWordArt(doc, "Hello World! This text is bold, and italic.", 
        "Arial", 480, 24, Color.White, Color.Black, ShapeType.TextPlainText);

    // Wenden Sie die Formatierungseinstellungen „Fett“ und „Kursiv“ mithilfe der entsprechenden Eigenschaften auf den Text an.
    shape.TextPath.Bold = true;
    shape.TextPath.Italic = true;

    // Nachfolgend finden Sie verschiedene andere Eigenschaften im Zusammenhang mit der Textformatierung.
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

    // Verwenden Sie die Eigenschaft „On“, um den Text anzuzeigen/auszublenden.
    shape = AppendWordArt(doc, "On set to \"true\"", "Calibri", 150, 24, Color.Yellow, Color.Red, ShapeType.TextPlainText);
    shape.TextPath.On = true;

    shape = AppendWordArt(doc, "On set to \"false\"", "Calibri", 150, 24, Color.Yellow, Color.Purple, ShapeType.TextPlainText);
    shape.TextPath.On = false;

    // Verwenden Sie die Eigenschaft „Kerning“, um den Kerning-Abstand zwischen bestimmten Zeichen zu aktivieren/deaktivieren.
    shape = AppendWordArt(doc, "Kerning: VAV", "Times New Roman", 90, 24, Color.Orange, Color.Red, ShapeType.TextPlainText);
    shape.TextPath.Kerning = true;

    shape = AppendWordArt(doc, "No kerning: VAV", "Times New Roman", 100, 24, Color.Orange, Color.Red, ShapeType.TextPlainText);
    shape.TextPath.Kerning = false;

    // Verwenden Sie die Eigenschaft „Spacing“, um den benutzerdefinierten Abstand zwischen Zeichen auf einer Skala von 0,0 (keine) bis 1,0 (Standard) festzulegen.
    shape = AppendWordArt(doc, "Spacing set to 0.1", "Calibri", 120, 24, Color.BlueViolet, Color.Blue, ShapeType.TextCascadeDown);
    shape.TextPath.Spacing = 0.1;

    // Setzen Sie die Eigenschaft „RotateLetters“ auf „true“, um jedes Zeichen um 90 Grad gegen den Uhrzeigersinn zu drehen.
    shape = AppendWordArt(doc, "RotateLetters", "Calibri", 200, 36, Color.GreenYellow, Color.Green, ShapeType.TextWave);
    shape.TextPath.RotateLetters = true;

    // Setzen Sie die Eigenschaft „SameLetterHeights“ auf „true“, damit die x-Höhe jedes Zeichens der Versalhöhe entspricht.
    shape = AppendWordArt(doc, "Same character height for lower and UPPER case", "Calibri", 300, 24, Color.DeepSkyBlue, Color.DodgerBlue, ShapeType.TextSlantUp);
    shape.TextPath.SameLetterHeights = true;

    // Standardmäßig wird die Textgröße immer an die Größe der enthaltenden Form angepasst und überschreibt dabei die Einstellung für die Textgröße.
    shape = AppendWordArt(doc, "FitShape on", "Calibri", 160, 24, Color.LightBlue, Color.Blue, ShapeType.TextPlainText);
    Assert.True(shape.TextPath.FitShape);
    shape.TextPath.Size = 24.0;

    // Wenn wir die Eigenschaft „FitShape:“ auf „false“ setzen, behält der Text die Größe
    // was die Eigenschaft „Size“ unabhängig von der Größe der Form angibt.
    // Verwenden Sie die Eigenschaft „TextPathAlignment“ auch, um den Text an einer Seite der Form auszurichten.
    shape = AppendWordArt(doc, "FitShape off", "Calibri", 160, 24, Color.LightBlue, Color.Blue, ShapeType.TextPlainText);
    shape.TextPath.FitShape = false;
    shape.TextPath.Size = 24.0;
    shape.TextPath.TextPathAlignment = TextPathAlignment.Right;

    doc.Save(ArtifactsDir + "Shape.InsertTextPaths.docx");
}

/// <summary>
/// Einen neuen Absatz mit einer WordArt-Form darin einfügen.
/// </summary>
private static Shape AppendWordArt(Document doc, string text, string textFontFamily, double shapeWidth, double shapeHeight, Color wordArtFill, Color line, ShapeType wordArtShapeType)
{
    // Erstelle eine Inline-Form, die als Container für unser WordArt dient.
    // Die Form kann nur dann eine gültige WordArt-Form sein, wenn wir ihr einen von WordArt angegebenen ShapeType zuweisen.
    // Diese Typen haben „WordArt-Objekt“ in der Beschreibung,
    // und die Namen ihrer Enumeratorkonstanten beginnen alle mit „Text“.
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

* class [TextPath](../)
* namensraum [Aspose.Words.Drawing](../../textpath/)
* Montage [Aspose.Words](../../../)


