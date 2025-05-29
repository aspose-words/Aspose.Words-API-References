---
title: Row.EnsureMinimum
linktitle: EnsureMinimum
articleTitle: EnsureMinimum
second_title: .NET için Aspose.Words
description: Row EnsureMinimum metodunu keşfedin, mevcut olmayan bir Hücreyi zahmetsizce oluşturun ve ekleyin, böylece veri yapınızın yönetimini geliştirin.
type: docs
weight: 150
url: /tr/net/aspose.words.tables/row/ensureminimum/
---
## Row.EnsureMinimum method

Eğer[`Row`](../) hücre yok, bir hücre oluşturur ve ekler[`Cell`](../../cell/) .

```csharp
public void EnsureMinimum()
```

## Örnekler

Bir satır düğümünün, ona içerik eklemeye başlamak için ihtiyaç duyduğumuz düğümleri içerdiğinden nasıl emin olacağımızı gösterir.

```csharp
Document doc = new Document();
Table table = new Table(doc);
doc.FirstSection.Body.AppendChild(table);
Row row = new Row(doc);
table.AppendChild(row);

// Satırlar, tipik öğeler (örneğin koşular, şekiller ve hatta diğer tablolar) içeren paragraflar içeren hücreler içerir.
// Yeni satırımızda bu düğümlerin hiçbiri yok ve bu düğümler oluşana kadar satıra içerik ekleyemeyiz.
Assert.AreEqual(0, row.GetChildNodes(NodeType.Any, true).Count);

// Bir tabloda "EnsureMinimum" metodunu çağırmak,
// tabloda en az bir boş paragraf içeren hücre var.
row.EnsureMinimum();
row.FirstCell.FirstParagraph.AppendChild(new Run(doc, "Hello world!"));
```

### Ayrıca bakınız

* class [Row](../)
* ad alanı [Aspose.Words.Tables](../../../aspose.words.tables/)
* toplantı [Aspose.Words](../../../)
