---
title: PageSetup.BottomMargin
second_title: Aspose.Words for .NET API Referansı
description: PageSetup mülk. Sayfanın alt kenarı ile gövde metninin alt sınırı arasındaki mesafeyi nokta cinsinden döndürür veya ayarlar.
type: docs
weight: 80
url: /tr/net/aspose.words/pagesetup/bottommargin/
---
## PageSetup.BottomMargin property

Sayfanın alt kenarı ile gövde metninin alt sınırı arasındaki mesafeyi (nokta cinsinden) döndürür veya ayarlar.

```csharp
public double BottomMargin { get; set; }
```

### Örnekler

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
* ad alanı [Aspose.Words](../../pagesetup/)
* toplantı [Aspose.Words](../../../)


