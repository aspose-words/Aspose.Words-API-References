---
title: PreferredWidth.Auto
linktitle: Auto
articleTitle: Auto
second_title: Aspose.Words pour .NET
description: Découvrez le champ PreferredWidth Auto, qui gère efficacement les valeurs de largeur non spécifiées pour une personnalisation optimale de la mise en page dans vos projets.
type: docs
weight: 10
url: /fr/net/aspose.words.tables/preferredwidth/auto/
---
## PreferredWidth.Auto field

Renvoie une instance qui représente la valeur « la largeur préférée n'est pas spécifiée ».

```csharp
public static readonly PreferredWidth Auto;
```

## Exemples

Montre comment définir une largeur préférée pour les cellules du tableau.

```csharp
Document doc = new Document();
DocumentBuilder builder = new DocumentBuilder(doc);
Table table = builder.StartTable();

// Il existe deux manières d'appliquer la classe « PreferredWidth » aux cellules du tableau.
// 1 - Définir une largeur préférée absolue en fonction des points :
builder.InsertCell();
builder.CellFormat.PreferredWidth = PreferredWidth.FromPoints(40);
builder.CellFormat.Shading.BackgroundPatternColor = Color.LightYellow;
builder.Writeln($"Cell with a width of {builder.CellFormat.PreferredWidth}.");

// 2 - Définir une largeur préférée relative en fonction du pourcentage de la largeur du tableau :
builder.InsertCell();
builder.CellFormat.PreferredWidth = PreferredWidth.FromPercent(20);
builder.CellFormat.Shading.BackgroundPatternColor = Color.LightBlue;
builder.Writeln($"Cell with a width of {builder.CellFormat.PreferredWidth}.");

builder.InsertCell();

// Une cellule sans largeur préférée spécifiée occupera le reste de l'espace disponible.
builder.CellFormat.PreferredWidth = PreferredWidth.Auto;

// Chaque configuration de la propriété « PreferredWidth » crée un nouvel objet.
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
