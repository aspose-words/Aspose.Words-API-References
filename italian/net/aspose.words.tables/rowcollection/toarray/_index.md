---
title: RowCollection.ToArray
linktitle: ToArray
articleTitle: ToArray
second_title: Aspose.Words per .NET
description: Converti senza sforzo la tua RowCollection in un nuovo array con il metodo ToArray, assicurando una gestione dei dati impeccabile e prestazioni migliorate.
type: docs
weight: 20
url: /it/net/aspose.words.tables/rowcollection/toarray/
---
## RowCollection.ToArray method

Copia tutte le righe dalla raccolta in un nuovo array di righe.

```csharp
public Row[] ToArray()
```

### Valore di ritorno

Una serie di righe.

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

* class [Row](../../row/)
* class [RowCollection](../)
* spazio dei nomi [Aspose.Words.Tables](../../../aspose.words.tables/)
* assemblea [Aspose.Words](../../../)
