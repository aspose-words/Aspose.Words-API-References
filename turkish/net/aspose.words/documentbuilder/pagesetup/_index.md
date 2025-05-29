---
title: DocumentBuilder.PageSetup
linktitle: PageSetup
articleTitle: PageSetup
second_title: .NET için Aspose.Words
description: Belge biçimlendirmenizi ve düzen verimliliğinizi artırmak için geçerli sayfa ve bölüm ayarlarına erişmek üzere DocumentBuilder PageSetup özelliğini keşfedin.
type: docs
weight: 160
url: /tr/net/aspose.words/documentbuilder/pagesetup/
---
## DocumentBuilder.PageSetup property

Geçerli sayfa düzenini ve bölüm özelliklerini temsil eden bir nesne döndürür.

```csharp
public PageSetup PageSetup { get; }
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

* class [PageSetup](../../pagesetup/)
* class [DocumentBuilder](../)
* ad alanı [Aspose.Words](../../../aspose.words/)
* toplantı [Aspose.Words](../../../)
