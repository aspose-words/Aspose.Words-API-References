---
title: PageSetup.HeaderDistance
linktitle: HeaderDistance
articleTitle: HeaderDistance
second_title: .NET için Aspose.Words
description: Belgenizin düzenini daha iyi okunabilirlik ve sunum için geliştirmek amacıyla, başlık aralıklarını noktalar halinde özelleştirmek üzere PageSetup HeaderDistance özelliğini ayarlayın.
type: docs
weight: 170
url: /tr/net/aspose.words/pagesetup/headerdistance/
---
## PageSetup.HeaderDistance property

Başlık ile sayfanın üstü arasındaki mesafeyi (nokta cinsinden) döndürür veya ayarlar.

```csharp
public double HeaderDistance { get; set; }
```

## Örnekler

Bir bölüm için kağıt boyutunun, yönlendirmenin, kenar boşluklarının ve diğer ayarların nasıl ayarlanacağını gösterir.

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
