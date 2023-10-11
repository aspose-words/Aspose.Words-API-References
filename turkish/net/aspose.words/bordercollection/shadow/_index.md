---
title: BorderCollection.Shadow
second_title: Aspose.Words for .NET API Referansı
description: BorderCollection mülk. Kenarlığın gölgesi olup olmadığını belirten bir değer alır veya ayarlar.
type: docs
weight: 110
url: /tr/net/aspose.words/bordercollection/shadow/
---
## BorderCollection.Shadow property

Kenarlığın gölgesi olup olmadığını belirten bir değer alır veya ayarlar.

```csharp
public bool Shadow { get; set; }
```

### Notlar

Koleksiyondaki ilk kenarlıktan değeri alır.

Koleksiyondaki çapraz kenarlıklar hariç tüm kenarlıkların değerini ayarlar.

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


