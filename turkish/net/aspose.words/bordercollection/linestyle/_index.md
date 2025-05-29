---
title: BorderCollection.LineStyle
linktitle: LineStyle
articleTitle: LineStyle
second_title: .NET için Aspose.Words
description: Tasarımınızı esnek kenarlık stilleriyle özelleştirmek için BorderCollection LineStyle özelliğini keşfedin. Projenizin görsel çekiciliğini zahmetsizce artırın!
type: docs
weight: 80
url: /tr/net/aspose.words/bordercollection/linestyle/
---
## BorderCollection.LineStyle property

Kenarlık stilini alır veya ayarlar.

```csharp
public LineStyle LineStyle { get; set; }
```

## Notlar

Koleksiyondaki ilk kenarlığın stilini döndürür.

Koleksiyondaki çapraz kenarlıklar hariç tüm kenarlıkların stilini ayarlar.

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

* enum [LineStyle](../../linestyle/)
* class [BorderCollection](../)
* ad alanı [Aspose.Words](../../../aspose.words/)
* toplantı [Aspose.Words](../../../)
