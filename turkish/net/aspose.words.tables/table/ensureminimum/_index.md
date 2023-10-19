---
title: Table.EnsureMinimum
linktitle: EnsureMinimum
articleTitle: EnsureMinimum
second_title: Aspose.Words for .NET
description: Table EnsureMinimum yöntem. Tabloda hiç satır yoksa bir tane oluşturur ve eklerRow  C#'da.
type: docs
weight: 400
url: /tr/net/aspose.words.tables/table/ensureminimum/
---
## Table.EnsureMinimum method

Tabloda hiç satır yoksa bir tane oluşturur ve ekler[`Row`](../../row/) .

```csharp
public void EnsureMinimum()
```

## Örnekler

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
* ad alanı [Aspose.Words.Tables](../../../aspose.words.tables/)
* toplantı [Aspose.Words](../../../)
