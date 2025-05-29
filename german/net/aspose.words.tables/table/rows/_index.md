---
title: Table.Rows
linktitle: Rows
articleTitle: Rows
second_title: Aspose.Words für .NET
description: Greifen Sie mit unserer typisierten Eigenschaft mühelos auf Tabellenzeilen zu und gewährleisten Sie so eine nahtlose Datenverwaltung und verbesserte Organisation Ihrer Projekte.
type: docs
weight: 260
url: /de/net/aspose.words.tables/table/rows/
---
## Table.Rows property

Bietet typisierten Zugriff auf die Zeilen der Tabelle.

```csharp
public RowCollection Rows { get; }
```

## Beispiele

Zeigt, wie die Zeilen aus zwei Tabellen zu einer kombiniert werden.

```csharp
Document doc = new Document(MyDir + "Tables.docx");

// Unten sind zwei Möglichkeiten, eine Tabelle aus einem Dokument zu erhalten.
// 1 – Aus der „Tabellen“-Sammlung eines Body-Knotens:
Table firstTable = doc.FirstSection.Body.Tables[0];

// 2 - Verwenden der Methode „GetChild“:
Table secondTable = (Table)doc.GetChild(NodeType.Table, 1, true);

// Alle Zeilen der aktuellen Tabelle an die nächste anhängen.
while (secondTable.HasChildNodes)
    firstTable.Rows.Add(secondTable.FirstRow);

// Entfernen Sie den leeren Tabellencontainer.
secondTable.Remove();

doc.Save(ArtifactsDir + "Table.CombineTables.docx");
```

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

* class [RowCollection](../../rowcollection/)
* class [Table](../)
* namensraum [Aspose.Words.Tables](../../../aspose.words.tables/)
* Montage [Aspose.Words](../../../)
