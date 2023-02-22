---
title: Row.EnsureMinimum
second_title: Aspose.Words for .NET API Referansı
description: Row yöntem. Sıra hücre yok bir tane oluşturur ve ekler Hücre .
type: docs
weight: 110
url: /tr/net/aspose.words.tables/row/ensureminimum/
---
## Row.EnsureMinimum method

**Sıra** hücre yok, bir tane oluşturur ve ekler **Hücre** .

```csharp
public void EnsureMinimum()
```

### Örnekler

Bir satır düğümünün, ona içerik eklemeye başlamak için ihtiyaç duyduğumuz düğümleri içerdiğinden nasıl emin olunacağını gösterir.

```csharp
Document doc = new Document();
Table table = new Table(doc);
doc.FirstSection.Body.AppendChild(table);
Row row = new Row(doc);
table.AppendChild(row);

// Satırlar, koşular, şekiller ve hatta diğer tablolar gibi tipik öğeler içeren paragraflar içeren hücreler içerir.
// Yeni satırımızda bu düğümlerin hiçbiri yok ve o gelene kadar ona içerik ekleyemeyiz.
Assert.AreEqual(0, row.GetChildNodes(NodeType.Any, true).Count);

// Bir tabloda "EnsureMinimum" yöntemini çağırmak,
// tabloda boş bir paragraf içeren en az bir hücre var.
row.EnsureMinimum();
row.FirstCell.FirstParagraph.AppendChild(new Run(doc, "Hello world!"));
```

### Ayrıca bakınız

* class [Row](../)
* ad alanı [Aspose.Words.Tables](../../row/)
* toplantı [Aspose.Words](../../../)


