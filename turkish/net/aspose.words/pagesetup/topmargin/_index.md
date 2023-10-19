---
title: PageSetup.TopMargin
linktitle: TopMargin
articleTitle: TopMargin
second_title: Aspose.Words for .NET
description: PageSetup TopMargin mülk. Sayfanın üst kenarı ile gövde metninin üst sınırı arasındaki mesafeyi nokta cinsinden döndürür veya ayarlar C#'da.
type: docs
weight: 440
url: /tr/net/aspose.words/pagesetup/topmargin/
---
## PageSetup.TopMargin property

Sayfanın üst kenarı ile gövde metninin üst sınırı arasındaki mesafeyi (nokta cinsinden) döndürür veya ayarlar.

```csharp
public double TopMargin { get; set; }
```

## Örnekler

Bir bölüm için kağıt boyutunun, yönünün, kenar boşluklarının ve diğer ayarların nasıl ayarlanacağını gösterir.

```csharp
Document doc = new Document();
DocumentBuilder builder = new DocumentBuilder(doc);

builder.PageSetup.PaperSize = PaperSize.Legal;
builder.PageSetup.Orientation = Orientation.Landscape;
builder.PageSetup.TopMargin = ConvertUtil.InchToPoint(1.0);
builder.PageSetup.BottomMargin = ConvertUtil.InchToPoint(1.0);
builder.PageSetup.LeftMargin = ConvertUtil.InchToPoint(1.5);
builder.PageSetup.RightMargin = ConvertUtil.InchToPoint(1.5);
builder.PageSetup.HeaderDistance = ConvertUtil.InchToPoint(0.2);
builder.PageSetup.FooterDistance = ConvertUtil.InchToPoint(0.2);

builder.Writeln("Hello world!");

doc.Save(ArtifactsDir + "PageSetup.PageMargins.docx");
```

### Ayrıca bakınız

* class [PageSetup](../)
* ad alanı [Aspose.Words](../../../aspose.words/)
* toplantı [Aspose.Words](../../../)
