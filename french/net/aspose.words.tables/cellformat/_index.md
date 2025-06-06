---
title: CellFormat Class
linktitle: CellFormat
articleTitle: CellFormat
second_title: Aspose.Words pour .NET
description: Découvrez la classe Aspose.Words.Tables.CellFormat pour une mise en forme complète des cellules de tableau. Améliorez le style de vos documents grâce à des fonctionnalités intuitives !
type: docs
weight: 7110
url: /fr/net/aspose.words.tables/cellformat/
---
## CellFormat class

Représente toute la mise en forme d'une cellule de tableau.

Pour en savoir plus, visitez le[Travailler avec des tableaux](https://docs.aspose.com/words/net/working-with-tables/) article de documentation.

```csharp
public class CellFormat
```

## Propriétés

| Nom | La description |
| --- | --- |
| [Borders](../../aspose.words.tables/cellformat/borders/) { get; } | Obtient la collection des bordures de la cellule. |
| [BottomPadding](../../aspose.words.tables/cellformat/bottompadding/) { get; set; } | Renvoie ou définit la quantité d'espace (en points) à ajouter sous le contenu de la cellule. |
| [FitText](../../aspose.words.tables/cellformat/fittext/) { get; set; } | Si`vrai` , ajuste le texte dans la cellule, en compressant chaque paragraphe à la largeur de la cellule. |
| [HideMark](../../aspose.words.tables/cellformat/hidemark/) { get; set; } | Renvoie ou définit la visibilité de la marque de cellule. |
| [HorizontalMerge](../../aspose.words.tables/cellformat/horizontalmerge/) { get; set; } | Spécifie comment la cellule est fusionnée horizontalement avec les autres cellules de la ligne. |
| [LeftPadding](../../aspose.words.tables/cellformat/leftpadding/) { get; set; } | Renvoie ou définit la quantité d'espace (en points) à ajouter à gauche du contenu de la cellule. |
| [Orientation](../../aspose.words.tables/cellformat/orientation/) { get; set; } | Renvoie ou définit l'orientation du texte dans une cellule de tableau. |
| [PreferredWidth](../../aspose.words.tables/cellformat/preferredwidth/) { get; set; } | Renvoie ou définit la largeur préférée de la cellule. |
| [RightPadding](../../aspose.words.tables/cellformat/rightpadding/) { get; set; } | Renvoie ou définit la quantité d'espace (en points) à ajouter à droite du contenu de la cellule. |
| [Shading](../../aspose.words.tables/cellformat/shading/) { get; } | Renvoie un[`Shading`](../../aspose.words/shading/) objet qui fait référence à la mise en forme de l'ombrage de la cellule. |
| [TopPadding](../../aspose.words.tables/cellformat/toppadding/) { get; set; } | Renvoie ou définit la quantité d'espace (en points) à ajouter au-dessus du contenu de la cellule. |
| [VerticalAlignment](../../aspose.words.tables/cellformat/verticalalignment/) { get; set; } | Renvoie ou définit l'alignement vertical du texte dans la cellule. |
| [VerticalMerge](../../aspose.words.tables/cellformat/verticalmerge/) { get; set; } | Spécifie comment la cellule est fusionnée avec d'autres cellules verticalement. |
| [Width](../../aspose.words.tables/cellformat/width/) { get; set; } | Obtient la largeur de la cellule en points. |
| [WrapText](../../aspose.words.tables/cellformat/wraptext/) { get; set; } | Si`vrai` , envelopper le texte pour la cellule. |

## Méthodes

| Nom | La description |
| --- | --- |
| [ClearFormatting](../../aspose.words.tables/cellformat/clearformatting/)() | Rétablit la mise en forme par défaut de la cellule. Ne modifie pas la largeur de la cellule. |
| [SetPaddings](../../aspose.words.tables/cellformat/setpaddings/)(*double, double, double, double*) | Définit la quantité d'espace (en points) à ajouter à gauche/en haut/à droite/en bas du contenu de la cellule. |

## Exemples

Montre comment modifier la mise en forme d'une cellule de tableau.

```csharp
Document doc = new Document(MyDir + "Tables.docx");
Table table = doc.FirstSection.Body.Tables[0];
Cell firstCell = table.FirstRow.FirstCell;

// Utilisez la propriété « CellFormat » d'une cellule pour définir la mise en forme qui modifie l'apparence de cette cellule.
firstCell.CellFormat.Width = 30;
firstCell.CellFormat.Orientation = TextOrientation.Downward;
firstCell.CellFormat.Shading.ForegroundPatternColor = Color.LightGreen;

doc.Save(ArtifactsDir + "Table.CellFormat.docx");
```

Montre comment modifier le format des lignes et des cellules dans un tableau.

```csharp
Document doc = new Document();
DocumentBuilder builder = new DocumentBuilder(doc);

Table table = builder.StartTable();
builder.InsertCell();
builder.Write("City");
builder.InsertCell();
builder.Write("Country");
builder.EndRow();
builder.InsertCell();
builder.Write("London");
builder.InsertCell();
builder.Write("U.K.");
builder.EndTable();

// Utilisez la propriété « RowFormat » de la première ligne pour modifier la mise en forme
// du contenu de toutes les cellules de cette ligne.
RowFormat rowFormat = table.FirstRow.RowFormat;
rowFormat.Height = 25;
rowFormat.Borders[BorderType.Bottom].Color = Color.Red;

// Utilisez la propriété « CellFormat » de la première cellule de la dernière ligne pour modifier la mise en forme du contenu de cette cellule.
CellFormat cellFormat = table.LastRow.FirstCell.CellFormat;
cellFormat.Width = 100;
cellFormat.Shading.BackgroundPatternColor = Color.Orange;

doc.Save(ArtifactsDir + "Table.RowCellFormat.docx");
```

Montre comment créer un tableau avec des bordures personnalisées.

```csharp
Document doc = new Document();
DocumentBuilder builder = new DocumentBuilder(doc);

builder.StartTable();

// Définition des options de formatage de tableau pour un générateur de documents
// les appliquera à chaque ligne et cellule que nous ajouterons avec lui.
builder.ParagraphFormat.Alignment = ParagraphAlignment.Center;

builder.CellFormat.ClearFormatting();
builder.CellFormat.Width = 150;
builder.CellFormat.VerticalAlignment = CellVerticalAlignment.Center;
builder.CellFormat.Shading.BackgroundPatternColor = Color.GreenYellow;
builder.CellFormat.WrapText = false;
builder.CellFormat.FitText = true;

builder.RowFormat.ClearFormatting();
builder.RowFormat.HeightRule = HeightRule.Exactly;
builder.RowFormat.Height = 50;
builder.RowFormat.Borders.LineStyle = LineStyle.Engrave3D;
builder.RowFormat.Borders.Color = Color.Orange;

builder.InsertCell();
builder.Write("Row 1, Col 1");

builder.InsertCell();
builder.Write("Row 1, Col 2");
builder.EndRow();

// La modification de la mise en forme l'appliquera à la cellule actuelle,
// et toutes les nouvelles cellules que nous créons avec le générateur par la suite.
// Cela n'affectera pas les cellules que nous avons ajoutées précédemment.
builder.CellFormat.Shading.ClearFormatting();

builder.InsertCell();
builder.Write("Row 2, Col 1");

builder.InsertCell();
builder.Write("Row 2, Col 2");

builder.EndRow();

// Augmenter la hauteur de la ligne pour s'adapter au texte vertical.
builder.InsertCell();
builder.RowFormat.Height = 150;
builder.CellFormat.Orientation = TextOrientation.Upward;
builder.Write("Row 3, Col 1");

builder.InsertCell();
builder.CellFormat.Orientation = TextOrientation.Downward;
builder.Write("Row 3, Col 2");

builder.EndRow();
builder.EndTable();

doc.Save(ArtifactsDir + "DocumentBuilder.InsertTable.docx");
```

### Voir également

* espace de noms [Aspose.Words.Tables](../../aspose.words.tables/)
* Assemblée [Aspose.Words](../../)
