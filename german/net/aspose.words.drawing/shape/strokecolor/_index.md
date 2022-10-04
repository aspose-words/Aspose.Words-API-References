---
title: StrokeColor
second_title: Aspose.Words für .NET-API-Referenz
description: Definiert die Farbe eines Strichs.
type: docs
weight: 190
url: /de/net/aspose.words.drawing/shape/strokecolor/
---
## Shape.StrokeColor property

Definiert die Farbe eines Strichs.

```csharp
public Color StrokeColor { get; set; }
```

### Bemerkungen

Dies ist eine Verknüpfung zum[`Color`](../../stroke/color/) Eigentum.

Der Standardwert ist Black.

### Beispiele

Zeigt, wie eine Form mit einer Volltonfarbe gefüllt wird.

```csharp
Document doc = new Document();
DocumentBuilder builder = new DocumentBuilder(doc);

// Schreiben Sie etwas Text und bedecken Sie ihn dann mit einer schwebenden Form.
builder.Font.Size = 32;
builder.Writeln("Hello world!");

Shape shape = builder.InsertShape(ShapeType.CloudCallout, RelativeHorizontalPosition.LeftMargin, 25,
    RelativeVerticalPosition.TopMargin, 25, 250, 150, WrapType.None);

// Verwenden Sie die Eigenschaft "StrokeColor", um die Farbe des Umrisses der Form festzulegen.
shape.StrokeColor = Color.CadetBlue;

// Verwenden Sie die Eigenschaft "FillColor", um die Farbe des Innenbereichs der Form festzulegen.
shape.FillColor = Color.LightBlue;

// Die Eigenschaft "Deckkraft" bestimmt, wie transparent die Farbe auf einer Skala von 0-1 ist,
// wobei 1 vollständig undurchsichtig und 0 unsichtbar ist.
// Die Formfüllung ist standardmäßig vollständig undurchsichtig, sodass wir den Text, auf dem sich diese Form befindet, nicht sehen können.
Assert.AreEqual(1.0d, shape.Fill.Opacity);

// Setzen Sie die Deckkraft der Füllfarbe der Form auf einen niedrigeren Wert, damit wir den Text darunter sehen können.
shape.Fill.Opacity = 0.3;

doc.Save(ArtifactsDir + "Shape.Fill.docx");
```

Zeigt, wie alle Formen in einem Dokument durchlaufen werden.

```csharp
{
    Document doc = new Document(MyDir + "Revision shape.docx");
    ShapeAppearancePrinter visitor = new ShapeAppearancePrinter();
    doc.Accept(visitor);

    Console.WriteLine(visitor.GetText());
}

/// <summary>
/// Protokolliert erscheinungsbezogene Informationen über besuchte Shapes.
/// </summary>
private class ShapeAppearancePrinter : DocumentVisitor
{
    public ShapeAppearancePrinter()
    {
        mShapesVisited = 0;
        mTextIndentLevel = 0;
        mStringBuilder = new StringBuilder();
    }

    /// <summary>
    /// Hängt eine Zeile mit einem vorangestellten Tabulatorzeichen für jede Einzugsebene an den StringBuilder an.
    /// </summary>
    private void AppendLine(string text)
    {
        for (int i = 0; i < mTextIndentLevel; i++) mStringBuilder.Append('\t');

        mStringBuilder.AppendLine(text);
    }

    /// <summary>
    /// Den gesamten Text zurückgeben, den der StringBuilder angesammelt hat.
    /// </summary>
    public string GetText()
    {
        return $"Shapes visited: {mShapesVisited}\n{mStringBuilder}";
    }

    /// <summary>
    /// Wird aufgerufen, wenn dieser Besucher den Anfang eines Shape-Knotens besucht.
    /// </summary>
    public override VisitorAction VisitShapeStart(Shape shape)
    {
        AppendLine($"Shape found: {shape.ShapeType}");

        mTextIndentLevel++;

        if (shape.HasChart)
            AppendLine($"Has chart: {shape.Chart.Title.Text}");

        AppendLine($"Extrusion enabled: {shape.ExtrusionEnabled}");
        AppendLine($"Shadow enabled: {shape.ShadowEnabled}");
        AppendLine($"StoryType: {shape.StoryType}");

        if (shape.Stroked)
        {
            Assert.AreEqual(shape.Stroke.Color, shape.StrokeColor);
            AppendLine($"Stroke colors: {shape.Stroke.Color}, {shape.Stroke.Color2}");
            AppendLine($"Stroke weight: {shape.StrokeWeight}");

        }

        if (shape.Filled)
            AppendLine($"Filled: {shape.FillColor}");

        if (shape.OleFormat != null)
            AppendLine($"Ole found of type: {shape.OleFormat.ProgId}");

        if (shape.SignatureLine != null)
            AppendLine($"Found signature line for: {shape.SignatureLine.Signer}, {shape.SignatureLine.SignerTitle}");

        return VisitorAction.Continue;
    }

    /// <summary>
    /// Wird aufgerufen, wenn dieser Besucher das Ende eines Shape-Knotens besucht.
    /// </summary>
    public override VisitorAction VisitShapeEnd(Shape shape)
    {
        mTextIndentLevel--;
        mShapesVisited++;
        AppendLine($"End of {shape.ShapeType}");

        return VisitorAction.Continue;
    }

    /// <summary>
    /// Wird aufgerufen, wenn dieser Besucher den Anfang eines GroupShape-Knotens besucht.
    /// </summary>
    public override VisitorAction VisitGroupShapeStart(GroupShape groupShape)
    {
        AppendLine($"Shape group found: {groupShape.ShapeType}");
        mTextIndentLevel++;

        return VisitorAction.Continue;
    }

    /// <summary>
    /// Wird aufgerufen, wenn dieser Besucher das Ende eines GroupShape-Knotens besucht.
    /// </summary>
    public override VisitorAction VisitGroupShapeEnd(GroupShape groupShape)
    {
        mTextIndentLevel--;
        AppendLine($"End of {groupShape.ShapeType}");

        return VisitorAction.Continue;
    }

    private int mShapesVisited;
    private int mTextIndentLevel;
    private readonly StringBuilder mStringBuilder;
}
```

### Siehe auch

* class [Shape](../)
* namensraum [Aspose.Words.Drawing](../../shape/)
* Montage [Aspose.Words](../../../)

<!-- DO NOT EDIT: generated by xmldocmd for Aspose.Words.dll -->
