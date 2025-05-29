---
title: PageSetup.BorderAppliesTo
linktitle: BorderAppliesTo
articleTitle: BorderAppliesTo
second_title: .NET için Aspose.Words
description: PageSetup BorderAppliesTo özelliğinin, sayfa kenarlığı yazdırmayı kontrol ederek belge düzeninizi nasıl geliştirdiğini ve cilalı, profesyonel bir görünüm sağladığını keşfedin.
type: docs
weight: 30
url: /tr/net/aspose.words/pagesetup/borderappliesto/
---
## PageSetup.BorderAppliesTo property

Sayfa kenarlığının hangi sayfalara yazdırılacağını belirtir.

```csharp
public PageBorderAppliesTo BorderAppliesTo { get; set; }
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

* enum [PageBorderAppliesTo](../../pageborderappliesto/)
* class [PageSetup](../)
* ad alanı [Aspose.Words](../../../aspose.words/)
* toplantı [Aspose.Words](../../../)
