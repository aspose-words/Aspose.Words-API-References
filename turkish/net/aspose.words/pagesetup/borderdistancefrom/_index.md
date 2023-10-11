---
title: PageSetup.BorderDistanceFrom
second_title: Aspose.Words for .NET API Referansı
description: PageSetup mülk. Belirtilen sayfa kenarlığının sayfanın kenarından mı yoksa onu çevreleyen metinden mi ölçüldüğünü belirten bir değer alır veya ayarlar.
type: docs
weight: 40
url: /tr/net/aspose.words/pagesetup/borderdistancefrom/
---
## PageSetup.BorderDistanceFrom property

Belirtilen sayfa kenarlığının sayfanın kenarından mı yoksa onu çevreleyen metinden mi ölçüldüğünü belirten bir değer alır veya ayarlar.

```csharp
public PageBorderDistanceFrom BorderDistanceFrom { get; set; }
```

### Örnekler

İlk sayfanın üst kısmında geniş mavi bant kenarlığının nasıl oluşturulacağını gösterir.

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
* ad alanı [Aspose.Words](../../pagesetup/)
* toplantı [Aspose.Words](../../../)


