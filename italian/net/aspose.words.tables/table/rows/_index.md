---
title: Table.Rows
linktitle: Rows
articleTitle: Rows
second_title: Aspose.Words per .NET
description: Accedi senza sforzo alle righe della tabella con la nostra proprietà tipizzata, assicurando una gestione dei dati fluida e un'organizzazione migliorata per i tuoi progetti.
type: docs
weight: 260
url: /it/net/aspose.words.tables/table/rows/
---
## Table.Rows property

Fornisce accesso tipizzato alle righe della tabella.

```csharp
public RowCollection Rows { get; }
```

## Esempi

Mostra come combinare le righe di due tabelle in una.

```csharp
Document doc = new Document(MyDir + "Tables.docx");

// Di seguito sono riportati due modi per ottenere una tabella da un documento.
// 1 - Dalla raccolta "Tabelle" di un nodo Corpo:
Table firstTable = doc.FirstSection.Body.Tables[0];

// 2 - Utilizzo del metodo "GetChild":
Table secondTable = (Table)doc.GetChild(NodeType.Table, 1, true);

// Aggiunge tutte le righe dalla tabella corrente a quella successiva.
while (secondTable.HasChildNodes)
    firstTable.Rows.Add(secondTable.FirstRow);

// Rimuove il contenitore della tabella vuota.
secondTable.Remove();

doc.Save(ArtifactsDir + "Table.CombineTables.docx");
```

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

* class [RowCollection](../../rowcollection/)
* class [Table](../)
* spazio dei nomi [Aspose.Words.Tables](../../../aspose.words.tables/)
* assemblea [Aspose.Words](../../../)
