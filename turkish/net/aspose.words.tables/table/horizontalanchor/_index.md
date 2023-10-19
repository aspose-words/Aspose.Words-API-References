---
title: Table.HorizontalAnchor
linktitle: HorizontalAnchor
articleTitle: HorizontalAnchor
second_title: Aspose.Words for .NET
description: Table HorizontalAnchor mülk. Kayan tablonun yatay konumunun hesaplanması gereken temel nesneyi alır. Varsayılan değerColumn  C#'da.
type: docs
weight: 170
url: /tr/net/aspose.words.tables/table/horizontalanchor/
---
## Table.HorizontalAnchor property

Kayan tablonun yatay konumunun hesaplanması gereken temel nesneyi alır. Varsayılan değer:Column .

```csharp
public RelativeHorizontalPosition HorizontalAnchor { get; set; }
```

## Örnekler

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

* enum [RelativeHorizontalPosition](../../../aspose.words.drawing/relativehorizontalposition/)
* class [Table](../)
* ad alanı [Aspose.Words.Tables](../../../aspose.words.tables/)
* toplantı [Aspose.Words](../../../)
