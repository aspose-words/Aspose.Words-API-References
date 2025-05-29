---
title: PageSetup.Gutter
linktitle: Gutter
articleTitle: Gutter
second_title: .NET için Aspose.Words
description: Belge kenar boşluklarını ciltleme için optimize etmek üzere PageSetup Gutter ayarlarını düzenleyin. Profesyonel sonuçlar için düzeninizi mükemmel kenar boşluklarıyla geliştirin.
type: docs
weight: 160
url: /tr/net/aspose.words/pagesetup/gutter/
---
## PageSetup.Gutter property

Belge bağlama için kenar boşluğuna eklenen ekstra alan miktarını alır veya ayarlar.

```csharp
public double Gutter { get; set; }
```

## Örnekler

Kitap katlaması olarak yazdırılabilecek bir belgenin nasıl yapılandırılacağını gösterir.

```csharp
Document doc = new Document();

// 16 sayfaya yayılacak metni ekleyin.
DocumentBuilder builder = new DocumentBuilder(doc);
builder.Writeln("My Booklet:");

for (int i = 0; i < 15; i++)
{
    builder.InsertBreak(BreakType.PageBreak);
    builder.Write($"Booklet face #{i}");
}

// Belgeyi kitap katlaması biçiminde yazdırmak için ilk bölümün "PageSetup" özelliğini yapılandırın.
// Bu belgeyi her iki tarafa da yazdırdığımızda sayfaları istiflemek için kullanabiliriz
// ve hepsini aynı anda ortadan katlayın. Belgenin içerikleri bir kitap katlaması şeklinde sıralanacaktır.
PageSetup pageSetup = doc.Sections[0].PageSetup;
pageSetup.MultiplePages = MultiplePagesType.BookFoldPrinting;

// Sayfa sayısını yalnızca 4'ün katları şeklinde belirtebiliriz.
pageSetup.SheetsPerBooklet = 4;

doc.Save(ArtifactsDir + "PageSetup.Booklet.docx");
```

Oluk kenar boşluklarının nasıl ayarlanacağını gösterir.

```csharp
Document doc = new Document();

// Birkaç sayfaya yayılan metin ekleyin.
DocumentBuilder builder = new DocumentBuilder(doc);
for (int i = 0; i < 6; i++)
{
    builder.Write("Lorem ipsum dolor sit amet, consectetur adipiscing elit, " +
                  "sed do eiusmod tempor incididunt ut labore et dolore magna aliqua.");
    builder.InsertBreak(BreakType.PageBreak);
}

// Bir oluk, sayfanın sol veya sağ kenar boşluğuna boşluklar ekler,
// Kitabın sayfalarının ortadan katlanmasıyla sayfa düzeninin bozulmasına neden olan bir durumdur.
PageSetup pageSetup = doc.Sections[0].PageSetup;

 // Sayfalarımızın kenar boşluklarında metin için ne kadar alan olacağını belirleyin ve ardından kenar boşluğuna bir miktar boşluk ekleyin.
Assert.AreEqual(470.30d, pageSetup.PageWidth - pageSetup.LeftMargin - pageSetup.RightMargin, 0.01d);

pageSetup.Gutter = 100.0d;

// Sağdan sola yazılan metinler için oluğu daha uygun bir konuma yerleştirmek amacıyla "RtlGutter" özelliğini "true" olarak ayarlayın.
pageSetup.RtlGutter = true;

// "MultiplePages" özelliğini alternatif olarak "MultiplePagesType.MirrorMargins" olarak ayarlayın
// her sayfada kenar boşluklarının sol/sağ sayfa tarafı konumu.
pageSetup.MultiplePages = MultiplePagesType.MirrorMargins;

doc.Save(ArtifactsDir + "PageSetup.Gutter.docx");
```

### Ayrıca bakınız

* class [PageSetup](../)
* ad alanı [Aspose.Words](../../../aspose.words/)
* toplantı [Aspose.Words](../../../)
