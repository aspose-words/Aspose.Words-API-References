---
title: BorderCollection.Horizontal
linktitle: Horizontal
articleTitle: Horizontal
second_title: Aspose.Words pour .NET
description: Découvrez la propriété BorderCollection Horizontal pour des bordures de cellules et de paragraphes harmonieuses. Améliorez votre mise en page avec un alignement et un style parfaits !
type: docs
weight: 50
url: /fr/net/aspose.words/bordercollection/horizontal/
---
## BorderCollection.Horizontal property

Obtient la bordure horizontale utilisée entre les cellules ou les paragraphes conformes.

```csharp
public Border Horizontal { get; }
```

## Exemples

Montre comment appliquer des paramètres aux bordures horizontales au format d'un paragraphe.

```csharp
Document doc = new Document();
DocumentBuilder builder = new DocumentBuilder(doc);

// Créez une bordure horizontale rouge pour le paragraphe. Tous les paragraphes créés ultérieurement hériteront de ces paramètres de bordure.
BorderCollection borders = doc.FirstSection.Body.FirstParagraph.ParagraphFormat.Borders;
borders.Horizontal.Color = Color.Red;
borders.Horizontal.LineStyle = LineStyle.DashSmallGap;
borders.Horizontal.LineWidth = 3;

// Écrivez du texte dans le document sans créer de nouveau paragraphe par la suite.
// Comme il n'y a pas de paragraphe en dessous, la bordure horizontale ne sera pas visible.
builder.Write("Paragraph above horizontal border.");

// Une fois que nous avons ajouté un deuxième paragraphe, la bordure du premier paragraphe deviendra visible.
builder.InsertParagraph();
builder.Write("Paragraph below horizontal border.");

doc.Save(ArtifactsDir + "Border.HorizontalBorders.docx");
```

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
