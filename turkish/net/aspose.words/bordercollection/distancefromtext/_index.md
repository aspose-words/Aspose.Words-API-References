---
title: BorderCollection.DistanceFromText
second_title: Aspose.Words for .NET API Referansı
description: BorderCollection mülk. Kenarlığın metinden uzaklığını nokta cinsinden alır veya ayarlar.
type: docs
weight: 40
url: /tr/net/aspose.words/bordercollection/distancefromtext/
---
## BorderCollection.DistanceFromText property

Kenarlığın metinden uzaklığını nokta cinsinden alır veya ayarlar.

```csharp
public double DistanceFromText { get; set; }
```

### Notlar

İlk kenarlık için metinden uzaklığı alır.

Çapraz kenarlıklar hariç, koleksiyondaki tüm kenarlıklar için metinden uzaklığı ayarlar.

Hiçbir etkisi yoktur ve tablo hücrelerinin kenarlıkları otomatik olarak sıfırlanır.

### Örnekler

Gölgeli yeşil dalgalı sayfa kenarlığının nasıl oluşturulacağını gösterir.

```csharp
Document doc = new Document();
PageSetup pageSetup = doc.Sections[0].PageSetup;

pageSetup.Borders.LineStyle = LineStyle.DoubleWave;
pageSetup.Borders.LineWidth = 2;
pageSetup.Borders.Color = Color.Green;
pageSetup.Borders.DistanceFromText = 24;
pageSetup.Borders.Shadow = true;

doc.Save(ArtifactsDir + "PageSetup.PageBorders.docx");
```

### Ayrıca bakınız

* class [BorderCollection](../)
* ad alanı [Aspose.Words](../../bordercollection/)
* toplantı [Aspose.Words](../../../)


