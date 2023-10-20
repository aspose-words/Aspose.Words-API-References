---
title: Cell.PreviousCell
linktitle: PreviousCell
articleTitle: PreviousCell
second_title: Aspose.Words pour .NET
description: Cell PreviousCell propriété. Récupère le précédentCell nœud en C#.
type: docs
weight: 110
url: /fr/net/aspose.words.tables/cell/previouscell/
---
## Cell.PreviousCell property

Récupère le précédent[`Cell`](../) nœud.

```csharp
public Cell PreviousCell { get; }
```

## Remarques

La méthode peut être utilisée lorsque vous avez besoin d'un accès typé aux cellules d'un[`Row`](../../row/) . Si a [`StructuredDocumentTag`](../../../aspose.words.markup/structureddocumenttag/) Le nœud se trouve dans une ligne au lieu d'une cellule, il est automatiquement parcouru pour obtenir une cellule contenue à l'intérieur.

## Exemples

Montre comment énumérer toutes les cellules du tableau.

```csharp
Document doc = new Document(MyDir + "Tables.docx");
Table table = doc.FirstSection.Body.Tables[0];

// Énumère toutes les cellules du tableau.
for (Row row = table.FirstRow; row != null; row = row.NextRow)
{
    for (Cell cell = row.FirstCell; cell != null; cell = cell.NextCell)
    {
        Console.WriteLine(cell.GetText());
    }
}
```

### Voir également

* class [Cell](../)
* espace de noms [Aspose.Words.Tables](../../../aspose.words.tables/)
* Assemblée [Aspose.Words](../../../)
