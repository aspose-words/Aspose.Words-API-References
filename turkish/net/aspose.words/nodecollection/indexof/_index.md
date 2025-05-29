---
title: NodeCollection.IndexOf
linktitle: IndexOf
articleTitle: IndexOf
second_title: .NET için Aspose.Words
description: Koleksiyonlarınızdaki belirtilen herhangi bir düğümün sıfır tabanlı dizinini verimli bir şekilde bulmak için NodeCollection IndexOf yöntemini keşfedin.
type: docs
weight: 70
url: /tr/net/aspose.words/nodecollection/indexof/
---
## NodeCollection.IndexOf method

Belirtilen düğümün sıfır tabanlı dizinini döndürür.

```csharp
public int IndexOf(Node node)
```

| Parametre | Tip | Tanım |
| --- | --- | --- |
| node | Node | Bulunması gereken düğüm. |

### Geri dönüş değeri

Koleksiyondaki düğümün sıfır tabanlı indeksi, bulunursa; aksi takdirde -1.

## Notlar

Bu yöntem doğrusal bir arama gerçekleştirir; bu nedenle, ortalama yürütme süresi şuna orantılıdır:[`Count`](../count/).

## Örnekler

Bir koleksiyondaki düğümün dizininin nasıl alınacağını gösterir.

```csharp
Document doc = new Document(MyDir + "Tables.docx");

Table table = doc.FirstSection.Body.Tables[0];
NodeCollection allTables = doc.GetChildNodes(NodeType.Table, true);

Assert.AreEqual(0, allTables.IndexOf(table));

Row row = table.Rows[2];

Assert.AreEqual(2, table.IndexOf(row));

Cell cell = row.LastCell;

Assert.AreEqual(4, row.IndexOf(cell));
```

### Ayrıca bakınız

* class [Node](../../node/)
* class [NodeCollection](../)
* ad alanı [Aspose.Words](../../../aspose.words/)
* toplantı [Aspose.Words](../../../)
