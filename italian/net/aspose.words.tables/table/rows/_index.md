---
title: Table.Rows
second_title: Aspose.Words per .NET API Reference
description: Table proprietà. Fornisce laccesso digitato alle righe della tabella.
type: docs
weight: 260
url: /it/net/aspose.words.tables/table/rows/
---
## Table.Rows property

Fornisce l'accesso digitato alle righe della tabella.

```csharp
public RowCollection Rows { get; }
```

### Esempi

Mostra come combinare le righe di due tabelle in una.

```csharp
Document doc = new Document(MyDir + "Tables.docx");

// Di seguito sono riportati due modi per ottenere una tabella da un documento.
// 1 - Dalla raccolta "Tables" di un nodo Body:
Table firstTable = doc.FirstSection.Body.Tables[0];

// 2 - Utilizzando il metodo "GetChild":
Table secondTable = (Table)doc.GetChild(NodeType.Table, 1, true);

// Aggiunge tutte le righe della tabella corrente a quella successiva.
while (secondTable.HasChildNodes)
    firstTable.Rows.Add(secondTable.FirstRow);

// Rimuove il contenitore della tabella vuota.
secondTable.Remove();

doc.Save(ArtifactsDir + "Table.CombineTables.docx");
```

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

* class [RowCollection](../../rowcollection/)
* class [Table](../)
* spazio dei nomi [Aspose.Words.Tables](../../table/)
* assemblea [Aspose.Words](../../../)


