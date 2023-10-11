---
title: Table.EnsureMinimum
second_title: Aspose.Words for .NET API Referansı
description: Table yöntem. Tabloda hiç satır yoksa bir tane oluşturur ve eklerRow .
type: docs
weight: 420
url: /tr/net/aspose.words.tables/table/ensureminimum/
---
## Table.EnsureMinimum method

Tabloda hiç satır yoksa bir tane oluşturur ve ekler[`Row`](../../row/) .

```csharp
public void EnsureMinimum()
```

### Örnekler

Bir tablo düğümünün içerik eklemek için ihtiyaç duyduğumuz düğümleri içerdiğinden nasıl emin olacağımızı gösterir.

```csharp
Document doc = new Document();
Table table = new Table(doc);
doc.FirstSection.Body.AppendChild(table);

// Tablolar, paragraf içerebilen hücreleri içeren satırları içerir
// diziler, şekiller ve hatta diğer tablolar gibi tipik öğelerle.
// Yeni tablomuzda bu düğümlerin hiçbiri yok ve bu düğümler bulunana kadar ona içerik ekleyemeyiz.
Assert.AreEqual(0, table.GetChildNodes(NodeType.Any, true).Count);

// Bir tabloda "EnsureMinimum" yöntemini çağırmak şunları sağlayacaktır:
// tabloda en az bir satır ve boş paragraf içeren bir hücre var.
table.EnsureMinimum();
table.FirstRow.FirstCell.FirstParagraph.AppendChild(new Run(doc, "Hello world!"));
```

### Ayrıca bakınız

* class [Table](../)
* ad alanı [Aspose.Words.Tables](../../table/)
* toplantı [Aspose.Words](../../../)


