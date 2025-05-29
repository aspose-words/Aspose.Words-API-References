---
title: RowCollection Class
linktitle: RowCollection
articleTitle: RowCollection
second_title: Aspose.Words pour .NET
description: Explorez Aspose.Words.Tables.RowCollection pour un accès efficace aux nœuds de lignes. Améliorez le traitement de vos documents grâce à nos puissantes fonctionnalités de collection typée.
type: docs
weight: 7170
url: /fr/net/aspose.words.tables/rowcollection/
---
## RowCollection class

Fournit un accès typé à une collection de[`Row`](../row/) nœuds.

Pour en savoir plus, visitez le[Travailler avec des tableaux](https://docs.aspose.com/words/net/working-with-tables/) article de documentation.

```csharp
public class RowCollection : NodeCollection
```

## Propriétés

| Nom | La description |
| --- | --- |
| [Count](../../aspose.words/nodecollection/count/) { get; } | Obtient le nombre de nœuds dans la collection. |
| [Item](../../aspose.words.tables/rowcollection/item/) { get; } | Récupère un[`Row`](../row/) à l'index donné. (2 indexers) |

## Méthodes

| Nom | La description |
| --- | --- |
| [Add](../../aspose.words/nodecollection/add/)(*[Node](../../aspose.words/node/)*) | Ajoute un nœud à la fin de la collection. |
| [Clear](../../aspose.words/nodecollection/clear/)() | Supprime tous les nœuds de cette collection et du document. |
| [Contains](../../aspose.words/nodecollection/contains/)(*[Node](../../aspose.words/node/)*) | Détermine si un nœud est dans la collection. |
| [GetEnumerator](../../aspose.words/nodecollection/getenumerator/)() | Fournit une itération simple de style « foreach » sur la collection de nœuds. |
| [IndexOf](../../aspose.words/nodecollection/indexof/)(*[Node](../../aspose.words/node/)*) | Renvoie l'index de base zéro du nœud spécifié. |
| [Insert](../../aspose.words/nodecollection/insert/)(*int, [Node](../../aspose.words/node/)*) | Insère un nœud dans la collection à l'index spécifié. |
| [Remove](../../aspose.words/nodecollection/remove/)(*[Node](../../aspose.words/node/)*) | Supprime le nœud de la collection et du document. |
| [RemoveAt](../../aspose.words/nodecollection/removeat/)(*int*) | Supprime le nœud à l'index spécifié de la collection et du document. |
| [ToArray](../../aspose.words.tables/rowcollection/toarray/#toarray_1)() | Copie toutes les lignes de la collection dans un nouveau tableau de lignes. (2 methods) |

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

* class [NodeCollection](../../aspose.words/nodecollection/)
* espace de noms [Aspose.Words.Tables](../../aspose.words.tables/)
* Assemblée [Aspose.Words](../../)
