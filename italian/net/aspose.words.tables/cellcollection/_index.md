---
title: CellCollection Class
linktitle: CellCollection
articleTitle: CellCollection
second_title: Aspose.Words per .NET
description: Scopri la classe Aspose.Words.Tables.CellCollection per un accesso semplice e tipizzato ai nodi Cell, migliorando l'efficienza e la manipolazione dei documenti.
type: docs
weight: 7100
url: /it/net/aspose.words.tables/cellcollection/
---
## CellCollection class

Fornisce accesso tipizzato a una raccolta di[`Cell`](../cell/) nodi.

Per saperne di più, visita il[Lavorare con le tabelle](https://docs.aspose.com/words/net/working-with-tables/) articolo di documentazione.

```csharp
public class CellCollection : NodeCollection
```

## Proprietà

| Nome | Descrizione |
| --- | --- |
| [Count](../../aspose.words/nodecollection/count/) { get; } | Ottiene il numero di nodi nella raccolta. |
| [Item](../../aspose.words.tables/cellcollection/item/) { get; } | Recupera un[`Cell`](../cell/) all'indice dato. (2 indexers) |

## Metodi

| Nome | Descrizione |
| --- | --- |
| [Add](../../aspose.words/nodecollection/add/)(*[Node](../../aspose.words/node/)*) | Aggiunge un nodo alla fine della raccolta. |
| [Clear](../../aspose.words/nodecollection/clear/)() | Rimuove tutti i nodi da questa raccolta e dal documento. |
| [Contains](../../aspose.words/nodecollection/contains/)(*[Node](../../aspose.words/node/)*) | Determina se un nodo è nella raccolta. |
| [GetEnumerator](../../aspose.words/nodecollection/getenumerator/)() | Fornisce una semplice iterazione in stile "foreach" sulla raccolta di nodi. |
| [IndexOf](../../aspose.words/nodecollection/indexof/)(*[Node](../../aspose.words/node/)*) | Restituisce l'indice basato su zero del nodo specificato. |
| [Insert](../../aspose.words/nodecollection/insert/)(*int, [Node](../../aspose.words/node/)*) | Inserisce un nodo nella raccolta all'indice specificato. |
| [Remove](../../aspose.words/nodecollection/remove/)(*[Node](../../aspose.words/node/)*) | Rimuove il nodo dalla raccolta e dal documento. |
| [RemoveAt](../../aspose.words/nodecollection/removeat/)(*int*) | Rimuove il nodo all'indice specificato dalla raccolta e dal documento. |
| [ToArray](../../aspose.words.tables/cellcollection/toarray/#toarray_1)() | Copia tutte le celle dalla raccolta in un nuovo array di celle. (2 methods) |

## Esempi

Mostra come scorrere tutte le tabelle del documento e stampare il contenuto di ogni cella.

```csharp
Document doc = new Document(MyDir + "Tables.docx");
TableCollection tables = doc.FirstSection.Body.Tables;

Assert.AreEqual(2, tables.ToArray().Length);

for (int i = 0; i < tables.Count; i++)
{
    Console.WriteLine($"Start of Table {i}");

    RowCollection rows = tables[i].Rows;

    // Possiamo usare il metodo "ToArray" su una raccolta di righe per clonarla in un array.
    Assert.AreEqual(rows, rows.ToArray());
    Assert.AreNotSame(rows, rows.ToArray());

    for (int j = 0; j < rows.Count; j++)
    {
        Console.WriteLine($"\tStart of Row {j}");

        CellCollection cells = rows[j].Cells;

        // Possiamo usare il metodo "ToArray" su una raccolta di celle per clonarla in un array.
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

### Guarda anche

* class [NodeCollection](../../aspose.words/nodecollection/)
* spazio dei nomi [Aspose.Words.Tables](../../aspose.words.tables/)
* assemblea [Aspose.Words](../../)
