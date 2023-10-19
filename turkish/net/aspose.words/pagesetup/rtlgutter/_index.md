---
title: PageSetup.RtlGutter
linktitle: RtlGutter
articleTitle: RtlGutter
second_title: Aspose.Words for .NET
description: PageSetup RtlGutter mülk. Microsoft Wordün bölüm için cilt paylarını sağdan sola dile mi yoksa soldan sağa dile mi dayalı olarak kullanacağını alır veya ayarlar C#'da.
type: docs
weight: 380
url: /tr/net/aspose.words/pagesetup/rtlgutter/
---
## PageSetup.RtlGutter property

Microsoft Word'ün bölüm için cilt paylarını sağdan sola dile mi, yoksa soldan sağa dile mi dayalı olarak kullanacağını alır veya ayarlar.

```csharp
public bool RtlGutter { get; set; }
```

## Örnekler

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
* ad alanı [Aspose.Words](../../../aspose.words/)
* toplantı [Aspose.Words](../../../)
