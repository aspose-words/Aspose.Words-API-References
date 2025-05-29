---
title: Table.AllowOverlap
linktitle: AllowOverlap
articleTitle: AllowOverlap
second_title: .NET için Aspose.Words
description: Yüzen nesnelerin tablonuzun üzerine binip binmeyeceğini kontrol eden Table AllowOverlap özelliğini keşfedin. Daha iyi belge sunumu için düzen esnekliğini artırın.
type: docs
weight: 70
url: /tr/net/aspose.words.tables/table/allowoverlap/
---
## Table.AllowOverlap property

Bir yüzen tablonun, görüntülendiğinde belgedeki diğer yüzen nesnelerin kendi kapsamlarını kaplamasına izin verip vermeyeceğini alır. Varsayılan değer`doğru` .

```csharp
public bool AllowOverlap { get; }
```

## Örnekler

Yüzen tablo özellikleriyle nasıl çalışılacağını gösterir.

```csharp
Document doc = new Document(MyDir + "Table wrapped by text.docx");

Table table = doc.FirstSection.Body.Tables[0];

if (table.TextWrapping == TextWrapping.Around)
{
    Assert.AreEqual(RelativeHorizontalPosition.Margin, table.HorizontalAnchor);
    Assert.AreEqual(RelativeVerticalPosition.Paragraph, table.VerticalAnchor);
    Assert.AreEqual(false, table.AllowOverlap);

    // YatayBağlantı ayarlayıcısı için RelativeHorizontalPosition'da yalnızca Kenar Boşluğu, Sayfa, Sütun kullanılabilir.
    // Diğer tüm değerler için ArgumentException atılacaktır.
    table.HorizontalAnchor = RelativeHorizontalPosition.Column;

    // VerticalAnchor ayarlayıcısı için RelativeVerticalPosition'da yalnızca Kenar Boşluğu, Sayfa, Paragraf kullanılabilir.
    // Diğer tüm değerler için ArgumentException atılacaktır.
    table.VerticalAnchor = RelativeVerticalPosition.Page;
}
```

### Ayrıca bakınız

* class [Table](../)
* ad alanı [Aspose.Words.Tables](../../../aspose.words.tables/)
* toplantı [Aspose.Words](../../../)
