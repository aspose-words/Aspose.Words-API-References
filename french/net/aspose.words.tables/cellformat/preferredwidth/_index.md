---
title: CellFormat.PreferredWidth
linktitle: PreferredWidth
articleTitle: PreferredWidth
second_title: Aspose.Words pour .NET
description: Découvrez la propriété CellFormat PreferredWidth pour personnaliser facilement la largeur des cellules et optimiser la mise en page et le design de vos feuilles de calcul. Améliorez la présentation de vos données !
type: docs
weight: 80
url: /fr/net/aspose.words.tables/cellformat/preferredwidth/
---
## CellFormat.PreferredWidth property

Renvoie ou définit la largeur préférée de la cellule.

```csharp
public PreferredWidth PreferredWidth { get; set; }
```

## Remarques

La largeur préférée (ainsi que l'option d'ajustement automatique du tableau) détermine comment la largeur réelle de la cellule est calculée par l'algorithme de mise en page du tableau. La mise en page du tableau peut être effectuée par Aspose.Words lors de l'enregistrement du document ou par Microsoft Word lors de son affichage.

La largeur préférée peut être spécifiée en points ou en pourcentage. La largeur préférée (largeur ) peut également être définie sur « auto », ce qui signifie qu'aucune largeur préférée n'est spécifiée.

La valeur par défaut est[`Auto`](../../preferredwidth/auto/).

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

* class [PreferredWidth](../../preferredwidth/)
* class [CellFormat](../)
* espace de noms [Aspose.Words.Tables](../../../aspose.words.tables/)
* Assemblée [Aspose.Words](../../../)
