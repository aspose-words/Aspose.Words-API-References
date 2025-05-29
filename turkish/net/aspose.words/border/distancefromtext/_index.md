---
title: Border.DistanceFromText
linktitle: DistanceFromText
articleTitle: DistanceFromText
second_title: .NET için Aspose.Words
description: Gelişmiş düzen kontrolü için metin veya sayfa kenarlarından kenarlık aralığını noktalar halinde kolayca ayarlamak üzere Border DistanceFromText özelliğini keşfedin.
type: docs
weight: 20
url: /tr/net/aspose.words/border/distancefromtext/
---
## Border.DistanceFromText property

Kenarlığın metinden veya sayfa kenarından uzaklığını noktalar halinde alır veya ayarlar.

```csharp
public double DistanceFromText { get; set; }
```

## Notlar

Hiçbir etkisi yoktur ve tablo hücrelerinin sınırları için otomatik olarak sıfırlanır.

## Örnekler

İlk sayfanın üst kısmına geniş mavi bantlı bir kenarlığın nasıl oluşturulacağını gösterir.

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
* ad alanı [Aspose.Words](../../../aspose.words/)
* toplantı [Aspose.Words](../../../)
