---
title: Table.LastRow
linktitle: LastRow
articleTitle: LastRow
second_title: Aspose.Words für .NET
description: Entdecken Sie die Eigenschaft „Table LastRow“, um einfach auf den letzten Zeilenknoten in Ihrer Tabelle zuzugreifen und so die Datenverwaltung und Effizienz zu verbessern.
type: docs
weight: 180
url: /de/net/aspose.words.tables/table/lastrow/
---
## Table.LastRow property

Gibt die letzte[`Row`](../../row/) Knoten in der Tabelle.

```csharp
public Row LastRow { get; }
```

## Beispiele

Zeigt, wie die erste und die letzte Zeile aller Tabellen in einem Dokument entfernt werden.

```csharp
Document doc = new Document(MyDir + "Tables.docx");

TableCollection tables = doc.FirstSection.Body.Tables;

Assert.AreEqual(5, tables[0].Rows.Count);
Assert.AreEqual(4, tables[1].Rows.Count);

foreach (Table table in tables.OfType<Table>())
{
    table.FirstRow?.Remove();
    table.LastRow?.Remove();
}

Assert.AreEqual(3, tables[0].Rows.Count);
Assert.AreEqual(2, tables[1].Rows.Count);
```

### Siehe auch

* class [Row](../../row/)
* class [Table](../)
* namensraum [Aspose.Words.Tables](../../../aspose.words.tables/)
* Montage [Aspose.Words](../../../)
