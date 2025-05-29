---
title: PreferredWidth.Value
linktitle: Value
articleTitle: Value
second_title: .NET için Aspose.Words
description: Tercih ettiğiniz genişliğe kolayca erişmek ve özelleştirmek için PreferredWidth Değer özelliğini keşfedin. Tasarımınızı bugün hassas ölçümlerle geliştirin!
type: docs
weight: 50
url: /tr/net/aspose.words.tables/preferredwidth/value/
---
## PreferredWidth.Value property

Tercih edilen genişlik değerini alır. Ölçü birimi,[`Type`](../type/) mülk.

```csharp
public double Value { get; }
```

## Örnekler

Bir tablo hücresinin tercih edilen genişlik türünün ve değerinin nasıl doğrulanacağını gösterir.

```csharp
Document doc = new Document(MyDir + "Tables.docx");

Table table = doc.FirstSection.Body.Tables[0];
Cell firstCell = table.FirstRow.FirstCell;

Assert.AreEqual(PreferredWidthType.Percent, firstCell.CellFormat.PreferredWidth.Type);
Assert.AreEqual(11.16d, firstCell.CellFormat.PreferredWidth.Value);
```

### Ayrıca bakınız

* class [PreferredWidth](../)
* ad alanı [Aspose.Words.Tables](../../../aspose.words.tables/)
* toplantı [Aspose.Words](../../../)
