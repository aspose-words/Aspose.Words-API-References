---
title: RowCollection.ToArray
second_title: Aspose.Words für .NET-API-Referenz
description: RowCollection methode. Kopiert alle Zeilen aus der Sammlung in ein neues Array von Zeilen.
type: docs
weight: 20
url: /de/net/aspose.words.tables/rowcollection/toarray/
---
## RowCollection.ToArray method

Kopiert alle Zeilen aus der Sammlung in ein neues Array von Zeilen.

```csharp
public Row[] ToArray()
```

### Rückgabewert

Ein Array von Zeilen.

### Beispiele

Zeigt, wie alle Tabellen im Dokument durchlaufen und der Inhalt jeder Zelle gedruckt wird.

```csharp
Document doc = new Document(MyDir + "Tables.docx");
TableCollection tables = doc.FirstSection.Body.Tables;

Assert.AreEqual(2, tables.ToArray().Length);

for (int i = 0; i < tables.Count; i++)
{
    Console.WriteLine($"Start of Table {i}");

    RowCollection rows = tables[i].Rows;

    // Wir können die "ToArray"-Methode für eine Zeilensammlung verwenden, um sie in ein Array zu klonen.
    Assert.AreEqual(rows, rows.ToArray());
    Assert.AreNotSame(rows, rows.ToArray());

    for (int j = 0; j < rows.Count; j++)
    {
        Console.WriteLine($"\tStart of Row {j}");

        CellCollection cells = rows[j].Cells;

        // Wir können die "ToArray"-Methode für eine Zellsammlung verwenden, um sie in ein Array zu klonen.
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

### Siehe auch

* class [Row](../../row/)
* class [RowCollection](../)
* namensraum [Aspose.Words.Tables](../../rowcollection/)
* Montage [Aspose.Words](../../../)


