---
title: BorderCollection.Color
linktitle: Color
articleTitle: Color
second_title: .NET için Aspose.Words
description: Tasarımlarınız için kenarlık renklerini kolayca özelleştirmek ve yönetmek için BorderCollection Color özelliğini keşfedin. Canlı seçeneklerle kullanıcı arayüzünüzü geliştirin!
type: docs
weight: 20
url: /tr/net/aspose.words/bordercollection/color/
---
## BorderCollection.Color property

Sınır rengini alır veya ayarlar.

```csharp
public Color Color { get; set; }
```

## Notlar

Koleksiyondaki ilk kenarlığın rengini döndürür.

Koleksiyondaki çapraz kenarlıklar hariç tüm kenarlıkların rengini ayarlar.

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
