---
title: BorderCollection.LineWidth
linktitle: LineWidth
articleTitle: LineWidth
second_title: .NET için Aspose.Words
description: Tasarımınızın hassasiyetini ve görsel çekiciliğini artırmak için kenarlık genişliğini noktalar halinde kolayca ayarlamak üzere BorderCollection LineWidth özelliğini keşfedin.
type: docs
weight: 90
url: /tr/net/aspose.words/bordercollection/linewidth/
---
## BorderCollection.LineWidth property

Sınır genişliğini noktalar halinde alır veya ayarlar.

```csharp
public double LineWidth { get; set; }
```

## Notlar

Koleksiyondaki ilk kenarlığın genişliğini döndürür.

Koleksiyondaki çapraz kenarlıklar hariç tüm kenarlıkların genişliğini ayarlar.

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
