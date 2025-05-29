---
title: HtmlSaveOptions.ExportPageSetup
linktitle: ExportPageSetup
articleTitle: ExportPageSetup
second_title: .NET için Aspose.Words
description: HtmlSaveOptions ExportPageSetup özelliğinin, daha iyi çıktı için özelleştirilebilir sayfa kurulumlarına izin vererek HTML, MHTML veya EPUB dışa aktarma işlemlerinizi nasıl geliştirdiğini keşfedin.
type: docs
weight: 220
url: /tr/net/aspose.words.saving/htmlsaveoptions/exportpagesetup/
---
## HtmlSaveOptions.ExportPageSetup property

Sayfa düzeninin HTML, MHTML veya EPUB'a aktarılıp aktarılmayacağını belirtir. Varsayılan`YANLIŞ` .

```csharp
public bool ExportPageSetup { get; set; }
```

## Notlar

Her biri[`Section`](../../../aspose.words/section/) Aspose.Words belge modelinde sayfa kurulumu bilgisi yoluyla sağlanır[`PageSetup`](../../../aspose.words/pagesetup/) sınıf. Bir belgeyi HTML biçimine aktardığınızda bu bilgiyi daha sonraki kullanımlar için saklamanız gerekebilir . Özellikle, sayfa düzeni sayfalı medyaya işleme (yazdırma) veya daha sonra yerel Microsoft Word dosya biçimlerine (DOCX, DOC, RTF, WML) dönüştürme için önemli olabilir.

Çoğu durumda HTML, sayfalamanın gerçekleştirilmediği tarayıcılarda görüntülenmek üzere tasarlanmıştır. Bu nedenle bu feature varsayılan olarak etkin değildir.

## Örnekler

HTML'e kaydederken bölüm yapısının/sayfa kurulum bilgilerinin korunup korunmayacağına nasıl karar verileceğini gösterir.

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

// Belgeyi HTML'e kaydederken SaveOptions nesnesini geçirebiliriz
// sayfa düzeni ayarlarının korunup korunmayacağına karar vermek için.
// "ExportPageSetup" bayrağını "true" olarak ayarlarsak, çıktı HTML belgesi sayfa kurulum yapılandırmamızı içerecektir.
// "ExportPageSetup" bayrağını "false" olarak ayarlarsak, kaydetme işlemi sayfa düzeni ayarlarımızı atacaktır
// ilk bölüm için ve her iki bölüm de aynı görünecektir.
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
