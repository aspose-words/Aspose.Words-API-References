---
title: Table.ConvertToHorizontallyMergedCells
second_title: Référence de l'API Aspose.Words pour .NET
description: Table méthode. Convertit les cellules fusionnées horizontalement par largeur en cellules fusionnées parHorizontalMerge .
type: docs
weight: 390
url: /fr/net/aspose.words.tables/table/converttohorizontallymergedcells/
---
## Table.ConvertToHorizontallyMergedCells method

Convertit les cellules fusionnées horizontalement par largeur en cellules fusionnées par[`HorizontalMerge`](../../cellformat/horizontalmerge/) .

```csharp
public void ConvertToHorizontallyMergedCells()
```

### Remarques

Les cellules du tableau peuvent être fusionnées horizontalement soit en utilisant des indicateurs de fusion[`HorizontalMerge`](../../cellformat/horizontalmerge/) ou en utilisant la largeur de cellule[`Width`](../../cellformat/width/).

Lorsque la cellule du tableau est fusionnée par la propriété width[`HorizontalMerge`](../../cellformat/horizontalmerge/) n'a pas de sens, mais parfois, avoir des drapeaux de fusion est un moyen plus pratique.

Utilisez cette méthode pour transformer des cellules de tableau fusionnées horizontalement par largeur en cellules fusionnées par des indicateurs de fusion.

### Exemples

Montre comment convertir des cellules fusionnées horizontalement par largeur en cellules fusionnées par CellFormat.HorizontalMerge.

```csharp
Document doc = new Document(MyDir + "Table with merged cells.docx");

// Microsoft Word n'écrit plus les indicateurs de fusion, définissant les cellules fusionnées par largeur à la place.
// Aspose.Words par défaut ne définit que 5 cellules d'affilée, et aucune d'entre elles n'a le drapeau de fusion horizontale,
// même s'il y avait 7 cellules dans la ligne avant la fusion horizontale.
Table table = doc.FirstSection.Body.Tables[0];
Row row = table.Rows[0];

Assert.AreEqual(5, row.Cells.Count);
Assert.True(row.Cells.All(c => ((Cell)c).CellFormat.HorizontalMerge == CellMerge.None));

// Utilisez la méthode "ConvertToHorizontallyMergedCells" pour convertir les cellules fusionnées horizontalement
// par sa largeur à la cellule fusionnée horizontalement par des drapeaux.
// Maintenant, nous avons 7 cellules, et certaines d'entre elles ont des valeurs de fusion horizontales.
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
* espace de noms [Aspose.Words.Tables](../../table/)
* Assemblée [Aspose.Words](../../../)


