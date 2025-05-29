---
title: ShapeBase.AllowOverlap
linktitle: AllowOverlap
articleTitle: AllowOverlap
second_title: .NET için Aspose.Words
description: ShapeBase AllowOverlap özelliğini keşfedin, diğer şekillerle örtüşmeyi etkinleştirerek veya devre dışı bırakarak şekil etkileşimlerini kontrol edin ve böylece tasarım esnekliğini artırın.
type: docs
weight: 10
url: /tr/net/aspose.words.drawing/shapebase/allowoverlap/
---
## ShapeBase.AllowOverlap property

Bu şeklin diğer şekillerle örtüşüp örtüşmeyeceğini belirten bir değer alır veya ayarlar.

```csharp
public bool AllowOverlap { get; set; }
```

## Notlar

Bu özellik Microsoft Word'deki şeklin davranışını etkiler. Aspose.Words bu özelliğin değerini yoksayar.

Bu özellik yalnızca en üst seviye şekillere uygulanabilir.

Varsayılan değer:`doğru`.

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

* class [ShapeBase](../)
* ad alanı [Aspose.Words.Drawing](../../../aspose.words.drawing/)
* toplantı [Aspose.Words](../../../)
