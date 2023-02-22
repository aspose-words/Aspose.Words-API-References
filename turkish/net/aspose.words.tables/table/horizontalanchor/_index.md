---
title: Table.HorizontalAnchor
second_title: Aspose.Words for .NET API Referansı
description: Table mülk. Kayan tablonun yatay konumunun hesaplanması gereken temel nesneyi alır. Varsayılan değerColumn .
type: docs
weight: 170
url: /tr/net/aspose.words.tables/table/horizontalanchor/
---
## Table.HorizontalAnchor property

Kayan tablonun yatay konumunun hesaplanması gereken temel nesneyi alır. Varsayılan değerColumn .

```csharp
public RelativeHorizontalPosition HorizontalAnchor { get; set; }
```

### Örnekler

Kayan tablo özellikleriyle nasıl çalışılacağını gösterir.

```csharp
Document doc = new Document(MyDir + "Table wrapped by text.docx");

Table table = doc.FirstSection.Body.Tables[0];

if (table.TextWrapping == TextWrapping.Around)
{
    Assert.AreEqual(RelativeHorizontalPosition.Margin, table.HorizontalAnchor);
    Assert.AreEqual(RelativeVerticalPosition.Paragraph, table.VerticalAnchor);
    Assert.AreEqual(false, table.AllowOverlap);

    // HorizontalAnchor ayarlayıcı için RelativeHorizontalPosition'da yalnızca Margin, Page, Column kullanılabilir.
    // Diğer değerler için ArgumentException oluşturulacak.
    table.HorizontalAnchor = RelativeHorizontalPosition.Column;

    // VerticalAnchor ayarlayıcı için RelativeVerticalPosition'da yalnızca Kenar Boşluğu, Sayfa, Paragraf kullanılabilir.
    // Diğer değerler için ArgumentException oluşturulacak.
    table.VerticalAnchor = RelativeVerticalPosition.Page;
}
```

### Ayrıca bakınız

* enum [RelativeHorizontalPosition](../../../aspose.words.drawing/relativehorizontalposition/)
* class [Table](../)
* ad alanı [Aspose.Words.Tables](../../table/)
* toplantı [Aspose.Words](../../../)


