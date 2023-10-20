---
title: Row.Cells
linktitle: Cells
articleTitle: Cells
second_title: Aspose.Words pour .NET
description: Row Cells propriété. Fournit un accès typé auCell nœuds enfants de la ligne en C#.
type: docs
weight: 20
url: /fr/net/aspose.words.tables/row/cells/
---
## Row.Cells property

Fournit un accès typé au[`Cell`](../../cell/) nœuds enfants de la ligne.

```csharp
public CellCollection Cells { get; }
```

## Exemples

Montre comment parcourir tous les tableaux du document et imprimer le contenu de chaque cellule.

```csharp
Document doc = new Document(MyDir + "Tables.docx");
TableCollection tables = doc.FirstSection.Body.Tables;

Assert.AreEqual(2, tables.ToArray().Length);

for (int i = 0; i < tables.Count; i++)
{
    Console.WriteLine($"Start of Table {i}");

    RowCollection rows = tables[i].Rows;

    // On peut utiliser la méthode "ToArray" sur une collection de lignes pour la cloner dans un tableau.
    Assert.AreEqual(rows, rows.ToArray());
    Assert.AreNotSame(rows, rows.ToArray());

    for (int j = 0; j < rows.Count; j++)
    {
        Console.WriteLine($"\tStart of Row {j}");

        CellCollection cells = rows[j].Cells;

        // On peut utiliser la méthode "ToArray" sur une collection de cellules pour la cloner dans un tableau.
        Assert.AreEqual(cells, cells.ToArray());
        Assert.AreNotSame(cells, cells.ToArray());

        for (int k = 0; k < cells.Count; k++)
        {
            string cellText = cells[k].ToString(SaveFormat.Text).Trim();
            Console.WriteLine($"\t\tContents of Cell:{k} = \"{cellText}\"");
        }

        Console.WriteLine($"\tEnd of Row {j}");
    }

    Console.WriteLine($"End of Table {i}\n");
}
```

### Voir également

* class [CellCollection](../../cellcollection/)
* class [Row](../)
* espace de noms [Aspose.Words.Tables](../../../aspose.words.tables/)
* Assemblée [Aspose.Words](../../../)
