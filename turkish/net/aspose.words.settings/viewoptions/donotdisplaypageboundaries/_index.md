---
title: DoNotDisplayPageBoundaries
second_title: Aspose.Words for .NET API Referansı
description: Metnin üst kısmı ile sayfanın üst kenarı arasındaki boşluğun görüntülenmesini kapatır.
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

// 3 sayfaya yayılan içeriği ekleyin.
builder.Writeln("Paragraph 1, Page 1.");
builder.InsertBreak(BreakType.PageBreak);
builder.Writeln("Paragraph 2, Page 2.");
builder.InsertBreak(BreakType.PageBreak);
builder.Writeln("Paragraph 3, Page 3.");

// Bir üst bilgi ve bir alt bilgi ekleyin.
builder.MoveToHeaderFooter(HeaderFooterType.HeaderPrimary);
builder.Writeln("This is the header.");
builder.MoveToHeaderFooter(HeaderFooterType.FooterPrimary);
builder.Writeln("This is the footer.");

// Bu belge, birkaç tam sayfalık yer kaplayan az miktarda içerik içeriyor.
// Microsoft Word'ün eski sürümlerinin üstbilgileri atlamasını sağlamak için "DoNotDisplayPageBoundaries" bayrağını "true" olarak ayarlayın,
// altbilgiler ve belgemizi görüntülerken dikey boşlukların çoğu.
// Microsoft Word'ün eski sürümlerini almak için "DoNotDisplayPageBoundaries" bayrağını "false" olarak ayarlayın
// normalde belgemizi görüntülemek için.
doc.ViewOptions.DoNotDisplayPageBoundaries = doNotDisplayPageBoundaries;

doc.Save(ArtifactsDir + "ViewOptions.DisplayPageBoundaries.doc");
```

### Ayrıca bakınız

* class [ViewOptions](../../viewoptions)
* ad alanı [Aspose.Words.Settings](../../viewoptions)
* toplantı [Aspose.Words](../../../)

<!-- DO NOT EDIT: generated by xmldocmd for Aspose.Words.dll -->
