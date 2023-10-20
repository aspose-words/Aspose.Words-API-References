---
title: HtmlSaveOptions.ExportPageSetup
linktitle: ExportPageSetup
articleTitle: ExportPageSetup
second_title: Aspose.Words for .NET
description: HtmlSaveOptions ExportPageSetup mülk. Sayfa düzeninin HTMLye mi MHTMLye mi yoksa EPUBa mı aktarılacağını belirtir. VarsayılanYANLIŞ  C#'da.
type: docs
weight: 220
url: /tr/net/aspose.words.saving/htmlsaveoptions/exportpagesetup/
---
## HtmlSaveOptions.ExportPageSetup property

Sayfa düzeninin HTML'ye mi, MHTML'ye mi yoksa EPUB'a mı aktarılacağını belirtir. Varsayılan:`YANLIŞ` .

```csharp
public bool ExportPageSetup { get; set; }
```

## Notlar

Her biri[`Section`](../../../aspose.words/section/) Aspose.Words belge modelinde sayfa düzeni bilgileri aracılığıyla sağlanır[`PageSetup`](../../../aspose.words/pagesetup/) sınıf. Bir belgeyi HTML formatına aktardığınızda, bu information bilgisini daha sonra kullanmak üzere saklamanız gerekebilir. Özellikle, sayfa düzeni, sayfalanmış ortama (yazdırma) veya daha sonra yerel Microsoft Word dosya biçimlerine (DOCX, DOC, RTF, WML) dönüştürme için önemli olabilir.

Çoğu durumda HTML, sayfalandırmanın yapılmadığı tarayıcılarda görüntülenmek üzere tasarlanmıştır. Dolayısıyla bu feature varsayılan olarak etkin değildir.

## Örnekler

HTML'ye kaydederken bölüm yapısı/sayfa düzeni bilgilerinin korunup korunmayacağına nasıl karar verileceğini gösterir.

```csharp
Document doc = new Document();
DocumentBuilder builder = new DocumentBuilder(doc);

builder.Write("Section 1");
builder.InsertBreak(BreakType.SectionBreakNewPage);
builder.Write("Section 2");

PageSetup pageSetup = doc.Sections[0].PageSetup;
pageSetup.TopMargin = 36.0;
pageSetup.BottomMargin = 36.0;
pageSetup.PaperSize = PaperSize.A5;

// Belgeyi HTML'ye kaydederken bir SaveOptions nesnesi iletebiliriz
// sayfa düzeni ayarlarının korunacağına veya atılacağına karar vermek için.
// "ExportPageSetup" bayrağını "true" olarak ayarlarsak, çıktı HTML belgesi sayfa yapısı yapılandırmamızı içerecektir.
// "ExportPageSetup" bayrağını "false" olarak ayarlarsak, kaydetme işlemi sayfa yapısı ayarlarımızı iptal edecektir
// ilk bölüm için, her iki bölüm de aynı görünecektir.
HtmlSaveOptions options = new HtmlSaveOptions { ExportPageSetup = exportPageSetup };

doc.Save(ArtifactsDir + "HtmlSaveOptions.ExportPageSetup.html", options);

string outDocContents = File.ReadAllText(ArtifactsDir + "HtmlSaveOptions.ExportPageSetup.html");

if (exportPageSetup)
{
    Assert.True(outDocContents.Contains(
        "<style type=\"text/css\">" +
            "@page Section_1 { size:419.55pt 595.3pt; margin:36pt 70.85pt; -aw-footer-distance:35.4pt; -aw-header-distance:35.4pt }" +
            "@page Section_2 { size:612pt 792pt; margin:70.85pt; -aw-footer-distance:35.4pt; -aw-header-distance:35.4pt }" +
            "div.Section_1 { page:Section_1 }div.Section_2 { page:Section_2 }" +
        "</style>"));

    Assert.True(outDocContents.Contains(
        "<div class=\"Section_1\">" +
            "<p style=\"margin-top:0pt; margin-bottom:0pt\">" +
                "<span>Section 1</span>" +
            "</p>" +
        "</div>"));
}
else
{
    Assert.False(outDocContents.Contains("style type=\"text/css\">"));

    Assert.True(outDocContents.Contains(
        "<div>" +
            "<p style=\"margin-top:0pt; margin-bottom:0pt\">" +
                "<span>Section 1</span>" +
            "</p>" +
        "</div>"));
}
```

### Ayrıca bakınız

* class [HtmlSaveOptions](../)
* ad alanı [Aspose.Words.Saving](../../../aspose.words.saving/)
* toplantı [Aspose.Words](../../../)
