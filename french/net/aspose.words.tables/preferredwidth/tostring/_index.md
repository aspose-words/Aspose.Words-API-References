---
title: PreferredWidth.ToString
linktitle: ToString
articleTitle: ToString
second_title: Aspose.Words pour .NET
description: PreferredWidth ToString méthode. Renvoie une chaîne conviviale qui affiche la valeur de cet objet en C#.
type: docs
weight: 80
url: /fr/net/aspose.words.tables/preferredwidth/tostring/
---
## PreferredWidth.ToString method

Renvoie une chaîne conviviale qui affiche la valeur de cet objet.

```csharp
public override string ToString()
```

## Exemples

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
