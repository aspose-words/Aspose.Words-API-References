---
title: Row.EnsureMinimum
second_title: Aspose.Words for .NET API Referansı
description: Row yöntem. EğerRow hiç hücresi yoktur bir tane oluşturur ve eklerCell .
type: docs
weight: 150
url: /tr/net/aspose.words.tables/row/ensureminimum/
---
## Row.EnsureMinimum method

Eğer[`Row`](../) hiç hücresi yoktur, bir tane oluşturur ve ekler[`Cell`](../../cell/) .

```csharp
public void EnsureMinimum()
```

### Örnekler

Bir satır düğümünün, ona içerik eklemeye başlamamız için gereken düğümleri içerdiğinden nasıl emin olacağımızı gösterir.

```csharp
Document doc = new Document();
Table table = new Table(doc);
doc.FirstSection.Body.AppendChild(table);
Row row = new Row(doc);
table.AppendChild(row);

// Satırlar, diziler, şekiller ve hatta diğer tablolar gibi tipik öğelerin bulunduğu paragrafları içeren hücreleri içerir.
// Yeni satırımızda bu düğümlerden hiçbiri yok ve bu düğümler bulunana kadar ona içerik ekleyemeyiz.
Assert.AreEqual(0, row.GetChildNodes(NodeType.Any, true).Count);

// Bir tabloda "EnsureMinimum" yöntemini çağırmak şunları sağlayacaktır:
// tabloda boş paragraf içeren en az bir hücre var.
row.EnsureMinimum();
row.FirstCell.FirstParagraph.AppendChild(new Run(doc, "Hello world!"));
```

### Ayrıca bakınız

* class [Row](../)
* ad alanı [Aspose.Words.Tables](../../row/)
* toplantı [Aspose.Words](../../../)


