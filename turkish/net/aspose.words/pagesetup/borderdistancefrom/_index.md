---
title: PageSetup.BorderDistanceFrom
linktitle: BorderDistanceFrom
articleTitle: BorderDistanceFrom
second_title: .NET için Aspose.Words
description: Hassas belge biçimlendirmesi için sayfa kenarlığı ölçülerini kontrol etmek üzere PageSetup BorderDistanceFrom özelliğini keşfedin. Düzeninizi bugün geliştirin!
type: docs
weight: 40
url: /tr/net/aspose.words/pagesetup/borderdistancefrom/
---
## PageSetup.BorderDistanceFrom property

Belirtilen sayfa kenarlığının sayfanın kenarından mı yoksa onu çevreleyen metinden mi ölçüldüğünü gösteren bir değer alır veya ayarlar.

```csharp
public PageBorderDistanceFrom BorderDistanceFrom { get; set; }
```

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

* enum [PageBorderDistanceFrom](../../pageborderdistancefrom/)
* class [PageSetup](../)
* ad alanı [Aspose.Words](../../../aspose.words/)
* toplantı [Aspose.Words](../../../)
