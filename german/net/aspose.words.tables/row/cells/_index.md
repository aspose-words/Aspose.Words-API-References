---
title: Row.Cells
linktitle: Cells
articleTitle: Cells
second_title: Aspose.Words für .NET
description: Greifen Sie mühelos mit typisierten Steuerelementen auf Zeilenzellen zu, um untergeordnete Knoten nahtlos zu verwalten und so Ihre Erfahrung bei der Datenmanipulation zu verbessern.
type: docs
weight: 20
url: /de/net/aspose.words.tables/row/cells/
---
## Row.Cells property

Bietet typisierten Zugriff auf die[`Cell`](../../cell/) untergeordnete Knoten der Zeile.

```csharp
public CellCollection Cells { get; }
```

## Beispiele

Zeigt, wie alle Tabellen im Dokument durchlaufen und der Inhalt jeder Zelle gedruckt wird.

```csharp
Document doc = new Document(MyDir + "Tables.docx");
TableCollection tables = doc.FirstSection.Body.Tables;

Assert.AreEqual(2, tables.ToArray().Length);

for (int i = 0; i < tables.Count; i++)
{
    Console.WriteLine($"Start of Table {i}");

    RowCollection rows = tables[i].Rows;

    // Wir können die Methode „ToArray“ auf eine Zeilensammlung anwenden, um sie in ein Array zu klonen.
    Assert.AreEqual(rows, rows.ToArray());
    Assert.AreNotSame(rows, rows.ToArray());

    for (int j = 0; j < rows.Count; j++)
    {
        Console.WriteLine($"\tStart of Row {j}");

        CellCollection cells = rows[j].Cells;

        // Wir können die Methode „ToArray“ auf eine Zellensammlung anwenden, um sie in ein Array zu klonen.
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

* class [CellCollection](../../cellcollection/)
* class [Row](../)
* namensraum [Aspose.Words.Tables](../../../aspose.words.tables/)
* Montage [Aspose.Words](../../../)
