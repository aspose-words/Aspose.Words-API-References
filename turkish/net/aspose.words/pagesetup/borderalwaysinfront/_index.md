---
title: PageSetup.BorderAlwaysInFront
linktitle: BorderAlwaysInFront
articleTitle: BorderAlwaysInFront
second_title: Aspose.Words for .NET
description: PageSetup BorderAlwaysInFront mülk. Sayfa kenarlığının kesişen metinlere ve nesnelere göre nereye konumlandırılacağını belirtir C#'da.
type: docs
weight: 20
url: /tr/net/aspose.words/pagesetup/borderalwaysinfront/
---
## PageSetup.BorderAlwaysInFront property

Sayfa kenarlığının kesişen metinlere ve nesnelere göre nereye konumlandırılacağını belirtir.

```csharp
public bool BorderAlwaysInFront { get; set; }
```

## Örnekler

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

* class [PageSetup](../)
* ad alanı [Aspose.Words](../../../aspose.words/)
* toplantı [Aspose.Words](../../../)
