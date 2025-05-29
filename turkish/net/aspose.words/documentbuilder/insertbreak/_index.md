---
title: DocumentBuilder.InsertBreak
linktitle: InsertBreak
articleTitle: InsertBreak
second_title: .NET için Aspose.Words
description: Belgelerinizi DocumentBuilder InsertBreak yöntemiyle zahmetsizce geliştirin; gelişmiş biçimlendirme için özel kesmeleri sorunsuz bir şekilde eklemenize olanak tanır.
type: docs
weight: 260
url: /tr/net/aspose.words/documentbuilder/insertbreak/
---
## DocumentBuilder.InsertBreak method

Belgeye belirtilen türde bir kesme ekler.

```csharp
public void InsertBreak(BreakType breakType)
```

| Parametre | Tip | Tanım |
| --- | --- | --- |
| breakType | BreakType | Eklenecek kesmenin türünü belirtir. |

## Notlar

Belgeye paragraf, sayfa, sütun, bölüm veya satır sonu eklemek için bu yöntemi kullanın.

## Örnekler

DocumentBuilder kullanılarak bir belgede üstbilgi ve altbilgilerin nasıl oluşturulacağını gösterir.

```csharp
Document doc = new Document();
DocumentBuilder builder = new DocumentBuilder(doc);

// İlk, çift ve tek sayfalar için farklı üstbilgi ve altbilgi istediğimizi belirtin.
builder.PageSetup.DifferentFirstPageHeaderFooter = true;
builder.PageSetup.OddAndEvenPagesHeaderFooter = true;

// Başlıkları oluşturun, ardından her başlık türünü görüntülemek için belgeye üç sayfa ekleyin.
builder.MoveToHeaderFooter(HeaderFooterType.HeaderFirst);
builder.Write("Header for the first page");
builder.MoveToHeaderFooter(HeaderFooterType.HeaderEven);
builder.Write("Header for even pages");
builder.MoveToHeaderFooter(HeaderFooterType.HeaderPrimary);
builder.Write("Header for all other pages");

builder.MoveToSection(0);
builder.Writeln("Page1");
builder.InsertBreak(BreakType.PageBreak);
builder.Writeln("Page2");
builder.InsertBreak(BreakType.PageBreak);
builder.Writeln("Page3");

doc.Save(ArtifactsDir + "DocumentBuilder.HeadersAndFooters.docx");
```

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

Başlık stillerini girdi olarak kullanarak bir belgeye İçindekiler Tablosu'nun (TOC) nasıl ekleneceğini gösterir.

```csharp
Document doc = new Document();
DocumentBuilder builder = new DocumentBuilder(doc);

// Belgenin ilk sayfasına bir içerik tablosu ekleyin.
// Tabloyu 1 ila 3 düzey başlıklarına sahip paragrafları alacak şekilde yapılandırın.
// Ayrıca, girişlerini bizi götürecek köprü metinleri olarak ayarlayın
// Microsoft Word'de sol tıklandığında başlığın bulunduğu yere.
builder.InsertTableOfContents("\\o \"1-3\" \\h \\z \\u");
builder.InsertBreak(BreakType.PageBreak);

// Başlık stilleri içeren paragraflar ekleyerek içindekiler tablosunu doldurun.
// 1 ile 3 arasında bir seviyeye sahip her başlık tabloda bir girdi oluşturacaktır.
builder.ParagraphFormat.StyleIdentifier = StyleIdentifier.Heading1;
builder.Writeln("Heading 1");

builder.ParagraphFormat.StyleIdentifier = StyleIdentifier.Heading2;
builder.Writeln("Heading 1.1");
builder.Writeln("Heading 1.2");

builder.ParagraphFormat.StyleIdentifier = StyleIdentifier.Heading1;
builder.Writeln("Heading 2");
builder.Writeln("Heading 3");

builder.ParagraphFormat.StyleIdentifier = StyleIdentifier.Heading2;
builder.Writeln("Heading 3.1");

builder.ParagraphFormat.StyleIdentifier = StyleIdentifier.Heading3;
builder.Writeln("Heading 3.1.1");
builder.Writeln("Heading 3.1.2");
builder.Writeln("Heading 3.1.3");

builder.ParagraphFormat.StyleIdentifier = StyleIdentifier.Heading4;
builder.Writeln("Heading 3.1.3.1");
builder.Writeln("Heading 3.1.3.2");

builder.ParagraphFormat.StyleIdentifier = StyleIdentifier.Heading2;
builder.Writeln("Heading 3.2");
builder.Writeln("Heading 3.3");

// İçindekiler tablosu, güncel bir sonuç göstermek için güncellenmesi gereken bir tür alandır.
doc.UpdateFields();
doc.Save(ArtifactsDir + "DocumentBuilder.InsertToc.docx");
```

### Ayrıca bakınız

* enum [BreakType](../../breaktype/)
* class [DocumentBuilder](../)
* ad alanı [Aspose.Words](../../../aspose.words/)
* toplantı [Aspose.Words](../../../)
