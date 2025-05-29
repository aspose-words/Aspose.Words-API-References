---
title: Row.RowFormat
linktitle: RowFormat
articleTitle: RowFormat
second_title: Aspose.Words pour .NET
description: Découvrez la propriété Row RowFormat pour un accès facile aux options de formatage de ligne personnalisables, améliorant ainsi la présentation de vos données sans effort.
type: docs
weight: 110
url: /fr/net/aspose.words.tables/row/rowformat/
---
## Row.RowFormat property

Donne accès aux propriétés de formatage de la ligne.

```csharp
public RowFormat RowFormat { get; }
```

## Exemples

Montre comment modifier la mise en forme d'une ligne de tableau.

```csharp
Document doc = new Document(MyDir + "Tables.docx");
Table table = doc.FirstSection.Body.Tables[0];

// Utilisez la propriété « RowFormat » de la première ligne pour définir la mise en forme qui modifie l'apparence de cette ligne entière.
Row firstRow = table.FirstRow;
firstRow.RowFormat.Borders.LineStyle = LineStyle.None;
firstRow.RowFormat.HeightRule = HeightRule.Auto;
firstRow.RowFormat.AllowBreakAcrossPages = true;

doc.Save(ArtifactsDir + "Table.RowFormat.docx");
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

### Voir également

* class [RowFormat](../../rowformat/)
* class [Row](../)
* espace de noms [Aspose.Words.Tables](../../../aspose.words.tables/)
* Assemblée [Aspose.Words](../../../)
