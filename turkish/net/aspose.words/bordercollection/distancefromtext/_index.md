---
title: BorderCollection.DistanceFromText
linktitle: DistanceFromText
articleTitle: DistanceFromText
second_title: .NET için Aspose.Words
description: Tasarımlarınızdaki metinden kenarlık aralığını kolayca özelleştirmek için BorderCollection DistanceFromText özelliğini keşfedin. Düzeninizi zahmetsizce optimize edin!
type: docs
weight: 40
url: /tr/net/aspose.words/bordercollection/distancefromtext/
---
## BorderCollection.DistanceFromText property

Sınırın metinden uzaklığını noktalar halinde alır veya ayarlar.

```csharp
public double DistanceFromText { get; set; }
```

## Notlar

İlk kenarlığın metinden uzaklığını alır.

Koleksiyondaki çapraz kenarlıklar hariç tüm kenarlıklar için metinden uzaklığı ayarlar.

Hiçbir etkisi yoktur ve tablo hücrelerinin sınırları için otomatik olarak sıfırlanır.

## Örnekler

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
* ad alanı [Aspose.Words](../../../aspose.words/)
* toplantı [Aspose.Words](../../../)
