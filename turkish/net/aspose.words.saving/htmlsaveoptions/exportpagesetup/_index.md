---
title: ExportPageSetup
second_title: Aspose.Words for .NET API Referansı
description: Sayfa düzeninin HTML MHTML veya EPUBa aktarılıp aktarılmayacağını belirtir. Varsayılanyanlış .
type: docs
weight: 230
url: /tr/net/aspose.words.saving/htmlsaveoptions/exportpagesetup/
---
## HtmlSaveOptions.ExportPageSetup property

Sayfa düzeninin HTML, MHTML veya EPUB'a aktarılıp aktarılmayacağını belirtir. Varsayılan`yanlış` .

```csharp
public bool ExportPageSetup { get; set; }
```

### Notlar

Her biri[`Section`](../../../aspose.words/section) Aspose.Words belge modelinde sayfa kurulum bilgisi aracılığıyla[`PageSetup`](../../../aspose.words/pagesetup) sınıf. Bir belgeyi HTML biçimine dışa aktardığınızda, daha fazla kullanım için bu bilgiyi saklamanız gerekebilir. Özellikle, sayfa düzeni, disk belleği ortamına işleme (yazdırma) veya daha sonra yerel Microsoft Word dosya biçimlerine (DOCX, DOC, RTF, WML) dönüştürme için önemli olabilir.

Çoğu durumda HTML, sayfalandırmanın yapılmadığı tarayıcılarda görüntülenmek üzere tasarlanmıştır. Bu nedenle bu feature varsayılan olarak etkin değildir.

### Örnekler

HTML'ye kaydederken bölüm yapısı/sayfa düzeni bilgilerinin korunup korunmayacağının nasıl kararlaştırılacağını gösterir.

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

// Belgeyi HTML'ye kaydederken SaveOptions nesnesini iletebiliriz
// sayfa kurulum ayarlarının korunup korunmayacağına karar vermek için.
// "ExportPageSetup" bayrağını "true" olarak ayarlarsak, çıktı HTML belgesi sayfa kurulum yapılandırmamızı içerecektir.
// "ExportPageSetup" bayrağını "false" olarak ayarlarsak, kaydetme işlemi sayfa kurulum ayarlarımızı silecektir
// ilk bölüm için ve her iki bölüm de aynı görünecek.
HtmlSaveOptions options = new HtmlSaveOptions { ExportPageSetup = exportPageSetup };

doc.Save(ArtifactsDir + "HtmlSaveOptions.ExportPageSetup.html", options);

string outDocContents = File.ReadAllText(ArtifactsDir + "HtmlSaveOptions.ExportPageSetup.html");

if (exportPageSetup)
{
    Assert.True(outDocContents.Contains(
        "<style type=\"text/css\">" +
            "@page Section1 { size:419.55pt 595.3pt; margin:36pt 70.85pt }" +
            "@page Section2 { size:612pt 792pt; margin:70.85pt }" +
            "div.Section1 { page:Section1 }div.Section2 { page:Section2 }" +
        "</style>"));

    Assert.True(outDocContents.Contains(
        "<div class=\"Section1\">" +
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

* class [HtmlSaveOptions](../../htmlsaveoptions)
* ad alanı [Aspose.Words.Saving](../../htmlsaveoptions)
* toplantı [Aspose.Words](../../../)

<!-- DO NOT EDIT: generated by xmldocmd for Aspose.Words.dll -->
