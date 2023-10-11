---
title: PreferredWidth.GetHashCode
second_title: Référence de l'API Aspose.Words pour .NET
description: PreferredWidth méthode. Sert de fonction de hachage pour ce type.
type: docs
weight: 70
url: /fr/net/aspose.words.tables/preferredwidth/gethashcode/
---
## PreferredWidth.GetHashCode method

Sert de fonction de hachage pour ce type.

```csharp
public override int GetHashCode()
```

### Exemples

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
* espace de noms [Aspose.Words.Tables](../../preferredwidth/)
* Assemblée [Aspose.Words](../../../)


