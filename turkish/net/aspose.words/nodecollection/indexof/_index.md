---
title: NodeCollection.IndexOf
linktitle: IndexOf
articleTitle: IndexOf
second_title: Aspose.Words for .NET
description: NodeCollection IndexOf yöntem. Belirtilen düğümün sıfır tabanlı dizinini döndürür C#'da.
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
| node | Node | Bulunacak düğüm. |

### Geri dönüş değeri

Bulunursa koleksiyon içindeki düğümün sıfır tabanlı dizini; aksi halde -1.

## Notlar

Bu yöntem doğrusal bir arama gerçekleştirir; bu nedenle, ortalama yürütme süresi orantılıdır[`Count`](../count/).

## Örnekler

Koleksiyondaki bir düğümün dizininin nasıl alınacağını gösterir.

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
