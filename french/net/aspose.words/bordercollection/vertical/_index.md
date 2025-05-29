---
title: BorderCollection.Vertical
linktitle: Vertical
articleTitle: Vertical
second_title: Aspose.Words pour .NET
description: Découvrez la propriété BorderCollection Vertical pour des bordures de cellules harmonieuses. Sublimez votre design avec des bordures verticales personnalisables pour un rendu soigné !
type: docs
weight: 130
url: /fr/net/aspose.words/bordercollection/vertical/
---
## BorderCollection.Vertical property

Obtient la bordure verticale utilisée entre les cellules.

```csharp
public Border Vertical { get; }
```

## Exemples

Montre comment appliquer des paramètres aux bordures verticales au format d'une ligne de tableau.

```csharp
Document doc = new Document();
DocumentBuilder builder = new DocumentBuilder(doc);

// Créez un tableau avec des bordures intérieures rouges et bleues.
Table table = builder.StartTable();

for (int i = 0; i < 3; i++)
{
    builder.InsertCell();
    builder.Write($"Row {i + 1}, Column 1");
    builder.InsertCell();
    builder.Write($"Row {i + 1}, Column 2");

    Row row = builder.EndRow();
    BorderCollection borders = row.RowFormat.Borders;

    // Ajustez l'apparence des bordures qui apparaîtront entre les lignes.
    borders.Horizontal.Color = Color.Red;
    borders.Horizontal.LineStyle = LineStyle.Dot;
    borders.Horizontal.LineWidth = 2.0d;

    // Ajustez l'apparence des bordures qui apparaîtront entre les cellules.
    borders.Vertical.Color = Color.Blue;
    borders.Vertical.LineStyle = LineStyle.Dot;
    borders.Vertical.LineWidth = 2.0d;
}

// Un format de ligne et le paragraphe intérieur d'une cellule utilisent des paramètres de bordure différents.
Border border = table.FirstRow.FirstCell.LastParagraph.ParagraphFormat.Borders.Vertical;

Assert.AreEqual(Color.Empty.ToArgb(), border.Color.ToArgb());
Assert.AreEqual(0.0d, border.LineWidth);
Assert.AreEqual(LineStyle.None, border.LineStyle);

doc.Save(ArtifactsDir + "Border.VerticalBorders.docx");
```

### Voir également

* class [Border](../../border/)
* class [BorderCollection](../)
* espace de noms [Aspose.Words](../../../aspose.words/)
* Assemblée [Aspose.Words](../../../)
