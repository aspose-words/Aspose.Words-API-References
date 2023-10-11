---
title: Table.VerticalAnchor
second_title: Aspose.Words for .NET API Referansı
description: Table mülk. Kayan tablonun dikey konumunun hesaplanması gereken temel nesneyi alır. Varsayılan değerMargin .
type: docs
weight: 340
url: /tr/net/aspose.words.tables/table/verticalanchor/
---
## Table.VerticalAnchor property

Kayan tablonun dikey konumunun hesaplanması gereken temel nesneyi alır. Varsayılan değer:Margin .

```csharp
public RelativeVerticalPosition VerticalAnchor { get; set; }
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

    // HorizontalAnchor ayarlayıcı için RelativeHorizontalPosition'da yalnızca Kenar Boşluğu, Sayfa, Sütun mevcuttur.
    // ArgumentException diğer değerler için atılacak.
    table.HorizontalAnchor = RelativeHorizontalPosition.Column;

    // VerticalAnchor ayarlayıcı için RelativeVerticalPosition'da yalnızca Kenar Boşluğu, Sayfa, Paragraf mevcuttur.
    // ArgumentException diğer değerler için atılacak.
    table.VerticalAnchor = RelativeVerticalPosition.Page;
}
```

### Ayrıca bakınız

* enum [RelativeVerticalPosition](../../../aspose.words.drawing/relativeverticalposition/)
* class [Table](../)
* ad alanı [Aspose.Words.Tables](../../table/)
* toplantı [Aspose.Words](../../../)


