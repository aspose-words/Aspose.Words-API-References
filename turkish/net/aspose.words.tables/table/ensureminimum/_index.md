---
title: Table.EnsureMinimum
linktitle: EnsureMinimum
articleTitle: EnsureMinimum
second_title: .NET için Aspose.Words
description: Table EnsureMinimum yöntemini keşfedin, tablonuz boşken zahmetsizce bir satır oluşturun ve ekleyin; böylece sorunsuz veri yönetimi sağlayın.
type: docs
weight: 420
url: /tr/net/aspose.words.tables/table/ensureminimum/
---
## Table.EnsureMinimum method

Tabloda satır yoksa bir tane oluşturur ve ekler[`Row`](../../row/) .

```csharp
public void EnsureMinimum()
```

## Örnekler

Bir tablo düğümünün içerik eklememiz gereken düğümleri içerdiğinden nasıl emin olacağımızı gösterir.

```csharp
Document doc = new Document();
Table table = new Table(doc);
doc.FirstSection.Body.AppendChild(table);

// Tablolar, hücreler içeren satırlar ve hücreler de paragraflar içerebilir
// tipik elemanlar olan koşular, şekiller ve hatta diğer tablolar ile.
// Yeni tablomuzda bu düğümlerin hiçbiri yok ve bu düğümler oluşana kadar tabloya içerik ekleyemeyiz.
Assert.AreEqual(0, table.GetChildNodes(NodeType.Any, true).Count);

// Bir tabloda "EnsureMinimum" metodunu çağırmak,
// tabloda en az bir satır ve boş paragraf içeren bir hücre var.
table.EnsureMinimum();
table.FirstRow.FirstCell.FirstParagraph.AppendChild(new Run(doc, "Hello world!"));
```

### Ayrıca bakınız

* class [Table](../)
* ad alanı [Aspose.Words.Tables](../../../aspose.words.tables/)
* toplantı [Aspose.Words](../../../)
