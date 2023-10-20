---
title: Table.ConvertToHorizontallyMergedCells
linktitle: ConvertToHorizontallyMergedCells
articleTitle: ConvertToHorizontallyMergedCells
second_title: Aspose.Words pour .NET
description: Table ConvertToHorizontallyMergedCells méthode. Convertit les cellules fusionnées horizontalement par largeur en cellules fusionnées parHorizontalMerge  en C#.
type: docs
weight: 390
url: /fr/net/aspose.words.tables/table/converttohorizontallymergedcells/
---
## Table.ConvertToHorizontallyMergedCells method

Convertit les cellules fusionnées horizontalement par largeur en cellules fusionnées par[`HorizontalMerge`](../../cellformat/horizontalmerge/) .

```csharp
public void ConvertToHorizontallyMergedCells()
```

## Remarques

Les cellules du tableau peuvent être fusionnées horizontalement à l'aide d'indicateurs de fusion[`HorizontalMerge`](../../cellformat/horizontalmerge/) ou en utilisant la largeur de cellule[`Width`](../../cellformat/width/).

Lorsque la cellule du tableau est fusionnée par la propriété width[`HorizontalMerge`](../../cellformat/horizontalmerge/) cela n'a aucun sens, mais parfois, avoir des indicateurs de fusion est un moyen plus pratique.

Utilisez cette méthode pour transformer les cellules du tableau fusionnées horizontalement par largeur en cellules fusionnées par des indicateurs de fusion.

## Exemples

Montre comment convertir des cellules fusionnées horizontalement par largeur en cellules fusionnées par CellFormat.HorizontalMerge.

```csharp
Document doc = new Document(MyDir + "Table with merged cells.docx");

// Microsoft Word n'écrit plus d'indicateurs de fusion, définissant plutôt les cellules fusionnées par largeur.
// Aspose.Words définit par défaut seulement 5 cellules d'affilée, et aucune d'entre elles n'a l'indicateur de fusion horizontale,
// même s'il y avait 7 cellules dans la ligne avant la fusion horizontale.
Table table = doc.FirstSection.Body.Tables[0];
Row row = table.Rows[0];

Assert.AreEqual(5, row.Cells.Count);
Assert.True(row.Cells.All(c => ((Cell)c).CellFormat.HorizontalMerge == CellMerge.None));

// Utilisez la méthode "ConvertToHorizontallyMergedCells" pour convertir les cellules fusionnées horizontalement
// par sa largeur à la cellule fusionnée horizontalement par les drapeaux.
// Maintenant, nous avons 7 cellules, et certaines d'entre elles ont des valeurs de fusion horizontale.
table.ConvertToHorizontallyMergedCells();
row = table.Rows[0];

Assert.AreEqual(7, row.Cells.Count);

Assert.AreEqual(CellMerge.None, row.Cells[0].CellFormat.HorizontalMerge);
Assert.AreEqual(CellMerge.First, row.Cells[1].CellFormat.HorizontalMerge);
Assert.AreEqual(CellMerge.Previous, row.Cells[2].CellFormat.HorizontalMerge);
Assert.AreEqual(CellMerge.None, row.Cells[3].CellFormat.HorizontalMerge);
Assert.AreEqual(CellMerge.First, row.Cells[4].CellFormat.HorizontalMerge);
Assert.AreEqual(CellMerge.Previous, row.Cells[5].CellFormat.HorizontalMerge);
Assert.AreEqual(CellMerge.None, row.Cells[6].CellFormat.HorizontalMerge);
```

### Voir également

* class [Table](../)
* espace de noms [Aspose.Words.Tables](../../../aspose.words.tables/)
* Assemblée [Aspose.Words](../../../)
