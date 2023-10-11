---
title: PageSetup.ClearFormatting
second_title: Aspose.Words for .NET API Referansı
description: PageSetup yöntem. Sayfa düzenini varsayılan kağıt boyutuna kenar boşluklarına ve yönlendirmeye sıfırlar.
type: docs
weight: 460
url: /tr/net/aspose.words/pagesetup/clearformatting/
---
## PageSetup.ClearFormatting method

Sayfa düzenini varsayılan kağıt boyutuna, kenar boşluklarına ve yönlendirmeye sıfırlar.

```csharp
public void ClearFormatting()
```

### Örnekler

Sayfa yapısı ayarlarının bir belgedeki bölümlere nasıl uygulanacağını ve geri döndürüleceğini gösterir.

```csharp
Document doc = new Document();
DocumentBuilder builder = new DocumentBuilder(doc);

// Oluşturucunun geçerli bölümü için sayfa düzeni özelliklerini değiştirin ve metin ekleyin.
builder.PageSetup.Orientation = Orientation.Landscape;
builder.PageSetup.VerticalAlignment = PageVerticalAlignment.Center;
builder.Writeln("This is the first section, which landscape oriented with vertically centered text.");

// Bir belge oluşturucu kullanarak yeni bir bölüme başlarsak,
// oluşturucunun mevcut sayfa düzeni özelliklerini devralacaktır.
builder.InsertBreak(BreakType.SectionBreakNewPage);

Assert.AreEqual(Orientation.Landscape, doc.Sections[1].PageSetup.Orientation);
Assert.AreEqual(PageVerticalAlignment.Center, doc.Sections[1].PageSetup.VerticalAlignment);

// "ClearFormatting" yöntemini kullanarak sayfa düzeni özelliklerini varsayılan değerlerine döndürebiliriz.
builder.PageSetup.ClearFormatting();

Assert.AreEqual(Orientation.Portrait, doc.Sections[1].PageSetup.Orientation);
Assert.AreEqual(PageVerticalAlignment.Top, doc.Sections[1].PageSetup.VerticalAlignment);

builder.Writeln("This is the second section, which is in default Letter paper size, portrait orientation and top alignment.");

doc.Save(ArtifactsDir + "PageSetup.ClearFormatting.docx");
```

### Ayrıca bakınız

* class [PageSetup](../)
* ad alanı [Aspose.Words](../../pagesetup/)
* toplantı [Aspose.Words](../../../)


