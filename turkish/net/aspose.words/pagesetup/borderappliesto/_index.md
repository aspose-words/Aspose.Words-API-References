---
title: PageSetup.BorderAppliesTo
second_title: Aspose.Words for .NET API Referansı
description: PageSetup mülk. Sayfa kenarlığının hangi sayfalara yazdırılacağını belirtir.
type: docs
weight: 30
url: /tr/net/aspose.words/pagesetup/borderappliesto/
---
## PageSetup.BorderAppliesTo property

Sayfa kenarlığının hangi sayfalara yazdırılacağını belirtir.

```csharp
public PageBorderAppliesTo BorderAppliesTo { get; set; }
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

* enum [PageBorderAppliesTo](../../pageborderappliesto/)
* class [PageSetup](../)
* ad alanı [Aspose.Words](../../pagesetup/)
* toplantı [Aspose.Words](../../../)


