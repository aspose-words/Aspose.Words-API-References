---
title: PageSetup.Gutter
second_title: Aspose.Words for .NET API Referansı
description: PageSetup mülk. Belge ciltleme için kenar boşluğuna eklenen ekstra alan miktarını alır veya ayarlar.
type: docs
weight: 160
url: /tr/net/aspose.words/pagesetup/gutter/
---
## PageSetup.Gutter property

Belge ciltleme için kenar boşluğuna eklenen ekstra alan miktarını alır veya ayarlar.

```csharp
public double Gutter { get; set; }
```

### Örnekler

Kitap katlaması olarak yazdırılabilecek bir belgenin nasıl yapılandırılacağını gösterir.

```csharp
Document doc = new Document();

// 16 sayfaya yayılan metni ekleyin.
DocumentBuilder builder = new DocumentBuilder(doc);
builder.Writeln("My Booklet:");

for (int i = 0; i < 15; i++)
{
    builder.InsertBreak(BreakType.PageBreak);
    builder.Write($"Booklet face #{i}");
}

// Belgeyi kitap katlama biçiminde yazdırmak için ilk bölümün "PageSetup" özelliğini yapılandırın.
// Bu belgeyi her iki tarafa da yazdırdığımızda sayfaları istiflemek için alabiliriz
// ve hepsini aynı anda ortadan katlayın. Belgenin içeriği bir kitap katlama şeklinde sıralanacaktır.
PageSetup pageSetup = doc.Sections[0].PageSetup;
pageSetup.MultiplePages = MultiplePagesType.BookFoldPrinting;

// Sayfa sayısını yalnızca 4'ün katları olarak belirtebiliriz.
pageSetup.SheetsPerBooklet = 4;

doc.Save(ArtifactsDir + "PageSetup.Booklet.docx");
```

Cilt payı marjlarının nasıl ayarlanacağını gösterir.

```csharp
Document doc = new Document();

// Birkaç sayfaya yayılan metni ekleyin.
DocumentBuilder builder = new DocumentBuilder(doc);
for (int i = 0; i < 6; i++)
{
    builder.Write("Lorem ipsum dolor sit amet, consectetur adipiscing elit, " +
                  "sed do eiusmod tempor incididunt ut labore et dolore magna aliqua.");
    builder.InsertBreak(BreakType.PageBreak);
}

// Cilt payı, sayfanın sol veya sağ kenar boşluğuna boşluklar ekler,
// bu, sayfa düzenini ihlal eden bir kitaptaki sayfaların ortadan katlanmasını telafi eder.
PageSetup pageSetup = doc.Sections[0].PageSetup;

// Sayfalarımızın kenar boşluklarında metin için ne kadar alana sahip olduğunu belirleyin ve ardından kenar boşluğunu doldurmak için bir miktar ekleyin.
Assert.AreEqual(470.30d, pageSetup.PageWidth - pageSetup.LeftMargin - pageSetup.RightMargin, 0.01d);

pageSetup.Gutter = 100.0d;

// Sağdan sola metin için cilt payını daha uygun bir konuma yerleştirmek amacıyla "RtlGutter" özelliğini "true" olarak ayarlayın.
pageSetup.RtlGutter = true;

// Alternatif olarak "MultiplePages" özelliğini "MultiplePagesType.MirrorMargins" olarak ayarlayın
// her sayfada kenar boşluklarının sol/sağ sayfa tarafı konumu.
pageSetup.MultiplePages = MultiplePagesType.MirrorMargins;

doc.Save(ArtifactsDir + "PageSetup.Gutter.docx");
```

### Ayrıca bakınız

* class [PageSetup](../)
* ad alanı [Aspose.Words](../../pagesetup/)
* toplantı [Aspose.Words](../../../)


