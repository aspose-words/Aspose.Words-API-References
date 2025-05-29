---
title: Cell.EnsureMinimum
linktitle: EnsureMinimum
articleTitle: EnsureMinimum
second_title: .NET için Aspose.Words
description: EnsureMinimum yöntemi ile hücre yapınızı optimize edin, son çocuk paragraf değilse bile zahmetsizce bir paragraf ekleyin. Belgenizin netliğini artırın!
type: docs
weight: 160
url: /tr/net/aspose.words.tables/cell/ensureminimum/
---
## Cell.EnsureMinimum method

Son çocuk bir paragraf değilse, boş bir paragraf oluşturur ve ekler.

```csharp
public void EnsureMinimum()
```

## Örnekler

Bir hücre düğümünün, ona içerik eklemeye başlamak için ihtiyaç duyduğumuz düğümleri içerdiğinden nasıl emin olacağımızı gösterir.

```csharp
Document doc = new Document();
Table table = new Table(doc);
doc.FirstSection.Body.AppendChild(table);
Row row = new Row(doc);
table.AppendChild(row);
Cell cell = new Cell(doc);
row.AppendChild(cell);

// Hücreler, koşular, şekiller ve hatta diğer tablolar gibi tipik öğeler içeren paragraflar içerebilir.
// Yeni hücremizde herhangi bir paragraf yok ve bu olana kadar çalıştırma ve şekil düğümleri gibi içerikleri ekleyemeyiz.
Assert.AreEqual(0, cell.GetChildNodes(NodeType.Any, true).Count);

// Bir hücrede "EnsureMinimum" metodunu çağırmak,
// hücrede en az bir boş paragraf var, bu paragrafa içerik ekleyebiliriz.
cell.EnsureMinimum();
cell.FirstParagraph.AppendChild(new Run(doc, "Hello world!"));
```

### Ayrıca bakınız

* class [Cell](../)
* ad alanı [Aspose.Words.Tables](../../../aspose.words.tables/)
* toplantı [Aspose.Words](../../../)
