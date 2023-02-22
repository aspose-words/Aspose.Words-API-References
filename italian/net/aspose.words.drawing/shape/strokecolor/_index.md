---
title: Shape.StrokeColor
second_title: Aspose.Words per .NET API Reference
description: Shape proprietà. Definisce il colore di un tratto.
type: docs
weight: 190
url: /it/net/aspose.words.drawing/shape/strokecolor/
---
## Shape.StrokeColor property

Definisce il colore di un tratto.

```csharp
public Color StrokeColor { get; set; }
```

### Osservazioni

Questa è una scorciatoia per il[`Color`](../../stroke/color/) proprietà.

Il valore predefinito è Black.

### Esempi

Mostra come riempire una forma con un colore solido.

```csharp
Document doc = new Document();
DocumentBuilder builder = new DocumentBuilder(doc);

// Scrivi del testo e poi coprilo con una forma fluttuante.
builder.Font.Size = 32;
builder.Writeln("Hello world!");

Shape shape = builder.InsertShape(ShapeType.CloudCallout, RelativeHorizontalPosition.LeftMargin, 25,
    RelativeVerticalPosition.TopMargin, 25, 250, 150, WrapType.None);

// Usa la proprietà "StrokeColor" per impostare il colore del contorno della forma.
shape.StrokeColor = Color.CadetBlue;

// Usa la proprietà "FillColor" per impostare il colore dell'area interna della forma.
shape.FillColor = Color.LightBlue;

// La proprietà "Opacità" determina la trasparenza del colore su una scala 0-1,
// con 1 completamente opaco e 0 invisibile.
// Il riempimento della forma per impostazione predefinita è completamente opaco, quindi non possiamo vedere il testo su cui si trova questa forma.
Assert.AreEqual(1.0d, shape.Fill.Opacity);

// Imposta l'opacità del colore di riempimento della forma su un valore inferiore in modo da poter vedere il testo sottostante.
shape.Fill.Opacity = 0.3;

doc.Save(ArtifactsDir + "Shape.Fill.docx");
```

Mostra come scorrere tutte le forme in un documento.

```csharp
{
    Document doc = new Document(MyDir + "Revision shape.docx");
    ShapeAppearancePrinter visitor = new ShapeAppearancePrinter();
    doc.Accept(visitor);

    Console.WriteLine(visitor.GetText());
}

/// <summary>
/// Registra le informazioni relative all'aspetto delle forme visitate.
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
    /// Aggiunge una riga a StringBuilder con un carattere di tabulazione anteposto per ogni livello di rientro.
    /// </summary>
    private void AppendLine(string text)
    {
        for (int i = 0; i < mTextIndentLevel; i++) mStringBuilder.Append('\t');

        mStringBuilder.AppendLine(text);
    }

    /// <summary>
    /// Restituisce tutto il testo accumulato da StringBuilder.
    /// </summary>
    public string GetText()
    {
        return $"Shapes visited: {mShapesVisited}\n{mStringBuilder}";
    }

    /// <summary>
    /// Chiamato quando questo visitatore visita l'inizio di un nodo Shape.
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
    /// Chiamato quando questo visitatore visita la fine di un nodo Shape.
    /// </summary>
    public override VisitorAction VisitShapeEnd(Shape shape)
    {
        mTextIndentLevel--;
        mShapesVisited++;
        AppendLine($"End of {shape.ShapeType}");

        return VisitorAction.Continue;
    }

    /// <summary>
    /// Chiamato quando questo visitatore visita l'inizio di un nodo GroupShape.
    /// </summary>
    public override VisitorAction VisitGroupShapeStart(GroupShape groupShape)
    {
        AppendLine($"Shape group found: {groupShape.ShapeType}");
        mTextIndentLevel++;

        return VisitorAction.Continue;
    }

    /// <summary>
    /// Chiamato quando questo visitatore visita la fine di un nodo GroupShape.
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

### Guarda anche

* class [Shape](../)
* spazio dei nomi [Aspose.Words.Drawing](../../shape/)
* assemblea [Aspose.Words](../../../)


