---
title: Cell.NextCell
linktitle: NextCell
articleTitle: NextCell
second_title: Aspose.Words pour .NET
description: Découvrez la propriété NextCell pour accéder facilement au nœud Cell suivant, améliorant ainsi votre gestion des données et rationalisant votre flux de travail.
type: docs
weight: 70
url: /fr/net/aspose.words.tables/cell/nextcell/
---
## Cell.NextCell property

Obtient le suivant[`Cell`](../) nœud.

```csharp
public Cell NextCell { get; }
```

## Remarques

La méthode peut être utilisée lorsque vous avez besoin d'un accès typé aux cellules d'un[`Row`](../../row/) . Si a [`StructuredDocumentTag`](../../../aspose.words.markup/structureddocumenttag/) le nœud est trouvé dans une ligne au lieu d'une cellule, il est automatiquement parcouru pour obtenir une cellule contenue à l'intérieur.

## Exemples

Montre comment énumérer toutes les cellules du tableau.

```csharp
Document doc = new Document(MyDir + "Tables.docx");
Table table = doc.FirstSection.Body.Tables[0];

// Énumérer toutes les cellules du tableau.
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
