---
title: Color
second_title: Aspose.Words for .NET API Referansı
description: Kenarlık rengini alır veya ayarlar.
type: docs
weight: 20
url: /tr/net/aspose.words/bordercollection/color/
---
## BorderCollection.Color property

Kenarlık rengini alır veya ayarlar.

```csharp
public Color Color { get; set; }
```

### Notlar

Koleksiyondaki ilk kenarlığın rengini döndürür.

Çapraz kenarlıklar hariç koleksiyondaki tüm kenarlıkların rengini ayarlar.

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

* class [BorderCollection](../../bordercollection)
* ad alanı [Aspose.Words](../../bordercollection)
* toplantı [Aspose.Words](../../../)

<!-- DO NOT EDIT: generated by xmldocmd for Aspose.Words.dll -->
