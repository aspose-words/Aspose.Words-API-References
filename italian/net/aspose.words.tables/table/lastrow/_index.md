---
title: Table.LastRow
linktitle: LastRow
articleTitle: LastRow
second_title: Aspose.Words per .NET
description: Table LastRow proprietà. Restituisce lultimoRow nodo nella tabella in C#.
type: docs
weight: 180
url: /it/net/aspose.words.tables/table/lastrow/
---
## Table.LastRow property

Restituisce l'ultimo[`Row`](../../row/) nodo nella tabella.

```csharp
public Row LastRow { get; }
```

## Esempi

Mostra come rimuovere la prima e l'ultima riga di tutte le tabelle in un documento.

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

### Guarda anche

* class [Row](../../row/)
* class [Table](../)
* spazio dei nomi [Aspose.Words.Tables](../../../aspose.words.tables/)
* assemblea [Aspose.Words](../../../)
