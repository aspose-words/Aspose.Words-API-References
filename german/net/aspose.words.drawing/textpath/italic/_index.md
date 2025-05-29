---
title: TextPath.Italic
linktitle: Italic
articleTitle: Italic
second_title: Aspose.Words für .NET
description: Entdecken Sie die TextPath Italic-Eigenschaft. Überprüfen Sie ganz einfach, ob Ihre Schrift kursiv formatiert ist, um Textdesign und Lesbarkeit zu verbessern. Verbessern Sie Ihre Typografie noch heute!
type: docs
weight: 50
url: /de/net/aspose.words.drawing/textpath/italic/
---
## TextPath.Italic property

Wahr, wenn die Schriftart kursiv formatiert ist.

```csharp
public bool Italic { get; set; }
```

## Bemerkungen

Der Standardwert ist`FALSCH`.

## Beispiele

Zeigt, wie mit WordArt gearbeitet wird.

```csharp
public void InsertTextPaths()
{
    Document doc = new Document();

    // Fügen Sie ein WordArt-Objekt ein, um Text in einer Form anzuzeigen, deren Größe wir mithilfe der Maus in Microsoft Word ändern und verschieben können.
    // Geben Sie einen „ShapeType“ als Argument an, um eine Form für das WordArt festzulegen.
    Shape shape = AppendWordArt(doc, "Hello World! This text is bold, and italic.",
        "Arial", 480, 24, Color.White, Color.Black, ShapeType.TextPlainText);

    // Wenden Sie die Formatierungseinstellungen „Fett“ und „Kursiv“ mithilfe der jeweiligen Eigenschaften auf den Text an.
    shape.TextPath.Bold = true;
    shape.TextPath.Italic = true;

    // Nachfolgend finden Sie verschiedene andere Eigenschaften zur Textformatierung.
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

    // Verwenden Sie die Eigenschaft „Ein“, um den Text anzuzeigen/auszublenden.
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

    // Setzen Sie die Eigenschaft „SameLetterHeights“ auf „true“, um die x-Höhe jedes Zeichens gleich der Großbuchstabenhöhe zu machen.
    shape = AppendWordArt(doc, "Same character height for lower and UPPER case", "Calibri", 300, 24, Color.DeepSkyBlue, Color.DodgerBlue, ShapeType.TextSlantUp);
    shape.TextPath.SameLetterHeights = true;

    // Standardmäßig wird die Textgröße immer an die Größe der enthaltenen Form angepasst und die Einstellung für die Textgröße überschrieben.
    shape = AppendWordArt(doc, "FitShape on", "Calibri", 160, 24, Color.LightBlue, Color.Blue, ShapeType.TextPlainText);
    Assert.True(shape.TextPath.FitShape);
    shape.TextPath.Size = 24.0;

    // Wenn wir die Eigenschaft "FitShape:" auf "false" setzen, behält der Text die Größe
    // die die Eigenschaft „Größe“ unabhängig von der Größe der Form angibt.
    // Verwenden Sie die Eigenschaft „TextPathAlignment“, um den Text auch an einer Seite der Form auszurichten.
    shape = AppendWordArt(doc, "FitShape off", "Calibri", 160, 24, Color.LightBlue, Color.Blue, ShapeType.TextPlainText);
    shape.TextPath.FitShape = false;
    shape.TextPath.Size = 24.0;
    shape.TextPath.TextPathAlignment = TextPathAlignment.Right;

    doc.Save(ArtifactsDir + "Shape.InsertTextPaths.docx");
}

/// <summary>
/// Fügen Sie einen neuen Absatz mit einer WordArt-Form darin ein.
/// </summary>
private static Shape AppendWordArt(Document doc, string text, string textFontFamily, double shapeWidth, double shapeHeight, Color wordArtFill, Color line, ShapeType wordArtShapeType)
{
    // Erstellen Sie eine Inline-Form, die als Container für unser WordArt dient.
    // Die Form kann nur dann eine gültige WordArt-Form sein, wenn wir ihr einen von WordArt festgelegten ShapeType zuweisen.
    // Diese Typen haben „WordArt-Objekt“ in der Beschreibung,
    // und ihre Enumeratorkonstantennamen beginnen alle mit „Text“.
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
* namensraum [Aspose.Words.Drawing](../../../aspose.words.drawing/)
* Montage [Aspose.Words](../../../)
