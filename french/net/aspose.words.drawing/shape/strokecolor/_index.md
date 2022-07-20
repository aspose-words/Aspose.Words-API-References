---
title: StrokeColor
second_title: Référence de l'API Aspose.Words pour .NET
description: Définit la couleur dun trait.
type: docs
weight: 190
url: /fr/net/aspose.words.drawing/shape/strokecolor/
---
## Shape.StrokeColor property

Définit la couleur d'un trait.

```csharp
public Color StrokeColor { get; set; }
```

### Remarques

Il s'agit d'un raccourci vers le[`Color`](../../stroke/color) propriété.

La valeur par défaut est Black.

### Exemples

Montre comment remplir une forme avec une couleur unie.

```csharp
Document doc = new Document();
DocumentBuilder builder = new DocumentBuilder(doc);

// Écrivez du texte, puis recouvrez-le d'une forme flottante.
builder.Font.Size = 32;
builder.Writeln("Hello world!");

Shape shape = builder.InsertShape(ShapeType.CloudCallout, RelativeHorizontalPosition.LeftMargin, 25,
    RelativeVerticalPosition.TopMargin, 25, 250, 150, WrapType.None);

// Utilisez la propriété "StrokeColor" pour définir la couleur du contour de la forme.
shape.StrokeColor = Color.CadetBlue;

// Utilisez la propriété "FillColor" pour définir la couleur de la zone intérieure de la forme.
shape.FillColor = Color.LightBlue;

// La propriété "Opacité" détermine la transparence de la couleur sur une échelle de 0 à 1,
// avec 1 étant entièrement opaque et 0 étant invisible.
// Le remplissage de la forme par défaut est entièrement opaque, nous ne pouvons donc pas voir le texte sur lequel cette forme se trouve.
Assert.AreEqual(1.0d, shape.Fill.Opacity);

// Définit l'opacité de la couleur de remplissage de la forme sur une valeur inférieure afin que nous puissions voir le texte en dessous.
shape.Fill.Opacity = 0.3;

doc.Save(ArtifactsDir + "Shape.Fill.docx");
```

Montre comment parcourir toutes les formes d'un document.

```csharp
{
    Document doc = new Document(MyDir + "Revision shape.docx");
    ShapeAppearancePrinter visitor = new ShapeAppearancePrinter();
    doc.Accept(visitor);

    Console.WriteLine(visitor.GetText());
}

/// <summary>
/// Consigne les informations relatives à l'apparence des formes visitées.
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
    /// Ajoute une ligne au StringBuilder avec un caractère de tabulation ajouté pour chaque niveau d'indentation.
    /// </summary>
    private void AppendLine(string text)
    {
        for (int i = 0; i < mTextIndentLevel; i++) mStringBuilder.Append('\t');

        mStringBuilder.AppendLine(text);
    }

    /// <summary>
    /// Renvoie tout le texte que le StringBuilder a accumulé.
    /// </summary>
    public string GetText()
    {
        return $"Shapes visited: {mShapesVisited}\n{mStringBuilder}";
    }

    /// <summary>
    /// Appelé lorsque ce visiteur visite le début d'un nœud Shape.
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
    /// Appelé lorsque ce visiteur visite la fin d'un nœud Shape.
    /// </summary>
    public override VisitorAction VisitShapeEnd(Shape shape)
    {
        mTextIndentLevel--;
        mShapesVisited++;
        AppendLine($"End of {shape.ShapeType}");

        return VisitorAction.Continue;
    }

    /// <summary>
    /// Appelé lorsque ce visiteur visite le début d'un nœud GroupShape.
    /// </summary>
    public override VisitorAction VisitGroupShapeStart(GroupShape groupShape)
    {
        AppendLine($"Shape group found: {groupShape.ShapeType}");
        mTextIndentLevel++;

        return VisitorAction.Continue;
    }

    /// <summary>
    /// Appelé lorsque ce visiteur visite la fin d'un nœud GroupShape.
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

### Voir également

* class [Shape](../../shape)
* espace de noms [Aspose.Words.Drawing](../../shape)
* Assemblée [Aspose.Words](../../../)

<!-- DO NOT EDIT: generated by xmldocmd for Aspose.Words.dll -->
