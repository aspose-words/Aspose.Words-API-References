---
title: BorderCollection.Shadow
linktitle: Shadow
articleTitle: Shadow
second_title: .NET için Aspose.Words
description: Tasarımlarınızı geliştirmek için BorderCollection Shadow özelliğini keşfedin. Projelerinizde modern ve şık bir görünüm için kenarlık gölgelerini kolayca kontrol edin!
type: docs
weight: 110
url: /tr/net/aspose.words/bordercollection/shadow/
---
## BorderCollection.Shadow property

Sınırın gölgesi olup olmadığını belirten bir değer alır veya ayarlar.

```csharp
public bool Shadow { get; set; }
```

## Notlar

Koleksiyondaki ilk sınırdan değeri alır.

Koleksiyondaki çapraz kenarlıklar hariç tüm kenarlıklar için değeri ayarlar.

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
