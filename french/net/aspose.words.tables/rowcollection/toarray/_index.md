---
title: RowCollection.ToArray
linktitle: ToArray
articleTitle: ToArray
second_title: Aspose.Words pour .NET
description: RowCollection ToArray méthode. Copie toutes les lignes de la collection vers un nouveau tableau de lignes en C#.
type: docs
weight: 20
url: /fr/net/aspose.words.tables/rowcollection/toarray/
---
## RowCollection.ToArray method

Copie toutes les lignes de la collection vers un nouveau tableau de lignes.

```csharp
public Row[] ToArray()
```

### Return_Value

Un tableau de lignes.

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

* class [Row](../../row/)
* class [RowCollection](../)
* espace de noms [Aspose.Words.Tables](../../../aspose.words.tables/)
* Assemblée [Aspose.Words](../../../)
