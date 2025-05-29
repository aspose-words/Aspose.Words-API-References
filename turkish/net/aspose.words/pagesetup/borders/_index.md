---
title: PageSetup.Borders
linktitle: Borders
articleTitle: Borders
second_title: .NET için Aspose.Words
description: Belgelerinizde cilalı, profesyonel bir görünüm için sayfa kenarlarınıza kolayca erişmek ve bunları özelleştirmek amacıyla PageSetup Borders özelliğini keşfedin.
type: docs
weight: 50
url: /tr/net/aspose.words/pagesetup/borders/
---
## PageSetup.Borders property

Sayfa kenarlıklarının bir koleksiyonunu alır.

```csharp
public BorderCollection Borders { get; }
```

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

* class [BorderCollection](../../bordercollection/)
* class [PageSetup](../)
* ad alanı [Aspose.Words](../../../aspose.words/)
* toplantı [Aspose.Words](../../../)
