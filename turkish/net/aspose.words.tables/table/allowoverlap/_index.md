---
title: Table.AllowOverlap
linktitle: AllowOverlap
articleTitle: AllowOverlap
second_title: Aspose.Words for .NET
description: Table AllowOverlap mülk. Bir kayan tablonun belge içindeki diğer kayan nesnelerin görüntülendiğinde kapsamlarıyla çakışmasına izin verip vermeyeceğini alır. Varsayılan değerdoğru  C#'da.
type: docs
weight: 70
url: /tr/net/aspose.words.tables/table/allowoverlap/
---
## Table.AllowOverlap property

Bir kayan tablonun, belge içindeki diğer kayan nesnelerin görüntülendiğinde kapsamlarıyla çakışmasına izin verip vermeyeceğini alır. Varsayılan değer:`doğru` .

```csharp
public bool AllowOverlap { get; }
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

* class [Table](../)
* ad alanı [Aspose.Words.Tables](../../../aspose.words.tables/)
* toplantı [Aspose.Words](../../../)
