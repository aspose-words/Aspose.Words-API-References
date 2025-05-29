---
title: Table.LastRow
linktitle: LastRow
articleTitle: LastRow
second_title: .NET için Aspose.Words
description: Tablonuzdaki son Satır düğümüne kolayca erişmek, veri yönetimini ve verimliliği artırmak için Table LastRow özelliğini keşfedin.
type: docs
weight: 180
url: /tr/net/aspose.words.tables/table/lastrow/
---
## Table.LastRow property

Sonuncuyu döndürür[`Row`](../../row/) tablodaki düğüm.

```csharp
public Row LastRow { get; }
```

## Örnekler

Bir belgedeki tüm tabloların ilk ve son satırlarının nasıl kaldırılacağını gösterir.

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

### Ayrıca bakınız

* class [Row](../../row/)
* class [Table](../)
* ad alanı [Aspose.Words.Tables](../../../aspose.words.tables/)
* toplantı [Aspose.Words](../../../)
