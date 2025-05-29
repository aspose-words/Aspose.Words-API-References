---
title: Table.VerticalAnchor
linktitle: VerticalAnchor
articleTitle: VerticalAnchor
second_title: .NET için Aspose.Words
description: Yüzen tablo konumlandırmasını optimize etmek için Table VerticalAnchor özelliğini keşfedin. Varsayılan Margin değeriyle düzen denetimini nasıl geliştireceğinizi öğrenin.
type: docs
weight: 340
url: /tr/net/aspose.words.tables/table/verticalanchor/
---
## Table.VerticalAnchor property

Yüzen tablonun dikey konumlandırmasının hesaplanacağı temel nesneyi alır. Varsayılan değerMargin .

```csharp
public RelativeVerticalPosition VerticalAnchor { get; set; }
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

* enum [RelativeVerticalPosition](../../../aspose.words.drawing/relativeverticalposition/)
* class [Table](../)
* ad alanı [Aspose.Words.Tables](../../../aspose.words.tables/)
* toplantı [Aspose.Words](../../../)
