---
title: Shape.ShadowEnabled
second_title: Referencia de API de Aspose.Words para .NET
description: Shape propiedad. Devuelve verdadero si un efecto de sombra está habilitado.
type: docs
weight: 150
url: /es/net/aspose.words.drawing/shape/shadowenabled/
---
## Shape.ShadowEnabled property

Devuelve verdadero si un efecto de sombra está habilitado.

```csharp
public bool ShadowEnabled { get; }
```

### Ejemplos

Muestra cómo iterar sobre todas las formas en un documento.

```csharp
{
    Document doc = new Document(MyDir + "Revision shape.docx");
    ShapeAppearancePrinter visitor = new ShapeAppearancePrinter();
    doc.Accept(visitor);

    Console.WriteLine(visitor.GetText());
}

/// <summary>
/// Registra información relacionada con la apariencia de las formas visitadas.
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
    /// Agrega una línea a StringBuilder con un carácter de tabulación antepuesto para cada nivel de sangría.
    /// </summary>
    private void AppendLine(string text)
    {
        for (int i = 0; i < mTextIndentLevel; i++) mStringBuilder.Append('\t');

        mStringBuilder.AppendLine(text);
    }

    /// <summary>
    /// Devolver todo el texto que ha acumulado el StringBuilder.
    /// </summary>
    public string GetText()
    {
        return $"Shapes visited: {mShapesVisited}\n{mStringBuilder}";
    }

    /// <summary>
    /// Llamado cuando este visitante visita el inicio de un nodo Shape.
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
    /// Llamado cuando este visitante visita el final de un nodo Shape.
    /// </summary>
    public override VisitorAction VisitShapeEnd(Shape shape)
    {
        mTextIndentLevel--;
        mShapesVisited++;
        AppendLine($"End of {shape.ShapeType}");

        return VisitorAction.Continue;
    }

    /// <summary>
    /// Llamado cuando este visitante visita el inicio de un nodo GroupShape.
    /// </summary>
    public override VisitorAction VisitGroupShapeStart(GroupShape groupShape)
    {
        AppendLine($"Shape group found: {groupShape.ShapeType}");
        mTextIndentLevel++;

        return VisitorAction.Continue;
    }

    /// <summary>
    /// Llamado cuando este visitante visita el final de un nodo GroupShape.
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

### Ver también

* class [Shape](../)
* espacio de nombres [Aspose.Words.Drawing](../../shape/)
* asamblea [Aspose.Words](../../../)


