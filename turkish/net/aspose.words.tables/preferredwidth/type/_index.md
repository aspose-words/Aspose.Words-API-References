---
title: PreferredWidth.Type
linktitle: Type
articleTitle: Type
second_title: .NET için Aspose.Words
description: Tasarımınızın hassasiyetini ve esnekliğini artıran, tercih edilen genişlik değerleri için ölçüm birimini tanımlayan PreferredWidth Type özelliğini keşfedin.
type: docs
weight: 40
url: /tr/net/aspose.words.tables/preferredwidth/type/
---
## PreferredWidth.Type property

Bu tercih edilen genişlik değeri için kullanılan ölçü birimini alır.

```csharp
public PreferredWidthType Type { get; }
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

* enum [PreferredWidthType](../../preferredwidthtype/)
* class [PreferredWidth](../)
* ad alanı [Aspose.Words.Tables](../../../aspose.words.tables/)
* toplantı [Aspose.Words](../../../)
