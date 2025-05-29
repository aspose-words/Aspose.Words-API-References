---
title: PageSetup.VerticalAlignment
linktitle: VerticalAlignment
articleTitle: VerticalAlignment
second_title: .NET için Aspose.Words
description: PageSetup VerticalAlignment özelliğinin, okunabilirliği ve sunumu iyileştirmek için metin hizalamasını ayarlayarak belge düzenini nasıl geliştirdiğini keşfedin.
type: docs
weight: 450
url: /tr/net/aspose.words/pagesetup/verticalalignment/
---
## PageSetup.VerticalAlignment property

Bir belgedeki veya bölümdeki her sayfadaki metnin dikey hizalamasını döndürür veya ayarlar.

```csharp
public PageVerticalAlignment VerticalAlignment { get; set; }
```

## Örnekler

Bir belgedeki bölümlere sayfa düzeni ayarlarının nasıl uygulanacağını ve geri alınacağını gösterir.

```csharp
Document doc = new Document();
DocumentBuilder builder = new DocumentBuilder(doc);

// Oluşturucunun geçerli bölümünün sayfa düzeni özelliklerini değiştirin ve metin ekleyin.
builder.PageSetup.Orientation = Orientation.Landscape;
builder.PageSetup.VerticalAlignment = PageVerticalAlignment.Center;
builder.Writeln("This is the first section, which landscape oriented with vertically centered text.");

// Belge oluşturucuyu kullanarak yeni bir bölüm başlatırsak,
// Oluşturucunun geçerli sayfa düzeni özelliklerini devralacaktır.
builder.InsertBreak(BreakType.SectionBreakNewPage);

Assert.AreEqual(Orientation.Landscape, doc.Sections[1].PageSetup.Orientation);
Assert.AreEqual(PageVerticalAlignment.Center, doc.Sections[1].PageSetup.VerticalAlignment);

// "ClearFormatting" metodunu kullanarak sayfa düzeni özelliklerini varsayılan değerlerine döndürebiliriz.
builder.PageSetup.ClearFormatting();

Assert.AreEqual(Orientation.Portrait, doc.Sections[1].PageSetup.Orientation);
Assert.AreEqual(PageVerticalAlignment.Top, doc.Sections[1].PageSetup.VerticalAlignment);

builder.Writeln("This is the second section, which is in default Letter paper size, portrait orientation and top alignment.");

doc.Save(ArtifactsDir + "PageSetup.ClearFormatting.docx");
```

### Ayrıca bakınız

* enum [PageVerticalAlignment](../../pageverticalalignment/)
* class [PageSetup](../)
* ad alanı [Aspose.Words](../../../aspose.words/)
* toplantı [Aspose.Words](../../../)
