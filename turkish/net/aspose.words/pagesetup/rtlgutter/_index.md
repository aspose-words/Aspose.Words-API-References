---
title: PageSetup.RtlGutter
linktitle: RtlGutter
articleTitle: RtlGutter
second_title: .NET için Aspose.Words
description: Microsoft Word'deki PageSetup RtlGutter özelliğinin sağdan sola ve soldan sağa diller için bölüm düzenlerini nasıl optimize ettiğini keşfedin. Belge tasarımınızı geliştirin!
type: docs
weight: 380
url: /tr/net/aspose.words/pagesetup/rtlgutter/
---
## PageSetup.RtlGutter property

Microsoft Word'ün bölüm için sağdan sola veya soldan sağa bir dile dayalı oluklar kullanıp kullanmayacağını alır veya ayarlar.

```csharp
public bool RtlGutter { get; set; }
```

## Örnekler

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
