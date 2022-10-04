---
title: RowFormat
second_title: Référence de l'API Aspose.Words pour .NET
description: Représente toute la mise en forme dune ligne de tableau.
type: docs
weight: 6030
url: /fr/net/aspose.words.tables/rowformat/
---
## RowFormat class

Représente toute la mise en forme d'une ligne de tableau.

```csharp
public class RowFormat
```

## Propriétés

| Nom | La description |
| --- | --- |
| [AllowBreakAcrossPages](../../aspose.words.tables/rowformat/allowbreakacrosspages/) { get; set; } | Vrai si le texte d'une ligne de tableau est autorisé à être fractionné sur un saut de page. |
| [Borders](../../aspose.words.tables/rowformat/borders/) { get; } | Obtient la collection de bordures de cellule par défaut pour la ligne. |
| [HeadingFormat](../../aspose.words.tables/rowformat/headingformat/) { get; set; } | Vrai si la ligne est répétée en tant qu'en-tête de tableau sur chaque page lorsque le tableau s'étend sur plusieurs pages. |
| [Height](../../aspose.words.tables/rowformat/height/) { get; set; } | Obtient ou définit la hauteur de la ligne du tableau en points. |
| [HeightRule](../../aspose.words.tables/rowformat/heightrule/) { get; set; } | Obtient ou définit la règle pour déterminer la hauteur de la ligne du tableau. |

## Méthodes

| Nom | La description |
| --- | --- |
| [ClearFormatting](../../aspose.words.tables/rowformat/clearformatting/)() | Réinitialise le formatage de ligne par défaut. |

### Exemples

Montre comment modifier la mise en forme d'une ligne de tableau.

```csharp
Document doc = new Document(MyDir + "Tables.docx");
Table table = doc.FirstSection.Body.Tables[0];

// Utilisez la propriété "RowFormat" de la première ligne pour définir le formatage qui modifie l'apparence de cette ligne entière.
Row firstRow = table.FirstRow;
firstRow.RowFormat.Borders.LineStyle = LineStyle.None;
firstRow.RowFormat.HeightRule = HeightRule.Auto;
firstRow.RowFormat.AllowBreakAcrossPages = true;

doc.Save(ArtifactsDir + "Table.RowFormat.docx");
```

Montre comment modifier le format des lignes et des cellules d'un tableau.

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

// Utiliser la propriété "RowFormat" de la première ligne pour modifier la mise en forme
// du contenu de toutes les cellules de cette ligne.
RowFormat rowFormat = table.FirstRow.RowFormat;
rowFormat.Height = 25;
rowFormat.Borders[BorderType.Bottom].Color = Color.Red;

// Utilisez la propriété "CellFormat" de la première cellule de la dernière ligne pour modifier la mise en forme du contenu de cette cellule.
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

// Définition des options de formatage de tableau pour un générateur de document
// les appliquera à chaque ligne et cellule que nous ajouterons avec.
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

// Changer la mise en forme l'appliquera à la cellule courante,
// et toutes les nouvelles cellules que nous créons avec le constructeur par la suite.
// Cela n'affectera pas les cellules que nous avons ajoutées précédemment.
builder.CellFormat.Shading.ClearFormatting();

builder.InsertCell();
builder.Write("Row 2, Col 1");

builder.InsertCell();
builder.Write("Row 2, Col 2");

builder.EndRow();

// Augmente la hauteur de ligne pour s'adapter au texte vertical.
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

<!-- DO NOT EDIT: generated by xmldocmd for Aspose.Words.dll -->
