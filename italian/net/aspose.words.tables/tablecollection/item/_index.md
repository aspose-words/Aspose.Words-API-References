---
title: TableCollection.Item
second_title: Aspose.Words per .NET API Reference
description: TableCollection proprietà. Recupera aTable allindice indicato.
type: docs
weight: 10
url: /it/net/aspose.words.tables/tablecollection/item/
---
## TableCollection indexer

Recupera a[`Table`](../../table/) all'indice indicato.

```csharp
public Table this[int index] { get; }
```

| Parametro | Descrizione |
| --- | --- |
| index | Un indice nella raccolta. |

### Osservazioni

L'indice è a base zero.

Gli indici negativi sono consentiti e indicano l'accesso dal retro della raccolta. Ad esempio -1 significa l'ultimo elemento, -2 significa il penultimo e così via.

Se indice è maggiore o uguale al numero di elementi nell'elenco, restituisce un riferimento null.

Se indice è negativo e il suo valore assoluto è maggiore del numero di elementi nell'elenco, restituisce un riferimento null.

### Esempi

Mostra come scorrere tutte le tabelle del documento e stampare il contenuto di ciascuna cella.

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

        // Possiamo utilizzare il metodo "ToArray" su una raccolta di celle per clonarla in un array.
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

* class [Table](../../table/)
* class [TableCollection](../)
* spazio dei nomi [Aspose.Words.Tables](../../tablecollection/)
* assemblea [Aspose.Words](../../../)


