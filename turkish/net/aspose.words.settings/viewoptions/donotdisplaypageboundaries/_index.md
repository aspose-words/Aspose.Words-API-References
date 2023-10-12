---
title: ViewOptions.DoNotDisplayPageBoundaries
second_title: Aspose.Words for .NET API Referansı
description: ViewOptions mülk. Metnin üst kısmı ile sayfanın üst kenarı arasındaki boşluğun görüntülenmesini kapatır.
type: docs
weight: 20
url: /tr/net/aspose.words.settings/viewoptions/donotdisplaypageboundaries/
---
## ViewOptions.DoNotDisplayPageBoundaries property

Metnin üst kısmı ile sayfanın üst kenarı arasındaki boşluğun görüntülenmesini kapatır.

```csharp
public bool DoNotDisplayPageBoundaries { get; set; }
```

### Örnekler

Görünüm seçeneklerinde dikey boşlukların ve üstbilgilerin/altbilgilerin nasıl gizleneceğini gösterir.

```csharp
Document doc = new Document();
DocumentBuilder builder = new DocumentBuilder(doc);

// 3 sayfaya yayılan içerik ekleyin.
builder.Writeln("Paragraph 1, Page 1.");
builder.InsertBreak(BreakType.PageBreak);
builder.Writeln("Paragraph 2, Page 2.");
builder.InsertBreak(BreakType.PageBreak);
builder.Writeln("Paragraph 3, Page 3.");

// Bir üstbilgi ve bir altbilgi ekleyin.
builder.MoveToHeaderFooter(HeaderFooterType.HeaderPrimary);
builder.Writeln("This is the header.");
builder.MoveToHeaderFooter(HeaderFooterType.FooterPrimary);
builder.Writeln("This is the footer.");

// Bu belge, birkaç tam sayfalık yer kaplayan az miktarda içerik içeriyor.
// Microsoft Word'ün eski sürümlerinin başlıkları atlaması için "DoNotDisplayPageBoundaries" bayrağını "true" olarak ayarlayın,
// altbilgiler ve belgemizi görüntülerken dikey boşlukların çoğu.
// Microsoft Word'ün eski sürümlerini almak için "DoNotDisplayPageBoundaries" bayrağını "false" olarak ayarlayın
// belgemizi normal şekilde görüntülemek için.
doc.ViewOptions.DoNotDisplayPageBoundaries = doNotDisplayPageBoundaries;

doc.Save(ArtifactsDir + "ViewOptions.DisplayPageBoundaries.doc");
```

### Ayrıca bakınız

* class [ViewOptions](../)
* ad alanı [Aspose.Words.Settings](../../viewoptions/)
* toplantı [Aspose.Words](../../../)


