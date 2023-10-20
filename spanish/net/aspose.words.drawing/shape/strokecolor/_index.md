---
title: Shape.StrokeColor
linktitle: StrokeColor
articleTitle: StrokeColor
second_title: Aspose.Words para .NET
description: Shape StrokeColor propiedad. Define el color de un trazo en C#.
type: docs
weight: 190
url: /es/net/aspose.words.drawing/shape/strokecolor/
---
## Shape.StrokeColor property

Define el color de un trazo.

```csharp
public Color StrokeColor { get; set; }
```

## Observaciones

Este es un atajo hacia el[`Color`](../../stroke/color/) propiedad.

El valor predeterminado es Black.

## Ejemplos

Muestra cómo rellenar una forma con un color sólido.

```csharp
Document doc = new Document();
DocumentBuilder builder = new DocumentBuilder(doc);

// Escribe un texto y luego cúbrelo con una forma flotante.
builder.Font.Size = 32;
builder.Writeln("Hello world!");

Shape shape = builder.InsertShape(ShapeType.CloudCallout, RelativeHorizontalPosition.LeftMargin, 25,
    RelativeVerticalPosition.TopMargin, 25, 250, 150, WrapType.None);

// Utilice la propiedad "StrokeColor" para establecer el color del contorno de la forma.
shape.StrokeColor = Color.CadetBlue;

// Utilice la propiedad "FillColor" para establecer el color del área interior de la forma.
shape.FillColor = Color.LightBlue;

// La propiedad "Opacidad" determina qué tan transparente es el color en una escala de 0-1,
// siendo 1 completamente opaco y 0 invisible.
// El relleno de forma por defecto es completamente opaco, por lo que no podemos ver el texto sobre el que se encuentra esta forma.
Assert.AreEqual(1.0d, shape.Fill.Opacity);

// Establece la opacidad del color de relleno de la forma en un valor más bajo para que podamos ver el texto debajo.
shape.Fill.Opacity = 0.3;

doc.Save(ArtifactsDir + "Shape.Fill.docx");
```

Muestra cómo iterar sobre todas las formas de un documento.

```csharp
public void VisitShapes()
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
    /// Agrega una línea al StringBuilder con un carácter de tabulación antepuesto para cada nivel de sangría.
    /// </summary>
    private void AppendLine(string text)
    {
        for (int i = 0; i < mTextIndentLevel; i++) mStringBuilder.Append('\t');

        mStringBuilder.AppendLine(text);
    }

    /// <summary>
    /// Devuelve todo el texto que ha acumulado StringBuilder.
    /// </summary>
    public string GetText()
    {
        return $"Shapes visited: {mShapesVisited}\n{mStringBuilder}";
    }

    /// <summary>
    /// Se llama cuando este visitante visita el inicio de un nodo Shape.
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
    /// Se llama cuando este visitante visita el final de un nodo Shape.
    /// </summary>
    public override VisitorAction VisitShapeEnd(Shape shape)
    {
        mTextIndentLevel--;
        mShapesVisited++;
        AppendLine($"End of {shape.ShapeType}");

        return VisitorAction.Continue;
    }

    /// <summary>
    /// Se llama cuando este visitante visita el inicio de un nodo GroupShape.
    /// </summary>
    public override VisitorAction VisitGroupShapeStart(GroupShape groupShape)
    {
        AppendLine($"Shape group found: {groupShape.ShapeType}");
        mTextIndentLevel++;

        return VisitorAction.Continue;
    }

    /// <summary>
    /// Se llama cuando este visitante visita el final de un nodo GroupShape.
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
* espacio de nombres [Aspose.Words.Drawing](../../../aspose.words.drawing/)
* asamblea [Aspose.Words](../../../)
