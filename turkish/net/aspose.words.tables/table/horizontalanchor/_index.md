---
title: Table.HorizontalAnchor
linktitle: HorizontalAnchor
articleTitle: HorizontalAnchor
second_title: .NET için Aspose.Words
description: Kayan tablo konumlandırmasını optimize etmek için Table HorizontalAnchor özelliğini keşfedin. Gelişmiş düzen kontrolü için yatay hizalamayı kolayca özelleştirin.
type: docs
weight: 170
url: /tr/net/aspose.words.tables/table/horizontalanchor/
---
## Table.HorizontalAnchor property

Yüzen tablonun yatay konumlandırmasının hesaplanacağı temel nesneyi alır. Varsayılan değerColumn .

```csharp
public RelativeHorizontalPosition HorizontalAnchor { get; set; }
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

* enum [RelativeHorizontalPosition](../../../aspose.words.drawing/relativehorizontalposition/)
* class [Table](../)
* ad alanı [Aspose.Words.Tables](../../../aspose.words.tables/)
* toplantı [Aspose.Words](../../../)
