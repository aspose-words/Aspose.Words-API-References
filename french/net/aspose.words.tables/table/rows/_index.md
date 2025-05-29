---
title: Table.Rows
linktitle: Rows
articleTitle: Rows
second_title: Aspose.Words pour .NET
description: Accédez aux lignes du tableau sans effort avec notre propriété typée, garantissant une gestion transparente des données et une organisation améliorée pour vos projets.
type: docs
weight: 260
url: /fr/net/aspose.words.tables/table/rows/
---
## Table.Rows property

Fournit un accès typé aux lignes de la table.

```csharp
public RowCollection Rows { get; }
```

## Exemples

Montre comment combiner les lignes de deux tables en une seule.

```csharp
Document doc = new Document(MyDir + "Tables.docx");

// Vous trouverez ci-dessous deux manières d’obtenir un tableau à partir d’un document.
// 1 - À partir de la collection « Tables » d'un nœud Body :
Table firstTable = doc.FirstSection.Body.Tables[0];

// 2 - Utilisation de la méthode « GetChild » :
Table secondTable = (Table)doc.GetChild(NodeType.Table, 1, true);

// Ajouter toutes les lignes de la table actuelle à la suivante.
while (secondTable.HasChildNodes)
    firstTable.Rows.Add(secondTable.FirstRow);

// Supprimez le conteneur de table vide.
secondTable.Remove();

doc.Save(ArtifactsDir + "Table.CombineTables.docx");
```

Montre comment parcourir tous les tableaux du document et imprimer le contenu de chaque cellule.

```csharp
Document doc = new Document(MyDir + "Tables.docx");
TableCollection tables = doc.FirstSection.Body.Tables;

Assert.AreEqual(2, tables.ToArray().Length);

for (int i = 0; i < tables.Count; i++)
{
    Console.WriteLine($"Start of Table {i}");

    RowCollection rows = tables[i].Rows;

    // Nous pouvons utiliser la méthode « ToArray » sur une collection de lignes pour la cloner dans un tableau.
    Assert.AreEqual(rows, rows.ToArray());
    Assert.AreNotSame(rows, rows.ToArray());

    for (int j = 0; j < rows.Count; j++)
    {
        Console.WriteLine($"\tStart of Row {j}");

        CellCollection cells = rows[j].Cells;

        // Nous pouvons utiliser la méthode « ToArray » sur une collection de cellules pour la cloner dans un tableau.
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

* class [RowCollection](../../rowcollection/)
* class [Table](../)
* espace de noms [Aspose.Words.Tables](../../../aspose.words.tables/)
* Assemblée [Aspose.Words](../../../)
