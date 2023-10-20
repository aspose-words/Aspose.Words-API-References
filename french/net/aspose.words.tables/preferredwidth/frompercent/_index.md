---
title: PreferredWidth.FromPercent
linktitle: FromPercent
articleTitle: FromPercent
second_title: Aspose.Words pour .NET
description: PreferredWidth FromPercent méthode. Une méthode de création qui renvoie une nouvelle instance qui représente une largeur préférée spécifiée sous forme de pourcentage en C#.
type: docs
weight: 20
url: /fr/net/aspose.words.tables/preferredwidth/frompercent/
---
## PreferredWidth.FromPercent method

Une méthode de création qui renvoie une nouvelle instance qui représente une largeur préférée spécifiée sous forme de pourcentage.

```csharp
public static PreferredWidth FromPercent(double percent)
```

| Paramètre | Taper | La description |
| --- | --- | --- |
| percent | Double | La valeur doit être comprise entre 0 et 100. |

## Exemples

Montre comment définir un tableau pour qu'il s'ajuste automatiquement à 50 % de la largeur de la page.

```csharp
Document doc = new Document();
DocumentBuilder builder = new DocumentBuilder(doc);

Table table = builder.StartTable();
builder.InsertCell();
builder.Write("Cell #1");
builder.InsertCell();
builder.Write("Cell #2");
builder.InsertCell();
builder.Write("Cell #3");

table.PreferredWidth = PreferredWidth.FromPercent(50);

doc.Save(ArtifactsDir + "DocumentBuilder.InsertTableWithPreferredWidth.docx");
```

Montre comment définir une largeur préférée pour les cellules du tableau.

```csharp
Document doc = new Document();
DocumentBuilder builder = new DocumentBuilder(doc);
Table table = builder.StartTable();

// Il existe deux manières d'appliquer la classe "PreferredWidth" aux cellules d'un tableau.
// 1 - Définit une largeur préférée absolue basée sur les points :
builder.InsertCell();
builder.CellFormat.PreferredWidth = PreferredWidth.FromPoints(40);
builder.CellFormat.Shading.BackgroundPatternColor = Color.LightYellow;
builder.Writeln($"Cell with a width of {builder.CellFormat.PreferredWidth}.");

// 2 - Définit une largeur préférée relative basée sur le pourcentage de la largeur du tableau :
builder.InsertCell();
builder.CellFormat.PreferredWidth = PreferredWidth.FromPercent(20);
builder.CellFormat.Shading.BackgroundPatternColor = Color.LightBlue;
builder.Writeln($"Cell with a width of {builder.CellFormat.PreferredWidth}.");

builder.InsertCell();

// Une cellule sans largeur préférée spécifiée occupera le reste de l'espace disponible.
builder.CellFormat.PreferredWidth = PreferredWidth.Auto;

// Chaque configuration de la propriété "PreferredWidth" crée un nouvel objet.
Assert.AreNotEqual(table.FirstRow.Cells[1].CellFormat.PreferredWidth.GetHashCode(),
    builder.CellFormat.PreferredWidth.GetHashCode());

builder.CellFormat.Shading.BackgroundPatternColor = Color.LightGreen;
builder.Writeln("Automatically sized cell.");

doc.Save(ArtifactsDir + "DocumentBuilder.InsertCellsWithPreferredWidths.docx");
```

### Voir également

* class [PreferredWidth](../)
* espace de noms [Aspose.Words.Tables](../../../aspose.words.tables/)
* Assemblée [Aspose.Words](../../../)
