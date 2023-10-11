---
title: Border.DistanceFromText
second_title: Aspose.Words for .NET API Referansı
description: Border mülk. Kenarlığın metinden veya sayfa kenarından nokta cinsinden mesafesini alır veya ayarlar.
type: docs
weight: 20
url: /tr/net/aspose.words/border/distancefromtext/
---
## Border.DistanceFromText property

Kenarlığın metinden veya sayfa kenarından nokta cinsinden mesafesini alır veya ayarlar.

```csharp
public double DistanceFromText { get; set; }
```

### Notlar

Hiçbir etkisi yoktur ve tablo hücrelerinin sınırları otomatik olarak sıfırlanır.

### Örnekler

İlk sayfanın üst kısmında geniş mavi bant kenarlığının nasıl oluşturulacağını gösterir.

```csharp
Document doc = new Document();

PageSetup pageSetup = doc.Sections[0].PageSetup;
pageSetup.BorderAlwaysInFront = false;
pageSetup.BorderDistanceFrom = PageBorderDistanceFrom.PageEdge;
pageSetup.BorderAppliesTo = PageBorderAppliesTo.FirstPage;

Border border = pageSetup.Borders[BorderType.Top];
border.LineStyle = LineStyle.Single;
border.LineWidth = 30;
border.Color = Color.Blue;
border.DistanceFromText = 0;

doc.Save(ArtifactsDir + "PageSetup.PageBorderProperties.docx");
```

### Ayrıca bakınız

* class [Border](../)
* ad alanı [Aspose.Words](../../border/)
* toplantı [Aspose.Words](../../../)


