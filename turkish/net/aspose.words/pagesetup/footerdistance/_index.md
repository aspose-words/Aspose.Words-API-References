---
title: PageSetup.FooterDistance
second_title: Aspose.Words for .NET API Referansı
description: PageSetup mülk. Alt bilgi ile sayfanın altı arasındaki mesafeyi nokta olarak döndürür veya ayarlar.
type: docs
weight: 140
url: /tr/net/aspose.words/pagesetup/footerdistance/
---
## PageSetup.FooterDistance property

Alt bilgi ile sayfanın altı arasındaki mesafeyi (nokta olarak) döndürür veya ayarlar.

```csharp
public double FooterDistance { get; set; }
```

### Örnekler

Bir bölüm için diğer ayarlarla birlikte kağıt boyutunun, yönün, kenar boşluklarının nasıl ayarlanacağını gösterir.

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


