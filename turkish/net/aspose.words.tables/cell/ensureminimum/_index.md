---
title: Cell.EnsureMinimum
linktitle: EnsureMinimum
articleTitle: EnsureMinimum
second_title: Aspose.Words for .NET
description: Cell EnsureMinimum yöntem. Son alt öğe bir paragraf değilse boş bir paragraf oluşturur ve ekler C#'da.
type: docs
weight: 140
url: /tr/net/aspose.words.tables/cell/ensureminimum/
---
## Cell.EnsureMinimum method

Son alt öğe bir paragraf değilse, boş bir paragraf oluşturur ve ekler.

```csharp
public void EnsureMinimum()
```

## Örnekler

Bir hücre düğümünün, ona içerik eklemeye başlamak için ihtiyacımız olan düğümleri içerdiğinden nasıl emin olacağımızı gösterir.

```csharp
Document doc = new Document();
Table table = new Table(doc);
doc.FirstSection.Body.AppendChild(table);
Row row = new Row(doc);
table.AppendChild(row);
Cell cell = new Cell(doc);
row.AppendChild(cell);

// Hücreler, diziler, şekiller ve hatta diğer tablolar gibi tipik öğelerin bulunduğu paragraflar içerebilir.
// Yeni hücremizde paragraf bulunmamaktadır ve bu hücre bulununcaya kadar ona düğüm çalıştırma, şekil verme gibi içerikler ekleyemiyoruz.
Assert.AreEqual(0, cell.GetChildNodes(NodeType.Any, true).Count);

// Bir hücrede "EnsureMinimum" yöntemini çağırmak şunları sağlayacaktır:
// hücrede daha sonra içerik ekleyebileceğimiz en az bir boş paragraf var.
cell.EnsureMinimum();
cell.FirstParagraph.AppendChild(new Run(doc, "Hello world!"));
```

### Ayrıca bakınız

* class [Cell](../)
* ad alanı [Aspose.Words.Tables](../../../aspose.words.tables/)
* toplantı [Aspose.Words](../../../)
