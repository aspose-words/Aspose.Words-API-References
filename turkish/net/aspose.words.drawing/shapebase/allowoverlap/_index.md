---
title: ShapeBase.AllowOverlap
linktitle: AllowOverlap
articleTitle: AllowOverlap
second_title: Aspose.Words for .NET
description: ShapeBase AllowOverlap mülk. Bu şeklin diğer şekillerle örtüşüp çakışmayacağını belirten bir değer alır veya ayarlar C#'da.
type: docs
weight: 10
url: /tr/net/aspose.words.drawing/shapebase/allowoverlap/
---
## ShapeBase.AllowOverlap property

Bu şeklin diğer şekillerle örtüşüp çakışmayacağını belirten bir değer alır veya ayarlar.

```csharp
public bool AllowOverlap { get; set; }
```

## Notlar

Bu özellik Microsoft Word'deki şeklin davranışını etkiler. Aspose.Words bu özelliğin değerini yok sayar.

Bu özellik yalnızca üst düzey şekillere uygulanabilir.

Varsayılan değer:`doğru`.

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

* class [ShapeBase](../)
* ad alanı [Aspose.Words.Drawing](../../../aspose.words.drawing/)
* toplantı [Aspose.Words](../../../)
